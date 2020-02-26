## <a name="currencies-to-transactioncurrencies"></a>Para birimleri ve transactioncurrencies

Bu şablon, Finance and Operations uygulamaları ve Common Data Service arasında verileri eşitler.

Kaynak filtresi: ((CURRENCYCODE != "999"))

Finance and Operations alanı | Eşleme türü | Diğer Dynamics 365 alanı | Varsayılan değer
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
hiçbiri | >> | exchangerate | 1
