```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusEntriesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    agreementId: '', // optional
    entryKey: '', // optional
    source: '', // optional
    ref: '', // optional
    orderId: '' // optional
});
```
