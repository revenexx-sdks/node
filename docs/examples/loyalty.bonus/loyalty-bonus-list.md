```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    programId: '', // optional
    membershipId: '', // optional
    organizationId: '', // optional
    period: '', // optional
    periodStart: '', // optional
    periodEnd: '', // optional
    baseSource: '', // optional
    turnoverSource: '', // optional
    reachedTierId: '', // optional
    reachedTierCode: '', // optional
    projectedTierCode: '', // optional
    currency: '', // optional
    state: '', // optional
    receivablesCleared: '', // optional
    receivablesCheckedBy: '', // optional
    forfeitReason: '', // optional
    documentRef: '', // optional
    payoutRef: '', // optional
    approvedBy: '', // optional
    externalId: '' // optional
});
```
