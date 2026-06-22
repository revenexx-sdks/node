```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const apps = new sdk.Apps(client);

const result = await apps.appsListTemplates({
    runtimes: [sdk.Runtimes.Node180], // optional
    useCases: [sdk.UseCases.Starter], // optional
    limit: null, // optional
    offset: null, // optional
    total: null // optional
});
```
