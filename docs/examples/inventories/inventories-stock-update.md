```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const inventories = new sdk.Inventories(client);

const result = await inventories.inventoriesStockUpdate({
    id: '',
    locationId: '', // optional
    metadata: {}, // optional
    onHand: null, // optional
    productId: '', // optional
    reorderPoint: null, // optional
    reserved: null, // optional
    sku: '' // optional
});
```
