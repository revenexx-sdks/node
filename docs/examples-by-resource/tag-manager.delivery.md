# tag-manager.delivery

## tag-manager-delivery-container

Read the storefront's published container

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerDelivery = new sdk.TagManagerDelivery(client);

const result = await tagManagerDelivery.tagManagerDeliveryContainer();
```

## tag-manager-delivery-preview

Read the draft container by preview token

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const tagManagerDelivery = new sdk.TagManagerDelivery(client);

const result = await tagManagerDelivery.tagManagerDeliveryPreview({
    token: ''
});
```
