```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    code: 'invoice', // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    enabled: true, // optional
    provider: 'stripe' // optional
});
```
