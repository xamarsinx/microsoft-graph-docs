---
title: "Create calendar"
description: "Create a new calendar object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create calendar
Namespace: microsoft.graph

Create a new [calendar](../resources/calendar.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/calendars
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [calendar](../resources/calendar.md) object.

The following table shows the properties that are required when you create the [calendar](../resources/calendar.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|name|String|**TODO: Add Description**|
|color|calendarColor|**TODO: Add Description**. Possible values are: `lightBlue`, `lightGreen`, `lightOrange`, `lightGray`, `lightYellow`, `lightTeal`, `lightPink`, `lightBrown`, `lightRed`, `maxColor`, `auto`.|
|hexColor|String|**TODO: Add Description**|
|isDefaultCalendar|Boolean|**TODO: Add Description**|
|changeKey|String|**TODO: Add Description**|
|canShare|Boolean|**TODO: Add Description**|
|canViewPrivateItems|Boolean|**TODO: Add Description**|
|isShared|Boolean|**TODO: Add Description**|
|isSharedWithMe|Boolean|**TODO: Add Description**|
|canEdit|Boolean|**TODO: Add Description**|
|owner|[emailAddress](../resources/emailaddress.md)|**TODO: Add Description**|
|calendarGroupId|String|**TODO: Add Description**|
|allowedOnlineMeetingProviders|onlineMeetingProviderType collection|**TODO: Add Description**. Possible values are: `unknown`, `skypeForBusiness`, `skypeForConsumer`, `teamsForBusiness`.|
|defaultOnlineMeetingProvider|onlineMeetingProviderType|**TODO: Add Description**. Possible values are: `unknown`, `skypeForBusiness`, `skypeForConsumer`, `teamsForBusiness`.|
|isTallyingResponses|Boolean|**TODO: Add Description**|
|isRemovable|Boolean|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [calendar](../resources/calendar.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_calendar_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/calendars
Content-Type: application/json
Content-length: 597

{
  "@odata.type": "#microsoft.graph.calendar",
  "name": "String",
  "color": "String",
  "hexColor": "String",
  "isDefaultCalendar": "Boolean",
  "changeKey": "String",
  "canShare": "Boolean",
  "canViewPrivateItems": "Boolean",
  "isShared": "Boolean",
  "isSharedWithMe": "Boolean",
  "canEdit": "Boolean",
  "owner": {
    "@odata.type": "microsoft.graph.emailAddress"
  },
  "calendarGroupId": "String",
  "allowedOnlineMeetingProviders": [
    "String"
  ],
  "defaultOnlineMeetingProvider": "String",
  "isTallyingResponses": "Boolean",
  "isRemovable": "Boolean"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
}
-->
``` http
HTTP/1.1 201 Created

Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.calendar",
  "id": "813c5e4f-5e4f-813c-4f5e-3c814f5e3c81",
  "name": "String",
  "color": "String",
  "hexColor": "String",
  "isDefaultCalendar": "Boolean",
  "changeKey": "String",
  "canShare": "Boolean",
  "canViewPrivateItems": "Boolean",
  "isShared": "Boolean",
  "isSharedWithMe": "Boolean",
  "canEdit": "Boolean",
  "owner": {
    "@odata.type": "microsoft.graph.emailAddress"
  },
  "calendarGroupId": "String",
  "allowedOnlineMeetingProviders": [
    "String"
  ],
  "defaultOnlineMeetingProvider": "String",
  "isTallyingResponses": "Boolean",
  "isRemovable": "Boolean"
}
```
