---
title: Services84.SaleAgent.GetSummaryByAssociate SOAP
generated: 1
uid: Services84-Sale-GetSummaryByAssociate
---

# Services84 Sale GetSummaryByAssociate

SOAP request and response examples **Remote/Services84/Sale.svc**
Implemented by the <see cref="M:SuperOffice.Services84.ISaleAgent.GetSummaryByAssociate">SuperOffice.Services84.ISaleAgent.GetSummaryByAssociate</see> method.

## GetSummaryByAssociate



* **associateId:** 
* **fromDate:** 
* **toDate:** 



[WSDL file for Services84/Sale](../Services84-Sale.md)

Obtain a ticket from the [Services84/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetSummaryByAssociate Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices842="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices841="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Sale="http://www.superoffice.net/ws/crm/NetServer/Services84">
  <Sale:ApplicationToken>1234567-1234-9876</Sale:ApplicationToken>
  <Sale:Credentials>
    <Sale:Ticket>7T:1234abcxyzExample==</Sale:Ticket>
  </Sale:Credentials>
 <SOAP-ENV:Body>
   <Sale:GetSummaryByAssociate>
    <Sale:AssociateId xsi:type="xsd:int">0</Sale:AssociateId>
    <Sale:FromDate xsi:type="xsd:dateTime">2021-11-30T13:22:21Z</Sale:FromDate>
    <Sale:ToDate xsi:type="xsd:dateTime">2021-11-30T13:22:21Z</Sale:ToDate>
   </Sale:GetSummaryByAssociate>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetSummaryByAssociate Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices842="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices841="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Sale="http://www.superoffice.net/ws/crm/NetServer/Services84">
 <SOAP-ENV:Body>
  <Sale:GetSummaryByAssociateResponse>
   <Sale:Response xsi:type="Sale:SaleSummary">
    <Sale:BaseCurrency xsi:type="xsd:string"></Sale:BaseCurrency>
    <Sale:OwnCurrency xsi:type="xsd:string"></Sale:OwnCurrency>
    <Sale:SoldTotalBaseCurrency xsi:type="xsd:double">0.0</Sale:SoldTotalBaseCurrency>
    <Sale:Sold xsi:type="xsd:int">0</Sale:Sold>
    <Sale:SoldTotalOwnCurrency xsi:type="xsd:double">0.0</Sale:SoldTotalOwnCurrency>
    <Sale:Lost xsi:type="xsd:int">0</Sale:Lost>
    <Sale:LostTotalBaseCurrency xsi:type="xsd:double">0.0</Sale:LostTotalBaseCurrency>
    <Sale:LostTotalOwnCurrency xsi:type="xsd:double">0.0</Sale:LostTotalOwnCurrency>
    <Sale:Open xsi:type="xsd:int">0</Sale:Open>
    <Sale:OpenTotalBaseCurrency xsi:type="xsd:double">0.0</Sale:OpenTotalBaseCurrency>
    <Sale:OpenTotalOwnCurrency xsi:type="xsd:double">0.0</Sale:OpenTotalOwnCurrency>
    <Sale:OpenWeightedBaseCurrency xsi:type="xsd:double">0.0</Sale:OpenWeightedBaseCurrency>
    <Sale:OpenWeightedOwnCurrency xsi:type="xsd:double">0.0</Sale:OpenWeightedOwnCurrency>
    <Sale:PreviousOverdue xsi:type="xsd:int">0</Sale:PreviousOverdue>
    <Sale:PreviousOverdueTotalBaseCurrency xsi:type="xsd:double">0.0</Sale:PreviousOverdueTotalBaseCurrency>
    <Sale:PreviousOverdueTotalOwnCurrency xsi:type="xsd:double">0.0</Sale:PreviousOverdueTotalOwnCurrency>
    <Sale:PreviousOverdueWeightedBaseCurrency xsi:type="xsd:double">0.0</Sale:PreviousOverdueWeightedBaseCurrency>
    <Sale:PreviousOverdueWeightedOwnCurrency xsi:type="xsd:double">0.0</Sale:PreviousOverdueWeightedOwnCurrency>
    <Sale:CurrentOverdue xsi:type="xsd:int">0</Sale:CurrentOverdue>
    <Sale:CurrentOverdueTotalBaseCurrency xsi:type="xsd:double">0.0</Sale:CurrentOverdueTotalBaseCurrency>
    <Sale:CurrentOverdueTotalOwnCurrency xsi:type="xsd:double">0.0</Sale:CurrentOverdueTotalOwnCurrency>
    <Sale:CurrentOverdueWeightedBaseCurrency xsi:type="xsd:double">0.0</Sale:CurrentOverdueWeightedBaseCurrency>
    <Sale:CurrentOverdueWeightedOwnCurrency xsi:type="xsd:double">0.0</Sale:CurrentOverdueWeightedOwnCurrency>
    <Sale:FutureOpen xsi:type="xsd:int">0</Sale:FutureOpen>
    <Sale:FutureOpenTotalBaseCurrency xsi:type="xsd:double">0.0</Sale:FutureOpenTotalBaseCurrency>
    <Sale:FutureOpenTotalOwnCurrency xsi:type="xsd:double">0.0</Sale:FutureOpenTotalOwnCurrency>
    <Sale:FutureOpenWeightedBaseCurrency xsi:type="xsd:double">0.0</Sale:FutureOpenWeightedBaseCurrency>
    <Sale:FutureOpenWeightedOwnCurrency xsi:type="xsd:double">0.0</Sale:FutureOpenWeightedOwnCurrency>
   </Sale:Response>
  </Sale:GetSummaryByAssociateResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```
