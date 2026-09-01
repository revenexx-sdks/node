```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingMethods = new sdk.ShippingMethods(client);

const result = await shippingMethods.shippingTiersLadder({
    methodId: '',
    basePrice: 4.9,
    step: 5,
    toValue: 30,
    fromValue: 0, // optional
    replace: true, // optional
    stepPrice: 2 // optional
});
```
