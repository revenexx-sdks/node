```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const apps = new sdk.Apps(client);

const result = await apps.appsCreateDeployment({
    functionId: '',
    activate: true,
    code: InputFile.fromPath('/path/to/file', 'filename'),
    commands: '', // optional
    entrypoint: '' // optional
});
```
