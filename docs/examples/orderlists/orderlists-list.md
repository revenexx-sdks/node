```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orderlists = new sdk.Orderlists(client);

const result = await orderlists.orderlistsList({
    ownerId: '', // optional
    organizationId: '', // optional
    kind: '', // optional
    limit: null, // optional
    offset: null, // optional
    order: '' // optional
});
```
