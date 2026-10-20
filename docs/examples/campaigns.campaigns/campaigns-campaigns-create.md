```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsCampaigns = new sdk.CampaignsCampaigns(client);

const result = await campaignsCampaigns.campaignsCampaignsCreate({
    code: '',
    name: '',
    currency: '', // optional
    description: '', // optional
    endsAt: '2026-01-01T12:00:00Z', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    goalMetric: sdk.GoalMetric.Revenue, // optional
    goalValue: 9.99, // optional
    metadata: null, // optional
    ownerId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    startsAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.CampaignsCampaignsCreateStatus.Draft, // optional
    tags: null, // optional
    utmCampaign: '' // optional
});
```
