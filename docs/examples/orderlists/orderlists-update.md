```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orderlists = new sdk.Orderlists(client);

const result = await orderlists.orderlistsUpdate({
    id: '',
    kind: 'shopping', // optional
    metadata: {
        "department": "facility",
        "erp_reference": "REQ-2026-0042"
    }, // optional
    name: 'Weekly office supplies', // optional
    shared: true // optional
});
```
