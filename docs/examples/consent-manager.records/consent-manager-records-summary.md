```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRecords = new sdk.ConsentManagerRecords(client);

const result = await consentManagerRecords.consentManagerRecordsSummary({
    market: 'de', // optional
    from: '2026-01-01T00:00:00Z', // optional
    to: '2026-02-01T00:00:00Z' // optional
});
```
