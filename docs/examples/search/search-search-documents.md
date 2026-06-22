```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const search = new sdk.Search(client);

const result = await search.searchSearchDocuments({
    collection: sdk.Collection.Greetings,
    facetBy: '', // optional
    filterBy: '', // optional
    page: null, // optional
    perPage: null, // optional
    q: '', // optional
    queryBy: '', // optional
    sortBy: '' // optional
});
```
