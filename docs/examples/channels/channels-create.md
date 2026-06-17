```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsCreate({
    code: '',
    name: '',
    isDefault: null, // optional
    labels: {}, // optional
    position: null, // optional
    status: sdk.ChannelStatus.Active, // optional
    type: sdk.ChannelType.Storefront // optional
});
```
