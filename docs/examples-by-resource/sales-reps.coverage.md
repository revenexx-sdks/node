# sales-reps.coverage

## sales-reps-assignment-roles-list

List the roles this merchant keeps for coverage

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentRolesList({
    id: '', // optional
    code: 'field_sales', // optional
    title: 'Field sales', // optional
    description: 'Visits the customer. The rep who travels to the account.', // optional
    isDefault: true, // optional
    active: true, // optional
    tone: sdk.Tone.Neutral, // optional
    position: 1, // optional
    isSystem: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## sales-reps-assignment-roles-create

Add one role

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentRolesCreate({
    code: 'field_sales',
    title: 'Field sales',
    active: true, // optional
    description: 'Visits the customer. The rep who travels to the account.', // optional
    descriptions: {
        "de": "Besucht den Kunden.",
        "en": "Visits the customer."
    }, // optional
    isDefault: true, // optional
    isSystem: true, // optional
    labels: {
        "de": "Au\u00dfendienst",
        "en": "Field sales"
    }, // optional
    position: 1, // optional
    tone: sdk.Tone.Neutral // optional
});
```

## sales-reps-assignment-roles-defaults

Seed the roles this app ships

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentRolesDefaults({
    data: {}
});
```

## sales-reps-assignment-roles-delete

Remove one role

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentRolesDelete({
    id: ''
});
```

## sales-reps-assignment-roles-get

Read one role

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentRolesGet({
    id: ''
});
```

## sales-reps-assignment-roles-update

Rename, re-tone or reorder one role

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentRolesUpdate({
    id: '',
    active: true, // optional
    code: 'field_sales', // optional
    description: 'Visits the customer. The rep who travels to the account.', // optional
    descriptions: {
        "de": "Besucht den Kunden.",
        "en": "Visits the customer."
    }, // optional
    isDefault: true, // optional
    isSystem: true, // optional
    labels: {
        "de": "Au\u00dfendienst",
        "en": "Field sales"
    }, // optional
    position: 1, // optional
    title: 'Field sales', // optional
    tone: sdk.Tone.Neutral // optional
});
```

## sales-reps-assignments-list

List which rep carries which customer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentsList({
    id: '', // optional
    repCode: 'VK-04711', // optional
    organizationId: '', // optional
    role: 'field_sales', // optional
    isPrimary: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## sales-reps-assignments-create

Give one customer to one rep

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentsCreate({
    organizationId: '',
    repCode: 'VK-04711',
    role: 'field_sales' // optional
});
```

## sales-reps-assignments-delete

Take one customer off one rep

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentsDelete({
    id: ''
});
```

## sales-reps-assignments-get

Read one assignment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentsGet({
    id: ''
});
```

## sales-reps-assignments-update

Correct what a rep does for one customer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentsUpdate({
    id: '',
    role: 'field_sales' // optional
});
```

## sales-reps-assignments-make-primary

Make this rep the responsible one for their customer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsAssignmentsMakePrimary({
    id: '',
    data: {}
});
```

## sales-reps-vocabularies-list

List the value sets this app owns

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsVocabulariesList();
```

## sales-reps-vocabularies-get

Read one value set in full

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const salesRepsCoverage = new sdk.SalesRepsCoverage(client);

const result = await salesRepsCoverage.salesRepsVocabulariesGet({
    name: sdk.SalesRepsVocabulariesGetName.Assignmentroles
});
```
