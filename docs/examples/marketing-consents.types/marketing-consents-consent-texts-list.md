```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsList({
    id: '', // optional
    subscriptionTypeId: '', // optional
    version: 1, // optional
    locale: '', // optional
    wording: '', // optional
    publishedAt: '2026-01-01T12:00:00Z', // optional
    publishedBy: '', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: '', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: '', // optional
    trashed: sdk.Trashed.Exclude, // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```
