```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customers = new sdk.Customers(client);

const result = await customers.customersContactsList({
    organizationId: '', // optional
    role: '', // optional
    status: '', // optional
    email: '', // optional
    limit: null, // optional
    offset: null, // optional
    order: '' // optional
});
```
