```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const payments = new sdk.Payments(client);

const result = await payments.paymentsMethodsCreate({
    code: '',
    name: '',
    countries: [], // optional
    description: '', // optional
    enabled: null, // optional
    feeAmount: null, // optional
    feeCurrency: '', // optional
    feeType: sdk.PaymentFeeType.None, // optional
    kind: sdk.PaymentMethodKind.SelfManaged, // optional
    labels: {}, // optional
    maxOrderValue: null, // optional
    metadata: {}, // optional
    minOrderValue: null, // optional
    position: null, // optional
    provider: '', // optional
    providerMethod: '' // optional
});
```
