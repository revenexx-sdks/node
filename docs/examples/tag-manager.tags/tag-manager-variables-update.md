```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVariablesUpdate({
    id: '',
    code: '', // optional
    constantValue: null, // optional
    kind: sdk.TagManagerVariablesCreateKind.EventField, // optional
    name: '', // optional
    path: '' // optional
});
```
