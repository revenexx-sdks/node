```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    provider: 'stripe', // optional
    enabled: true, // optional
    testMode: true // optional
});
```
