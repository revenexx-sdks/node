```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tokens = new sdk.Tokens(client);

const result = await tokens.tokensList({
    bucketId: '',
    fileId: '',
    queries: [], // optional
    total: null // optional
});
```
