```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesUpdate({
    id: '',
    active: true, // optional
    code: '', // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    kind: sdk.Kind.Active, // optional
    labels: null, // optional
    metadata: null, // optional
    ruleMatch: sdk.RuleMatch.All, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```
