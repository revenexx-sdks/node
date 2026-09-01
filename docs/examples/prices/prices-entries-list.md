```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const prices = new sdk.Prices(client);

const result = await prices.pricesEntriesList({
    listId: '',
    id: '', // optional
    productId: '', // optional
    sku: 'BOLT-M8-30', // optional
    priceType: sdk.PriceEntryType.Standard, // optional
    quantityMin: 9.99, // optional
    unitPrice: 9.99, // optional
    unit: 'pcs', // optional
    validFrom: '2026-01-01T12:00:00Z', // optional
    validUntil: '2026-01-01T12:00:00Z', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```
