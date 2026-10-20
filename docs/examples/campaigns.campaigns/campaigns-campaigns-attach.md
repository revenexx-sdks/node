```javascript
const sdk = require('@revenexx/node');

const client = new sdk.Client()
    .setEndpoint('https://api.revenexx.com') // Your API Endpoint
    .setTenant('<TENANT_SLUG>') // Your tenant slug
    .setApiKeyAuth('<API_KEY>'); // A gateway-managed scoped API key (rvxk_…).

const campaignsCampaigns = new sdk.CampaignsCampaigns(client);

const result = await campaignsCampaigns.campaignsCampaignsAttach({
    id: '',
    adCampaignLinkId: '', // optional
    assetApp: sdk.AssetApp.Promotions, // optional
    assetEntity: '', // optional
    assetId: '', // optional
    formId: '', // optional
    journeyId: '', // optional
    label: '', // optional
    libraryItemId: '', // optional
    mailingId: '', // optional
    pageId: '', // optional
    promotionId: '' // optional
});
```
