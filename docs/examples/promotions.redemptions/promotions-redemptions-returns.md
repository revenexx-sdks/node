```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsReturns({
    orderId: '',
    all: true, // optional
    lines: [], // optional
    remainingAmounts: {}, // optional
    remainingLines: [], // optional
    returnRef: '' // optional
});
```
