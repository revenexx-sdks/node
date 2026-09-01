```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const search = new sdk.Search(client);

const result = await search.searchSearchDocumentsGet({
    collection: sdk.Collection.Products,
    q: '', // optional
    queryBy: '', // optional
    filterBy: '', // optional
    sortBy: '', // optional
    facetBy: '', // optional
    maxFacetValues: 1, // optional
    groupBy: '', // optional
    includeFields: '', // optional
    excludeFields: '', // optional
    highlightFullFields: '', // optional
    numTypos: 1, // optional
    prefix: '', // optional
    page: 1, // optional
    perPage: 1 // optional
});
```
