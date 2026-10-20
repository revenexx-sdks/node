```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsCreate({
    productId: '',
    rating: 1,
    authorFirstName: '', // optional
    authorLastName: '', // optional
    body: '', // optional
    contactId: '', // optional
    externalId: '', // optional
    externalRefs: {}, // optional
    locale: '', // optional
    market: '', // optional
    orderId: '', // optional
    productName: '', // optional
    publishedAt: '2026-01-01T12:00:00Z', // optional
    sku: '', // optional
    source: sdk.ReviewsReviewsCreateSource.Admin, // optional
    sourceData: {}, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    state: sdk.ReviewsReviewsCreateState.Pending, // optional
    title: '' // optional
});
```
