---
title: PUT List/Reason/Items/{id}/UserGroups
uid: v1ReasonList_PutReasonUserGroupsForListItem
---

# PUT List/Reason/Items/{id}/UserGroups

```http
PUT /api/v1/List/Reason/Items/{itemId}/UserGroups
```

Saves user groups visible for the Reason list's item.

Calls the List agent service SaveHeadingsForListItemFromListDefinition.

| Path Part | Type | Description |
|-----------|------|-------------|
| itemId | int32 | The ID of the item to save. **Required** |

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
PUT /api/v1/List/Reason/Items/{itemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 198,
    "Name": "Stiedemann, Stiedemann and Stokes",
    "ToolTip": "Id ullam enim ut.",
    "Deleted": true,
    "Rank": 952,
    "Type": "asperiores",
    "ColorBlock": 349,
    "IconHint": "ea",
    "Selected": false,
    "LastChanged": "2010-05-11T11:10:54.5509324+02:00",
    "ChildItems": [
      {
        "Id": 125,
        "Name": "Grady Group",
        "ToolTip": "Quisquam cumque.",
        "Deleted": false,
        "Rank": 720,
        "Type": "quasi",
        "ColorBlock": 939,
        "IconHint": "sed",
        "Selected": true,
        "LastChanged": "2016-11-20T11:10:54.5509324+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "eveniet",
        "StyleHint": "rerum",
        "Hidden": false,
        "FullName": "Zita Wiza"
      }
    ],
    "ExtraInfo": "tempore",
    "StyleHint": "odio",
    "Hidden": false,
    "FullName": "Miss Eli Tito Gutmann"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 318,
    "Name": "Jones-Little",
    "ToolTip": "Possimus architecto cum.",
    "Deleted": false,
    "Rank": 490,
    "Type": "dolorum",
    "ColorBlock": 451,
    "IconHint": "accusantium",
    "Selected": true,
    "LastChanged": "1996-12-11T11:10:54.5529312+01:00",
    "ChildItems": [
      {
        "Id": 273,
        "Name": "Stark Group",
        "ToolTip": "Qui ut in dolorum est.",
        "Deleted": false,
        "Rank": 227,
        "Type": "facilis",
        "ColorBlock": 584,
        "IconHint": "ex",
        "Selected": false,
        "LastChanged": "1997-05-17T11:10:54.5529312+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "laudantium",
        "StyleHint": "provident",
        "Hidden": false,
        "FullName": "Gardner Kuvalis",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 350
          }
        }
      }
    ],
    "ExtraInfo": "reiciendis",
    "StyleHint": "aspernatur",
    "Hidden": false,
    "FullName": "Joaquin Bartoletti",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 792
      }
    }
  }
]
```