# journeys.vocabularies

## journeys-vocabularies-list

List the closed vocabularies this app enforces

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysVocabularies = new sdk.JourneysVocabularies(client);

const result = await journeysVocabularies.journeysVocabulariesList();
```

## journeys-vocabularies-get

Read one vocabulary with its values and labels

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const journeysVocabularies = new sdk.JourneysVocabularies(client);

const result = await journeysVocabularies.journeysVocabulariesGet({
    name: ''
});
```
