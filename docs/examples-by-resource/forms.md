# forms

## forms-list

List forms

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsList({
    id: '', // optional
    name: 'Contact request', // optional
    slug: 'contact', // optional
    status: sdk.FormStatus.Draft, // optional
    campaignRef: '', // optional
    leadStage: 'lead', // optional
    createdAt: '2026-01-31T09:15:00Z', // optional
    updatedAt: '2026-01-31T09:15:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## forms-create

Create a form

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsCreate({
    name: 'Price request',
    slug: 'price-request',
    campaignRef: '', // optional
    definition: [{"$formkit":"text","label":"Company","name":"company","validation":"required"},{"$formkit":"email","label":"Email","name":"email","validation":"required|email"},{"$formkit":"textarea","label":"What do you need a price for?","name":"message","rows":4},{"$el":"p","children":"We answer price requests within one working day."}], // optional
    leadStage: 'lead', // optional
    metadata: {}, // optional
    settings: {}, // optional
    status: sdk.FormStatus.Draft // optional
});
```

## forms-defaults

Seed the sample contact form

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsDefaults();
```

## forms-submissions-list

List submissions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsList({
    id: '', // optional
    formId: '', // optional
    formSlug: 'contact', // optional
    source: '/contact', // optional
    status: sdk.FormSubmissionStatus.New, // optional
    contactId: '', // optional
    pageUrl: 'https://example.com/kontakt', // optional
    campaignRef: '', // optional
    leadStage: 'lead', // optional
    createdAt: '2026-01-31T09:15:00Z', // optional
    updatedAt: '2026-01-31T09:15:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## forms-submissions-create

Record a submission

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsCreate({
    data: {
        "company": "Example GmbH",
        "email": "buyer@example.com",
        "message": "Please quote 200 units of ACME-4711-BLK, delivered to Hamburg."
    },
    formId: '',
    campaignRef: '', // optional
    ip: '203.0.113.10', // optional
    locale: 'de-DE', // optional
    metadata: {}, // optional
    pageUrl: 'https://example.com/kontakt', // optional
    source: '/contact', // optional
    userAgent: 'Mozilla/5.0' // optional
});
```

## forms-submissions-prune

Prune submissions past retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsPrune({
    dryRun: true, // optional
    formSlug: 'contact', // optional
    olderThanDays: 1, // optional
    status: sdk.FormsSubmissionsPruneStatus.New // optional
});
```

## forms-submissions-delete

Delete a submission

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsDelete({
    id: ''
});
```

## forms-submissions-get

Read one submission

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsGet({
    id: ''
});
```

## forms-submissions-update

Update a submission

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsUpdate({
    id: '',
    data: {
        "company": "Example GmbH",
        "email": "buyer@example.com",
        "message": "Please quote 200 units of ACME-4711-BLK, delivered to Hamburg."
    }, // optional
    formId: '', // optional
    formSlug: 'contact', // optional
    metadata: {}, // optional
    source: '/contact', // optional
    status: sdk.FormSubmissionStatus.New // optional
});
```

## forms-vocabularies-list

List vocabularies

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsVocabulariesList();
```

## forms-vocabularies-get

Read one vocabulary

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsVocabulariesGet({
    name: sdk.FormsVocabulariesGetName.Formstatuses
});
```

## forms-delete

Delete a form

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsDelete({
    id: ''
});
```

## forms-get

Read one form

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsGet({
    id: ''
});
```

## forms-update

Update a form

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsUpdate({
    id: '',
    campaignRef: '', // optional
    definition: [{"$formkit":"text","label":"Company","name":"company","validation":"required"},{"$formkit":"email","label":"Email","name":"email","validation":"required|email"},{"$formkit":"textarea","label":"What do you need a price for?","name":"message","rows":4},{"$el":"p","children":"We answer price requests within one working day."}], // optional
    leadStage: 'lead', // optional
    metadata: {}, // optional
    name: 'Price request', // optional
    settings: {}, // optional
    slug: 'price-request', // optional
    status: sdk.FormStatus.Draft // optional
});
```
