# The Beat Drop — Claude Operating Instructions (Shopify Listings)

*Enforceable rulebook for every Shopify listing task. Read `the-beat-drop-brand-identity.md` first for the "why." Listing copy lives ONLY in the four gold-standard `-v2.docx` files. This file holds structure, rules and process, never template wording. The owner (Karol) can override any rule for a single listing in the prompt.*

---

## Store & Scope

- **Store:** thebeatdrop.myshopify.com · **Account:** admin@thebeatdrop.store · **Claude builds Shopify listings only.** Etsy and TikTok listings are managed elsewhere. The one exception is Etsy tags: Claude picks them and writes them into the Shopify product's **Tags** field.
- **Theme template:** `gp-template-581878106541785827` on every new listing. Never Shopify's default.
- **Prompt format:** `Intake_Spec_Single_Listing.md` (one listing) or `BATCH_LISTING.md` (several). Everything Claude needs is in the prompt plus this file.

---

## Critical Rules

1. **DRAFT only.** Never set ACTIVE, never publish. Claude drafts; a human publishes.
2. **Never write "The Beat Drop"** in a title, description, SEO title, meta description or alt text.
3. **Banned → required words (customer-facing):** "cheap"/"knockoff" → omit · "devotees" → "fans" · "variants" (meaning colors) → "colors"/"multi-color" in Claude's own wording; template labels such as "Color Options" stay as written · "fit" → "outfit"/"clothing".
4. **No artist, festival or event names in customer-facing copy** (title, description, SEO title, meta, alt text, tags). The templates are generic; the `[Design]` slot describes the artwork only. No disclaimer sentences, never the word "official," nothing implying licensed or official merch. The name in the prompt's first line is internal (Product Type, SKU code, Roster).
5. **Copy is verbatim** from the correct `.docx`. Only the documented fill-in slots change.
6. **The prompt beats the defaults.** If the prompt specifies a variant structure, price, inventory or code that differs from this file, build exactly what the prompt says.
7. **Live SKUs beat convention.** If an existing live SKU conflicts with the SKU convention, match it. Never "fix" it silently.
8. **Required from the prompt (no defaults exist):** the product line; Design; Dimensions in inches (all four lines); the color-to-image map, which supplies `[Colors]` (Sprout, Kandi Charm), or the featured image (bundles); prices for Sprout Bundles and Kandi Bundles; pack naming for Sprout Bundles. A Design that contains an artist, festival or event name counts as missing. If any is missing, ask **once, up front, for the whole batch**. Never stop mid-build.
9. **Everything else: don't block.** Use the documented default or Claude's own call, finish the build, and record the decision in the build summary and the Product Roster Notes column.

---

## Product Lines

| Line | Physical build | Template (`.docx`) | Category | Variant options |
|---|---|---|---|---|
| Sprout | Charm + K-Hole + Sprocket + metal spring clip, one design | `Gold_Standard_Sprout_Listing-v2` | Hair Pins | Color + Pack Size |
| Sprout Bundle | Same build, themed multi-design set, no colors | `Gold_Standard_Sprout_Bundle_Listing-v2` | Hair Pins | Pack Size |
| Kandi Charm | Clip-less charm with K-Hole bead hole and Sprocket spring pocket, one design | `Gold_Standard_Kandi_Charm_Listing-v2` | Charms | Color + Pack Size |
| Kandi Bundle | Same charm build, variety of designs, no colors | `Gold_Standard_Kandi_Bundle_Listing-v2` | Charms | Pack Size |

**Product Type: Claude works it out.** Use the exact live spelling:
- Kandi Charm or Kandi Bundle → `Kandi Beads`
- A festival or event is the subject → `Festival Sprouts`
- Everything else → `Artist Sprout`

State the choice in the build summary. `Rave Sprout` is a legacy type; never assign it.

**Collections: Claude assigns none.** Smart collections pick listings up from Product Type and Pack Size. The owner adds manual collections before publishing.

**Category paths:** Hair Pins = `Apparel & Accessories > Clothing Accessories > Hair Accessories > Hair Pins, Claws & Clips` · Charms = `Apparel & Accessories > Jewelry > Charms & Pendants > Charms`

---

## Description Format

All four `-v2` templates share one layout. The **Product Title** and **Description** labels are not copy: the line under Product Title is the title pattern (see Titles & SEO), and the body is everything under Description.

**Body order (verbatim):** two intro paragraphs → **Features** heading + 5 bullets → **Product Details** heading + bullets → **Please Note:** paragraph → italic closing line.

| Fill-in slot | Sprout | Sprout Bundle | Kandi Charm | Kandi Bundle |
|---|---|---|---|---|
| `[Colors]` | Color & Pack Options bullet: all colors incl. Multicolor (e.g. "Pink, Blue, White and Multicolor") | — | Color Options bullet: solid colors only (e.g. "Pink, Blue and White"); the template already says "including multicolor assortments" | — |
| `[x] in x [x] in x [x] in` | Dimensions from the prompt | Dimensions from the prompt | Dimensions from the prompt | Dimensions from the prompt |

- Everything else is fixed: pack sizes, weight (~ 6 g), bead hole, packaging, the Kandi "Includes:" line and the closing line.
- Bold exactly what the `.docx` bolds (headings, bullet labels, "Please Note:"); the closing line is italic (`<p><em>…</em></p>`).
- **Kandi:** the "Includes: Loose kandi charms only. Bracelet, string, and spring clip hardware not included." line stays verbatim. Title, meta and alt text must never imply a bracelet is included: no "kandi bracelet" in a Kandi title. "Bracelet Beads" in the title pattern is fine; "kandi bracelet" is fine as a tag.
- **All lines:** HTML `<ul><li>` only, never manual bullet characters (●, •).

