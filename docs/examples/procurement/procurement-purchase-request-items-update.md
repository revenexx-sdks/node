```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestItemsUpdate({
    id: '',
    configuration: {}, // optional
    costCenter: '', // optional
    lineTotal: 9.99, // optional
    metadata: {}, // optional
    name: '', // optional
    position: 1, // optional
    positionText: '', // optional
    product: {}, // optional
    productId: '', // optional
    purchaseRequestId: '', // optional
    quantity: 9.99, // optional
    sku: '', // optional
    taxAmount: 9.99, // optional
    taxRate: 9.99, // optional
    type: sdk.ProcurementPurchaseRequestItemsCreateType.Product, // optional
    unit: '', // optional
    unitPrice: 9.99, // optional
    userData: {} // optional
});
```
