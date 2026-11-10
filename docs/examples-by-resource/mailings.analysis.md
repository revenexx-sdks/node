# mailings.analysis

## mailings-analysis-list-clicks

List clicked links of mailings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisListClicks({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    mailingId: '', // optional
    url: '' // optional
});
```

## mailings-analysis-get-click

Read one clicked link

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisGetClick({
    id: ''
});
```

## mailings-analysis-list-engagements

List recorded reactions to mailings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisListEngagements({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    mailingId: '', // optional
    kind: '', // optional
    email: '', // optional
    contactId: '', // optional
    messageId: '', // optional
    isMachine: '' // optional
});
```

## mailings-analysis-get-engagement

Read one recorded reaction

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisGetEngagement({
    id: ''
});
```

## mailings-analysis-clicks

Read the click map of a mailing

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisClicks({
    id: ''
});
```

## mailings-analysis-stats

Read what a mailing achieved

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisStats({
    id: ''
});
```

## mailings-analysis-timeline

Read the opens and clicks of a mailing per day

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisTimeline({
    id: ''
});
```

## mailings-analysis-list-stats

List the figures of mailings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisListStats({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    mailingId: '' // optional
});
```

## mailings-analysis-sweep

Bring the figures of the last 30 days up to date

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisSweep({
    data: {}
});
```

## mailings-analysis-get-stats

Read one figures row

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsAnalysis = new sdk.MailingsAnalysis(client);

const result = await mailingsAnalysis.mailingsAnalysisGetStats({
    id: ''
});
```
