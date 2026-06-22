```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orders = new sdk.Orders(client);

const result = await orders.ordersUpdate({
    id: '',
    billingAddress: {}, // optional
    buyer: {}, // optional
    customerOrderNumber: '', // optional
    metadata: {}, // optional
    shippingAddress: {}, // optional
    userData: {} // optional
});
```
