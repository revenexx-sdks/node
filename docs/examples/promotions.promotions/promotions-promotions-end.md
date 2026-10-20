```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsPromotions = new sdk.PromotionsPromotions(client);

const result = await promotionsPromotions.promotionsPromotionsEnd({
    id: '',
    at: '2026-01-01T12:00:00Z', // optional
    honourReservations: true, // optional
    when: sdk.When.Now // optional
});
```
