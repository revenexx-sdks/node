```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsToggleTask({
    pageId: '',
    uuid: '',
    taskIndex: 1
});
```
