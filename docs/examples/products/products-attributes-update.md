```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const products = new sdk.Products(client);

const result = await products.productsAttributesUpdate({
    id: '',
    code: '', // optional
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
    type: '', // optional
    usableInGrid: null, // optional
    validation: {} // optional
});
```
