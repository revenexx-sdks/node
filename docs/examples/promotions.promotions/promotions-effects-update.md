```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsPromotions = new sdk.PromotionsPromotions(client);

const result = await promotionsPromotions.promotionsEffectsUpdate({
    id: '',
    amount: 9.99, // optional
    appliesTo: null, // optional
    bundleId: '', // optional
    customPayload: null, // optional
    customShapeVersion: 1, // optional
    customTypeId: '', // optional
    freeItemQuantity: 1, // optional
    freeItems: null, // optional
    kind: sdk.PromotionsEffectsCreateKind.Discount, // optional
    maxDiscount: 9.99, // optional
    message: null, // optional
    metadata: null, // optional
    position: 1, // optional
    promotionId: '', // optional
    requiresChoice: true, // optional
    spread: true, // optional
    targetScope: sdk.TargetScope.UnitPrice, // optional
    unitChoice: sdk.UnitChoice.Cheapest, // optional
    unitPosition: 1, // optional
    valueType: sdk.ValueType.Percentage // optional
});
```
