```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsSpend = new sdk.CampaignsSpend(client);

const result = await campaignsSpend.campaignsSpendList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    campaignId: '', // optional
    budgetId: '', // optional
    platform: '', // optional
    spendDate: '', // optional
    currency: '', // optional
    impressions: '', // optional
    clicks: '' // optional
});
```
