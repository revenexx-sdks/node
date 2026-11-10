# loyalty.vocabularies

## loyalty-vocabularies-list

List the closed vocabularies this app enforces

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyVocabularies = new sdk.LoyaltyVocabularies(client);

const result = await loyaltyVocabularies.loyaltyVocabulariesList();
```

## loyalty-vocabularies-get

Read one vocabulary with its values and labels

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyVocabularies = new sdk.LoyaltyVocabularies(client);

const result = await loyaltyVocabularies.loyaltyVocabulariesGet({
    name: ''
});
```
