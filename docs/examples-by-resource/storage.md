# storage

## asset-index

List assets

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetIndex({
    search: '' // optional
});
```

## asset-store

Upload an asset

```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetStore({
    file: InputFile.fromPath('/path/to/file', 'filename'),
    altText: '', // optional
    description: '', // optional
    displayName: '', // optional
    folderId: '', // optional
    keepArchive: true, // optional
    tags: [], // optional
    unpack: true, // optional
    visibility: sdk.AssetStoreVisibility.Public // optional
});
```

## asset-bulk

Upload several assets

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetBulk({
    folderId: '', // optional
    visibility: '' // optional
});
```

## asset-destroy

Delete an asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetDestroy({
    id: ''
});
```

## asset-show

Get an asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetShow({
    id: ''
});
```

## asset-update

Update an asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetUpdate({
    id: '',
    altText: '', // optional
    description: '', // optional
    displayName: '', // optional
    folderId: '', // optional
    name: '', // optional
    tags: [], // optional
    visibility: sdk.AssetStoreVisibility.Public // optional
});
```

## asset-download

Download an asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetDownload({
    id: ''
});
```

## asset-permanent

Permanently delete an asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetPermanent({
    id: ''
});
```

## asset-reprocess

Reprocess an asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetReprocess({
    id: ''
});
```

## asset-restore

Restore a deleted asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetRestore({
    id: ''
});
```

## asset-sign

Create a signed asset URL

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetSign({
    id: '',
    ttlSeconds: 1 // optional
});
```

## asset-unpack

Unpack an archive asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetUnpack({
    id: '',
    keepArchive: true, // optional
    targetFolderId: '' // optional
});
```

## folder-index

List folders

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.folderIndex();
```

## folder-store

Create a folder

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.folderStore({
    name: '',
    parentId: '' // optional
});
```

## folder-destroy

Delete a folder

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.folderDestroy({
    id: '',
    recursive: true // optional
});
```

## folder-show

Get a folder

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.folderShow({
    id: ''
});
```

## folder-update

Rename or move a folder

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.folderUpdate({
    id: '',
    name: '', // optional
    parentId: '' // optional
});
```

## sync-rule-index

List SFTP sync rules

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleIndex();
```

## sync-rule-store

Create an SFTP sync rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleStore({
    sftpAccountId: '',
    sourcePath: '/uploads',
    enabled: true, // optional
    options: [], // optional
    schedule: '0 3 * * *', // optional
    targetFolderId: '' // optional
});
```

## sync-rule-destroy

Delete an SFTP sync rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleDestroy({
    id: ''
});
```

## sync-rule-show

Get an SFTP sync rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleShow({
    id: ''
});
```

## sync-rule-update

Update an SFTP sync rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleUpdate({
    id: '',
    enabled: true, // optional
    options: [], // optional
    schedule: '0 3 * * *', // optional
    sftpAccountId: '', // optional
    sourcePath: '/uploads', // optional
    targetFolderId: '' // optional
});
```

## sync-rule-run

Run an SFTP sync rule now

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleRun({
    id: ''
});
```

## sync-rule-run-protocol

Get an SFTP sync run protocol

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleRunProtocol({
    id: '',
    runId: ''
});
```

## sync-rule-history

List SFTP sync history

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.syncRuleHistory({
    ruleId: '', // optional
    from: '2026-01-01T12:00:00Z', // optional
    to: '2026-01-01T12:00:00Z' // optional
});
```

## tenant-stats

Get storage statistics

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.tenantStats();
```

## tenant-usage

Get storage usage

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.tenantUsage();
```
