```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsDataModel = new sdk.ProductsDataModel(client);

const result = await productsDataModel.productsMeasurementFamiliesUpdate({
    id: '',
    code: 'weight', // optional
    labels: {
        "de": "Gewicht",
        "en": "Weight"
    }, // optional
    standardUnit: 'kilogram', // optional
    units: [
        {
            "code": "kilogram",
            "convert_factor": 1,
            "symbol": "kg"
        },
        {
            "code": "gram",
            "convert_factor": 0.001,
            "symbol": "g"
        }
    ] // optional
});
```
