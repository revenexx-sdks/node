```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsList({
    id: '', // optional
    formId: '', // optional
    formSlug: 'contact', // optional
    source: '/contact', // optional
    status: sdk.FormSubmissionStatus.New, // optional
    createdAt: '2026-01-31T09:15:00Z', // optional
    updatedAt: '2026-01-31T09:15:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```
