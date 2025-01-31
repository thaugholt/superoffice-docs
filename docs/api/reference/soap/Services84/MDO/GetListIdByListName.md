---
title: Services84.MDOAgent.GetListIdByListName SOAP
generated: 1
uid: Services84-MDO-GetListIdByListName
---

# Services84 MDO GetListIdByListName

SOAP request and response examples **Remote/Services84/MDO.svc**
Implemented by the <see cref="M:SuperOffice.Services84.IMDOAgent.GetListIdByListName">SuperOffice.Services84.IMDOAgent.GetListIdByListName</see> method.

## GetListIdByListName

Retrieve the UdListDefinition id of a list, by its name. Not all lists have such an ID, but those that are based on tables do (the list name is then the same as the table name)

* **name:** The list name, same as the table name for lists that are backed by tables

**Returns:** List id in the UdListDefinition table

[WSDL file for Services84/MDO](../Services84-MDO.md)

Obtain a ticket from the [Services84/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetListIdByListName Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices842="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices841="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:MDO="http://www.superoffice.net/ws/crm/NetServer/Services84">
  <MDO:ApplicationToken>1234567-1234-9876</MDO:ApplicationToken>
  <MDO:Credentials>
    <MDO:Ticket>7T:1234abcxyzExample==</MDO:Ticket>
  </MDO:Credentials>
 <SOAP-ENV:Body>
   <MDO:GetListIdByListName>
    <MDO:Name xsi:type="xsd:string"></MDO:Name>
   </MDO:GetListIdByListName>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

## GetListIdByListName Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices842="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices841="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:MDO="http://www.superoffice.net/ws/crm/NetServer/Services84">
 <SOAP-ENV:Body>
  <MDO:GetListIdByListNameResponse>
   <MDO:Response xsi:type="xsd:int">0</MDO:Response>
  </MDO:GetListIdByListNameResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
