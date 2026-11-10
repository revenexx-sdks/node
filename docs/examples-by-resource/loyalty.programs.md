# loyalty.programs

## loyalty-programs-list

List loyalty programmes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    code: '', // optional
    description: '', // optional
    kind: '', // optional
    holder: '', // optional
    currency: '', // optional
    period: '', // optional
    autoEnroll: '', // optional
    active: '', // optional
    memberCount: '', // optional
    externalId: '', // optional
    deletedBy: '', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeBlockedReason: '' // optional
});
```

## loyalty-programs-create

Create a loyalty programme

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsCreate({
    code: '',
    kind: sdk.LoyaltyProgramsCreateKind.Points,
    labels: null,
    active: true, // optional
    autoEnroll: true, // optional
    currency: '', // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    holder: sdk.Holder.Contact, // optional
    metadata: null, // optional
    period: sdk.Period.CalendarYear, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## loyalty-programs-empty-trash

Empty the programme trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsEmptyTrash();
```

## loyalty-programs-purge

Delete the programmes that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsPurge();
```

## loyalty-programs-delete

Move a programme to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsDelete({
    id: ''
});
```

## loyalty-programs-get

Read one programme

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsGet({
    id: ''
});
```

## loyalty-programs-update

Correct a programme

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsUpdate({
    id: '',
    active: true, // optional
    autoEnroll: true, // optional
    code: '', // optional
    currency: '', // optional
    description: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    holder: sdk.Holder.Contact, // optional
    kind: sdk.LoyaltyProgramsCreateKind.Points, // optional
    labels: null, // optional
    metadata: null, // optional
    period: sdk.Period.CalendarYear, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## loyalty-programs-figures

Read the active members of a programme per tier

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsFigures({
    id: ''
});
```

## loyalty-programs-open-period

Open the yearly bonus agreements for every member of a turnover bonus programme

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsOpenPeriod({
    id: '',
    period: '' // optional
});
```

## loyalty-programs-restore

Bring a programme back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyPrograms = new sdk.LoyaltyPrograms(client);

const result = await loyaltyPrograms.loyaltyProgramsRestore({
    id: ''
});
```
