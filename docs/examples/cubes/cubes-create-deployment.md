```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesCreateDeployment({
    cubeId: '',
    code: InputFile.fromPath('/path/to/file', 'filename'),
    activate: true // optional
});
```
