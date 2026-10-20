```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsRecipients = new sdk.MailingsRecipients(client);

const result = await mailingsRecipients.mailingsRecipientsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    mailingId: '', // optional
    contactId: '', // optional
    email: '', // optional
    outcome: '', // optional
    reason: '', // optional
    market: '', // optional
    messageId: '' // optional
});
```
