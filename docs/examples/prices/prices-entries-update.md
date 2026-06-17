```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const prices = new sdk.Prices(client);

const result = await prices.pricesEntriesUpdate({
    listId: '',
    id: '',
    metadata: {}, // optional
    priceType: sdk.PriceEntryType.Standard, // optional
    productId: '', // optional
    quantityMin: null, // optional
    sku: '', // optional
    unit: '', // optional
    unitPrice: null, // optional
    validFrom: '', // optional
    validUntil: '' // optional
});
```
