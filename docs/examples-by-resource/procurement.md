# procurement

## procurement-approval-rules-list

List ApprovalRule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementApprovalRulesList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-approval-rules-create

Create a approval rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementApprovalRulesCreate({
    condition: sdk.ConditionEnum.Always,
    effect: sdk.Effect.PendingOrder,
    name: '',
    active: true, // optional
    approverContactId: '', // optional
    approverRole: '', // optional
    approverType: sdk.ApproverType.Contact, // optional
    conditionParameters: {}, // optional
    costCenterId: '', // optional
    effectParameters: {}, // optional
    metadata: {}, // optional
    sequence: 1, // optional
    showCondition: true // optional
});
```

## procurement-approval-rules-delete

Delete a approval rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementApprovalRulesDelete({
    id: ''
});
```

## procurement-approval-rules-get

Read one approval rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementApprovalRulesGet({
    id: ''
});
```

## procurement-approval-rules-update

Update a approval rule

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementApprovalRulesUpdate({
    id: '',
    active: true, // optional
    approverContactId: '', // optional
    approverRole: '', // optional
    approverType: sdk.ApproverType.Contact, // optional
    condition: sdk.ConditionEnum.Always, // optional
    conditionParameters: {}, // optional
    costCenterId: '', // optional
    effect: sdk.Effect.PendingOrder, // optional
    effectParameters: {}, // optional
    metadata: {}, // optional
    name: '', // optional
    sequence: 1, // optional
    showCondition: true // optional
});
```

## procurement-budget-releases-list

List BudgetRelease

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementBudgetReleasesList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-budget-releases-get

Read one budget release

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementBudgetReleasesGet({
    id: ''
});
```

## procurement-budget-releases-retry

Retry giving back a cancelled order's budget — from pending or refused (409 otherwise)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementBudgetReleasesRetry({
    id: ''
});
```

## procurement-budget-releases-settle

Settle a refused budget release by hand, with a note — the budget then stays booked for that order (administrator; 409 unless refused)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementBudgetReleasesSettle({
    id: '',
    note: ''
});
```

## procurement-direct-orders-list

List DirectOrder

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementDirectOrdersList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-direct-orders-get

Read one direct order

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementDirectOrdersGet({
    id: ''
});
```

## procurement-direct-orders-commit

Retry a direct order's budget commit from the movement recorded at submit — from commit_pending or commit_refused (409 otherwise)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementDirectOrdersCommit({
    id: ''
});
```

## procurement-direct-orders-settle

Settle a refused budget commit by hand, with a note — the budget is then never booked for that order (administrator; 409 unless commit_refused)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementDirectOrdersSettle({
    id: '',
    note: ''
});
```

## procurement-purchase-request-items-open

List the lines of open purchase requests that name a product

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestItemsOpen({
    productId: '',
    status: 'pending,approved', // optional
    limit: 1, // optional
    offset: 1 // optional
});
```

## procurement-pending-approvals-list

List PendingApproval

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPendingApprovalsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-pending-approvals-get

Read one pending approval

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPendingApprovalsGet({
    id: ''
});
```

## procurement-pending-approvals-approve

Approve one pending approval layer; unlocks the next, or approves the PR when all chains clear

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPendingApprovalsApprove({
    id: '',
    reason: '' // optional
});
```

## procurement-pending-approvals-decline

Decline one pending approval — terminates the whole purchase request and withdraws its budget

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPendingApprovalsDecline({
    id: '',
    reason: '' // optional
});
```

## procurement-purchase-request-events-list

List PurchaseRequestEvent

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestEventsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-purchase-request-events-get

