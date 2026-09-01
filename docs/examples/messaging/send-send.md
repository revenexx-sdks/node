```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const messaging = new sdk.Messaging(client);

const result = await messaging.sendSend({
    channel: '',
    template: '',
    to: '',
    attachments: [], // optional
    data: {}, // optional
    draft: true, // optional
    locale: '', // optional
    market: '', // optional
    sendAt: '2026-01-01T12:00:00Z' // optional
});
```
