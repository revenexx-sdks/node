```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorMutate({
    pageId: '',
    plugin: 'add',
    langcode: 'de', // optional
    payload: {} // optional
});
```
