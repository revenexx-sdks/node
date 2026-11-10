# products.assets

## products-assets-list

List assets

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.ProductsListTrashed.Only, // optional
    id: '', // optional
    assetFamilyId: '', // optional
    code: 'acme-4711-blk_packshot_1', // optional
    source: sdk.DocumentsDocumentsListSource.Storage, // optional
    storageAssetId: 'ast_01J8ZQ0000000000000000', // optional
    deliveryPath: 'packshots/acme-4711-blk_1.jpg', // optional
    externalUrl: 'https://cdn.example.com/packshots/acme-4711-blk_1.jpg', // optional
    fileName: 'acme-4711-blk_1.jpg', // optional
    fileFormat: 'JPG', // optional
    fileSize: 1, // optional
    fileSizeLabel: '2,2 MB', // optional
    rightsHolder: 'Studio Weiss, Stuttgart', // optional
    license: sdk.License.Own, // optional
    usageRights: 'Online-Shop und Print-Katalog, nur DACH, keine Social-Media-Werbung.', // optional
    licenseValidFrom: '2026-01-01', // optional
    licenseValidUntil: '2026-01-01', // optional
    copyrightNotice: '© 2026 Studio Weiss', // optional
    rightsOrigin: 'Hersteller-Medienportal, Lizenzvertrag 2026-014', // optional
    attributeValues: '{}', // optional
    externalId: 'DAM-88231', // optional
    externalRefs: '{}', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    sourceData: '{}', // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'merchant@example.com', // optional
    deletedById: '283746592837465012', // optional
    trashBatch: '', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: ''S1230020C1TI25' still has stock at 2 location(s)' // optional
});
```

## products-assets-create

Create asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsCreate({
    assetFamilyId: '',
    code: 'acme-4711-blk_packshot_1',
    attributeValues: {
        "common": {
            "shot_type": "cutout"
        },
        "locale_specific": {
            "de": {
                "alt_text": "Akku-Bohrschrauber, freigestellt"
            }
        }
    }, // optional
    copyrightNotice: '© 2026 Studio Weiss', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'merchant@example.com', // optional
    deletedById: '283746592837465012', // optional
    deliveryPath: 'packshots/acme-4711-blk_1.jpg', // optional
    externalId: 'DAM-88231', // optional
    externalRefs: {
        "entitys": "4711",
        "gtin": "4012345000009"
    }, // optional
    externalUrl: 'https://cdn.example.com/packshots/acme-4711-blk_1.jpg', // optional
    fileFormat: 'JPG', // optional
    fileName: 'acme-4711-blk_1.jpg', // optional
    fileSize: 2306867, // optional
    license: sdk.AssetsLicense.Licensed, // optional
    licenseValidFrom: '2026-01-01', // optional
    licenseValidUntil: '2028-12-31', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: ''S1230020C1TI25' still has stock at 2 location(s)', // optional
    rightsHolder: 'Studio Weiss, Stuttgart', // optional
    rightsOrigin: 'Hersteller-Medienportal, Lizenzvertrag 2026-014', // optional
    source: sdk.AssetsSource.Storage, // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "BMECAT_GROUP": "EL-4711"
        },
        "system": "pim"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    storageAssetId: 'ast_01J8ZQ0000000000000000', // optional
    trashBatch: '', // optional
    usageRights: 'Online-Shop und Print-Katalog, nur DACH, keine Social-Media-Werbung.' // optional
});
```

## products-assets-empty-trash

Empty the trash of assets

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsEmptyTrash();
```

## products-assets-delete

Move asset to the trash, or delete it for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsDelete({
    id: ''
});
```

## products-assets-get

Get asset

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsGet({
    id: ''
});
```

## products-assets-update

Update asset

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
            "shot_type": "cutout"
        },
        "locale_specific": {
            "de": {
                "alt_text": "Akku-Bohrschrauber, freigestellt"
            }
        }
    }, // optional
    code: 'acme-4711-blk_packshot_1', // optional
    copyrightNotice: '© 2026 Studio Weiss', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'merchant@example.com', // optional
    deletedById: '283746592837465012', // optional
    deliveryPath: 'packshots/acme-4711-blk_1.jpg', // optional
    externalId: 'DAM-88231', // optional
    externalRefs: {
        "entitys": "4711",
        "gtin": "4012345000009"
    }, // optional
    externalUrl: 'https://cdn.example.com/packshots/acme-4711-blk_1.jpg', // optional
    fileFormat: 'JPG', // optional
    fileName: 'acme-4711-blk_1.jpg', // optional
    fileSize: 2306867, // optional
    license: sdk.AssetsLicense.Licensed, // optional
    licenseValidFrom: '2026-01-01', // optional
    licenseValidUntil: '2028-12-31', // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: ''S1230020C1TI25' still has stock at 2 location(s)', // optional
    rightsHolder: 'Studio Weiss, Stuttgart', // optional
    rightsOrigin: 'Hersteller-Medienportal, Lizenzvertrag 2026-014', // optional
    source: sdk.AssetsSource.Storage, // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "BMECAT_GROUP": "EL-4711"
        },
        "system": "pim"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    storageAssetId: 'ast_01J8ZQ0000000000000000', // optional
    trashBatch: '', // optional
    usageRights: 'Online-Shop und Print-Katalog, nur DACH, keine Social-Media-Werbung.' // optional
});
```

## products-assets-restore

Restore asset from the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsAssets = new sdk.ProductsAssets(client);

const result = await productsAssets.productsAssetsRestore({
    id: ''
});
```
