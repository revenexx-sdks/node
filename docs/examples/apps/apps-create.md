```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const apps = new sdk.Apps(client);

const result = await apps.appsCreate({
    functionId: '',
    name: '',
    runtime: sdk.Runtime.Node180,
    commands: 'npm install', // optional
    enabled: true, // optional
    entrypoint: 'src/main.js', // optional
    events: [], // optional
    execute: ["any"], // optional
    installationId: '', // optional
    logging: true, // optional
    providerBranch: 'main', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    schedule: '0 3 * * *', // optional
    scopes: [sdk.Scopes.SessionsWrite], // optional
    specification: 's-1vcpu-512mb', // optional
    timeout: 1 // optional
});
```
