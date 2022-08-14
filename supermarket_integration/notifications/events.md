---
label: Events
icon: pulse
order: 1
---

Based on the notifications you are subscribed to, Grocerly will **POST** the following payloads to the webhook you provided.

---

```js **order_completed**
{
    event: 'order_completed',
    orderNumber: 23,
    customer: {
        firstName: 'John',
        lastName: 'Doe',
        email: 'johndoe@example.com'
    },
    items: [ // Array of product items
        {
            barcode: 'XXXXXX',
            quantity: 2,
            price: 200, // Price in cents of the product at the time of placing an order.
        }
    ]
}
```
