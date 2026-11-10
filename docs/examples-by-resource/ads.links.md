# ads.links

## ads-links-list

List ad campaigns and their campaigns

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsLinks = new sdk.AdsLinks(client);

const result = await adsLinks.adsLinksList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    adAccountId: '', // optional
    externalCampaignId: '', // optional
    externalName: '', // optional
    campaignId: '' // optional
});
```

## ads-links-create

List an ad campaign

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsLinks = new sdk.AdsLinks(client);

const result = await adsLinks.adsLinksCreate({
    adAccountId: '',
    externalCampaignId: '',
    campaignId: '', // optional
    externalName: '', // optional
    externalRefs: null, // optional
    metadata: null, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```

## ads-links-delete

Remove an ad campaign without spend

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsLinks = new sdk.AdsLinks(client);

const result = await adsLinks.adsLinksDelete({
    id: ''
});
```

## ads-links-get

Read one ad campaign link

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsLinks = new sdk.AdsLinks(client);

const result = await adsLinks.adsLinksGet({
    id: ''
});
```

## ads-links-update

Map an ad campaign to a campaign

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsLinks = new sdk.AdsLinks(client);

const result = await adsLinks.adsLinksUpdate({
    id: '',
    adAccountId: '', // optional
    campaignId: '', // optional
    externalCampaignId: '', // optional
    externalName: '', // optional
    externalRefs: null, // optional
    metadata: null, // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z' // optional
});
```
