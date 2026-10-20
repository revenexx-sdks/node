```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsList({
    id: '', // optional
    code: 'key_accounts', // optional
    position: 1, // optional
    active: true, // optional
    ruleMatch: sdk.RuleMatch.All, // optional
    memberType: sdk.MemberType.Organization, // optional
    rulesComputedAt: '2026-01-01T12:00:00Z', // optional
    externalId: 'PREISGRUPPE-03', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'vertrieb@example.com', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: '', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    trashed: sdk.Trashed.Exclude, // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```
