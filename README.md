# OpenAPIClient-php

API for Polario

__Naming:__

* json properties are formatted in camel case (fooBar) besides of enums (FooBar)
* route params are formatted in hyphen case (foo-bar)
* query params are formatted in snake case (foo_bar)
* query params could hold lists of elements if they are comma separated
* enum properties are formatted in capitalized camel case (FooBar)

__Default values:__

* default values are specified for optional parameters do only apply to POST requests

__Types:__

* numbers are considered to be float values
* strings that are not specified to be html formatted should be careful to interpreted them as html to avoid against xss attacks
* timestamps are considered to be in unix time

__Headers:__

* ___Platform___: can be always set as header param to specify the platform of the request for the logging output


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->authAccountAnalyticsAccountSettingsGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountAnalyticsAccountSettingsGet: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://custom.polario.de/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountApi* | [**authAccountAnalyticsAccountSettingsGet**](docs/Api/AccountApi.md#authaccountanalyticsaccountsettingsget) | **GET** /auth/account/analytics/account-settings | Get account settings analytics for cursor
*AccountApi* | [**authAccountAnalyticsAccountSettingsSearchPost**](docs/Api/AccountApi.md#authaccountanalyticsaccountsettingssearchpost) | **POST** /auth/account/analytics/account-settings/search | Create account settings analytics cursor
*AccountApi* | [**authAccountColorGet**](docs/Api/AccountApi.md#authaccountcolorget) | **GET** /auth/account/color | account colors
*AccountApi* | [**authAccountDelete**](docs/Api/AccountApi.md#authaccountdelete) | **DELETE** /auth/account | Delete accounts
*AccountApi* | [**authAccountDeleteOwnPost**](docs/Api/AccountApi.md#authaccountdeleteownpost) | **POST** /auth/account/delete-own | Delete own
*AccountApi* | [**authAccountGet**](docs/Api/AccountApi.md#authaccountget) | **GET** /auth/account | Get accounts
*AccountApi* | [**authAccountIdAccessGet**](docs/Api/AccountApi.md#authaccountidaccessget) | **GET** /auth/account/{id}/access | Get account access configuration
*AccountApi* | [**authAccountIdAccessPatch**](docs/Api/AccountApi.md#authaccountidaccesspatch) | **PATCH** /auth/account/{id}/access | Update account access configuration
*AccountApi* | [**authAccountIdCredentialsPatch**](docs/Api/AccountApi.md#authaccountidcredentialspatch) | **PATCH** /auth/account/{id}/credentials | Update account credentials
*AccountApi* | [**authAccountIdDelete**](docs/Api/AccountApi.md#authaccountiddelete) | **DELETE** /auth/account/{id} | Delete account
*AccountApi* | [**authAccountIdDeviceDeviceIdLogoutGet**](docs/Api/AccountApi.md#authaccountiddevicedeviceidlogoutget) | **GET** /auth/account/{id}/device/{deviceId}/logout | Logout device
*AccountApi* | [**authAccountIdDeviceGet**](docs/Api/AccountApi.md#authaccountiddeviceget) | **GET** /auth/account/{id}/device | Get account devices
*AccountApi* | [**authAccountIdGet**](docs/Api/AccountApi.md#authaccountidget) | **GET** /auth/account/{id} | Get account
*AccountApi* | [**authAccountIdGroupProjectProjectIdGet**](docs/Api/AccountApi.md#authaccountidgroupprojectprojectidget) | **GET** /auth/account/{id}/group/project/{projectId} | Get group list for account for project
*AccountApi* | [**authAccountIdGroupProjectProjectIdPut**](docs/Api/AccountApi.md#authaccountidgroupprojectprojectidput) | **PUT** /auth/account/{id}/group/project/{projectId} | Update account groups membership for project
*AccountApi* | [**authAccountIdPermissionGet**](docs/Api/AccountApi.md#authaccountidpermissionget) | **GET** /auth/account/{id}/permission | Get account permissions
*AccountApi* | [**authAccountIdProfileGet**](docs/Api/AccountApi.md#authaccountidprofileget) | **GET** /auth/account/{id}/profile | Get account profile
*AccountApi* | [**authAccountIdProfilePatch**](docs/Api/AccountApi.md#authaccountidprofilepatch) | **PATCH** /auth/account/{id}/profile | Update account profile
*AccountApi* | [**authAccountIdProjectProjectIdVisitPut**](docs/Api/AccountApi.md#authaccountidprojectprojectidvisitput) | **PUT** /auth/account/{id}/project/{projectId}/visit | Account entered project first time
*AccountApi* | [**authAccountIdPushDelete**](docs/Api/AccountApi.md#authaccountidpushdelete) | **DELETE** /auth/account/{id}/push | Remove push token
*AccountApi* | [**authAccountIdPushGet**](docs/Api/AccountApi.md#authaccountidpushget) | **GET** /auth/account/{id}/push | Get push token
*AccountApi* | [**authAccountIdPushPut**](docs/Api/AccountApi.md#authaccountidpushput) | **PUT** /auth/account/{id}/push | Set push token
*AccountApi* | [**authAccountIdRolesGet**](docs/Api/AccountApi.md#authaccountidrolesget) | **GET** /auth/account/{id}/roles | Get roles of an account
*AccountApi* | [**authAccountIdRolesPut**](docs/Api/AccountApi.md#authaccountidrolesput) | **PUT** /auth/account/{id}/roles | Update the roles of an account
*AccountApi* | [**authAccountIdSettingsGet**](docs/Api/AccountApi.md#authaccountidsettingsget) | **GET** /auth/account/{id}/settings | Get account settings
*AccountApi* | [**authAccountIdSettingsNotificationGet**](docs/Api/AccountApi.md#authaccountidsettingsnotificationget) | **GET** /auth/account/{id}/settings/notification | Get account notification settings
*AccountApi* | [**authAccountIdSettingsNotificationPatch**](docs/Api/AccountApi.md#authaccountidsettingsnotificationpatch) | **PATCH** /auth/account/{id}/settings/notification | Update account notification settings
*AccountApi* | [**authAccountIdSettingsProjectProjectIdGet**](docs/Api/AccountApi.md#authaccountidsettingsprojectprojectidget) | **GET** /auth/account/{id}/settings/project/{projectId} | Get account project settings
*AccountApi* | [**authAccountIdSettingsProjectProjectIdPatch**](docs/Api/AccountApi.md#authaccountidsettingsprojectprojectidpatch) | **PATCH** /auth/account/{id}/settings/project/{projectId} | Update account project settings
*AccountApi* | [**authAccountIdSettingsTrackingGet**](docs/Api/AccountApi.md#authaccountidsettingstrackingget) | **GET** /auth/account/{id}/settings/tracking | Get account tracking settings
*AccountApi* | [**authAccountIdSettingsTrackingPut**](docs/Api/AccountApi.md#authaccountidsettingstrackingput) | **PUT** /auth/account/{id}/settings/tracking | Update account tracking settings
*AccountApi* | [**authAccountIdSettingsVisibilityGet**](docs/Api/AccountApi.md#authaccountidsettingsvisibilityget) | **GET** /auth/account/{id}/settings/visibility | Get account visibility settings
*AccountApi* | [**authAccountIdSettingsVisibilityPatch**](docs/Api/AccountApi.md#authaccountidsettingsvisibilitypatch) | **PATCH** /auth/account/{id}/settings/visibility | Update account visibility settings
*AccountApi* | [**authAccountMetaGet**](docs/Api/AccountApi.md#authaccountmetaget) | **GET** /auth/account-meta | Get meta item setup
*AccountApi* | [**authAccountMetaPut**](docs/Api/AccountApi.md#authaccountmetaput) | **PUT** /auth/account-meta | Update meta item setup
*AccountApi* | [**authAccountPost**](docs/Api/AccountApi.md#authaccountpost) | **POST** /auth/account | Create account
*AccountApi* | [**authAccountProjectProjectIdIdGet**](docs/Api/AccountApi.md#authaccountprojectprojectididget) | **GET** /auth/account/project/{projectId}/id | Get project account ids
*AccountApi* | [**authAccountProjectProjectIdStatsGet**](docs/Api/AccountApi.md#authaccountprojectprojectidstatsget) | **GET** /auth/account/project/{projectId}/stats | Get project accounts statistics
*AccountApi* | [**authAccountProjectProjectIdStatsRecordGet**](docs/Api/AccountApi.md#authaccountprojectprojectidstatsrecordget) | **GET** /auth/account/project/{projectId}/stats/record | Get project accounts statistic records
*AccountApi* | [**authAccountSearchPost**](docs/Api/AccountApi.md#authaccountsearchpost) | **POST** /auth/account/search | Search accounts
*AccountApi* | [**authAccountStatsGet**](docs/Api/AccountApi.md#authaccountstatsget) | **GET** /auth/account/stats | Get accounts statistics
*AccountApi* | [**authAccountStatsRecordGet**](docs/Api/AccountApi.md#authaccountstatsrecordget) | **GET** /auth/account/stats/record | Get accounts statistic records
*AccountApi* | [**authEmailPost**](docs/Api/AccountApi.md#authemailpost) | **POST** /auth/email | Change email first
*AccountApi* | [**authEmailPut**](docs/Api/AccountApi.md#authemailput) | **PUT** /auth/email | Change email final
*AccountApi* | [**authPasswordChangePost**](docs/Api/AccountApi.md#authpasswordchangepost) | **POST** /auth/password/change | Request password change
*AccountApi* | [**authPasswordPut**](docs/Api/AccountApi.md#authpasswordput) | **PUT** /auth/password | Change Password
*AccountApi* | [**authPasswordRecoverPost**](docs/Api/AccountApi.md#authpasswordrecoverpost) | **POST** /auth/password/recover | Recover Password
*AccountApi* | [**authRegisterPost**](docs/Api/AccountApi.md#authregisterpost) | **POST** /auth/register | Registration
*AdminAreaApi* | [**newsDefaultIdPreviewDesktopGet**](docs/Api/AdminAreaApi.md#newsdefaultidpreviewdesktopget) | **GET** /news/default/{id}/preview/desktop | Get article preview desktop
*AdminAreaApi* | [**newsDefaultIdPreviewGet**](docs/Api/AdminAreaApi.md#newsdefaultidpreviewget) | **GET** /news/default/{id}/preview | Get article preview mobile
*AdminAreaApi* | [**newsDefaultPreviewSearchPost**](docs/Api/AdminAreaApi.md#newsdefaultpreviewsearchpost) | **POST** /news/default/preview/search | Create cursor
*AdminAreaApi* | [**newsDefaultProjectIdPreviewGet**](docs/Api/AdminAreaApi.md#newsdefaultprojectidpreviewget) | **GET** /news/default/project/{id}/preview | Get article list preview for project
*AdminAreaApi* | [**newsDefaultProjectIdPreviewIdsGet**](docs/Api/AdminAreaApi.md#newsdefaultprojectidpreviewidsget) | **GET** /news/default/project/{id}/preview/ids | Get article preview ids for project
*AdminAreaApi* | [**pageDefaultIdPreviewDesktopGet**](docs/Api/AdminAreaApi.md#pagedefaultidpreviewdesktopget) | **GET** /page/default/{id}/preview/desktop | Get page preview desktop
*AdminAreaApi* | [**pageDefaultIdPreviewGet**](docs/Api/AdminAreaApi.md#pagedefaultidpreviewget) | **GET** /page/default/{id}/preview | Get page preview mobile
*AdminAreaApi* | [**pageDefaultProjectIdPreviewGet**](docs/Api/AdminAreaApi.md#pagedefaultprojectidpreviewget) | **GET** /page/default/project/{id}/preview | Get page list preview for project
*AppointmentAdminApi* | [**calendarAdminAppointmentConfigIdDelete**](docs/Api/AppointmentAdminApi.md#calendaradminappointmentconfigiddelete) | **DELETE** /calendar/admin/appointment/config/{id} | Delete appointment config
*AppointmentAdminApi* | [**calendarAdminAppointmentConfigIdGet**](docs/Api/AppointmentAdminApi.md#calendaradminappointmentconfigidget) | **GET** /calendar/admin/appointment/config/{id} | Get appointment config
*AppointmentAdminApi* | [**calendarAdminAppointmentConfigIdPatch**](docs/Api/AppointmentAdminApi.md#calendaradminappointmentconfigidpatch) | **PATCH** /calendar/admin/appointment/config/{id} | Update appointment config
*AppointmentAdminApi* | [**calendarAdminAppointmentConfigPost**](docs/Api/AppointmentAdminApi.md#calendaradminappointmentconfigpost) | **POST** /calendar/admin/appointment/config | Create appointment config
*AppointmentAdminApi* | [**calendarAdminAppointmentConfigProjectIdGet**](docs/Api/AppointmentAdminApi.md#calendaradminappointmentconfigprojectidget) | **GET** /calendar/admin/appointment/config/project/{id} | Get appointment config list for project
*AppointmentDefaultApi* | [**calendarDefaultAppointmentGet**](docs/Api/AppointmentDefaultApi.md#calendardefaultappointmentget) | **GET** /calendar/default/appointment | Get appointment list for cursor
*AppointmentDefaultApi* | [**calendarDefaultAppointmentIdGet**](docs/Api/AppointmentDefaultApi.md#calendardefaultappointmentidget) | **GET** /calendar/default/appointment/{id} | Get appointment
*AppointmentDefaultApi* | [**calendarDefaultAppointmentPost**](docs/Api/AppointmentDefaultApi.md#calendardefaultappointmentpost) | **POST** /calendar/default/appointment | Create appointment
*AppointmentDefaultApi* | [**calendarDefaultAppointmentSearchPost**](docs/Api/AppointmentDefaultApi.md#calendardefaultappointmentsearchpost) | **POST** /calendar/default/appointment/search | Create cursor
*AppointmentDefaultApi* | [**calendarDefaultAppointmentSlotAllGet**](docs/Api/AppointmentDefaultApi.md#calendardefaultappointmentslotallget) | **GET** /calendar/default/appointment/slot/all | Get all appointment slot options
*AppointmentDefaultApi* | [**calendarDefaultAppointmentSlotSearchPost**](docs/Api/AppointmentDefaultApi.md#calendardefaultappointmentslotsearchpost) | **POST** /calendar/default/appointment/slot/search | Get possible appointment slot options
*AuthApi* | [**authAuthPost**](docs/Api/AuthApi.md#authauthpost) | **POST** /auth/auth | SCRAM First
*CalendarAdminApi* | [**calendarAdminEntryIdAccessGet**](docs/Api/CalendarAdminApi.md#calendaradminentryidaccessget) | **GET** /calendar/admin/entry/{id}/access | Get calendar entry access configuration
*CalendarAdminApi* | [**calendarAdminEntryIdAccessPatch**](docs/Api/CalendarAdminApi.md#calendaradminentryidaccesspatch) | **PATCH** /calendar/admin/entry/{id}/access | Update calendar entry access configuration
*CalendarAdminApi* | [**calendarAdminEntryIdBookingAccountAccountIdDelete**](docs/Api/CalendarAdminApi.md#calendaradminentryidbookingaccountaccountiddelete) | **DELETE** /calendar/admin/entry/{id}/booking/account/{accountId} | Delete booking
*CalendarAdminApi* | [**calendarAdminEntryIdBookingPost**](docs/Api/CalendarAdminApi.md#calendaradminentryidbookingpost) | **POST** /calendar/admin/entry/{id}/booking | Create booking
*CalendarAdminApi* | [**calendarAdminEntryIdDelete**](docs/Api/CalendarAdminApi.md#calendaradminentryiddelete) | **DELETE** /calendar/admin/entry/{id} | Delete calendar entry
*CalendarAdminApi* | [**calendarAdminEntryIdGet**](docs/Api/CalendarAdminApi.md#calendaradminentryidget) | **GET** /calendar/admin/entry/{id} | Get calendar entry
*CalendarAdminApi* | [**calendarAdminEntryIdPut**](docs/Api/CalendarAdminApi.md#calendaradminentryidput) | **PUT** /calendar/admin/entry/{id} | Update calendar entry
*CalendarAdminApi* | [**calendarAdminIdContentGet**](docs/Api/CalendarAdminApi.md#calendaradminidcontentget) | **GET** /calendar/admin/{id}/content | Get calendar entries list for calendar
*CalendarAdminApi* | [**calendarAdminIdContentPost**](docs/Api/CalendarAdminApi.md#calendaradminidcontentpost) | **POST** /calendar/admin/{id}/content | Add calendar entries
*CalendarAdminApi* | [**calendarAdminIdDelete**](docs/Api/CalendarAdminApi.md#calendaradminiddelete) | **DELETE** /calendar/admin/{id} | Delete calendar
*CalendarAdminApi* | [**calendarAdminIdDetailGet**](docs/Api/CalendarAdminApi.md#calendaradminiddetailget) | **GET** /calendar/admin/{id}/detail | Get calendar detail view
*CalendarAdminApi* | [**calendarAdminIdDetailPut**](docs/Api/CalendarAdminApi.md#calendaradminiddetailput) | **PUT** /calendar/admin/{id}/detail | Update calendar detail view
*CalendarAdminApi* | [**calendarAdminIdGet**](docs/Api/CalendarAdminApi.md#calendaradminidget) | **GET** /calendar/admin/{id} | Get calendar
*CalendarAdminApi* | [**calendarAdminIdItemsGet**](docs/Api/CalendarAdminApi.md#calendaradminiditemsget) | **GET** /calendar/admin/{id}/items | Get calendar detail view items
*CalendarAdminApi* | [**calendarAdminIdListSettingsGet**](docs/Api/CalendarAdminApi.md#calendaradminidlistsettingsget) | **GET** /calendar/admin/{id}/list-settings | Get calendar list settings
*CalendarAdminApi* | [**calendarAdminIdListSettingsPut**](docs/Api/CalendarAdminApi.md#calendaradminidlistsettingsput) | **PUT** /calendar/admin/{id}/list-settings | Update calendar list settings
*CalendarAdminApi* | [**calendarAdminIdPatch**](docs/Api/CalendarAdminApi.md#calendaradminidpatch) | **PATCH** /calendar/admin/{id} | Update calendar info
*CalendarAdminApi* | [**calendarAdminIdSelectionsGet**](docs/Api/CalendarAdminApi.md#calendaradminidselectionsget) | **GET** /calendar/admin/{id}/selections | Get calendar detail view selections
*CalendarAdminApi* | [**calendarAdminPost**](docs/Api/CalendarAdminApi.md#calendaradminpost) | **POST** /calendar/admin | Create calendar
*CalendarAdminApi* | [**calendarAdminProjectIdGet**](docs/Api/CalendarAdminApi.md#calendaradminprojectidget) | **GET** /calendar/admin/project/{id} | Get calendar list for project
*CalendarAdminApi* | [**calendarAdminSyncPut**](docs/Api/CalendarAdminApi.md#calendaradminsyncput) | **PUT** /calendar/admin/sync | Sync operators for all calendar entries
*CalendarAdminApi* | [**calendarAdminTemplateGet**](docs/Api/CalendarAdminApi.md#calendaradmintemplateget) | **GET** /calendar/admin/template | Get calendar template list
*CalendarDefaultApi* | [**calendarDefaultEntryGet**](docs/Api/CalendarDefaultApi.md#calendardefaultentryget) | **GET** /calendar/default/entry | Get calendar entries list for cursor
*CalendarDefaultApi* | [**calendarDefaultEntryIdBookingGet**](docs/Api/CalendarDefaultApi.md#calendardefaultentryidbookingget) | **GET** /calendar/default/entry/{id}/booking | Get booking
*CalendarDefaultApi* | [**calendarDefaultEntryIdGet**](docs/Api/CalendarDefaultApi.md#calendardefaultentryidget) | **GET** /calendar/default/entry/{id} | Get calendar entry
*CalendarDefaultApi* | [**calendarDefaultEntrySearchPost**](docs/Api/CalendarDefaultApi.md#calendardefaultentrysearchpost) | **POST** /calendar/default/entry/search | Create entry cursor
*CalendarDefaultApi* | [**calendarDefaultIdContentGet**](docs/Api/CalendarDefaultApi.md#calendardefaultidcontentget) | **GET** /calendar/default/{id}/content | Get calendar entries list for calendar
*CalendarDefaultApi* | [**calendarDefaultIdGet**](docs/Api/CalendarDefaultApi.md#calendardefaultidget) | **GET** /calendar/default/{id} | Get calendar
*CalendarDefaultApi* | [**calendarDefaultMyCalendarContentGet**](docs/Api/CalendarDefaultApi.md#calendardefaultmycalendarcontentget) | **GET** /calendar/default/my-calendar/content | Get calendar entries list for my calendar
*CalendarDefaultApi* | [**calendarDefaultMyCalendarGet**](docs/Api/CalendarDefaultApi.md#calendardefaultmycalendarget) | **GET** /calendar/default/my-calendar | Get my calendar
*ChatAdminApi* | [**chatAdminChannelChannelURLDelete**](docs/Api/ChatAdminApi.md#chatadminchannelchannelurldelete) | **DELETE** /chat/admin/channel/{channelURL} | delete a chat channel
*ChatAdminApi* | [**chatAdminChannelGet**](docs/Api/ChatAdminApi.md#chatadminchannelget) | **GET** /chat/admin/channel | Get list of chat channels
*ChatAdminApi* | [**chatAdminFeedIdAccessGet**](docs/Api/ChatAdminApi.md#chatadminfeedidaccessget) | **GET** /chat/admin/feed/{id}/access | Get chat feed access configuration
*ChatAdminApi* | [**chatAdminFeedIdAccessPatch**](docs/Api/ChatAdminApi.md#chatadminfeedidaccesspatch) | **PATCH** /chat/admin/feed/{id}/access | Update chat feed access configuration
*ChatAdminApi* | [**chatAdminFeedIdDelete**](docs/Api/ChatAdminApi.md#chatadminfeediddelete) | **DELETE** /chat/admin/feed/{id} | Delete chat feed
*ChatAdminApi* | [**chatAdminFeedIdGet**](docs/Api/ChatAdminApi.md#chatadminfeedidget) | **GET** /chat/admin/feed/{id} | Get chat feed
*ChatAdminApi* | [**chatAdminFeedIdPatch**](docs/Api/ChatAdminApi.md#chatadminfeedidpatch) | **PATCH** /chat/admin/feed/{id} | Update chat feed
*ChatAdminApi* | [**chatAdminFeedPost**](docs/Api/ChatAdminApi.md#chatadminfeedpost) | **POST** /chat/admin/feed | Create chat feed
*ChatAdminApi* | [**chatAdminFeedProjectIdGet**](docs/Api/ChatAdminApi.md#chatadminfeedprojectidget) | **GET** /chat/admin/feed/project/{id} | Get chat feeds of project
*ChatAdminApi* | [**chatAdminFeedSyncPut**](docs/Api/ChatAdminApi.md#chatadminfeedsyncput) | **PUT** /chat/admin/feed/sync | Sync Operators for all chat feeds
*ChatDefaultApi* | [**chatDefaultChannelChannelURLInvitePost**](docs/Api/ChatDefaultApi.md#chatdefaultchannelchannelurlinvitepost) | **POST** /chat/default/channel/{channelURL}/invite | invite users to protected chat channel
*ChatDefaultApi* | [**chatDefaultChannelChannelURLJoinPost**](docs/Api/ChatDefaultApi.md#chatdefaultchannelchannelurljoinpost) | **POST** /chat/default/channel/{channelURL}/join | request join for protected chat channel
*ChatDefaultApi* | [**chatDefaultChannelChannelURLRequestGet**](docs/Api/ChatDefaultApi.md#chatdefaultchannelchannelurlrequestget) | **GET** /chat/default/channel/{channelURL}/request | get requests for chat channel
*ChatDefaultApi* | [**chatDefaultChannelChannelURLRequestIdGet**](docs/Api/ChatDefaultApi.md#chatdefaultchannelchannelurlrequestidget) | **GET** /chat/default/channel/{channelURL}/request/{id} | get request of account for chat channel
*ChatDefaultApi* | [**chatDefaultChannelChannelURLRequestIdPost**](docs/Api/ChatDefaultApi.md#chatdefaultchannelchannelurlrequestidpost) | **POST** /chat/default/channel/{channelURL}/request/{id} | process join request for protected chat channel
*ChatDefaultApi* | [**chatDefaultChannelRequestGet**](docs/Api/ChatDefaultApi.md#chatdefaultchannelrequestget) | **GET** /chat/default/channel/request | get requests for all chat channels for requesting account
*ChatDefaultApi* | [**chatDefaultChannelRequestPost**](docs/Api/ChatDefaultApi.md#chatdefaultchannelrequestpost) | **POST** /chat/default/channel/request | get requests for chat channels
*ChatDefaultApi* | [**chatDefaultFeedIdGet**](docs/Api/ChatDefaultApi.md#chatdefaultfeedidget) | **GET** /chat/default/feed/{id} | Get chat feed
*ChatDefaultApi* | [**chatDefaultFeedIdJoinPost**](docs/Api/ChatDefaultApi.md#chatdefaultfeedidjoinpost) | **POST** /chat/default/feed/{id}/join | Join chat feed
*ChatDefaultApi* | [**chatDefaultFeedProjectIdGet**](docs/Api/ChatDefaultApi.md#chatdefaultfeedprojectidget) | **GET** /chat/default/feed/project/{id} | Get chat feeds of project
*ConfigAdminApi* | [**configAdminDesignCustomCssGet**](docs/Api/ConfigAdminApi.md#configadmindesigncustomcssget) | **GET** /config/admin/design/custom-css | Get Custom CSS
*ConfigAdminApi* | [**configAdminDesignCustomCssPatch**](docs/Api/ConfigAdminApi.md#configadmindesigncustomcsspatch) | **PATCH** /config/admin/design/custom-css | Update Custom CSS
*ConfigAdminApi* | [**configAdminDesignDefaultGet**](docs/Api/ConfigAdminApi.md#configadmindesigndefaultget) | **GET** /config/admin/design/default | Get factory default design
*ConfigAdminApi* | [**configAdminDesignGet**](docs/Api/ConfigAdminApi.md#configadmindesignget) | **GET** /config/admin/design | Get design
*ConfigAdminApi* | [**configAdminDesignPatch**](docs/Api/ConfigAdminApi.md#configadmindesignpatch) | **PATCH** /config/admin/design | Update design
*ConfigAdminApi* | [**configAdminDesignSchemeGet**](docs/Api/ConfigAdminApi.md#configadmindesignschemeget) | **GET** /config/admin/design/scheme | Get schemes list
*ConfigAdminApi* | [**configAdminDesignSchemeIdDefaultGet**](docs/Api/ConfigAdminApi.md#configadmindesignschemeiddefaultget) | **GET** /config/admin/design/scheme/{id}/default | Get factory default for system scheme
*ConfigAdminApi* | [**configAdminDesignSchemeIdDelete**](docs/Api/ConfigAdminApi.md#configadmindesignschemeiddelete) | **DELETE** /config/admin/design/scheme/{id} | Delete custom scheme
*ConfigAdminApi* | [**configAdminDesignSchemeIdGet**](docs/Api/ConfigAdminApi.md#configadmindesignschemeidget) | **GET** /config/admin/design/scheme/{id} | Get scheme
*ConfigAdminApi* | [**configAdminDesignSchemeIdPatch**](docs/Api/ConfigAdminApi.md#configadmindesignschemeidpatch) | **PATCH** /config/admin/design/scheme/{id} | Update scheme
*ConfigAdminApi* | [**configAdminDesignSchemePost**](docs/Api/ConfigAdminApi.md#configadmindesignschemepost) | **POST** /config/admin/design/scheme | Create custom scheme
*ConfigAdminApi* | [**configAdminFeaturesGet**](docs/Api/ConfigAdminApi.md#configadminfeaturesget) | **GET** /config/admin/features | Get features
*ConfigAdminApi* | [**configAdminFeaturesPatch**](docs/Api/ConfigAdminApi.md#configadminfeaturespatch) | **PATCH** /config/admin/features | Update features
*ConfigAdminApi* | [**configAdminKnowledgeBaseObjectTypeGet**](docs/Api/ConfigAdminApi.md#configadminknowledgebaseobjecttypeget) | **GET** /config/admin/knowledge-base/{objectType} | Get knowledge base articles
*ConfigAdminApi* | [**configAdminPremiumGet**](docs/Api/ConfigAdminApi.md#configadminpremiumget) | **GET** /config/admin/premium | Get premium features
*ConfigAdminApi* | [**configAdminPremiumPatch**](docs/Api/ConfigAdminApi.md#configadminpremiumpatch) | **PATCH** /config/admin/premium | Update premium features
*ConfigAdminApi* | [**configAdminSecurityDefaultGet**](docs/Api/ConfigAdminApi.md#configadminsecuritydefaultget) | **GET** /config/admin/security/default | Get factory default security settings
*ConfigAdminApi* | [**configAdminSecurityGet**](docs/Api/ConfigAdminApi.md#configadminsecurityget) | **GET** /config/admin/security | Get security settings
*ConfigAdminApi* | [**configAdminSecurityPatch**](docs/Api/ConfigAdminApi.md#configadminsecuritypatch) | **PATCH** /config/admin/security | Update security settings
*ConfigDefaultApi* | [**configDefaultDesignGet**](docs/Api/ConfigDefaultApi.md#configdefaultdesignget) | **GET** /config/default/design | Get design
*ConfigDefaultApi* | [**configDefaultDesignSchemeIdGet**](docs/Api/ConfigDefaultApi.md#configdefaultdesignschemeidget) | **GET** /config/default/design/scheme/{id} | Get scheme
*ConfigDefaultApi* | [**configDefaultFeaturesGet**](docs/Api/ConfigDefaultApi.md#configdefaultfeaturesget) | **GET** /config/default/features | Get features
*ConfigDefaultApi* | [**configDefaultPremiumGet**](docs/Api/ConfigDefaultApi.md#configdefaultpremiumget) | **GET** /config/default/premium | Get premium features
*ConfigDefaultApi* | [**configDefaultSecurityGet**](docs/Api/ConfigDefaultApi.md#configdefaultsecurityget) | **GET** /config/default/security | Get security settings
*ConnectedAppApi* | [**authConnectedAppGet**](docs/Api/ConnectedAppApi.md#authconnectedappget) | **GET** /auth/connected-app | get connected apps list
*ConnectedAppApi* | [**authConnectedAppIdDelete**](docs/Api/ConnectedAppApi.md#authconnectedappiddelete) | **DELETE** /auth/connected-app/{id} | Delete connected app
*ConnectedAppApi* | [**authConnectedAppIdGet**](docs/Api/ConnectedAppApi.md#authconnectedappidget) | **GET** /auth/connected-app/{id} | get connected app
*ConnectedAppApi* | [**authConnectedAppIdPatch**](docs/Api/ConnectedAppApi.md#authconnectedappidpatch) | **PATCH** /auth/connected-app/{id} | Update connected app
*ConnectedAppApi* | [**authConnectedAppIdSecretDelete**](docs/Api/ConnectedAppApi.md#authconnectedappidsecretdelete) | **DELETE** /auth/connected-app/{id}/secret | Remove secret
*ConnectedAppApi* | [**authConnectedAppIdSecretPost**](docs/Api/ConnectedAppApi.md#authconnectedappidsecretpost) | **POST** /auth/connected-app/{id}/secret | Add secret
*ConnectedAppApi* | [**authConnectedAppIdSessionPost**](docs/Api/ConnectedAppApi.md#authconnectedappidsessionpost) | **POST** /auth/connected-app/{id}/session | Create session
*ConnectedAppApi* | [**authConnectedAppPost**](docs/Api/ConnectedAppApi.md#authconnectedapppost) | **POST** /auth/connected-app | Create connected app
*DirectoryAdminApi* | [**directoryAdminGet**](docs/Api/DirectoryAdminApi.md#directoryadminget) | **GET** /directory/admin | Get directory list for cursor
*DirectoryAdminApi* | [**directoryAdminIdContentGet**](docs/Api/DirectoryAdminApi.md#directoryadminidcontentget) | **GET** /directory/admin/{id}/content | Get directory content rows list
*DirectoryAdminApi* | [**directoryAdminIdContentPost**](docs/Api/DirectoryAdminApi.md#directoryadminidcontentpost) | **POST** /directory/admin/{id}/content | Add directory content rows
*DirectoryAdminApi* | [**directoryAdminIdCopyPost**](docs/Api/DirectoryAdminApi.md#directoryadminidcopypost) | **POST** /directory/admin/{id}/copy | Copy directory
*DirectoryAdminApi* | [**directoryAdminIdDelete**](docs/Api/DirectoryAdminApi.md#directoryadminiddelete) | **DELETE** /directory/admin/{id} | Delete directory
*DirectoryAdminApi* | [**directoryAdminIdDetailGet**](docs/Api/DirectoryAdminApi.md#directoryadminiddetailget) | **GET** /directory/admin/{id}/detail | Get directory detail view
*DirectoryAdminApi* | [**directoryAdminIdDetailPut**](docs/Api/DirectoryAdminApi.md#directoryadminiddetailput) | **PUT** /directory/admin/{id}/detail | Update directory detail view
*DirectoryAdminApi* | [**directoryAdminIdGet**](docs/Api/DirectoryAdminApi.md#directoryadminidget) | **GET** /directory/admin/{id} | Get directory
*DirectoryAdminApi* | [**directoryAdminIdItemsGet**](docs/Api/DirectoryAdminApi.md#directoryadminiditemsget) | **GET** /directory/admin/{id}/items | Get directory detail view items
*DirectoryAdminApi* | [**directoryAdminIdListSettingsGet**](docs/Api/DirectoryAdminApi.md#directoryadminidlistsettingsget) | **GET** /directory/admin/{id}/list-settings | Get directory list settings
*DirectoryAdminApi* | [**directoryAdminIdListSettingsPut**](docs/Api/DirectoryAdminApi.md#directoryadminidlistsettingsput) | **PUT** /directory/admin/{id}/list-settings | Update directory list settings
*DirectoryAdminApi* | [**directoryAdminIdPatch**](docs/Api/DirectoryAdminApi.md#directoryadminidpatch) | **PATCH** /directory/admin/{id} | Update directory info
*DirectoryAdminApi* | [**directoryAdminIdSelectionsGet**](docs/Api/DirectoryAdminApi.md#directoryadminidselectionsget) | **GET** /directory/admin/{id}/selections | Get directory detail view selections
*DirectoryAdminApi* | [**directoryAdminPost**](docs/Api/DirectoryAdminApi.md#directoryadminpost) | **POST** /directory/admin | Create directory
*DirectoryAdminApi* | [**directoryAdminProjectIdGet**](docs/Api/DirectoryAdminApi.md#directoryadminprojectidget) | **GET** /directory/admin/project/{id} | Get directory list for project
*DirectoryAdminApi* | [**directoryAdminRowIdAccessGet**](docs/Api/DirectoryAdminApi.md#directoryadminrowidaccessget) | **GET** /directory/admin/row/{id}/access | Get directory row access configuration
*DirectoryAdminApi* | [**directoryAdminRowIdAccessPatch**](docs/Api/DirectoryAdminApi.md#directoryadminrowidaccesspatch) | **PATCH** /directory/admin/row/{id}/access | Update directory row access configuration
*DirectoryAdminApi* | [**directoryAdminRowIdDelete**](docs/Api/DirectoryAdminApi.md#directoryadminrowiddelete) | **DELETE** /directory/admin/row/{id} | Delete directory content row
*DirectoryAdminApi* | [**directoryAdminRowIdGet**](docs/Api/DirectoryAdminApi.md#directoryadminrowidget) | **GET** /directory/admin/row/{id} | Get directory content row
*DirectoryAdminApi* | [**directoryAdminRowIdPut**](docs/Api/DirectoryAdminApi.md#directoryadminrowidput) | **PUT** /directory/admin/row/{id} | Update directory content row
*DirectoryAdminApi* | [**directoryAdminSearchPost**](docs/Api/DirectoryAdminApi.md#directoryadminsearchpost) | **POST** /directory/admin/search | Create cursor
*DirectoryAdminApi* | [**directoryAdminTemplateGet**](docs/Api/DirectoryAdminApi.md#directoryadmintemplateget) | **GET** /directory/admin/template | Get directory template list
*DirectoryDefaultApi* | [**directoryDefaultIdContentGet**](docs/Api/DirectoryDefaultApi.md#directorydefaultidcontentget) | **GET** /directory/default/{id}/content | Get directory content rows list
*DirectoryDefaultApi* | [**directoryDefaultIdGet**](docs/Api/DirectoryDefaultApi.md#directorydefaultidget) | **GET** /directory/default/{id} | Get directory
*DirectoryDefaultApi* | [**directoryDefaultIdRowPost**](docs/Api/DirectoryDefaultApi.md#directorydefaultidrowpost) | **POST** /directory/default/{id}/row | Add directory content row
*DirectoryDefaultApi* | [**directoryDefaultRowIdDelete**](docs/Api/DirectoryDefaultApi.md#directorydefaultrowiddelete) | **DELETE** /directory/default/row/{id} | Delete directory content row
*DirectoryDefaultApi* | [**directoryDefaultRowIdGet**](docs/Api/DirectoryDefaultApi.md#directorydefaultrowidget) | **GET** /directory/default/row/{id} | Get directory content row
*DirectoryDefaultApi* | [**directoryDefaultRowIdPut**](docs/Api/DirectoryDefaultApi.md#directorydefaultrowidput) | **PUT** /directory/default/row/{id} | Update directory content row
*EmailAdminApi* | [**notificationAdminEmailIdDelete**](docs/Api/EmailAdminApi.md#notificationadminemailiddelete) | **DELETE** /notification/admin/email/{id} | Delete email
*EmailAdminApi* | [**notificationAdminEmailIdGet**](docs/Api/EmailAdminApi.md#notificationadminemailidget) | **GET** /notification/admin/email/{id} | Get email
*EmailAdminApi* | [**notificationAdminEmailIdPatch**](docs/Api/EmailAdminApi.md#notificationadminemailidpatch) | **PATCH** /notification/admin/email/{id} | Update email
*EmailAdminApi* | [**notificationAdminEmailPost**](docs/Api/EmailAdminApi.md#notificationadminemailpost) | **POST** /notification/admin/email | Create email
*EmailAdminApi* | [**notificationAdminEmailProjectIdGet**](docs/Api/EmailAdminApi.md#notificationadminemailprojectidget) | **GET** /notification/admin/email/project/{id} | Get all project emails
*EmailAdminApi* | [**notificationAdminEmailTestPost**](docs/Api/EmailAdminApi.md#notificationadminemailtestpost) | **POST** /notification/admin/email/test | Test email content
*GroupApi* | [**authGroupGet**](docs/Api/GroupApi.md#authgroupget) | **GET** /auth/group | Get group list
*GroupApi* | [**authGroupIdAccountDelete**](docs/Api/GroupApi.md#authgroupidaccountdelete) | **DELETE** /auth/group/{id}/account | remove accounts from group
*GroupApi* | [**authGroupIdAccountGet**](docs/Api/GroupApi.md#authgroupidaccountget) | **GET** /auth/group/{id}/account | Get accounts of group
*GroupApi* | [**authGroupIdAccountPost**](docs/Api/GroupApi.md#authgroupidaccountpost) | **POST** /auth/group/{id}/account | add accounts to group
*GroupApi* | [**authGroupIdDelete**](docs/Api/GroupApi.md#authgroupiddelete) | **DELETE** /auth/group/{id} | Delete group
*GroupApi* | [**authGroupIdGet**](docs/Api/GroupApi.md#authgroupidget) | **GET** /auth/group/{id} | Get group
*GroupApi* | [**authGroupIdPatch**](docs/Api/GroupApi.md#authgroupidpatch) | **PATCH** /auth/group/{id} | Update group
*GroupApi* | [**authGroupPost**](docs/Api/GroupApi.md#authgrouppost) | **POST** /auth/group | Create group
*GroupApi* | [**authGroupProjectIdGet**](docs/Api/GroupApi.md#authgroupprojectidget) | **GET** /auth/group/project/{id} | Get group list for project
*I18nAdminApi* | [**configAdminLanguageDefaultPut**](docs/Api/I18nAdminApi.md#configadminlanguagedefaultput) | **PUT** /config/admin/language/default | Update default language
*I18nAdminApi* | [**configAdminLanguageGet**](docs/Api/I18nAdminApi.md#configadminlanguageget) | **GET** /config/admin/language | Get languages
*I18nAdminApi* | [**configAdminLanguageIdGet**](docs/Api/I18nAdminApi.md#configadminlanguageidget) | **GET** /config/admin/language/{id} | Get language
*I18nAdminApi* | [**configAdminLanguageIdLocalizationDefaultPut**](docs/Api/I18nAdminApi.md#configadminlanguageidlocalizationdefaultput) | **PUT** /config/admin/language/{id}/localization/default | Reset localizations
*I18nAdminApi* | [**configAdminLanguageIdLocalizationGet**](docs/Api/I18nAdminApi.md#configadminlanguageidlocalizationget) | **GET** /config/admin/language/{id}/localization | Get localizations of language
*I18nAdminApi* | [**configAdminLanguageIdPatch**](docs/Api/I18nAdminApi.md#configadminlanguageidpatch) | **PATCH** /config/admin/language/{id} | Update language
*I18nAdminApi* | [**configAdminLocalizationGet**](docs/Api/I18nAdminApi.md#configadminlocalizationget) | **GET** /config/admin/localization | Get localizations for cursor
*I18nAdminApi* | [**configAdminLocalizationGlossaryGet**](docs/Api/I18nAdminApi.md#configadminlocalizationglossaryget) | **GET** /config/admin/localization/glossary | Get glossary
*I18nAdminApi* | [**configAdminLocalizationGlossaryIdDelete**](docs/Api/I18nAdminApi.md#configadminlocalizationglossaryiddelete) | **DELETE** /config/admin/localization/glossary/{id} | Delete glossary entry
*I18nAdminApi* | [**configAdminLocalizationGlossaryIdGet**](docs/Api/I18nAdminApi.md#configadminlocalizationglossaryidget) | **GET** /config/admin/localization/glossary/{id} | Get glossary entry
*I18nAdminApi* | [**configAdminLocalizationGlossaryIdPut**](docs/Api/I18nAdminApi.md#configadminlocalizationglossaryidput) | **PUT** /config/admin/localization/glossary/{id} | Update glossary entry
*I18nAdminApi* | [**configAdminLocalizationGlossaryPost**](docs/Api/I18nAdminApi.md#configadminlocalizationglossarypost) | **POST** /config/admin/localization/glossary | Create glossary entry
*I18nAdminApi* | [**configAdminLocalizationIdDefaultPut**](docs/Api/I18nAdminApi.md#configadminlocalizationiddefaultput) | **PUT** /config/admin/localization/{id}/default | Reset localization
*I18nAdminApi* | [**configAdminLocalizationIdGet**](docs/Api/I18nAdminApi.md#configadminlocalizationidget) | **GET** /config/admin/localization/{id} | Get localization
*I18nAdminApi* | [**configAdminLocalizationIdPatch**](docs/Api/I18nAdminApi.md#configadminlocalizationidpatch) | **PATCH** /config/admin/localization/{id} | Update localization
*I18nAdminApi* | [**configAdminLocalizationKeysGet**](docs/Api/I18nAdminApi.md#configadminlocalizationkeysget) | **GET** /config/admin/localization/keys | Get localization keys
*I18nAdminApi* | [**configAdminLocalizationSearchPost**](docs/Api/I18nAdminApi.md#configadminlocalizationsearchpost) | **POST** /config/admin/localization/search | Create cursor
*I18nDefaultApi* | [**configDefaultLanguageGet**](docs/Api/I18nDefaultApi.md#configdefaultlanguageget) | **GET** /config/default/language | Get languages
*I18nDefaultApi* | [**configDefaultLocalizationGet**](docs/Api/I18nDefaultApi.md#configdefaultlocalizationget) | **GET** /config/default/localization | Get localizations
*IndexAdminApi* | [**indexAdminGet**](docs/Api/IndexAdminApi.md#indexadminget) | **GET** /index/admin | Get index items for cursor
*IndexAdminApi* | [**indexAdminObjectTypeObjectIdGet**](docs/Api/IndexAdminApi.md#indexadminobjecttypeobjectidget) | **GET** /index/admin/{objectType}/{objectId} | Get index
*IndexAdminApi* | [**indexAdminObjectTypeObjectIdLinkedGet**](docs/Api/IndexAdminApi.md#indexadminobjecttypeobjectidlinkedget) | **GET** /index/admin/{objectType}/{objectId}/linked | Get linked items
*IndexAdminApi* | [**indexAdminSearchPost**](docs/Api/IndexAdminApi.md#indexadminsearchpost) | **POST** /index/admin/search | Create cursor
*IndexDefaultApi* | [**indexDefaultGet**](docs/Api/IndexDefaultApi.md#indexdefaultget) | **GET** /index/default | Get index items for cursor
*IndexDefaultApi* | [**indexDefaultObjectTypeObjectIdLinkedGet**](docs/Api/IndexDefaultApi.md#indexdefaultobjecttypeobjectidlinkedget) | **GET** /index/default/{objectType}/{objectId}/linked | Get linked items
*IndexDefaultApi* | [**indexDefaultSearchPost**](docs/Api/IndexDefaultApi.md#indexdefaultsearchpost) | **POST** /index/default/search | Create cursor
*JourneyAdminApi* | [**reactionAdminJourneyIdAttendeeDelete**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidattendeedelete) | **DELETE** /reaction/admin/journey/{id}/attendee | Remove attendees
*JourneyAdminApi* | [**reactionAdminJourneyIdAttendeeGet**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidattendeeget) | **GET** /reaction/admin/journey/{id}/attendee | Get attendees
*JourneyAdminApi* | [**reactionAdminJourneyIdAttendeePatch**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidattendeepatch) | **PATCH** /reaction/admin/journey/{id}/attendee | Update attendees
*JourneyAdminApi* | [**reactionAdminJourneyIdAttendeePost**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidattendeepost) | **POST** /reaction/admin/journey/{id}/attendee | Add attendees
*JourneyAdminApi* | [**reactionAdminJourneyIdDelete**](docs/Api/JourneyAdminApi.md#reactionadminjourneyiddelete) | **DELETE** /reaction/admin/journey/{id} | Delete journey
*JourneyAdminApi* | [**reactionAdminJourneyIdGet**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidget) | **GET** /reaction/admin/journey/{id} | Get journey
*JourneyAdminApi* | [**reactionAdminJourneyIdPatch**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidpatch) | **PATCH** /reaction/admin/journey/{id} | Update journey
*JourneyAdminApi* | [**reactionAdminJourneyIdStagesGet**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidstagesget) | **GET** /reaction/admin/journey/{id}/stages | Get stages
*JourneyAdminApi* | [**reactionAdminJourneyIdStagesPut**](docs/Api/JourneyAdminApi.md#reactionadminjourneyidstagesput) | **PUT** /reaction/admin/journey/{id}/stages | Update stages
*JourneyAdminApi* | [**reactionAdminJourneyPost**](docs/Api/JourneyAdminApi.md#reactionadminjourneypost) | **POST** /reaction/admin/journey | Create journey
*JourneyAdminApi* | [**reactionAdminJourneyProjectIdGet**](docs/Api/JourneyAdminApi.md#reactionadminjourneyprojectidget) | **GET** /reaction/admin/journey/project/{id} | Get journey list for project
*JourneyDefaultApi* | [**reactionDefaultJourneyGet**](docs/Api/JourneyDefaultApi.md#reactiondefaultjourneyget) | **GET** /reaction/default/journey | Get journey processes list for cursor
*JourneyDefaultApi* | [**reactionDefaultJourneyIdGet**](docs/Api/JourneyDefaultApi.md#reactiondefaultjourneyidget) | **GET** /reaction/default/journey/{id} | Get journey
*JourneyDefaultApi* | [**reactionDefaultJourneyIdProcessGet**](docs/Api/JourneyDefaultApi.md#reactiondefaultjourneyidprocessget) | **GET** /reaction/default/journey/{id}/process | Get journey process
*JourneyDefaultApi* | [**reactionDefaultJourneyIdStageStageIdPatch**](docs/Api/JourneyDefaultApi.md#reactiondefaultjourneyidstagestageidpatch) | **PATCH** /reaction/default/journey/{id}/stage/{stageId} | Update stage status
*JourneyDefaultApi* | [**reactionDefaultJourneySearchPost**](docs/Api/JourneyDefaultApi.md#reactiondefaultjourneysearchpost) | **POST** /reaction/default/journey/search | Create cursor
*JourneyDefaultApi* | [**reactionDefaultJourneyStatsGet**](docs/Api/JourneyDefaultApi.md#reactiondefaultjourneystatsget) | **GET** /reaction/default/journey/stats | Get journey stats
*KeywordAdminApi* | [**keywordAdminCategoryGet**](docs/Api/KeywordAdminApi.md#keywordadmincategoryget) | **GET** /keyword/admin/category | Get keyword category list
*KeywordAdminApi* | [**keywordAdminCategoryIdDelete**](docs/Api/KeywordAdminApi.md#keywordadmincategoryiddelete) | **DELETE** /keyword/admin/category/{id} | Delete keyword category
*KeywordAdminApi* | [**keywordAdminCategoryIdGet**](docs/Api/KeywordAdminApi.md#keywordadmincategoryidget) | **GET** /keyword/admin/category/{id} | Get keyword category
*KeywordAdminApi* | [**keywordAdminCategoryIdPatch**](docs/Api/KeywordAdminApi.md#keywordadmincategoryidpatch) | **PATCH** /keyword/admin/category/{id} | Update keyword category
*KeywordAdminApi* | [**keywordAdminCategoryPost**](docs/Api/KeywordAdminApi.md#keywordadmincategorypost) | **POST** /keyword/admin/category | Create keyword category
*KeywordAdminApi* | [**keywordAdminGet**](docs/Api/KeywordAdminApi.md#keywordadminget) | **GET** /keyword/admin | Get keyword list
*KeywordAdminApi* | [**keywordAdminIdDelete**](docs/Api/KeywordAdminApi.md#keywordadminiddelete) | **DELETE** /keyword/admin/{id} | Delete keyword
*KeywordAdminApi* | [**keywordAdminIdGet**](docs/Api/KeywordAdminApi.md#keywordadminidget) | **GET** /keyword/admin/{id} | Get keyword
*KeywordAdminApi* | [**keywordAdminIdPatch**](docs/Api/KeywordAdminApi.md#keywordadminidpatch) | **PATCH** /keyword/admin/{id} | Update keyword
*KeywordAdminApi* | [**keywordAdminPost**](docs/Api/KeywordAdminApi.md#keywordadminpost) | **POST** /keyword/admin | Create keyword
*KeywordDefaultApi* | [**keywordDefaultCategoryGet**](docs/Api/KeywordDefaultApi.md#keyworddefaultcategoryget) | **GET** /keyword/default/category | Get keyword category list
*KeywordDefaultApi* | [**keywordDefaultCategoryIdGet**](docs/Api/KeywordDefaultApi.md#keyworddefaultcategoryidget) | **GET** /keyword/default/category/{id} | Get keyword category
*KeywordDefaultApi* | [**keywordDefaultGet**](docs/Api/KeywordDefaultApi.md#keyworddefaultget) | **GET** /keyword/default | Get keyword list
*LegalAdminApi* | [**configAdminLegalGet**](docs/Api/LegalAdminApi.md#configadminlegalget) | **GET** /config/admin/legal | Get legal
*LegalAdminApi* | [**configAdminLegalImprintGet**](docs/Api/LegalAdminApi.md#configadminlegalimprintget) | **GET** /config/admin/legal/imprint | Get imprint
*LegalAdminApi* | [**configAdminLegalImprintPut**](docs/Api/LegalAdminApi.md#configadminlegalimprintput) | **PUT** /config/admin/legal/imprint | Update imprint
*LegalAdminApi* | [**configAdminLegalPatch**](docs/Api/LegalAdminApi.md#configadminlegalpatch) | **PATCH** /config/admin/legal | Update legal
*LegalAdminApi* | [**configAdminLegalPolicyGet**](docs/Api/LegalAdminApi.md#configadminlegalpolicyget) | **GET** /config/admin/legal/policy | Get policy
*LegalAdminApi* | [**configAdminLegalPolicyPut**](docs/Api/LegalAdminApi.md#configadminlegalpolicyput) | **PUT** /config/admin/legal/policy | Update policy
*LegalAdminApi* | [**configAdminLegalTermsGet**](docs/Api/LegalAdminApi.md#configadminlegaltermsget) | **GET** /config/admin/legal/terms | Get terms
*LegalAdminApi* | [**configAdminLegalTermsPut**](docs/Api/LegalAdminApi.md#configadminlegaltermsput) | **PUT** /config/admin/legal/terms | Update terms
*LegalDefaultApi* | [**configDefaultLegalGet**](docs/Api/LegalDefaultApi.md#configdefaultlegalget) | **GET** /config/default/legal | Get legal
*LegalDefaultApi* | [**configDefaultLegalImprintGet**](docs/Api/LegalDefaultApi.md#configdefaultlegalimprintget) | **GET** /config/default/legal/imprint | Get imprint
*LegalDefaultApi* | [**configDefaultLegalPolicyGet**](docs/Api/LegalDefaultApi.md#configdefaultlegalpolicyget) | **GET** /config/default/legal/policy | Get policy
*LegalDefaultApi* | [**configDefaultLegalTermsGet**](docs/Api/LegalDefaultApi.md#configdefaultlegaltermsget) | **GET** /config/default/legal/terms | Get terms
*LegalDefaultApi* | [**configDefaultLegalTrackingGet**](docs/Api/LegalDefaultApi.md#configdefaultlegaltrackingget) | **GET** /config/default/legal/tracking | Get tracking legal
*LocationAdminApi* | [**locationAdminIdAccessGet**](docs/Api/LocationAdminApi.md#locationadminidaccessget) | **GET** /location/admin/{id}/access | Get location access configuration
*LocationAdminApi* | [**locationAdminIdAccessPatch**](docs/Api/LocationAdminApi.md#locationadminidaccesspatch) | **PATCH** /location/admin/{id}/access | Update location access configuration
*LocationAdminApi* | [**locationAdminIdDelete**](docs/Api/LocationAdminApi.md#locationadminiddelete) | **DELETE** /location/admin/{id} | Delete location
*LocationAdminApi* | [**locationAdminIdGet**](docs/Api/LocationAdminApi.md#locationadminidget) | **GET** /location/admin/{id} | Get location
*LocationAdminApi* | [**locationAdminIdPatch**](docs/Api/LocationAdminApi.md#locationadminidpatch) | **PATCH** /location/admin/{id} | Update location
*LocationAdminApi* | [**locationAdminPost**](docs/Api/LocationAdminApi.md#locationadminpost) | **POST** /location/admin | Create location
*LocationAdminApi* | [**locationAdminProjectIdGet**](docs/Api/LocationAdminApi.md#locationadminprojectidget) | **GET** /location/admin/project/{id} | Get location list for project
*LocationDefaultApi* | [**locationDefaultIdGet**](docs/Api/LocationDefaultApi.md#locationdefaultidget) | **GET** /location/default/{id} | Get location
*LocationDefaultApi* | [**locationDefaultProjectIdGet**](docs/Api/LocationDefaultApi.md#locationdefaultprojectidget) | **GET** /location/default/project/{id} | Get location list for project
*MapAdminApi* | [**locationAdminMapIdAccessGet**](docs/Api/MapAdminApi.md#locationadminmapidaccessget) | **GET** /location/admin/map/{id}/access | Get map access configuration
*MapAdminApi* | [**locationAdminMapIdAccessPatch**](docs/Api/MapAdminApi.md#locationadminmapidaccesspatch) | **PATCH** /location/admin/map/{id}/access | Update map access configuration
*MapAdminApi* | [**locationAdminMapIdDelete**](docs/Api/MapAdminApi.md#locationadminmapiddelete) | **DELETE** /location/admin/map/{id} | Delete map
*MapAdminApi* | [**locationAdminMapIdGet**](docs/Api/MapAdminApi.md#locationadminmapidget) | **GET** /location/admin/map/{id} | Get map
*MapAdminApi* | [**locationAdminMapIdPatch**](docs/Api/MapAdminApi.md#locationadminmapidpatch) | **PATCH** /location/admin/map/{id} | Update map
*MapAdminApi* | [**locationAdminMapPost**](docs/Api/MapAdminApi.md#locationadminmappost) | **POST** /location/admin/map | Create map
*MapAdminApi* | [**locationAdminMapProjectIdGet**](docs/Api/MapAdminApi.md#locationadminmapprojectidget) | **GET** /location/admin/map/project/{id} | Get map list for project
*MapDefaultApi* | [**locationDefaultMapIdGet**](docs/Api/MapDefaultApi.md#locationdefaultmapidget) | **GET** /location/default/map/{id} | Get map
*MediaAdminApi* | [**configAdminMediaDefaultGet**](docs/Api/MediaAdminApi.md#configadminmediadefaultget) | **GET** /config/admin/media/default | Get factory default media configuration
*MediaAdminApi* | [**configAdminMediaGet**](docs/Api/MediaAdminApi.md#configadminmediaget) | **GET** /config/admin/media | Get media configuration
*MediaAdminApi* | [**configAdminMediaPatch**](docs/Api/MediaAdminApi.md#configadminmediapatch) | **PATCH** /config/admin/media | Update media configuration
*MediaAdminApi* | [**mediaAdminFolderGet**](docs/Api/MediaAdminApi.md#mediaadminfolderget) | **GET** /media/admin/folder | Get folder list
*MediaAdminApi* | [**mediaAdminFolderIdDelete**](docs/Api/MediaAdminApi.md#mediaadminfolderiddelete) | **DELETE** /media/admin/folder/{id} | Delete folder
*MediaAdminApi* | [**mediaAdminFolderIdGet**](docs/Api/MediaAdminApi.md#mediaadminfolderidget) | **GET** /media/admin/folder/{id} | Get folder
*MediaAdminApi* | [**mediaAdminFolderIdPatch**](docs/Api/MediaAdminApi.md#mediaadminfolderidpatch) | **PATCH** /media/admin/folder/{id} | Update folder
*MediaAdminApi* | [**mediaAdminFolderPost**](docs/Api/MediaAdminApi.md#mediaadminfolderpost) | **POST** /media/admin/folder | Create folder
*MediaAdminApi* | [**mediaAdminGet**](docs/Api/MediaAdminApi.md#mediaadminget) | **GET** /media/admin | Get media items list
*MediaAdminApi* | [**mediaAdminIdAccessGet**](docs/Api/MediaAdminApi.md#mediaadminidaccessget) | **GET** /media/admin/{id}/access | Get media item access configuration
*MediaAdminApi* | [**mediaAdminIdAccessPatch**](docs/Api/MediaAdminApi.md#mediaadminidaccesspatch) | **PATCH** /media/admin/{id}/access | Update media item access configuration
*MediaAdminApi* | [**mediaAdminIdDelete**](docs/Api/MediaAdminApi.md#mediaadminiddelete) | **DELETE** /media/admin/{id} | Delete media item and file
*MediaAdminApi* | [**mediaAdminIdDuplicatePost**](docs/Api/MediaAdminApi.md#mediaadminidduplicatepost) | **POST** /media/admin/{id}/duplicate | Duplicate media item and file
*MediaAdminApi* | [**mediaAdminIdFileGet**](docs/Api/MediaAdminApi.md#mediaadminidfileget) | **GET** /media/admin/{id}/file | Get file
*MediaAdminApi* | [**mediaAdminIdFilePut**](docs/Api/MediaAdminApi.md#mediaadminidfileput) | **PUT** /media/admin/{id}/file | Update file
*MediaAdminApi* | [**mediaAdminIdGet**](docs/Api/MediaAdminApi.md#mediaadminidget) | **GET** /media/admin/{id} | Get media item
*MediaAdminApi* | [**mediaAdminIdPatch**](docs/Api/MediaAdminApi.md#mediaadminidpatch) | **PATCH** /media/admin/{id} | Update media item metadata
*MediaAdminApi* | [**mediaAdminIdPermalinkGet**](docs/Api/MediaAdminApi.md#mediaadminidpermalinkget) | **GET** /media/admin/{id}/permalink | Get permalink
*MediaAdminApi* | [**mediaAdminIdThumbnailGet**](docs/Api/MediaAdminApi.md#mediaadminidthumbnailget) | **GET** /media/admin/{id}/thumbnail | Get thumbnail
*MediaAdminApi* | [**mediaAdminPost**](docs/Api/MediaAdminApi.md#mediaadminpost) | **POST** /media/admin | Upload file &amp; create media item
*MediaAdminApi* | [**mediaAdminSearchPost**](docs/Api/MediaAdminApi.md#mediaadminsearchpost) | **POST** /media/admin/search | Create cursor
*MediaDefaultApi* | [**configDefaultMediaGet**](docs/Api/MediaDefaultApi.md#configdefaultmediaget) | **GET** /config/default/media | Get media configuration
*MediaDefaultApi* | [**mediaDefaultDownloadGet**](docs/Api/MediaDefaultApi.md#mediadefaultdownloadget) | **GET** /media/default/download | Download media items
*MediaDefaultApi* | [**mediaDefaultDownloadIdGet**](docs/Api/MediaDefaultApi.md#mediadefaultdownloadidget) | **GET** /media/default/download/{id} | Get download status
*MediaDefaultApi* | [**mediaDefaultFolderIdContentGet**](docs/Api/MediaDefaultApi.md#mediadefaultfolderidcontentget) | **GET** /media/default/folder/{id}/content | Get media items list of folder
*MediaDefaultApi* | [**mediaDefaultGet**](docs/Api/MediaDefaultApi.md#mediadefaultget) | **GET** /media/default | Get media items list
*MediaDefaultApi* | [**mediaDefaultIdDelete**](docs/Api/MediaDefaultApi.md#mediadefaultiddelete) | **DELETE** /media/default/{id} | Delete media item and file
*MediaDefaultApi* | [**mediaDefaultIdFileGet**](docs/Api/MediaDefaultApi.md#mediadefaultidfileget) | **GET** /media/default/{id}/file | Get file
*MediaDefaultApi* | [**mediaDefaultIdFilePut**](docs/Api/MediaDefaultApi.md#mediadefaultidfileput) | **PUT** /media/default/{id}/file | Update file
*MediaDefaultApi* | [**mediaDefaultIdGet**](docs/Api/MediaDefaultApi.md#mediadefaultidget) | **GET** /media/default/{id} | Get media item
*MediaDefaultApi* | [**mediaDefaultIdPatch**](docs/Api/MediaDefaultApi.md#mediadefaultidpatch) | **PATCH** /media/default/{id} | Update media item metadata
*MediaDefaultApi* | [**mediaDefaultIdThumbnailGet**](docs/Api/MediaDefaultApi.md#mediadefaultidthumbnailget) | **GET** /media/default/{id}/thumbnail | Get thumbnail
*MediaDefaultApi* | [**mediaDefaultIdsGet**](docs/Api/MediaDefaultApi.md#mediadefaultidsget) | **GET** /media/default/ids | Get media item ids
*MediaDefaultApi* | [**mediaDefaultPost**](docs/Api/MediaDefaultApi.md#mediadefaultpost) | **POST** /media/default | Upload file &amp; create media item
*MediaDefaultApi* | [**mediaDefaultSearchPost**](docs/Api/MediaDefaultApi.md#mediadefaultsearchpost) | **POST** /media/default/search | Create cursor
*MenuAdminApi* | [**menuAdminProjectIdAccessGet**](docs/Api/MenuAdminApi.md#menuadminprojectidaccessget) | **GET** /menu/admin/project/{id}/access | Get menu access configuration
*MenuAdminApi* | [**menuAdminProjectIdAccessPatch**](docs/Api/MenuAdminApi.md#menuadminprojectidaccesspatch) | **PATCH** /menu/admin/project/{id}/access | Update menu access configuration
*MenuAdminApi* | [**menuAdminProjectIdContentGet**](docs/Api/MenuAdminApi.md#menuadminprojectidcontentget) | **GET** /menu/admin/project/{id}/content | Get menu content
*MenuAdminApi* | [**menuAdminProjectIdContentPut**](docs/Api/MenuAdminApi.md#menuadminprojectidcontentput) | **PUT** /menu/admin/project/{id}/content | Update menu content
*MenuAdminApi* | [**menuAdminProjectIdGet**](docs/Api/MenuAdminApi.md#menuadminprojectidget) | **GET** /menu/admin/project/{id} | Get menu for project
*MenuAdminApi* | [**menuAdminProjectIdPost**](docs/Api/MenuAdminApi.md#menuadminprojectidpost) | **POST** /menu/admin/project/{id} | Create menu for project
*MenuAdminApi* | [**menuAdminProjectIdSettingsGet**](docs/Api/MenuAdminApi.md#menuadminprojectidsettingsget) | **GET** /menu/admin/project/{id}/settings | Get menu settings
*MenuAdminApi* | [**menuAdminProjectIdSettingsPut**](docs/Api/MenuAdminApi.md#menuadminprojectidsettingsput) | **PUT** /menu/admin/project/{id}/settings | Update menu settings
*MenuDefaultApi* | [**menuDefaultProjectIdGet**](docs/Api/MenuDefaultApi.md#menudefaultprojectidget) | **GET** /menu/default/project/{id} | Get menu for project
*NewsAdminApi* | [**newsAdminGet**](docs/Api/NewsAdminApi.md#newsadminget) | **GET** /news/admin | Get article list for cursor
*NewsAdminApi* | [**newsAdminIdAccessGet**](docs/Api/NewsAdminApi.md#newsadminidaccessget) | **GET** /news/admin/{id}/access | Get article access configuration
*NewsAdminApi* | [**newsAdminIdAccessPatch**](docs/Api/NewsAdminApi.md#newsadminidaccesspatch) | **PATCH** /news/admin/{id}/access | Update article access configuration
*NewsAdminApi* | [**newsAdminIdContentDesktopDelete**](docs/Api/NewsAdminApi.md#newsadminidcontentdesktopdelete) | **DELETE** /news/admin/{id}/content/desktop | Delete article desktop version
*NewsAdminApi* | [**newsAdminIdContentDesktopGet**](docs/Api/NewsAdminApi.md#newsadminidcontentdesktopget) | **GET** /news/admin/{id}/content/desktop | Get article desktop content
*NewsAdminApi* | [**newsAdminIdContentDesktopPut**](docs/Api/NewsAdminApi.md#newsadminidcontentdesktopput) | **PUT** /news/admin/{id}/content/desktop | Update article desktop content
*NewsAdminApi* | [**newsAdminIdContentGet**](docs/Api/NewsAdminApi.md#newsadminidcontentget) | **GET** /news/admin/{id}/content | Get article mobile content
*NewsAdminApi* | [**newsAdminIdContentPut**](docs/Api/NewsAdminApi.md#newsadminidcontentput) | **PUT** /news/admin/{id}/content | Update article mobile content
*NewsAdminApi* | [**newsAdminIdDelete**](docs/Api/NewsAdminApi.md#newsadminiddelete) | **DELETE** /news/admin/{id} | Delete article
*NewsAdminApi* | [**newsAdminIdGet**](docs/Api/NewsAdminApi.md#newsadminidget) | **GET** /news/admin/{id} | Get article mobile
*NewsAdminApi* | [**newsAdminIdPatch**](docs/Api/NewsAdminApi.md#newsadminidpatch) | **PATCH** /news/admin/{id} | Update article info
*NewsAdminApi* | [**newsAdminIdSettingsGet**](docs/Api/NewsAdminApi.md#newsadminidsettingsget) | **GET** /news/admin/{id}/settings | Get article settings
*NewsAdminApi* | [**newsAdminIdSettingsPut**](docs/Api/NewsAdminApi.md#newsadminidsettingsput) | **PUT** /news/admin/{id}/settings | Update article settings
*NewsAdminApi* | [**newsAdminPost**](docs/Api/NewsAdminApi.md#newsadminpost) | **POST** /news/admin | Create article
*NewsAdminApi* | [**newsAdminPostCountProjectIdGet**](docs/Api/NewsAdminApi.md#newsadminpostcountprojectidget) | **GET** /news/admin/post-count/project/{id} | Get article post counts for project
*NewsAdminApi* | [**newsAdminProjectIdGet**](docs/Api/NewsAdminApi.md#newsadminprojectidget) | **GET** /news/admin/project/{id} | Get article list for project
*NewsAdminApi* | [**newsAdminSearchPost**](docs/Api/NewsAdminApi.md#newsadminsearchpost) | **POST** /news/admin/search | Create cursor
*NewsAdminApi* | [**newsAdminSyncPut**](docs/Api/NewsAdminApi.md#newsadminsyncput) | **PUT** /news/admin/sync | Sync Operators for all articles
*NewsDefaultApi* | [**newsDefaultGet**](docs/Api/NewsDefaultApi.md#newsdefaultget) | **GET** /news/default | Get published article list for cursor
*NewsDefaultApi* | [**newsDefaultIdDesktopGet**](docs/Api/NewsDefaultApi.md#newsdefaultiddesktopget) | **GET** /news/default/{id}/desktop | Get article desktop
*NewsDefaultApi* | [**newsDefaultIdGet**](docs/Api/NewsDefaultApi.md#newsdefaultidget) | **GET** /news/default/{id} | Get article mobile
*NewsDefaultApi* | [**newsDefaultPostCountIdGet**](docs/Api/NewsDefaultApi.md#newsdefaultpostcountidget) | **GET** /news/default/post-count/{id} | Get article post count
*NewsDefaultApi* | [**newsDefaultPostCountProjectIdGet**](docs/Api/NewsDefaultApi.md#newsdefaultpostcountprojectidget) | **GET** /news/default/post-count/project/{id} | Get article post counts for project
*NewsDefaultApi* | [**newsDefaultProjectIdGet**](docs/Api/NewsDefaultApi.md#newsdefaultprojectidget) | **GET** /news/default/project/{id} | Get published article list for project
*NewsDefaultApi* | [**newsDefaultProjectIdIdsGet**](docs/Api/NewsDefaultApi.md#newsdefaultprojectididsget) | **GET** /news/default/project/{id}/ids | Get published article ids for project
*NewsDefaultApi* | [**newsDefaultSearchPost**](docs/Api/NewsDefaultApi.md#newsdefaultsearchpost) | **POST** /news/default/search | Create cursor
*NotificationAdminApi* | [**configAdminNotificationCertificateInfoPost**](docs/Api/NotificationAdminApi.md#configadminnotificationcertificateinfopost) | **POST** /config/admin/notification/certificate/info | Get certificate info
*NotificationAdminApi* | [**configAdminNotificationGet**](docs/Api/NotificationAdminApi.md#configadminnotificationget) | **GET** /config/admin/notification | Get notification configuration
*NotificationAdminApi* | [**configAdminNotificationIosCertificateCsrGet**](docs/Api/NotificationAdminApi.md#configadminnotificationioscertificatecsrget) | **GET** /config/admin/notification/ios-certificate/csr | Create iOS push CSR
*NotificationAdminApi* | [**configAdminNotificationIosCertificatePut**](docs/Api/NotificationAdminApi.md#configadminnotificationioscertificateput) | **PUT** /config/admin/notification/ios-certificate | Update iOS push certificate
*NotificationAdminApi* | [**configAdminNotificationPatch**](docs/Api/NotificationAdminApi.md#configadminnotificationpatch) | **PATCH** /config/admin/notification | Update notification configuration
*NotificationAdminApi* | [**configAdminNotificationSafariCertificateCsrGet**](docs/Api/NotificationAdminApi.md#configadminnotificationsafaricertificatecsrget) | **GET** /config/admin/notification/safari-certificate/csr | Create Safari push CSR
*NotificationAdminApi* | [**configAdminNotificationSafariCertificatePut**](docs/Api/NotificationAdminApi.md#configadminnotificationsafaricertificateput) | **PUT** /config/admin/notification/safari-certificate | Update Safari push certificate
*NotificationAdminApi* | [**notificationAdminIdDelete**](docs/Api/NotificationAdminApi.md#notificationadminiddelete) | **DELETE** /notification/admin/{id} | Delete notification
*NotificationAdminApi* | [**notificationAdminIdGet**](docs/Api/NotificationAdminApi.md#notificationadminidget) | **GET** /notification/admin/{id} | Get notification
*NotificationAdminApi* | [**notificationAdminIdPatch**](docs/Api/NotificationAdminApi.md#notificationadminidpatch) | **PATCH** /notification/admin/{id} | Update notification
*NotificationAdminApi* | [**notificationAdminPost**](docs/Api/NotificationAdminApi.md#notificationadminpost) | **POST** /notification/admin | Create notification
*NotificationAdminApi* | [**notificationAdminProjectIdGet**](docs/Api/NotificationAdminApi.md#notificationadminprojectidget) | **GET** /notification/admin/project/{id} | Get all project notifications
*NotificationDefaultApi* | [**notificationDefaultDelete**](docs/Api/NotificationDefaultApi.md#notificationdefaultdelete) | **DELETE** /notification/default | Delete account notifications
*NotificationDefaultApi* | [**notificationDefaultGet**](docs/Api/NotificationDefaultApi.md#notificationdefaultget) | **GET** /notification/default | Get all account notifications
*NotificationDefaultApi* | [**notificationDefaultIdDelete**](docs/Api/NotificationDefaultApi.md#notificationdefaultiddelete) | **DELETE** /notification/default/{id} | Delete account notification
*NotificationDefaultApi* | [**notificationDefaultIdGet**](docs/Api/NotificationDefaultApi.md#notificationdefaultidget) | **GET** /notification/default/{id} | Get account notification
*NotificationDefaultApi* | [**notificationDefaultIdPut**](docs/Api/NotificationDefaultApi.md#notificationdefaultidput) | **PUT** /notification/default/{id} | Update account notification
*NotificationDefaultApi* | [**notificationDefaultReadAllPut**](docs/Api/NotificationDefaultApi.md#notificationdefaultreadallput) | **PUT** /notification/default/read-all | Read all account notifications
*NotificationDefaultApi* | [**notificationDefaultReadPut**](docs/Api/NotificationDefaultApi.md#notificationdefaultreadput) | **PUT** /notification/default/read | Read account notifications
*NotificationDefaultApi* | [**notificationDefaultSafariGet**](docs/Api/NotificationDefaultApi.md#notificationdefaultsafariget) | **GET** /notification/default/safari | Get safari settings
*NotificationDefaultApi* | [**notificationDefaultUnreadPut**](docs/Api/NotificationDefaultApi.md#notificationdefaultunreadput) | **PUT** /notification/default/unread | Unread account notifications
*NotificationDefaultApi* | [**notificationDefaultVapidPublicGet**](docs/Api/NotificationDefaultApi.md#notificationdefaultvapidpublicget) | **GET** /notification/default/vapid/public | Get vapid public key
*NotificationJobAdminApi* | [**notificationAdminJobGet**](docs/Api/NotificationJobAdminApi.md#notificationadminjobget) | **GET** /notification/admin/job | Get job list for project
*NotificationJobAdminApi* | [**notificationAdminJobIdDefaultGet**](docs/Api/NotificationJobAdminApi.md#notificationadminjobiddefaultget) | **GET** /notification/admin/job/{id}/default | Get default job
*NotificationJobAdminApi* | [**notificationAdminJobIdDelete**](docs/Api/NotificationJobAdminApi.md#notificationadminjobiddelete) | **DELETE** /notification/admin/job/{id} | Delete Notification Job
*NotificationJobAdminApi* | [**notificationAdminJobIdGet**](docs/Api/NotificationJobAdminApi.md#notificationadminjobidget) | **GET** /notification/admin/job/{id} | Get job
*NotificationJobAdminApi* | [**notificationAdminJobIdPatch**](docs/Api/NotificationJobAdminApi.md#notificationadminjobidpatch) | **PATCH** /notification/admin/job/{id} | Update job
*NotificationJobAdminApi* | [**notificationAdminJobPost**](docs/Api/NotificationJobAdminApi.md#notificationadminjobpost) | **POST** /notification/admin/job | Create job
*NotificationJobAdminApi* | [**notificationAdminJobTestPost**](docs/Api/NotificationJobAdminApi.md#notificationadminjobtestpost) | **POST** /notification/admin/job/test | Test job content
*OneTimeTokenApi* | [**authOttValidatePost**](docs/Api/OneTimeTokenApi.md#authottvalidatepost) | **POST** /auth/ott/validate | Validate one time token
*PageAdminApi* | [**pageAdminIdAccessGet**](docs/Api/PageAdminApi.md#pageadminidaccessget) | **GET** /page/admin/{id}/access | Get page access configuration
*PageAdminApi* | [**pageAdminIdAccessPatch**](docs/Api/PageAdminApi.md#pageadminidaccesspatch) | **PATCH** /page/admin/{id}/access | Update page access configuration
*PageAdminApi* | [**pageAdminIdContentDesktopDelete**](docs/Api/PageAdminApi.md#pageadminidcontentdesktopdelete) | **DELETE** /page/admin/{id}/content/desktop | Delete desktop content
*PageAdminApi* | [**pageAdminIdContentDesktopGet**](docs/Api/PageAdminApi.md#pageadminidcontentdesktopget) | **GET** /page/admin/{id}/content/desktop | Get page desktop content
*PageAdminApi* | [**pageAdminIdContentDesktopPut**](docs/Api/PageAdminApi.md#pageadminidcontentdesktopput) | **PUT** /page/admin/{id}/content/desktop | Update page desktop content
*PageAdminApi* | [**pageAdminIdContentGet**](docs/Api/PageAdminApi.md#pageadminidcontentget) | **GET** /page/admin/{id}/content | Get page mobile content
*PageAdminApi* | [**pageAdminIdContentPut**](docs/Api/PageAdminApi.md#pageadminidcontentput) | **PUT** /page/admin/{id}/content | Update page mobile content
*PageAdminApi* | [**pageAdminIdDelete**](docs/Api/PageAdminApi.md#pageadminiddelete) | **DELETE** /page/admin/{id} | Delete page
*PageAdminApi* | [**pageAdminIdDesktopGet**](docs/Api/PageAdminApi.md#pageadminiddesktopget) | **GET** /page/admin/{id}/desktop | Get page desktop content
*PageAdminApi* | [**pageAdminIdGet**](docs/Api/PageAdminApi.md#pageadminidget) | **GET** /page/admin/{id} | Get page
*PageAdminApi* | [**pageAdminIdPatch**](docs/Api/PageAdminApi.md#pageadminidpatch) | **PATCH** /page/admin/{id} | Update page
*PageAdminApi* | [**pageAdminIdSettingsGet**](docs/Api/PageAdminApi.md#pageadminidsettingsget) | **GET** /page/admin/{id}/settings | Get page settings
*PageAdminApi* | [**pageAdminIdSettingsPut**](docs/Api/PageAdminApi.md#pageadminidsettingsput) | **PUT** /page/admin/{id}/settings | Update page settings
*PageAdminApi* | [**pageAdminPost**](docs/Api/PageAdminApi.md#pageadminpost) | **POST** /page/admin | Create page
*PageAdminApi* | [**pageAdminPostCountProjectIdGet**](docs/Api/PageAdminApi.md#pageadminpostcountprojectidget) | **GET** /page/admin/post-count/project/{id} | Get page post counts for project
*PageAdminApi* | [**pageAdminProjectIdGet**](docs/Api/PageAdminApi.md#pageadminprojectidget) | **GET** /page/admin/project/{id} | Get page list for project
*PageAdminApi* | [**pageAdminSyncPut**](docs/Api/PageAdminApi.md#pageadminsyncput) | **PUT** /page/admin/sync | Sync Operators for all pages
*PageDefaultApi* | [**pageDefaultIdDesktopGet**](docs/Api/PageDefaultApi.md#pagedefaultiddesktopget) | **GET** /page/default/{id}/desktop | Get page desktop content
*PageDefaultApi* | [**pageDefaultIdGet**](docs/Api/PageDefaultApi.md#pagedefaultidget) | **GET** /page/default/{id} | Get page
*PageDefaultApi* | [**pageDefaultPostCountIdGet**](docs/Api/PageDefaultApi.md#pagedefaultpostcountidget) | **GET** /page/default/post-count/{id} | Get page post count
*PageDefaultApi* | [**pageDefaultPostCountProjectIdGet**](docs/Api/PageDefaultApi.md#pagedefaultpostcountprojectidget) | **GET** /page/default/post-count/project/{id} | Get page post counts for project
*PartyAdminApi* | [**partyAdminGet**](docs/Api/PartyAdminApi.md#partyadminget) | **GET** /party/admin | Get party list for cursor
*PartyAdminApi* | [**partyAdminIdConfigPut**](docs/Api/PartyAdminApi.md#partyadminidconfigput) | **PUT** /party/admin/{id}/config | Update party configuration
*PartyAdminApi* | [**partyAdminIdDelete**](docs/Api/PartyAdminApi.md#partyadminiddelete) | **DELETE** /party/admin/{id} | Delete party
*PartyAdminApi* | [**partyAdminIdGet**](docs/Api/PartyAdminApi.md#partyadminidget) | **GET** /party/admin/{id} | Get party
*PartyAdminApi* | [**partyAdminIdReactionPost**](docs/Api/PartyAdminApi.md#partyadminidreactionpost) | **POST** /party/admin/{id}/reaction | Create reaction
*PartyAdminApi* | [**partyAdminPost**](docs/Api/PartyAdminApi.md#partyadminpost) | **POST** /party/admin | Create party
*PartyAdminApi* | [**partyAdminReactionGet**](docs/Api/PartyAdminApi.md#partyadminreactionget) | **GET** /party/admin/reaction | Get reaction list for cursor
*PartyAdminApi* | [**partyAdminReactionIdDelete**](docs/Api/PartyAdminApi.md#partyadminreactioniddelete) | **DELETE** /party/admin/reaction/{id} | Delete reaction
*PartyAdminApi* | [**partyAdminReactionIdGet**](docs/Api/PartyAdminApi.md#partyadminreactionidget) | **GET** /party/admin/reaction/{id} | Get reaction
*PartyAdminApi* | [**partyAdminReactionIdPut**](docs/Api/PartyAdminApi.md#partyadminreactionidput) | **PUT** /party/admin/reaction/{id} | Update reaction
*PartyAdminApi* | [**partyAdminReactionSearchPost**](docs/Api/PartyAdminApi.md#partyadminreactionsearchpost) | **POST** /party/admin/reaction/search | Create cursor
*PartyAdminApi* | [**partyAdminSearchPost**](docs/Api/PartyAdminApi.md#partyadminsearchpost) | **POST** /party/admin/search | Create cursor
*PartyDefaultApi* | [**partyDefaultGet**](docs/Api/PartyDefaultApi.md#partydefaultget) | **GET** /party/default | Get party list for cursor
*PartyDefaultApi* | [**partyDefaultIdReactionGet**](docs/Api/PartyDefaultApi.md#partydefaultidreactionget) | **GET** /party/default/{id}/reaction | Get reaction
*PartyDefaultApi* | [**partyDefaultIdReactionPut**](docs/Api/PartyDefaultApi.md#partydefaultidreactionput) | **PUT** /party/default/{id}/reaction | Set reaction
*PartyDefaultApi* | [**partyDefaultObjectTypeObjectIdGet**](docs/Api/PartyDefaultApi.md#partydefaultobjecttypeobjectidget) | **GET** /party/default/{objectType}/{objectId} | Get party
*PartyDefaultApi* | [**partyDefaultObjectTypeReferenceObjectIdGet**](docs/Api/PartyDefaultApi.md#partydefaultobjecttypereferenceobjectidget) | **GET** /party/default/{objectType}/reference/{objectId} | Get parties for reference
*PartyDefaultApi* | [**partyDefaultReactionGet**](docs/Api/PartyDefaultApi.md#partydefaultreactionget) | **GET** /party/default/reaction | Get reaction list for cursor
*PartyDefaultApi* | [**partyDefaultReactionSearchPost**](docs/Api/PartyDefaultApi.md#partydefaultreactionsearchpost) | **POST** /party/default/reaction/search | Create cursor
*PartyDefaultApi* | [**partyDefaultSearchPost**](docs/Api/PartyDefaultApi.md#partydefaultsearchpost) | **POST** /party/default/search | Create cursor
*PermissionApi* | [**authPermissionGet**](docs/Api/PermissionApi.md#authpermissionget) | **GET** /auth/permission | List permissions
*PermissionApi* | [**authPermissionPermissionGet**](docs/Api/PermissionApi.md#authpermissionpermissionget) | **GET** /auth/permission/{permission} | Check permission existence
*ProjectApi* | [**projectDefaultIdGuestVisitPut**](docs/Api/ProjectApi.md#projectdefaultidguestvisitput) | **PUT** /project/default/{id}/guest-visit | guest visit
*ProjectAdminApi* | [**projectAdminCopyGet**](docs/Api/ProjectAdminApi.md#projectadmincopyget) | **GET** /project/admin/copy | Get project copy processes
*ProjectAdminApi* | [**projectAdminCopyIdGet**](docs/Api/ProjectAdminApi.md#projectadmincopyidget) | **GET** /project/admin/copy/{id} | Get project copy process
*ProjectAdminApi* | [**projectAdminGet**](docs/Api/ProjectAdminApi.md#projectadminget) | **GET** /project/admin | Get project list
*ProjectAdminApi* | [**projectAdminIdAccessGet**](docs/Api/ProjectAdminApi.md#projectadminidaccessget) | **GET** /project/admin/{id}/access | Get project access configuration
*ProjectAdminApi* | [**projectAdminIdAccessPatch**](docs/Api/ProjectAdminApi.md#projectadminidaccesspatch) | **PATCH** /project/admin/{id}/access | Update project access configuration
*ProjectAdminApi* | [**projectAdminIdCopyPost**](docs/Api/ProjectAdminApi.md#projectadminidcopypost) | **POST** /project/admin/{id}/copy | Duplicate project
*ProjectAdminApi* | [**projectAdminIdDelete**](docs/Api/ProjectAdminApi.md#projectadminiddelete) | **DELETE** /project/admin/{id} | Delete project
*ProjectAdminApi* | [**projectAdminIdGet**](docs/Api/ProjectAdminApi.md#projectadminidget) | **GET** /project/admin/{id} | Get project
*ProjectAdminApi* | [**projectAdminIdPatch**](docs/Api/ProjectAdminApi.md#projectadminidpatch) | **PATCH** /project/admin/{id} | Update project
*ProjectAdminApi* | [**projectAdminIdSettingsGet**](docs/Api/ProjectAdminApi.md#projectadminidsettingsget) | **GET** /project/admin/{id}/settings | Get project settings
*ProjectAdminApi* | [**projectAdminIdSettingsTrackingGet**](docs/Api/ProjectAdminApi.md#projectadminidsettingstrackingget) | **GET** /project/admin/{id}/settings/tracking | Get project tracking settings
*ProjectAdminApi* | [**projectAdminIdSettingsTrackingPatch**](docs/Api/ProjectAdminApi.md#projectadminidsettingstrackingpatch) | **PATCH** /project/admin/{id}/settings/tracking | Update project tracking settings
*ProjectAdminApi* | [**projectAdminPost**](docs/Api/ProjectAdminApi.md#projectadminpost) | **POST** /project/admin | Create project
*ProjectDefaultApi* | [**projectDefaultGet**](docs/Api/ProjectDefaultApi.md#projectdefaultget) | **GET** /project/default | Get published project list
*ProjectDefaultApi* | [**projectDefaultIdGet**](docs/Api/ProjectDefaultApi.md#projectdefaultidget) | **GET** /project/default/{id} | Get project
*ReactionAdminApi* | [**reactionAdminObjectTypeGet**](docs/Api/ReactionAdminApi.md#reactionadminobjecttypeget) | **GET** /reaction/admin/{objectType} | Get reactions of type
*ReactionAdminApi* | [**reactionAdminObjectTypeSearchPost**](docs/Api/ReactionAdminApi.md#reactionadminobjecttypesearchpost) | **POST** /reaction/admin/{objectType}/search | Create cursor
*ReactionDefaultApi* | [**reactionDefaultBookmarkGet**](docs/Api/ReactionDefaultApi.md#reactiondefaultbookmarkget) | **GET** /reaction/default/bookmark | Get bookmarks for current user
*ReactionDefaultApi* | [**reactionDefaultBookmarkObjectTypeGet**](docs/Api/ReactionDefaultApi.md#reactiondefaultbookmarkobjecttypeget) | **GET** /reaction/default/bookmark/{objectType} | Get bookmarks for object type
*ReactionDefaultApi* | [**reactionDefaultBookmarkObjectTypeObjectIdDelete**](docs/Api/ReactionDefaultApi.md#reactiondefaultbookmarkobjecttypeobjectiddelete) | **DELETE** /reaction/default/bookmark/{objectType}/{objectId} | Delete a bookmark
*ReactionDefaultApi* | [**reactionDefaultBookmarkObjectTypeObjectIdGet**](docs/Api/ReactionDefaultApi.md#reactiondefaultbookmarkobjecttypeobjectidget) | **GET** /reaction/default/bookmark/{objectType}/{objectId} | Get bookmark of object for your account
*ReactionDefaultApi* | [**reactionDefaultBookmarkObjectTypeObjectIdPost**](docs/Api/ReactionDefaultApi.md#reactiondefaultbookmarkobjecttypeobjectidpost) | **POST** /reaction/default/bookmark/{objectType}/{objectId} | Create a bookmark
*ReactionDefaultApi* | [**reactionDefaultObjectTypeGet**](docs/Api/ReactionDefaultApi.md#reactiondefaultobjecttypeget) | **GET** /reaction/default/{objectType} | Get reactions of type
*ReactionDefaultApi* | [**reactionDefaultObjectTypeObjectIdDelete**](docs/Api/ReactionDefaultApi.md#reactiondefaultobjecttypeobjectiddelete) | **DELETE** /reaction/default/{objectType}/{objectId} | Delete your reaction
*ReactionDefaultApi* | [**reactionDefaultObjectTypeObjectIdGet**](docs/Api/ReactionDefaultApi.md#reactiondefaultobjecttypeobjectidget) | **GET** /reaction/default/{objectType}/{objectId} | Get reactions of object
*ReactionDefaultApi* | [**reactionDefaultObjectTypeObjectIdPost**](docs/Api/ReactionDefaultApi.md#reactiondefaultobjecttypeobjectidpost) | **POST** /reaction/default/{objectType}/{objectId} | Create or update your reaction
*ReactionDefaultApi* | [**reactionDefaultObjectTypeSearchPost**](docs/Api/ReactionDefaultApi.md#reactiondefaultobjecttypesearchpost) | **POST** /reaction/default/{objectType}/search | Create cursor
*RoleApi* | [**authRoleAllowedToSetGet**](docs/Api/RoleApi.md#authroleallowedtosetget) | **GET** /auth/role/allowed-to-set | Get roles allowed assigning
*RoleApi* | [**authRoleGet**](docs/Api/RoleApi.md#authroleget) | **GET** /auth/role | Get roles
*RoleApi* | [**authRoleIdDelete**](docs/Api/RoleApi.md#authroleiddelete) | **DELETE** /auth/role/{id} | Delete role
*RoleApi* | [**authRoleIdGet**](docs/Api/RoleApi.md#authroleidget) | **GET** /auth/role/{id} | Get role
*RoleApi* | [**authRoleIdPatch**](docs/Api/RoleApi.md#authroleidpatch) | **PATCH** /auth/role/{id} | Update role
*RoleApi* | [**authRolePost**](docs/Api/RoleApi.md#authrolepost) | **POST** /auth/role | Create role
*SSOAdminApi* | [**authAdminSsoProviderGet**](docs/Api/SSOAdminApi.md#authadminssoproviderget) | **GET** /auth/admin/sso-provider | Get all sso provider
*SSOAdminApi* | [**authAdminSsoProviderIdDelete**](docs/Api/SSOAdminApi.md#authadminssoprovideriddelete) | **DELETE** /auth/admin/sso-provider/{id} | Delete a sso provider
*SSOAdminApi* | [**authAdminSsoProviderIdGet**](docs/Api/SSOAdminApi.md#authadminssoprovideridget) | **GET** /auth/admin/sso-provider/{id} | Get a single sso provider
*SSOAdminApi* | [**authAdminSsoProviderIdPut**](docs/Api/SSOAdminApi.md#authadminssoprovideridput) | **PUT** /auth/admin/sso-provider/{id} | Update a sso provider
*SSOAdminApi* | [**authAdminSsoProviderPost**](docs/Api/SSOAdminApi.md#authadminssoproviderpost) | **POST** /auth/admin/sso-provider | Creates a sso provider
*SSODefaultApi* | [**authDefaultSsoProviderGet**](docs/Api/SSODefaultApi.md#authdefaultssoproviderget) | **GET** /auth/default/sso-provider | Get all published sso provider
*SSODefaultApi* | [**authSaml2IdGet**](docs/Api/SSODefaultApi.md#authsaml2idget) | **GET** /auth/Saml2/{id} | Start a saml2 auth flow
*SSODefaultApi* | [**authSaml2IdMetadataGet**](docs/Api/SSODefaultApi.md#authsaml2idmetadataget) | **GET** /auth/Saml2/{id}/metadata | Generates a metadata.xml file
*SSODefaultApi* | [**authSaml2IdResponsePost**](docs/Api/SSODefaultApi.md#authsaml2idresponsepost) | **POST** /auth/Saml2/{id}/response | Response endpoint of saml2 auth flow
*SSODefaultApi* | [**authSsoCodePost**](docs/Api/SSODefaultApi.md#authssocodepost) | **POST** /auth/sso-code | Create a session based on sso auth code
*SessionApi* | [**authLoginPost**](docs/Api/SessionApi.md#authloginpost) | **POST** /auth/login | Login
*SessionApi* | [**authLogoutGet**](docs/Api/SessionApi.md#authlogoutget) | **GET** /auth/logout | Logout
*SessionApi* | [**authSessionPost**](docs/Api/SessionApi.md#authsessionpost) | **POST** /auth/session | Refresh
*ShippingAdminApi* | [**shippingAdminAccountGet**](docs/Api/ShippingAdminApi.md#shippingadminaccountget) | **GET** /shipping/admin/Account | Get accounts shipping list
*ShippingAdminApi* | [**shippingAdminAccountIdGet**](docs/Api/ShippingAdminApi.md#shippingadminaccountidget) | **GET** /shipping/admin/Account/{id} | Get account shipping
*ShippingAdminApi* | [**shippingAdminAccountIdPost**](docs/Api/ShippingAdminApi.md#shippingadminaccountidpost) | **POST** /shipping/admin/Account/{id} | Add account shipping data
*ShippingAdminApi* | [**shippingAdminAccountIdPut**](docs/Api/ShippingAdminApi.md#shippingadminaccountidput) | **PUT** /shipping/admin/Account/{id} | Start account shipping process
*ShippingAdminApi* | [**shippingAdminAccountPost**](docs/Api/ShippingAdminApi.md#shippingadminaccountpost) | **POST** /shipping/admin/Account | Create account shipping
*ShippingAdminApi* | [**shippingAdminIdGet**](docs/Api/ShippingAdminApi.md#shippingadminidget) | **GET** /shipping/admin/{id} | Get shipping
*StreamAdminApi* | [**streamAdminIdAccessGet**](docs/Api/StreamAdminApi.md#streamadminidaccessget) | **GET** /stream/admin/{id}/access | Get stream access configuration
*StreamAdminApi* | [**streamAdminIdAccessPatch**](docs/Api/StreamAdminApi.md#streamadminidaccesspatch) | **PATCH** /stream/admin/{id}/access | Update stream access configuration
*StreamAdminApi* | [**streamAdminIdDelete**](docs/Api/StreamAdminApi.md#streamadminiddelete) | **DELETE** /stream/admin/{id} | Delete stream
*StreamAdminApi* | [**streamAdminIdGet**](docs/Api/StreamAdminApi.md#streamadminidget) | **GET** /stream/admin/{id} | Get stream
*StreamAdminApi* | [**streamAdminIdPatch**](docs/Api/StreamAdminApi.md#streamadminidpatch) | **PATCH** /stream/admin/{id} | Update stream
*StreamAdminApi* | [**streamAdminPost**](docs/Api/StreamAdminApi.md#streamadminpost) | **POST** /stream/admin | Create stream
*StreamAdminApi* | [**streamAdminProjectIdGet**](docs/Api/StreamAdminApi.md#streamadminprojectidget) | **GET** /stream/admin/project/{id} | Get stream list for project
*StreamDefaultApi* | [**streamDefaultIdGet**](docs/Api/StreamDefaultApi.md#streamdefaultidget) | **GET** /stream/default/{id} | Get stream
*StreamDefaultApi* | [**streamDefaultIdWatchGet**](docs/Api/StreamDefaultApi.md#streamdefaultidwatchget) | **GET** /stream/default/{id}/watch | Get stream viewer count
*StreamDefaultApi* | [**streamDefaultIdWatchPut**](docs/Api/StreamDefaultApi.md#streamdefaultidwatchput) | **PUT** /stream/default/{id}/watch | Set stream viewer
*UtilApi* | [**configCspPost**](docs/Api/UtilApi.md#configcsppost) | **POST** /config/csp | Check csp of url
*WebhookApi* | [**webhookGet**](docs/Api/WebhookApi.md#webhookget) | **GET** /webhook | Get all webhooks
*WebhookApi* | [**webhookIdCallPost**](docs/Api/WebhookApi.md#webhookidcallpost) | **POST** /webhook/{id}/call | Call webhook
*WebhookApi* | [**webhookIdDelete**](docs/Api/WebhookApi.md#webhookiddelete) | **DELETE** /webhook/{id} | Delete webhook
*WebhookApi* | [**webhookIdGet**](docs/Api/WebhookApi.md#webhookidget) | **GET** /webhook/{id} | Get webhook
*WebhookApi* | [**webhookIdLogsGet**](docs/Api/WebhookApi.md#webhookidlogsget) | **GET** /webhook/{id}/logs | Get webhook logs
*WebhookApi* | [**webhookIdPatch**](docs/Api/WebhookApi.md#webhookidpatch) | **PATCH** /webhook/{id} | Update webhook
*WebhookApi* | [**webhookPost**](docs/Api/WebhookApi.md#webhookpost) | **POST** /webhook | Create webhook

## Models

- [AccountCreateRequest](docs/Model/AccountCreateRequest.md)
- [AccountMetaAdmin](docs/Model/AccountMetaAdmin.md)
- [AccountMetaDataResponse](docs/Model/AccountMetaDataResponse.md)
- [AccountMetaDataTranslationResponse](docs/Model/AccountMetaDataTranslationResponse.md)
- [AccountMetaItem](docs/Model/AccountMetaItem.md)
- [AccountPatchCredentialsRequest](docs/Model/AccountPatchCredentialsRequest.md)
- [AccountPatchProfileRequest](docs/Model/AccountPatchProfileRequest.md)
- [AccountProfileResponse](docs/Model/AccountProfileResponse.md)
- [AccountProjectSettingsRequest](docs/Model/AccountProjectSettingsRequest.md)
- [AccountProjectStatsRecordResponse](docs/Model/AccountProjectStatsRecordResponse.md)
- [AccountProjectStatsRecordResponseSettings](docs/Model/AccountProjectStatsRecordResponseSettings.md)
- [AccountProjectStatsResponse](docs/Model/AccountProjectStatsResponse.md)
- [AccountPutMetaRequest](docs/Model/AccountPutMetaRequest.md)
- [AccountRegistrationRequest](docs/Model/AccountRegistrationRequest.md)
- [AccountRequestMetaSelection](docs/Model/AccountRequestMetaSelection.md)
- [AccountResponse](docs/Model/AccountResponse.md)
- [AccountSearch](docs/Model/AccountSearch.md)
- [AccountSettingsResponse](docs/Model/AccountSettingsResponse.md)
- [AccountStatsResponse](docs/Model/AccountStatsResponse.md)
- [AccountTrackingRequest](docs/Model/AccountTrackingRequest.md)
- [AccountTrackingResponse](docs/Model/AccountTrackingResponse.md)
- [AccountVisibilitySettingsRequest](docs/Model/AccountVisibilitySettingsRequest.md)
- [AccountVisibilitySettingsResponse](docs/Model/AccountVisibilitySettingsResponse.md)
- [AccountnotificationAccountNotification](docs/Model/AccountnotificationAccountNotification.md)
- [AnalyticsAccountSettingsRecord](docs/Model/AnalyticsAccountSettingsRecord.md)
- [AnalyticsCursorFilterOption](docs/Model/AnalyticsCursorFilterOption.md)
- [AnalyticsCursorRequest](docs/Model/AnalyticsCursorRequest.md)
- [AppointmentAllSlotsResponse](docs/Model/AppointmentAllSlotsResponse.md)
- [AppointmentAvailableSlotsResponse](docs/Model/AppointmentAvailableSlotsResponse.md)
- [AppointmentConfigPatchRequest](docs/Model/AppointmentConfigPatchRequest.md)
- [AppointmentConfigPostRequest](docs/Model/AppointmentConfigPostRequest.md)
- [AppointmentConfigResponse](docs/Model/AppointmentConfigResponse.md)
- [AppointmentCursorFilterOptionDefault](docs/Model/AppointmentCursorFilterOptionDefault.md)
- [AppointmentCursorRequestDefault](docs/Model/AppointmentCursorRequestDefault.md)
- [AppointmentDurationSlotResponse](docs/Model/AppointmentDurationSlotResponse.md)
- [AppointmentPostRequest](docs/Model/AppointmentPostRequest.md)
- [AppointmentResponse](docs/Model/AppointmentResponse.md)
- [AppointmentSlotFilter](docs/Model/AppointmentSlotFilter.md)
- [AppointmentSlotRequest](docs/Model/AppointmentSlotRequest.md)
- [AppointmentSlotSearchRequest](docs/Model/AppointmentSlotSearchRequest.md)
- [AuthAccountMetaGet200Response](docs/Model/AuthAccountMetaGet200Response.md)
- [AuthAuthenticationRequest](docs/Model/AuthAuthenticationRequest.md)
- [AuthAuthenticationResponse](docs/Model/AuthAuthenticationResponse.md)
- [AuthEmailChangeFirstRequest](docs/Model/AuthEmailChangeFirstRequest.md)
- [AuthEmailChangeRedeemTokenRequest](docs/Model/AuthEmailChangeRedeemTokenRequest.md)
- [AuthEmailChangeResponse](docs/Model/AuthEmailChangeResponse.md)
- [AuthLoginRequest](docs/Model/AuthLoginRequest.md)
- [AuthLoginResponse](docs/Model/AuthLoginResponse.md)
- [AuthOttValidateRequest](docs/Model/AuthOttValidateRequest.md)
- [AuthPasswordChangeRequest](docs/Model/AuthPasswordChangeRequest.md)
- [AuthPasswordChangeResponse](docs/Model/AuthPasswordChangeResponse.md)
- [AuthPasswordChangeTokenResponse](docs/Model/AuthPasswordChangeTokenResponse.md)
- [AuthPasswordRecoverRequest](docs/Model/AuthPasswordRecoverRequest.md)
- [AuthPushTokenRequest](docs/Model/AuthPushTokenRequest.md)
- [AuthPushTokenRequestWebPushKeys](docs/Model/AuthPushTokenRequestWebPushKeys.md)
- [AuthPushTokenResponse](docs/Model/AuthPushTokenResponse.md)
- [AuthRefreshRequest](docs/Model/AuthRefreshRequest.md)
- [AuthRefreshResponse](docs/Model/AuthRefreshResponse.md)
- [AuthScramFinalRequest](docs/Model/AuthScramFinalRequest.md)
- [AuthServerSignatureResponse](docs/Model/AuthServerSignatureResponse.md)
- [AuthSwagPermissionsAssociated](docs/Model/AuthSwagPermissionsAssociated.md)
- [AuthorizationAccessResponse](docs/Model/AuthorizationAccessResponse.md)
- [AuthorizationPermissionObject](docs/Model/AuthorizationPermissionObject.md)
- [AuthorizationPermissionResponse](docs/Model/AuthorizationPermissionResponse.md)
- [BookingCalendarBookingResponseAdmin](docs/Model/BookingCalendarBookingResponseAdmin.md)
- [BookingCalendarBookingResponseDefault](docs/Model/BookingCalendarBookingResponseDefault.md)
- [BookingPostRequest](docs/Model/BookingPostRequest.md)
- [BookmarkResponse](docs/Model/BookmarkResponse.md)
- [CalendarAdminEntryIdGet200Response](docs/Model/CalendarAdminEntryIdGet200Response.md)
- [CalendarAdminIdContentPost200ResponseInner](docs/Model/CalendarAdminIdContentPost200ResponseInner.md)
- [CalendarAdminIdDetailGet200Response](docs/Model/CalendarAdminIdDetailGet200Response.md)
- [CalendarAdminPost200Response](docs/Model/CalendarAdminPost200Response.md)
- [CalendarAdminProjectIdGet200ResponseInner](docs/Model/CalendarAdminProjectIdGet200ResponseInner.md)
- [CalendarAdminTemplateGet200ResponseInner](docs/Model/CalendarAdminTemplateGet200ResponseInner.md)
- [CalendarBodySectionTranslationResponse](docs/Model/CalendarBodySectionTranslationResponse.md)
- [CalendarDefaultEntryIdGet200Response](docs/Model/CalendarDefaultEntryIdGet200Response.md)
- [CalendarDefaultIdGet200Response](docs/Model/CalendarDefaultIdGet200Response.md)
- [CalendarItemTranslationResponse](docs/Model/CalendarItemTranslationResponse.md)
- [CalendarPatchRequest](docs/Model/CalendarPatchRequest.md)
- [CalendarPostRequest](docs/Model/CalendarPostRequest.md)
- [CalendarPutDetailRequest](docs/Model/CalendarPutDetailRequest.md)
- [CalendarRequestBodySection](docs/Model/CalendarRequestBodySection.md)
- [CalendarRequestCalendarSelection](docs/Model/CalendarRequestCalendarSelection.md)
- [CalendarRequestDetailPart](docs/Model/CalendarRequestDetailPart.md)
- [CalendarRequestItem](docs/Model/CalendarRequestItem.md)
- [CalendarResponseAdmin](docs/Model/CalendarResponseAdmin.md)
- [CalendarResponseBodySection](docs/Model/CalendarResponseBodySection.md)
- [CalendarResponseDefault](docs/Model/CalendarResponseDefault.md)
- [CalendarResponseDefaultListSettings](docs/Model/CalendarResponseDefaultListSettings.md)
- [CalendarResponseDetailAdmin](docs/Model/CalendarResponseDetailAdmin.md)
- [CalendarResponseDetailModelPart](docs/Model/CalendarResponseDetailModelPart.md)
- [CalendarResponseListAdmin](docs/Model/CalendarResponseListAdmin.md)
- [CalendarSwagResponseCalendarItem](docs/Model/CalendarSwagResponseCalendarItem.md)
- [CalendarTranslationResponse](docs/Model/CalendarTranslationResponse.md)
- [ChannelChatChannelJoinRequestResponse](docs/Model/ChannelChatChannelJoinRequestResponse.md)
- [ChannelChatChannelRequest](docs/Model/ChannelChatChannelRequest.md)
- [ChannelChatChannelRequestListRequest](docs/Model/ChannelChatChannelRequestListRequest.md)
- [ChannelChatChannelsResponse](docs/Model/ChannelChatChannelsResponse.md)
- [ConfigurationCSPRequest](docs/Model/ConfigurationCSPRequest.md)
- [ConfigurationCSPResponse](docs/Model/ConfigurationCSPResponse.md)
- [ConfigurationCertificateInfoResponse](docs/Model/ConfigurationCertificateInfoResponse.md)
- [ConfigurationDesignCustomCSSRequestAdmin](docs/Model/ConfigurationDesignCustomCSSRequestAdmin.md)
- [ConfigurationDesignCustomCSSResponseAdmin](docs/Model/ConfigurationDesignCustomCSSResponseAdmin.md)
- [ConfigurationDesignMenuResponseDefault](docs/Model/ConfigurationDesignMenuResponseDefault.md)
- [ConfigurationDesignRequestAdmin](docs/Model/ConfigurationDesignRequestAdmin.md)
- [ConfigurationDesignResponseAdmin](docs/Model/ConfigurationDesignResponseAdmin.md)
- [ConfigurationDesignResponseDefault](docs/Model/ConfigurationDesignResponseDefault.md)
- [ConfigurationFeaturesResponseAdmin](docs/Model/ConfigurationFeaturesResponseAdmin.md)
- [ConfigurationFeaturesResponseAdminChat](docs/Model/ConfigurationFeaturesResponseAdminChat.md)
- [ConfigurationFeaturesResponseAdminChatDomainFilter](docs/Model/ConfigurationFeaturesResponseAdminChatDomainFilter.md)
- [ConfigurationFeaturesResponseAdminChatImageModeration](docs/Model/ConfigurationFeaturesResponseAdminChatImageModeration.md)
- [ConfigurationFeaturesResponseAdminChatProfanityFilter](docs/Model/ConfigurationFeaturesResponseAdminChatProfanityFilter.md)
- [ConfigurationFeaturesResponseAdminChatProfanityFilterRegexFiltersInner](docs/Model/ConfigurationFeaturesResponseAdminChatProfanityFilterRegexFiltersInner.md)
- [ConfigurationFeaturesResponseAdminChatProfanityTriggeredModeration](docs/Model/ConfigurationFeaturesResponseAdminChatProfanityTriggeredModeration.md)
- [ConfigurationFeaturesResponseDefault](docs/Model/ConfigurationFeaturesResponseDefault.md)
- [ConfigurationImprintRequestAdmin](docs/Model/ConfigurationImprintRequestAdmin.md)
- [ConfigurationImprintResponse](docs/Model/ConfigurationImprintResponse.md)
- [ConfigurationLegalRequestAdmin](docs/Model/ConfigurationLegalRequestAdmin.md)
- [ConfigurationLegalResponseAdmin](docs/Model/ConfigurationLegalResponseAdmin.md)
- [ConfigurationLegalResponseDefault](docs/Model/ConfigurationLegalResponseDefault.md)
- [ConfigurationMediaConfigurationRequestAdmin](docs/Model/ConfigurationMediaConfigurationRequestAdmin.md)
- [ConfigurationMediaConfigurationResponse](docs/Model/ConfigurationMediaConfigurationResponse.md)
- [ConfigurationNotificationRequestAdmin](docs/Model/ConfigurationNotificationRequestAdmin.md)
- [ConfigurationNotificationResponseAdmin](docs/Model/ConfigurationNotificationResponseAdmin.md)
- [ConfigurationPatchChatRequestAdmin](docs/Model/ConfigurationPatchChatRequestAdmin.md)
- [ConfigurationPatchChatRequestAdminDomainFilter](docs/Model/ConfigurationPatchChatRequestAdminDomainFilter.md)
- [ConfigurationPatchChatRequestAdminImageModeration](docs/Model/ConfigurationPatchChatRequestAdminImageModeration.md)
- [ConfigurationPatchChatRequestAdminImageModerationLimits](docs/Model/ConfigurationPatchChatRequestAdminImageModerationLimits.md)
- [ConfigurationPatchChatRequestAdminProfanityFilter](docs/Model/ConfigurationPatchChatRequestAdminProfanityFilter.md)
- [ConfigurationPatchChatRequestAdminProfanityTriggeredModeration](docs/Model/ConfigurationPatchChatRequestAdminProfanityTriggeredModeration.md)
- [ConfigurationPatchFeaturesRequestAdmin](docs/Model/ConfigurationPatchFeaturesRequestAdmin.md)
- [ConfigurationPatchFeaturesResponseAdmin](docs/Model/ConfigurationPatchFeaturesResponseAdmin.md)
- [ConfigurationPolicyRequestAdmin](docs/Model/ConfigurationPolicyRequestAdmin.md)
- [ConfigurationPolicyResponse](docs/Model/ConfigurationPolicyResponse.md)
- [ConfigurationPremiumRequest](docs/Model/ConfigurationPremiumRequest.md)
- [ConfigurationPremiumResponseAdmin](docs/Model/ConfigurationPremiumResponseAdmin.md)
- [ConfigurationPremiumResponseDefault](docs/Model/ConfigurationPremiumResponseDefault.md)
- [ConfigurationSecurityRequestAdmin](docs/Model/ConfigurationSecurityRequestAdmin.md)
- [ConfigurationSecurityResponseAdmin](docs/Model/ConfigurationSecurityResponseAdmin.md)
- [ConfigurationSecurityResponseDefault](docs/Model/ConfigurationSecurityResponseDefault.md)
- [ConfigurationTermsRequestAdmin](docs/Model/ConfigurationTermsRequestAdmin.md)
- [ConfigurationTermsResponse](docs/Model/ConfigurationTermsResponse.md)
- [ConfigurationTrackingLegalResponse](docs/Model/ConfigurationTrackingLegalResponse.md)
- [ConnectedappAddSecretRequest](docs/Model/ConnectedappAddSecretRequest.md)
- [ConnectedappRequest](docs/Model/ConnectedappRequest.md)
- [ConnectedappResponse](docs/Model/ConnectedappResponse.md)
- [ConnectedappResponseList](docs/Model/ConnectedappResponseList.md)
- [ConnectedappSecretRequest](docs/Model/ConnectedappSecretRequest.md)
- [ConnectedappSecretResponse](docs/Model/ConnectedappSecretResponse.md)
- [ContentDeprecatedCalendarEntryValue](docs/Model/ContentDeprecatedCalendarEntryValue.md)
- [ContentDeprecatedEntryResponseListDefault](docs/Model/ContentDeprecatedEntryResponseListDefault.md)
- [ContentEntryDateTimeResponse](docs/Model/ContentEntryDateTimeResponse.md)
- [ContentEntryPostRequest](docs/Model/ContentEntryPostRequest.md)
- [ContentEntryRequest](docs/Model/ContentEntryRequest.md)
- [ContentEntryResponseAdmin](docs/Model/ContentEntryResponseAdmin.md)
- [ContentEntryResponseDefault](docs/Model/ContentEntryResponseDefault.md)
- [ContentEntryResponseListAdmin](docs/Model/ContentEntryResponseListAdmin.md)
- [ContentEntryResponseListDefault](docs/Model/ContentEntryResponseListDefault.md)
- [ContentEntryTabRequest](docs/Model/ContentEntryTabRequest.md)
- [ContentEntryTabResponse](docs/Model/ContentEntryTabResponse.md)
- [ContentEntryTabTranslation](docs/Model/ContentEntryTabTranslation.md)
- [ContentEntryTranslation](docs/Model/ContentEntryTranslation.md)
- [ContentEntryValueRequest](docs/Model/ContentEntryValueRequest.md)
- [ContentEntryValueResponse](docs/Model/ContentEntryValueResponse.md)
- [ContentEntryValueTranslation](docs/Model/ContentEntryValueTranslation.md)
- [ContentRowPostRequestAdmin](docs/Model/ContentRowPostRequestAdmin.md)
- [ContentRowRequestAdmin](docs/Model/ContentRowRequestAdmin.md)
- [ContentRowRequestDefault](docs/Model/ContentRowRequestDefault.md)
- [ContentRowResponseAdmin](docs/Model/ContentRowResponseAdmin.md)
- [ContentRowResponseDefault](docs/Model/ContentRowResponseDefault.md)
- [ContentRowValueRequest](docs/Model/ContentRowValueRequest.md)
- [ContentbuilderItemTranslationResponse](docs/Model/ContentbuilderItemTranslationResponse.md)
- [ContentbuilderRequestItem](docs/Model/ContentbuilderRequestItem.md)
- [ContentbuilderRequestItemAppliedFilter](docs/Model/ContentbuilderRequestItemAppliedFilter.md)
- [ContentbuilderSwagResponseItemAdmin](docs/Model/ContentbuilderSwagResponseItemAdmin.md)
- [ContentbuilderSwagResponseItemAppliedFilter](docs/Model/ContentbuilderSwagResponseItemAppliedFilter.md)
- [ContentbuilderSwagResponseItemDefault](docs/Model/ContentbuilderSwagResponseItemDefault.md)
- [CopyprocessRequest](docs/Model/CopyprocessRequest.md)
- [CopyprocessResponse](docs/Model/CopyprocessResponse.md)
- [DeeplinkRequest](docs/Model/DeeplinkRequest.md)
- [DirectoryAdminGet200ResponseInner](docs/Model/DirectoryAdminGet200ResponseInner.md)
- [DirectoryAdminIdDetailGet200Response](docs/Model/DirectoryAdminIdDetailGet200Response.md)
- [DirectoryAdminPost200Response](docs/Model/DirectoryAdminPost200Response.md)
- [DirectoryAdminTemplateGet200ResponseInner](docs/Model/DirectoryAdminTemplateGet200ResponseInner.md)
- [DirectoryBodySectionTranslationResponse](docs/Model/DirectoryBodySectionTranslationResponse.md)
- [DirectoryCopyPostRequest](docs/Model/DirectoryCopyPostRequest.md)
- [DirectoryCursorFilterOptionAdmin](docs/Model/DirectoryCursorFilterOptionAdmin.md)
- [DirectoryCursorRequestAdmin](docs/Model/DirectoryCursorRequestAdmin.md)
- [DirectoryDefaultIdGet200Response](docs/Model/DirectoryDefaultIdGet200Response.md)
- [DirectoryItemTranslationResponse](docs/Model/DirectoryItemTranslationResponse.md)
- [DirectoryPatchRequest](docs/Model/DirectoryPatchRequest.md)
- [DirectoryPostRequest](docs/Model/DirectoryPostRequest.md)
- [DirectoryPutDetailRequest](docs/Model/DirectoryPutDetailRequest.md)
- [DirectoryRequestBodySection](docs/Model/DirectoryRequestBodySection.md)
- [DirectoryRequestDetailPart](docs/Model/DirectoryRequestDetailPart.md)
- [DirectoryRequestDirectorySelection](docs/Model/DirectoryRequestDirectorySelection.md)
- [DirectoryRequestItem](docs/Model/DirectoryRequestItem.md)
- [DirectoryResponseAdmin](docs/Model/DirectoryResponseAdmin.md)
- [DirectoryResponseBodySection](docs/Model/DirectoryResponseBodySection.md)
- [DirectoryResponseDefault](docs/Model/DirectoryResponseDefault.md)
- [DirectoryResponseDefaultDetail](docs/Model/DirectoryResponseDefaultDetail.md)
- [DirectoryResponseDefaultDetailHeaderSection](docs/Model/DirectoryResponseDefaultDetailHeaderSection.md)
- [DirectoryResponseDefaultListSettings](docs/Model/DirectoryResponseDefaultListSettings.md)
- [DirectoryResponseDetail](docs/Model/DirectoryResponseDetail.md)
- [DirectoryResponseDetailModelPart](docs/Model/DirectoryResponseDetailModelPart.md)
- [DirectoryResponseListAdmin](docs/Model/DirectoryResponseListAdmin.md)
- [DirectorySwagResponseDirectoryItem](docs/Model/DirectorySwagResponseDirectoryItem.md)
- [DirectoryTranslationResponse](docs/Model/DirectoryTranslationResponse.md)
- [DownloadrequestResponse](docs/Model/DownloadrequestResponse.md)
- [FeedPatchRequest](docs/Model/FeedPatchRequest.md)
- [FeedPostRequest](docs/Model/FeedPostRequest.md)
- [FeedResponseAdmin](docs/Model/FeedResponseAdmin.md)
- [FeedResponseDefault](docs/Model/FeedResponseDefault.md)
- [FeedResponseListAdmin](docs/Model/FeedResponseListAdmin.md)
- [FolderPatchRequest](docs/Model/FolderPatchRequest.md)
- [FolderRequest](docs/Model/FolderRequest.md)
- [FolderResponse](docs/Model/FolderResponse.md)
- [GitPlazzNetReposSandmannBackendServicesCalendarContentCursorFilterOptionDefault](docs/Model/GitPlazzNetReposSandmannBackendServicesCalendarContentCursorFilterOptionDefault.md)
- [GitPlazzNetReposSandmannBackendServicesCalendarTemplateResponseAdmin](docs/Model/GitPlazzNetReposSandmannBackendServicesCalendarTemplateResponseAdmin.md)
- [GitPlazzNetReposSandmannBackendServicesDirectoryTemplateResponseAdmin](docs/Model/GitPlazzNetReposSandmannBackendServicesDirectoryTemplateResponseAdmin.md)
- [GitPlazzNetReposSandmannBackendServicesPartyReactionCursorFilterOptionAdmin](docs/Model/GitPlazzNetReposSandmannBackendServicesPartyReactionCursorFilterOptionAdmin.md)
- [GitPlazzNetReposSandmannBackendServicesPartyReactionCursorFilterOptionDefault](docs/Model/GitPlazzNetReposSandmannBackendServicesPartyReactionCursorFilterOptionDefault.md)
- [GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestAdmin](docs/Model/GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestAdmin.md)
- [GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestDefault](docs/Model/GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestDefault.md)
- [GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault](docs/Model/GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault.md)
- [GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault](docs/Model/GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault.md)
- [GroupPatchRequest](docs/Model/GroupPatchRequest.md)
- [GroupPostRequest](docs/Model/GroupPostRequest.md)
- [GroupResponse](docs/Model/GroupResponse.md)
- [GuestvisitRequest](docs/Model/GuestvisitRequest.md)
- [IndexAdminGet200ResponseInner](docs/Model/IndexAdminGet200ResponseInner.md)
- [IndexAdminObjectTypeObjectIdGet200Response](docs/Model/IndexAdminObjectTypeObjectIdGet200Response.md)
- [IndexCursorRequestAdmin](docs/Model/IndexCursorRequestAdmin.md)
- [IndexCursorRequestDefault](docs/Model/IndexCursorRequestDefault.md)
- [IndexResponse](docs/Model/IndexResponse.md)
- [IndexSwagIndexMetaMap](docs/Model/IndexSwagIndexMetaMap.md)
- [JobPatchRequest](docs/Model/JobPatchRequest.md)
- [JobRequestAdmin](docs/Model/JobRequestAdmin.md)
- [JobResponseAdmin](docs/Model/JobResponseAdmin.md)
- [JobResponseListAdmin](docs/Model/JobResponseListAdmin.md)
- [JobTestContentRequest](docs/Model/JobTestContentRequest.md)
- [JourneyPatchRequest](docs/Model/JourneyPatchRequest.md)
- [JourneyPostRequest](docs/Model/JourneyPostRequest.md)
- [JourneyRequestStage](docs/Model/JourneyRequestStage.md)
- [JourneyResponseAdmin](docs/Model/JourneyResponseAdmin.md)
- [JourneyResponseDefault](docs/Model/JourneyResponseDefault.md)
- [JourneyResponseListAdmin](docs/Model/JourneyResponseListAdmin.md)
- [JourneyResponseStageAdmin](docs/Model/JourneyResponseStageAdmin.md)
- [JourneyResponseStageDefault](docs/Model/JourneyResponseStageDefault.md)
- [JourneyResponseStatsDefault](docs/Model/JourneyResponseStatsDefault.md)
- [JourneyStageTranslationResponse](docs/Model/JourneyStageTranslationResponse.md)
- [JourneyTranslationResponse](docs/Model/JourneyTranslationResponse.md)
- [JourneyprocessCursorFilterOptionDefault](docs/Model/JourneyprocessCursorFilterOptionDefault.md)
- [JourneyprocessCursorRequestDefault](docs/Model/JourneyprocessCursorRequestDefault.md)
- [JourneyprocessPatchRequest](docs/Model/JourneyprocessPatchRequest.md)
- [JourneyprocessPatchStageStatus](docs/Model/JourneyprocessPatchStageStatus.md)
- [JourneyprocessPostEntry](docs/Model/JourneyprocessPostEntry.md)
- [JourneyprocessResponseAdmin](docs/Model/JourneyprocessResponseAdmin.md)
- [JourneyprocessResponseDefault](docs/Model/JourneyprocessResponseDefault.md)
- [JourneyprocessResponseListDefault](docs/Model/JourneyprocessResponseListDefault.md)
- [JourneyprocessTranslationResponse](docs/Model/JourneyprocessTranslationResponse.md)
- [KeywordPatchRequest](docs/Model/KeywordPatchRequest.md)
- [KeywordRequest](docs/Model/KeywordRequest.md)
- [KeywordResponseAdmin](docs/Model/KeywordResponseAdmin.md)
- [KeywordResponseDefault](docs/Model/KeywordResponseDefault.md)
- [KeywordcategoryRequest](docs/Model/KeywordcategoryRequest.md)
- [KeywordcategoryResponseAdmin](docs/Model/KeywordcategoryResponseAdmin.md)
- [KeywordcategoryResponseDefault](docs/Model/KeywordcategoryResponseDefault.md)
- [KnowledgebaseArticle](docs/Model/KnowledgebaseArticle.md)
- [KnowledgebaseFolder](docs/Model/KnowledgebaseFolder.md)
- [LanguagePatchRequest](docs/Model/LanguagePatchRequest.md)
- [LanguagePutDefaultRequest](docs/Model/LanguagePutDefaultRequest.md)
- [LanguageResponseAdmin](docs/Model/LanguageResponseAdmin.md)
- [LanguageResponseDefault](docs/Model/LanguageResponseDefault.md)
- [LocalizationCursorFilterOptionAdmin](docs/Model/LocalizationCursorFilterOptionAdmin.md)
- [LocalizationCursorRequestAdmin](docs/Model/LocalizationCursorRequestAdmin.md)
- [LocalizationGlossaryEntryRequest](docs/Model/LocalizationGlossaryEntryRequest.md)
- [LocalizationPatchLocalizationRequest](docs/Model/LocalizationPatchLocalizationRequest.md)
- [LocalizationResponseAdmin](docs/Model/LocalizationResponseAdmin.md)
- [LocationPatchRequest](docs/Model/LocationPatchRequest.md)
- [LocationRequestAdmin](docs/Model/LocationRequestAdmin.md)
- [LocationResponseAdmin](docs/Model/LocationResponseAdmin.md)
- [LocationResponseDefault](docs/Model/LocationResponseDefault.md)
- [LocationResponseListAdmin](docs/Model/LocationResponseListAdmin.md)
- [LocationResponseListDefault](docs/Model/LocationResponseListDefault.md)
- [LocationmapMapMarkerTranslationResponse](docs/Model/LocationmapMapMarkerTranslationResponse.md)
- [LocationmapMarkerRequest](docs/Model/LocationmapMarkerRequest.md)
- [LocationmapMarkerResponseAdmin](docs/Model/LocationmapMarkerResponseAdmin.md)
- [LocationmapMarkerResponseDefault](docs/Model/LocationmapMarkerResponseDefault.md)
- [LocationmapPatchRequest](docs/Model/LocationmapPatchRequest.md)
- [LocationmapRequestAdmin](docs/Model/LocationmapRequestAdmin.md)
- [LocationmapResponseAdmin](docs/Model/LocationmapResponseAdmin.md)
- [LocationmapResponseDefault](docs/Model/LocationmapResponseDefault.md)
- [LocationmapResponseListAdmin](docs/Model/LocationmapResponseListAdmin.md)
- [LocationmapTranslationResponse](docs/Model/LocationmapTranslationResponse.md)
- [MediaCursorFilterOptionAdmin](docs/Model/MediaCursorFilterOptionAdmin.md)
- [MediaCursorFilterOptionDefault](docs/Model/MediaCursorFilterOptionDefault.md)
- [MediaCursorRequestAdmin](docs/Model/MediaCursorRequestAdmin.md)
- [MediaCursorRequestDefault](docs/Model/MediaCursorRequestDefault.md)
- [MediaDuplicationRequest](docs/Model/MediaDuplicationRequest.md)
- [MediaPatchRequestAdmin](docs/Model/MediaPatchRequestAdmin.md)
- [MediaPatchRequestDefault](docs/Model/MediaPatchRequestDefault.md)
- [MediaResponseAdmin](docs/Model/MediaResponseAdmin.md)
- [MediaResponseDefault](docs/Model/MediaResponseDefault.md)
- [MediaResponseListAdmin](docs/Model/MediaResponseListAdmin.md)
- [MediaResponseListDefault](docs/Model/MediaResponseListDefault.md)
- [MediaResponsePermalink](docs/Model/MediaResponsePermalink.md)
- [MenuAdminProjectIdGet200Response](docs/Model/MenuAdminProjectIdGet200Response.md)
- [MenuDefaultProjectIdGet200Response](docs/Model/MenuDefaultProjectIdGet200Response.md)
- [MenuItemTranslationResponse](docs/Model/MenuItemTranslationResponse.md)
- [MenuRequest](docs/Model/MenuRequest.md)
- [MenuRequestDesignWeb](docs/Model/MenuRequestDesignWeb.md)
- [MenuRequestItem](docs/Model/MenuRequestItem.md)
- [MenuRequestSettings](docs/Model/MenuRequestSettings.md)
- [MenuResponseAdmin](docs/Model/MenuResponseAdmin.md)
- [MenuResponseDefault](docs/Model/MenuResponseDefault.md)
- [MenuResponseDesignWebDefault](docs/Model/MenuResponseDesignWebDefault.md)
- [MenuResponseSettingsAdmin](docs/Model/MenuResponseSettingsAdmin.md)
- [MenuResponseSettingsDefault](docs/Model/MenuResponseSettingsDefault.md)
- [MenuSwagMenuItemAdmin](docs/Model/MenuSwagMenuItemAdmin.md)
- [MenuSwagMenuItemDefault](docs/Model/MenuSwagMenuItemDefault.md)
- [ModelAccess](docs/Model/ModelAccess.md)
- [ModelAccountChatVisibleAnalyticsSnapshot](docs/Model/ModelAccountChatVisibleAnalyticsSnapshot.md)
- [ModelAccountDevice](docs/Model/ModelAccountDevice.md)
- [ModelAccountMetaData](docs/Model/ModelAccountMetaData.md)
- [ModelAccountNotificationSettings](docs/Model/ModelAccountNotificationSettings.md)
- [ModelAccountNotifyConfiguration](docs/Model/ModelAccountNotifyConfiguration.md)
- [ModelAccountPlaceholderConfig](docs/Model/ModelAccountPlaceholderConfig.md)
- [ModelAccountProfileColor](docs/Model/ModelAccountProfileColor.md)
- [ModelAccountProjectSettings](docs/Model/ModelAccountProjectSettings.md)
- [ModelAccountRole](docs/Model/ModelAccountRole.md)
- [ModelAccountStatsRecord](docs/Model/ModelAccountStatsRecord.md)
- [ModelAccountTrackingAnalyticsSnapshot](docs/Model/ModelAccountTrackingAnalyticsSnapshot.md)
- [ModelAddress](docs/Model/ModelAddress.md)
- [ModelAppointmentReceiver](docs/Model/ModelAppointmentReceiver.md)
- [ModelAppointmentSlotTimeConfig](docs/Model/ModelAppointmentSlotTimeConfig.md)
- [ModelArticleSettings](docs/Model/ModelArticleSettings.md)
- [ModelAutoTranslation](docs/Model/ModelAutoTranslation.md)
- [ModelCalendarBodySection](docs/Model/ModelCalendarBodySection.md)
- [ModelCalendarBodySectionLocalization](docs/Model/ModelCalendarBodySectionLocalization.md)
- [ModelCalendarDetail](docs/Model/ModelCalendarDetail.md)
- [ModelCalendarItem](docs/Model/ModelCalendarItem.md)
- [ModelCalendarItemLocalization](docs/Model/ModelCalendarItemLocalization.md)
- [ModelCalendarListSettings](docs/Model/ModelCalendarListSettings.md)
- [ModelChatFeedTranslation](docs/Model/ModelChatFeedTranslation.md)
- [ModelChatSettings](docs/Model/ModelChatSettings.md)
- [ModelCoords](docs/Model/ModelCoords.md)
- [ModelCursorResponse](docs/Model/ModelCursorResponse.md)
- [ModelDatePeriod](docs/Model/ModelDatePeriod.md)
- [ModelDateTime](docs/Model/ModelDateTime.md)
- [ModelDeeplinkObject](docs/Model/ModelDeeplinkObject.md)
- [ModelDirectoryBodySection](docs/Model/ModelDirectoryBodySection.md)
- [ModelDirectoryBodySectionLocalization](docs/Model/ModelDirectoryBodySectionLocalization.md)
- [ModelDirectoryDetail](docs/Model/ModelDirectoryDetail.md)
- [ModelDirectoryHeaderSection](docs/Model/ModelDirectoryHeaderSection.md)
- [ModelDirectoryItem](docs/Model/ModelDirectoryItem.md)
- [ModelDirectoryItemLocalization](docs/Model/ModelDirectoryItemLocalization.md)
- [ModelDirectoryListSettings](docs/Model/ModelDirectoryListSettings.md)
- [ModelDirectoryRowValue](docs/Model/ModelDirectoryRowValue.md)
- [ModelDirectoryRowValueTranslation](docs/Model/ModelDirectoryRowValueTranslation.md)
- [ModelEmailSettings](docs/Model/ModelEmailSettings.md)
- [ModelEventStatusFilter](docs/Model/ModelEventStatusFilter.md)
- [ModelFeatureEnabled](docs/Model/ModelFeatureEnabled.md)
- [ModelFeaturePaidUntil](docs/Model/ModelFeaturePaidUntil.md)
- [ModelGeoInformation](docs/Model/ModelGeoInformation.md)
- [ModelJourneyProcessStageStatus](docs/Model/ModelJourneyProcessStageStatus.md)
- [ModelJourneyStageStartCondition](docs/Model/ModelJourneyStageStartCondition.md)
- [ModelJourneyStageStartConditionOffset](docs/Model/ModelJourneyStageStartConditionOffset.md)
- [ModelKeywordCategorySettings](docs/Model/ModelKeywordCategorySettings.md)
- [ModelKeywordCategoryTranslation](docs/Model/ModelKeywordCategoryTranslation.md)
- [ModelKeywordTranslation](docs/Model/ModelKeywordTranslation.md)
- [ModelLocationTranslation](docs/Model/ModelLocationTranslation.md)
- [ModelMailEvent](docs/Model/ModelMailEvent.md)
- [ModelMailTopic](docs/Model/ModelMailTopic.md)
- [ModelMediaItemResolution](docs/Model/ModelMediaItemResolution.md)
- [ModelMediaItemTranslation](docs/Model/ModelMediaItemTranslation.md)
- [ModelMediaType](docs/Model/ModelMediaType.md)
- [ModelMetaItemConfig](docs/Model/ModelMetaItemConfig.md)
- [ModelMimeType](docs/Model/ModelMimeType.md)
- [ModelNotificationJobLocalization](docs/Model/ModelNotificationJobLocalization.md)
- [ModelNotificationRecipients](docs/Model/ModelNotificationRecipients.md)
- [ModelNotificationTranslation](docs/Model/ModelNotificationTranslation.md)
- [ModelObjectIdentification](docs/Model/ModelObjectIdentification.md)
- [ModelObjectType](docs/Model/ModelObjectType.md)
- [ModelOperation](docs/Model/ModelOperation.md)
- [ModelOperationAccess](docs/Model/ModelOperationAccess.md)
- [ModelPageSettings](docs/Model/ModelPageSettings.md)
- [ModelPalette](docs/Model/ModelPalette.md)
- [ModelPaletteAuto](docs/Model/ModelPaletteAuto.md)
- [ModelPartyBookingSlot](docs/Model/ModelPartyBookingSlot.md)
- [ModelPartyConfiguration](docs/Model/ModelPartyConfiguration.md)
- [ModelProfileDefaultConfig](docs/Model/ModelProfileDefaultConfig.md)
- [ModelProjectCopyProcessConfig](docs/Model/ModelProjectCopyProcessConfig.md)
- [ModelProjectCopyProcessStatusDetail](docs/Model/ModelProjectCopyProcessStatusDetail.md)
- [ModelProjectCopyProcessedData](docs/Model/ModelProjectCopyProcessedData.md)
- [ModelProjectTranslation](docs/Model/ModelProjectTranslation.md)
- [ModelPushSettings](docs/Model/ModelPushSettings.md)
- [ModelSSOAccountMapping](docs/Model/ModelSSOAccountMapping.md)
- [ModelSSOGroupConfigurationMapping](docs/Model/ModelSSOGroupConfigurationMapping.md)
- [ModelSSOIdp](docs/Model/ModelSSOIdp.md)
- [ModelSSOMetaConfigurationMapping](docs/Model/ModelSSOMetaConfigurationMapping.md)
- [ModelSSOProviderTranslation](docs/Model/ModelSSOProviderTranslation.md)
- [ModelSSORoleConfigurationMapping](docs/Model/ModelSSORoleConfigurationMapping.md)
- [ModelSSOType](docs/Model/ModelSSOType.md)
- [ModelSearch](docs/Model/ModelSearch.md)
- [ModelShipAccountData](docs/Model/ModelShipAccountData.md)
- [ModelShippingConfig](docs/Model/ModelShippingConfig.md)
- [ModelShippingProcess](docs/Model/ModelShippingProcess.md)
- [ModelStreamTranslation](docs/Model/ModelStreamTranslation.md)
- [ModelSwagErrorBadGateway](docs/Model/ModelSwagErrorBadGateway.md)
- [ModelSwagErrorBadRequest](docs/Model/ModelSwagErrorBadRequest.md)
- [ModelSwagErrorBadRequestWithErrorFields](docs/Model/ModelSwagErrorBadRequestWithErrorFields.md)
- [ModelSwagErrorConflict](docs/Model/ModelSwagErrorConflict.md)
- [ModelSwagErrorContentTooLarge](docs/Model/ModelSwagErrorContentTooLarge.md)
- [ModelSwagErrorForbidden](docs/Model/ModelSwagErrorForbidden.md)
- [ModelSwagErrorInternalServerError](docs/Model/ModelSwagErrorInternalServerError.md)
- [ModelSwagErrorNotFound](docs/Model/ModelSwagErrorNotFound.md)
- [ModelSwagErrorNotImplemented](docs/Model/ModelSwagErrorNotImplemented.md)
- [ModelSwagErrorPaymentRequired](docs/Model/ModelSwagErrorPaymentRequired.md)
- [ModelSwagErrorPreconditionFailed](docs/Model/ModelSwagErrorPreconditionFailed.md)
- [ModelSwagErrorPreconditionRequired](docs/Model/ModelSwagErrorPreconditionRequired.md)
- [ModelSwagErrorRangeNotSatisfiable](docs/Model/ModelSwagErrorRangeNotSatisfiable.md)
- [ModelSwagErrorUnauthorized](docs/Model/ModelSwagErrorUnauthorized.md)
- [ModelSwagStatusOk](docs/Model/ModelSwagStatusOk.md)
- [ModelSystemNotification](docs/Model/ModelSystemNotification.md)
- [ModelTimeSlot](docs/Model/ModelTimeSlot.md)
- [ModelWebhookAction](docs/Model/ModelWebhookAction.md)
- [ModelWebhookRequestLogMessage](docs/Model/ModelWebhookRequestLogMessage.md)
- [NewsAdminIdContentGet200ResponseInner](docs/Model/NewsAdminIdContentGet200ResponseInner.md)
- [NewsAdminPost200Response](docs/Model/NewsAdminPost200Response.md)
- [NewsAdminPost200ResponseAllOfContentInner](docs/Model/NewsAdminPost200ResponseAllOfContentInner.md)
- [NewsAdminPost200ResponseAllOfContentInnerAllOfColumnsInner](docs/Model/NewsAdminPost200ResponseAllOfContentInnerAllOfColumnsInner.md)
- [NewsArticlePatchRequest](docs/Model/NewsArticlePatchRequest.md)
- [NewsArticlePostCountResponse](docs/Model/NewsArticlePostCountResponse.md)
- [NewsArticleRequest](docs/Model/NewsArticleRequest.md)
- [NewsArticleResponseAdmin](docs/Model/NewsArticleResponseAdmin.md)
- [NewsArticleResponseDefault](docs/Model/NewsArticleResponseDefault.md)
- [NewsArticleResponseListAdmin](docs/Model/NewsArticleResponseListAdmin.md)
- [NewsArticleResponseListDefault](docs/Model/NewsArticleResponseListDefault.md)
- [NewsArticleTranslationResponse](docs/Model/NewsArticleTranslationResponse.md)
- [NewsCursorFilterOptionAdmin](docs/Model/NewsCursorFilterOptionAdmin.md)
- [NewsCursorFilterOptionDefault](docs/Model/NewsCursorFilterOptionDefault.md)
- [NewsCursorFilterOptionPreviewDefault](docs/Model/NewsCursorFilterOptionPreviewDefault.md)
- [NewsCursorRequestAdmin](docs/Model/NewsCursorRequestAdmin.md)
- [NewsCursorRequestDefault](docs/Model/NewsCursorRequestDefault.md)
- [NewsDefaultIdGet200Response](docs/Model/NewsDefaultIdGet200Response.md)
- [NewsDefaultIdGet200ResponseAllOfContentInner](docs/Model/NewsDefaultIdGet200ResponseAllOfContentInner.md)
- [NewsDefaultIdGet200ResponseAllOfContentInnerAllOfColumnsInner](docs/Model/NewsDefaultIdGet200ResponseAllOfContentInnerAllOfColumnsInner.md)
- [NewsPlatform](docs/Model/NewsPlatform.md)
- [NewsPostCursorPreviewDefault](docs/Model/NewsPostCursorPreviewDefault.md)
- [NewsRequestColumn](docs/Model/NewsRequestColumn.md)
- [NewsRequestSection](docs/Model/NewsRequestSection.md)
- [NewsResponseColumnAdmin](docs/Model/NewsResponseColumnAdmin.md)
- [NewsResponseColumnDefault](docs/Model/NewsResponseColumnDefault.md)
- [NewsResponseSectionAdmin](docs/Model/NewsResponseSectionAdmin.md)
- [NewsResponseSectionDefault](docs/Model/NewsResponseSectionDefault.md)
- [NewsResponseSettingsDefault](docs/Model/NewsResponseSettingsDefault.md)
- [NewsSwagNewsColumnAdmin](docs/Model/NewsSwagNewsColumnAdmin.md)
- [NewsSwagNewsColumnDefault](docs/Model/NewsSwagNewsColumnDefault.md)
- [NewsSwagNewsSectionAdmin](docs/Model/NewsSwagNewsSectionAdmin.md)
- [NewsSwagNewsSectionDefault](docs/Model/NewsSwagNewsSectionDefault.md)
- [NotificationEmailResponseAdmin](docs/Model/NotificationEmailResponseAdmin.md)
- [NotificationPatchEmailRequest](docs/Model/NotificationPatchEmailRequest.md)
- [NotificationPatchNotificationRequest](docs/Model/NotificationPatchNotificationRequest.md)
- [NotificationPostEmailRequest](docs/Model/NotificationPostEmailRequest.md)
- [NotificationPostNotificationRequest](docs/Model/NotificationPostNotificationRequest.md)
- [NotificationPutAccountNotificationRequest](docs/Model/NotificationPutAccountNotificationRequest.md)
- [NotificationPutAccountNotificationResponse](docs/Model/NotificationPutAccountNotificationResponse.md)
- [NotificationResponseAdmin](docs/Model/NotificationResponseAdmin.md)
- [NotificationSafariSettings](docs/Model/NotificationSafariSettings.md)
- [NotificationTestEmailContentRequest](docs/Model/NotificationTestEmailContentRequest.md)
- [NotificationVAPIDPublicKeyResponse](docs/Model/NotificationVAPIDPublicKeyResponse.md)
- [PageAdminIdContentGet200ResponseInner](docs/Model/PageAdminIdContentGet200ResponseInner.md)
- [PageAdminPost200Response](docs/Model/PageAdminPost200Response.md)
- [PageAdminPost200ResponseAllOfContentInner](docs/Model/PageAdminPost200ResponseAllOfContentInner.md)
- [PageAdminPost200ResponseAllOfContentInnerAllOfColumnsInner](docs/Model/PageAdminPost200ResponseAllOfContentInnerAllOfColumnsInner.md)
- [PageDefaultIdGet200Response](docs/Model/PageDefaultIdGet200Response.md)
- [PageDefaultIdGet200ResponseAllOfContentInner](docs/Model/PageDefaultIdGet200ResponseAllOfContentInner.md)
- [PageDefaultIdGet200ResponseAllOfContentInnerAllOfColumnsInner](docs/Model/PageDefaultIdGet200ResponseAllOfContentInnerAllOfColumnsInner.md)
- [PagePatchRequest](docs/Model/PagePatchRequest.md)
- [PagePlatform](docs/Model/PagePlatform.md)
- [PagePostCountResponse](docs/Model/PagePostCountResponse.md)
- [PageRequest](docs/Model/PageRequest.md)
- [PageRequestColumn](docs/Model/PageRequestColumn.md)
- [PageRequestSection](docs/Model/PageRequestSection.md)
- [PageResponseAdmin](docs/Model/PageResponseAdmin.md)
- [PageResponseColumnAdmin](docs/Model/PageResponseColumnAdmin.md)
- [PageResponseColumnDefault](docs/Model/PageResponseColumnDefault.md)
- [PageResponseDefault](docs/Model/PageResponseDefault.md)
- [PageResponseListAdmin](docs/Model/PageResponseListAdmin.md)
- [PageResponseListDefault](docs/Model/PageResponseListDefault.md)
- [PageResponseSectionAdmin](docs/Model/PageResponseSectionAdmin.md)
- [PageResponseSectionDefault](docs/Model/PageResponseSectionDefault.md)
- [PageResponseSettingsDefault](docs/Model/PageResponseSettingsDefault.md)
- [PageSwagPageColumnAdmin](docs/Model/PageSwagPageColumnAdmin.md)
- [PageSwagPageColumnDefault](docs/Model/PageSwagPageColumnDefault.md)
- [PageSwagPageSectionAdmin](docs/Model/PageSwagPageSectionAdmin.md)
- [PageSwagPageSectionDefault](docs/Model/PageSwagPageSectionDefault.md)
- [PageTranslationResponse](docs/Model/PageTranslationResponse.md)
- [PartyCursorFilterOptionAdmin](docs/Model/PartyCursorFilterOptionAdmin.md)
- [PartyCursorFilterOptionDefault](docs/Model/PartyCursorFilterOptionDefault.md)
- [PartyCursorRequestAdmin](docs/Model/PartyCursorRequestAdmin.md)
- [PartyCursorRequestDefault](docs/Model/PartyCursorRequestDefault.md)
- [PartyRequestAdmin](docs/Model/PartyRequestAdmin.md)
- [PartyRequestBookingSlot](docs/Model/PartyRequestBookingSlot.md)
- [PartyRequestConfiguration](docs/Model/PartyRequestConfiguration.md)
- [PartyResponseAdmin](docs/Model/PartyResponseAdmin.md)
- [PartyResponseDefault](docs/Model/PartyResponseDefault.md)
- [PartyResponsePartyConfigurationDefault](docs/Model/PartyResponsePartyConfigurationDefault.md)
- [ProjectPatchRequest](docs/Model/ProjectPatchRequest.md)
- [ProjectPatchRequestTracking](docs/Model/ProjectPatchRequestTracking.md)
- [ProjectPostRequest](docs/Model/ProjectPostRequest.md)
- [ProjectResponseAdmin](docs/Model/ProjectResponseAdmin.md)
- [ProjectResponseDefault](docs/Model/ProjectResponseDefault.md)
- [ProjectResponseListAdmin](docs/Model/ProjectResponseListAdmin.md)
- [ProjectResponseSettings](docs/Model/ProjectResponseSettings.md)
- [ProjectResponseTracking](docs/Model/ProjectResponseTracking.md)
- [ReactionCursorObjectIDsFilterOption](docs/Model/ReactionCursorObjectIDsFilterOption.md)
- [ReactionCursorObjectIDsRequest](docs/Model/ReactionCursorObjectIDsRequest.md)
- [ReactionInfo](docs/Model/ReactionInfo.md)
- [ReactionPostReactionRequest](docs/Model/ReactionPostReactionRequest.md)
- [ReactionRequest](docs/Model/ReactionRequest.md)
- [ReactionRequestAdmin](docs/Model/ReactionRequestAdmin.md)
- [ReactionResponseAdmin](docs/Model/ReactionResponseAdmin.md)
- [ReactionResponseListAdmin](docs/Model/ReactionResponseListAdmin.md)
- [RolePatchRequest](docs/Model/RolePatchRequest.md)
- [RolePostRequest](docs/Model/RolePostRequest.md)
- [RoleResponse](docs/Model/RoleResponse.md)
- [SchemeRequestAdmin](docs/Model/SchemeRequestAdmin.md)
- [SchemeResponseAdmin](docs/Model/SchemeResponseAdmin.md)
- [SchemeResponseDefault](docs/Model/SchemeResponseDefault.md)
- [SelectionAPIOptionDesignRequest](docs/Model/SelectionAPIOptionDesignRequest.md)
- [SelectionAPIOptionDesignResponseAdmin](docs/Model/SelectionAPIOptionDesignResponseAdmin.md)
- [SelectionAPIOptionDesignResponseDefault](docs/Model/SelectionAPIOptionDesignResponseDefault.md)
- [SelectionAPIOptionRequest](docs/Model/SelectionAPIOptionRequest.md)
- [SelectionAPIOptionResponseAdmin](docs/Model/SelectionAPIOptionResponseAdmin.md)
- [SelectionAPIOptionResponseDefault](docs/Model/SelectionAPIOptionResponseDefault.md)
- [SelectionAPIOptionTranslationResponse](docs/Model/SelectionAPIOptionTranslationResponse.md)
- [SelectionAPIResponseAdmin](docs/Model/SelectionAPIResponseAdmin.md)
- [SelectionAPIResponseDefault](docs/Model/SelectionAPIResponseDefault.md)
- [SendbirdImageModerationLimits](docs/Model/SendbirdImageModerationLimits.md)
- [ShippingRequestBaseAdmin](docs/Model/ShippingRequestBaseAdmin.md)
- [ShippingResponseAdmin](docs/Model/ShippingResponseAdmin.md)
- [SsoCodeRequest](docs/Model/SsoCodeRequest.md)
- [SsoProviderRequest](docs/Model/SsoProviderRequest.md)
- [SsoProviderResponseAdmin](docs/Model/SsoProviderResponseAdmin.md)
- [SsoProviderResponseDefault](docs/Model/SsoProviderResponseDefault.md)
- [StreamOutput](docs/Model/StreamOutput.md)
- [StreamPatchRequest](docs/Model/StreamPatchRequest.md)
- [StreamPostRequest](docs/Model/StreamPostRequest.md)
- [StreamResponseAdmin](docs/Model/StreamResponseAdmin.md)
- [StreamResponseDefault](docs/Model/StreamResponseDefault.md)
- [StreamResponseListAdmin](docs/Model/StreamResponseListAdmin.md)
- [StreamResponseViewerCount](docs/Model/StreamResponseViewerCount.md)
- [TranslationGlossaryEntry](docs/Model/TranslationGlossaryEntry.md)
- [WebhookCallRequest](docs/Model/WebhookCallRequest.md)
- [WebhookRequest](docs/Model/WebhookRequest.md)
- [WebhookResponse](docs/Model/WebhookResponse.md)

## Authorization
Endpoints do not require authorization.

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `5.4.3`
    - Generator version: `7.19.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
