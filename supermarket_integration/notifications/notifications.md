---
label: Webhooks
icon: issue-opened
order: 2
---

Grocerly allows you to implement business logic that reacts to order journey events in real time. We notify you of these events by means of webhooks. By subscribing to certain events, we will notify your webhook as they happen.

> You can view supported [Events](events.md) over here.

#### Subscribe to Notifictions

+++ Request

```
POST /supermarket/webhook
Host: https://api.grocerly.store
X-API-KEY: :YOUR_API_KEY:
Content-Type: application/json
```

```js
{
  webhookUrl: 'XXXXXX'
  events: ['order_complete'] // For a full set of events visit the events page mentioned above.
}
```

+++

> A supermarket can only subscribe to events using a **single** webhook. If you would like to update the webhook url with a new one, simply re-run the above request.
