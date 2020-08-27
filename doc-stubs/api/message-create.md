---
title: "Create message"
description: "Create a new message object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create message
Namespace: microsoft.graph

Create a new [message](../resources/message.md) object.

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
POST /users/{usersId}/messages
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [message](../resources/message.md) object.

The following table shows the properties that are required when you create the [message](../resources/message.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|createdDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|changeKey|String|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|categories|String collection|**TODO: Add Description** Inherited from [outlookItem](../resources/outlookitem.md)|
|receivedDateTime|DateTimeOffset|**TODO: Add Description**|
|sentDateTime|DateTimeOffset|**TODO: Add Description**|
|hasAttachments|Boolean|**TODO: Add Description**|
|internetMessageId|String|**TODO: Add Description**|
|internetMessageHeaders|[internetMessageHeader](../resources/internetmessageheader.md) collection|**TODO: Add Description**|
|subject|String|**TODO: Add Description**|
|body|[itemBody](../resources/itembody.md)|**TODO: Add Description**|
|bodyPreview|String|**TODO: Add Description**|
|importance|importance|**TODO: Add Description**. Possible values are: `low`, `normal`, `high`.|
|parentFolderId|String|**TODO: Add Description**|
|sender|[recipient](../resources/recipient.md)|**TODO: Add Description**|
|from|[recipient](../resources/recipient.md)|**TODO: Add Description**|
|toRecipients|[recipient](../resources/recipient.md) collection|**TODO: Add Description**|
|ccRecipients|[recipient](../resources/recipient.md) collection|**TODO: Add Description**|
|bccRecipients|[recipient](../resources/recipient.md) collection|**TODO: Add Description**|
|replyTo|[recipient](../resources/recipient.md) collection|**TODO: Add Description**|
|conversationId|String|**TODO: Add Description**|
|conversationIndex|Binary|**TODO: Add Description**|
|uniqueBody|[itemBody](../resources/itembody.md)|**TODO: Add Description**|
|isDeliveryReceiptRequested|Boolean|**TODO: Add Description**|
|isReadReceiptRequested|Boolean|**TODO: Add Description**|
|isRead|Boolean|**TODO: Add Description**|
|isDraft|Boolean|**TODO: Add Description**|
|webLink|String|**TODO: Add Description**|
|mentionsPreview|[mentionsPreview](../resources/mentionspreview.md)|**TODO: Add Description**|
|inferenceClassification|inferenceClassificationType|**TODO: Add Description**. Possible values are: `focused`, `other`.|
|unsubscribeData|String collection|**TODO: Add Description**|
|unsubscribeEnabled|Boolean|**TODO: Add Description**|
|flag|[followupFlag](../resources/followupflag.md)|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [message](../resources/message.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_message_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/messages
Content-Type: application/json
Content-length: 1619

{
  "@odata.type": "#microsoft.graph.message",
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
HTTP/1.1 201 Created

Content-Type: application/json
{
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
```
