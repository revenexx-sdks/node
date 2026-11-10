# loyalty.points

## loyalty-points-list

List point bookings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPoints = new sdk.LoyaltyPoints(client);

const result = await loyaltyPoints.loyaltyPointsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    membershipId: '', // optional
    entryKey: '', // optional
    kind: '', // optional
    points: '', // optional
    remaining: '', // optional
    orderId: '', // optional
    rewardId: '', // optional
    redemptionId: '', // optional
    reason: '' // optional
});
```

## loyalty-points-get

Read one point booking

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPoints = new sdk.LoyaltyPoints(client);

const result = await loyaltyPoints.loyaltyPointsGet({
    id: ''
});
```

## loyalty-points-award

Credit points to a member for a reason

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
