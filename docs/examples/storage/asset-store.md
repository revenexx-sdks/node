```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const storage = new sdk.Storage(client);

const result = await storage.assetStore({
    file: '',
    altText: '', // optional
    description: '', // optional
    displayName: '', // optional
    folderId: '', // optional
    keepArchive: null, // optional
    tags: [], // optional
    unpack: null, // optional
    visibility: sdk.Visibility.Public // optional
});
```
