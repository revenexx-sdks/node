```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orders = new sdk.Orders(client);

const result = await orders.ordersList({
    status: sdk.Status.Pending, // optional
    paymentStatus: sdk.PaymentStatus.Open, // optional
    fulfillmentStatus: sdk.FulfillmentStatus.Unfulfilled, // optional
    contactId: '', // optional
    organizationId: '', // optional
    channelId: '', // optional
    marketId: '', // optional
    number: '', // optional
    limit: null, // optional
    offset: null, // optional
    order: '' // optional
});
```
