```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsMailings = new sdk.MailingsMailings(client);

const result = await mailingsMailings.mailingsMailingsPreview({
    id: '',
    contactId: '', // optional
    device: sdk.Device.Desktop, // optional
    email: '', // optional
    firstName: '', // optional
    lastName: '', // optional
    locale: '', // optional
    market: '' // optional
});
```
