---
label: Events
icon: pulse
order: 1
---

Based on the notifications you are subscribed to, Grocerly will **POST** the following payloads to the webhook you provided.

---

Event: `order_completed`

```js
{
    event: 'order_completed',
    customer: {
        firstName: 'John',
        lastName: 'Doe',
        email: 'johndoe@example.com'
    },
    items: [
        {
            barcode: 'XXXXXX',
            quantity: 2,
        }
    ]
}
```
