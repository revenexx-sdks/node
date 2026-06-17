```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateTemplateDeployment({
    siteId: '',
    owner: '',
    reference: '',
    repository: '',
    rootDirectory: '',
    type: sdk.Type.Branch,
    activate: null // optional
});
```
