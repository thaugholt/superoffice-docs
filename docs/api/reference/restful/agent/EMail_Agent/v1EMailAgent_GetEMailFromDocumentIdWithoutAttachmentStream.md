---
title: POST Agents/EMail/GetEMailFromDocumentIdWithoutAttachmentStream
uid: v1EMailAgent_GetEMailFromDocumentIdWithoutAttachmentStream
---

# POST Agents/EMail/GetEMailFromDocumentIdWithoutAttachmentStream

```http
POST /api/v1/Agents/EMail/GetEMailFromDocumentIdWithoutAttachmentStream
```

Get an e-mail based on an archived document

## Online Restricted: ## The EMail agent is not available in Online by default. Access must be requested specifically when app is registered

## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/EMail/GetEMailFromDocumentIdWithoutAttachmentStream?$select=name,department,category/id
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

DocumentId

| Property Name | Type |  Description |
|----------------|------|--------------|
| DocumentId | int32 |  |

## Response

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body:

| Property Name | Type |  Description |
|----------------|------|--------------|
| To | array | To recipients of e-mail |
| Cc | array | Cc recipients of e-mail |
| Bcc | array | Bcc recipient of e-mail |
| Subject | string | Subject of the e-mail |
| HTMLBody | string | Body formatted in HTML |
| From |  | Who did the e-mail originate from |
| Sent | date-time | When was the e-mail sent |
| Size | int32 | Total size of the e-mail |
| Priority | string | Importance of the e-mail |
| Flags | string | Flag status of this mail (unread, replied, deleted ) |
| MessageID | string | Unique id of e-mails |
| PlainBody | string | Body formatted in plain text |
| IsSent | bool | Is this a sent e-mail (not new) |
| EMailSOInfo |  | Glue between SuperOffice data and an e-mail. |
| ServerId | int32 | Unique id for the e-mail on the server |
| Attachments | array |  |
| CustomHeaderList | array | Non standard e-mail headers |
| FolderName | string | Name of folder the e-mail belongs in |
| EmailItemId | int32 | Primary key |
| AccountId | int32 | Account Id |
| ReceivedAt | date-time | Received date time |
| InReplyTo |  | The envelope of the email this email is a reply to, if it exists |
| RepliedAt | date-time | When this email was replied at |
| HasCalendarData | bool | If this email contains exactly one iCal appointment |
| CalMethod | string | Method stored in the associated iCal appointment. Indicates if the iCal data is a reply, counter proposal etc. |
| CalReplyStatus | string | Reply status stored in calendar data for the ical method is REPLY |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/EMail/GetEMailFromDocumentIdWithoutAttachmentStream
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

{
  "DocumentId": 139
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "To": [
    {
      "ContactId": 662,
      "ContactName": "Grimes-Kihn",
      "PersonId": 432,
      "PersonName": "Romaguera, Jaskolski and Ryan",
      "AssociateId": 946,
      "Address": "nihil",
      "EmailId": 676,
      "DuplicatePersonIds": [
        477,
        618
      ],
      "Name": "Graham, Balistreri and Mitchell",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.String",
          "FieldLength": 389
        }
      }
    }
  ],
  "Cc": [
    {
      "ContactId": 279,
      "ContactName": "Weber, Turner and Kozey",
      "PersonId": 371,
      "PersonName": "Prosacco LLC",
      "AssociateId": 47,
      "Address": "eum",
      "EmailId": 407,
      "DuplicatePersonIds": [
        253,
        987
      ],
      "Name": "Hirthe, Mante and Pfeffer",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 1002
        }
      }
    }
  ],
  "Bcc": [
    {
      "ContactId": 266,
      "ContactName": "Roberts-Kertzmann",
      "PersonId": 947,
      "PersonName": "Romaguera-Von",
      "AssociateId": 523,
      "Address": "magni",
      "EmailId": 198,
      "DuplicatePersonIds": [
        369,
        578
      ],
      "Name": "Littel-Stroman",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 874
        }
      }
    }
  ],
  "Subject": "dolores",
  "HTMLBody": "et",
  "From": null,
  "Sent": "1999-04-07T11:10:26.8694246+02:00",
  "Size": 96,
  "Priority": "High",
  "Flags": "Answered",
  "MessageID": "dolores",
  "PlainBody": "expedita",
  "IsSent": false,
  "EMailSOInfo": null,
  "ServerId": 536,
  "Attachments": [
    {
      "Description": "Persistent coherent local area network",
      "Filename": "qui",
      "Size": 477,
      "Type": "nemo",
      "Encoding": "quidem",
      "Id": "quidem",
      "Disposition": "provident",
      "Stream": "GIF89....File contents as raw bytes...",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 262
        }
      }
    }
  ],
  "CustomHeaderList": [
    {
      "Name": "Kub, Block and Bauch",
      "Values": [
        "aliquid",
        "voluptas"
      ],
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 319
        }
      }
    },
    {
      "Name": "Kub, Block and Bauch",
      "Values": [
        "aliquid",
        "voluptas"
      ],
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 319
        }
      }
    }
  ],
  "FolderName": "Yost-Keebler",
  "EmailItemId": 965,
  "AccountId": 602,
  "ReceivedAt": "2001-04-11T11:10:26.8704248+02:00",
  "InReplyTo": null,
  "RepliedAt": "2009-05-27T11:10:26.8704248+02:00",
  "HasCalendarData": false,
  "CalMethod": "Add",
  "CalReplyStatus": "Accepted",
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.String",
      "FieldLength": 140
    }
  }
}
```
