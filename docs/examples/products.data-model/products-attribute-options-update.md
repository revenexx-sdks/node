```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsDataModel = new sdk.ProductsDataModel(client);

const result = await productsDataModel.productsAttributeOptionsUpdate({
    id: '',
    attributeId: '', // optional
    code: 'stainless_steel', // optional
    labels: {
        "de": "Edelstahl",
        "en": "Stainless steel"
    }, // optional
    position: 1, // optional
    swatch: {
        "hex": "#c0c0c0"
    } // optional
});
```
