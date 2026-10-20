```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsCreate({
    code: '',
    labels: null,
    pointsCost: 1,
    programId: '',
    promotionId: '',
    active: true, // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    metadata: null, // optional
    minTierId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    voucherBatchId: '' // optional
});
```
