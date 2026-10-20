```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsFeeds = new sdk.AdsFeeds(client);

const result = await adsFeeds.adsFeedsUpdate({
    id: '',
    active: true, // optional
    destination: sdk.Destination.GoogleMerchantCenter, // optional
    feedId: '', // optional
    feedUrl: '', // optional
    label: '', // optional
    market: '', // optional
    metadata: null // optional
});
```
