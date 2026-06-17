```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const messaging = new sdk.Messaging(client);

const result = await messaging.messagingCreateMsg91Provider({
    name: '',
    providerId: '',
    authKey: '', // optional
    enabled: null, // optional
    senderId: '', // optional
    templateId: '' // optional
});
```
