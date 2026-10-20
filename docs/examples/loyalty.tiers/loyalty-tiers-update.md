```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyTiers = new sdk.LoyaltyTiers(client);

const result = await loyaltyTiers.loyaltyTiersUpdate({
    id: '',
    active: true, // optional
    bonusPercent: 9.99, // optional
    code: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    labels: null, // optional
    metadata: null, // optional
    perks: null, // optional
    pointsMultiplier: 9.99, // optional
    position: 1, // optional
    programId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    thresholdKind: sdk.ThresholdKind.Absolute, // optional
    thresholdValue: 9.99 // optional
});
```
