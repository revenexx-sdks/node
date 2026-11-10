# promotions.evaluation

## promotions-evaluation-available

List the promotions this buyer could still reach

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsEvaluation = new sdk.PromotionsEvaluation(client);

const result = await promotionsEvaluation.promotionsEvaluationAvailable({
    currency: '',
    channel: '', // optional
    contactId: '', // optional
    itemCount: 1, // optional
    lines: [], // optional
    market: '', // optional
    organizationId: '', // optional
    paymentFee: 9.99, // optional
    precision: 1, // optional
    rounding: '', // optional
    shipping: 9.99, // optional
    subtotal: 9.99, // optional
    taxIncluded: true // optional
});
```

## promotions-evaluation-check-code

Say whether one code is live, without a cart

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsEvaluation = new sdk.PromotionsEvaluation(client);

const result = await promotionsEvaluation.promotionsEvaluationCheckCode({
    code: '',
    contactId: '' // optional
});
```

## promotions-evaluation-evaluate

Answer what a priced cart is owed, writing nothing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsEvaluation = new sdk.PromotionsEvaluation(client);

const result = await promotionsEvaluation.promotionsEvaluationEvaluate({
    currency: '',
    channel: '', // optional
    codes: [], // optional
    contactId: '', // optional
    itemCount: 1, // optional
    lines: [], // optional
    market: '', // optional
    organizationId: '', // optional
    paymentFee: 9.99, // optional
    precision: 1, // optional
    previewPromotionIds: [], // optional
    rounding: '', // optional
    shipping: 9.99, // optional
    subtotal: 9.99, // optional
    taxIncluded: true // optional
});
```

## promotions-evaluation-vocabularies

List the closed vocabularies this app enforces

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsEvaluation = new sdk.PromotionsEvaluation(client);

const result = await promotionsEvaluation.promotionsEvaluationVocabularies();
```

## promotions-evaluation-vocabulary

Read one vocabulary

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsEvaluation = new sdk.PromotionsEvaluation(client);

const result = await promotionsEvaluation.promotionsEvaluationVocabulary({
    name: ''
});
```