---

## Titles & SEO

**`[Design]`** comes from the prompt: a plain description of the artwork (e.g. "Pixel Skull", "Halloween Mix"), never an artist, festival or event name.

| Line | Product title (≤140) | SEO title (≤60) | Meta description (≤160) |
|---|---|---|---|
| Sprout | The template's Product Title line with `[Design]` filled | `[Design] Rave Sprout Clips \| Festival Hat & Hair Accessory` | Design + "rave sprout clips" + colors + packs |
| Sprout Bundle | The template's Product Title line with `[Design]` filled | `[Design] Rave Sprout Bundle \| Festival Hair & Hat Clips` | Design + "rave sprout bundle" + pack sizes |
| Kandi Charm | The template's Product Title line with `[Design]` filled | `[Design] Rave Kandi Charms \| 3D Printed Festival Beads` | Design + "rave kandi charms" + colors + packs + "Charms only, no bracelet." |
| Kandi Bundle | The template's Product Title line with `[Design]` filled | `[Design] Kandi Charm Bundle \| 3D Printed Festival Beads` | Design + "kandi charm bundle" + pack sizes + "Charms only, no bracelet." |

- If the `.docx` title pattern changes, it wins over this table.
- **Over a limit:** SEO titles drop `3D Printed ` (Kandi) or `Festival ` (Sprout lines) first, then shorten `[Design]`. A product title over 140 shortens `[Design]`.
- **Alt text:** `[Design] rave sprout|rave kandi charm [color] — [brief descriptor]`. Bundles use `[Design] rave sprout bundle|kandi charm bundle — [brief descriptor]`. Never pack sizes or names. A photo showing a bracelet says "shown on a display bracelet (not included)."

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
- **Fill in this order:** 1–2 tags from the line's tag tab (`Keywords - Sprout Tags` is a bank to pick from, not a set; `Keywords - Kandi Tags` is the Kandi starting set) → prompt focus keywords → High-priority master rows → Medium rows that fit the exact design. Always **13** in total.
- **Write them to Shopify.** Set the product's `tags` field to exactly these 13 (replace, never append) when creating or updating the draft. Then **read the product back and confirm all 13 are there** before handoff. Tags that appear only in the build summary are not done.
- **Kandi:** no sprout or clip keywords. `kandi bracelet` and `kandi bracelet bead` are fine as tags (never `kandi bracelet` in the title). **Sprouts:** no kandi-only keywords. `Keywords - Legacy` holds the retired tags for reference only.

---

## Deliverables

1. **Shopify draft** per listing (status DRAFT), with the 13 tags in its Tags field.
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

- [ ] Correct template for the line; body verbatim; only the documented slots changed
- [ ] Correct `-v2` template; Features and Product Details intact; only `[Colors]` and Dimensions filled; Kandi "Includes:" line present; nothing implies a bracelet is included
- [ ] Title is the template line with `[Design]` filled; no artist, festival or event names anywhere customer-facing
- [ ] No disclaimer sentences, no "official," no "The Beat Drop," no banned words; `<li>` only
- [ ] Title / SEO title / meta follow the line's pattern and limits
- [ ] Product Type derived and stated; Category correct for the line; theme template set
- [ ] Color and Pack Size options **linked**; product-level metafields populated; new entries logged; category metafields set for the line
- [ ] Pack names, prices, inventory and compare-at (blank) match the prompt or defaults; no Kandi 1 Pack; no Multicolor 1 Pack
- [ ] SKUs follow convention or match live SKUs; generated code checked for clashes
- [ ] Every image uploaded with original filename and alt text; every variant linked
- [ ] 13 Etsy tags, no shared first words, **written to the Shopify Tags field and confirmed by reading the product back**
- [ ] Status DRAFT · build summary saved in `Build_Summaries/` · Roster, SKU and Notes updated

---

## Reference Files

| File | Purpose |
|---|---|
| `the-beat-drop-brand-identity.md` | Voice rationale, audience, positioning. Read first |
| `Gold_Standard_Sprout_Listing-v2.docx` | **Sole source** of Sprout copy and title pattern |
| `Gold_Standard_Sprout_Bundle_Listing-v2.docx` | **Sole source** of Sprout Bundle copy and title pattern |
| `Gold_Standard_Kandi_Charm_Listing-v2.docx` | **Sole source** of Kandi Charm copy and title pattern |
| `Gold_Standard_Kandi_Bundle_Listing-v2.docx` | **Sole source** of Kandi Bundle copy and title pattern |
| `Intake_Spec_Single_Listing.md` | The four prompt templates |
| `BATCH_LISTING.md` | Batch prompt + execution steps |
| `Platform_Reference.xlsx` | Live catalog source of truth. Tabs: Field Mapping, Character Limits, Category Mapping, `Keywords - Master`, `Keywords - Sprout Tags`, `Keywords - Kandi Tags`, `Keywords - Legacy`, `SKU - Rules`, `SKU - Codes`, `SKU - Bank`, Product Roster, `Pricing - Packs`, `Pricing - Colors`, `Pricing - Pack Sizes`, Shorthand Map, Design Library |
| `Build_Summaries/` | Every build summary `.docx`. `Seven_Stars_*_Build_Summary.docx` there is the layout reference only (its copy predates the current templates) |

**Retired:** the pre-v2 templates (in `_Archive/`), GRiZ/Griztronics and earlier Zeds Dead drafts. The four `-v2.docx` files win.

**Keeping in sync:** if a `.docx` change ever seems to require editing this file too, template wording has leaked in here. Remove it.
