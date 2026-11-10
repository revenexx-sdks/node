# campaigns.vocabularies

## campaigns-vocabularies-list

List the closed vocabularies this app enforces

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsVocabularies = new sdk.CampaignsVocabularies(client);

const result = await campaignsVocabularies.campaignsVocabulariesList();
```

## campaigns-vocabularies-get

Read one vocabulary with its values and labels

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsVocabularies = new sdk.CampaignsVocabularies(client);

const result = await campaignsVocabularies.campaignsVocabulariesGet({
    name: ''
});
```
