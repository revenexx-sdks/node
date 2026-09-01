```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesUpdate({
    id: '',
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    direction: sdk.CartIoDirection.Import, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    isTemplate: true, // optional
    mapping: {}, // optional
    name: 'cart-export-csv', // optional
    options: {} // optional
});
```
