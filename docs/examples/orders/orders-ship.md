```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orders = new sdk.Orders(client);

const result = await orders.ordersShip({
    id: '',
    carrier: '', // optional
    metadata: {}, // optional
    number: '', // optional
    positions: [], // optional
    shippedAt: '', // optional
    trackingCode: '', // optional
    trackingUrl: '' // optional
});
```
