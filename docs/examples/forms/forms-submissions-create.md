```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const forms = new sdk.Forms(client);

const result = await forms.formsSubmissionsCreate({
    data: {
        "company": "Example GmbH",
        "email": "buyer@example.com",
        "message": "Please quote 200 units of ACME-4711-BLK, delivered to Hamburg."
    },
    formId: '',
    formSlug: 'contact', // optional
    metadata: {}, // optional
    source: '/contact', // optional
    status: sdk.FormSubmissionStatus.New // optional
});
```
