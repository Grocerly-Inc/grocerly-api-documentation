---
label: Product Categories
icon: stack
order: 1
---

All of the supported Product Categories, referenced by their IDs, are listed below:

| Category ID                | Category Name     |
| -------------------------- | ----------------- |
| `61dc4d05239ecc4395c5d0b5` | Bakery            |
| `61dc4ef50001b24456940176` | Meat and Fish     |
| `61dc52d10001b244569401bd` | Fruits and Veg    |
| `61dc51d80001b244569401ae` | Frozen            |
| `61dc4f740001b24456940182` | Chilled and Dairy |
| `61dc500e0001b2445694018d` | Deli              |
| `61dc53c20001b244569401c9` | Pantry            |
| `636da38910a65a3c614a4a80` | Health            |
| `61dc56d00001b24456940200` | Snacks            |
| `61dc4e890001b2445694016b` | Beverages         |
| `61dc55240001b244569401e9` | Household         |
| `61dc56ee0001b24456940204` | Toileteries       |
| `61dc571c0001b24456940209` | Pet               |
| `636d9dd610a65a3c614a4a68` | Baby              |

---

Additionally you can fetch the above list programatically using the following endpoint:

+++ Request

```js [!badge variant="success" text="GET"] /supermarket/product-categories
// Empty body
```

+++ Response

```js
{
  categories: [
    {
      "_id": "61dc4d05239ecc4395c5d0b5",
      "name": "Bakery",
      "photoUrl": null,
      "subcategories": [
          {
              "_id": "61dc4d05239ecc4395c5d0b6",
              "name": "Bread"
          },
          {
              "_id": "61dc4d05239ecc4395c5d0b7",
              "name": "Other"
          }
      ]
    },
    {
      "_id": "61dc4e890001b2445694016b",
      "name": "Beverages",
      "photoUrl": null,
      ...
    },
    ...
  ]
}
```

+++
