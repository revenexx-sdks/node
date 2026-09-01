```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsUpdate({
    id: '',
    assetFamilyId: '', // optional
    attributeValues: {
        "common": {
            "copyright": "\u00a9 Acme Tools",
            "expires_on": "2028-12-31"
        },
        "locale_specific": {
            "de_DE": {
                "alt_text": "Akku-Bohrschrauber, freigestellt"
            }
        }
    }, // optional
    code: 'acme-4711-blk_packshot_1', // optional
    deliveryPath: 'packshots/acme-4711-blk_1.jpg', // optional
    externalUrl: 'https://cdn.example.com/packshots/acme-4711-blk_1.jpg', // optional
    source: sdk.AssetsSource.Storage, // optional
    storageAssetId: 'ast_01J8ZQ0000000000000000' // optional
});
```
