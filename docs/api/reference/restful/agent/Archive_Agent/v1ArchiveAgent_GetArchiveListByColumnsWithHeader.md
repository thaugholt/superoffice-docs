---
title: POST Agents/Archive/GetArchiveListByColumnsWithHeader
uid: v1ArchiveAgent_GetArchiveListByColumnsWithHeader
---

# POST Agents/Archive/GetArchiveListByColumnsWithHeader

```http
POST /api/v1/Agents/Archive/GetArchiveListByColumnsWithHeader
```

Get a page of results for an archive list, explicitly specifying the restrictions, orderby and chosen columns; as well as a name/value string formatted set of options.

The return value includes a header that has various extra information, in addition to the actual rows.
Archive Restriction Info objects represent search terms.

Column names and operator strings are defined elsewhere.

Values should be encoded using the CultureDataFormatter, so 10 is "[I:10]".
Default string encodings should be handled ok, but beware of non-invariant cultures leading to incorrect date and float parsing.

```

var restriction1 = new ArchiveRestrictionInfo("category", "equals", "[I:10]");

```

## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/Archive/GetArchiveListByColumnsWithHeader?$select=name,department,category/id
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

## Request Body: request

ProviderName, Columns, SortOrder, Restriction, Entities, Page, PageSize, Options

| Property Name | Type |  Description |
|----------------|------|--------------|
| ProviderName | string |  |
| Columns | array |  |
| SortOrder | array |  |
| Restriction | array |  |
| Entities | array |  |
| Page | int32 |  |
| PageSize | int32 |  |
| Options | string |  |

## Response

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body:

| Property Name | Type |  Description |
|----------------|------|--------------|
| RowCount | int32 | Count of rows, independent of paging. If you order up page 1 with page size 50, the row count may still be 279, that being the number of rows that would have been returned in a  paging-off situation |
| Rows | array | The actual rows, according to the paging info, of the result. See RowCount for a paging-independent count estimate |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Archive/GetArchiveListByColumnsWithHeader
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "ProviderName": "Schowalter-Kerluke",
  "Columns": [
    "aut",
    "et"
  ],
  "SortOrder": [
    {
      "Name": "Ruecker, Reinger and Zboncak",
      "Direction": "ASC"
    },
    {
      "Name": "Ruecker, Reinger and Zboncak",
      "Direction": "ASC"
    }
  ],
  "Restriction": [
    {
      "Name": "Hermann Inc and Sons",
      "Operator": "aut",
      "Values": [
        "recusandae",
        "ab"
      ],
      "DisplayValues": [
        "voluptatum",
        "quis"
      ],
      "ColumnInfo": null,
      "IsActive": false,
      "SubRestrictions": [
        {},
        {}
      ],
      "InterParenthesis": 711,
      "InterOperator": "And",
      "UniqueHash": 262
    }
  ],
  "Entities": [
    "corporis",
    "et"
  ],
  "Page": 935,
  "PageSize": 875,
  "Options": "ut"
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "RowCount": 7,
  "Rows": [
    {
      "EntityName": "Koelpin-Raynor",
      "PrimaryKey": 220,
      "ColumnData": {
        "fieldName": {
          "DisplayValue": "ut",
          "TooltipHint": "hic",
          "LinkHint": "nihil"
        }
      },
      "LinkHint": "dolores",
      "StyleHint": "corporis",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 59
        }
      }
    }
  ],
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 626
    }
  }
}
```