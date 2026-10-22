# BATCH_LISTING.md — Multi-Listing Batch Workflow

*The process wrapper around `CLAUDE.md` for building several Shopify drafts in one run. It doesn't repeat CLAUDE.md's rules.*

---

## Section 1 — Batch Prompt

Open with this line, then paste one filled template per listing from `Intake_Spec_Single_Listing.md`, one after another:

```
Create draft Shopify listings for the batch below.
```

Each block's first line names the product line: **Sprout**, **Sprout Bundle**, **Kandi Charm** or **Kandi Bundle**. Mixed lines in one batch are fine.

**Required for each listing:**

| Line | Required |
|---|---|
| Sprout | Name; Design; Dimensions (in); one `Color: filename` line per color |
| Sprout Bundle | Name; Design; Dimensions (in); pack naming (Pack / Sprout Bundle); prices; featured image |
| Kandi Charm | Name; Design; Dimensions (in); one `Color: filename` line per color; packs & prices (pre-filled defaults) |
| Kandi Bundle | Name; Design; Dimensions (in); prices; featured image |

**Images:** only the variant images are listed. Every other file in `IMGs/` that shares a listing's filename prefix is uploaded automatically.

**If a required field is missing:** Claude asks **once, up front, for the whole batch** before building anything. Once the batch starts, the prompt is final.

---

## Section 2 — Execution (Claude)

1. **Check inputs.**
   - `CLAUDE.md`, the four gold-standard `-v2.docx` files and `Platform_Reference.xlsx` are present and current.
   - Every image named in the prompt exists in `IMGs/`.
   - Required fields are filled.
2. **For each listing:**
   1. Work out the Product Type (`Kandi Beads` / `Festival Sprouts` / `Artist Sprout`), the template, and the Category for the line.
   2. Generate the SKU code (next in series, or a new 4 letters + digit) and check it for clashes.
   3. Copy the correct `-v2.docx` verbatim. Fill only `[Design]` (title), `[Colors]` and Dimensions.
   4. Build the Shopify draft:
      - title / SEO / meta from the line's pattern
      - HTML body
      - **linked** Color and Pack Size options, with prices, SKUs and inventory
      - images and alt text, mapped per the prompt
      - theme template and Category
      - category metafields for the line
      - status **DRAFT**
   5. Create any missing Color or Pack Size entries, and log them.
   6. Pick 13 Etsy tags, write them to the product's Shopify **Tags** field, and read the product back to confirm all 13 are there.
   7. Run CLAUDE.md's Pre-Handoff Checklist.
3. **Update `Platform_Reference.xlsx`:**
   - Product Roster, `SKU - Codes` and `SKU - Bank` for every listing
   - `Pricing - Colors` / `Pricing - Pack Sizes` for any new entry
   - Follow CLAUDE.md → Deliverables #3 for the fixed table layout
   - Notes (append-only) for every assumption, Product Type decision or flag
4. **Deliver the build summary** `.docx`, one per listing or one per batch, saved in `Build_Summaries/`.
5. **Hand off.** Everything stays DRAFT. The owner adds manual collections and publishes.

---

## Section 3 — Defaults (used only when the prompt is silent)

| Field | Default |
|---|---|
| Sprout packs & prices | 1/10/20/30 Pack (Multicolor 10/20/30 only) · $3 / $28 / $55 / $81 |
| Sprout inventory | 200 / 100 / 50 / 10 |
| Kandi Charm packs & prices | 10/20/30 Pack, **no 1 Pack** · $23 / $45 / $67 |
| Kandi Charm inventory | 100 / 50 / 10 per color |
| Bundle inventory (Sprout & Kandi) | 100 / 50 / 10 |
| Kandi Bundle pack naming | Always "Pack" |
| SKU code | Next in the existing series, or a new 4 letters + `1` |
| Compare-at price | Blank, always |
| Product Type | Derived: Kandi → Kandi Beads · festival subject → Festival Sprouts · else Artist Sprout |
| Category | Sprout lines: Hair Pins, Claws & Clips · Kandi lines: Charms |
| Theme template | `gp-template-581878106541785827` |
| Status | DRAFT, always |

Nothing here overrides an explicit value in the prompt.
