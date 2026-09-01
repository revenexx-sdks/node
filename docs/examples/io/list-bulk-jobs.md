```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.listBulkJobs({
    type: null, // optional
    status: null, // optional
    vendor: '', // optional
    app: '', // optional
    entity: '', // optional
    limit: 1 // optional
});
```
