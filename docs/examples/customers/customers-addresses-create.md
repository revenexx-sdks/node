```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customers = new sdk.Customers(client);

const result = await customers.customersAddressesCreate({
    city: '',
    country: '',
    street: '',
    zip: '',
    company: '', // optional
    contactId: '', // optional
    isDefault: null, // optional
    name: '', // optional
    organizationId: '', // optional
    phone: '', // optional
    region: '', // optional
    street2: '', // optional
    type: sdk.AddressType.Billing // optional
});
```
