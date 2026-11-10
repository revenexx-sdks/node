# mailings.mailings

## mailings-mailings-list

List mailings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    state: '', // optional
    folder: '', // optional
    campaignRef: '', // optional
    audienceId: '', // optional
    subscriptionType: '', // optional
    templateKey: '', // optional
    starter: '', // optional
    timezoneMode: '', // optional
    duplicatedFromId: '' // optional
});
```

## mailings-mailings-create

Write a mailing down as a draft

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsCreate({
    name: '',
    audienceId: '', // optional
    campaignRef: '', // optional
    currency: '', // optional
    excludeAudienceIds: [], // optional
    graymail: true, // optional
    graymailSends: 1, // optional
    metadata: null, // optional
    previewText: '', // optional
    replyTo: '', // optional
    sendAt: '2026-01-01T12:00:00Z', // optional
    sender: '', // optional
    senderName: '', // optional
    starter: sdk.Starter.Blank, // optional
    subject: '', // optional
    subscriptionType: '', // optional
    templateKey: '', // optional
    timezoneMode: sdk.TimezoneMode.Tenant, // optional
    voucherBatchId: '' // optional
});
```

## mailings-mailings-empty-trash

Empty the mailing trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsEmptyTrash();
```

## mailings-mailings-purge

Delete the mailings that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsPurge();
```

## mailings-mailings-delete

Move a mailing to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsDelete({
    id: ''
});
```

## mailings-mailings-get

Read one mailing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsGet({
    id: ''
});
```

## mailings-mailings-update

Change a mailing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsUpdate({
    id: '',
    audienceId: '', // optional
    campaignRef: '', // optional
    currency: '', // optional
    excludeAudienceIds: [], // optional
    graymail: true, // optional
    graymailSends: 1, // optional
    metadata: null, // optional
    name: '', // optional
    previewText: '', // optional
    replyTo: '', // optional
    sendAt: '2026-01-01T12:00:00Z', // optional
    sender: '', // optional
    senderName: '', // optional
    starter: sdk.Starter.Blank, // optional
    subject: '', // optional
    subscriptionType: '', // optional
    templateKey: '', // optional
    timezoneMode: sdk.TimezoneMode.Tenant, // optional
    voucherBatchId: '' // optional
});
```

## mailings-mailings-archive

Archive a mailing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsArchive({
    id: '',
    data: {}
});
```

## mailings-mailings-cancel

Cancel a scheduled or sending mailing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsCancel({
    id: '',
    data: {}
});
```

## mailings-mailings-checklist

Read what must be true before a mailing may be scheduled

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsChecklist({
    id: ''
});
```

## mailings-mailings-duplicate

Copy a mailing as a new draft

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsDuplicate({
    id: '',
    data: {}
});
```

## mailings-mailings-preview

Render a mailing as one recipient sees it

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsPreview({
    id: '',
    contactId: '', // optional
    device: sdk.Device.Desktop, // optional
    email: '', // optional
    firstName: '', // optional
    lastName: '', // optional
    locale: '', // optional
    market: '' // optional
});
```

## mailings-mailings-reach

Read how many a mailing would reach

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsReach({
    id: ''
});
```

## mailings-mailings-restore

Bring a mailing back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsRestore({
    id: ''
});
```

## mailings-mailings-schedule

Schedule a mailing, now or at a time

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsSchedule({
    id: '',
    sendAt: '', // optional
    start: true, // optional
    timezoneMode: sdk.TimezoneMode.Tenant // optional
});
```

## mailings-mailings-test

Send a mailing to colleagues as a test

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsTest({
    id: '',
    locale: '', // optional
    market: '', // optional
    recipients: [] // optional
});
```

## mailings-mailings-unarchive

Take a mailing out of the archive

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsUnarchive({
    id: '',
    data: {}
});
```
