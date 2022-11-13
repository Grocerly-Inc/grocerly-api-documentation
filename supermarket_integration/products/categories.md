---
label: Product Categories
icon: stack
order: 1
---

All of the supported Product Categories, referenced by their IDs, are listed below:

| Category Name     | Category ID                | Subcategory Name | Subcategory ID           |
| ----------------- | -------------------------- | ---------------- | ------------------------ |
| Bakery            | `61dc4d05239ecc4395c5d0b5` |                  |                          |
|                   |                            | Bread            | 61dc4d05239ecc4395c5d0b6 |
|                   |                            | Other            | 61dc4d05239ecc4395c5d0b7 |
| Baby              | `636d9dd610a65a3c614a4a68` |                  |                          |
| Beverages         | `61dc4e890001b2445694016b` |                  |                          |
| Chilled and Dairy | `61dc4f740001b24456940182` |                  |                          |
| Deli              | `61dc500e0001b2445694018d` |                  |                          |
| Frozen            | `61dc51d80001b244569401ae` |                  |                          |
| Fruits and Veg    | `61dc52d10001b244569401bd` |                  |                          |
| Health            | `636da38910a65a3c614a4a80` |                  |                          |
| Household         | `61dc55240001b244569401e9` |                  |                          |
| Meat and Fish     | `61dc4ef50001b24456940176` |                  |                          |
| Pantry            | `61dc53c20001b244569401c9` |                  |                          |
| Pet               | `61dc571c0001b24456940209` |                  |                          |
| Snacks            | `61dc56d00001b24456940200` |                  |                          |
| Toileteries       | `61dc56ee0001b24456940204` |                  |                          |

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
      "id": "61dc4d05239ecc4395c5d0b5",
      "name": "Bakery",
      "subcategories": [
          {
              "id": "61dc4d05239ecc4395c5d0b6",
              "name": "Bread"
          },
          {
              "id": "61dc4d05239ecc4395c5d0b7",
              "name": "Other"
          }
      ]
    },
    {
      "id": "61dc4e890001b2445694016b",
      "name": "Beverages",
      ...
    },
    ...
  ]
}
```

+++
