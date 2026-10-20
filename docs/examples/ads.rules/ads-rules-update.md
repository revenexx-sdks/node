```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsRules = new sdk.AdsRules(client);

const result = await adsRules.adsRulesUpdate({
    id: '',
    active: true, // optional
    adAccountId: '', // optional
    consentPurpose: '', // optional
    event: sdk.Event.OrderPlaced, // optional
    externalConversionRef: '', // optional
    fixedValue: 9.99, // optional
    metadata: null, // optional
    name: '', // optional
    valueSource: sdk.ValueSource.OrderNet // optional
});
```
