```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesUpdate({
    siteId: '',
    framework: sdk.Framework.Analog,
    name: '',
    adapter: sdk.Adapter.Static, // optional
    buildCommand: '', // optional
    buildRuntime: sdk.BuildRuntime.Node180, // optional
    enabled: null, // optional
    fallbackFile: '', // optional
    installCommand: '', // optional
    installationId: '', // optional
    logging: null, // optional
    outputDirectory: '', // optional
    providerBranch: '', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: null, // optional
    specification: '', // optional
    timeout: null // optional
});
```
