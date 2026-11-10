# customers.roles

## customers-permissions-ledger

Read the permission ledger

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersPermissionsLedger();
```

## customers-roles-list

List the customer role catalogue

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersRolesList();
```

## customers-roles-create

Create a customer role with its permissions

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersRolesCreate({
    title: 'Einkauf Zentrale',
    active: true, // optional
    description: '', // optional
    descriptions: {}, // optional
    isDefault: true, // optional
    key: 'einkauf-zentrale', // optional
    labels: {}, // optional
    permissions: [], // optional
    position: 1 // optional
});
```

## customers-roles-defaults

Seed the built-in customer roles

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersRolesDefaults({
    data: {}
});
```

## customers-roles-update

Edit a customer role

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersRolesUpdate({
    key: 'einkauf-zentrale',
    active: true, // optional
    description: '', // optional
    descriptions: {}, // optional
    isDefault: true, // optional
    labels: {}, // optional
    position: 1, // optional
    title: 'Einkauf Zentrale', // optional
    tone: sdk.Tone.Neutral // optional
});
```

## customers-roles-copy

Start a new role from an existing one

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersRolesCopy({
    key: 'buyer',
    title: 'Einkäufer Werk 2',
    description: '', // optional
    keyBody: '' // optional
});
```

## customers-roles-permissions-replace

Replace a role's permission set

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersRoles = new sdk.CustomersRoles(client);

const result = await customersRoles.customersRolesPermissionsReplace({
    key: 'buyer',
    permissions: []
});
```
