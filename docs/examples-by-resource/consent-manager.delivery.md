# consent-manager.delivery

## consent-manager-delivery-policy

Read the published policy for this market (storefront)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerDelivery = new sdk.ConsentManagerDelivery(client);

const result = await consentManagerDelivery.consentManagerDeliveryPolicy();
```

## consent-manager-delivery-preview

Read a draft preview by token

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerDelivery = new sdk.ConsentManagerDelivery(client);

const result = await consentManagerDelivery.consentManagerDeliveryPreview({
    token: ''
});
```
