```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const punchout = new sdk.Punchout(client);

const result = await punchout.punchoutFieldMappingsImport({
    accountId: '',
    configuration: {},
    protocol: sdk.Protocol.Oci // optional
});
```
