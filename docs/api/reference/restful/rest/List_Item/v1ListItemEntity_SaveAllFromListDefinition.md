---
title: PUT List/{id}/Items
uid: v1ListItemEntity_SaveAllFromListDefinition
---

# PUT List/{id}/Items

```http
PUT /api/v1/List/{udListDefinitionId}/Items
```

Save all list items for the specified list defintion

| Path Part | Type | Description |
|-----------|------|-------------|
| udListDefinitionId | int32 | The id of the list definition, indicating which list to save the items to. Negative numbers indicate TableNumber value instead of UDListDefId. e.g. -64 = category. **Required** |

## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Content-Type | Content-type of the request body: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |

## Request Body: items

The list items

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The identity of the list item |
| Name | string | The name of the list item |
| Tooltip | string | The tooltip of the list item |
| Deleted | bool | True if the list item is marked as deleted |
| UdListDefinitionId | int32 | The id of the list which this list item belongs to |
| Rank | int32 | The rank of the list item |

## Response: array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The identity of the list item |
| Name | string | The name of the list item |
| Tooltip | string | The tooltip of the list item |
| Deleted | bool | True if the list item is marked as deleted |
| UdListDefinitionId | int32 | The id of the list which this list item belongs to |
| Rank | int32 | The rank of the list item |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
PUT /api/v1/List/{udListDefinitionId}/Items
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 648,
    "Name": "Wilkinson, Lesch and Lowe",
    "Tooltip": "et",
    "Deleted": true,
    "UdListDefinitionId": 806,
    "Rank": 84
  },
  {
    "Id": 648,
    "Name": "Wilkinson, Lesch and Lowe",
    "Tooltip": "et",
    "Deleted": true,
    "UdListDefinitionId": 806,
    "Rank": 84
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 862,
    "Name": "Rohan-Nienow",
    "Tooltip": "natus",
    "Deleted": true,
    "UdListDefinitionId": 105,
    "Rank": 787,
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 54
      }
    }
  }
]
```
