# cubes

## cubes-list

List Cubes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesList({
    queries: [], // optional
    search: '', // optional
    total: true // optional
});
```

## cubes-create

Create Cube

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesCreate({
    cubeId: '',
    name: '',
    enabled: true, // optional
    installationId: '', // optional
    logging: true, // optional
    providerBranch: '', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    vcsTriggerMode: sdk.VcsTriggerMode.Push // optional
});
```

## cubes-delete

Delete Cube

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesDelete({
    cubeId: ''
});
```

## cubes-get

Get Cube

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesGet({
    cubeId: ''
});
```

## cubes-update

Update Cube

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesUpdate({
    cubeId: '',
    name: '',
    enabled: true, // optional
    installationId: '', // optional
    logging: true, // optional
    providerBranch: '', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    vcsTriggerMode: sdk.VcsTriggerMode.Push // optional
});
```

## cubes-list-deployments

List deployments

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesListDeployments({
    cubeId: '',
    queries: [], // optional
    search: '', // optional
    total: true // optional
});
```

## cubes-create-deployment

Create deployment

```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesCreateDeployment({
    cubeId: '',
    code: InputFile.fromPath('/path/to/file', 'filename'),
    activate: true, // optional
    releaseMode: sdk.ReleaseMode.Deploy // optional
});
```

## cubes-create-vcs-deployment

Create VCS deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesCreateVcsDeployment({
    cubeId: '',
    reference: '',
    type: sdk.CubesCreateVcsDeploymentType.Branch,
    activate: true // optional
});
```

## cubes-get-deployment

Get deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesGetDeployment({
    cubeId: '',
    deploymentId: ''
});
```

## cubes-list-releases

List cube releases

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesListReleases({
    cubeId: ''
});
```

## cubes-accept-release

Accept cube release candidate

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesAcceptRelease({
    cubeId: '',
    rc: 1, // optional
    version: '' // optional
});
```

## cubes-rebuild-release

Rebuild cube release

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const cubes = new sdk.Cubes(client);

const result = await cubes.cubesRebuildRelease({
    cubeId: '',
    version: '',
    commit: '', // optional
    deploymentId: '' // optional
});
```
