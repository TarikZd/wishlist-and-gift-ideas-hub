# 📖 Start Here: Wishlist & Gift Ideas Hub

Welcome to the **Wishlist & Gift Ideas Hub** by **Moorish Dev**. Start adding wishes and gift ideas in under 60 seconds.

---

## ⚡ Quick Start (60 Seconds)

1. **Duplicate this template** → Click `Duplicate` in the top-right corner.
2. **Add people** → Open the `People` view, add the friends/family you buy gifts for, and set their birthdays and budget.
3. **Add your own wishlist** → Click "🎁 Add Wish", set `For = Myself`, and fill in the item details.
4. **Add gift ideas** → Click "🎁 Add Wish", set `For = [Person's Name]`, and link it to that person.

---

## 🏗️ Architecture Overview

| Location | What's Here |
| --- | --- |
| **Main Dashboard** | Wishlist Gallery + People Gift Tracker |
| **`[DB] Backend`** | Raw `Wishlist Items` and `People` databases |

---

## ✍️ Manual Setup Steps (Required)

### Step 1: Set Up the Wishlist Gallery View
1. On the Wishlist Items Linked View → `+ Add a view` → `Gallery`.
2. Set Card Preview to `Product Image URL`. Name it `🛍️ My Wishlist`.

### Step 2: Configure the Gift Budget Rollup
1. Open `[DB] Backend` → `People` database.
2. Click `Total Gift Value` → **Edit Property** → Type = `Rollup`.
3. Set: Relation = `Gift Ideas`, Property = `Price (£)`, Calculate = `Sum`.

### Step 3: Create Filtered Views
1. In the Wishlist Items Linked View: add a filter `For = Myself` → name it `🛍️ My Wishlist`.
2. Add another view with filter `Status = 💭 Wishful` → name it `💡 Ideas Pending`.

### Step 4: Create Button Blocks
1. Type `/button` → Create `🎁 Add Wish` and `✅ Mark as Purchased`.

---

## 🎨 Customization Tips
- **Birthday Reminders**: The `People` database's Birthday field lets you build a filtered view of upcoming birthdays this month.
- **Secret Sharing**: Share only the `🎁 Gift Ideas` filtered view (not the full database) with family for coordinated gift-giving.
- **Price Alerts**: Add a `Budget Overrun` formula: `if(prop("Price (£)") > prop("Budget"), "⚠️ Over Budget", "✅ Within Budget")`.

---

*Built by Moorish Dev | Last Updated: June 2026*
