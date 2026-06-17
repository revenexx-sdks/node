```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const products = new sdk.Products(client);

const result = await products.productsProductAssociationsUpdate({
    id: '',
    associationTypeId: '', // optional
    position: null, // optional
    productId: '', // optional
    quantity: null, // optional
    targetProductId: '' // optional
});
```
