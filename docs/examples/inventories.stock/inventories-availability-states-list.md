```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const inventoriesStock = new sdk.InventoriesStock(client);

const result = await inventoriesStock.inventoriesAvailabilityStatesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    code: 'on_order', // optional
    title: 'On order', // optional
    description: 'Replenishment is on its way; the expected date says when.', // optional
    labels: '{}', // optional
    descriptions: '{}', // optional
    orderable: true, // optional
    isDefault: true, // optional
    tone: sdk.Tone.Neutral, // optional
    position: 1, // optional
    isSystem: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z' // optional
});
```
