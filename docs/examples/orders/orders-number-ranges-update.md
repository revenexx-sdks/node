```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orders = new sdk.Orders(client);

const result = await orders.ordersNumberRangesUpdate({
    id: '',
    channelId: '', // optional
    code: '', // optional
    counter: null, // optional
    metadata: {}, // optional
    padding: null, // optional
    positionStep: null, // optional
    prefix: '', // optional
    step: null, // optional
    suffix: '' // optional
});
```
