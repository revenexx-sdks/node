```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const carts = new sdk.Carts(client);

const result = await carts.cartsUpdate({
    id: '',
    channelId: '', // optional
    currency: '', // optional
    marketId: '', // optional
    metadata: {}, // optional
    name: '' // optional
});
```
