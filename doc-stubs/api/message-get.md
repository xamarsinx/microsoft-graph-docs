---
title: "Get message"
description: "Read the properties and relationships of a message object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get message
Namespace: microsoft.graph

Read the properties and relationships of a [message](../resources/message.md) object.

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
GET /users/{usersId}/messages/{messageId}
GET /users/{usersId}/mailFolders/{mailFolderId}/messages/{messageId}
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [message](../resources/message.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_message"
}
-->
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/messages/{messageId}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
}
-->
``` http
HTTP/1.1 200 OK

Content-Type: application/json
{
  "value": {
    "@odata.type": "#microsoft.graph.message",
    "id": "ca97281a-281a-ca97-1a28-97ca1a2897ca",
    "createdDateTime": "String (timestamp)",
    "lastModifiedDateTime": "String (timestamp)",
    "changeKey": "String",
    "categories": [
      "String"
    ],
    "receivedDateTime": "String (timestamp)",
    "sentDateTime": "String (timestamp)",
    "hasAttachments": "Boolean",
    "internetMessageId": "String",
    "internetMessageHeaders": [
      {
        "@odata.type": "microsoft.graph.internetMessageHeader"
      }
    ],
    "subject": "String",
    "body": {
      "@odata.type": "microsoft.graph.itemBody"
    },
    "bodyPreview": "String",
    "importance": "String",
    "parentFolderId": "String",
    "sender": {
      "@odata.type": "microsoft.graph.recipient"
    },
    "from": {
      "@odata.type": "microsoft.graph.recipient"
    },
    "toRecipients": [
      {
        "@odata.type": "microsoft.graph.recipient"
      }
    ],
    "ccRecipients": [
      {
        "@odata.type": "microsoft.graph.recipient"
      }
    ],
    "bccRecipients": [
      {
        "@odata.type": "microsoft.graph.recipient"
      }
    ],
    "replyTo": [
      {
        "@odata.type": "microsoft.graph.recipient"
      }
    ],
    "conversationId": "String",
    "conversationIndex": "Binary",
    "uniqueBody": {
      "@odata.type": "microsoft.graph.itemBody"
    },
    "isDeliveryReceiptRequested": "Boolean",
    "isReadReceiptRequested": "Boolean",
    "isRead": "Boolean",
    "isDraft": "Boolean",
    "webLink": "String",
    "mentionsPreview": {
      "@odata.type": "microsoft.graph.mentionsPreview"
    },
    "inferenceClassification": "String",
    "unsubscribeData": [
      "String"
    ],
    "unsubscribeEnabled": "Boolean",
    "flag": {
      "@odata.type": "microsoft.graph.followupFlag"
    }
  }
}
```
