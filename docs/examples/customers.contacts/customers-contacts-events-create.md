```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersContacts = new sdk.CustomersContacts(client);

const result = await customersContacts.customersContactsEventsCreate({
    contactId: '',
    subject: 'Called about the annual requirement',
    actor: 'vertrieb@example.com', // optional
    kind: sdk.ContactActivityKind.Note, // optional
    note: 'Asked for a quote on the annual bolt requirement; call back in week 34.', // optional
    occurredAt: '2026-01-01T12:00:00Z' // optional
});
```
