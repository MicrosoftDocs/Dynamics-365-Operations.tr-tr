## <a name="customer-groups-to-msdyn_customergroups"></a>Müşteri grupları ve msdyn_customergroups

Bu şablon, Finance and Operations uygulamaları ve Common Data Service arasında verileri eşitler.

Finance and Operations alanı | Eşleme türü | Diğer Dynamics 365 alanı | Varsayılan değer
---|---|---|---
CUSTOMERGROUPID | = | msdyn_groupid | 
DESCRIPTION | = | msdyn_description | 
ISSALESTAXINCLUDEDINPRICE | >< | msdyn_issalestaxincludedinprice | 
PAYMENTTERMID | = | msdyn_paymenttermid.msdyn_name | 
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn_clearingperiodpaymenttermname.msdyn_name | 
