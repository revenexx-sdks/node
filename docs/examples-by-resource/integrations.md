# integrations

## integrations-list

List integrations

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsList({
    queries: [], // optional
    search: '', // optional
    total: true // optional
});
```

## integrations-create

Create integration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsCreate({
    integrationId: '',
    name: '',
    enabled: true, // optional
    installationId: '', // optional
    logging: true, // optional
    providerBranch: '', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    vcsPreviewsEnabled: true, // optional
    vcsTriggerMode: sdk.VcsTriggerMode.Push // optional
});
```

## integrations-delete

Delete integration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsDelete({
    integrationId: ''
});
```

## integrations-get

Get integration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsGet({
    integrationId: ''
});
```

## integrations-update

Update integration

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsUpdate({
    integrationId: '',
    name: '',
    enabled: true, // optional
    installationId: '', // optional
    logging: true, // optional
    providerBranch: '', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    vcsPreviewsEnabled: true, // optional
    vcsTriggerMode: sdk.VcsTriggerMode.Push // optional
});
```

## integrations-list-deployments

List deployments

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsListDeployments({
    integrationId: '',
    queries: [], // optional
    search: '', // optional
    total: true // optional
});
```

## integrations-create-deployment

Create deployment

```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsCreateDeployment({
    integrationId: '',
    code: InputFile.fromPath('/path/to/file', 'filename'),
    activate: true, // optional
    releaseMode: sdk.ReleaseMode.Deploy // optional
});
```

## integrations-create-vcs-deployment

Create VCS deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsCreateVcsDeployment({
    integrationId: '',
    reference: '',
    type: sdk.CubesCreateVcsDeploymentType.Branch,
    activate: true // optional
});
```

## integrations-get-deployment

Get deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsGetDeployment({
    integrationId: '',
    deploymentId: ''
});
```

## integrations-list-releases

List integration releases

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsListReleases({
    integrationId: ''
});
```

## integrations-accept-release

Accept integration release candidate

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsAcceptRelease({
    integrationId: '',
    rc: 1, // optional
    version: '' // optional
});
```

## integrations-rebuild-release

Rebuild integration release

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const integrations = new sdk.Integrations(client);

const result = await integrations.integrationsRebuildRelease({
    integrationId: '',
    version: '',
    commit: '' // optional
});
```
