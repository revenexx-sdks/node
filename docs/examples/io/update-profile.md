```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.updateProfile({
    id: '',
    app: '',
    direction: sdk.Direction.Import,
    entity: '',
    format: '',
    name: '',
    vendor: '',
    applyMode: sdk.ApplyMode.Upsert, // optional
    mapping: {}, // optional
    markets: [], // optional
    options: {} // optional
});
```
