```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsLinks = new sdk.AdsLinks(client);

const result = await adsLinks.adsLinksUpdate({
    id: '',
    adAccountId: '', // optional
    campaignId: '', // optional
    externalCampaignId: '', // optional
    externalName: '', // optional
    externalRefs: null, // optional
    metadata: null, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```
