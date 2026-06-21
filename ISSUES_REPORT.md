# Template Audit & Friction Points — Wishlist & Gift Ideas Hub

## 1. Logo Hosting Issue (Notion API)
- **Problem:** The Notion API does not support local file uploads for page icons.
- **Resolution:** Distribute `moorish_dev_logo.png` to `assets/`. User sets it as page icon manually.

## 2. Total Wishlist Value Rollup
- **Problem:** A Rollup summing `Price (£)` from all Wishlist Items requires the `Price (£)` property to be a `Number` type. If any entries have empty prices, the sum will exclude them (which is actually correct behavior — document this).
- **Resolution:** Add a note in `setup_guide/Setup_Guide.md` that items without a price are excluded from the total value calculation.

## 3. Sharing the Wishlist
- **Problem:** Sharing your wishlist with friends/family so they can see what to buy you — but without them accidentally seeing items you're buying FOR them — is a design challenge.
- **Resolution:** Recommend creating two separate database views: one for `My Wishlist` (your items) filtered by the `For` field = "Self", and one `Gift Ideas` view filtered by `For` = specific person. Share the relevant view link publicly.

## 4. Product Image Gallery
- **Problem:** A Gallery view showing product images requires a `Cover URL` field with external image URLs. The API can create the property but cannot populate product images automatically.
- **Resolution:** Add a `Product Image URL` property (URL type). Document in `setup_guide/Setup_Guide.md` that users can paste product image URLs from Amazon, etc.

## 5. Button Block API Limitation
- **Problem:** Notion's native Button blocks cannot be created via the public Notion API.
- **Resolution:** User must manually create `🎁 Add Wish` and `✅ Mark as Purchased` button blocks.
