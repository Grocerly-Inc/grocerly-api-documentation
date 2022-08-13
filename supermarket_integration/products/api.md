---
label: Product API Sync
icon: sync
order: 3
---

This sections provides the necessary information required to **CREATE**, **UPDATE** and **DELETE** products on the grocerly system allowing you to synchronise your products.

> Please view the [Product Units](units.md) and [Product Categories](categories.md) pages for a full list of all available product units and categories.

---

#### Create a new product

+++ Request

```
POST /supermarket/products/
Host: https://api.grocerly.store
X-API-KEY: :YOUR_API_KEY:
Content-Type: application/json
```

```js
{
  barcode: 'XXXXXX', // Must be unique
  name: "Heinz Ketchup",
  price: 200, // In cents - Translates to 2 euro
  categoryId: 'XXXXXX', // View the Product Categories page for a full list of all possible categories
  inStock: true, // Whether an item is in stock
  unit: 'GRAM', // View the Product Units page for a full list of all possible units
  weight: 100,
  isWeighed: false, //  Set to true if the product can be sold based on weight. Defaults to false if not provided
  image?: File, // (Optional) Buffer Array
}
```

+++

---

#### Update an existing product

+++ Request

```
PUT /supermarket/products/:PRODUCT_BARCODE:
Host: https://api.grocerly.store
X-API-KEY: :YOUR_API_KEY:
Content-Type: application/json
```

```js
{
  name: "Daniels Ketchup",
  price: 400, // In cents - Translates to 4 euro
  inStock: true, // Whether an item is in stock
  image?: File, // (Optional) Buffer Array
}
```

+++

---

#### Delete a product

+++ Request

```
DELETE /supermarket/products/:PRODUCT_ID:
Host: https://api.grocerly.store
X-API-KEY: :YOUR_API_KEY:
Content-Type: application/json
```

+++

---
