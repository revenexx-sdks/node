```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shipping = new sdk.Shipping(client);

const result = await shipping.shippingMethodsCreate({
    code: '',
    name: '',
    carrier: '', // optional
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
    position: null, // optional
    price: null, // optional
    pricingType: sdk.ShippingMethodPricingType.Fixed // optional
});
```
