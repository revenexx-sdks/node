```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const avatars = new sdk.Avatars(client);

const result = await avatars.avatarsGetFlag({
    code: sdk.Code.Af,
    width: null, // optional
    height: null, // optional
    quality: null // optional
});
```
