# campaigns.tasks

## campaigns-tasks-list

List campaign tasks

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    campaignId: '', // optional
    title: '', // optional
    notes: '', // optional
    assignee: '' // optional
});
```

## campaigns-tasks-create

Add a task to a campaign

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksCreate({
    campaignId: '',
    title: '',
    assignee: '', // optional
    doneAt: '2026-01-01T12:00:00Z', // optional
    dueAt: '2026-01-01T12:00:00Z', // optional
    notes: '' // optional
});
```

## campaigns-tasks-delete

Delete a task

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksDelete({
    id: ''
});
```

## campaigns-tasks-get

Read one task

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksGet({
    id: ''
});
```

## campaigns-tasks-update

Correct a task

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksUpdate({
    id: '',
    assignee: '', // optional
    campaignId: '', // optional
    doneAt: '2026-01-01T12:00:00Z', // optional
    dueAt: '2026-01-01T12:00:00Z', // optional
    notes: '', // optional
    title: '' // optional
});
```

## campaigns-tasks-complete

Tick a task off

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksComplete({
    id: ''
});
```

## campaigns-tasks-reopen

Open a task again

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsTasks = new sdk.CampaignsTasks(client);

const result = await campaignsTasks.campaignsTasksReopen({
    id: ''
});
```
