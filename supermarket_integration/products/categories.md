---
label: Product Categories
icon: stack
order: 1
---

All of the supported Product Categories, referenced by their IDs, are listed below:

| Category ID                | Category Name       |
| -------------------------- | ------------------- |
| `61dc4e890001b2445694016b` | Beverages           |
| `61dc500e0001b2445694018d` | Confectionary       |
| `61dc4ef50001b24456940176` | Butcher             |
| `61dc4f740001b24456940182` | Chilled and Dairy   |
| `61dc53c20001b244569401c9` | Groceries           |
| `61dc56d00001b24456940200` | Organic             |
| `61dc56ee0001b24456940204` | Personal Care       |
| `61dc4d05239ecc4395c5d0b5` | Bakery              |
| `61dc52d10001b244569401bd` | Fruits & Vegetables |
| `61dc55240001b244569401e9` | Household           |
| `61dc57540001b24456940210` | Wine Cellar         |
| `61dc50800001b24456940197` | Delicatessen        |
| `61dc8a0f23eebb0036795ea3` | Other               |
| `61dc50c50001b244569401a2` | Fish                |
| `61dc51d80001b244569401ae` | Frozen Foods        |
| `61dc547a0001b244569401e1` | Home Garden         |
| `61dc571c0001b24456940209` | Pets                |

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
      id: '61dc4e890001b2445694016b',
      name: 'Beverages',
    },
    {
      id: '61dc500e0001b2445694018d',
      name: 'Confectionary',
    },
    {
      id: '61dc4ef50001b24456940176',
      name: 'Butcher',
    },
    {
      id: '61dc4f740001b24456940182',
      name: 'Chilled and Dairy',
    },
    ...
  ]
}
```

+++
