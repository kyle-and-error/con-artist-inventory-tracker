# artist-alley-inventory-manager
An open source, locally hosted inventory tracker, built by Artist Alley, for Artist Alley.


While you're here, please consider [supporting the development of this tool.](https://ko-fi.com/kyleanderror)

While this tool is in development, please feel free to try out [this](https://docs.google.com/spreadsheets/d/1Ng14v-IQt59Q3Ktimy4e6UgFWp5q-t3A6-hEjoX3xSw/edit?usp=drivesdk) Google Sheets Template. 

# [Inventory Tracking Google Sheets Template](https://docs.google.com/spreadsheets/d/1Ng14v-IQt59Q3Ktimy4e6UgFWp5q-t3A6-hEjoX3xSw/edit?usp=drivesdk)

## 📄 Sheet Overview

### `Date Marker`

* Choose how you want 'Master Inventory' to display your events (chronological or reverse chronological)
* Log **inventory events** (e.g., Restock, Sales)
* These populate dropdowns in inventory sheets

---

### `[Category] Inventory` (from `Accessories Inventory`)

* Duplicate `Accessories Inventory` and rename:

  ```
  [Category] Inventory
  ```

**Key features:**

* **A1 dropdown** → Selects category (auto-pulls from `Category Settings!A2:A`)
* Columns after **F** → Inventory events (from `Date Marker`)
* Enter **changes only** (+/-), not totals
* Column E → Auto-calculated current inventory

---

### `Master Inventory`

* Aggregates all sheets named:

  ```
  [Category] Inventory
  ```
* Central view + filtering tools

---

### `Manage Items`

* Add and manage items
* SKUs are generated automatically

---

### `Category Settings`

* Define:

  * Categories
  * Types/Sizes
  * Groups/Franchises
  * SKU prefixes
* Supports dropdowns across the sheet

---

### 🔒 Hidden Sheets

* `sort helper` → auto-sorts items
* `typeDropdown` → supports item dropdowns

---

## 🏷️ SKU Format

Readable, structured IDs based on:

```
Category + Type/Size + Group + Item Name
```

Example:

```
SH-LG-ANIME-DRAGONTEE
```

---

## 🚶 Core Workflows

### 1. Add a New Item

1. (If needed) Go to `Category Settings`

   * Add category, type/size, group, SKU prefixes
2. Go to `Manage Items`

   * Add item and individual ID → SKU auto-generates

---

### 2. Record Inventory Changes

1. Go to `Date Marker`

   * Create an event (e.g., "Restock April")
2. Go to `[Category] Inventory`

   * Select event in a new column (after F)
   * Enter **change values** (+/- only)
   * You may switch columns AFTER F around to suit your organization style, but A:F must remain in place.

✔️ Totals update automatically in Column E
❌ Do not enter totals manually

---

## ⚠️ Rules to Follow

* Sheet names must match:

  ```
  [Category] Inventory
  ```
* Do not edit formulas or hidden sheets
* Always log **events first**, then changes

---

If something breaks, check:

* Category setup in `Category Settings`
* Event created in `Date Marker`
