# The Beat Drop — Claude Operating Instructions (Shopify Listings)

*Enforceable rulebook for every Shopify listing task. Read `the-beat-drop-brand-identity.md` first for the "why." Listing copy lives ONLY in the four gold-standard `.docx` files. This file holds structure, rules and process, never template wording. The owner (Karol) can override any rule for a single listing in the prompt.*

---

## Store & Scope

- **Store:** thebeatdrop.myshopify.com · **Account:** admin@thebeatdrop.store · **Claude builds Shopify listings only.** Etsy and TikTok listings are managed elsewhere. The one exception is Etsy tags: Claude picks them and writes them into the Shopify product's **Tags** field.
- **Theme template:** `gp-template-581878106541785827` on every new listing. Never Shopify's default.
- **Prompt format:** `Intake_Spec_Single_Listing.md` (one listing) or `BATCH_LISTING.md` (several). Everything Claude needs is in the prompt plus this file.

---

## Critical Rules

1. **DRAFT only.** Never set ACTIVE, never publish. Claude drafts; a human publishes.
2. **Never write "The Beat Drop"** in a title, description, SEO title, meta description or alt text.
3. **Banned → required words (customer-facing):** "cheap"/"knockoff" → omit · "devotees" → "fans" · "variants"/"options" → "colors"/"multi-color" · "fit" → "outfit"/"clothing".
4. **No disclaimer sentences, and never the word "official."** Sprout templates carry fan-made framing through word choice; Kandi templates intentionally don't mention it. Never add "not an official partnership with [Artist]" or anything implying licensed or official merch.
5. **Copy is verbatim** from the correct `.docx`. Only the documented fill-in slots change.
6. **The prompt beats the defaults.** If the prompt specifies a variant structure, price, inventory or code that differs from this file, build exactly what the prompt says.
7. **Live SKUs beat convention.** If an existing live SKU conflicts with the SKU convention, match it. Never "fix" it silently.
8. **Required from the prompt (no defaults exist):** the product line; the color-to-image map (Sprout, Kandi Charm) or featured image (bundles); prices for Sprout Bundles and Kandi Bundles; pack naming for Sprout Bundles; dimensions and weight for both Kandi lines. If any is missing, ask **once, up front, for the whole batch**. Never stop mid-build.
9. **Everything else: don't block.** Use the documented default or Claude's own call, finish the build, and record the decision in the build summary and the Product Roster Notes column.

---

## Product Lines

| Line | Physical build | Template (`.docx`) | Category | Variant options |
|---|---|---|---|---|
| Sprout | Charm + K-Hole + Sprocket + metal spring clip, one design | `Gold_Standard_Sprout_Listing` | Hair Pins | Color + Pack Size |
| Sprout Bundle | Same build, themed multi-design set, no colors | `Gold_Standard_Sprout_Bundle_Listing` | Hair Pins | Pack Size |
| Kandi Charm | Clip-less charm with bead hole, one design | `Gold_Standard_Kandi_Charm_Listing` | Charms | Color + Pack Size |
| Kandi Bundle | Clip-less charms, variety of designs, no colors | `Gold_Standard_Kandi_Bundle_Listing` | Charms | Pack Size |

**Product Type: Claude works it out.** Use the exact live spelling:
- Kandi Charm or Kandi Bundle → `Kandi Beads`
- A festival or event is the subject → `Festival Sprouts`
- Everything else → `Artist Sprout`

State the choice in the build summary. `Rave Sprout` is a legacy type; never assign it.

**Collections: Claude assigns none.** Smart collections pick listings up from Product Type and Pack Size. The owner adds manual collections before publishing.

**Category paths:** Hair Pins = `Apparel & Accessories > Clothing Accessories > Hair Accessories > Hair Pins, Claws & Clips` · Charms = `Apparel & Accessories > Jewelry > Charms & Pendants > Charms`

---

## Description Format

**Document label / title line.** The bold first line of each `.docx` is not body copy. On the Sprout templates it's a document label (e.g. "Zeds Dead Product Description"). On the Kandi templates it's the TikTok-compatible **product title** pattern (see Titles & SEO).

### Sprout & Sprout Bundle

**Body order:** Hook → Intro (2 sentences) → 5 bullets → closing paragraph → CTA line. No signoff, no in-body headline. **Fixed:** bullets 1–4, the CTA line, the 5-bullet count.

| Fill-in slot | Sprout | Sprout Bundle |
|---|---|---|
| Name in hook / intro / closing | Artist | Bundle or festival name |
| Headliner or audience in intro | — | Optional |
| Bullet 5 | This listing's colors | Pack sizes |
| Festivals in closing | **Fixed:** Electric Forest, Lost Lands, Seven Stars | Fit the theme |
| Venue detail (e.g. "two tents over") | — | Adapt for non-camping events |

- **Bold** all SEO keywords, plus "K-Hole" and "Sprocket." Primary focus keyword within the **first 160 characters** of the body.
- **Research links** (optional): light venue or vibe details only. Never write a bio.

