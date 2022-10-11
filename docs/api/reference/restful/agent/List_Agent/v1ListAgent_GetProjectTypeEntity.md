---
title: POST Agents/List/GetProjectTypeEntity
uid: v1ListAgent_GetProjectTypeEntity
---

# POST Agents/List/GetProjectTypeEntity

```http
POST /api/v1/Agents/List/GetProjectTypeEntity
```

Gets a ProjectTypeEntity object.

## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| projectTypeEntityId | int32 | **Required** The primary key. |
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/List/GetProjectTypeEntity?projectTypeEntityId=161
POST /api/v1/Agents/List/GetProjectTypeEntity?$select=name,department,category/id
```

## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |

## Response

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body:

| Property Name | Type |  Description |
|----------------|------|--------------|
| ProjTypeId | int32 | Primary key |
| Name | string | The list item |
| Tooltip | string | Tooltip or other description |
| Rank | int32 | Rank order |
| DurationUnit | string | Units for the duration |
| ProjectDuration | int32 | Expected duration of project, in given units |
| Deleted | bool | 0 -&gt; record is active 1 -&gt; record is 'deleted' and should not be shown in lists |
| HasGuide | bool | Does this project type have a guide attached |
| IsAutoAdvance | bool | Does the project status advance automatically, when the last guided activity in a status is completed? |
| Stages | array | Stages (project statuses), those associated with this ProjType are selected. |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/List/GetProjectTypeEntity
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "ProjTypeId": 627,
  "Name": "Hagenes Group",
  "Tooltip": "dolorum",
  "Rank": 916,
  "DurationUnit": "Century",
  "ProjectDuration": 438,
  "Deleted": true,
  "HasGuide": false,
  "IsAutoAdvance": false,
  "Stages": [
    {
      "Id": 88,
      "Name": "Hane, Tremblay and Goodwin",
      "ToolTip": "Voluptas consectetur assumenda est vero officiis et.",
      "Deleted": false,
      "Rank": 242,
      "Type": "nesciunt",
      "ColorBlock": 349,
      "IconHint": "qui",
      "Selected": true,
      "LastChanged": "2020-09-29T11:10:27.1394226+02:00",
      "ChildItems": [
        {},
        {}
      ],
      "ExtraInfo": "ipsum",
      "StyleHint": "totam",
      "Hidden": true,
      "FullName": "Brandi Schumm",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 633
        }
      }
    }
  ],
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 507
    }
  }
}
```