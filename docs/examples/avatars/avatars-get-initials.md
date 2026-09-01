```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const avatars = new sdk.Avatars(client);

const result = await avatars.avatarsGetInitials({
    name: 'Ada Lovelace', // optional
    width: 1, // optional
    height: 1, // optional
    background: '1a73e8' // optional
});
```
