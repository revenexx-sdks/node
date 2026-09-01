```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateDeployment({
    siteId: '',
    activate: true,
    code: InputFile.fromPath('/path/to/file', 'filename'),
    buildCommand: '', // optional
    installCommand: '', // optional
    outputDirectory: '' // optional
});
```
