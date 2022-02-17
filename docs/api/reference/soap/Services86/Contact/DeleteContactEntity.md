---
title: Services86.ContactAgent.DeleteContactEntity SOAP
generated: 1
uid: Services86-Contact-DeleteContactEntity
---

# Services86 Contact DeleteContactEntity

SOAP request and response examples **Remote/Services86/Contact.svc**
Implemented by the <see cref="M:SuperOffice.Services86.IContactAgent.DeleteContactEntity">SuperOffice.Services86.IContactAgent.DeleteContactEntity</see> method.

## DeleteContactEntity

Deletes the ContactEntity.
This table supports Soft Delete; records will be marked as deleted and disappear from the GUI and API results, but will not be physically deleted by this (and any other) method.

* **contactEntityId:** The identity of the ContactEntity



[WSDL file for Services86/Contact](../Services86-Contact.md)

Obtain a ticket from the [Services86/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## DeleteContactEntity Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices862="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices861="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Contact="http://www.superoffice.net/ws/crm/NetServer/Services86">
  <Contact:ApplicationToken>1234567-1234-9876</Contact:ApplicationToken>
  <Contact:Credentials>
    <Contact:Ticket>7T:1234abcxyzExample==</Contact:Ticket>
  </Contact:Credentials>
 <SOAP-ENV:Body>
   <Contact:DeleteContactEntity>
    <Contact:ContactEntityId xsi:type="xsd:int">0</Contact:ContactEntityId>
   </Contact:DeleteContactEntity>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## DeleteContactEntity Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices862="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices861="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Contact="http://www.superoffice.net/ws/crm/NetServer/Services86">
 <SOAP-ENV:Body>
  <Contact:DeleteContactEntityResponse>
  </Contact:DeleteContactEntityResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
