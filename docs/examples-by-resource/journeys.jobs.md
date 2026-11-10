# journeys.jobs

## journeys-jobs-steps

Run the step job once

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJobs = new sdk.JourneysJobs(client);

const result = await journeysJobs.journeysJobsSteps({
    budgetMs: 1 // optional
});
```

## journeys-jobs-triggers

Run date triggers and the sweep once

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJobs = new sdk.JourneysJobs(client);

const result = await journeysJobs.journeysJobsTriggers({
    force: true // optional
});
```
