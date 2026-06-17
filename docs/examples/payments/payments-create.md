```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const payments = new sdk.Payments(client);

const result = await payments.paymentsCreate({
    amount: null,
    methodCode: '',
    cartId: '', // optional
    contactId: '', // optional
    country: '', // optional
    currency: '', // optional
    idempotencyKey: '', // optional
    metadata: {}, // optional
    orderRef: '', // optional
    returnUrl: '' // optional
});
```
