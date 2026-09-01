```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsEligible({
    amount: 49.9, // optional
    country: 'DE', // optional
    currency: 'EUR' // optional
});
```
