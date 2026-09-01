```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const messaging = new sdk.Messaging(client);

const result = await messaging.statsIndex({
    days: 1, // optional
    from: '2026-01-01', // optional
    to: '2026-01-01' // optional
});
```
