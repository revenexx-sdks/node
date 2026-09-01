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
    status: sdk.PaymentStatus.Created, // optional
    orderRef: 'ORD-10042', // optional
    methodCode: 'invoice', // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    provider: 'stripe', // optional
    dunningStage: sdk.PaymentDunningStage.None, // optional
    idempotencyKey: 'checkout-2f9c41' // optional
});
```
