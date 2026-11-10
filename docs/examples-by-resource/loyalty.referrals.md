# loyalty.referrals

## loyalty-referrals-codes-list

List referral codes

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsCodesList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    membershipId: '', // optional
    contactId: '', // optional
    code: '', // optional
    uses: '', // optional
    active: '' // optional
});
```

## loyalty-referrals-codes-get

Read one referral code

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsCodesGet({
    id: ''
});
```

## loyalty-referrals-codes-deactivate

Retire a referral code

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsCodesDeactivate({
    id: '',
    data: {}
});
```

## loyalty-referrals-list

List referrals

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsList({
    limit: 50, // optional
    offset: 0, // optional
    order: 'created_at.desc', // optional
    id: '', // optional
    referralCodeId: '', // optional
    referrerMembershipId: '', // optional
    referrerContactId: '', // optional
    refereeContactId: '', // optional
    state: '', // optional
    orderId: '', // optional
    reason: '', // optional
    refereeVoucherCode: '', // optional
    referrerVoucherCode: '' // optional
});
```

## loyalty-referrals-claim

Claim a referral code for a new customer

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsClaim({
    code: '',
    contactId: ''
});
```

## loyalty-referrals-get

Read one referral

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsGet({
    id: ''
});
```

## loyalty-referrals-reject

Reject a referral with a reason

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsReject({
    id: '',
    reason: ''
});
```

## loyalty-referrals-reward

Issue the referrer reward of a qualified referral again

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const loyaltyReferrals = new sdk.LoyaltyReferrals(client);

const result = await loyaltyReferrals.loyaltyReferralsReward({
    id: '',
    data: {}
});
```
