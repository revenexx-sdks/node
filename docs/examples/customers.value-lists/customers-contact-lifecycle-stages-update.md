```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersValueLists = new sdk.CustomersValueLists(client);

const result = await customersValueLists.customersContactLifecycleStagesUpdate({
    id: '',
    active: true, // optional
    description: 'Showed an interest of their own — a form, a fair, a call.', // optional
    descriptions: {
        "de": "Hat selbst Interesse gezeigt.",
        "en": "Showed an interest of their own."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Lead",
        "en": "Lead"
    }, // optional
    position: 1, // optional
    title: 'Lead', // optional
    tone: sdk.Tone.Neutral // optional
});
```
