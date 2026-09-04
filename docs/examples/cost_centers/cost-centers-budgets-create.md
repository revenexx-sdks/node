```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const costCenters = new sdk.CostCenters(client);

const result = await costCenters.costCentersBudgetsCreate({
    costCenterId: '',
    name: '',
    active: true, // optional
    initialValue: 9.99, // optional
    metadata: {}, // optional
    periodLength: 1, // optional
    periodStart: '2026-01-01', // optional
    recurring: true, // optional
    sequence: 1, // optional
    takeover: {} // optional
});
```
