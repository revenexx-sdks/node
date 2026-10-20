```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesCreate({
    code: 'newsletter',
    labels: {
        "de": "Newsletter",
        "en": "Newsletter"
    },
    allowsExistingCustomer: true, // optional
    channels: [sdk.Channels.Email, sdk.Channels.Sms], // optional
    descriptions: {}, // optional
    position: 10, // optional
    requiresDoi: true, // optional
    similarGoodsNote: {
        "de": "Ersatzteile und Zubeh\u00f6r zu gekauften Ger\u00e4ten.",
        "en": "Spare parts and accessories for purchased devices."
    } // optional
});
```
