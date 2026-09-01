```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const avatars = new sdk.Avatars(client);

const result = await avatars.avatarsGetFlag({
    code: sdk.AvatarsGetFlagCode.Af,
    width: 1, // optional
    height: 1, // optional
    quality: 1 // optional
});
```
