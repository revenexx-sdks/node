# campaigns.attribution

## campaigns-attribution-list

List attribution facts

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsAttribution = new sdk.CampaignsAttribution(client);

const result = await campaignsAttribution.campaignsAttributionList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    factKey: '', // optional
    campaignId: '', // optional
    orderId: '', // optional
    orderNumber: '', // optional
    contactId: '', // optional
    organizationId: '', // optional
    currency: '', // optional
    market: '', // optional
    touchKind: '', // optional
    touchRef: '', // optional
    isFirstTouch: '' // optional
});
```

## campaigns-attribution-get

Read one attribution fact

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsAttribution = new sdk.CampaignsAttribution(client);

const result = await campaignsAttribution.campaignsAttributionGet({
    id: ''
});
```

## campaigns-attribution-sweep

Record what orders and redemptions of the last two days owe campaigns

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsAttribution = new sdk.CampaignsAttribution(client);

const result = await campaignsAttribution.campaignsAttributionSweep({
    data: {}
});
```
