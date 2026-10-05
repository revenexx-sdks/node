```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    promotionId: '', // optional
    name: '', // optional
    pattern: '', // optional
    alphabet: '', // optional
    requested: '', // optional
    createdCount: '', // optional
    redeemedCount: '', // optional
    status: '', // optional
    requestRef: '' // optional
});
```
