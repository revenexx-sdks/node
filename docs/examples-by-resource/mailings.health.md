# mailings.health

## mailings-health-read

Read the sending health of the last 30 days

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const mailingsHealth = new sdk.MailingsHealth(client);

const result = await mailingsHealth.mailingsHealthRead();
```
