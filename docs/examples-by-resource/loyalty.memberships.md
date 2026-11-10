# loyalty.memberships

## loyalty-memberships-list

List members

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    programId: '', // optional
    holder: '', // optional
    holderKey: '', // optional
    contactId: '', // optional
    organizationId: '', // optional
    tierId: '', // optional
    tierCode: '', // optional
    status: '', // optional
    pointsBalance: '', // optional
    pointsPeriod: '', // optional
    pointsLifetime: '', // optional
    market: '', // optional
    externalId: '' // optional
});
```

## loyalty-memberships-create

Enrol a contact or a company

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsCreate({
    programId: '',
    contactId: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    market: '', // optional
    metadata: null, // optional
    organizationId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.LoyaltyMembershipsCreateStatus.Active // optional
});
```

## loyalty-memberships-lookup

Read the tier, perks, balance and bonus agreement of a contact or company

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsLookup({
    contactId: '', // optional
    organizationId: '' // optional
});
```

## loyalty-memberships-delete

Delete a membership with no bookings

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsDelete({
    id: ''
});
```

## loyalty-memberships-get

Read one membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsGet({
    id: ''
});
```

## loyalty-memberships-update

Pause, resume or end a membership

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsUpdate({
    id: '',
    contactId: '', // optional
    externalId: '', // optional
    externalRefs: null, // optional
    market: '', // optional
    metadata: null, // optional
    organizationId: '', // optional
    programId: '', // optional
    sourceData: null, // optional
    sourceSyncedAt: '2026-01-01T12:00:00Z', // optional
    status: sdk.LoyaltyMembershipsCreateStatus.Active // optional
});
```

## loyalty-memberships-adjust

Correct a member balance by hand

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsAdjust({
    id: '',
    points: 1,
    reason: '',
    key: '' // optional
});
```

## loyalty-memberships-progress

Read the way of a member to the next tier

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsProgress({
    id: ''
});
```

## loyalty-memberships-referral-code

Read or make the referral code of a member

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyMemberships = new sdk.LoyaltyMemberships(client);

const result = await loyaltyMemberships.loyaltyMembershipsReferralCode({
    id: '',
    contactId: '' // optional
});
```
