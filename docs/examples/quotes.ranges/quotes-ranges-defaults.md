```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesRanges = new sdk.QuotesRanges(client);

const result = await quotesRanges.quotesRangesDefaults({
    library: [], // optional
    menus: [], // optional
    mode: sdk.PagesSeedMode.Fill, // optional
    pages: [], // optional
    settings: {} // optional
});
```
