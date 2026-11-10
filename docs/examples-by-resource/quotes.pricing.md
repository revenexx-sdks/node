# quotes.pricing

## quotes-pricing-expire

Expire what has run out

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingExpire({
    data: {}
});
```

## quotes-pricing-remove-item

Take a position off a quote being shaped

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingRemoveItem({
    id: '',
    data: {}
});
```

## quotes-pricing-follow-up

Set the day the desk looks at a quote again

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingFollowUp({
    id: '',
    followUpAt: '2026-10-25' // optional
});
```

## quotes-pricing-add-item

Add a position to a quote being shaped

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingAddItem({
    id: '',
    configuration: {}, // optional
    discountPercent: 5, // optional
    externalId: 'ANG-20481', // optional
    externalRefs: {
        "cpq": "Q-88120",
        "entitys": "4711"
    }, // optional
    leadTimeDays: 1, // optional
    listPrice: 1088, // optional
    metadata: {}, // optional
    name: '', // optional
    position: 1, // optional
    priceReason: sdk.PriceReason.Volume, // optional
    productId: '', // optional
    quantity: 10, // optional
    quotedPrice: 9.99, // optional
    sku: '', // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "Salesperson_Code": "VK07"
        },
        "system": "business-central"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    taxRate: 19, // optional
    unit: '' // optional
});
```

## quotes-pricing-item

Price one position

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingItem({
    id: '',
    itemId: '',
    discountPercent: 8, // optional
    leadTimeDays: 1, // optional
    priceReason: sdk.PriceReason.Volume, // optional
    quantity: 12, // optional
    quotedPrice: 980 // optional
});
```

## quotes-pricing-price

Put prices on a quote

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingPrice({
    id: '',
    externalId: 'ANG-20481', // optional
    externalRefs: {
        "cpq": "Q-88120",
        "entitys": "4711"
    }, // optional
    items: [], // optional
    sellerNote: '', // optional
    senderCountry: 'DE', // optional
    shippingAmount: 9.99, // optional
    shippingTaxRate: 9.99, // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "Salesperson_Code": "VK07"
        },
        "system": "business-central"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    validUntil: '2026-01-01T12:00:00Z' // optional
});
```

## quotes-pricing-review

Take a request onto the desk

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingReview({
    id: '',
    contactId: '', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    expiresAt: '2026-01-01T12:00:00Z', // optional
    idBody: '', // optional
    issuedCount: 1, // optional
    items: null, // optional
    journeyRef: '', // optional
    locale: '', // optional
    market: '', // optional
    metadata: null, // optional
    orderId: '', // optional
    orderNumber: '', // optional
    organizationId: '', // optional
    productIds: null, // optional
    reviewedCount: 1, // optional
    state: sdk.QuotesPricingReviewState.Issued, // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    usedAt: '2026-01-01T12:00:00Z' // optional
});
```

## quotes-pricing-remind

Remind the buyer of a sent quote

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesPricing = new sdk.QuotesPricing(client);

const result = await quotesPricing.quotesPricingRemind({
    id: '',
    data: {}
});
```
