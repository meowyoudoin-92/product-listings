# Claude Code Prompt Templates — The Beat Drop Listings

*Pick the template for the product line, fill in the brackets, delete any optional line you don't need, and paste it into Claude Code from the Product_Listing_Claude folder. Claude Code loads `CLAUDE.md` on its own, so nothing else needs to be said. For several listings at once, paste one filled block after another under the line `Create draft Shopify listings for the batch below.` (see `BATCH_LISTING.md`).*

**Images:** list only the variant images. Every other file in `IMGs/` with the same filename prefix (e.g. all `Griz_Kandi_Bones_####.jpeg`) uploads automatically with alt text. The colors you list in the image lines become the listing's colors.

---

## 1. Sprout — single design with colors

```
Create a draft Shopify listing for [ARTIST or FESTIVAL NAME] [Festival — delete for an artist] Sprout.

Images (IMGs/) — one line per color:
[Color]: [filename]
[Color]: [filename]
[Color]: [filename]
Multicolor: [filename]

Optional — delete any line you don't need:
Variant structure: [e.g. individual colors 1 Pack only; Multicolor 10/20/30 Pack]
Pricing: 1 → $[ ]  10 → $[ ]  20 → $[ ]  30 → $[ ]
Research link: [url]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Blank = 1/10/20/30 Pack (Multicolor 10/20/30 only) at $3 / $28 / $55 / $81; SKU code generated.

---

## 2. Sprout Bundle — themed set, no colors

```
Create a draft Shopify listing for [ARTIST or FESTIVAL NAME] [Festival — delete for an artist] Sprout Bundle.

Pack naming: [Pack / Sprout Bundle]
Pricing: 10 → $[ ]  20 → $[ ]  30 → $[ ]

Images (IMGs/):
Featured image: [filename]

Optional — delete any line you don't need:
Headliner: [artist]
Theme notes: [e.g. city festival, not camping; closing festivals: X, Y, Z]
Inventory: 10 → [ ]  20 → [ ]  30 → [ ]
Research link: [url]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

**Pack** gives "10 Pack + (1 FREE)" and joins the 1 FREE Sprout collection; **Sprout Bundle** gives "10 Sprout Bundle + (1 FREE)" and stays out. Blank inventory = 100 / 50 / 30.

---

## 3. Kandi Charm — single design with colors

```
Create a draft Shopify listing for [ARTIST NAME] Kandi Charm.

Images (IMGs/) — one line per color:
[Color]: [filename]
[Color]: [filename]
[Color]: [filename]
Multicolor: [filename]

Packs & pricing: 10 → $23  20 → $45  30 → $67
Dimensions: [L] × [W] × [H] cm
Weight: [ ] g

Optional — delete any line you don't need:
Inventory per color: 10 → [ ]  20 → [ ]  30 → [ ]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Pre-filled prices are the defaults; edit them only if this design is different. No 1 Pack. Blank inventory = 20 / 10 / 5 per color.

---

## 4. Kandi Bundle — variety of designs, no colors

```
Create a draft Shopify listing for [BUNDLE or FESTIVAL NAME] Kandi Bundle.

Packs & pricing: 10 → $[ ]  20 → $[ ]  30 → $[ ]
Dimensions: [Vary by design / L × W × H cm]
Weight: ~[ ] g

Images (IMGs/):
Featured image: [filename]

Optional — delete any line you don't need:
Inventory: 10 → [ ]  20 → [ ]  30 → [ ]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Pack names are always "10 Pack + (1 FREE)" style. Blank inventory = 100 / 50 / 30.

---

## What you never need to type

Claude handles these per `CLAUDE.md`:
- Product Type, Shopify Category, theme template
- Title, SEO title and meta (from each line's pattern)
- Category metafields and linked Color/Pack Size options (plus any new entries)
- SKU code (unless you give one)
- 13 Etsy tags, written to the Shopify Tags field
- DRAFT status

Collections are left for you to add before publishing.

## What you get back

- The Shopify draft
- A build summary `.docx`: Product Type and code chosen, character counts, any new Color or Pack Size entries, flags to review
- `Platform_Reference.xlsx` updated: Roster, SKU bank, Notes, and any new Color Code or Pack Size rows

If a required line is missing (images, bundle prices, Sprout Bundle pack naming, Kandi dimensions and weight), Claude asks once before starting.
