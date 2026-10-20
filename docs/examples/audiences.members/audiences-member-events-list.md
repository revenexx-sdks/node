```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const audiencesMembers = new sdk.AudiencesMembers(client);

const result = await audiencesMembers.audiencesMemberEventsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    audienceId: '', // optional
    contactId: '', // optional
    kind: '', // optional
    source: '', // optional
    reason: '' // optional
});
```
