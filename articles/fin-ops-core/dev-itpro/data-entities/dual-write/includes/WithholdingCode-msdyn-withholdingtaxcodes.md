## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Stopaj vergisi kodları ve msdyn_withholdingtaxcodes

Bu şablon, Finance and Operations uygulamaları ve Common Data Service arasında verileri eşitler.

Finance and Operations alanı | Eşleme türü | Diğer Dynamics 365 alanı | Varsayılan değer
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
