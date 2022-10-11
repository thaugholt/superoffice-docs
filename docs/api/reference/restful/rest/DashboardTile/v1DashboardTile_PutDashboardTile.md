---
title: PUT DashboardTile/{id}
uid: v1DashboardTile_PutDashboardTile
---

# PUT DashboardTile/{id}

```http
PUT /api/v1/DashboardTile/{id}
```

Updates the existing DashboardTile

| Path Part | Type | Description |
|-----------|------|-------------|
| id | int32 | The DashboardTile id to update. **Required** |

## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category" Default = show all fields. |

```http
PUT /api/v1/DashboardTile/{id}?$select=name,department,category/id
```

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

## Request Body: entity

The DashboardTile to be saved.

| Property Name | Type |  Description |
|----------------|------|--------------|
| DashboardTileId | int32 | The tile id |
| Caption | string | The tile caption |
| Description | string | The tile description |
| ChartName | string | The original chart name |
| ChartId | string | The original chart Id |
| IsDefault | bool | True if this is one of the default tiles |
| AssociateId | int32 | Id of the associate who owns this tile |
| GroupId | int32 | Id of the associates primary group at storage time |
| SelectionId | int32 | The selection that defines the data filter/restrictions |
| Config | string | The tile config |
| Type | string | The tile type, what kind of tile this is |
| EntityType | string | The tile entity type |
| Options | array | The tile options |
| VisibleFor | array | The set of users or groups the record is visible for |

## Response

DashboardTile updated.

| Response | Description |
|----------------|-------------|
| 200 | DashboardTile updated. |
| 400 | Bad request. Entity to save is not in request body. |

Response body:

| Property Name | Type |  Description |
|----------------|------|--------------|
| DashboardTileId | int32 | The tile id |
| Caption | string | The tile caption |
| Description | string | The tile description |
| ChartName | string | The original chart name |
| ChartId | string | The original chart Id |
| IsDefault | bool | True if this is one of the default tiles |
| AssociateId | int32 | Id of the associate who owns this tile |
| GroupId | int32 | Id of the associates primary group at storage time |
| SelectionId | int32 | The selection that defines the data filter/restrictions |
| Config | string | The tile config |
| Type | string | The tile type, what kind of tile this is |
| EntityType | string | The tile entity type |
| Options | array | The tile options |
| VisibleFor | array | The set of users or groups the record is visible for |
| TableRight |  |  |
| FieldProperties | object |  |
| _Links | object |  |

## Sample request

```http!
PUT /api/v1/DashboardTile/{id}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "DashboardTileId": 498,
  "Caption": "debitis",
  "Description": "Customizable maximized database",
  "ChartName": "Hudson, Rosenbaum and Gislason",
  "ChartId": "voluptatem",
  "IsDefault": true,
  "AssociateId": 967,
  "GroupId": 125,
  "SelectionId": 62,
  "Config": "sint",
  "Type": "Bignum",
  "EntityType": "Activity",
  "Options": [
    {
      "Name": "Nienow-Schroeder",
      "Description": "Configurable 6th generation ability",
      "Type": "Boolean",
      "ListName": "Kohler-Brekke",
      "ListItems": [
        {},
        {}
      ],
      "Value": "ea",
      "DefaultDataOption": true
    }
  ],
  "VisibleFor": [
    {
      "VisibleId": 881,
      "Visibility": "All",
      "DisplayValue": "officia"
    },
    {
      "VisibleId": 881,
      "Visibility": "All",
      "DisplayValue": "officia"
    }
  ]
}
```

## Sample response

```http_
HTTP/1.1 200 DashboardTile updated.
Content-Type: application/json; charset=utf-8

{
  "DashboardTileId": 715,
  "Caption": "dicta",
  "Description": "Re-engineered cohesive budgetary management",
  "ChartName": "Willms Inc and Sons",
  "ChartId": "vel",
  "IsDefault": true,
  "AssociateId": 73,
  "GroupId": 481,
  "SelectionId": 93,
  "Config": "corrupti",
  "Type": "Bignum",
  "EntityType": "Activity",
  "Options": [
    {
      "Name": "Huel, O'Kon and Boyle",
      "Description": "Progressive contextually-based knowledge user",
      "Type": "Boolean",
      "ListName": "Abshire, O'Hara and Cruickshank",
      "ListItems": [
        {},
        {}
      ],
      "Value": "ea",
      "DefaultDataOption": false,
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 862
        }
      }
    }
  ],
  "VisibleFor": [
    {
      "VisibleId": 253,
      "Visibility": "All",
      "DisplayValue": "consectetur",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 272
        }
      }
    },
    {
      "VisibleId": 253,
      "Visibility": "All",
      "DisplayValue": "consectetur",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 272
        }
      }
    }
  ],
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 992
    }
  },
  "_Links": {
    "Self": "https://www.example.com/api/v1/project/321",
    "Archive": "https://www.example.com/api/v1/project"
  }
}
```