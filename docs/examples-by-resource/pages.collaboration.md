# pages.collaboration

## pages-editor-notifications-list

List the current user's notifications

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorNotificationsList({
    after: '', // optional
    markAsRead: 'true' // optional
});
```

## pages-editor-notifications-mark-all-read

Mark all notifications read

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorNotificationsMarkAllRead();
```

## pages-editor-notifications-unread-count

Unread notification count

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorNotificationsUnreadCount();
```

## pages-editor-users

List users for @mentions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorUsers();
```

## pages-editor-comments-list

List a page's comments

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsList({
    pageId: ''
});
```

## pages-editor-comments-create

Add a comment or reply

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsCreate({
    pageId: '',
    body: '<p>Please shorten this headline.</p>',
    blockUuids: [], // optional
    parentUuid: '' // optional
});
```

## pages-editor-comments-delete

Delete a comment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsDelete({
    pageId: '',
    uuid: ''
});
```

## pages-editor-comments-update

Edit a comment body

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsUpdate({
    pageId: '',
    uuid: '',
    body: '<p>Please shorten this headline.</p>'
});
```

## pages-editor-comments-resolve

Resolve a comment thread

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsResolve({
    pageId: '',
    uuid: ''
});
```

## pages-editor-comments-toggle-task

Toggle a task checkbox in a comment

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

## pages-editor-comments-unresolve

Reopen a resolved thread

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesCollaboration = new sdk.PagesCollaboration(client);

const result = await pagesCollaboration.pagesEditorCommentsUnresolve({
    pageId: '',
    uuid: ''
});
```
