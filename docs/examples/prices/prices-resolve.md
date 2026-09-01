```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const prices = new sdk.Prices(client);

const result = await prices.pricesResolve({
    items: [],
    at: '2026-03-15T09:00:00Z', // optional
    channelId: '', // optional
    contactId: '', // optional
    currency: 'EUR', // optional
    marketId: '', // optional
    organizationId: '' // optional
});
```
