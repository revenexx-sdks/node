# quotes.acceptance

## quotes-acceptance-accept

Accept a quote, whole or line by line

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesAcceptance = new sdk.QuotesAcceptance(client);

const result = await quotesAcceptance.quotesAcceptanceAccept({
    id: '',
    items: [] // optional
});
```

## quotes-acceptance-decline

Decline a quote

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesAcceptance = new sdk.QuotesAcceptance(client);

const result = await quotesAcceptance.quotesAcceptanceDecline({
    id: '',
    reason: '' // optional
});
```

## quotes-acceptance-ordered

Record the order a quote produced

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesAcceptance = new sdk.QuotesAcceptance(client);

const result = await quotesAcceptance.quotesAcceptanceOrdered({
    id: '',
    orderId: '',
    itemIds: [] // optional
});
```

## quotes-acceptance-reject

Refuse to quote

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const quotesAcceptance = new sdk.QuotesAcceptance(client);

const result = await quotesAcceptance.quotesAcceptanceReject({
    id: '',
    reason: ''
});
```
