```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsPromotions = new sdk.PromotionsPromotions(client);

const result = await promotionsPromotions.promotionsConditionsUpdate({
    id: '',
    addend: 9.99, // optional
    compareValue: null, // optional
    compareValueTo: null, // optional
    comparison: '', // optional
    factor: 9.99, // optional
    kind: sdk.AudiencesRulesCreateKind.Group, // optional
    matchMode: sdk.MatchMode.All, // optional
    negate: true, // optional
    parentId: '', // optional
    position: 1, // optional
    promotionId: '', // optional
    rightSubject: '', // optional
    subject: '' // optional
});
```
