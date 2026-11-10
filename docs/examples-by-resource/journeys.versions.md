# journeys.versions

## journeys-versions-list

List journey versions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysVersions = new sdk.JourneysVersions(client);

const result = await journeysVersions.journeysVersionsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    journeyId: '', // optional
    version: '', // optional
    state: '', // optional
    entryKey: '', // optional
    stepCount: '', // optional
    publishedBy: '', // optional
    notes: '' // optional
});
```

## journeys-versions-get

Read one version

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysVersions = new sdk.JourneysVersions(client);

const result = await journeysVersions.journeysVersionsGet({
    id: ''
});
```
