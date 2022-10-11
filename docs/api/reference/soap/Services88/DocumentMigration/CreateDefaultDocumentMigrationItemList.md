---
title: Services88.DocumentMigrationAgent.CreateDefaultDocumentMigrationItemList SOAP
generated: 1
uid: Services88-DocumentMigration-CreateDefaultDocumentMigrationItemList
---

# Services88 DocumentMigration CreateDefaultDocumentMigrationItemList

SOAP request and response examples **Remote/Services88/DocumentMigration.svc**
Implemented by the <see cref="M:SuperOffice.Services88.IDocumentMigrationAgent.CreateDefaultDocumentMigrationItemList">SuperOffice.Services88.IDocumentMigrationAgent.CreateDefaultDocumentMigrationItemList</see> method.

## CreateDefaultDocumentMigrationItemList

Loading default values into a new DocumentMigrationItemList.
NetServer calculates default values (e.g. Country) on the entity, which is required when creating/storing a new instance
<para /><b>Online Restricted:</b> The DocumentMigration agent is not available in Online by default. Access must be requested specifically when app is registered. Intended for SuperOffice-internal apps.

**Returns:** New DocumentMigrationItemList with default values

[WSDL file for Services88/DocumentMigration](../Services88-DocumentMigration.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## CreateDefaultDocumentMigrationItemList Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:DocumentMigration="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <DocumentMigration:ApplicationToken>1234567-1234-9876</DocumentMigration:ApplicationToken>
  <DocumentMigration:Credentials>
    <DocumentMigration:Ticket>7T:1234abcxyzExample==</DocumentMigration:Ticket>
  </DocumentMigration:Credentials>
 <SOAP-ENV:Body>
   <DocumentMigration:CreateDefaultDocumentMigrationItemList>
   </DocumentMigration:CreateDefaultDocumentMigrationItemList>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

## CreateDefaultDocumentMigrationItemList Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:DocumentMigration="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <DocumentMigration:CreateDefaultDocumentMigrationItemListResponse>
   <DocumentMigration:Response xsi:type="DocumentMigration:DocumentMigrationItemList">
    <DocumentMigration:NumDocumentsOmitted xsi:type="xsd:int">0</DocumentMigration:NumDocumentsOmitted>
    <DocumentMigration:NumDocumentsAlreadyMigrated xsi:type="xsd:int">0</DocumentMigration:NumDocumentsAlreadyMigrated>
    <DocumentMigration:Documents xsi:type="DocumentMigration:ArrayOfDocumentMigrationItem">
     <DocumentMigration:DocumentMigrationItem xsi:type="DocumentMigration:DocumentMigrationItem">
      <DocumentMigration:DocumentId xsi:type="xsd:int">0</DocumentMigration:DocumentId>
      <DocumentMigration:ContactId xsi:type="xsd:int">0</DocumentMigration:ContactId>
      <DocumentMigration:PersonId xsi:type="xsd:int">0</DocumentMigration:PersonId>
      <DocumentMigration:SaleId xsi:type="xsd:int">0</DocumentMigration:SaleId>
      <DocumentMigration:ProjectId xsi:type="xsd:int">0</DocumentMigration:ProjectId>
      <DocumentMigration:DocTmplId xsi:type="xsd:int">0</DocumentMigration:DocTmplId>
      <DocumentMigration:AssociateId xsi:type="xsd:int">0</DocumentMigration:AssociateId>
      <DocumentMigration:UserGroupId xsi:type="xsd:int">0</DocumentMigration:UserGroupId>
      <DocumentMigration:VisibleForId xsi:type="xsd:int">0</DocumentMigration:VisibleForId>
     </DocumentMigration:DocumentMigrationItem>
    </DocumentMigration:Documents>
    <DocumentMigration:Associates xsi:type="DocumentMigration:ArrayOfDocumentMigrationAssociate">
     <DocumentMigration:DocumentMigrationAssociate xsi:type="DocumentMigration:DocumentMigrationAssociate">
      <DocumentMigration:AssociateId xsi:type="xsd:int">0</DocumentMigration:AssociateId>
      <DocumentMigration:EmailAddress xsi:type="xsd:string"></DocumentMigration:EmailAddress>
     </DocumentMigration:DocumentMigrationAssociate>
    </DocumentMigration:Associates>
   </DocumentMigration:Response>
  </DocumentMigration:CreateDefaultDocumentMigrationItemListResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```