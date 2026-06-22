```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const prices = new sdk.Prices(client);

const result = await prices.pricesListsCreate({
    code: '',
    name: '',
    channelId: '', // optional
    contactId: '', // optional
    currency: '', // optional
    description: '', // optional
    isDefault: null, // optional
    labels: {}, // optional
    marketId: '', // optional
    metadata: {}, // optional
    organizationId: '', // optional
    priority: null, // optional
    status: sdk.PriceListStatus.Active, // optional
    taxIncluded: null, // optional
    validFrom: '', // optional
    validUntil: '' // optional
});
```
