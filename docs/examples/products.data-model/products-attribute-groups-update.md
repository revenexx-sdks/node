```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsDataModel = new sdk.ProductsDataModel(client);

const result = await productsDataModel.productsAttributeGroupsUpdate({
    id: '',
    code: 'technical_attributes', // optional
    labels: {
        "de": "Technische Attribute",
        "en": "Technical attributes"
    }, // optional
    position: 1 // optional
});
```
