```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleStore({
    sftpAccountId: '',
    sourcePath: '/uploads',
    enabled: true, // optional
    options: [], // optional
    schedule: '0 3 * * *', // optional
    targetFolderId: '' // optional
});
```
