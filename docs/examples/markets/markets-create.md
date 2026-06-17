```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCreate({
    code: '',
    name: '',
    currency: '', // optional
    isDefault: null, // optional
    labels: {}, // optional
    position: null, // optional
    status: sdk.MarketStatus.Active // optional
});
```
