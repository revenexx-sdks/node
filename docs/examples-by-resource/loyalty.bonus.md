# loyalty.bonus

## loyalty-bonus-list

List bonus agreements

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    programId: '', // optional
    membershipId: '', // optional
    organizationId: '', // optional
    period: '', // optional
    periodStart: '', // optional
    periodEnd: '', // optional
    baseSource: '', // optional
    turnoverSource: '', // optional
    reachedTierId: '', // optional
    reachedTierCode: '', // optional
    projectedTierCode: '', // optional
    currency: '', // optional
    state: '', // optional
    receivablesCleared: '', // optional
    receivablesCheckedBy: '', // optional
    forfeitReason: '', // optional
    documentRef: '', // optional
    payoutRef: '', // optional
    approvedBy: '', // optional
    externalId: '' // optional
});
```

## loyalty-bonus-create

Open the bonus agreement of a company for a year

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

## loyalty-bonus-get

Read one bonus agreement

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusGet({
    id: ''
});
```

## loyalty-bonus-update

Correct the base, the document or the turnover source of an agreement

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusUpdate({
    id: '',
    baseTurnover: 9.99, // optional
    documentRef: '', // optional
    metadata: null, // optional
    turnoverSource: sdk.TurnoverSource.Orders // optional
});
```

## loyalty-bonus-approve

Approve a calculated bonus

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusApprove({
    id: '',
    checkedBy: '', // optional
    receivablesCleared: true // optional
});
```

## loyalty-bonus-calculate

Calculate the bonus after the year has ended

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusCalculate({
    id: '',
    data: {}
});
```

## loyalty-bonus-forfeit

Forfeit a calculated bonus with a reason

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusForfeit({
    id: '',
    reason: ''
});
```

## loyalty-bonus-pay

Record that an approved bonus was paid

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusPay({
    id: '',
    payoutRef: '' // optional
});
```

## loyalty-bonus-progress

Read where a company stands in its bonus year

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusProgress({
    id: ''
});
```

## loyalty-bonus-rebuild

Read the year completed orders of the company into the agreement again

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusRebuild({
    id: '',
    data: {}
});
```

## loyalty-bonus-entries-list

List the turnover lines of agreements

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

## loyalty-bonus-entries-correct

Correct the turnover of an agreement by hand

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusEntriesCorrect({
    agreementId: '',
    amount: 9.99,
    ref: '',
    at: '2026-01-01T12:00:00Z', // optional
    key: '' // optional
});
```

## loyalty-bonus-entries-get

Read one turnover line

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusEntriesGet({
    id: ''
});
```

## loyalty-bonus-import

Import turnover figures from the ERP

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyBonus = new sdk.LoyaltyBonus(client);

const result = await loyaltyBonus.loyaltyBonusImport({
    rows: []
});
```
