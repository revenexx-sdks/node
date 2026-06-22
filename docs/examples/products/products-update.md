```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const products = new sdk.Products(client);

const result = await products.productsUpdate({
    id: '',
    attributeValues: {}, // optional
    completeness: {}, // optional
    deletedAt: '', // optional
    enabled: null, // optional
    familyId: '', // optional
    familyVariantId: '', // optional
    kind: '', // optional
    parentId: '', // optional
    quantifiedAssociations: {}, // optional
    sku: '', // optional
    taxClass: '' // optional
});
```
