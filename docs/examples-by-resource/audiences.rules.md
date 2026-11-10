# audiences.rules

## audiences-rules-list

List audience rules

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesRules = new sdk.AudiencesRules(client);

const result = await audiencesRules.audiencesRulesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    audienceId: '', // optional
    parentId: '', // optional
    kind: '', // optional
    matchMode: '', // optional
    negate: '', // optional
    subject: '', // optional
    field: '', // optional
    operator: '', // optional
    windowDays: '', // optional
    channel: '', // optional
    position: '' // optional
});
```

## audiences-rules-create

Add a rule or a group to an audience

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesRules = new sdk.AudiencesRules(client);

const result = await audiencesRules.audiencesRulesCreate({
    audienceId: '',
    channel: sdk.Channel.Email, // optional
    field: '', // optional
    kind: sdk.AudiencesRulesCreateKind.Group, // optional
    matchMode: sdk.MatchMode.All, // optional
    negate: true, // optional
    operator: '', // optional
    parentId: '', // optional
    position: 1, // optional
    subject: '', // optional
    value: null, // optional
    valueTo: null, // optional
    windowDays: 1 // optional
});
```

## audiences-rules-delete

Remove a rule (and, for a group, what it holds)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesRules = new sdk.AudiencesRules(client);

const result = await audiencesRules.audiencesRulesDelete({
    id: ''
});
```

## audiences-rules-get

Read one rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesRules = new sdk.AudiencesRules(client);

const result = await audiencesRules.audiencesRulesGet({
    id: ''
});
```

## audiences-rules-update

Correct a rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesRules = new sdk.AudiencesRules(client);

const result = await audiencesRules.audiencesRulesUpdate({
    id: '',
    audienceId: '', // optional
    channel: sdk.Channel.Email, // optional
    field: '', // optional
    kind: sdk.AudiencesRulesCreateKind.Group, // optional
    matchMode: sdk.MatchMode.All, // optional
    negate: true, // optional
    operator: '', // optional
    parentId: '', // optional
    position: 1, // optional
    subject: '', // optional
    value: null, // optional
    valueTo: null, // optional
    windowDays: 1 // optional
});
```
