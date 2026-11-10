# customers.segments

## customers-segment-members-list

Browse segment memberships

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentMembersList({
    id: '', // optional
    segmentId: '', // optional
    organizationId: '', // optional
    contactId: '', // optional
    source: sdk.Source.Manual, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```

## customers-segment-members-create

Put a company into a segment by hand

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentMembersCreate({
    organizationId: '',
    segmentId: '',
    createdAt: '2026-01-01T12:00:00Z', // optional
    source: sdk.SegmentMemberSource.Manual // optional
});
```

## customers-segment-members-delete

Take a company out of a segment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentMembersDelete({
    id: ''
});
```

## customers-segment-members-get

Read one membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentMembersGet({
    id: ''
});
```

## customers-segment-members-update

Update a membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentMembersUpdate({
    id: '',
    organizationId: '', // optional
    segmentId: '', // optional
    source: sdk.SegmentMemberSource.Manual // optional
});
```

## customers-segments-list

Browse the customer segments

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsList({
    id: '', // optional
    code: 'key_accounts', // optional
    position: 1, // optional
    active: true, // optional
    ruleMatch: sdk.RuleMatch.All, // optional
    memberType: sdk.MemberType.Organization, // optional
    rulesComputedAt: '2026-01-01T12:00:00Z', // optional
    externalId: 'PREISGRUPPE-03', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'vertrieb@example.com', // optional
    deletedById: '', // optional
    trashBatch: '', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: '', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    trashed: sdk.Trashed.Exclude, // optional
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc' // optional
});
```

## customers-segments-create

Create a segment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsCreate({
    active: true, // optional
    code: 'key_accounts', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    labels: {
        "de": "Gro\u00dfkunden",
        "en": "Key accounts"
    }, // optional
    position: 1, // optional
    ruleMatch: sdk.SegmentRuleMatch.All, // optional
    rules: {} // optional
});
```

## customers-segments-rules-recompute-all

Recompute every ruled segment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsRulesRecomputeAll({
    data: {}
});
```

## customers-segments-trash-empty

Empty the segment trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsTrashEmpty();
```

## customers-segments-delete

Delete a segment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsDelete({
    id: ''
});
```

## customers-segments-get

Read one segment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsGet({
    id: ''
});
```

## customers-segments-update

Update a segment

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsUpdate({
    id: '',
    active: true, // optional
    code: 'key_accounts', // optional
    labels: {
        "de": "Gro\u00dfkunden",
        "en": "Key accounts"
    }, // optional
    position: 1, // optional
    ruleMatch: sdk.SegmentRuleMatch.All, // optional
    rules: {} // optional
});
```

## customers-segments-restore

Restore a segment from the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsRestore({
    id: ''
});
```

## customers-segments-rules-preview

Preview a segment rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsRulesPreview({
    segmentId: '',
    conditions: [],
    ruleMatch: sdk.RuleMatch.All, // optional
    target: sdk.Target.Organizations // optional
});
```

## customers-segments-rules-recompute

Recompute one segment's rule memberships

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customersSegments = new sdk.CustomersSegments(client);

const result = await customersSegments.customersSegmentsRulesRecompute({
    segmentId: '',
    cursor: '' // optional
});
```
