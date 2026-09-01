```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsCreate({
    code: 'key_accounts',
    labels: {
        "de": "Gro\u00dfkunden",
        "en": "Key accounts"
    }, // optional
    position: 1, // optional
    ruleMatch: sdk.SegmentRuleMatch.All, // optional
    rules: {} // optional
});
```
