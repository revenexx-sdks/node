```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orderlists = new sdk.Orderlists(client);

const result = await orderlists.orderlistsKindsUpdate({
    id: '',
    description: 'Chemicals ordered against a standing lab protocol.', // optional
    descriptions: {
        "de": "Chemikalien, die nach einem festen Laborprotokoll bestellt werden.",
        "en": "Chemicals ordered against a standing lab protocol."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Reagenzienliste",
        "en": "Reagent list"
    }, // optional
    position: 2, // optional
    title: 'Reagent list', // optional
    tone: sdk.OrderListKindTone.Neutral // optional
});
```
