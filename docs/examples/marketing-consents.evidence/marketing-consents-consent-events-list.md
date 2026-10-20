```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsConsentEventsList({
    id: '', // optional
    subscriptionId: '', // optional
    contactId: '', // optional
    subscriptionTypeId: '', // optional
    channel: sdk.Channel.Email, // optional
    addressHash: '', // optional
    kind: sdk.MarketingConsentsConsentEventsListKind.Requested, // optional
    source: sdk.MarketingConsentsConsentEventsListSource.Form, // optional
    sourceRef: '', // optional
    legalBasis: sdk.MarketingConsentsConsentEventsListLegalBasis.ConsentDoi, // optional
    consentTextId: '', // optional
    campaignRef: '', // optional
    pageUrl: '', // optional
    ip: '', // optional
    userAgent: '', // optional
    ipTruncatedAt: '2026-01-01T12:00:00Z', // optional
    at: '2026-01-01T12:00:00Z', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```
