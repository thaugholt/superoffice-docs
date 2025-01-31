---
title: PUT List/Competitor/Items/{id}/UserGroups
uid: v1CompetitorList_PutCompetitorUserGroupsForListItem
---

# PUT List/Competitor/Items/{id}/UserGroups

```http
PUT /api/v1/List/Competitor/Items/{itemId}/UserGroups
```

Saves user groups visible for the Competitor list's item.

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
PUT /api/v1/List/Competitor/Items/{itemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 689,
    "Name": "Crist, Marquardt and Conn",
    "ToolTip": "Sunt numquam et.",
    "Deleted": true,
    "Rank": 268,
    "Type": "et",
    "ColorBlock": 154,
    "IconHint": "aut",
    "Selected": false,
    "LastChanged": "2012-09-24T11:10:53.9611851+02:00",
    "ChildItems": [
      {
        "Id": 487,
        "Name": "Lehner Inc and Sons",
        "ToolTip": "Praesentium totam laboriosam ut.",
        "Deleted": true,
        "Rank": 658,
        "Type": "ut",
        "ColorBlock": 896,
        "IconHint": "nobis",
        "Selected": false,
        "LastChanged": "1999-12-17T11:10:53.9621856+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "at",
        "StyleHint": "doloribus",
        "Hidden": false,
        "FullName": "Dr. Mateo Brooklyn Casper"
      }
    ],
    "ExtraInfo": "et",
    "StyleHint": "rerum",
    "Hidden": true,
    "FullName": "Jerod Farrell"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 159,
    "Name": "Hilll-Leuschke",
    "ToolTip": "Quam quas dolore sed molestias eos.",
    "Deleted": true,
    "Rank": 820,
    "Type": "commodi",
    "ColorBlock": 32,
    "IconHint": "perferendis",
    "Selected": false,
    "LastChanged": "2012-05-06T11:10:53.9631856+02:00",
    "ChildItems": [
      {
        "Id": 455,
        "Name": "Blick-Larkin",
        "ToolTip": "Explicabo officia.",
        "Deleted": false,
        "Rank": 440,
        "Type": "molestiae",
        "ColorBlock": 20,
        "IconHint": "quos",
        "Selected": true,
        "LastChanged": "2014-10-24T11:10:53.9631856+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "expedita",
        "StyleHint": "molestias",
        "Hidden": false,
        "FullName": "Mrs. Baby Anne Ernser",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 210
          }
        }
      }
    ],
    "ExtraInfo": "aperiam",
    "StyleHint": "reprehenderit",
    "Hidden": false,
    "FullName": "Miss Lucio Madisyn Marks Jr.",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 914
      }
    }
  }
]
```
