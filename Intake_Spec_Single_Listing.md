# Claude Code Prompt Templates — The Beat Drop Listings

*Pick the template for the product line (or #5 to finish a draft that already exists), fill in the brackets, delete any optional line you don't need, and paste it into Claude Code from the Product_Listing_Claude folder. Claude Code loads `CLAUDE.md` on its own, so nothing else needs to be said. For several listings at once, paste one filled block after another under the line `Create draft Shopify listings for the batch below.` (see `BATCH_LISTING.md`).*

**Required in every prompt:**
- **Design:** a plain description of the artwork, e.g. `Pixel Skull`, `Phoenix Wings`, `Halloween Mix`. It leads every title, and Claude rewrites the gold standard's artwork wording to match it. Never an artist, festival or event name.
- **Colors** (Sprout and Kandi Charm only): one image line per color. The colors you list there become the listing's colors.

**Etsy tags (optional, recommended):** list up to 13. Claude uses yours first, as long as each is 20 characters or fewer and no two start with the same word, then fills the rest to 13.

The name in the first line (artist, festival or bundle) is internal only: Claude uses it for the Product Type, SKU code and Product Roster, never in customer-facing copy.

**Images:** list only the variant images. Every other file in `IMGs/` with the same filename prefix (e.g. all `Griz_Kandi_Bones_####.jpeg`) uploads automatically.

---

## 1. Sprout — single design with colors

```
Create a draft Shopify listing for [ARTIST or FESTIVAL NAME] [Festival — delete for an artist] Sprout.

Design: [plain description, no artist or festival names]

Colors & images (IMGs/) — one line per color:
[Color]: [filename]
[Color]: [filename]
[Color]: [filename]
Multicolor: [filename]

Optional — delete any line you don't need:
Variant structure: [e.g. individual colors 1 Pack only; Multicolor 11/22/33 Pack]
Pricing: 1 → $[ ]  11 → $[ ]  22 → $[ ]  33 → $[ ]
Etsy tags: [tag], [tag], [tag]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Blank = 1/11/22/33 Pack (Multicolor 11/22/33 only) at $3 / $28 / $55 / $81; inventory 200 / 100 / 50 / 10; SKU code generated.

---

## 2. Sprout Bundle — themed set, no colors

```
Create a draft Shopify listing for [ARTIST or FESTIVAL NAME] [Festival — delete for an artist] Sprout Bundle.

Design: [plain description of the set, no artist or festival names]
Pricing: 11 → $[ ]  22 → $[ ]  33 → $[ ]

Images (IMGs/):
Featured image: [filename]

Optional — delete any line you don't need:
Inventory: 11 → [ ]  22 → [ ]  33 → [ ]
Etsy tags: [tag], [tag], [tag]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Packs are 11 Pack, 22 Pack and 33 Pack. Blank inventory = 100 / 50 / 10.

---

## 3. Kandi Charm — single design with colors

```
Create a draft Shopify listing for [ARTIST NAME] Kandi Charm.

Design: [plain description, no artist or festival names]

Colors & images (IMGs/) — one line per color:
[Color]: [filename]
[Color]: [filename]
[Color]: [filename]
Multicolor: [filename]

Packs & pricing: 11 → $23  22 → $45  33 → $67

Optional — delete any line you don't need:
Inventory per color: 11 → [ ]  22 → [ ]  33 → [ ]
Etsy tags: [tag], [tag], [tag]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Pre-filled prices are the defaults; edit them only if this design is different. No 1 Pack. Blank inventory = 100 / 50 / 10 per color.

---

## 4. Kandi Bundle — variety of designs, no colors

```
Create a draft Shopify listing for [BUNDLE or FESTIVAL NAME] Kandi Bundle.

Design: [plain description of the set, no artist or festival names]
Packs & pricing: 11 → $[ ]  22 → $[ ]  33 → $[ ]

Images (IMGs/):
Featured image: [filename]

Optional — delete any line you don't need:
Inventory: 11 → [ ]  22 → [ ]  33 → [ ]
Etsy tags: [tag], [tag], [tag]
Focus keywords: [keyword], [keyword]
SKU code: [code]
```

Packs are 11 Pack, 22 Pack and 33 Pack. Blank inventory = 100 / 50 / 10.

---

## 5. Finish an existing draft — any line

```
Finish the existing draft Shopify listing [product ID, handle or exact title]. Line: [Sprout / Sprout Bundle / Kandi Charm / Kandi Bundle].

Design: [plain description, no artist or festival names]

Optional — delete any line you don't need:
Colors & images (IMGs/) — one line per color:
[Color]: [filename]
Featured image: [filename]
Pricing: 11 → $[ ]  22 → $[ ]  33 → $[ ]
Etsy tags: [tag], [tag], [tag]
Leave as is: [fields not to touch, e.g. alt text, tags]
Also change: [anything else]

Read the draft first and compare every field, including the TikTok Title and TikTok Description metafields, to CLAUDE.md and the line's gold standard. Fix whatever is missing or doesn't match, except anything under "Leave as is". Keep the product ID, handle and existing SKUs. Don't delete variants or images; list any that should go in the build summary. Status stays DRAFT.
```

Design can be left out only if the draft's title already has it. Colors, images and prices are needed only when they're missing or changing; Claude keeps what the draft already has.

---

## What you never need to type

Claude handles these per `CLAUDE.md`:
- Product Type, Shopify Category, theme template
- Title, SEO title, meta and alt text (each line's pattern, led by your Design)
- Shopify description, written from the line's gold standard
- Category metafields and linked Color/Pack Size options (plus any new entries)
- SKU code (unless you give one)
- The rest of the 13 Etsy tags, written to the Shopify Tags field
- TikTok Title and TikTok Description metafields (from the line's gold standard)
- DRAFT status

Collections are left for you to add before publishing.

## What you get back

- The Shopify draft
- A build summary `.docx` in `Build_Summaries/`: Product Type and code chosen, character counts, any new Color or Pack Size entries, flags to review
- `Platform_Reference.xlsx` updated: Roster, SKU bank, Notes, and any new Color Code or Pack Size rows

If a required line is missing (Design, the color/image lines or featured image, bundle prices), Claude asks once before starting.
