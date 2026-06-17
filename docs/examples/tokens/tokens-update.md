```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tokens = new sdk.Tokens(client);

const result = await tokens.tokensUpdate({
    tokenId: '',
    expire: '' // optional
});
```
