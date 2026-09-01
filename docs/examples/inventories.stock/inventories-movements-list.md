```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const inventoriesStock = new sdk.InventoriesStock(client);

const result = await inventoriesStock.inventoriesMovementsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    locationId: '', // optional
    productId: '', // optional
    sku: 'ACME-4711-BLK', // optional
    type: sdk.InventoriesMovementsListType.Inbound, // optional
    quantity: 5, // optional
    orderRef: 'SO-2026-000123', // optional
    reason: 'Delivery note 4711', // optional
    metadata: '{}', // optional
    createdAt: '2026-01-01T12:00:00Z' // optional
});
```
