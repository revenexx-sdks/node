```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.createImport({
    app: '',
    entity: '',
    objectKey: '',
    vendor: '',
    format: sdk.Format.Csv, // optional
    keys: [], // optional
    maxRejects: 1, // optional
    mode: sdk.Mode.Upsert, // optional
    profileId: '', // optional
    target: sdk.CreateImportTarget.Live // optional
});
```
