```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsManufacturers = new sdk.ProductsManufacturers(client);

const result = await productsManufacturers.productsManufacturersProducts({
    id: '',
    limit: 1, // optional
    offset: 1, // optional
    order: 'sku.asc' // optional
});
```
