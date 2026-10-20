```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysCreate({
    name: '',
    campaignRef: '', // optional
    currency: '', // optional
    description: '', // optional
    entry: '', // optional
    goalConfig: null, // optional
    metadata: null, // optional
    reenrol: true, // optional
    reenrolGapDays: 1, // optional
    steps: [], // optional
    triggerConfig: null, // optional
    triggerKind: sdk.TriggerKind.Event // optional
});
```
