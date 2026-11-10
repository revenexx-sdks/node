# ads.rules

## ads-rules-list

List conversion rules

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsRules = new sdk.AdsRules(client);

const result = await adsRules.adsRulesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    adAccountId: '', // optional
    name: '', // optional
    event: '', // optional
    valueSource: '', // optional
    externalConversionRef: '', // optional
    consentPurpose: '', // optional
    active: '' // optional
});
```

## ads-rules-create

Add a conversion rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsRules = new sdk.AdsRules(client);

const result = await adsRules.adsRulesCreate({
    adAccountId: '',
    event: sdk.Event.OrderPlaced,
    name: '',
    active: true, // optional
    consentPurpose: '', // optional
    externalConversionRef: '', // optional
    fixedValue: 9.99, // optional
    metadata: null, // optional
    valueSource: sdk.ValueSource.OrderNet // optional
});
```

## ads-rules-delete

Delete a rule that recorded nothing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsRules = new sdk.AdsRules(client);

const result = await adsRules.adsRulesDelete({
    id: ''
});
```

## ads-rules-get

Read one conversion rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const adsRules = new sdk.AdsRules(client);

const result = await adsRules.adsRulesGet({
    id: ''
});
```

## ads-rules-update

Correct a conversion rule

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
