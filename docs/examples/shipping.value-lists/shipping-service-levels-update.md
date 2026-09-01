```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsUpdate({
    id: '',
    description: 'When to pick this service level.', // optional
    descriptions: {
        "de": "Wann diese Option zu w\u00e4hlen ist.",
        "en": "When to pick this service level."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Night courier",
        "en": "Night courier"
    }, // optional
    position: 1, // optional
    title: 'Night courier', // optional
    tone: sdk.Tone.Neutral // optional
});
```
