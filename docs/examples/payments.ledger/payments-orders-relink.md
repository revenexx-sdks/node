```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsOrdersRelink({
    after: '2026-06-14T12:38:33.246Z', // optional
    apply: true, // optional
    limit: 100 // optional
});
```