### Kandi Charm & Kandi Bundle

**Body order (verbatim):** intro paragraph → second paragraph → **Features** (4 bullets) → **Product Details** (5 bullets) → bold tagline → closing line → italic note. The artist or bundle name does **not** go into the body.

| Fill-in slot | Kandi Charm | Kandi Bundle |
|---|---|---|
| Color Options bullet | This listing's colors + "Multi-Color" | — (no colors) |
| Value Packs bullet | Pack numbers (e.g. 10-, 20-, or 30-Pack) | Pack numbers (e.g. 10-, 20-, or 30-piece packs) |
| Dimensions | From the prompt | From the prompt ("Vary by design" if given) |
| Weight | From the prompt | From the prompt |

- Bold exactly what the `.docx` bolds (the headings and the tagline); the note is italic (`<p><em>…</em></p>`).
- The "Includes: Kandi charms ONLY (no bracelet or string)" line stays verbatim. Title, meta, alt text and tags must never imply a bracelet is included. "Bracelet Bead" in the title means a bead for bracelets and is fine.

**All lines:** HTML `<ul><li>` only, never manual bullet characters (●, •).

---

## Titles & SEO

| Line | Product title (≤140) | SEO title (≤60) | Meta description (≤160) |
|---|---|---|---|
| Sprout | `[Artist] Rave Sprouts \| EDM Accessory \| Festival Gift \| [Color] [Color] [Color]` | `[Artist] Rave Sprouts \| EDM Festival Gift` | Primary keyword + color names |
| Sprout Bundle | `[Name] Rave Sprout Bundle \| [Headliner] Festival Hair Clip Accessory Set \| Festival Gifts` | `[Name] Rave Sprout Bundle \| EDM Festival Gift` | Primary keyword + pack sizes |
| Kandi Charm | `3D Printed [Artist] Rave Kandi Charm, Music Festival Bracelet Bead, DIY Kandi Jewelry Accessory` | `[Artist] Rave Kandi Charm \| 3D Printed Festival Bead` | Keyword + colors + "Charms only, no bracelet." |
| Kandi Bundle | `[Name] Rave Kandi Bead Variety Bundle \| [X], [Y] & [Z]-Pack \| 3D Printed Festival Beads` | `[Name] Rave Kandi Bead Bundle \| 3D Printed Festival Beads` | Keyword + pack sizes + "Charms only, no bracelet." |

- Kandi titles follow the bold first line of their `.docx`; if the `.docx` pattern changes, it wins over this table.
- **SEO title over 60 characters:** Sprout lines drop `EDM ` first; Kandi lines drop `3D Printed ` first. **No headliner** for a Sprout Bundle: use `EDM` in that slot.
- **Alt text:** `[Name] [design descriptor] rave sprout|rave kandi charm [color] — [brief descriptor]`. Bundles use the bundle name in place of the color. Never pack sizes. A photo showing a bracelet says "shown on a display bracelet (not included)."

---

## Variants, Pricing & Inventory

Every pack above 1 includes a **FREE bonus of the same product**: Sprouts get bonus sprouts, Kandi gets bonus kandi charms. The `+ (N FREE)` pack names say it; copy never promises a different product as the bonus.

| Line | Pack names | Default prices | Default inventory |
|---|---|---|---|
| Sprout | `[Color] / 1 Pack` · `[Color] / 10 Pack + (1 FREE)` · `20 Pack + (2 FREE)` · `30 Pack + (3 FREE)` | $3 / $28 / $55 / $81 | 50 / 20 / 10 / 5 |
| Kandi Charm | `[Color] / 10 Pack + (1 FREE)` · `20 Pack + (2 FREE)` · `30 Pack + (3 FREE)` (**no 1 Pack**) | $23 / $45 / $67 | 20 / 10 / 5 per color |
| Sprout Bundle | "Pack" → `10 Pack + (1 FREE)`… or "Sprout Bundle" → `10 Sprout Bundle + (1 FREE)`… (from the prompt) | From the prompt | 100 / 50 / 30 |
| Kandi Bundle | Always "Pack": `10 Pack + (1 FREE)` · `20 Pack + (2 FREE)` · `30 Pack + (3 FREE)` | From the prompt | 100 / 50 / 30 |

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
  - **Color:** Label = the color name; Base color = the closest Shopify base color(s); Base pattern = `Solid` (use `Rainbow` for Multicolor or Rainbow). Assign a new 4-letter color code and add a row to Pricing Master → Standard Color Codes.
  - **Pack Size:** Label = the exact variant name. Add a row to Pricing Master → Pack Sizes.
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
  - A design that fits two series (artist at a festival) → whichever name leads the product title.
  - Before using a code, check `Platform_Reference.xlsx` → SKU Convention **and** live Shopify SKUs for clashes.
- **Color codes:** only codes in Pricing Master → Standard Color Codes. Never use the codes flagged there as typos (`MTCL`, `WHTE`, `YLTR`, `PKWH`).

