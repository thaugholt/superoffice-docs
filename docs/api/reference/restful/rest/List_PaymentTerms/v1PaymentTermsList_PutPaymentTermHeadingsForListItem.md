---
title: PUT List/PaymentTerm/Items/{id}/Headings
uid: v1PaymentTermsList_PutPaymentTermHeadingsForListItem
---

# PUT List/PaymentTerm/Items/{id}/Headings

```http
PUT /api/v1/List/PaymentTerm/Items/{itemId}/Headings
```

Saves headings for the PaymentTerm list's item.

Calls the List agent service SaveHeadingsForListItemFromListDefinition.

| Path Part | Type | Description |
|-----------|------|-------------|
| itemId | int32 | The ID of the headings to be saved. **Required** |

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

## Request Body: entities

The headings to be saved.

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The Id of the ListItem |
| Name | string | The name of the ListItem |
| ToolTip | string | The tooltip of the ListItem |
| Deleted | bool | The deleted status of the ListItem |
| Rank | int32 | The rank of the ListItem |
| Type | string | The type of the ListItem. Custom field. |
| ColorBlock | int32 | The color indicator of the ListItem color block |
| IconHint | string | The Icon hint of the ListItem. Custom field. |
| Selected | bool | True if the ListItem is selected |
| LastChanged | date-time | Time of last change. |
| ChildItems | array | The child items of the SelectableMDOListItem |
| ExtraInfo | string | Extra information added to the ListItem. Could be information such as sort order etc or other meta data. Custom field. |
| StyleHint | string | Style hint indicating, information such as background color etc. Custom field. |
| Hidden | bool | True if the ListItem is hidden |
| FullName | string | The name of the ListItem in its context |

## Response: array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The Id of the ListItem |
| Name | string | The name of the ListItem |
| ToolTip | string | The tooltip of the ListItem |
| Deleted | bool | The deleted status of the ListItem |
| Rank | int32 | The rank of the ListItem |
| Type | string | The type of the ListItem. Custom field. |
| ColorBlock | int32 | The color indicator of the ListItem color block |
| IconHint | string | The Icon hint of the ListItem. Custom field. |
| Selected | bool | True if the ListItem is selected |
| LastChanged | date-time | Time of last change. |
| ChildItems | array | The child items of the SelectableMDOListItem |
| ExtraInfo | string | Extra information added to the ListItem. Could be information such as sort order etc or other meta data. Custom field. |
| StyleHint | string | Style hint indicating, information such as background color etc. Custom field. |
| Hidden | bool | True if the ListItem is hidden |
| FullName | string | The name of the ListItem in its context |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
PUT /api/v1/List/PaymentTerm/Items/{itemId}/Headings
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 453,
    "Name": "Smitham-Rohan",
    "ToolTip": "Eos at non aut autem.",
    "Deleted": true,
    "Rank": 459,
    "Type": "ea",
    "ColorBlock": 110,
    "IconHint": "possimus",
    "Selected": false,
    "LastChanged": "2000-05-24T11:10:54.3459022+02:00",
    "ChildItems": [
      {
        "Id": 516,
        "Name": "Reinger, Kulas and Luettgen",
        "ToolTip": "Dicta omnis aut.",
        "Deleted": true,
        "Rank": 63,
        "Type": "illo",
        "ColorBlock": 569,
        "IconHint": "earum",
        "Selected": false,
        "LastChanged": "1995-05-30T11:10:54.3459022+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "laborum",
        "StyleHint": "animi",
        "Hidden": false,
        "FullName": "Mrs. Bradford Jillian Homenick"
      }
    ],
    "ExtraInfo": "dolorem",
    "StyleHint": "aut",
    "Hidden": false,
    "FullName": "Kylie Effertz"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 140,
    "Name": "Heidenreich, Koepp and Ondricka",
    "ToolTip": "Reprehenderit laudantium.",
    "Deleted": true,
    "Rank": 813,
    "Type": "quo",
    "ColorBlock": 56,
    "IconHint": "quidem",
    "Selected": false,
    "LastChanged": "2013-08-25T11:10:54.3479023+02:00",
    "ChildItems": [
      {
        "Id": 754,
        "Name": "Hayes-Parisian",
        "ToolTip": "Harum error quos rerum dolore.",
        "Deleted": false,
        "Rank": 22,
        "Type": "laboriosam",
        "ColorBlock": 690,
        "IconHint": "omnis",
        "Selected": true,
        "LastChanged": "2021-12-17T11:10:54.3479023+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "repellendus",
        "StyleHint": "qui",
        "Hidden": true,
        "FullName": "Prof. Gracie Renner PhD",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 139
          }
        }
      }
    ],
    "ExtraInfo": "aut",
    "StyleHint": "reprehenderit",
    "Hidden": false,
    "FullName": "Elda McGlynn",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.String",
        "FieldLength": 827
      }
    }
  }
]
```