# marketing-consents.types

## marketing-consents-consent-texts-list

List the consent texts and their versions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsList({
    id: '', // optional
    subscriptionTypeId: '', // optional
    version: 1, // optional
    locale: '', // optional
    wording: '', // optional
    publishedAt: '2026-01-01T12:00:00Z', // optional
    publishedBy: '', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: '', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: '', // optional
    trashed: sdk.Trashed.Exclude, // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## marketing-consents-consent-texts-create

Write a new draft version of a consent text

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsCreate({
    locale: 'de',
    subscriptionTypeId: '',
    wording: 'Ja, ich möchte den Newsletter mit Neuheiten und Aktionen erhalten. Abmeldung jederzeit über den Link in jeder Mail.'
});
```

## marketing-consents-consent-texts-empty-trash

Empty the consent text trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsEmptyTrash();
```

## marketing-consents-consent-texts-purge

Delete the consent texts that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsPurge();
```

## marketing-consents-consent-texts-delete

Move a consent text to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsDelete({
    id: ''
});
```

## marketing-consents-consent-texts-get

Read one consent text

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsGet({
    id: ''
});
```

## marketing-consents-consent-texts-update

Edit a draft consent text

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsUpdate({
    id: '',
    wording: 'Ja, ich möchte den Newsletter mit Neuheiten und Aktionen erhalten. Abmeldung jederzeit über den Link in jeder Mail.'
});
```

## marketing-consents-consent-texts-publish

Publish a consent text version

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsPublish({
    id: '',
    data: {}
});
```

## marketing-consents-consent-texts-restore

Bring a consent text back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsRestore({
    id: ''
});
```

## marketing-consents-subscription-types-list

List the subscription types

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesList({
    id: '', // optional
    code: '', // optional
    requiresDoi: true, // optional
    allowsExistingCustomer: true, // optional
    position: 1, // optional
    archivedAt: '2026-01-01T12:00:00Z', // optional
    externalId: '', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: '', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: '', // optional
    trashed: sdk.Trashed.Exclude, // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## marketing-consents-subscription-types-create

Create a subscription type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesCreate({
    code: 'newsletter',
    labels: {
        "de": "Newsletter",
        "en": "Newsletter"
    },
    allowsExistingCustomer: true, // optional
    channels: [sdk.Channels.Email, sdk.Channels.Sms], // optional
    descriptions: {}, // optional
    position: 10, // optional
    requiresDoi: true, // optional
    similarGoodsNote: {
        "de": "Ersatzteile und Zubeh\u00f6r zu gekauften Ger\u00e4ten.",
        "en": "Spare parts and accessories for purchased devices."
    } // optional
});
```

## marketing-consents-subscription-types-empty-trash

Empty the subscription type trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesEmptyTrash();
```

## marketing-consents-subscription-types-purge

Delete the subscription types that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesPurge();
```

## marketing-consents-subscription-types-delete

Move a subscription type to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesDelete({
    id: ''
});
```

## marketing-consents-subscription-types-get

Read one subscription type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesGet({
    id: ''
});
```

## marketing-consents-subscription-types-update

Edit a subscription type; its code is fixed

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesUpdate({
    id: '',
    allowsExistingCustomer: true, // optional
    channels: [sdk.Channels.Email, sdk.Channels.Sms], // optional
    code: 'newsletter', // optional
    descriptions: {}, // optional
    labels: {
        "de": "Newsletter",
        "en": "Newsletter"
    }, // optional
    position: 10, // optional
    requiresDoi: true, // optional
    similarGoodsNote: {
        "de": "Ersatzteile und Zubeh\u00f6r zu gekauften Ger\u00e4ten.",
        "en": "Spare parts and accessories for purchased devices."
    } // optional
});
```

## marketing-consents-subscription-types-archive

Archive a subscription type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesArchive({
    id: '',
    data: {}
});
```

## marketing-consents-subscription-types-restore

Bring a subscription type back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesRestore({
    id: ''
});
```

## marketing-consents-subscription-types-unarchive

Bring an archived subscription type back

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsSubscriptionTypesUnarchive({
    id: '',
    data: {}
});
```

## marketing-consents-vocabularies-list

List the value sets this app owns

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsVocabulariesList();
```

## marketing-consents-vocabularies-get

Read one value set with its words

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsVocabulariesGet({
    name: sdk.MarketingConsentsVocabulariesGetName.Channels
});
```
