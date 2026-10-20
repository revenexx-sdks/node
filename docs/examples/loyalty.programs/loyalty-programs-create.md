```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsCreate({
    code: '',
    kind: sdk.LoyaltyProgramsCreateKind.Points,
    labels: null,
    active: true, // optional
    autoEnroll: true, // optional
    currency: '', // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    holder: sdk.Holder.Contact, // optional
    metadata: null, // optional
    period: sdk.Period.CalendarYear, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```
