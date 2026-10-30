# The Beat Drop — Claude Operating Instructions (Shopify Listings)

*Enforceable rulebook for every Shopify listing task. Read `the-beat-drop-brand-identity.md` first for the "why." Listing copy lives ONLY in the four gold-standard `.docx` files (the Neon Retro set). This file holds structure, rules and process, never template wording. The owner (Karol) can override any rule for a single listing in the prompt.*

---

## Store & Scope

- **Store:** thebeatdrop.myshopify.com · **Account:** admin@thebeatdrop.store · **Claude builds Shopify listings only.** Etsy and TikTok listings are managed elsewhere. Two exceptions: Claude picks the Etsy tags and writes them into the Shopify **Tags** field, and fills the two TikTok metafields that the TikTok sync app sends to TikTok Shop (see TikTok Metafields).
- **Theme template:** `gp-template-581878106541785827` on every new listing. Never Shopify's default.
- **Prompt format:** `Intake_Spec_Single_Listing.md` (one listing) or `BATCH_LISTING.md` (several). Everything Claude needs is in the prompt plus this file.

---

## Critical Rules

1. **DRAFT only.** Never set ACTIVE, never publish. Claude drafts; a human publishes.
2. **Never write "The Beat Drop"** in a title, description, SEO title, meta description or alt text.
3. **Banned → required words (customer-facing):** "cheap"/"knockoff" → omit · "devotees" → "fans" · "variants" (meaning colors) → "colors"/"multi-color" in Claude's own wording; labels written in the gold standards stay as written · "fit" → "outfit"/"clothing".
4. **No artist, festival or event names in customer-facing copy** (title, description, SEO title, meta, alt text, tags). The gold standards are generic; `[Design]` describes the artwork only. No disclaimer sentences, never the word "official," nothing implying licensed or official merch. The name in the prompt's first line is internal (Product Type, SKU code, Roster).
5. **Copy follows the line's gold standard** word for word, except the wording that describes the artwork, which is rewritten for the listing's Design (see Gold Standards & Copy).
6. **The prompt beats the defaults.** If the prompt specifies a variant structure, price, inventory or code that differs from this file, build exactly what the prompt says.
7. **Live SKUs beat convention.** If an existing live SKU conflicts with the SKU convention, match it. Never "fix" it silently.
8. **Required from the prompt (no defaults exist):** the product line; Design; the color-to-image map (Sprout, Kandi Charm) or the featured image (bundles); prices for Sprout Bundles and Kandi Bundles; pack naming for Sprout Bundles. A Design that contains an artist, festival or event name counts as missing. If any is missing, ask **once, up front, for the whole batch**. Never stop mid-build.
9. **Everything else: don't block.** Use the documented default or Claude's own call, finish the build, and record the decision in the build summary and the Product Roster Notes column.

---

## Product Lines

| Line | Physical build | Gold standard (`.docx`) | Category | Variant options |
|---|---|---|---|---|
| Sprout | Charm + K-Hole + Sprocket + metal spring clip, one design | `Neon Retro Rave Sprout Hair Clips \| Festival Hair Clips` | Hair Pins | Color + Pack Size |
| Sprout Bundle | Same build, themed multi-design set, no colors | `Neon Retro Rave Sprout Bundle \| Festival Hair Clip Set` | Hair Pins | Pack Size |
| Kandi Charm | Clip-less charm with K-Hole bead hole and Sprocket spring pocket, one design | `Neon Retro TV Rave Kandi Charm \| 3D Printed Bead` | Charms | Color + Pack Size |
| Kandi Bundle | Same charm build, variety of designs, no colors | `Neon Retro Rave Kandi Bundle \| Festival Bead Charms` | Charms | Pack Size |

**Product Type: Claude works it out.** Use the exact live spelling:
- Kandi Charm or Kandi Bundle → `Kandi Beads`
- A festival or event is the subject → `Festival Sprouts`
- Everything else → `Artist Sprout`

State the choice in the build summary. `Rave Sprout` is a legacy type; never assign it.

**Collections: Claude assigns none.** Smart collections pick listings up from Product Type and Pack Size. The owner adds manual collections before publishing.

