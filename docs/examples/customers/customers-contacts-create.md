```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const customers = new sdk.Customers(client);

const result = await customers.customersContactsCreate({
    email: '',
    firstName: '', // optional
    isPrimary: null, // optional
    lastName: '', // optional
    locale: '', // optional
    organizationId: '', // optional
    phone: '', // optional
    role: sdk.ContactRole.Buyer, // optional
    status: sdk.ContactStatus.Invited // optional
});
```
