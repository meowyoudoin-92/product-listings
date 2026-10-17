Update the 17 Kandi Beads DRAFT listings in Shopify using Kandi_TikTok_Update_Source.md in this folder. This is a one-time update of existing drafts, not a new build.

SCOPE
- Only the 17 product IDs in the source file. Before changing anything, confirm each is status DRAFT and product type Kandi Beads. Skip and report any that isn't.
- Never touch an ACTIVE listing (Seven Stars, Hulaween). Never publish: everything stays DRAFT.
- If the Shopify connection isn't available, stop and say so before doing anything.

CHANGE (use the source file's values exactly)
- Title, SEO title, meta description, and URL handle (only where the source gives a new one).
- Description: replace the whole body with the source HTML.
- Tags: replace with the exact 13 listed. For Escape Halloween and BOO Seattle, pick 13 per CLAUDE.md → Etsy Tags.
- Variants: the changes listed per listing (charm prices, Wobbleween prices, Force Fields rebuild).
- Variant images: Griz and Pretty Lights Multicolor only.
- Category metafields: Jewelry material = Polylactic Acid (PLA). If that entry doesn't exist, create it (base value Plastic) and log it. Clear Material and Construction.

OVERRIDES FOR THIS UPDATE ONLY
- Description copy comes from the source file, not the Gold Standard Kandi templates. This overrides CLAUDE.md Critical Rule 5 and the Kandi body order.
- Titles are the TikTok titles in the source file, not the CLAUDE.md title pattern.
- Don't add the "KANDI CHARMS ONLY" line, Features / Product Details sections, dimensions, weight or keyword lists.
- Don't edit CLAUDE.md, the templates or the source file.

DO NOT CHANGE
- Alt text (the owner enters it manually).
- Images, other than linking the variant images listed.
- Collections, Product Type, Category, theme template.
- Inventory and SKUs, except the Force Fields rebuild.
- Any "/ 1 Pack" variant. Don't delete them; just list any that remain.

VERIFY
Read every product back and confirm: title, SEO title, meta, handle, body, all 13 tags, variant names / prices / SKUs / inventory, Jewelry material, and status DRAFT. Fix any mismatch, then re-read.

REPORT
- Kandi_TikTok_Update_Summary.docx in this folder, one section per listing:
  - what changed and the read-back result;
  - any new metaobject entries created;
  - flags: remaining 1 Pack variants, variants without an image, count of images with blank alt text, anything that differed from the source or couldn't be applied;
  - the 13 tags chosen for Escape Halloween and BOO Seattle.
- Platform_Reference.xlsx:
  - Product Roster: new prices (12 charms, Wobbleween, Force Fields).
  - SKU Convention: FFBD1_PCK10 / PCK20 / PCK30.
  - Notes (append-only): one line per listing, "TikTok copy update [date]".