**Category paths:** Hair Pins = `Apparel & Accessories > Clothing Accessories > Hair Accessories > Hair Pins, Claws & Clips` · Charms = `Apparel & Accessories > Jewelry > Charms & Pendants > Charms`

---

## Gold Standards & Copy

Each line's gold standard (see Product Lines) is a finished example listing from the Neon Retro set, with Keyword Strategy, Shopify, Etsy and TikTok Shop sections. They are worked examples, not fill-in templates:
- **Copy them section by section.** Rewrite only the wording that describes the artwork (the example's neon, arcade, retro, pixel, geometric or TV wording, and the first bullet's label and text) to fit the listing's Design. Every other sentence and every other bullet stays word for word, in the same order.
- **Shopify body** = the example's Shopify section: one intro paragraph, then its 4 bullets as `Label: text`. HTML `<p>` then `<ul><li>`; bold nothing the `.docx` doesn't bold. Never manual bullet characters (●, •).
- **Kandi:** never imply a bracelet is included, in any field.
- **Keyword Strategy and Etsy sections** are reference only. Etsy listings are built outside Claude Code; Etsy tags follow the Etsy Tags section below.

---

## Titles & SEO

**`[Design]`** comes from the prompt: a plain description of the artwork (e.g. "Pixel Skull", "Halloween Mix"), never an artist, festival or event name.

| Line | Product title (≤140) | SEO title (≤60) | Meta description (≤160) |
|---|---|---|---|
| Sprout | `[Design] Rave Sprout Hair Clips \| Festival Hair Clips` | `[Design] Rave Sprout Clips \| Festival Hair Clips` | The example's meta, design words swapped |
| Sprout Bundle | `[Design] Rave Sprout Bundle \| Festival Hair Clip Set` | `[Design] Rave Sprout Bundle \| Festival Hair Clips` | The example's meta, design words swapped |
| Kandi Charm | `[Design] Rave Kandi Charm \| 3D Printed Bead` | `[Design] Kandi Charm \| Rave Bead Charm` | The example's meta, design words swapped |
| Kandi Bundle | `[Design] Rave Kandi Charms \| 3D Printed Beads` | `[Design] Kandi Charms \| Rave Bead Bundle` | The example's meta, design words swapped |

- These follow each gold standard's Shopify section; if a `.docx` changes, it wins over this table.
- **Over a limit:** shorten `[Design]`.
- **Alt text:** `[Design] rave sprout|rave kandi charm [color] — [brief descriptor]`. Bundles use `[Design] rave sprout bundle|kandi charm bundle — [brief descriptor]`. Never pack sizes or names. A photo showing a bracelet says "shown on a display bracelet (not included)."

---

## TikTok Metafields

The TikTok sync app sends two product metafields to TikTok Shop. Fill both on every listing Claude builds or finishes.

| Metafield | Namespace.key | Type |
|---|---|---|
| TikTok Title | `custom.tiktok_title` | single line text |
| TikTok Description | `custom.tiktok_description` | multi-line text (plain text, no HTML) |

**Source:** the **TikTok Shop** section of the line's gold standard (see Product Lines).

**TikTok Title** (≤255; keep under 100): the example's title with its design words ("Neon Arcade", "Neon Retro TV") replaced by `[Design]`:

| Line | Pattern |
|---|---|
| Sprout | `[Design] Rave Sprout Hair Clips, 3D Printed Festival Hair Accessories` |
| Sprout Bundle | `[Design] Rave Sprout Hair Clip Bundle, 3D Printed Festival Hair Accessories Set` |
| Kandi Charm | `[Design] Rave Kandi Charm, 3D Printed Bead for Bracelets & Festival Jewelry` |
| Kandi Bundle | `[Design] Rave Kandi Charms, 3D Printed Beads for Bracelets & Festival Jewelry` |

