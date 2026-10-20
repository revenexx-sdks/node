```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsConversions = new sdk.AdsConversions(client);

const result = await adsConversions.adsConversionsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    ruleId: '', // optional
    adAccountId: '', // optional
    eventKey: '', // optional
    event: '', // optional
    platform: '', // optional
    sourceRef: '', // optional
    orderId: '', // optional
    clickId: '', // optional
    clickIdKind: '', // optional
    hashedEmail: '', // optional
    currency: '', // optional
    state: '', // optional
    attempts: '', // optional
    externalRef: '', // optional
    lastError: '' // optional
});
```
