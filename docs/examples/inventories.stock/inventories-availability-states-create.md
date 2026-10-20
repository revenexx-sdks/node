```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const inventoriesStock = new sdk.InventoriesStock(client);

const result = await inventoriesStock.inventoriesAvailabilityStatesCreate({
    code: 'on_order',
    title: 'On order',
    active: true, // optional
    description: 'Replenishment is on its way; the expected date says when.', // optional
    descriptions: {
        "de": "Nachschub ist unterwegs.",
        "en": "Replenishment is on its way."
    }, // optional
    isDefault: true, // optional
    isSystem: true, // optional
    labels: {
        "de": "Bestellt",
        "en": "On order"
    }, // optional
    orderable: true, // optional
    position: 1, // optional
    tone: sdk.AvailabilityStateTone.Info // optional
});
```
