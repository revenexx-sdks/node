```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pages = new sdk.Pages(client);

const result = await pages.pagesTemplatesUpdate({
    id: '',
    description: 'Full-width hero followed by a two-column teaser row.', // optional
    fieldName: 'content', // optional
    isDefault: true, // optional
    label: 'Hero with two teasers', // optional
    pageBundle: 'standard', // optional
    tree: [] // optional
});
```
