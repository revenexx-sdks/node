# channels

## channels-list

List channels

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsList({
    id: '', // optional
    code: 'shop', // optional
    name: 'Shop', // optional
    labels: '{"en":"Shop","de":"Shop"}', // optional
    type: 'storefront', // optional
    status: sdk.ChannelStatus.Active, // optional
    unassignedVisibility: sdk.ChannelUnassignedVisibility.Inherit, // optional
    isDefault: true, // optional
    position: 1, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```

## channels-create

Create a channel

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsCreate({
    code: 'shop',
    name: 'Shop',
    isDefault: true, // optional
    labels: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    position: 1, // optional
    status: sdk.ChannelStatus.Active, // optional
    type: 'storefront', // optional
    unassignedVisibility: sdk.ChannelUnassignedVisibility.Inherit // optional
});
```

## channels-context

Resolve the active channel

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsContext({
    channel: 'shop' // optional
});
```

## channels-defaults

Restore the shipped defaults

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsDefaults();
```

## channels-types-list

The channel types this tenant keeps

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsTypesList({
    limit: 1, // optional
    offset: 1, // optional
    active: true // optional
});
```

## channels-types-create

Add a channel type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsTypesCreate({
    code: 'feed',
    title: 'Product feed',
    active: true, // optional
    description: 'A web shop a human browses.', // optional
    descriptions: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    position: 1, // optional
    tone: sdk.ChannelTypeTone.Neutral // optional
});
```

## channels-types-delete

Remove a channel type nothing uses

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsTypesDelete({
    id: ''
});
```

## channels-types-get

Read one channel type

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsTypesGet({
    id: ''
});
```

## channels-types-update

Rename a channel type or move it in the order

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsTypesUpdate({
    id: '',
    active: false, // optional
    description: 'A web shop a human browses.', // optional
    descriptions: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    position: 1, // optional
    title: 'Product feed', // optional
    tone: sdk.ChannelTypeTone.Neutral // optional
});
```

## channels-visibility

Decide which rows a channel may see

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsVisibility({
    items: [],
    channel: 'shop', // optional
    channelBody: 'shop' // optional
});
```

## channels-vocabularies-list

List vocabularies

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsVocabulariesList();
```

## channels-vocabularies-get

Read one vocabulary

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsVocabulariesGet({
    name: sdk.ChannelsVocabulariesGetName.Statuses
});
```

## channels-delete

Delete a channel by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsDelete({
    id: ''
});
```

## channels-get

Read one channel by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsGet({
    id: ''
});
```

## channels-update

Update a channel by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsUpdate({
    id: '',
    code: 'shop', // optional
    isDefault: true, // optional
    labels: {
        "de": "Shop",
        "en": "Shop"
    }, // optional
    name: 'Shop', // optional
    position: 1, // optional
    status: sdk.ChannelStatus.Active, // optional
    type: 'storefront', // optional
    unassignedVisibility: sdk.ChannelUnassignedVisibility.Inherit // optional
});
```
