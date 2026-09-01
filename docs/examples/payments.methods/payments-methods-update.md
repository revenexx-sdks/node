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
