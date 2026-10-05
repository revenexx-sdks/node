```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsCreate({
    chainedVendorCodes: [], // optional
    code: '', // optional
    config: {}, // optional
    description: '', // optional
    eventMap: {}, // optional
    isActive: true, // optional
    kind: sdk.TagManagerTagsCreateKind.Registry, // optional
    load: sdk.Load.Immediate, // optional
    name: '', // optional
    purposeCode: '', // optional
    registryKey: '', // optional
    scriptUrl: '', // optional
    vendorCode: '' // optional
});
```
