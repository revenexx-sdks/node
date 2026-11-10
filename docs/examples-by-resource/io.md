# io

## list-bulk-jobs

List bulk jobs for the tenant

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.listBulkJobs({
    type: null, // optional
    status: null, // optional
    vendor: '', // optional
    app: '', // optional
    entity: '', // optional
    limit: 1 // optional
});
```

## get-bulk-job

Get a bulk job's status

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.getBulkJob({
    id: ''
});
```

## list-io-entities

Catalogue of importable / exportable entities

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.listIoEntities();
```

## create-export

Export a tenant's entity to object storage

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.createExport({
    app: '',
    entity: '',
    vendor: '',
    format: sdk.Format.Csv, // optional
    profileId: '' // optional
});
```

## get-export-url

Signed download URL for a finished export

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.getExportUrl({
    id: ''
});
```

## create-import

Register an uploaded object as an import job

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.createImport({
    app: '',
    entity: '',
    objectKey: '',
    vendor: '',
    format: sdk.Format.Csv, // optional
    keys: [], // optional
    maxRejects: 1, // optional
    mode: sdk.Mode.Upsert, // optional
    profileId: '', // optional
    target: sdk.CreateImportTarget.Live // optional
});
```

## list-profiles

List the tenant's import/export profiles

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.listProfiles();
```

## create-profile

Create an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.createProfile({
    app: '',
    direction: sdk.Direction.Import,
    entity: '',
    format: '',
    name: '',
    vendor: '',
    applyMode: sdk.ApplyMode.Upsert, // optional
    mapping: {}, // optional
    markets: [], // optional
    options: {} // optional
});
```

## delete-profile

Delete an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.deleteProfile({
    id: ''
});
```

## show-profile

Get one import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.showProfile({
    id: ''
});
```

## update-profile

Update an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.updateProfile({
    id: '',
    app: '',
    direction: sdk.Direction.Import,
    entity: '',
    format: '',
    name: '',
    vendor: '',
    applyMode: sdk.ApplyMode.Upsert, // optional
    mapping: {}, // optional
    markets: [], // optional
    options: {} // optional
});
```

## run-profile

Run a saved profile (on-click import/export)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.runProfile({
    id: '',
    markets: [], // optional
    objectKey: '' // optional
});
```

## create-upload

Mint a tenant-scoped signed upload URL

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const io = new sdk.Io(client);

const result = await io.createUpload({
    extension: 'csv' // optional
});
```
