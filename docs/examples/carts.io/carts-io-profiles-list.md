```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesList({
    id: '', // optional
    name: 'cart-export-csv', // optional
    direction: sdk.CartIoDirection.Import, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    isTemplate: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```
