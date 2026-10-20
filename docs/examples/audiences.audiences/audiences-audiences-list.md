```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    code: '', // optional
    description: '', // optional
    kind: '', // optional
    ruleMatch: '', // optional
    active: '', // optional
    memberCount: '', // optional
    eligibleCount: '', // optional
    rulesSummary: '', // optional
    recomputeState: '', // optional
    recomputeError: '', // optional
    frozenFromId: '' // optional
});
```
