---
title: POST Agents/EMail/SaveEMailAccount
uid: v1EMailAgent_SaveEMailAccount
---

# POST Agents/EMail/SaveEMailAccount

```http
POST /api/v1/Agents/EMail/SaveEMailAccount
```

Updates the existing EMailAccount or creates a new EMailAccount if the id parameter is empty

## Online Restricted: ## The EMail agent is not available in Online by default. Access must be requested specifically when app is registered

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

The EMailAccount to be saved.

| Property Name | Type |  Description |
|----------------|------|--------------|
| EMailAccountId | int32 | The account primary key |
| EMailAddress | string | The account (from) address |
| AssociateId | int32 | Id of the associate who owns this account |
| IncomingCredentials |  | Account credentials for imap |
| OutgoingCredentials |  | Account credentials for smtp |
| AccountStatus | int32 | The account status (Disabled or...) Readonly field |
| ErrorCount | int32 | Count of concurring errors of fetching email. Readonly field |
| ErrorReason | string | Reason/Error message. Readonly field |
| InboxFolder | string | Inbox folder name if available in the db |
| SentFolder | string | Sent email folder name if available in the db |

## Response

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

Response body:

| Property Name | Type |  Description |
|----------------|------|--------------|
| EMailAccountId | int32 | The account primary key |
| EMailAddress | string | The account (from) address |
| AssociateId | int32 | Id of the associate who owns this account |
| IncomingCredentials |  | Account credentials for imap |
| OutgoingCredentials |  | Account credentials for smtp |
| AccountStatus | int32 | The account status (Disabled or...) Readonly field |
| ErrorCount | int32 | Count of concurring errors of fetching email. Readonly field |
| ErrorReason | string | Reason/Error message. Readonly field |
| InboxFolder | string | Inbox folder name if available in the db |
| SentFolder | string | Sent email folder name if available in the db |
| TableRight |  |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/EMail/SaveEMailAccount
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

{
  "EMailAccountId": 433,
  "EMailAddress": "occaecati",
  "AssociateId": 287,
  "IncomingCredentials": null,
  "OutgoingCredentials": null,
  "AccountStatus": 720,
  "ErrorCount": 890,
  "ErrorReason": "",
  "InboxFolder": "omnis",
  "SentFolder": "voluptatem"
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "EMailAccountId": 272,
  "EMailAddress": "quis",
  "AssociateId": 463,
  "IncomingCredentials": null,
  "OutgoingCredentials": null,
  "AccountStatus": 903,
  "ErrorCount": 365,
  "ErrorReason": "",
  "InboxFolder": "qui",
  "SentFolder": "illum",
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.Int32",
      "FieldLength": 373
    }
  }
}
```
