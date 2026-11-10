# reviews.moderation

## reviews-moderation-publish

Publish a review

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsModeration = new sdk.ReviewsModeration(client);

const result = await reviewsModeration.reviewsModerationPublish({
    id: '',
    data: {}
});
```

## reviews-moderation-reject

Reject a review, or take a published one down

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsModeration = new sdk.ReviewsModeration(client);

const result = await reviewsModeration.reviewsModerationReject({
    id: '',
    reason: ''
});
```

## reviews-moderation-reply

Answer a review publicly, or remove the answer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const reviewsModeration = new sdk.ReviewsModeration(client);

const result = await reviewsModeration.reviewsModerationReply({
    id: '',
    reply: '' // optional
});
```