**TikTok Description** (≤1,000 characters):
- Keep the example's structure: a 3–4 sentence intro, then its 5 bullets with the same labels in the same order.
- Rewrite only what describes the artwork (the example's neon, arcade, pixel, retro TV wording, and the first bullet's label and text) to fit this listing's Design. Every other sentence and bullet stays word for word.
- Format: the intro paragraph, one blank line, then one line per bullet starting `• ` (e.g. `• Lightweight PLA: 3D-printed decorative charms.`). No HTML, headings or emoji.
- Same limits as the rest of the listing: no artist, festival or event names, no "The Beat Drop," no "official," no unfilled placeholders such as `[Colors]`. Kandi descriptions never imply a bracelet is included.

**Write and confirm:** set both with `metafieldsSet` when creating or finishing the draft, then read the product back and confirm both values before handoff, the same way as tags.

---

## Variants, Pricing & Inventory

Every pack above 1 includes a **FREE bonus of the same product**: Sprouts get bonus sprouts, Kandi gets bonus kandi charms. The `+ (N FREE)` pack names say it; copy never promises a different product as the bonus.

| Line | Pack names | Default prices | Default inventory |
|---|---|---|---|
| Sprout | `[Color] / 1 Pack` · `[Color] / 10 Pack + (1 FREE)` · `20 Pack + (2 FREE)` · `30 Pack + (3 FREE)` | $3 / $28 / $55 / $81 | 200 / 100 / 50 / 10 |
| Kandi Charm | `[Color] / 10 Pack + (1 FREE)` · `20 Pack + (2 FREE)` · `30 Pack + (3 FREE)` (**no 1 Pack**) | $23 / $45 / $67 | 100 / 50 / 10 per color |
| Sprout Bundle | "Pack" → `10 Pack + (1 FREE)`… or "Sprout Bundle" → `10 Sprout Bundle + (1 FREE)`… (from the prompt) | From the prompt | 100 / 50 / 10 |
| Kandi Bundle | Always "Pack": `10 Pack + (1 FREE)` · `20 Pack + (2 FREE)` · `30 Pack + (3 FREE)` | From the prompt | 100 / 50 / 10 |

- Sprout: Multicolor never gets a 1 Pack. 25/40/50/100-pack tiers are legacy or wholesale only. Both apply unless the prompt says otherwise.
- `… Pack + (1 FREE)` names join the **1 FREE Sprout** collection; `… Sprout Bundle + (1 FREE)` names stay out.
- **Compare-at price:** always blank.

---

## Linked Variant Options (Color & Pack Size)

Variant options are **linked to metaobjects**, not typed as free text. Every live listing (e.g. AHEE Alien) is built this way.

