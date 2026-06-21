# 🗄️ Database Schema: Wishlist & Gift Ideas Hub

---

## Database 1: Wishlist Items

| Property Name | Type | Purpose |
| --- | --- | --- |
| **Item Name** | `Title` | e.g., "Sony WH-1000XM5 Headphones". |
| **For** | `Select` | Who this item is for: `Myself`, or a person's name. |
| **Category** | `Select` | `Tech`, `Fashion`, `Books`, `Home`, `Experiences`, `Health`. |
| **Price (£)** | `Number` | Estimated or actual price. |
| **Priority** | `Select` | `🔥 Must Have`, `⚡ Would Love`, `🌿 Nice to Have`. |
| **Priority Badge** | `Formula` | Emoji badge based on Priority. |
| **Status** | `Select` | `💭 Wishful`, `🛒 Ready to Buy`, `✅ Purchased`, `🎁 Gifted`. |
| **Product URL** | `URL` | Link to the product page. |
| **Product Image URL** | `URL` | URL of product image for Gallery view. |
| **Purchased By** | `Person` | Who bought this item (for gift tracking). |
| **Purchase Date** | `Date` | When it was purchased. |
| **Notes** | `Text` | Specific variant, color, size preferences. |

## Database 2: People (Gift Tracker)

| Property Name | Type | Purpose |
| --- | --- | --- |
| **Name** | `Title` | Friend or family member's name. |
| **Relationship** | `Select` | `Family`, `Friend`, `Partner`, `Colleague`. |
| **Birthday** | `Date` | Their birthday (for gift planning). |
| **Budget (£)** | `Number` | Your gift budget for this person. |
| **Gift Ideas** | `Relation` | Links to Wishlist Items tagged for them. |
| **Total Gift Value** | `Rollup` | Sum of linked Wishlist Items' prices. |
| **Notes** | `Text` | Their interests, sizes, or preferences. |

## Formula 2.0 Logic — Priority Badge
```javascript
ifs(
  prop("Priority") == "🔥 Must Have", "🔥 Must Have",
  prop("Priority") == "⚡ Would Love", "⚡ Would Love",
  "🌿 Nice to Have"
)
```

## Architectural Notes
- **Vault Method:** Both databases in `[DB] Backend`. Dashboard uses Gallery view (product images) and Board view (grouped by Status).
- **Recommended Views:** `🛍️ My Wishlist` (filtered: For = Myself), `🎁 Gift Ideas` (filtered: For ≠ Myself), `✅ Purchased` (filtered: Status = Purchased).
