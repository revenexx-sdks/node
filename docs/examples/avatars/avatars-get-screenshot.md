```javascript
const sdk = require('node-revenexx-a-p-i-—-revenexx');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const avatars = new sdk.Avatars(client);

const result = await avatars.avatarsGetScreenshot({
    url: '',
    headers: {}, // optional
    viewportWidth: null, // optional
    viewportHeight: null, // optional
    scale: null, // optional
    theme: sdk.Theme.Light, // optional
    userAgent: '', // optional
    fullpage: null, // optional
    locale: '', // optional
    timezone: sdk.Timezone.AfricaAbidjan, // optional
    latitude: null, // optional
    longitude: null, // optional
    accuracy: null, // optional
    touch: null, // optional
    permissions: [sdk.Permissions.Geolocation], // optional
    sleep: null, // optional
    width: null, // optional
    height: null, // optional
    quality: null, // optional
    output: sdk.Output.Jpg // optional
});
```
