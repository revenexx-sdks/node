# journeys.journeys

## journeys-journeys-list

List journeys

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    name: '', // optional
    description: '', // optional
    status: '', // optional
    triggerKind: '', // optional
    reenrol: '', // optional
    reenrolGapDays: '', // optional
    campaignRef: '', // optional
    templateCode: '', // optional
    currentVersion: '', // optional
    draftVersion: '', // optional
    triggerRanOn: '', // optional
    enrolledCount: '', // optional
    activeCount: '' // optional
});
```

## journeys-journeys-create

Create a draft journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysCreate({
    name: '',
    campaignRef: '', // optional
    currency: '', // optional
    description: '', // optional
    entry: '', // optional
    goalConfig: null, // optional
    metadata: null, // optional
    reenrol: true, // optional
    reenrolGapDays: 1, // optional
    steps: [], // optional
    triggerConfig: null, // optional
    triggerKind: sdk.TriggerKind.Event // optional
});
```

## journeys-journeys-empty-trash

Empty the journey trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysEmptyTrash();
```

## journeys-journeys-purge

Delete the journeys that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysPurge();
```

## journeys-journeys-delete

Move a journey to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysDelete({
    id: ''
});
```

## journeys-journeys-get

Read one journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysGet({
    id: ''
});
```

## journeys-journeys-update

Correct a journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysUpdate({
    id: '',
    campaignRef: '', // optional
    currency: '', // optional
    description: '', // optional
    goalConfig: null, // optional
    metadata: null, // optional
    name: '', // optional
    reenrol: true, // optional
    reenrolGapDays: 1, // optional
    triggerConfig: null, // optional
    triggerKind: sdk.TriggerKind.Event // optional
});
```

## journeys-journeys-archive

Archive a journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysArchive({
    id: '',
    data: {}
});
```

## journeys-journeys-enrol

Put one person into a live journey by hand

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysEnrol({
    id: '',
    contactId: '', // optional
    data: {}, // optional
    email: '', // optional
    key: '', // optional
    market: '' // optional
});
```

## journeys-journeys-graph

Read the steps of a journey version

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysGraph({
    id: '',
    version: '' // optional
});
```

## journeys-journeys-save-graph

Save the canvas as the draft

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysSaveGraph({
    id: '',
    steps: [],
    entry: '', // optional
    notes: '' // optional
});
```

## journeys-journeys-pause

Pause a live journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysPause({
    id: '',
    data: {}
});
```

## journeys-journeys-publish

Publish the draft

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysPublish({
    id: '',
    data: {}
});
```

## journeys-journeys-report

Read per-step counts of a journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysReport({
    id: '',
    version: '' // optional
});
```

## journeys-journeys-restore

Bring a journey back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysRestore({
    id: ''
});
```

## journeys-journeys-resume

Resume a paused journey

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysResume({
    id: '',
    data: {}
});
```

## journeys-journeys-run

Process the due steps of one journey now

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysRun({
    id: '',
    data: {}
});
```

## journeys-journeys-timeline

Read entries and reached goals of a journey per day

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysJourneys = new sdk.JourneysJourneys(client);

const result = await journeysJourneys.journeysJourneysTimeline({
    id: ''
});
```
