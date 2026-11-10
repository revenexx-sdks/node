# journeys.templates

## journeys-templates-list

List the shipped flows

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysTemplates = new sdk.JourneysTemplates(client);

const result = await journeysTemplates.journeysTemplatesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    code: '', // optional
    tier: '', // optional
    triggerKind: '', // optional
    position: '', // optional
    active: '' // optional
});
```

## journeys-templates-copy

Copy a template into a new draft journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysTemplates = new sdk.JourneysTemplates(client);

const result = await journeysTemplates.journeysTemplatesCopy({
    code: '',
    name: '' // optional
});
```

## journeys-templates-get

Read one template

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysTemplates = new sdk.JourneysTemplates(client);

const result = await journeysTemplates.journeysTemplatesGet({
    id: ''
});
```
