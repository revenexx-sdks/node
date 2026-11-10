# shipping.value-lists

## shipping-service-levels-list

The service levels this tenant keeps

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsList({
    limit: 1, // optional
    offset: 1, // optional
    active: true // optional
});
```

## shipping-service-levels-create

Add a service level

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsCreate({
    code: 'night_courier',
    title: 'Night courier',
    active: true, // optional
    description: 'When to pick this service level.', // optional
    descriptions: {
        "de": "Wann diese Option zu w\u00e4hlen ist.",
        "en": "When to pick this service level."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Night courier",
        "en": "Night courier"
    }, // optional
    position: 1, // optional
    tone: sdk.Tone.Neutral // optional
});
```

## shipping-service-levels-delete

Remove a service level no carrier uses

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsDelete({
    id: ''
});
```

## shipping-service-levels-get

Read one service level

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsGet({
    id: ''
});
```

## shipping-service-levels-update

Rename a service level or move it in the order

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsUpdate({
    id: '',
    active: true, // optional
    description: 'When to pick this service level.', // optional
    descriptions: {
        "de": "Wann diese Option zu w\u00e4hlen ist.",
        "en": "When to pick this service level."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Night courier",
        "en": "Night courier"
    }, // optional
    position: 1, // optional
    title: 'Night courier', // optional
    tone: sdk.Tone.Neutral // optional
});
```

## shipping-service-levels-make-default

Make this the default service level

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingServiceLevelsMakeDefault({
    id: '',
    data: {}
});
```

## shipping-vocabularies-list

List vocabularies

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingVocabulariesList();
```

## shipping-vocabularies-get

Read one vocabulary

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingVocabulariesGet({
    name: sdk.ShippingVocabulariesGetName.Carrierstatuses
});
```

## shipping-weight-units-list

The weight units this tenant quotes in

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsList({
    limit: 1, // optional
    offset: 1, // optional
    active: true // optional
});
```

## shipping-weight-units-create

Add a weight unit

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsCreate({
    code: 't',
    factor: 1000,
    title: 'Tonne',
    active: true, // optional
    description: 'When to pick this weight unit.', // optional
    descriptions: {
        "de": "Wann diese Option zu w\u00e4hlen ist.",
        "en": "When to pick this weight unit."
    }, // optional
    isDefault: true, // optional
    labels: {
        "de": "Tonne",
        "en": "Tonne"
    }, // optional
    position: 1, // optional
    tone: sdk.Tone.Neutral // optional
});
```

## shipping-weight-units-delete

Remove a weight unit nothing quotes in

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsDelete({
    id: ''
});
```

## shipping-weight-units-get

Read one weight unit

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsGet({
    id: ''
});
```

## shipping-weight-units-update

Rename a weight unit or correct its factor

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsUpdate({
    id: '',
    active: true, // optional
    description: 'When to pick this weight unit.', // optional
    descriptions: {
        "de": "Wann diese Option zu w\u00e4hlen ist.",
        "en": "When to pick this weight unit."
    }, // optional
    factor: 1000, // optional
    isDefault: true, // optional
    labels: {
        "de": "Tonne",
        "en": "Tonne"
    }, // optional
    position: 1, // optional
    title: 'Tonne', // optional
    tone: sdk.Tone.Neutral // optional
});
```

## shipping-weight-units-make-base

Make this the base weight unit

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsMakeBase({
    id: '',
    data: {}
});
```

## shipping-weight-units-make-default

Make this the default weight unit

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const shippingValueLists = new sdk.ShippingValueLists(client);

const result = await shippingValueLists.shippingWeightUnitsMakeDefault({
    id: '',
    data: {}
});
```
