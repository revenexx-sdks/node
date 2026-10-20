```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsCampaigns = new sdk.CampaignsCampaigns(client);

const result = await campaignsCampaigns.campaignsCampaignsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    code: '', // optional
    name: '', // optional
    description: '', // optional
    status: '', // optional
    effectiveState: '', // optional
    ownerId: '', // optional
    utmCampaign: '', // optional
    goalMetric: '', // optional
    currency: '', // optional
    ordersCount: '', // optional
    externalId: '' // optional
});
```
