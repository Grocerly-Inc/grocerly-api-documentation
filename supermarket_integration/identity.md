---
label: Identity
icon: note
order: 4
---

#### Fetch the supermarket

By default, Grocerly will have set up some information of your supermarket profile. You can fetch the identity information that Grocerly stores about the supermarket by using the following request:

+++ Request

```js [!badge variant="success" text="GET"] /supermarket/identity
// Empty body
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
      latitude: 33.92296519540646,
      longitude: 12.475051440278998,
      address: 'address',
      city: 'city',
      country: 'country',
  },
  contact: {
      email: 'info@yoursupermarket.com',
      phoneNumber: '+35612345678' // This will be used when the courier needs to contact the supermarket.
  }
}
```

+++

---

#### Update supermarket information

In order to update any out of date or additional information, you can use the request payload below.

+++ Request

```js [!badge variant="warning" text="PUT"] /supermarket/identity

{
    logo: File, // Array buffer
    location: {
      latitude: 33.92296519540646,
      longitude: 12.475051440278998,
      address: 'address',
      city: 'city',
      country: 'country',
    },
    contact: {
        email: 'info@yoursupermarket.com',
        phoneNumber: '+35612345678' // This will be used when the courier needs to contact the supermarket.
    }
}
```

+++ Response

```js
{
  success: true,
}
```

+++
