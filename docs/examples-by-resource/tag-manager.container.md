# tag-manager.container

## tag-manager-container-checks-list

List container checks

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerChecksList({
    limit: 1, // optional
    offset: 1, // optional
    order: '', // optional
    id: '', // optional
    containerVersionId: '', // optional
    containerVersionNumber: 1, // optional
    policyVersionNumber: 1, // optional
    reason: '', // optional
    ok: true, // optional
    checkedAt: '' // optional
});
```

## tag-manager-container-checks-get

Read one container check

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerChecksGet({
    id: ''
});
```

## tag-manager-container-versions-list

List container versions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerVersionsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '', // optional
    id: '', // optional
    number: 1, // optional
    market: '', // optional
    sha256: '', // optional
    policyVersionNumber: 1, // optional
    policySha256: '', // optional
    rolledBackFrom: 1, // optional
    note: '', // optional
    publishedBy: '', // optional
    publishedAt: '' // optional
});
```

## tag-manager-container-versions-get

Read one container version

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerVersionsGet({
    id: ''
});
```

## tag-manager-container-publish

Publish the container

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerPublish({
    note: '' // optional
});
```

## tag-manager-container-recheck

Re-check the live containers

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerRecheck({
    data: {}
});
```

## tag-manager-container-rollback

Publish an old version again

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerRollback({
    version: 1
});
```

## tag-manager-container-status

Show the live containers and their latest check

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerStatus();
```

## tag-manager-container-validate

Validate the draft container against the consent policy

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerContainerValidate({
    data: {}
});
```

## tag-manager-preview-create

Mint a preview token for the draft

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerContainer = new sdk.TagManagerContainer(client);

const result = await tagManagerContainer.tagManagerPreviewCreate({
    ttlMinutes: 1 // optional
});
```
