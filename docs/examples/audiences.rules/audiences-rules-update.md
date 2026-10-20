```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesRules = new sdk.AudiencesRules(client);

const result = await audiencesRules.audiencesRulesUpdate({
    id: '',
    audienceId: '', // optional
    channel: sdk.Channel.Email, // optional
    field: '', // optional
    kind: sdk.AudiencesRulesCreateKind.Group, // optional
    matchMode: sdk.MatchMode.All, // optional
    negate: true, // optional
    operator: '', // optional
    parentId: '', // optional
    position: 1, // optional
    subject: '', // optional
    value: null, // optional
    valueTo: null, // optional
    windowDays: 1 // optional
});
```
