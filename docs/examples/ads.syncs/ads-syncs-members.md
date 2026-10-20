```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsSyncs = new sdk.AdsSyncs(client);

const result = await adsSyncs.adsSyncsMembers({
    id: '',
    cursor: '', // optional
    limit: 1 // optional
});
```
