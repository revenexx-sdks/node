```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsCreate({
    externalAccountId: '',
    name: '',
    platform: sdk.Platform.Meta,
    clicksTotal: 1, // optional
    connectionRef: '', // optional
    conversionValueTotal: 9.99, // optional
    conversionsTotal: 1, // optional
    currency: '', // optional
    externalRefs: null, // optional
    figuresAt: '2026-01-01T12:00:00Z', // optional
    metadata: null, // optional
    roas: 9.99, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    spendTotal: 9.99 // optional
});
```
