# audiences.audiences

## audiences-audiences-list

List audiences

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    code: '', // optional
    description: '', // optional
    kind: '', // optional
    ruleMatch: '', // optional
    active: '', // optional
    memberCount: '', // optional
    eligibleCount: '', // optional
    rulesSummary: '', // optional
    recomputeState: '', // optional
    recomputeError: '', // optional
    frozenFromId: '' // optional
});
```

## audiences-audiences-create

Create an audience

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesCreate({
    code: '',
    active: true, // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    kind: sdk.Kind.Active, // optional
    labels: null, // optional
    metadata: null, // optional
    ruleMatch: sdk.RuleMatch.All, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## audiences-audiences-recompute-all

Recompute every active audience under one budget

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesRecomputeAll();
```

## audiences-audiences-empty-trash

Empty the audience trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesEmptyTrash();
```

## audiences-audiences-purge

Delete the audiences that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesPurge();
```

## audiences-audiences-delete

Move a audience to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesDelete({
    id: ''
});
```

## audiences-audiences-get

Read one audience

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesGet({
    id: ''
});
```

## audiences-audiences-update

Correct an audience

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesUpdate({
    id: '',
    active: true, // optional
    code: '', // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    kind: sdk.Kind.Active, // optional
    labels: null, // optional
    metadata: null, // optional
    ruleMatch: sdk.RuleMatch.All, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## audiences-audiences-freeze

Freeze an active audience into a new static one

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesFreeze({
    id: '',
    code: '', // optional
    description: '', // optional
    labels: {}, // optional
    targetId: '' // optional
});
```

## audiences-audiences-preview

Count who would be in an audience, writing nothing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesPreview({
    id: '',
    ruleMatch: sdk.RuleMatch.All, // optional
    rules: [] // optional
});
```

## audiences-audiences-recompute

Recompute an active audience — chunked, continues where it stopped

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesRecompute({
    id: '',
    restart: true // optional
});
```

## audiences-audiences-restore

Bring a audience back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesAudiencesRestore({
    id: ''
});
```

## audiences-vocabularies-list

List the closed lists this app enforces

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesVocabulariesList();
```

## audiences-vocabularies-get

Read one closed list with its values and labels

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesAudiences = new sdk.AudiencesAudiences(client);

const result = await audiencesAudiences.audiencesVocabulariesGet({
    name: ''
});
```
