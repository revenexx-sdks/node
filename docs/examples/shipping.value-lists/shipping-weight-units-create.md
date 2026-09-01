```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsCreate({
    code: 't',
    factor: 1000,
    title: 'Tonne',
    description: 'When to pick this weight unit.', // optional
    descriptions: {
        "de": "Wann diese Option zu w\u00e4hlen ist.",
        "en": "When to pick this weight unit."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Tonne",
        "en": "Tonne"
    }, // optional
    position: 1, // optional
    tone: sdk.Tone.Neutral // optional
});
```
