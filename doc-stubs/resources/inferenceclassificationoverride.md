---
title: "inferenceClassificationOverride resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# inferenceClassificationOverride resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List overrides](../api/inferenceclassification-list-overrides.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) collection|Get the inferenceClassificationOverrides from the overrides navigation property.|
|[Create overrides](../api/inferenceclassification-post-overrides.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md)|Create a new overrides object.|
|[Update overrides](../api/inferenceclassification-update-overrides.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md)|Update the properties of an overrides object.|
|[Get overrides](../api/inferenceclassification-get-inferenceclassificationoverride.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md)|Read the properties and relationships of an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.|
|[Delete overrides](../api/inferenceclassification-delete-overrides.md)|None|Delete an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.|
|[List inferenceClassificationOverrides](../api/inferenceclassificationoverride-list.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) collection|Get a list of the [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) objects and their properties.|
|[Create inferenceClassificationOverride](../api/inferenceclassificationoverride-create.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md)|Create a new [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.|
|[Get inferenceClassificationOverride](../api/inferenceclassificationoverride-get.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md)|Read the properties and relationships of an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.|
|[Update inferenceClassificationOverride](../api/inferenceclassificationoverride-update.md)|[inferenceClassificationOverride](../resources/inferenceclassificationoverride.md)|Update the properties of an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.|
|[Delete inferenceClassificationOverride](../api/inferenceclassificationoverride-delete.md)|None|Deletes an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|classifyAs|inferenceClassificationType|**TODO: Add Description**. Possible values are: `focused`, `other`.|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|senderEmailAddress|[emailAddress](../resources/emailaddress.md)|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.inferenceClassificationOverride",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.inferenceClassificationOverride",
  "id": "String (identifier)",
  "classifyAs": "String",
  "senderEmailAddress": {
    "@odata.type": "microsoft.graph.emailAddress"
  }
}
```
