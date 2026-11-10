# tag-manager.tags

## tag-manager-registry-list

List the supported registry keys

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerRegistryList();
```

## tag-manager-tags-list

List marketing tags

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '', // optional
    id: '', // optional
    code: '', // optional
    name: '', // optional
    description: '', // optional
    kind: '', // optional
    registryKey: '', // optional
    scriptUrl: '', // optional
    vendorCode: '', // optional
    purposeCode: '', // optional
    load: '', // optional
    isActive: true, // optional
    createdAt: '', // optional
    updatedAt: '' // optional
});
```

## tag-manager-tags-create

Create a marketing tag

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsCreate({
    chainedVendorCodes: [], // optional
    code: '', // optional
    config: {}, // optional
    description: '', // optional
    eventMap: {}, // optional
    isActive: true, // optional
    kind: sdk.TagManagerTagsCreateKind.Registry, // optional
    load: sdk.Load.Immediate, // optional
    name: '', // optional
    purposeCode: '', // optional
    registryKey: '', // optional
    scriptUrl: '', // optional
    vendorCode: '' // optional
});
```

## tag-manager-tags-delete

Delete a marketing tag

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsDelete({
    id: ''
});
```

## tag-manager-tags-get

Read one marketing tag

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsGet({
    id: ''
});
```

## tag-manager-tags-update

Edit a marketing tag

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsUpdate({
    id: '',
    chainedVendorCodes: [], // optional
    code: '', // optional
    config: {}, // optional
    description: '', // optional
    eventMap: {}, // optional
    isActive: true, // optional
    kind: sdk.TagManagerTagsCreateKind.Registry, // optional
    load: sdk.Load.Immediate, // optional
    name: '', // optional
    purposeCode: '', // optional
    registryKey: '', // optional
    scriptUrl: '', // optional
    vendorCode: '' // optional
});
```

## tag-manager-tags-triggers-list

List a marketing tag's triggers

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsTriggersList({
    id: ''
});
```

## tag-manager-tags-triggers-attach

Attach a trigger to a marketing tag

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsTriggersAttach({
    id: '',
    triggerId: ''
});
```

## tag-manager-tags-triggers-detach

Detach a trigger from a marketing tag

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTagsTriggersDetach({
    id: '',
    triggerId: ''
});
```

## tag-manager-triggers-list

List triggers

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTriggersList({
    limit: 1, // optional
    offset: 1, // optional
    order: '', // optional
    id: '', // optional
    code: '', // optional
    name: '', // optional
    kind: '', // optional
    eventName: '', // optional
    createdAt: '', // optional
    updatedAt: '' // optional
});
```

## tag-manager-triggers-create

Create a trigger

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTriggersCreate({
    code: '', // optional
    conditions: {}, // optional
    eventName: '', // optional
    kind: sdk.TagManagerTriggersCreateKind.PageView, // optional
    name: '' // optional
});
```

## tag-manager-triggers-delete

Delete a trigger

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTriggersDelete({
    id: ''
});
```

## tag-manager-triggers-get

Read one trigger

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTriggersGet({
    id: ''
});
```

## tag-manager-triggers-update

Edit a trigger

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerTriggersUpdate({
    id: '',
    code: '', // optional
    conditions: {}, // optional
    eventName: '', // optional
    kind: sdk.TagManagerTriggersCreateKind.PageView, // optional
    name: '' // optional
});
```

## tag-manager-variables-list

List variables

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVariablesList({
    limit: 1, // optional
    offset: 1, // optional
    order: '', // optional
    id: '', // optional
    code: '', // optional
    name: '', // optional
    kind: '', // optional
    path: '', // optional
    createdAt: '', // optional
    updatedAt: '' // optional
});
```

## tag-manager-variables-create

Create a variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVariablesCreate({
    code: '', // optional
    constantValue: null, // optional
    kind: sdk.TagManagerVariablesCreateKind.EventField, // optional
    name: '', // optional
    path: '' // optional
});
```

## tag-manager-variables-delete

Delete a variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVariablesDelete({
    id: ''
});
```

## tag-manager-variables-get

Read one variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVariablesGet({
    id: ''
});
```

## tag-manager-variables-update

Edit a variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVariablesUpdate({
    id: '',
    code: '', // optional
    constantValue: null, // optional
    kind: sdk.TagManagerVariablesCreateKind.EventField, // optional
    name: '', // optional
    path: '' // optional
});
```

## tag-manager-vocabularies-list

List the theme event vocabulary

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerTags = new sdk.TagManagerTags(client);

const result = await tagManagerTags.tagManagerVocabulariesList();
```
