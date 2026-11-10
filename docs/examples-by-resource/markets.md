# markets

## markets-list

List markets

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsList({
    id: '', // optional
    code: 'northwind', // optional
    name: 'Northwind', // optional
    labels: '{"de-DE":"Nordwind","en-GB":"Northwind"}', // optional
    currency: 'EUR', // optional
    shipFromCountry: 'DE', // optional
    shipFromCountryReview: false, // optional
    status: sdk.MarketsListStatus.Active, // optional
    isDefault: false, // optional
    position: 0, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'position.asc' // optional
});
```

## markets-create

Create a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCreate({
    code: 'northwind',
    name: 'Northwind',
    currency: 'EUR', // optional
    isDefault: false, // optional
    labels: {
        "de-DE": "Nordwind",
        "en-GB": "Northwind"
    }, // optional
    position: 0, // optional
    shipFromCountry: 'DE', // optional
    shipFromCountryReview: false, // optional
    status: sdk.MarketStatus.Active // optional
});
```

## markets-defaults

Store the settings this app needs stored

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsDefaults({
    data: {}
});
```

## markets-locale-policy

Read the tenant-wide locale policy

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsLocalePolicy();
```

## markets-setup

Read the setup checklist

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsSetup();
```

## markets-vocabularies

List vocabularies

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsVocabularies();
```

## markets-vocabulary

Read one vocabulary with its values

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsVocabulary({
    name: sdk.MarketsVocabularyName.Marketstatuses
});
```

## markets-delete

Delete a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsDelete({
    id: ''
});
```

## markets-get

Read one market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsGet({
    id: ''
});
```

## markets-update

Update a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsUpdate({
    id: '',
    code: 'northwind', // optional
    currency: 'EUR', // optional
    isDefault: false, // optional
    labels: {
        "de-DE": "Nordwind",
        "en-GB": "Northwind"
    }, // optional
    name: 'Northwind', // optional
    position: 0, // optional
    shipFromCountry: 'DE', // optional
    shipFromCountryReview: false, // optional
    status: sdk.MarketStatus.Active // optional
});
```

## markets-backfill

Fill a market's gaps from another market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsBackfill({
    id: 'northwind',
    source: 'northwind',
    currencies: true, // optional
    locales: true, // optional
    taxClasses: true // optional
});
```

## markets-clone

Clone a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsClone({
    id: 'northwind',
    code: 'northwind_b2b',
    copyCurrencies: true, // optional
    copyLocales: true, // optional
    copyTaxClasses: true, // optional
    currency: 'EUR', // optional
    name: 'Northwind B2B', // optional
    shipFromCountry: 'DE', // optional
    status: sdk.MarketStatus.Active // optional
});
```

## markets-confirm-ship-from

Confirm the ship-from country of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsConfirmShipFrom({
    id: 'northwind',
    data: {}
});
```

## markets-context

Resolve the full market context

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsContext({
    id: ''
});
```

## markets-make-default

Make this market the tenant default

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsMakeDefault({
    id: 'northwind',
    data: {}
});
```

## markets-readiness

Check whether a market can trade

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsReadiness({
    id: 'northwind'
});
```

## markets-currencies-list

List currencies of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCurrenciesList({
    marketId: '',
    id: '', // optional
    code: 'EUR', // optional
    isDefault: true, // optional
    active: true, // optional
    position: 0, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'position.asc' // optional
});
```

## markets-currencies-create

Create a currency of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCurrenciesCreate({
    marketId: '',
    code: 'EUR',
    active: true, // optional
    isDefault: true, // optional
    position: 0 // optional
});
```

## markets-currencies-delete

Delete a currency of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCurrenciesDelete({
    marketId: '',
    id: ''
});
```

## markets-currencies-get

Read one currency of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCurrenciesGet({
    marketId: '',
    id: ''
});
```

## markets-currencies-update

Update a currency of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsCurrenciesUpdate({
    marketId: '',
    id: '',
    active: true, // optional
    code: 'EUR', // optional
    isDefault: true, // optional
    position: 0 // optional
});
```

## markets-locales-list

List locales of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsLocalesList({
    marketId: '',
    id: '', // optional
    code: 'de-DE', // optional
    language: 'de', // optional
    country: 'DE', // optional
    isDefault: true, // optional
    position: 0, // optional
    status: 'active', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'position.asc' // optional
});
```

## markets-locales-create

Create a locale of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsLocalesCreate({
    marketId: '',
    code: 'de-DE',
    country: 'DE', // optional
    isDefault: true, // optional
    language: 'de', // optional
    position: 0, // optional
    status: sdk.MarketsLocalesCreateStatus.Active // optional
});
```

## markets-locales-delete

Delete a locale of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsLocalesDelete({
    marketId: '',
    id: ''
});
```

## markets-locales-get

Read one locale of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsLocalesGet({
    marketId: '',
    id: ''
});
```

## markets-locales-update

Update a locale of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsLocalesUpdate({
    marketId: '',
    id: '',
    code: 'de-DE', // optional
    country: 'DE', // optional
    isDefault: true, // optional
    language: 'de', // optional
    position: 0, // optional
    status: 'active' // optional
});
```

## markets-tax-classes-list

List tax classes of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsTaxClassesList({
    marketId: '',
    id: '', // optional
    code: 'standard', // optional
    name: 'Standard rate', // optional
    labels: '{"de-DE":"Regelsatz","en-GB":"Standard rate"}', // optional
    rate: 20, // optional
    isDefault: true, // optional
    active: true, // optional
    position: 0, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'position.asc' // optional
});
```

## markets-tax-classes-create

Create a tax class of a market

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsTaxClassesCreate({
    marketId: '',
    code: 'standard',
    name: 'Standard rate',
    active: true, // optional
    isDefault: true, // optional
    labels: {
        "de-DE": "Regelsatz",
        "en-GB": "Standard rate"
    }, // optional
    position: 0, // optional
    rate: 20 // optional
});
```

## markets-tax-classes-delete

Delete a tax class of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsTaxClassesDelete({
    marketId: '',
    id: ''
});
```

## markets-tax-classes-get

Read one tax class of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsTaxClassesGet({
    marketId: '',
    id: ''
});
```

## markets-tax-classes-update

Update a tax class of a market by id

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const markets = new sdk.Markets(client);

const result = await markets.marketsTaxClassesUpdate({
    marketId: '',
    id: '',
    active: true, // optional
    code: 'standard', // optional
    isDefault: true, // optional
    labels: {
        "de-DE": "Regelsatz",
        "en-GB": "Standard rate"
    }, // optional
    name: 'Standard rate', // optional
    position: 0, // optional
    rate: 20 // optional
});
```
