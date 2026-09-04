```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const costCenters = new sdk.CostCenters(client);

const result = await costCenters.costCentersBudgetsAdjust({
    id: '',
    actor: '',
    amount: 9.99, // optional
    currency: '', // optional
    note: '', // optional
    target: 9.99 // optional
});
```
