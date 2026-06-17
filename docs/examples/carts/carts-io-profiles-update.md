```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const carts = new sdk.Carts(client);

const result = await carts.cartsIoProfilesUpdate({
    id: '',
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    direction: sdk.CartIoDirection.Import, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    isTemplate: null, // optional
    mapping: {}, // optional
    name: '', // optional
    options: {} // optional
});
```
