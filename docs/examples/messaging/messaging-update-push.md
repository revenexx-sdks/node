```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const messaging = new sdk.Messaging(client);

const result = await messaging.messagingUpdatePush({
    messageId: '',
    action: '', // optional
    badge: null, // optional
    body: '', // optional
    color: '', // optional
    contentAvailable: null, // optional
    critical: null, // optional
    data: {}, // optional
    draft: null, // optional
    icon: '', // optional
    image: '', // optional
    priority: sdk.Priority.Normal, // optional
    scheduledAt: '', // optional
    sound: '', // optional
    tag: '', // optional
    targets: [], // optional
    title: '', // optional
    topics: [], // optional
    users: [] // optional
});
```
