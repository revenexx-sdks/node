# reviews.reviews

## reviews-reviews-list

List reviews

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    productId: '', // optional
    sku: '', // optional
    productName: '', // optional
    orderId: '', // optional
    orderNumber: '', // optional
    requestId: '', // optional
    contactId: '', // optional
    organizationId: '', // optional
    authorFirstName: '', // optional
    authorLastName: '', // optional
    rating: '', // optional
    title: '', // optional
    body: '', // optional
    locale: '', // optional
    market: '', // optional
    verifiedPurchase: '', // optional
    source: '', // optional
    state: '', // optional
    rejectionReason: '', // optional
    moderatedBy: '', // optional
    merchantReply: '', // optional
    repliedBy: '', // optional
    externalId: '' // optional
});
```

## reviews-reviews-create

Record a review by hand or from an import

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

## reviews-reviews-empty-trash

Empty the review trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsEmptyTrash();
```

## reviews-reviews-purge

Delete the reviews that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsPurge();
```

## reviews-reviews-delete

Move a review to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsDelete({
    id: ''
});
```

## reviews-reviews-get

Read one review

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsGet({
    id: ''
});
```

## reviews-reviews-restore

Bring a review back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsReviews = new sdk.ReviewsReviews(client);

const result = await reviewsReviews.reviewsReviewsRestore({
    id: ''
});
```
