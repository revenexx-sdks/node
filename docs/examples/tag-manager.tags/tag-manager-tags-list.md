```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '', // optional
    id: '', // optional
    code: '', // optional
    name: '', // optional
    description: '', // optional
    kind: '', // optional
    registryKey: '', // optional
    scriptUrl: '', // optional
    vendorCode: '', // optional
    purposeCode: '', // optional
    load: '', // optional
    isActive: true, // optional
    createdAt: '', // optional
    updatedAt: '' // optional
});
```
