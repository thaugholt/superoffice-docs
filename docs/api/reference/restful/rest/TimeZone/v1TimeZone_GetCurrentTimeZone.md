---
title: GET TimeZone/current
uid: v1TimeZone_GetCurrentTimeZone
---

# GET TimeZone/current

```http
GET /api/v1/TimeZone/current
```

Base Time Zone info.

This is the time zone used internally for storing data.

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
| TZLocationID | int32 |  |
| Name | string |  |
| TZLocationCode | string |  |
| TZLocationCities | string |  |
| IsoNumber | int32 |  |
| TimeZoneSTDRules | object |  |
| TimeZoneDSTRules | object |  |

## Sample request

```http!
GET /api/v1/TimeZone/current
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "TZLocationID": 50,
  "Name": "Carroll Inc and Sons",
  "TZLocationCode": "repudiandae",
  "TZLocationCities": "omnis",
  "IsoNumber": 922,
  "TimeZoneSTDRules": {
    "fieldName": {
      "StartDay": 573,
      "StartMonth": 600,
      "EndDay": 196,
      "EndMonth": 837,
      "TZOffset": 888,
      "StartRulePattern": "rerum",
      "EndRulePattern": "praesentium"
    }
  },
  "TimeZoneDSTRules": {
    "fieldName": {
      "StartDay": 335,
      "StartMonth": 701,
      "EndDay": 210,
      "EndMonth": 779,
      "TZOffset": 679,
      "StartRulePattern": "ut",
      "EndRulePattern": "culpa"
    }
  }
}
```