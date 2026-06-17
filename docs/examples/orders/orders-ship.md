```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
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
