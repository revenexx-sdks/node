# customers.leads

## customers-consent-mirror-run

Bring the marketing consent flag up to date

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersLeads = new sdk.CustomersLeads(client);

const result = await customersLeads.customersConsentMirrorRun();
```

## customers-contacts-handover

Hand a lead to a sales rep

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersLeads = new sdk.CustomersLeads(client);

const result = await customersLeads.customersContactsHandover({
    contactId: '',
    ownerId: 'AD-07',
    actor: '', // optional
    dueAt: '2026-01-01T12:00:00Z', // optional
    note: '', // optional
    subject: '' // optional
});
```

## customers-contacts-lifecycle

Move a person to another funnel stage

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
