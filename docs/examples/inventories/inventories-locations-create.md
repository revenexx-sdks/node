```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const inventories = new sdk.Inventories(client);

const result = await inventories.inventoriesLocationsCreate({
    code: '',
    name: '',
    address: {}, // optional
    enabled: null, // optional
    labels: {}, // optional
    metadata: {}, // optional
    priority: null, // optional
    type: sdk.LocationType.Warehouse // optional
});
```
