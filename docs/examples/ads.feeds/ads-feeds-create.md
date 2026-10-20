```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsFeeds = new sdk.AdsFeeds(client);

const result = await adsFeeds.adsFeedsCreate({
    destination: sdk.Destination.GoogleMerchantCenter,
    market: '',
    active: true, // optional
    feedId: '', // optional
    feedUrl: '', // optional
    label: '', // optional
    metadata: null // optional
});
```
