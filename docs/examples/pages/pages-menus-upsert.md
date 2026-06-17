```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pages = new sdk.Pages(client);

const result = await pages.pagesMenusUpsert({
    label: '',
    menuKey: '',
    items: [] // optional
});
```
