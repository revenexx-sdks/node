```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const products = new sdk.Products(client);

const result = await products.productsAssociationTypesUpdate({
    id: '',
    code: '', // optional
    isQuantified: null, // optional
    isTwoWay: null, // optional
    labels: {} // optional
});
```
