# payments.methods

## payments-methods-list

List payment method configurations

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    code: 'invoice', // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    enabled: true, // optional
    provider: 'stripe' // optional
});
```

## payments-methods-create

Create a payment method configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsCreate({
    code: 'invoice',
    name: 'Invoice',
    countries: ["DE","AT"], // optional
    description: 'Pay within 14 days of the invoice date.', // optional
    enabled: true, // optional
    feeAmount: 2.5, // optional
    feeCurrency: 'EUR', // optional
    feeType: sdk.PaymentFeeType.None, // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    labels: {
        "de": "Rechnung",
        "en": "Invoice"
    }, // optional
    maxOrderValue: 2500, // optional
    metadata: {
        "erp_payment_key": "ZTRM01"
    }, // optional
    minOrderValue: 10, // optional
    position: 0, // optional
    provider: 'stripe', // optional
    providerMethod: 'card' // optional
});
```

## payments-methods-defaults

Seed the default methods and providers

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsDefaults();
```

## payments-methods-eligible

Resolve the methods eligible for a buyer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsEligible({
    amount: 49.9, // optional
    country: 'DE', // optional
    currency: 'EUR' // optional
});
```

## payments-methods-delete

Delete a payment method configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsDelete({
    id: ''
});
```

## payments-methods-get

Read one payment method configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsGet({
    id: ''
});
```

## payments-methods-update

Update a payment method configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsMethodsUpdate({
    id: '',
    code: 'invoice', // optional
    countries: ["DE","AT"], // optional
    description: 'Pay within 14 days of the invoice date.', // optional
    enabled: true, // optional
    feeAmount: 2.5, // optional
    feeCurrency: 'EUR', // optional
    feeType: sdk.PaymentFeeType.None, // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    labels: {
        "de": "Rechnung",
        "en": "Invoice"
    }, // optional
    maxOrderValue: 2500, // optional
    metadata: {
        "erp_payment_key": "ZTRM01"
    }, // optional
    minOrderValue: 10, // optional
    name: 'Invoice', // optional
    position: 0, // optional
    provider: 'stripe', // optional
    providerMethod: 'card' // optional
});
```

## payments-tax-classes-usage

Count the methods using a tax class

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsMethods = new sdk.PaymentsMethods(client);

const result = await paymentsMethods.paymentsTaxClassesUsage({
    code: 'reduced'
});
```
