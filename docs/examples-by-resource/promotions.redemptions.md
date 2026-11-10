# promotions.redemptions

## promotions-redemptions-commit

Commit a cart holds against the order it became

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsCommit({
    orderId: '',
    cartId: '', // optional
    contactId: '', // optional
    currency: '', // optional
    market: '', // optional
    orderNumber: '', // optional
    organizationId: '', // optional
    promotions: [], // optional
    redeemedBy: '', // optional
    terms: {} // optional
});
```

## promotions-redemptions-sweep

Clear away holds that stopped counting

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsSweep();
```

## promotions-redemptions-list

List redemptions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    promotionId: '', // optional
    voucherId: '', // optional
    voucherCode: '', // optional
    batchId: '', // optional
    cartId: '', // optional
    orderId: '', // optional
    orderNumber: '', // optional
    contactId: '', // optional
    organizationId: '', // optional
    redeemedBy: '', // optional
    state: '' // optional
});
```

## promotions-redemptions-get

Read one redemption

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsGet({
    id: ''
});
```

## promotions-redemptions-release

Give a cart or an order redemptions back

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsRelease({
    cartId: '', // optional
    orderId: '', // optional
    reason: sdk.PromotionsRedemptionsReleaseReason.CartReleased // optional
});
```

## promotions-redemptions-reserve

Hold a cart promotions so nobody else can spend them

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsRedemptions = new sdk.PromotionsRedemptions(client);

const result = await promotionsRedemptions.promotionsRedemptionsReserve({
    cartId: '',
    contactId: '', // optional
    currency: '', // optional
    fromCartId: '', // optional
    organizationId: '', // optional
    promotions: [], // optional
    redeemedBy: '' // optional
});
```

## promotions-redemptions-returns

Credit back what a return took out of an order

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
