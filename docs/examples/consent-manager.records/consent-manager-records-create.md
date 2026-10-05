```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRecords = new sdk.ConsentManagerRecords(client);

const result = await consentManagerRecords.consentManagerRecordsCreate({
    action: sdk.Action.AcceptAll,
    consentId: '',
    locale: 'de',
    policyVersionId: '',
    surface: sdk.Surface.FirstLayer,
    clientTs: '2026-01-01T12:00:00Z', // optional
    decisions: {}, // optional
    pagePath: '/produkte/schrauben', // optional
    userAgentClass: 'Firefox 131' // optional
});
```
