```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersContacts = new sdk.CustomersContacts(client);

const result = await customersContacts.customersContactsCreate({
    email: 'einkauf@example.com',
    createdAt: '2026-01-01T12:00:00Z', // optional
    externalId: 'ASP000047', // optional
    firstName: 'Anna', // optional
    isPrimary: true, // optional
    jobTitle: 'Einkaufsleitung', // optional
    lastName: 'Berger', // optional
    locale: 'de-DE', // optional
    orderApprovalLimit: 25000, // optional
    orderApprovalMode: sdk.OrderApprovalMode.Limited, // optional
    organizationId: '', // optional
    phone: '+49 30 5550123', // optional
    registrationStatus: sdk.CustomersContactsCreateRegistrationStatus.Pending, // optional
    role: 'buyer', // optional
    status: sdk.ContactStatus.Invited // optional
});
```
