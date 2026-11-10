# payments.ledger

## payments-list

List payments

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    cartId: '', // optional
    contactId: '', // optional
    orderId: '', // optional
    organizationId: '', // optional
    status: sdk.PaymentStatus.Created, // optional
    orderRef: 'ORD-10042', // optional
    methodCode: 'invoice', // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    provider: 'stripe', // optional
    dunningStage: sdk.PaymentDunningStage.None, // optional
    idempotencyKey: 'checkout-2f9c41', // optional
    externalId: 'ZAHL-4711', // optional
    reference: 'pi_29f4c1b7a3d24e10', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## payments-create

Create and authorize a payment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsCreate({
    amount: 49.9,
    methodCode: 'invoice',
    cartId: '', // optional
    contactId: '', // optional
    country: 'DE', // optional
    currency: 'EUR', // optional
    externalId: 'ZAHL-4711', // optional
    externalRefs: {
        "bank_statement": "AZ-88120",
        "erp_ledger": "BEL-2026-004417"
    }, // optional
    idempotencyKey: 'checkout-2f9c41', // optional
    metadata: {
        "order_source": "web"
    }, // optional
    orderId: '', // optional
    orderRef: 'ORD-10042', // optional
    returnUrl: 'https://shop.example.com/checkout/return', // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "Journal_Batch_Name": "ZAHLUNG",
            "Payment_Method_Code": "RECHNUNG"
        },
        "system": "business-central"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## payments-dunning-scan

Scan the dunning and webhook clocks

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsDunningScan();
```

## payments-errors-redact

Reclassify pre-taxonomy error messages

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsErrorsRedact({
    apply: true, // optional
    limit: 500 // optional
});
```

## payments-orders-relink

Link payments to the order their reference names

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsOrdersRelink({
    after: '2026-06-14T12:38:33.246Z', // optional
    apply: true, // optional
    limit: 100 // optional
});
```

## payments-orders-capture

Capture what an order owes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsOrdersCapture({
    orderRef: 'ORD-10042'
});
```

## payments-vocabularies-list

List vocabularies

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsVocabulariesList();
```

## payments-vocabularies-get

Read one vocabulary

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsVocabulariesGet({
    name: sdk.PaymentsVocabulariesGetName.Connectionstates
});
```

## payments-webhooks-ingest

Ingest a PSP webhook callback

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsWebhooksIngest({
    provider: 'stripe',
    id: null, // optional
    request: {}, // optional
    verified: null // optional
});
```

## payments-get

Read one payment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsGet({
    id: ''
});
```

## payments-cancel

Cancel a payment before capture

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsCancel({
    id: '',
    reason: 'Buyer cancelled by phone' // optional
});
```

## payments-capture

Capture an authorized payment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsCapture({
    id: ''
});
```

## payments-confirm

Finish a payment after the PSP redirect

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsConfirm({
    id: ''
});
```

## payments-refund

Refund a captured payment in full

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsLedger = new sdk.PaymentsLedger(client);

const result = await paymentsLedger.paymentsRefund({
    id: '',
    reason: 'Buyer cancelled by phone' // optional
});
```
