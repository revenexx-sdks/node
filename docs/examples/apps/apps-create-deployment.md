```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const apps = new sdk.Apps(client);

const result = await apps.appsCreateDeployment({
    functionId: '',
    activate: null,
    code: '',
    commands: '', // optional
    entrypoint: '' // optional
});
```
