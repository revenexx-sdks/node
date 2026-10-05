```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesTrail = new sdk.QuotesTrail(client);

const result = await quotesTrail.quotesTrailAttach({
    id: '',
    fileRef: '',
    filename: '',
    byteSize: 1, // optional
    contentType: '', // optional
    direction: sdk.QuotesTrailAttachDirection.Buyer, // optional
    metadata: {}, // optional
    visibility: sdk.Visibility.Internal // optional
});
```
