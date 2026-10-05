```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersValueLists = new sdk.CustomersValueLists(client);

const result = await customersValueLists.customersContactPointKindsUpdate({
    id: '',
    description: 'Where the invoice is sent.', // optional
    descriptions: {
        "de": "Wohin die Rechnung geschickt wird.",
        "en": "Where the invoice is sent."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Rechnung",
        "en": "Invoice"
    }, // optional
    position: 1, // optional
    title: 'Invoice', // optional
    tone: sdk.Tone.Neutral // optional
});
```
