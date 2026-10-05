```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesRanges = new sdk.QuotesRanges(client);

const result = await quotesRanges.quotesRangesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```
