```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const carts = new sdk.Carts(client);

const result = await carts.cartsClaim({
    contactId: '',
    sessionKey: 'a1b2c3d4e5f6',
    strategy: sdk.CartMergeStrategy.Merge, // optional
    targetCartId: '' // optional
});
```
