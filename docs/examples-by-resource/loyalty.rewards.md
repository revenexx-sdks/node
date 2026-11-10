# loyalty.rewards

## loyalty-rewards-redemptions-list

List redeemed rewards

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsRedemptionsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    membershipId: '', // optional
    rewardId: '', // optional
    points: '', // optional
    voucherCode: '', // optional
    ledgerEntryId: '', // optional
    requestKey: '', // optional
    state: '', // optional
    usedOrderId: '' // optional
});
```

## loyalty-rewards-redemptions-get

Read one redeemed reward

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsRedemptionsGet({
    id: ''
});
```

## loyalty-rewards-list

List rewards

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    programId: '', // optional
    code: '', // optional
    description: '', // optional
    pointsCost: '', // optional
    promotionId: '', // optional
    voucherBatchId: '', // optional
    minTierId: '', // optional
    active: '', // optional
    redeemedCount: '', // optional
    externalId: '', // optional
    deletedBy: '', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeBlockedReason: '' // optional
});
```

## loyalty-rewards-create

Add a reward to a points programme

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsCreate({
    code: '',
    labels: null,
    pointsCost: 1,
    programId: '',
    promotionId: '',
    active: true, // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    metadata: null, // optional
    minTierId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    voucherBatchId: '' // optional
});
```

## loyalty-rewards-empty-trash

Empty the reward trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsEmptyTrash();
```

## loyalty-rewards-purge

Delete the rewards that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsPurge();
```

## loyalty-rewards-delete

Move a reward to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsDelete({
    id: ''
});
```

## loyalty-rewards-get

Read one reward

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsGet({
    id: ''
});
```

## loyalty-rewards-update

Correct a reward

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsUpdate({
    id: '',
    active: true, // optional
    code: '', // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    labels: null, // optional
    metadata: null, // optional
    minTierId: '', // optional
    pointsCost: 1, // optional
    programId: '', // optional
    promotionId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    voucherBatchId: '' // optional
});
```

## loyalty-rewards-redeem

Redeem points for a reward voucher

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsRedeem({
    id: '',
    contactId: '', // optional
    key: '', // optional
    membershipId: '', // optional
    organizationId: '' // optional
});
```

## loyalty-rewards-restore

Bring a reward back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyRewards = new sdk.LoyaltyRewards(client);

const result = await loyaltyRewards.loyaltyRewardsRestore({
    id: ''
});
```
