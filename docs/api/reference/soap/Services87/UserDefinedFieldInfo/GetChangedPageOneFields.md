---
title: Services87.UserDefinedFieldInfoAgent.GetChangedPageOneFields SOAP
generated: 1
uid: Services87-UserDefinedFieldInfo-GetChangedPageOneFields
---

# Services87 UserDefinedFieldInfo GetChangedPageOneFields

SOAP request and response examples **Remote/Services87/UserDefinedFieldInfo.svc**
Implemented by the <see cref="M:SuperOffice.Services87.IUserDefinedFieldInfoAgent.GetChangedPageOneFields">SuperOffice.Services87.IUserDefinedFieldInfoAgent.GetChangedPageOneFields</see> method.

## GetChangedPageOneFields

Gets which page one fields have changed from the current version

* **ownerType:** The user-defined field owner-entity.
* **userGroupId:** Id of UserGroup

[WSDL file for Services87/UserDefinedFieldInfo](../Services87-UserDefinedFieldInfo.md)

Obtain a ticket from the [Services87/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetChangedPageOneFields Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices872="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices871="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:UserDefinedFieldInfo="http://www.superoffice.net/ws/crm/NetServer/Services87">
  <UserDefinedFieldInfo:ApplicationToken>1234567-1234-9876</UserDefinedFieldInfo:ApplicationToken>
  <UserDefinedFieldInfo:Credentials>
    <UserDefinedFieldInfo:Ticket>7T:1234abcxyzExample==</UserDefinedFieldInfo:Ticket>
  </UserDefinedFieldInfo:Credentials>
 <SOAP-ENV:Body>
   <UserDefinedFieldInfo:GetChangedPageOneFields>
    <UserDefinedFieldInfo:OwnerType xsi:type="UserDefinedFieldInfo:UDefType">Invalid</UserDefinedFieldInfo:OwnerType>
    <UserDefinedFieldInfo:UserGroupId xsi:type="xsd:int">0</UserDefinedFieldInfo:UserGroupId>
   </UserDefinedFieldInfo:GetChangedPageOneFields>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

## GetChangedPageOneFields Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices872="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices871="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:UserDefinedFieldInfo="http://www.superoffice.net/ws/crm/NetServer/Services87">
 <SOAP-ENV:Body>
  <UserDefinedFieldInfo:GetChangedPageOneFieldsResponse>
   <UserDefinedFieldInfo:Response xsi:type="NetServerServices872:ArrayOfboolean">
    <NetServerServices872:boolean xsi:type="xsd:boolean">false</NetServerServices872:boolean>
   </UserDefinedFieldInfo:Response>
  </UserDefinedFieldInfo:GetChangedPageOneFieldsResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
