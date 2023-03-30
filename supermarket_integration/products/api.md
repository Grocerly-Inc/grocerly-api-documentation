---
label: Product API Sync
icon: sync
order: 3
---

These sections provide the necessary information required to **FIND**, **GET**, **CREATE**, **UPDATE** and **DELETE** products on the Grocerly system allowing you to synchronise your products.

> Please view the [Product Units](units.md) and [Product Categories](categories.md) pages for a full list of all available product units and categories.

---

#### Find a list of products

+++Request

```js [!badge variant="primary" text="POST"] /supermarket/products
// This will return a list of products that your supermarket has associated to the Grocerly app.
// By default it will only return the first 10 products.
// If you'd like to view more you can paginate through more by appending the url with the following query string
//
// ?hitsPerPage=10&page=1
```

+++ Response

```js
[
  {
    id: 'XXXXXXX' // Grocerly automatically generated Product ID
    barcode: 'XXXXXX',
    supermarketReferenceId: 'XXXXXX',
    name: 'Heinz Ketchup',
    price: 200,
    categoryId: 'XXXXXX',
    subcategoryId: 'XXXXXX',
    inStock: true,
    unitId: 'GRAM',
    measure: 100,
    minimumWeight: 50,
    isWeighed: false,
    photoUrl: "https://storage.googleapis.com/grocerly/image-example.png",
  },
  {
    id: 'XXXXXXX' // Grocerly automatically generated Product ID
    barcode: 'XXXXXX',
    supermarketReferenceId: 'XXXXXX',
    name: 'Heinz Ketchup',
    price: 200,
    categoryId: 'XXXXXX',
    subcategoryId: 'XXXXXX',
    inStock: true,
    unitId: 'GRAM',
    measure: 100,
    minimumWeight: 50,
    isWeighed: false,
    photoUrl: "https://storage.googleapis.com/grocerly/image-example.png",
  },
  ...

]
```

+++

---

#### Get a product

+++Request

```js [!badge variant="primary" text="POST"] /supermarket/products/$variableId
// The `variableId` can be any one of the following:
// 1. Grocerly ID
// 2. Product Barcode
// 3. Supermarket Reference ID
```

+++ Response

```js
{
  id: 'XXXXXXX' // Grocerly automatically generated Product ID
  barcode: 'XXXXXX',
  supermarketReferenceId: 'XXXXXX',
  name: 'Heinz Ketchup',
  price: 200,
  categoryId: 'XXXXXX',
  subcategoryId: 'XXXXXX',
  inStock: true,
  unitId: 'GRAM',
  measure: 100,
  minimumWeight: 50,
  isWeighed: false,
  photoUrl: "https://storage.googleapis.com/grocerly/image-example.png",
}
```

+++

---

#### Create a new product

+++ Request

```js [!badge variant="primary" text="POST"] /supermarket/products
{
  barcode: 'XXXXXX', // Replace with the product barcode
  supermarketReferenceId: 'XXXXXX' // Replace with your internal reference ID for this product
  name: 'Heinz Ketchup',
  price: 200, // In cents - Translates to 2 euro
  categoryId: 'XXXXXX', // View the Product Categories page for a full list of all possible categories
  subcategoryId: 'XXXXXX',
  inStock: true, // Whether an item is in stock
  unitId: 'GRAM', // View the Product Units page for a full list of all possible units
  measure: 100,
  isWeighed: false, //  Set to true if the product can be sold based on weight
  minimumWeight?: 50,
  photoUrl?: 'https://your-photo-url-here', // (Optional) Public product photo url
}
```

+++ Response

```js
{
  id: 'XXXXXXX' // Grocerly automatically generated Product ID
  barcode: 'XXXXXX',
  supermarketReferenceId: 'XXXXXX',
  name: 'Heinz Ketchup',
  price: 200,
  categoryId: 'XXXXXX',
  subcategoryId: 'XXXXXX',
  inStock: true,
  unitId: 'GRAM',
  measure: 100,
  minimumWeight: 50,
  isWeighed: false,
  photoUrl: "https://storage.googleapis.com/grocerly/image-example.png",
}
```

+++

---

#### Update an existing product

+++ Request

```js [!badge variant="warning" text="PUT"] /supermarket/product/:ID:REFERENCE_ID:BARCODE:
{
  barcode?: 'XXXXXX'
  name?: 'Another Ketchup',
  price?: 400, // In cents - Translates to 4 euro
  inStock?: true, // Whether an item is in stock
  photoUrl?: 'https://your-photo-url-here', // Public product photo url
  categoryId?: 'XXXXXX',
  subcategoryId?: 'XXXXXX',
  isWeighed?: true,
  unitId?: 'GRAM',
  measure?: 100,
}
```

+++ Response

```js
{
  id: 'XXXXXXX',
  barcode: 'XXXXXX',
  supermarketReferenceId: 'XXXXXXX',
  name: 'Another Ketchup',
  price: 400,
  categoryId: 'XXXXXX',
  subcategoryId: 'XXXXXX',
  inStock: true,
  unitId: 'GRAM',
  measure: 100,
  isWeighed: false,
  photoUrl: "https://storage.googleapis.com/grocerly/image-example.png",
}
```

+++

---

#### Delete a product

+++ Request

```js [!badge variant="danger" text="DELETE"] /supermarket/products/:ID:REFERENCE_ID:BARCODE:
// Empty body
```

+++ Response

```js
{
  success: true,
}
```

+++

---
