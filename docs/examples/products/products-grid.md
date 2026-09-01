```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const products = new sdk.Products(client);

const result = await products.productsGrid({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    q: 'cordless drill', // optional
    kind: sdk.Kind.Simple, // optional
    enabled: true, // optional
    familyId: '' // optional
});
```
