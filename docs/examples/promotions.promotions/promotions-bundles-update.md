```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsPromotions = new sdk.PromotionsPromotions(client);

const result = await promotionsPromotions.promotionsBundlesUpdate({
    id: '',
    allocation: sdk.Allocation.BestForBuyer, // optional
    maxPerCart: 1, // optional
    name: '', // optional
    promotionId: '', // optional
    selectors: null, // optional
    unitsRequired: 1 // optional
});
```
