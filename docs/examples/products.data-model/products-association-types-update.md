```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsDataModel = new sdk.ProductsDataModel(client);

const result = await productsDataModel.productsAssociationTypesUpdate({
    id: '',
    code: 'cross_sell', // optional
    isQuantified: true, // optional
    isTwoWay: true, // optional
    labels: {
        "de": "Querverkauf",
        "en": "Cross-sell"
    } // optional
});
```
