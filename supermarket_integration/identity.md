---
label: Identity
icon: note
order: 4
---

#### Fetch the supermarket

By default, The Grocerly Team will have set up some information of your supermarket profile. You can fetch the identity information that Grocerly stores about the supermarket by using the following request:


+++ Request

```
GET /supermarket/identity
Host: https://api.grocerly.store
X-API-KEY: :YOUR_API_KEY:
Content-Type: application/json
```

+++ Response

```js
{
  name: 'Your Supermarket',
  domain: 'https://yoursupermarket.com',
  timezone: 'Europe/Malta',
  logoUrl: 'https://storage.googleapis.com/grocerly/your-supermarket.png',
  currencyCode: 'EUR',
  location: {
      latitude: 35.92296519540646,
      longitude: 14.475051440278998,
      address: 'Uqija Street, Ibragg',
      city: 'Swieqi',
      country: 'Malta',
  },
  contact: {
      email: 'info@yoursupermarket.com',
      phoneNumber: '+35677486469' // This will be used when the courier needs to contact the supermarket.
  }
}
```
+++

---

#### Update supermarket information

In order to update any out of date or additional information, you can use the request payload below.

```
PUT /supermarket/identity
Host: https://api.grocerly.store
X-API-KEY: :YOUR_API_KEY:
Content-Type: application/json
```

Request Payload:

```js
{
    logo: File, // Array buffer
    location: {
      latitude: 35.92296519540646,
      longitude: 14.475051440278998,
      address: 'Uqija Street, Ibragg',
      city: 'Swieqi',
      country: 'Malta',
    },
    contact: {
        email: 'info@yoursupermarket.com',
        phoneNumber: '+35677486469' // This will be used when the courier needs to contact the supermarket.
    }
}
```
