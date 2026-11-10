# carts.io

## carts-export-all

Export many carts through one profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsExportAll({
    contactId: '', // optional
    createdFrom: '2026-09-01', // optional
    createdTo: '2026-09-30', // optional
    cursor: '', // optional
    format: sdk.CartExportFormat.Json, // optional
    limit: 1, // optional
    market: 'de', // optional
    profileId: '', // optional
    status: null // optional
});
```

## carts-import

Import a cart from JSON, CSV or Excel

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsImport({
    sessionKey: 'a1b2c3d4e5f6', // optional
    contactId: '', // optional
    csv: 'sku,name,quantity,unit_price
BOLT-M8-30,Hex bolt M8,100,0.12
NUT-M8,Hex nut M8,100,0.04
', // optional
    name: 'Weekly order', // optional
    organizationId: '', // optional
    payload: {
        "cart": {
            "currency": "EUR",
            "name": "Weekly order"
        },
        "items": [
            {
                "name": "Hex bolt M8",
                "quantity": 100,
                "sku": "BOLT-M8-30",
                "unit_price": 0.12
            }
        ]
    }, // optional
    profileId: '', // optional
    sessionKeyBody: 'a1b2c3d4e5f6', // optional
    targetCartId: '', // optional
    xlsx: 'UEsDBBQABgAIAAAAIQ…' // optional
});
```

## carts-io-fields

List the fields a profile can map

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoFields({
    entity: sdk.CartIoFieldEntity.CartItems, // optional
    role: sdk.CartIoFieldRole.Column // optional
});
```

## carts-io-profiles-list

List import/export profiles

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesList({
    id: '', // optional
    name: 'cart-export-csv', // optional
    direction: sdk.CartIoDirection.Import, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    isTemplate: true, // optional
    active: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```

## carts-io-profiles-create

Create an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesCreate({
    direction: sdk.CartIoDirection.Import,
    name: 'cart-export-csv',
    active: true, // optional
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    isTemplate: true, // optional
    mapping: {}, // optional
    options: {} // optional
});
```

## carts-io-profiles-defaults

Seed the bundled profile templates

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesDefaults();
```

## carts-io-profiles-delete

Delete an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesDelete({
    id: ''
});
```

## carts-io-profiles-get

Read one import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesGet({
    id: ''
});
```

## carts-io-profiles-update

Update an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesUpdate({
    id: '',
    active: true, // optional
    applyMode: sdk.CartIoApplyMode.Insert, // optional
    direction: sdk.CartIoDirection.Import, // optional
    entity: sdk.CartIoEntity.Carts, // optional
    format: sdk.CartIoFormat.Json, // optional
    isTemplate: true, // optional
    mapping: {}, // optional
    name: 'cart-export-csv', // optional
    options: {} // optional
});
```

## carts-io-profiles-copy

Copy an import/export profile

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsIoProfilesCopy({
    id: '',
    name: 'my-cart-import',
    parts: [] // optional
});
```

## carts-export

Export a cart as JSON, CSV or Excel

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cartsIo = new sdk.CartsIo(client);

const result = await cartsIo.cartsExport({
    id: '',
    sessionKey: 'a1b2c3d4e5f6', // optional
    format: sdk.CartExportFormat.Json, // optional
    profileId: '' // optional
});
```
