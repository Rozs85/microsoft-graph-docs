---
title: "Update educationalactivity"
description: "Update the properties of educationalactivity object."
localization_priority: Normal
author: "kevinbellinger"
ms.prod: "People"
doc_type: "apiPageType"
---

# Update educationalactivity

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of educationalactivity object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Not supported. |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Not supported. |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
PATCH /user/profile/educationalActivities
```

## Request headers

| Name       | Description|
|:-----------|:-----------|
| Authorization | Bearer {token} |

## Request body

In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, don't include existing values that haven't changed.

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|completionMonthYear|Date||
|endMonthYear|Date||
|institution|institutionData||
|program|educationalActivityDetail||
|startMonthYear|Date||

## Response

If successful, this method returns a `200 OK` response code and an updated [educationalActivity](../resources/educationalactivity.md) object in the response body.

## Examples

### Request

The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_educationalactivity"
}-->

```http
PATCH https://graph.microsoft.com/Beta/user/profile/educationalActivities
Content-type: application/json

{
  "completionMonthYear": "datetime-value",
  "endMonthYear": "datetime-value",
  "institution": {
    "description": "description-value",
    "displayName": "displayName-value",
    "location": {
      "type": "type-value",
      "postOfficeBox": "postOfficeBox-value",
      "street": "street-value",
      "city": "city-value",
      "state": "state-value",
      "countryOrRegion": "countryOrRegion-value",
      "postalCode": "postalCode-value"
    },
    "webUrl": "webUrl-value"
  },
  "program": {
    "abbreviation": "abbreviation-value",
    "activities": "activities-value",
    "awards": "awards-value",
    "description": "description-value",
    "displayName": "displayName-value",
    "fieldsOfStudy": "fieldsOfStudy-value",
    "grade": "grade-value",
    "notes": "notes-value",
    "webUrl": "webUrl-value"
  },
  "startMonthYear": "datetime-value"
}
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationalActivity"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "completionMonthYear": "datetime-value",
  "endMonthYear": "datetime-value",
  "institution": {
    "description": "description-value",
    "displayName": "displayName-value",
    "location": {
      "type": "type-value",
      "postOfficeBox": "postOfficeBox-value",
      "street": "street-value",
      "city": "city-value",
      "state": "state-value",
      "countryOrRegion": "countryOrRegion-value",
      "postalCode": "postalCode-value"
    },
    "webUrl": "webUrl-value"
  },
  "program": {
    "abbreviation": "abbreviation-value",
    "activities": "activities-value",
    "awards": "awards-value",
    "description": "description-value",
    "displayName": "displayName-value",
    "fieldsOfStudy": "fieldsOfStudy-value",
    "grade": "grade-value",
    "notes": "notes-value",
    "webUrl": "webUrl-value"
  },
  "startMonthYear": "datetime-value"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationalactivity",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->