```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    name: '', // optional
    description: '', // optional
    status: '', // optional
    triggerKind: '', // optional
    reenrol: '', // optional
    reenrolGapDays: '', // optional
    campaignRef: '', // optional
    templateCode: '', // optional
    currentVersion: '', // optional
    draftVersion: '', // optional
    triggerRanOn: '', // optional
    enrolledCount: '', // optional
    activeCount: '' // optional
});
```
