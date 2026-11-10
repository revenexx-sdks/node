# documents.kinds

## documents-kinds-list

List the document kinds this merchant keeps

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsList({
    id: '', // optional
    code: 'invoice', // optional
    title: 'Invoice', // optional
    description: 'What the buyer owes for an order.', // optional
    isDefault: true, // optional
    active: true, // optional
    tone: sdk.Tone.Neutral, // optional
    position: 0, // optional
    isSystem: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## documents-kinds-create

Add a document kind of your own

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsCreate({
    code: 'invoice',
    title: 'Invoice',
    active: true, // optional
    description: 'What the buyer owes for an order.', // optional
    descriptions: {
        "de": "Was der K\u00e4ufer f\u00fcr eine Bestellung schuldet.",
        "en": "What the buyer owes for an order."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Rechnung",
        "en": "Invoice"
    }, // optional
    position: 0, // optional
    tone: sdk.DocumentKindTone.Info // optional
});
```

## documents-kinds-defaults

Seed the four document kinds an order produces

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsDefaults({
    data: {}
});
```

## documents-kinds-delete

Remove one document kind

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsDelete({
    id: ''
});
```

## documents-kinds-get

Read one document kind

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsGet({
    id: ''
});
```

## documents-kinds-update

Edit one document kind

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsUpdate({
    id: '',
    active: true, // optional
    code: 'invoice', // optional
    description: 'What the buyer owes for an order.', // optional
    descriptions: {
        "de": "Was der K\u00e4ufer f\u00fcr eine Bestellung schuldet.",
        "en": "What the buyer owes for an order."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Rechnung",
        "en": "Invoice"
    }, // optional
    position: 0, // optional
    title: 'Invoice', // optional
    tone: sdk.DocumentKindTone.Info // optional
});
```

## documents-kinds-make-default

Make one document kind the default

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsKindsMakeDefault({
    id: ''
});
```

## documents-vocabularies-list

List the vocabularies this app owns

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsVocabulariesList();
```

## documents-vocabularies-get

Read one vocabulary with its values

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const documentsKinds = new sdk.DocumentsKinds(client);

const result = await documentsKinds.documentsVocabulariesGet({
    name: sdk.DocumentVocabularyPathName.Kinds
});
```
