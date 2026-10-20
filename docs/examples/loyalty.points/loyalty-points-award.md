```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPoints = new sdk.LoyaltyPoints(client);

const result = await loyaltyPoints.loyaltyPointsAward({
    points: 1,
    contactId: '', // optional
    key: '', // optional
    membershipId: '', // optional
    organizationId: '', // optional
    programCode: '', // optional
    reason: '' // optional
});
```
