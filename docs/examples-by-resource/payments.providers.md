# payments.providers

## payments-logos-get

Serve a provider logo

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsLogosGet({
    slug: 'stripe',
    variant: sdk.Variant.Logo // optional
});
```

## payments-providers-list

List PSP configurations

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    provider: 'stripe', // optional
    enabled: true, // optional
    testMode: true // optional
});
```

## payments-providers-create

Create a PSP configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersCreate({
    provider: 'stripe',
    credentials: {}, // optional
    enabled: true, // optional
    name: 'Stripe', // optional
    options: {
        "capture_method": "automatic",
        "logo_url": "https:\/\/apps.example.com\/payments\/logos\/stripe",
        "three_ds": false
    }, // optional
    testMode: true, // optional
    webhookSecret: '' // optional
});
```

## payments-providers-catalog

List the PSPs that can be configured

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersCatalog();
```

## payments-providers-delete

Delete a PSP configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersDelete({
    id: ''
});
```

## payments-providers-get

Read one PSP configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersGet({
    id: ''
});
```

## payments-providers-update

Update a PSP configuration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersUpdate({
    id: '',
    credentials: {}, // optional
    enabled: true, // optional
    name: 'Stripe', // optional
    options: {
        "capture_method": "automatic",
        "logo_url": "https:\/\/apps.example.com\/payments\/logos\/stripe",
        "three_ds": false
    }, // optional
    provider: 'stripe', // optional
    testMode: true, // optional
    webhookSecret: '' // optional
});
```

## payments-providers-check

Check a PSP configuration's credentials

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const paymentsProviders = new sdk.PaymentsProviders(client);

const result = await paymentsProviders.paymentsProvidersCheck({
    id: ''
});
```
