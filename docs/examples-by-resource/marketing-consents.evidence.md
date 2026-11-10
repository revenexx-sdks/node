# marketing-consents.evidence

## marketing-consents-consent-events-list

List the consent events

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsConsentEventsList({
    id: '', // optional
    subscriptionId: '', // optional
    contactId: '', // optional
    subscriptionTypeId: '', // optional
    channel: sdk.Channel.Email, // optional
    addressHash: '', // optional
    kind: sdk.MarketingConsentsConsentEventsListKind.Requested, // optional
    source: sdk.MarketingConsentsConsentEventsListSource.Form, // optional
    sourceRef: '', // optional
    legalBasis: sdk.MarketingConsentsConsentEventsListLegalBasis.ConsentDoi, // optional
    consentTextId: '', // optional
    campaignRef: '', // optional
    pageUrl: '', // optional
    ip: '', // optional
    userAgent: '', // optional
    ipTruncatedAt: '2026-01-01T12:00:00Z', // optional
    at: '2026-01-01T12:00:00Z', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## marketing-consents-consent-events-get

Read one consent event

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsConsentEventsGet({
    id: ''
});
```

## marketing-consents-contacts-get

Read one contact's consent record

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsContactsGet({
    contactId: ''
});
```

## marketing-consents-contacts-erase

Erase one contact's consents, keeping minimal proof

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsContactsErase({
    contactId: '',
    data: {}
});
```

## marketing-consents-contacts-export

Export one contact's consent record for an access request

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsContactsExport({
    contactId: ''
});
```

## marketing-consents-imports-list

List the imports

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsImportsList({
    id: '', // optional
    subscriptionTypeId: '', // optional
    channel: sdk.Channel.Email, // optional
    legalBasis: sdk.MarketingConsentsImportsListLegalBasis.ConsentSingle, // optional
    fileRef: '', // optional
    proofNote: '', // optional
    rows: 1, // optional
    accepted: 1, // optional
    rejected: 1, // optional
    state: sdk.State.Running, // optional
    createdBy: '', // optional
    finishedAt: '2026-01-01T12:00:00Z', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## marketing-consents-imports-create

Import an existing list with its recorded basis

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsImportsCreate({
    legalBasis: sdk.MarketingConsentsImportsListLegalBasis.ConsentSingle,
    proofNote: 'Altsystem Shopware, Double-Opt-in-Log 2019–2026',
    rows: [],
    subscriptionType: 'newsletter',
    channel: sdk.Channel.Email, // optional
    fileRef: 'newsletter-export-2026-09.csv' // optional
});
```

## marketing-consents-imports-get

Read one import

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsImportsGet({
    id: ''
});
```

## marketing-consents-ip-retention-run

Shorten IP addresses past their retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsIpRetentionRun({
    data: {}
});
```

## marketing-consents-lapse-run

Lapse unconfirmed sign-ups past their expiry

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsLapseRun({
    data: {}
});
```

## marketing-consents-sweep-run

Read what the event bus does not deliver yet

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsEvidence = new sdk.MarketingConsentsEvidence(client);

const result = await marketingConsentsEvidence.marketingConsentsSweepRun({
    data: {}
});
```
