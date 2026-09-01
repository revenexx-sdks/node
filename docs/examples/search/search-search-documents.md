```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const search = new sdk.Search(client);

const result = await search.searchSearchDocuments({
    collection: sdk.Collection.Products,
    excludeFields: '', // optional
    facetBy: '', // optional
    filterBy: '', // optional
    groupBy: '', // optional
    highlightFullFields: '', // optional
    includeFields: '', // optional
    maxFacetValues: 1, // optional
    numTypos: 1, // optional
    page: 1, // optional
    perPage: 1, // optional
    prefix: '', // optional
    q: '', // optional
    queryBy: '', // optional
    sortBy: '' // optional
});
```
