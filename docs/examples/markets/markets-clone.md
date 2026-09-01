```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsClone({
    id: 'northwind',
    code: 'northwind-b2b',
    copyCurrencies: true, // optional
    copyLocales: true, // optional
    copyTaxClasses: true, // optional
    currency: 'EUR', // optional
    name: 'Northwind B2B', // optional
    status: sdk.MarketStatus.Active // optional
});
```
