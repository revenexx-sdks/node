```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersOrganizations = new sdk.CustomersOrganizations(client);

const result = await customersOrganizations.customersOrganizationsChangeCredit({
    id: '',
    reason: sdk.CustomersOrganizationsChangeCreditReason.RatingChanged,
    creditLimit: 9.99, // optional
    creditLimitMode: sdk.CreditLimitMode.Unset, // optional
    note: '' // optional
});
```
