# marketing-consents.subscriptions

## marketing-consents-subscriptions-confirm

Confirm a sign-up by its link

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsSubscriptionsConfirm({
    token: '',
    purchaseRequestId: '',
    allocations: [], // optional
    currency: '', // optional
    note: '', // optional
    orderId: '' // optional
});
```

## marketing-consents-eligibility-check

Ask which recipients may get a marketing send of a type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsEligibilityCheck({
    recipients: [],
    subscriptionType: 'newsletter',
    channel: sdk.Channel.Email // optional
});
```

## marketing-consents-preferences-links

Issue preference centre links for addresses

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsPreferencesLinks({
    recipients: [],
    channel: sdk.Channel.Email // optional
});
```

## marketing-consents-preferences-get

Read what the preference centre shows

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsPreferencesGet({
    token: '',
    locale: 'de' // optional
});
```

## marketing-consents-preferences-update

Save what a recipient chose in the preference centre

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsPreferencesUpdate({
    token: '',
    choices: [], // optional
    ip: '', // optional
    locale: '', // optional
    unsubscribeAll: true, // optional
    userAgent: '' // optional
});
```

## marketing-consents-subscriptions-list

List the subscriptions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsSubscriptionsList({
    id: '', // optional
    contactId: '', // optional
    channel: sdk.Channel.Email, // optional
    address: '', // optional
    addressHash: '', // optional
    subscriptionTypeId: '', // optional
    state: sdk.MarketingConsentsSubscriptionsListState.Pending, // optional
    legalBasis: sdk.MarketingConsentsConsentEventsListLegalBasis.ConsentDoi, // optional
    consentTextId: '', // optional
    locale: '', // optional
    market: '', // optional
    campaignRef: '', // optional
    source: sdk.MarketingConsentsSubscriptionsListSource.Form, // optional
    sourceRef: '', // optional
    requestedAt: '2026-01-01T12:00:00Z', // optional
    confirmationSentAt: '2026-01-01T12:00:00Z', // optional
    confirmedAt: '2026-01-01T12:00:00Z', // optional
    withdrawnAt: '2026-01-01T12:00:00Z', // optional
    lapseAt: '2026-01-01T12:00:00Z', // optional
    erasedAt: '2026-01-01T12:00:00Z', // optional
    suppressionWrittenAt: '2026-01-01T12:00:00Z', // optional
    suppressionRef: '', // optional
    externalId: '', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## marketing-consents-subscriptions-request

Sign an address up for a subscription type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsSubscriptionsRequest({
    subscriptionType: 'newsletter',
    address: '', // optional
    campaignRef: '7a8b9c0d-0000-4000-8000-000000000000', // optional
    channel: sdk.Channel.Email, // optional
    consentTextId: '', // optional
    contactId: '', // optional
    email: 'anna.berger@example.com', // optional
    firstName: '', // optional
    ip: '203.0.113.7', // optional
    lastName: '', // optional
    locale: 'de', // optional
    pageUrl: 'https://shop.example.com/newsletter', // optional
    phone: '+4915112345678', // optional
    source: sdk.MarketingConsentsSubscriptionsRequestSource.Form, // optional
    sourceRef: 'form:5e6f7a8b-0000-4000-8000-000000000000', // optional
    userAgent: '' // optional
});
```

## marketing-consents-subscriptions-get

Read one subscription

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsSubscriptionsGet({
    id: ''
});
```

## marketing-consents-subscriptions-withdraw

Withdraw a subscription from the back office

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsSubscriptions = new sdk.MarketingConsentsSubscriptions(client);

const result = await marketingConsentsSubscriptions.marketingConsentsSubscriptionsWithdraw({
    id: '',
    purchaseRequestId: '',
    allocations: [], // optional
    currency: '', // optional
    note: '' // optional
});
```
