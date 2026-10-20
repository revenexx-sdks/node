```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsUpdate({
    id: '',
    clicksTotal: 1, // optional
    connectionRef: '', // optional
    conversionValueTotal: 9.99, // optional
    conversionsTotal: 1, // optional
    currency: '', // optional
    externalAccountId: '', // optional
    externalRefs: null, // optional
    figuresAt: '2026-01-01T12:00:00Z', // optional
    metadata: null, // optional
    name: '', // optional
    platform: sdk.Platform.Meta, // optional
    roas: 9.99, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    spendTotal: 9.99 // optional
});
```
