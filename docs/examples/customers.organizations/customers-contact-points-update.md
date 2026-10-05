```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersOrganizations = new sdk.CustomersOrganizations(client);

const result = await customersOrganizations.customersContactPointsUpdate({
    id: '',
    addressId: '', // optional
    email: 'rechnungen@example.com', // optional
    externalId: 'DSP-000047', // optional
    isPrimary: true, // optional
    kind: 'invoice', // optional
    organizationId: '', // optional
    phone: '+49 30 5550123', // optional
    position: 1 // optional
});
```
