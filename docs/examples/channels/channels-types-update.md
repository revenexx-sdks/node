```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsTypesUpdate({
    id: '',
    description: 'A web shop a human browses.', // optional
    descriptions: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    position: 1, // optional
    title: 'Product feed', // optional
    tone: sdk.ChannelTypeTone.Neutral // optional
});
```
