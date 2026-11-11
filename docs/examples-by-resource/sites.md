# sites

## sites-list

List sites

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesList({
    queries: [], // optional
    search: '', // optional
    total: true // optional
});
```

## sites-create

Create site

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreate({
    buildRuntime: sdk.BuildRuntime.Node180,
    framework: sdk.Framework.Analog,
    name: '',
    siteId: '',
    adapter: sdk.Adapter.Static, // optional
    buildCommand: 'npm run build', // optional
    enabled: true, // optional
    fallbackFile: 'index.html', // optional
    installCommand: 'npm install', // optional
    installationId: '', // optional
    logging: true, // optional
    outputDirectory: '', // optional
    providerBranch: 'main', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    specification: 's-1vcpu-512mb', // optional
    timeout: 1, // optional
    vcsPreviewsEnabled: true, // optional
    vcsTriggerMode: sdk.VcsTriggerMode.Push // optional
});
```

## sites-list-frameworks

List frameworks

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesListFrameworks();
```

## sites-list-specifications

List specifications

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesListSpecifications();
```

## sites-delete

Delete site

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesDelete({
    siteId: ''
});
```

## sites-get

Get site

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesGet({
    siteId: ''
});
```

## sites-update

Update site

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesUpdate({
    siteId: '',
    framework: sdk.Framework.Analog,
    name: '',
    adapter: sdk.Adapter.Static, // optional
    buildCommand: 'npm run build', // optional
    buildRuntime: sdk.BuildRuntime.Node180, // optional
    enabled: true, // optional
    fallbackFile: 'index.html', // optional
    installCommand: 'npm install', // optional
    installationId: '', // optional
    logging: true, // optional
    outputDirectory: '', // optional
    providerBranch: 'main', // optional
    providerRepositoryId: '', // optional
    providerRootDirectory: '', // optional
    providerSilentMode: true, // optional
    specification: 's-1vcpu-512mb', // optional
    timeout: 1, // optional
    vcsPreviewsEnabled: true, // optional
    vcsTriggerMode: sdk.VcsTriggerMode.Push // optional
});
```

## sites-update-site-deployment

Update site's deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesUpdateSiteDeployment({
    siteId: '',
    deploymentId: ''
});
```

## sites-list-deployments

List deployments

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesListDeployments({
    siteId: '',
    queries: [], // optional
    search: '', // optional
    total: true // optional
});
```

## sites-create-deployment

Create deployment

```javascript
const sdk = require('@revenexx/node');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateDeployment({
    siteId: '',
    activate: true,
    code: InputFile.fromPath('/path/to/file', 'filename'),
    buildCommand: '', // optional
    installCommand: '', // optional
    outputDirectory: '', // optional
    releaseMode: sdk.ReleaseMode.Deploy // optional
});
```

## sites-create-duplicate-deployment

Create duplicate deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateDuplicateDeployment({
    siteId: '',
    deploymentId: ''
});
```

## sites-create-template-deployment

Create template deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateTemplateDeployment({
    siteId: '',
    owner: '',
    reference: '',
    repository: '',
    rootDirectory: '',
    type: sdk.CubesCreateVcsDeploymentType.Branch,
    activate: true // optional
});
```

## sites-create-vcs-deployment

Create VCS deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateVcsDeployment({
    siteId: '',
    reference: 'main',
    type: sdk.CubesCreateVcsDeploymentType.Branch,
    activate: true // optional
});
```

## sites-delete-deployment

Delete deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesDeleteDeployment({
    siteId: '',
    deploymentId: ''
});
```

## sites-get-deployment

Get deployment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesGetDeployment({
    siteId: '',
    deploymentId: ''
});
```

## sites-get-deployment-download

Get deployment download

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesGetDeploymentDownload({
    siteId: '',
    deploymentId: '',
    type: sdk.AppsGetDeploymentDownloadType.Source // optional
});
```

## sites-update-deployment-status

Update deployment status

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesUpdateDeploymentStatus({
    siteId: '',
    deploymentId: ''
});
```

## sites-list-logs

List logs

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesListLogs({
    siteId: '',
    queries: [], // optional
    total: true // optional
});
```

## sites-delete-log

Delete log

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesDeleteLog({
    siteId: '',
    logId: ''
});
```

## sites-get-log

Get log

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesGetLog({
    siteId: '',
    logId: ''
});
```

## sites-list-variables

List variables

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesListVariables({
    siteId: ''
});
```

## sites-create-variable

Create variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesCreateVariable({
    siteId: '',
    key: '',
    value: '',
    secret: true // optional
});
```

## sites-delete-variable

Delete variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesDeleteVariable({
    siteId: '',
    variableId: ''
});
```

## sites-get-variable

Get variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesGetVariable({
    siteId: '',
    variableId: ''
});
```

## sites-update-variable

Update variable

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const sites = new sdk.Sites(client);

const result = await sites.sitesUpdateVariable({
    siteId: '',
    variableId: '',
    key: '',
    secret: true, // optional
    value: '' // optional
});
```
