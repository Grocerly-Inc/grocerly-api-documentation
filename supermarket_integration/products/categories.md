---
label: Product Categories
icon: stack
order: 1
---

All of the supported Product Categories are listed below:

| Category Name       | Category ID                |
| ------------------- | -------------------------- |
| Beverages           | `61dc4e890001b2445694016b` |
| Confectionary       | `61dc500e0001b2445694018d` |
| Butcher             | `61dc4ef50001b24456940176` |
| Chilled and Dairy   | `61dc4f740001b24456940182` |
| Groceries           | `61dc53c20001b244569401c9` |
| Organic             | `61dc56d00001b24456940200` |
| Personal Care       | `61dc56ee0001b24456940204` |
| Bakery              | `61dc4d05239ecc4395c5d0b5` |
| Fruits & Vegetables | `61dc52d10001b244569401bd` |
| Household           | `61dc55240001b244569401e9` |
| Wine Cellar         | `61dc57540001b24456940210` |
| Delicatessen        | `61dc50800001b24456940197` |
| Other               | `61dc8a0f23eebb0036795ea3` |
| Fish                | `61dc50c50001b244569401a2` |
| Frozen Foods        | `61dc51d80001b244569401ae` |
| Home Garden         | `61dc547a0001b244569401e1` |
| Pets                | `61dc571c0001b24456940209` |

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
  ];
}
```

+++
