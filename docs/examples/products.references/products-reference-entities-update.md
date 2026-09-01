```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsReferences = new sdk.ProductsReferences(client);

const result = await productsReferences.productsReferenceEntitiesUpdate({
    id: '',
    code: 'brand', // optional
    image: 'reference-entities/brand.svg', // optional
    labels: {
        "de": "Marke",
        "en": "Brand"
    } // optional
});
```
