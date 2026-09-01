```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersValueLists = new sdk.CustomersValueLists(client);

const result = await customersValueLists.customersLifecycleStagesCreate({
    code: '',
    title: 'Customer',
    description: 'Has ordered at least once and is being served.', // optional
    descriptions: {
        "de": "Hat mindestens einmal bestellt und wird betreut.",
        "en": "Has ordered at least once and is being served."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Kunde",
        "en": "Customer"
    }, // optional
    position: 1, // optional
    tone: sdk.Tone.Neutral // optional
});
```
