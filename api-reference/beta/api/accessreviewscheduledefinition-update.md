---
title: "Update accessReviewScheduleDefinition"
description: "In the Azure AD access reviews feature, update an existing accessReviewScheduleDefinition object to change one or more of its properties."
localization_priority: Normal
author: "isabelleatmsft"
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# Update accessReviewScheduleDefinition

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

>[!NOTE]
>Any updates made to an **accessReviewScheduleDefinition** will only apply to future instances. Currently running instances cannot be updated.
>Additionally, this API is not intended to update properties, including decisions, on the **accessReviewInstance** level. See [accessReviewInstance](../resources/accessreviewinstance.md) for more information on instances.

In the Azure AD [access reviews](../resources/accessreviewsv2-root.md) feature, update an existing [accessReviewScheduleDefinition](../resources/accessreviewscheduledefinition.md) object to change one or more of its properties.


## Permissions
One of the following permissions is required to call this API. Delegated permissions to personal Microsoft accounts are not supported. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type                        | Permissions (from least to most privileged)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegated (work or school account)     | AccessReview.ReadWrite.All |
|Application                            | AccessReview.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
PUT /identityGovernance/accessReviews/definitions/{reviewID}
```
## Request headers
| Name         | Description |
|:-------------|:------------|
| Content-type | application/json. Required. |

## Request body
In the request body, supply a JSON representation of an [accessReviewScheduleDefinition](../resources/accessreviewscheduledefinition.md) object.

The following table shows the properties accepted to update an accessReviewScheduleDefinition.

| Property     | Type       | Description | Additional Notes |
|:-------------|:------------|:------------|:------------|
| `displayName`             |`String`                      | Name of access review series.|
| `descriptionForAdmins`    |`String`                       | Context of the review provided to admins. |
| `descriptionForReviewers` |`String`                         | Context of the review provided to reviewers. |
| `settings`                |`microsoft.graph.accessReviewScheduleSettings`| The settings for an access review series. Recurrence is determined here. See [accessReviewScheduleSettings](../resources/accessreviewscheduledefinition.md). |
| `reviewers`               |`Collection(microsoft.graph.accessReviewReviewerScope)`|  Defines who the reviewers are. If none are specified, the review will be a self-review (users reviewed review their own access). See [accessReviewReviewerScope](../resources/accessreviewscheduledefinition.md). | Reviewers field is only updatable if individual users assigned as reviewers. |

Note that a PUT request expects the full object to be passed in, in addition to the properties being updated.

## Response
If successful, this method returns a `204, Accepted` response code and no response body.

## Example

This is an example of updating the displayName of an existing access review series.

##### Request
In the request body, supply a JSON representation of the new properties of the [accessReviewScheduleDefinition](../resources/accessreviewscheduledefinition.md) object.


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_accessReview"
}-->
```http
PUT https://graph.microsoft.com/beta/identityGovernance/accessReviews/definitions/60860cdd-fb4d-4054-91ba-f75e04444aa6

{
    "id": "60860cdd-fb4d-4054-91ba-f75e04444aa6",
    "displayName": "Test world UPDATED NAME!",
    "descriptionForAdmins": "Test world",
    "descriptionForReviewers": "Test world",
    "scope": {
        "query": "/groups/b7a059cb-038a-4802-8fc9-b9d1ed0cf11f/transitiveMembers",
        "queryType": "MicrosoftGraph"
    },
    "instanceEnumerationScope": {
        "query": "/groups/b7a059cb-038a-4802-8fc9-b9d1ed0cf11f",
        "queryType": "MicrosoftGraph"
    },
    "reviewers": [],
    "settings": {
        "mailNotificationsEnabled": true,
        "reminderNotificationsEnabled": true,
        "justificationRequiredOnApproval": true,
        "defaultDecisionEnabled": false,
        "defaultDecision": "None",
        "instanceDurationInDays": 3,
        "autoApplyDecisionsEnabled": false,
        "recommendationsEnabled": true,
        "recurrence": {
            "pattern": {
                "type": "weekly",
                "interval": 1
            },
            "range": {
                "type": "noEnd",
                "startDate": "2020-09-15"
            }
        }
    }
}
```
# [C#](#tab/csharp)
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### Response
>**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview"
} -->
```http
HTTP/1.1 204 Accepted
```

<!--
{
  "type": "#page.annotation",
  "description": "Update accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->