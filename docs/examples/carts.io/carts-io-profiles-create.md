```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesCreate({
    direction: sdk.CartIoDirection.Import,
    name: 'cart-export-csv',
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    isTemplate: true, // optional
    mapping: {}, // optional
    options: {} // optional
});
```