Read one purchase request outcome event

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestEventsGet({
    id: ''
});
```

## procurement-purchase-request-items-list

List PurchaseRequestItem

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestItemsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-purchase-request-items-create

Create a purchase request item

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestItemsCreate({
    name: '',
    purchaseRequestId: '',
    quantity: 9.99,
    configuration: {}, // optional
    costCenter: '', // optional
    lineTotal: 9.99, // optional
    metadata: {}, // optional
    position: 1, // optional
    positionText: '', // optional
    product: {}, // optional
    productId: '', // optional
    sku: '', // optional
    taxAmount: 9.99, // optional
    taxRate: 9.99, // optional
    type: sdk.ProcurementPurchaseRequestItemsCreateType.Product, // optional
    unit: '', // optional
    unitPrice: 9.99, // optional
    userData: {} // optional
});
```

## procurement-purchase-request-items-delete

Delete a purchase request item

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestItemsDelete({
    id: ''
});
```

## procurement-purchase-request-items-get

Read one purchase request item

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestItemsGet({
    id: ''
});
```

## procurement-purchase-request-items-update

Update a purchase request item

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

## procurement-purchase-requests-list

List PurchaseRequest

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestsList({
    limit: 1, // optional
    offset: 1, // optional
    order: '' // optional
});
```

## procurement-purchase-requests-get

Read one purchase request

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestsGet({
    id: ''
});
```

## procurement-purchase-requests-update

Update a purchase request

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestsUpdate({
    id: '',
    billingAddress: {}, // optional
    buyer: {}, // optional
    cartId: '', // optional
    channelId: '', // optional
    contactId: '', // optional
    currency: '', // optional
    customerOrderNumber: '', // optional
    externalRef: '', // optional
    grandTotal: 9.99, // optional
    itemCount: 1, // optional
    metadata: {}, // optional
    number: '', // optional
    organizationId: '', // optional
    payment: {}, // optional
    senderCountry: 'DE', // optional
    shipping: {}, // optional
    shippingAddress: {}, // optional
    shippingTotal: 9.99, // optional
    subtotal: 9.99, // optional
    taxTotal: 9.99, // optional
    userData: {} // optional
});
```

## procurement-purchase-requests-approve

Super-approve — clear all outstanding approval layers at once and drive the PR to ordered

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestsApprove({
    id: '',
    reason: '' // optional
});
```

## procurement-purchase-requests-cancel

Cancel a pending purchase request (admin) and withdraw its budget

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestsCancel({
    id: '',
    reason: '' // optional
});
```

## procurement-purchase-requests-order

Retry-safe approved→ordered: idempotently place the Order and confirm the budget

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementPurchaseRequestsOrder({
    id: ''
});
```

## procurement-reconcile

Reconciliation sweep — complete stuck approved→ordered promotions, release orphaned budget reservations, record any outcome whose write failed, finish direct orders whose budget commit is owed, and retry budget releases of cancelled orders

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementReconcile({
    limit: 1 // optional
});
```

## procurement-submit

Authoritative checkout submit — evaluate approval rules and create a direct Order, a Purchase Request, or block (409)

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementSubmit({
    cartId: '',
    items: [],
    billingAddress: {}, // optional
    buyer: {}, // optional
    channelId: '', // optional
    contactId: '', // optional
    currency: '', // optional
    customerOrderNumber: '', // optional
    externalRef: '', // optional
    metadata: {}, // optional
    organizationId: '', // optional
    payment: {}, // optional
    senderCountry: 'DE', // optional
    shipping: {}, // optional
    shippingAddress: {}, // optional
    userData: {} // optional
});
```

## procurement-submit-cart

Check out a stored cart by id — read it from carts and submit it as /procurement/submit does, then mark the cart ordered once an Order exists

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementSubmitCart({
    cartId: '',
    costCenterId: '', // optional
    customerOrderNumber: '' // optional
});
```

## procurement-vocabularies-list

List the enums this app publishes, by name and title, without their values

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementVocabulariesList();
```

## procurement-vocabularies-get

Read one vocabulary — every permitted value in constraint order, with its title and badge tone; 404 for a name that is not one

```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const procurement = new sdk.Procurement(client);

const result = await procurement.procurementVocabulariesGet({
    name: sdk.ProcurementVocabulariesGetName.Approvalstatuses
});
```
