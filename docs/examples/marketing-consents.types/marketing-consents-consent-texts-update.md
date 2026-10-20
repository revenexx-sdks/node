```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const marketingConsentsTypes = new sdk.MarketingConsentsTypes(client);

const result = await marketingConsentsTypes.marketingConsentsConsentTextsUpdate({
    id: '',
    wording: 'Ja, ich möchte den Newsletter mit Neuheiten und Aktionen erhalten. Abmeldung jederzeit über den Link in jeder Mail.'
});
```
