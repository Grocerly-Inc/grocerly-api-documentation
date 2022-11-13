---
label: Product Categories
icon: stack
order: 1
---

You can fetch a list of all product categories and their subcategories programatically using the following endpoint:

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

---

Additionall all of the above mentioned categories are referenced by their IDs, and listed below:

| Category          | Category ID                | Subcategory                | Subcategory ID             |
| ----------------- | -------------------------- | -------------------------- | -------------------------- |
| Bakery            | `61dc4d05239ecc4395c5d0b5` |                            |                            |
|                   |                            | Bread                      | `61dc4d05239ecc4395c5d0b6` |
|                   |                            | Other                      | `61dc4d05239ecc4395c5d0b7` |
| Baby              | `636d9dd610a65a3c614a4a68` |                            |                            |
|                   |                            | Food                       | `61dc571c0001b2445694020a` |
|                   |                            | Hygiene                    | `61dc571c0001b2445694020b` |
|                   |                            | Laundry                    | `61dc571c0001b2445694020c` |
|                   |                            | Wipes                      | `61dc571c0001b2445694020d` |
|                   |                            | Toys & Accessories         | `636d9e0410a65a3c614a4a69` |
|                   |                            | Nappies                    | `636d9e6910a65a3c614a4a6a` |
|                   |                            | Other                      | `636d9e8110a65a3c614a4a6b` |
| Beverages         | `61dc4e890001b2445694016b` |                            |                            |
|                   |                            | Beer and Ciders            | `61dc4e890001b2445694016c` |
|                   |                            | Soft Drinks                | `61dc4e890001b2445694016d` |
|                   |                            | Juices and Shakes          | `61dc4e890001b2445694016e` |
|                   |                            | Water                      | `61dc4e890001b2445694016f` |
|                   |                            | Tea and Coffee             | `61dc4e890001b24456940170` |
|                   |                            | Spirits                    | `61dc4e890001b24456940171` |
|                   |                            | Wine                       | `61dc4e890001b24456940172` |
|                   |                            | Energy Drinks              | `61dc4e890001b24456940173` |
|                   |                            | Other                      | `636da8b510a65a3c614a4a81` |
| Chilled and Dairy | `61dc4f740001b24456940182` |                            |                            |
|                   |                            | Milk                       | `61dc4f740001b24456940183` |
|                   |                            | Eggs                       | `61dc4f740001b24456940184` |
|                   |                            | Cooked Meats               | `61dc4f740001b24456940185` |
|                   |                            | Yoghurts & Desserts        | `61dc4f740001b24456940186` |
|                   |                            | Other                      | `61dc4f740001b24456940187` |
| Deli              | `61dc500e0001b2445694018d` |                            |                            |
|                   |                            | Cheese                     | `61dc500e0001b2445694018e` |
|                   |                            | Other                      | `61dc500e0001b2445694018f` |
| Frozen            | `61dc51d80001b244569401ae` |                            |                            |
|                   |                            | Chips and Potatoes         | `61dc51d80001b244569401af` |
|                   |                            | Pizza, Pasta and Pastries  | `61dc51d80001b244569401b0` |
|                   |                            | Meat and Alternatives      | `61dc51d80001b244569401b1` |
|                   |                            | Fish                       | `61dc51d80001b244569401b2` |
|                   |                            | Fruit and Vegetables       | `61dc51d80001b244569401b3` |
|                   |                            | Ice Cream & Desserts       | `61dc51d80001b244569401b4` |
|                   |                            | Other                      | `61dc51d80001b244569401b5` |
| Fruits and Veg    | `61dc52d10001b244569401bd` |                            |                            |
|                   |                            | Fruit                      | `61dc52d10001b244569401be` |
|                   |                            | Vegetables                 | `61dc52d10001b244569401bf` |
|                   |                            | Other                      | `61dc52d10001b244569401c0` |
| Health            | `636da38910a65a3c614a4a80` |                            |                            |
|                   |                            | Organic                    | `61dc55240001b244569401ea` |
|                   |                            | Gluten Free                | `61dc55240001b244569401eb` |
|                   |                            | Sugar Free                 | `61dc55240001b244569401ec` |
|                   |                            | Dietary Food               | `61dc55240001b244569401ed` |
|                   |                            | Other                      | `636dcffd16bd2d7b0729c62e` |
| Household         | `61dc55240001b244569401e9` |                            |                            |
|                   |                            | Cleaning                   | `61dc55240001b244569401ea` |
|                   |                            | Dishwash                   | `61dc55240001b244569401eb` |
|                   |                            | Laundry                    | `61dc55240001b244569401ec` |
|                   |                            | Tissues                    | `61dc55240001b244569401ed` |
|                   |                            | Fragrances                 | `61dc55240001b244569401ee` |
|                   |                            | Stationery                 | `61dc55240001b244569401ef` |
|                   |                            | Garden & Plants            | `61dc55240001b244569401f0` |
|                   |                            | DIY                        | `61dc55240001b244569401f1` |
|                   |                            | Other                      | `61dc55240001b244569401f2` |
| Meat and Fish     | `61dc4ef50001b24456940176` |                            |                            |
|                   |                            |                            |                            |
| Pantry            | `61dc53c20001b244569401c9` |                            |                            |
|                   |                            | Pasta and Rice             | `61dc53c20001b244569401ca` |
|                   |                            | Dips and Spreads           | `61dc53c20001b244569401cb` |
|                   |                            | Tinned Goods               | `61dc53c20001b244569401cc` |
|                   |                            | Herbs & Spices             | `61dc53c20001b244569401cd` |
|                   |                            | Oil and Vinegars           | `61dc53c20001b244569401ce` |
|                   |                            | Sauces                     | `61dc53c20001b244569401cf` |
|                   |                            | Soups                      | `61dc53c20001b244569401d0` |
|                   |                            | Dried Fruits and Nuts      | `61dc53c20001b244569401d1` |
|                   |                            | Flour                      | `61dc53c20001b244569401d2` |
|                   |                            | Baking                     | `61dc53c20001b244569401d3` |
|                   |                            | Sugar and Sweetners        | `61dc53c20001b244569401d4` |
|                   |                            | Pickles, Chutneys & Olives | `61dc53c20001b244569401d5` |
|                   |                            | Wraps                      | `61dc53c20001b244569401d6` |
|                   |                            | Cereals                    | `61dc53c20001b244569401d7` |
|                   |                            | Ready Meals                | `61dc53c20001b244569401d8` |
|                   |                            | World Food                 | `61dc53c20001b244569401d9` |
|                   |                            | Seasonal Food              | `61dc53c20001b244569401da` |
|                   |                            | Other                      | `61dc53c20001b244569401db` |
| Pet               | `61dc571c0001b24456940209` |                            |                            |
|                   |                            | Cat Food                   | `61dc571c0001b2445694020a` |
|                   |                            | Dog Food                   | `61dc571c0001b2445694020b` |
|                   |                            | Other Pet Food             | `61dc571c0001b2445694020c` |
|                   |                            | Hygeine                    | `61dc571c0001b2445694020d` |
|                   |                            | Toys & Accessories         | `636d9f1910a65a3c614a4a6c` |
|                   |                            | Other                      | `636d9f3610a65a3c614a4a6d` |
| Snacks            | `61dc56d00001b24456940200` |                            |                            |
|                   |                            | Chocolate                  | `61dc56d00001b24456940201` |
|                   |                            | Sweets                     | `636da27f10a65a3c614a4a7a` |
|                   |                            | Crisps                     | `636da29710a65a3c614a4a7b` |
|                   |                            | Cereals                    | `636da2b210a65a3c614a4a7c` |
|                   |                            | Cakes                      | `636da2cd10a65a3c614a4a7d` |
|                   |                            | Biscuits                   | `636da2ed10a65a3c614a4a7e` |
|                   |                            | Other                      | `636da30010a65a3c614a4a7f` |
| Toileteries       | `61dc56ee0001b24456940204` |                            |                            |
|                   |                            | Body and Face Care         | `61dc56ee0001b24456940205` |
|                   |                            | Bath and Shower Gels       | `61dc56ee0001b24456940206` |
|                   |                            | Oral Care                  | `636da0bc10a65a3c614a4a6e` |
|                   |                            | Hair Care                  | `636da0db10a65a3c614a4a6f` |
|                   |                            | Women's Deodorants         | `636da10310a65a3c614a4a70` |
|                   |                            | Men's Deodorants           | `636da12110a65a3c614a4a72` |
|                   |                            | Perfumes                   | `636da14510a65a3c614a4a73` |
|                   |                            | Feminine Care              | `636da16010a65a3c614a4a74` |
|                   |                            | Male Toiletaries           | `636da18a10a65a3c614a4a75` |
|                   |                            | Shaving Products           | `636da1a710a65a3c614a4a76` |
|                   |                            | Beauty                     | `636da1cd10a65a3c614a4a77` |
|                   |                            | Sun Care                   | `636da1df10a65a3c614a4a78` |
|                   |                            | Others                     | `636da1f410a65a3c614a4a79` |

---
