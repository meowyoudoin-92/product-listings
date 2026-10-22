# Claude Code Prompt Templates — The Beat Drop Listings

*Pick the template for the product line, fill in the brackets, delete any optional line you don't need, and paste it into Claude Code from the Product_Listing_Claude folder. Claude Code loads `CLAUDE.md` on its own, so nothing else needs to be said. For several listings at once, paste one filled block after another under the line `Create draft Shopify listings for the batch below.` (see `BATCH_LISTING.md`).*

**Required in every prompt** (these fill the placeholders in the `-v2` templates):
- **Design:** a plain description of the artwork, e.g. `Pixel Skull`, `Phoenix Wings`, `Halloween Mix`. It leads the title. Never an artist, festival or event name.
- **Dimensions:** `[x] in x [x] in x [x] in` (inches).
- **Colors** (Sprout and Kandi Charm only): one image line per color. The colors you list there fill `[Colors]` and become the listing's colors.

The name in the first line (artist, festival or bundle) is internal only: Claude uses it for the Product Type, SKU code and Product Roster, never in customer-facing copy.

**Images:** list only the variant images. Every other file in `IMGs/` with the same filename prefix (e.g. all `Griz_Kandi_Bones_####.jpeg`) uploads automatically.

---

## 1. Sprout — single design with colors

```
Create a draft Shopify listing for [ARTIST or FESTIVAL NAME] [Festival — delete for an artist] Sprout.

Design: [plain description, no artist or festival names]
Dimensions: [x] in x [x] in x [x] in

Colors & images (IMGs/) — one line per color:
[Color]: [filename]
[Color]: [filename]
[Color]: [filename]
Multicolor: [filename]

Optional — delete any line you don't need:
Variant structure: [e.g. individual colors 1 Pack only; Multicolor 10/20/30 Pack]
Pricing: 1 → $[ ]  10 → $[ ]  20 → $[ ]  30 → $[ ]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Blank = 1/10/20/30 Pack (Multicolor 10/20/30 only) at $3 / $28 / $55 / $81; inventory 200 / 100 / 50 / 10; SKU code generated.

---

## 2. Sprout Bundle — themed set, no colors

```
Create a draft Shopify listing for [ARTIST or FESTIVAL NAME] [Festival — delete for an artist] Sprout Bundle.

Design: [plain description of the set, no artist or festival names]
Dimensions: [x] in x [x] in x [x] in
Pack naming: [Pack / Sprout Bundle]
Pricing: 10 → $[ ]  20 → $[ ]  30 → $[ ]

Images (IMGs/):
Featured image: [filename]

Optional — delete any line you don't need:
Inventory: 10 → [ ]  20 → [ ]  30 → [ ]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

**Pack** gives "10 Pack + (1 FREE)" and joins the 1 FREE Sprout collection; **Sprout Bundle** gives "10 Sprout Bundle + (1 FREE)" and stays out. Blank inventory = 100 / 50 / 10.

---

## 3. Kandi Charm — single design with colors

```
Create a draft Shopify listing for [ARTIST NAME] Kandi Charm.

Design: [plain description, no artist or festival names]
Dimensions: [x] in x [x] in x [x] in

Colors & images (IMGs/) — one line per color:
[Color]: [filename]
[Color]: [filename]
[Color]: [filename]
Multicolor: [filename]

Packs & pricing: 10 → $23  20 → $45  30 → $67

Optional — delete any line you don't need:
Inventory per color: 10 → [ ]  20 → [ ]  30 → [ ]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Pre-filled prices are the defaults; edit them only if this design is different. No 1 Pack. Blank inventory = 100 / 50 / 10 per color.

---

## 4. Kandi Bundle — variety of designs, no colors

```
Create a draft Shopify listing for [BUNDLE or FESTIVAL NAME] Kandi Bundle.

Design: [plain description of the set, no artist or festival names]
Dimensions: [x] in x [x] in x [x] in
Packs & pricing: 10 → $[ ]  20 → $[ ]  30 → $[ ]

Images (IMGs/):
Featured image: [filename]

Optional — delete any line you don't need:
Inventory: 10 → [ ]  20 → [ ]  30 → [ ]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Pack names are always "10 Pack + (1 FREE)" style. Blank inventory = 100 / 50 / 10.

---

## What you never need to type

Claude handles these per `CLAUDE.md`:
- Product Type, Shopify Category, theme template
- Title, SEO title, meta and alt text (each line's pattern, led by your Design)
- Weight and every other fixed line in the template
- Category metafields and linked Color/Pack Size options (plus any new entries)
- SKU code (unless you give one)
- 13 Etsy tags, written to the Shopify Tags field
- DRAFT status

Collections are left for you to add before publishing.

## What you get back

- The Shopify draft
- A build summary `.docx` in `Build_Summaries/`: Product Type and code chosen, character counts, any new Color or Pack Size entries, flags to review
- `Platform_Reference.xlsx` updated: Roster, SKU bank, Notes, and any new Color Code or Pack Size rows

If a required line is missing (Design, Dimensions, the color/image lines or featured image, bundle prices, Sprout Bundle pack naming), Claude asks once before starting.
