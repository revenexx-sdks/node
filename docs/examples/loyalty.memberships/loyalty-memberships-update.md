```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsUpdate({
    id: '',
    contactId: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    market: '', // optional
    metadata: null, // optional
    organizationId: '', // optional
    programId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.LoyaltyMembershipsCreateStatus.Active // optional
});
```
