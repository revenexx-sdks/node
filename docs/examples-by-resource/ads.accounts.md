# ads.accounts

## ads-accounts-list

List ad accounts

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.Trashed.Exclude, // optional
    id: '', // optional
    platform: '', // optional
    externalAccountId: '', // optional
    name: '', // optional
    connectionRef: '', // optional
    status: '', // optional
    currency: '', // optional
    lastError: '', // optional
    clicksTotal: '', // optional
    conversionsTotal: '', // optional
    deletedBy: '', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeBlockedReason: '' // optional
});
```

## ads-accounts-create

Add an ad account

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsCreate({
    externalAccountId: '',
    name: '',
    platform: sdk.Platform.Meta,
    clicksTotal: 1, // optional
    connectionRef: '', // optional
    conversionValueTotal: 9.99, // optional
    conversionsTotal: 1, // optional
    currency: '', // optional
    externalRefs: null, // optional
    figuresAt: '2026-01-01T12:00:00Z', // optional
    metadata: null, // optional
    roas: 9.99, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    spendTotal: 9.99 // optional
});
```

## ads-accounts-empty-trash

Empty the ad account trash, deleting each one for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsEmptyTrash();
```

## ads-accounts-purge

Delete the ad accounts that outlived the trash retention

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsPurge();
```

## ads-accounts-delete

Move a ad account to the trash, or delete it for good from there

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsDelete({
    id: ''
});
```

## ads-accounts-get

Read one ad account

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsGet({
    id: ''
});
```

## ads-accounts-update

Rename an ad account or change its connection

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsUpdate({
    id: '',
    clicksTotal: 1, // optional
    connectionRef: '', // optional
    conversionValueTotal: 9.99, // optional
    conversionsTotal: 1, // optional
    currency: '', // optional
    externalAccountId: '', // optional
    externalRefs: null, // optional
    figuresAt: '2026-01-01T12:00:00Z', // optional
    metadata: null, // optional
    name: '', // optional
    platform: sdk.Platform.Meta, // optional
    roas: 9.99, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    spendTotal: 9.99 // optional
});
```

## ads-accounts-restore

Bring a ad account back out of the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsRestore({
    id: ''
});
```

## ads-accounts-status

Report the state of an ad account connection

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsAccounts = new sdk.AdsAccounts(client);

const result = await adsAccounts.adsAccountsStatus({
    id: '',
    status: sdk.Status.Connected,
    error: '' // optional
});
```
