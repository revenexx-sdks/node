```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const orderlists = new sdk.Orderlists(client);

const result = await orderlists.orderlistsItemsUpdate({
    listId: '',
    id: '',
    categorySlug: '', // optional
    costCenterId: '', // optional
    customSku: '', // optional
    image: '', // optional
    metadata: {}, // optional
    name: '', // optional
    position: null, // optional
    positionTexts: [], // optional
    price: null, // optional
    productId: '', // optional
    quantity: null, // optional
    sku: '', // optional
    subcategorySlug: '', // optional
    taxRate: null, // optional
    unit: '' // optional
});
```
