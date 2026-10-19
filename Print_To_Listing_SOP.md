# SOP: From Print File to Product Listing

Covers the path from Cody's Bambu print file to a draft Shopify listing: batch slicing, the 3DPrintForce
CSV, photos, and the listing build. Listing rules (titles, copy, packs, SKUs, images) live in `CLAUDE.md`
and the four `Gold_Standard_*.docx` files; this SOP only covers the steps around them.

Scripts live in this repo's `scripts/` folder. They read Cody's files from
`G:\Other computers\My Mac\The_Beat_Drop\Sprout Designs\` and write to `C:\Users\DATA A\Desktop\Sliced Exports\`,
never into the repo.

## Cody (designer)

1. Save the Bambu project in the correct folder under `Sprout Designs\` on the Mac: `ARTISTS\[Artist]\`, `Festivals\[Event]\`, or `Generic\`.
2. Name the file `V# [Artist/Event] - [Design]`, e.g. `V1 Boo Seattle - Spider.3mf`.
3. Fill one **stock plate** per colorway with the design. Other plates (coloring, preview) are fine; they're ignored.
4. Let the Mac sync to Google Drive, then say which file or folder is new.

## Slicing

5. Close Bambu Studio.
6. Open PowerShell in this repo folder and slice only the new folder:
   ```bash
   python scripts\batch_slice.py "Festivals\Boo Seattle"
   ```
   Files Cody changed since their last slice are not re-sliced automatically yet; delete that file's sliced plates in `Sliced Exports` first.
7. Open `Desktop\Sliced Exports\_slice_log.csv` and check the rows for that file:
   - **ok**: done.
   - **empty**: ignore.
   - **FAILED** on a stock plate: send Cody the *note* text. Failures on coloring plates or *"outside of the printable area"* can be ignored (see below).

## Data (with Claude)

8. Tell Claude: *"New sliced files in Sliced Exports\[folder]. Run intake."*
9. Claude returns, for review: product code (existing or proposed), design name, colorways, SKUs, and the 3DPrintForce row (print time, grams per color, printer, quantity per stock plate).
10. Approve any new code and correct colorway names if needed.
11. Claude builds the 3DPrintForce CSV (one row per stock plate = one colorway, time and grams per piece):
    ```bash
    python scripts\make_3dpf_csv.py "Festivals\Boo Seattle" --prefix "BOO Seattle" --code BSBD1
    ```
    Output: `Desktop\Sliced Exports\3DPrintForce_<name>.csv` plus a `_plates.csv` with every plate's totals.
12. **Karol** uploads the CSV to 3DPrintForce and confirms pricing per sales channel.

## Printing and photos

13. Print the stock plates.
14. Shoot photos. Kandi: mostly charms only (each design, each color, the pack as a bunch in a bowl or cup), at most 1–2 shots on a display bracelet.
15. Archive the full shoot in `G:\My Drive\📸 Product Photos\[Name]\`.
16. Copy the photos for the listing into this repo's flat `IMGs/` folder. Give each listing's set a shared filename prefix (the text before the last `_`), e.g. `Hex_Kandi_Witch_0001.jpg`; Claude uploads every file with a matching prefix and never renames them.

## Listing

17. Send Claude the prompt from `Intake_Spec_Single_Listing.md` (one listing) or `BATCH_LISTING.md` (several).
18. Claude builds the **DRAFT** in Shopify, the build summary `.docx`, and the `Platform_Reference.xlsx` updates, following `CLAUDE.md`.
19. **Karol** reviews and publishes.
20. Claude commits each update; push from GitHub Desktop.

## One-time: fill 3DPrintForce for the whole back catalog

21. Set the PC to never sleep, then run `python scripts\batch_slice.py` with no folder name. It takes about 6–12 hours; if it stops, run it again and it skips plates already done.
22. Tell Claude: *"Full slice done, build the 3DPrintForce bulk CSV."* Claude runs `python scripts\make_3dpf_all.py`, which writes `3DPrintForce_ALL.csv` (one row per design + colorway), `_plates.csv` (every plate) and `_codes.csv` (code family per folder, existing vs proposed) to `Desktop\Sliced Exports`.

## Notes

- Sliced files go to `Desktop\Sliced Exports\` in the same folder structure as `Sprout Designs`. Cody's originals are never changed.
- Each plate is sliced separately (`[file]_plate_[N].gcode.3mf`), because slicing all plates at once fails on any empty plate.
- Only 9 of 427 project files had slice data saved inside them (checked 2026-10-14), so slicing is needed for print time and grams.

## How Cody's Bambu files work (confirmed with Cody, 2026-10-16)

- **Versions:** the highest V# is the reliable one (V3 > V2 > V1). Older versions are superseded; the CSV scripts use only the latest version of each design.
- **Plates:** each file has several plates. **Stock plates** are filled up with one design in one colorway; those are what get printed and what the CSV uses (one row per stock plate). Other plates are used to color the design or preview it and are never printed.
- **Target stock:** one full stock plate per colorway. Batch size varies with the design's size.
- **Settings:** once a stock plate is filled, settings don't change. Print time varies by plate. The current preset is **"TBD Default"** (0.2 mm layers, 7% infill, 2 walls). Older files use SUNLU / X1C presets from before that preset existed, when Cody changed printer settings by hand.
- **Filament:** "NEW SILK SETTINGS" is Cody's custom silk profile (shown as "Custom, PLA Silk" in the CSV). Colors can't be preloaded by name in Bambu; Cody picks them from the color wheel, so colorway names are matched from the hex code.
- **Empty plates:** ignore.
- **Slicer errors that don't matter:** *"G-code outside of the printable area"* is usually the purge tower hanging off the plate (not a printable object) or a coloring plate Cody never prints. Cody ignores these in Bambu Studio, and so do we.
- **Real gaps:** `_cody_fix_list.csv` lists only stock plates of the latest version that failed and have no sliced stock plate to replace them (38 plates in 28 files on 2026-10-16, mostly *"Invalid parameter value(s)"* from the older presets).
