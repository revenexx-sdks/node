```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsBudgets = new sdk.CampaignsBudgets(client);

const result = await campaignsBudgets.campaignsBudgetsUpdate({
    id: '',
    campaignId: '', // optional
    currency: '', // optional
    line: '', // optional
    notes: '', // optional
    planned: 9.99, // optional
    spent: 9.99 // optional
});
```
