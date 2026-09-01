```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const channels = new sdk.Channels(client);

const result = await channels.channelsList({
    id: '', // optional
    code: 'shop', // optional
    name: 'Shop', // optional
    labels: '{"en":"Shop","de":"Shop"}', // optional
    type: 'storefront', // optional
    status: sdk.ChannelStatus.Active, // optional
    unassignedVisibility: sdk.ChannelUnassignedVisibility.Inherit, // optional
    isDefault: true, // optional
    position: 1, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```
