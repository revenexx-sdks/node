```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementApprovalRulesUpdate({
    id: '',
    active: true, // optional
    approverRef: '', // optional
    approverType: sdk.ApproverType.Contact, // optional
    condition: sdk.Condition.Always, // optional
    conditionParameters: {}, // optional
    costCenterId: '', // optional
    effect: sdk.Effect.PendingOrder, // optional
    effectParameters: {}, // optional
    metadata: {}, // optional
    name: '', // optional
    sequence: 1, // optional
    showCondition: true // optional
});
```
