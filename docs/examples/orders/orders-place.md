```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orders = new sdk.Orders(client);

const result = await orders.ordersPlace({
    items: [],
    billingAddress: {}, // optional
    buyer: {}, // optional
    cartId: '', // optional
    channelId: '', // optional
    contactId: '', // optional
    currency: '', // optional
    customerOrderNumber: '', // optional
    grandTotal: null, // optional
    marketId: '', // optional
    metadata: {}, // optional
    organizationId: '', // optional
    payment: {}, // optional
    shipping: {}, // optional
    shippingAddress: {}, // optional
    shippingTotal: null, // optional
    userData: {} // optional
});
```
