```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusCreate({
    organizationId: '',
    programId: '',
    baseTurnover: 9.99, // optional
    contactId: '', // optional
    documentRef: '', // optional
    period: '' // optional
});
```
