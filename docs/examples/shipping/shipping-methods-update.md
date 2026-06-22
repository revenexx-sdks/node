```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shipping = new sdk.Shipping(client);

const result = await shipping.shippingMethodsUpdate({
    id: '',
    carrier: '', // optional
    code: '', // optional
    countries: [], // optional
    currency: '', // optional
    description: '', // optional
    enabled: null, // optional
    etaDaysMax: null, // optional
    etaDaysMin: null, // optional
    freeAbove: null, // optional
    labels: {}, // optional
    matrixAttribute: '', // optional
    matrixBasis: sdk.ShippingMethodMatrixBasis.Weight, // optional
    metadata: {}, // optional
    name: '', // optional
    position: null, // optional
    price: null, // optional
    pricingType: sdk.ShippingMethodPricingType.Fixed // optional
});
```
