```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsReferences = new sdk.ProductsReferences(client);

const result = await productsReferences.productsReferenceEntityRecordsUpdate({
    id: '',
    attributeValues: {
        "common": {
            "country": "DE",
            "founded": 1946
        },
        "locale_specific": {
            "de_DE": {
                "description": "Werkzeughersteller aus S\u00fcddeutschland."
            }
        }
    }, // optional
    code: 'acme_tools', // optional
    labels: {
        "de": "Acme Tools",
        "en": "Acme Tools"
    }, // optional
    referenceEntityId: '' // optional
});
```