---

## Images

- **Source:** the flat `IMGs/` folder. Filenames are kept exactly as they are (e.g. `Griz_Kandi_Bones_0001.jpeg`).
- **The prompt maps the variant images.** Sprout and Kandi Charm: `Color: filename`. Bundles: `Featured image: filename`, which goes on every pack variant.
- **Other images are automatic.** Also upload every other file in `IMGs/` whose filename prefix (text before the last `_`) matches the listing's mapped images. List any `IMGs/` file that matches no listing in the build summary's flags, and don't upload it.
- On a Shopify filename collision, append `_v2` before the extension. Alt text on every image; every variant has an image.
- Shopify's CDN blocks server-side fetches (403). Never try to pull uploaded images back down.

---

## Etsy Tags (13 max · ≤20 chars each)

- **No two tags may share a first word.** This rule wins over everything else, including the tag bank's "apply all 10 Always."
- **Fill in this order:** Always tags (as many as the first-word rule allows) → prompt focus keywords → Rotate/Specific → listing-specific. Always **13** in total.
- **Write them to Shopify.** Set the product's `tags` field to exactly these 13 (replace, never append) when creating or updating the draft. Then **read the product back and confirm all 13 are there** before handoff. Tags that appear only in the build summary are not done.
- **Kandi:** drop clip-specific tags (`rave sprout`, `sprout clip`) and never use `kandi bracelet`. **Tag bank:** `Platform_Reference.xlsx` → Etsy Tag Bank; never reuse Retired tags.

---

## Deliverables

1. **Shopify draft** per listing (status DRAFT), with the 13 tags in its Tags field.
2. **Build summary `.docx`** per listing or batch, following the `Seven_Stars_*_Build_Summary.docx` layout: at-a-glance (including the Product Type decision and generated code), title/SEO with character counts, description, variants/SKUs/prices, images + alt text, metafields, Etsy tags, **new entries created**, **flags**, checklist result.
3. **`Platform_Reference.xlsx` updates:** Product Roster and SKU Convention tabs for every listing, plus Color Codes or Pack Sizes rows for any new entry. The **Notes column is append-only**.
4. **Revisions** after the first build-out: correct inline in chat. Don't regenerate the doc unless asked.

---

## Pre-Handoff Checklist

- [ ] Correct template for the line; body verbatim; only the documented slots changed
- [ ] Sprout lines: 5 bullets, CTA, no signoff; Sprout festivals = Electric Forest, Lost Lands, Seven Stars; K-Hole and Sprocket bolded; focus keyword in first 160 chars
- [ ] Kandi lines: Features + Product Details intact; colors, packs, dimensions and weight filled from the prompt; "Includes: Kandi charms ONLY" line present; nothing implies a bracelet is included
- [ ] No disclaimer sentences, no "official," no "The Beat Drop," no banned words; `<li>` only
- [ ] Title / SEO title / meta follow the line's pattern and limits
- [ ] Product Type derived and stated; Category correct for the line; theme template set
- [ ] Color and Pack Size options **linked**; product-level metafields populated; new entries logged; category metafields set for the line
- [ ] Pack names, prices, inventory and compare-at (blank) match the prompt or defaults; no Kandi 1 Pack; no Multicolor 1 Pack
- [ ] SKUs follow convention or match live SKUs; generated code checked for clashes
- [ ] Every image uploaded with original filename and alt text; every variant linked
- [ ] 13 Etsy tags, no shared first words, **written to the Shopify Tags field and confirmed by reading the product back**
- [ ] Status DRAFT · build summary delivered · Roster, SKU and Notes updated

---

## Reference Files

| File | Purpose |
|---|---|
| `the-beat-drop-brand-identity.md` | Voice rationale, audience, positioning. Read first |
| `Gold_Standard_Sprout_Listing.docx` | **Sole source** of Sprout copy |
| `Gold_Standard_Sprout_Bundle_Listing.docx` | **Sole source** of Sprout Bundle copy |
| `Gold_Standard_Kandi_Charm_Listing.docx` | **Sole source** of Kandi Charm copy and title pattern |
| `Gold_Standard_Kandi_Bundle_Listing.docx` | **Sole source** of Kandi Bundle copy and title pattern |
| `Intake_Spec_Single_Listing.md` | The four prompt templates |
| `BATCH_LISTING.md` | Batch prompt + execution steps |
| `Platform_Reference.xlsx` | Live catalog source of truth: SKU bank, Product Roster, Pricing Master (prices, Color Codes, Pack Sizes), Category Mapping, Etsy Tag Bank, Keyword Bank, character limits |
| `Seven_Stars_*_Build_Summary.docx` | Build summary layout reference only (their copy predates the current templates) |

**Retired tone references:** GRiZ/Griztronics, earlier Zeds Dead drafts, and the Keyword Bank note pointing to the GRiZ listing. The four `.docx` files win.

**Keeping in sync:** if a `.docx` change ever seems to require editing this file too, template wording has leaked in here. Remove it.
