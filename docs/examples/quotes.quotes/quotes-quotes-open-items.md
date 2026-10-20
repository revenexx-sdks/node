```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesQuotes = new sdk.QuotesQuotes(client);

const result = await quotesQuotes.quotesQuotesOpenItems({
    productId: '',
    status: 'requested,in_review,quoted,partially_accepted', // optional
    limit: 50, // optional
    offset: 0 // optional
});
```
