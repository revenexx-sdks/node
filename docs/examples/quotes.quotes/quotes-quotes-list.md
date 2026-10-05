```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesQuotes = new sdk.QuotesQuotes(client);

const result = await quotesQuotes.quotesQuotesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    status: '', // optional
    origin: sdk.Origin.Buyer, // optional
    organizationId: '', // optional
    contactId: '', // optional
    ownerId: '', // optional
    cartId: '', // optional
    number: '', // optional
    externalId: 'ANG-20481' // optional
});
```
