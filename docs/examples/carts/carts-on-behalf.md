```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const carts = new sdk.Carts(client);

const result = await carts.cartsOnBehalf({
    contactId: '',
    channel: sdk.CartOrderingChannel.Phone, // optional
    channelId: '', // optional
    currency: 'EUR', // optional
    name: 'Phone order', // optional
    note: 'Call back at 2 pm, deliver to plant north', // optional
    organizationId: '' // optional
});
```
