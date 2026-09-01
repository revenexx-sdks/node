```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersOrganizations = new sdk.CustomersOrganizations(client);

const result = await customersOrganizations.customersOrganizationsCreate({
    name: 'Beispiel Industrietechnik GmbH',
    branche: 'Maschinenbau', // optional
    creditLimit: 5000, // optional
    customerNumber: 'K-10042', // optional
    deliveryBlock: true, // optional
    lifecycleStage: 'customer', // optional
    paymentTerms: 'net_30', // optional
    priceList: 'standard', // optional
    settings: {
        "account_manager": "sales-north",
        "delivery_tour": "tuesday",
        "self_pickup": true
    }, // optional
    status: sdk.OrganizationStatus.Active, // optional
    vatId: 'DE123456789' // optional
});
```
