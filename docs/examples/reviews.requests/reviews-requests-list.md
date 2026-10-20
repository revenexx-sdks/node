```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsRequests = new sdk.ReviewsRequests(client);

const result = await reviewsRequests.reviewsRequestsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    orderId: '', // optional
    orderNumber: '', // optional
    contactId: '', // optional
    organizationId: '', // optional
    state: '', // optional
    journeyRef: '', // optional
    market: '', // optional
    locale: '', // optional
    reviewedCount: '', // optional
    issuedCount: '' // optional
});
```
