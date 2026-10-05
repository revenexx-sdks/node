```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsPromotions = new sdk.PromotionsPromotions(client);

const result = await promotionsPromotions.promotionsConditionsUpdate({
    id: '',
    promotionId: '',
    addend: 9.99, // optional
    compareValue: {}, // optional
    compareValueTo: {}, // optional
    comparison: '', // optional
    factor: 9.99, // optional
    kind: sdk.PromotionsConditionsCreateKind.Group, // optional
    matchMode: sdk.MatchMode.All, // optional
    negate: true, // optional
    parentId: '', // optional
    position: 1, // optional
    rightSubject: '', // optional
    subject: '' // optional
});
```
