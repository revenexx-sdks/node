# pages.editor

## pages-editor-edit-states

Search open edit states across pages

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorEditStates({
    status: sdk.PageEditStateStatus.Active, // optional
    limit: 1, // optional
    offset: 1 // optional
});
```

## pages-editor-translate

Machine-translate text fields

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorTranslate({
    items: [] // optional
});
```

## pages-editor-user-settings-get

Load the current user's editor settings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorUserSettingsGet();
```

## pages-editor-user-settings-put

Persist the current user's editor settings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorUserSettingsPut({
    settings: {} // optional
});
```

## pages-editor-history

Move the undo/redo pointer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorHistory({
    pageId: '',
    index: 1,
    langcode: 'de' // optional
});
```

## pages-editor-last-changed

Poll the edit state's last change

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorLastChanged({
    pageId: ''
});
```

## pages-editor-mutation-status

Soft-enable/disable a single mutation in the log

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorMutationStatus({
    pageId: '',
    enabled: true,
    index: 1,
    langcode: 'de' // optional
});
```

## pages-editor-mutate

Append a mutation to the edit state

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

## pages-editor-preview-grant

Create a preview share token

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorPreviewGrant({
    pageId: '',
    ttlHours: 1 // optional
});
```

## pages-editor-publish

Publish the edit state

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorPublish({
    pageId: '',
    force: true, // optional
    label: 'Autumn campaign' // optional
});
```

## pages-editor-revert

Discard all unpublished changes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorRevert({
    pageId: ''
});
```

## pages-editor-schedule

Park the edit state for a future publication date

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorSchedule({
    pageId: '',
    scheduledAt: '2026-01-01T12:00:00Z'
});
```

## pages-editor-state

Load the editor state for a page

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorState({
    pageId: '',
    langcode: 'de', // optional
    index: 1 // optional
});
```

## pages-editor-take-ownership

Take ownership of the edit state

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorTakeOwnership({
    pageId: ''
});
```

## pages-editor-templates-create

Create a template from the edit state

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorTemplatesCreate({
    pageId: '',
    label: 'Hero with two teasers',
    uuids: [],
    description: 'Full-width hero followed by a two-column teaser row.', // optional
    fieldName: 'content', // optional
    isDefault: true, // optional
    pageBundle: 'standard' // optional
});
```

## pages-editor-unschedule

Cancel a scheduled publish

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const pagesEditor = new sdk.PagesEditor(client);

const result = await pagesEditor.pagesEditorUnschedule({
    pageId: ''
});
```
