```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orders = new sdk.Orders(client);

const result = await orders.ordersReturn({
    id: '',
    metadata: {
        "rma_portal_case": "C-2026-0917"
    }, // optional
    positions: [], // optional
    reason: 'Damaged on arrival', // optional
    restock: true // optional
});
```
