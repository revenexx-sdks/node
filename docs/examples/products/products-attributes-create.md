```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const products = new sdk.Products(client);

const result = await products.productsAttributesCreate({
    code: '',
    type: '',
    config: {}, // optional
    entityRef: '', // optional
    entityType: '', // optional
    groupId: '', // optional
    isFilterable: null, // optional
    isUnique: null, // optional
    labels: {}, // optional
    localizable: null, // optional
    position: null, // optional
    scopable: null, // optional
    usableInGrid: null, // optional
    validation: {} // optional
});
```
