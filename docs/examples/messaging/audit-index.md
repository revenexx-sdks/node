```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const messaging = new sdk.Messaging(client);

const result = await messaging.auditIndex({
    resourceType: sdk.ResourceType.Template, // optional
    resourceId: '', // optional
    subject: '', // optional
    limit: 1 // optional
});
```