| Option name | Linked metafield | Metaobject type |
|---|---|---|
| `Color` | `shopify.color-pattern` (Shopify's Color field) | `shopify--color-pattern` |
| `Pack Size` | `custom.pack_size` | `pack_size` |

- Create each option as a linked option, and point every value at an existing entry by exact display name. The product-level Color and Pack Size metafields then fill automatically. **Confirm they did** before handoff.
- **Missing entry → create it.** Then add it to `Platform_Reference.xlsx` and list it under "New entries" in the build summary.
  - **Color:** Label = the color name; Base color = the closest Shopify base color(s); Base pattern = `Solid` (use `Rainbow` for Multicolor or Rainbow). Assign a new 4-letter color code and add a row to the `Pricing - Colors` tab.
  - **Pack Size:** Label = the exact variant name. Add a row to the `Pricing - Pack Sizes` tab.
- The **1 FREE Sprout** smart collection matches on the `10 Pack + (1 FREE)` entry. Never substitute a lookalike.

---

## Category Metafields

| Metafield | Sprout lines (Hair Pins) | Kandi lines (Charms) |
|---|---|---|
| Material | Polylactic Acid (PLA), Plastic, Metal | — (not in Charms) |
| Jewelry material | — | **Polylactic Acid (PLA)** only (create the entry with base value Plastic if missing) |
| Age group | Adults | Adults |
| Construction | Solid | — (not in Charms) |
| Target gender | Unisex | Unisex |

---

## SKU Convention

- **Format:** `[CODE]_[COLOR]_[PCK#]` (Sprout, Kandi Charm). Bundles: `[CODE]_[PCK#]`. Underscore separator only. ≤50 chars. `PCK#` is the pack number before the bonus (`10 Pack + (1 FREE)` → `PCK10`).
- **Claude generates the code** unless the prompt supplies one:
  - Artist or festival already has a series → next number in that series (`GRZ6` → `GRZ7`, `EXC12` → `EXC13`, `ZDL14` → `ZDL15`).
  - New artist, festival or bundle → 4 letters + `1` (`HLWN1`), built from the name's distinctive consonants (Kaskade → `KSKD1`).
  - A design that fits two series (artist at a festival) → the series named first in the prompt.
  - Before using a code, check `Platform_Reference.xlsx` → `SKU - Codes` and `SKU - Bank` **and** live Shopify SKUs for clashes.
- **Color codes:** only codes in the `Pricing - Colors` tab. Never use the codes flagged there as typos (`MTCL`, `WHTE`, `YLTR`, `PKWH`).

---

## Images

- **Source:** the flat `IMGs/` folder. Filenames are kept exactly as they are (e.g. `Griz_Kandi_Bones_0001.jpeg`).
- **The prompt maps the variant images.** Sprout and Kandi Charm: `Color: filename`. Bundles: `Featured image: filename`, which goes on every pack variant.
- **Other images are automatic.** Also upload every other file in `IMGs/` whose filename prefix (text before the last `_`) matches the listing's mapped images. List any `IMGs/` file that matches no listing in the build summary's flags, and don't upload it.
- On a Shopify filename collision, append `_v2` before the extension. Alt text on every image; every variant has an image.
- Shopify's CDN blocks server-side fetches (403). Never try to pull uploaded images back down.

---

## Etsy Tags (13 max · ≤20 chars each)

- **Source:** `Platform_Reference.xlsx` → `Keywords - Master`, `Keywords - Sprout Tags` and `Keywords - Kandi Tags`. Use only rows with Publishing Status = **Yes** and Etsy Tag Eligible = **Yes**, whose Product Type matches the line (Sprouts or Both for Sprout lines; Kandi or Both for Kandi lines). Never use Hold rows, and never an artist name.
- **No two tags may share a first word.** This rule wins over everything else.
- **Tags in the prompt come first.** Use them as given, as long as each is ≤20 characters and no two share a first word; drop or fix any that break a rule and flag it in the build summary.
- **Fill in this order:** prompt tags → 1–2 tags from the line's tag tab (`Keywords - Sprout Tags` is a bank to pick from, not a set; `Keywords - Kandi Tags` is the Kandi starting set) → prompt focus keywords → High-priority master rows → Medium rows that fit the exact design. Always **13** in total.
- **Write them to Shopify.** Set the product's `tags` field to exactly these 13 (replace, never append) when creating or updating the draft. Then **read the product back and confirm all 13 are there** before handoff. Tags that appear only in the build summary are not done.
- **Kandi:** no sprout or clip keywords. `kandi bracelet` and `kandi bracelet bead` are fine as tags (never `kandi bracelet` in the title). **Sprouts:** no kandi-only keywords. `Keywords - Legacy` holds the retired tags for reference only.

---

## Deliverables

1. **Shopify draft** per listing (status DRAFT), with the 13 tags in its Tags field and both TikTok metafields filled.
2. **Build summary `.docx`** per listing or batch, saved in `Build_Summaries/` (never the folder root), named `[Listing or Batch]_Build_Summary.docx`. Follow the `Build_Summaries/Seven_Stars_*_Build_Summary.docx` layout: at-a-glance (including the Product Type decision and generated code), title/SEO with character counts, description, variants/SKUs/prices, images + alt text, metafields, Etsy tags, **new entries created**, **flags**, checklist result.
3. **`Platform_Reference.xlsx` updates:** `Product Roster`, `SKU - Codes` and `SKU - Bank` for every listing, plus `Pricing - Colors` or `Pricing - Pack Sizes` rows for any new entry. The **Notes column is append-only**.
   - **Layout is fixed.** Each tab holds one Excel Table: row 1 title, row 2 note, row 3 headers, data from row 4. Add new rows directly under the table's last row and extend the table range to include them (openpyxl: update `ws.tables[name].ref`). Copy number format, font and alignment from the row above.
   - Never add fills, bold, merged cells, blank rows, section-label rows, a second table on a tab, or new tabs; never change rows 1–3 or column widths. Status colors and row banding come from the table style and conditional formatting.
4. **Revisions** after the first build-out: correct inline in chat. Don't regenerate the doc unless asked.

---

## GitHub Sync

- **Repo:** `meowyoudoin-92/product-listings` (public), branch `main`. This folder is the repo root.
- **Commit and push after every change to the repo**: new or edited files, build summaries, `Platform_Reference.xlsx` updates, image additions. No need to ask first. One commit per update, with a short message saying what changed.
- `.claude/`, `.DS_Store` and Office lock files (`~$*`) stay out via `.gitignore`.
- Git push and `gh` need the macOS keychain, which the sandbox blocks, so run them outside the sandbox.

---

## Pre-Handoff Checklist

- [ ] Copy follows the line's gold standard section by section; only the artwork wording changed; nothing implies a bracelet is included
- [ ] Title, SEO title and meta follow the line's pattern with `[Design]` filled; no artist, festival or event names anywhere customer-facing
- [ ] No disclaimer sentences, no "official," no "The Beat Drop," no banned words; `<li>` only
- [ ] Title / SEO title / meta follow the line's pattern and limits
- [ ] Product Type derived and stated; Category correct for the line; theme template set
- [ ] Color and Pack Size options **linked**; product-level metafields populated; new entries logged; category metafields set for the line
- [ ] Pack names, prices, inventory and compare-at (blank) match the prompt or defaults; no Kandi 1 Pack; no Multicolor 1 Pack
- [ ] SKUs follow convention or match live SKUs; generated code checked for clashes
- [ ] Every image uploaded with original filename and alt text; every variant linked
- [ ] 13 Etsy tags, no shared first words, **written to the Shopify Tags field and confirmed by reading the product back**
- [ ] TikTok Title and TikTok Description follow the line's gold standard, have no placeholders or names, and were **confirmed by reading the product back**
- [ ] Status DRAFT · build summary saved in `Build_Summaries/` · Roster, SKU and Notes updated

---

## Reference Files

| File | Purpose |
|---|---|
| `the-beat-drop-brand-identity.md` | Voice rationale, audience, positioning. Read first |
| `Neon Retro Rave Sprout Hair Clips \| Festival Hair Clips.docx` | **Sole source** of Sprout copy (Shopify and TikTok) |
| `Neon Retro Rave Sprout Bundle \| Festival Hair Clip Set.docx` | **Sole source** of Sprout Bundle copy (Shopify and TikTok) |
| `Neon Retro TV Rave Kandi Charm \| 3D Printed Bead.docx` | **Sole source** of Kandi Charm copy (Shopify and TikTok) |
| `Neon Retro Rave Kandi Bundle \| Festival Bead Charms.docx` | **Sole source** of Kandi Bundle copy (Shopify and TikTok) |
| `Intake_Spec_Single_Listing.md` | The prompt templates (four new-listing lines + finish a draft) |
| `BATCH_LISTING.md` | Batch prompt + execution steps |
| `Platform_Reference.xlsx` | Live catalog source of truth. Tabs: Field Mapping, Character Limits, Category Mapping, `Keywords - Master`, `Keywords - Sprout Tags`, `Keywords - Kandi Tags`, `Keywords - Legacy`, `SKU - Rules`, `SKU - Codes`, `SKU - Bank`, Product Roster, `Pricing - Packs`, `Pricing - Colors`, `Pricing - Pack Sizes`, Shorthand Map, Design Library |
| `Build_Summaries/` | Every build summary `.docx`. `Seven_Stars_*_Build_Summary.docx` there is the layout reference only (its copy predates the current templates) |

**Retired:** the older `Gold_Standard_*` templates (in `_Archive/`), GRiZ/Griztronics and earlier Zeds Dead drafts. The four Neon Retro gold standards win.

**Keeping in sync:** if a `.docx` change ever seems to require editing this file too, template wording has leaked in here. Remove it.
