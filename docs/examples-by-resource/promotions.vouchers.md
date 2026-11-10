# promotions.vouchers

## promotions-batches-list

List code batches

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

## promotions-batches-create

Create a code batch

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesCreate({
    name: '',
    promotionId: '',
    alphabet: '', // optional
    metadata: null, // optional
    pattern: '', // optional
    requestRef: '', // optional
    requested: 1, // optional
    status: sdk.PromotionsBatchesCreateStatus.Active // optional
});
```

## promotions-batches-delete

Delete a batch

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesDelete({
    id: ''
});
```

## promotions-batches-get

Read one batch

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesGet({
    id: ''
});
```

## promotions-batches-update

Correct a batch

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesUpdate({
    id: '',
    alphabet: '', // optional
    metadata: null, // optional
    name: '', // optional
    pattern: '', // optional
    promotionId: '', // optional
    requestRef: '', // optional
    requested: 1, // optional
    status: sdk.PromotionsBatchesCreateStatus.Active // optional
});
```

## promotions-batches-disable

Switch a batch and every code in it off

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesDisable({
    id: ''
});
```

## promotions-batches-export

Export a batch codes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesExport({
    id: ''
});
```

## promotions-batches-export-file

Export a batch codes as a CSV file

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesExportFile({
    id: ''
});
```

## promotions-batches-generate

Generate codes into a batch

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesGenerate({
    id: '',
    count: 1,
    alphabet: '', // optional
    pattern: '', // optional
    requestRef: '', // optional
    usageLimit: 1 // optional
});
```

## promotions-batches-generate-for

Generate one code per named recipient

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesGenerateFor({
    id: '',
    recipients: []
});
```

## promotions-batches-import

Import existing codes unchanged

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsBatchesImport({
    id: '',
    codes: [],
    usageLimit: 1 // optional
});
```

## promotions-voucher-reservations-list

List code reservations

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVoucherReservationsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    voucherId: '', // optional
    contactId: '', // optional
    organizationId: '' // optional
});
```

## promotions-voucher-reservations-create

Hold a code for a buyer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVoucherReservationsCreate({
    voucherId: '',
    contactId: '', // optional
    expiresAt: '2026-01-01T12:00:00Z', // optional
    organizationId: '' // optional
});
```

## promotions-voucher-reservations-delete

Release a reservation

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVoucherReservationsDelete({
    id: ''
});
```

## promotions-voucher-reservations-get

Read one reservation

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVoucherReservationsGet({
    id: ''
});
```

## promotions-voucher-reservations-update

Correct a reservation

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVoucherReservationsUpdate({
    id: '',
    contactId: '', // optional
    expiresAt: '2026-01-01T12:00:00Z', // optional
    organizationId: '', // optional
    voucherId: '' // optional
});
```

## promotions-vouchers-list

List voucher codes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVouchersList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    promotionId: '', // optional
    batchId: '', // optional
    code: '', // optional
    codeKey: '', // optional
    status: '', // optional
    usageLimit: '', // optional
    usageCount: '', // optional
    currency: '', // optional
    contactId: '', // optional
    organizationId: '', // optional
    reservationRequired: '' // optional
});
```

## promotions-vouchers-create

Issue a voucher code

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVouchersCreate({
    code: '',
    promotionId: '',
    batchId: '', // optional
    contactId: '', // optional
    currency: '', // optional
    endsAt: '2026-01-01T12:00:00Z', // optional
    metadata: null, // optional
    organizationId: '', // optional
    reservationLimit: 1, // optional
    reservationRequired: true, // optional
    residualValue: 9.99, // optional
    startsAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.PromotionsBatchesCreateStatus.Active, // optional
    usageLimit: 1 // optional
});
```

## promotions-vouchers-delete

Delete a voucher that was never redeemed

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVouchersDelete({
    id: ''
});
```

## promotions-vouchers-get

Read one voucher

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVouchersGet({
    id: ''
});
```

## promotions-vouchers-update

Correct a voucher

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsVouchers = new sdk.PromotionsVouchers(client);

const result = await promotionsVouchers.promotionsVouchersUpdate({
    id: '',
    batchId: '', // optional
    code: '', // optional
    contactId: '', // optional
    currency: '', // optional
    endsAt: '2026-01-01T12:00:00Z', // optional
    metadata: null, // optional
    organizationId: '', // optional
    promotionId: '', // optional
    reservationLimit: 1, // optional
    reservationRequired: true, // optional
    residualValue: 9.99, // optional
    startsAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.PromotionsBatchesCreateStatus.Active, // optional
    usageLimit: 1 // optional
});
```
