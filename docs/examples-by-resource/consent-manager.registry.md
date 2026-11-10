# consent-manager.registry

## consent-manager-catalog-list

List the shipped vendor catalogue

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCatalogList({
    category: 'analytics' // optional
});
```

## consent-manager-catalog-adopt

Copy a catalogue vendor into this tenant

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCatalogAdopt({
    key: 'etracker',
    purposes: ["statistics"], // optional
    refresh: true // optional
});
```

## consent-manager-cookies-list

List cookies and storage entries

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCookiesList({
    id: '', // optional
    vendorId: '', // optional
    name: '_ga', // optional
    kind: sdk.ConsentManagerCookiesListKind.Cookie, // optional
    host: 'first-party', // optional
    position: 1, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## consent-manager-cookies-create

Declare a cookie under a vendor

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCookiesCreate({
    name: '_ga',
    vendorId: '',
    description: {}, // optional
    duration: {
        "de": "2 Jahre",
        "en": "2 years"
    }, // optional
    host: 'first-party', // optional
    kind: sdk.ConsentManagerCookiesListKind.Cookie, // optional
    position: 1 // optional
});
```

## consent-manager-cookies-delete

Remove a cookie

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCookiesDelete({
    id: ''
});
```

## consent-manager-cookies-get

Read one cookie

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCookiesGet({
    id: ''
});
```

## consent-manager-cookies-update

Edit a cookie

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerCookiesUpdate({
    id: '',
    description: {}, // optional
    duration: {
        "de": "2 Jahre",
        "en": "2 years"
    }, // optional
    host: 'first-party', // optional
    kind: sdk.ConsentManagerCookiesListKind.Cookie, // optional
    name: '_ga', // optional
    position: 1, // optional
    vendorId: '' // optional
});
```

## consent-manager-defaults-run

Seed the five purposes and the default banner

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerDefaultsRun({
    data: {}
});
```

## consent-manager-purposes-list

List the purposes and their legal basis

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerPurposesList({
    id: '', // optional
    code: 'statistics', // optional
    legalBasis: sdk.LegalBasis.Consent, // optional
    position: 1, // optional
    isActive: true, // optional
    isSystem: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## consent-manager-purposes-create

Add a purpose

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerPurposesCreate({
    code: 'statistics',
    legalBasis: sdk.LegalBasis.Consent,
    name: {
        "de": "Statistik",
        "en": "Statistics"
    },
    description: {}, // optional
    googleSignals: [sdk.GoogleSignals.AnalyticsStorage], // optional
    isActive: true, // optional
    position: 1 // optional
});
```

## consent-manager-purposes-delete

Remove a purpose no vendor serves

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerPurposesDelete({
    id: ''
});
```

## consent-manager-purposes-get

Read one purpose

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerPurposesGet({
    id: ''
});
```

## consent-manager-purposes-update

Edit a purpose; its code is fixed

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerPurposesUpdate({
    id: '',
    code: 'statistics', // optional
    description: {}, // optional
    googleSignals: [sdk.GoogleSignals.AnalyticsStorage], // optional
    isActive: true, // optional
    legalBasis: sdk.LegalBasis.Consent, // optional
    name: {
        "de": "Statistik",
        "en": "Statistics"
    }, // optional
    position: 1 // optional
});
```

## consent-manager-vendors-list

List the vendors, flagged when the catalogue is newer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVendorsList({
    id: '', // optional
    code: 'google-analytics', // optional
    name: 'Google Analytics 4', // optional
    category: 'analytics', // optional
    company: 'Google Ireland Limited', // optional
    address: 'Gordon House, Barrow Street, Dublin 4, Ireland', // optional
    country: 'IE', // optional
    privacyPolicyUrl: 'https://policies.google.com/privacy', // optional
    dpaUrl: 'https://business.safety.google/adsprocessorterms/', // optional
    thirdCountryTransfer: true, // optional
    transferBasis: 'EU-US Data Privacy Framework; standard contractual clauses', // optional
    registryKey: 'googleAnalytics', // optional
    logo: 'data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciLz4=', // optional
    legalBasisOverride: sdk.LegalBasisOverride.Consent, // optional
    catalogKey: 'google-analytics', // optional
    catalogVersion: '2026.10.1', // optional
    position: 1, // optional
    isActive: true, // optional
    createdAt: '2026-01-01T12:00:00Z', // optional
    updatedAt: '2026-01-01T12:00:00Z', // optional
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc' // optional
});
```

## consent-manager-vendors-create

Declare a vendor

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVendorsCreate({
    code: 'google-analytics',
    name: 'Google Analytics 4',
    address: 'Gordon House, Barrow Street, Dublin 4, Ireland', // optional
    category: 'analytics', // optional
    chains: ["google-analytics"], // optional
    company: 'Google Ireland Limited', // optional
    country: 'IE', // optional
    description: {}, // optional
    dpaUrl: 'https://business.safety.google/adsprocessorterms/', // optional
    hosts: ["www.google-analytics.com"], // optional
    isActive: true, // optional
    legalBasisOverride: sdk.LegalBasisOverride.LegitimateInterest, // optional
    logo: 'data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciLz4=', // optional
    position: 1, // optional
    privacyPolicyUrl: 'https://policies.google.com/privacy', // optional
    purposes: ["statistics"], // optional
    registryKey: 'googleAnalytics', // optional
    retentionNote: {}, // optional
    thirdCountryTransfer: true, // optional
    transferBasis: 'EU-US Data Privacy Framework; standard contractual clauses' // optional
});
```

## consent-manager-vendors-delete

Remove a vendor with its cookies and purpose links

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVendorsDelete({
    id: ''
});
```

## consent-manager-vendors-get

Read one vendor with its purposes and cookies

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVendorsGet({
    id: ''
});
```

## consent-manager-vendors-update

Edit a vendor; its code is fixed

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVendorsUpdate({
    id: '',
    address: 'Gordon House, Barrow Street, Dublin 4, Ireland', // optional
    category: 'analytics', // optional
    chains: ["google-analytics"], // optional
    code: 'google-analytics', // optional
    company: 'Google Ireland Limited', // optional
    country: 'IE', // optional
    description: {}, // optional
    dpaUrl: 'https://business.safety.google/adsprocessorterms/', // optional
    hosts: ["www.google-analytics.com"], // optional
    isActive: true, // optional
    legalBasisOverride: sdk.LegalBasisOverride.LegitimateInterest, // optional
    logo: 'data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciLz4=', // optional
    name: 'Google Analytics 4', // optional
    position: 1, // optional
    privacyPolicyUrl: 'https://policies.google.com/privacy', // optional
    purposes: ["statistics"], // optional
    registryKey: 'googleAnalytics', // optional
    retentionNote: {}, // optional
    thirdCountryTransfer: true, // optional
    transferBasis: 'EU-US Data Privacy Framework; standard contractual clauses' // optional
});
```

## consent-manager-vocabularies-list

List the value sets this app owns

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVocabulariesList();
```

## consent-manager-vocabularies-get

Read one value set in full

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const consentManagerRegistry = new sdk.ConsentManagerRegistry(client);

const result = await consentManagerRegistry.consentManagerVocabulariesGet({
    name: sdk.ConsentManagerVocabulariesGetName.Legalbases
});
```
