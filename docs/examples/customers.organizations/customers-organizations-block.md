```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersOrganizations = new sdk.CustomersOrganizations(client);

const result = await customersOrganizations.customersOrganizationsBlock({
    id: '',
    reason: sdk.CustomersOrganizationsBlockReason.PaymentOverdue,
    actor: '', // optional
    kind: sdk.CustomersOrganizationsBlockKind.Order, // optional
    note: '' // optional
});
```
