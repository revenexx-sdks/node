```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const promotionsPromotions = new sdk.PromotionsPromotions(client);

const result = await promotionsPromotions.promotionsPromotionsUpdate({
    id: '',
    code: '',
    name: '',
    budgetDiscount: 9.99, // optional
    budgetRedemptions: 1, // optional
    campaignRef: '', // optional
    channelId: '', // optional
    conditionMatch: sdk.ConditionMatch.All, // optional
    currency: '', // optional
    description: '', // optional
    endsAt: '2026-01-01T12:00:00Z', // optional
    exclusive: true, // optional
    groupId: '', // optional
    labels: {}, // optional
    limitPerContact: 1, // optional
    limitPerOrganization: 1, // optional
    metadata: {}, // optional
    priority: 1, // optional
    reach: sdk.Reach.Automatic, // optional
    recurrenceDays: {}, // optional
    recurrenceFrom: '', // optional
    recurrenceKind: sdk.RecurrenceKind.None, // optional
    recurrenceUntil: '', // optional
    recurrenceWeekdays: {}, // optional
    returnBehaviour: sdk.ReturnBehaviour.ReverseProportionally, // optional
    searchBestCombination: true, // optional
    startsAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.PromotionsPromotionsCreateStatus.Draft, // optional
    tags: {}, // optional
    timezone: '' // optional
});
```
