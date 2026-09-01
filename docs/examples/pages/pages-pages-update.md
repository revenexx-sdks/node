```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pages = new sdk.Pages(client);

const result = await pages.pagesPagesUpdate({
    id: '',
    bundle: 'standard', // optional
    meta: {}, // optional
    slug: 'about-us', // optional
    status: sdk.PageStatus.Draft, // optional
    title: 'About us' // optional
});
```
