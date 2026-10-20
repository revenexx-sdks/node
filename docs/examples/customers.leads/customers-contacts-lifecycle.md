```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersLeads = new sdk.CustomersLeads(client);

const result = await customersLeads.customersContactsLifecycle({
    contactId: '',
    stage: 'mql',
    actor: '', // optional
    leadSource: sdk.LeadSource.Form, // optional
    leadSourceRef: '', // optional
    reason: 'Downloaded the catalogue twice' // optional
});
```
