>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# /causes/:id/permissions

**Authenication Required**

Retrieves and updates the permissions for a cause. These options are
used to determine the visibility of certain features on the administration
interface of the website. These options also disable features in the API.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "activated": true,
    "causeLeaderboard": false,
    "dashboardEnabled": true,
    "dashboardChart": true,
    "fundraisingEventsEnabled": false,
    "fundraisingEventsLeaderboard": false,
    "fundraisingEventsIncentives": false,
    "fundraisingEventsSchedule": false,
    "fundraisingEventsReporting": false,
    "fundraisingEventsReportingDonations": false,
    "fundraisingEventsReportingCampaigns": false,
    "fundraisingEventsReportingFundraisers": false,
    "fundraisingEventsGeneralEnabled": false,
    "fundraisingEventsGeneralDetails": false,
    "fundraisingEventsGeneralColors": false,
    "fundraisingEventsGeneralImages": false,
    "fundraisingEventsRegistrationEnabled": false,
    "fundraisingEventsVisibilityEnabled": false,
    "fundraisingEventsVisibilityDetails": false,
    "fundraisingEventsVisibilityLeaderboards": false,
    "adminEnabled": true,
    "adminGeneralEnabled": true,
    "adminFinanceEnabled": true,
    "adminBrandingEnabled": true,
    "adminBrandingDetails": false,
    "adminBrandingColors": false,
    "adminBrandingImages": false,
    "adminIntegrationsEnabled": false,
    "adminVisibilityEnabled": false,
    "adminApiEnabled": false,
    "reportingEnabled": true,
    "reportingDonations": true,
    "reportingCampaigns": false,
    "reportingFundraisers": false,
    "reportingChart": false
  }
}
```

## Examples

{% method %}
### GET /causes/35/permissions
Returns a list of permissions for cause with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/permissions
```

{% endmethod %}
