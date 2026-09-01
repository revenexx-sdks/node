```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const prices = new sdk.Prices(client);

const result = await prices.pricesEntriesAdjust({
    listId: '',
    amount: 9.99, // optional
    dryRun: true, // optional
    percent: 9.99, // optional
    rounding: sdk.PriceEndingRule.Exact, // optional
    skuPrefix: 'BOLT-' // optional
});
```
