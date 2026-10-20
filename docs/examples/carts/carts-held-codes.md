```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const carts = new sdk.Carts(client);

const result = await carts.cartsHeldCodes({
    code: 'FRUEHJAHR25,B2B-10', // optional
    status: 'active,abandoned', // optional
    limit: 1, // optional
    offset: 1 // optional
});
```
