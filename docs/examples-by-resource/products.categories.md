# products.categories

## products-categories-list

List categories

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    trashed: sdk.ProductsListTrashed.Only, // optional
    id: '', // optional
    code: 'cordless_drills', // optional
    parentId: '', // optional
    path: 'tools/power_tools/cordless_drills', // optional
    position: 1, // optional
    labels: '{}', // optional
    values: '{}', // optional
    rules: '{}', // optional
    ruleMatch: sdk.RuleMatch.All, // optional
    rulesComputedAt: '2026-01-01T12:00:00Z', // optional
    pathLabel: 'Werkzeug › Elektrowerkzeug › Akku-Bohrschrauber', // optional
    membersDirect: 1, // optional
    membersTotal: 1, // optional
    countsComputedAt: '2026-01-01T12:00:00Z', // optional
    active: true, // optional
    externalId: 'EG000024', // optional
    externalRefs: '{}', // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    sourceData: '{}', // optional
    metadata: '{}', // optional
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

## products-categories-create

Create category

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesCreate({
    code: 'cordless_drills',
    active: true, // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'merchant@example.com', // optional
    deletedById: '283746592837465012', // optional
    externalId: 'EG000024', // optional
    externalRefs: {
        "entitys": "4711",
        "gtin": "4012345000009"
    }, // optional
    labels: {
        "de": "Akku-Bohrschrauber",
        "en": "Cordless drills"
    }, // optional
    metadata: {
        "do_not_export": true,
        "sync_owner": "erp-nightly"
    }, // optional
    parentId: '', // optional
    path: 'tools/power_tools/cordless_drills', // optional
    position: 1, // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: ''S1230020C1TI25' still has stock at 2 location(s)', // optional
    ruleMatch: sdk.CategoriesRuleMatch.All, // optional
    rules: {
        "conditions": [
            {
                "field": "attribute:brand",
                "operator": "in",
                "value": [
                    "acme",
                    "globex"
                ]
            },
            {
                "field": "enabled",
                "operator": "eq",
                "value": true
            }
        ]
    }, // optional
    rulesComputedAt: '2026-01-01T12:00:00Z', // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "BMECAT_GROUP": "EL-4711"
        },
        "system": "pim"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    trashBatch: '', // optional
    values: {
        "image": "categories\/cordless-drills.jpg",
        "seo_title": "Cordless drills"
    } // optional
});
```

## products-categories-rules-recompute-all

Recompute every category rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesRulesRecomputeAll({
    data: {}
});
```

## products-categories-empty-trash

Empty the trash of categories

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesEmptyTrash();
```

## products-categories-rules-preview

Preview a category rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesRulesPreview({
    categoryId: '',
    conditions: [],
    ruleMatch: sdk.CategoryRuleMatch.All // optional
});
```

## products-categories-rules-recompute

Recompute a category's rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesRulesRecompute({
    categoryId: '',
    cursor: '' // optional
});
```

## products-categories-delete

Move category to the trash, or delete it for good

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesDelete({
    id: ''
});
```

## products-categories-get

Get category

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesGet({
    id: ''
});
```

## products-categories-update

Update category

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesUpdate({
    id: '',
    active: true, // optional
    code: 'cordless_drills', // optional
    deletedAt: '2026-01-01T12:00:00Z', // optional
    deletedBy: 'merchant@example.com', // optional
    deletedById: '283746592837465012', // optional
    externalId: 'EG000024', // optional
    externalRefs: {
        "entitys": "4711",
        "gtin": "4012345000009"
    }, // optional
    labels: {
        "de": "Akku-Bohrschrauber",
        "en": "Cordless drills"
    }, // optional
    metadata: {
        "do_not_export": true,
        "sync_owner": "erp-nightly"
    }, // optional
    parentId: '', // optional
    path: 'tools/power_tools/cordless_drills', // optional
    position: 1, // optional
    purgeAt: '2026-01-01T12:00:00Z', // optional
    purgeBlockedReason: ''S1230020C1TI25' still has stock at 2 location(s)', // optional
    ruleMatch: sdk.CategoriesRuleMatch.All, // optional
    rules: {
        "conditions": [
            {
                "field": "attribute:brand",
                "operator": "in",
                "value": [
                    "acme",
                    "globex"
                ]
            },
            {
                "field": "enabled",
                "operator": "eq",
                "value": true
            }
        ]
    }, // optional
    rulesComputedAt: '2026-01-01T12:00:00Z', // optional
    sourceData: {
        "etag": "W\/\"JzQ0O0c2\"",
        "raw": {
            "BMECAT_GROUP": "EL-4711"
        },
        "system": "pim"
    }, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    trashBatch: '', // optional
    values: {
        "image": "categories\/cordless-drills.jpg",
        "seo_title": "Cordless drills"
    } // optional
});
```

## products-categories-restore

Restore category from the trash

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesRestore({
    id: ''
});
```

## products-product-categories-list

List product category memberships

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsProductCategoriesList({
    limit: 1, // optional
    offset: 1, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    productId: '', // optional
    categoryId: '', // optional
    position: 1, // optional
    source: sdk.ProductsProductCategoriesListSource.Manual, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z' // optional
});
```

## products-product-categories-create

Create product category membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsProductCategoriesCreate({
    categoryId: '',
    productId: '',
    position: 1, // optional
    source: sdk.ProductCategoriesSource.Manual // optional
});
```

## products-product-categories-delete

Delete product category membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsProductCategoriesDelete({
    id: ''
});
```

## products-product-categories-get

Get product category membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsProductCategoriesGet({
    id: ''
});
```

## products-product-categories-update

Update product category membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsProductCategoriesUpdate({
    id: '',
    categoryId: '', // optional
    position: 1, // optional
    productId: '', // optional
    source: sdk.ProductCategoriesSource.Manual // optional
});
```

## products-categories-assign

File a product into a category

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const productsCategories = new sdk.ProductsCategories(client);

const result = await productsCategories.productsCategoriesAssign({
    id: '',
    categoryId: '',
    position: 1 // optional
});
```
