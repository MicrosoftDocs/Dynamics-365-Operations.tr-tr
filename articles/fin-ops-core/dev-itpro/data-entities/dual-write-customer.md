---
title: Tümleşik müşteri aslı
description: Bu konu Finance and Operations ile Common Data Service arasında müşteri verisi tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6c8c94eb8ff04d489eb24b7e0f4642aef20a3b18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182060"
---
## <a name="integrated-customer-master"></a>Tümleşik müşteri aslı

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Müşteri kayıtlarının birden fazla uygulamada hakim olmasına yönelik tipik bir uygulamadır. Örneğin, satış etkinliği Sales uygulaması üzerinden ticari müşteri kayıtlarını getirebilir ve e-Ticaret veya perakende satışlar Finance and Operations uygulaması aracılığıyla müşteri kayıtlarını getirebilir. Müşteri kaydının kaynağından bağımsız olarak, uygulama sınırları ve altyapı farklılıklarının sahne arkasına entegre edilmiştir. Tümleşik müşteri hakimiyeti çoklu hakimiyet senaryolarını işlemeye yardımcı olur ve Dynamics 365 uygulama paketine kapsamlı bir müşteri görünümü sağlar.

## <a name="customer-data-flow"></a>Müşteri veri akışı

*Müşteri*, uygulamalarda iyi tanımlanmış bir kavramdır. Bu nedenle, müşteri verileri tümleştirmesi yalnızca iki uygulama arasındaki müşteri kavramını uyumlu hale getirmeyi içerir. Aşağıdaki örnekte, müşteri verisi akışı gösterilmektedir.

![Müşteri veri akışı](media/dual-write-customer-data-flow.png)

Müşteriler, geniş anlamda iki türde sınıflandırılabilir: ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar. Bu iki tür müşteri Finance and Operations ve Common Data Service uygulamasında 'da farklı şekilde saklanır ve işlenir.

Finance and Operations'ta, ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar **CustTable** (CustomerCustomerV3Entity) adlı tek bir tabloda yönetilir ve **Tür** özniteliğine göre sınıflandırılır. ( **Tür** **Kuruluş** olarak ayarlanırsa, müşteri ticari/kuruluş müşterisidir; **Tür** **Kişi** olarak ayarlanırsa, müşteri bir tüketici/son kullanıcıdır.) Birincil ilgili kişi bilgileri SMMContactPersonEntity varlığı aracılığıyla işlenir.

Common Data Service'ta, ticari/kuruluş müşterileri Hesap varlığında yönetilir ve **RelationshipType** özniteliği **Müşteri** olarak ayarlandığında, müşteri olarak tanımlanır. Hem tüketiciler/son kullanıcılar hem de ilgili kişi, İlgili Kişi varlığı ile temsil edilir. Bir tüketici/son Kullanıcı ve bir ilgili kişi arasında net bir ayrım sağlamak için **İlgili Kişi** varlığında **satış yapılabilir** adlı bir Boole bayrağı bulunur. **Satış yapılabilir** için değer **Doğru** olduğunda, ilgili kişi bir tüketici/son kullanıcıdır ve bu ilgili kişi için teklifler ve siparişler oluşturulabilir. **Satış yapılabilir** için değer **Yanlış** olduğunda, ilgili kişi yalnızca bir müşterinin birincil ilgili kişisidir.

Satış yapılabilir olmayan bir ilgili kişi bir teklif veya sipariş sürecine katıldığında,  **Satış yapılabilir** alanı ilgili kişiyi satış yapılabilir kişi olarak işaretlemek üzere **Doğru** değerine ayarlanır. Satış yapılabilir ilgili kişi haline gelen bir ilgili kişi satış yapılabilir ilgili kişi olarak kalır.

## <a name="templates"></a>Şablonlar

Müşteri verileri, müşteriyle ilgili müşteri grubu, adresler, iletişim bilgileri, ödeme profili, fatura profili ve bağlılık durumu gibi tüm bilgileri içerir. Varlık eşlemeleri topluluğu, aşağıdaki tabloda gösterildiği gibi, müşteri veri etkileşimi sırasında birlikte çalışır.

Finance and Operations uygulamaları    | Diğer Dynamics 365 uygulamaları
--------------------------|---------------------------------
Müşteri V3               | Hesap
Müşteri V3               | Başvur
CDS İlgili Kişileri V2           | Başvur
Müşteri grupları           | Msdyn\_customergroups
Müşteri Ödeme Yöntemi   | Msdyn\_customerpaymentmethods
Bağlılık Programı Kartı              | Msdyn\_loyaltycards
Ödeme Planı          | Msdyn\_paymentschedules
Ödeme Planı          | Msdyn\_paymentschedulelines
Ödeme günü CDS           | Msdyn\_paymentdays
Ödeme günü satırları CDS     | Msdyn\_paymentdaylines
Ödeme Şartları          | Msdyn\_paymentterms
Ad Ekleri              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Müşteri V3'ten Hesaba

Bu şablon, Finance and Operations uygulamaları ile Common Data Service arasında ticari ve kurumsal müşterilere ilişkin müşteri ana bilgilerini eşitler.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | ad
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | faks
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | açıklama
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | yok
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
yok | \>\> | address1\_addresstypecode
yok | \>\> | customertypecode
PARTYTYPE | \<\< | yok
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Customer V3'ten İlgili Kişiye

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında tüketici ve son kullanıcılara ilişkin müşteri ana verilerini eşitler.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
yok | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | yok
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | yok
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | yok
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
yok | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
yok | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
yok | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | faks
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | açıklama

## <a name="contacts"></a>İlgili kişiler

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.

<!-- ![](media/dual-write-contacts.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | yok
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | faks
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | departman
NOTLAR | = | açıklama
CİNSİYET | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
yok | \>\> | msdyn\_contactforvendor
yok | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Müşteri Grupları

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşteri grubu bilgilerini eşitler.

<!-- ![](media/dual-write-customer-groups.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
AÇIKLAMA | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Müşteri Ödeme Yöntemleri

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşteri ödeme yöntemi bilgilerini eşitler.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AD | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
AÇIKLAMA | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Bağlılık Programı Kartları

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşteri bağlılık programı kartı bilgilerini eşitler.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Ödeme Planları

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin ödeme planı referans verilerini eşitler.

<!-- ![](media/dual-write-payment-schedules.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AD | = | msdyn\_name
AÇIKLAMA | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTLAR | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Ödeme Planı Satırları

Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin ödeme planı satırları referans verilerini eşitler.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Ödeme günleri

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin ödeme günleri referans verilerini eşitler.

<!-- ![](media/dual-write-payment-days.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AD | = | msdyn\_name
AÇIKLAMA | = | msdyn\_description

## <a name="payment-day-lines"></a>Ödeme Günü Satırları

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin ödeme günü satırları referans verilerini eşitler.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
AD | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Ödeme Koşulları

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin ödeme koşulları (ödeme koşulları) referans verilerini eşitler.

<!-- ![](media/dual-write-payment-terms.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AÇIKLAMA | = | msdyn\_description
AD | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Ad Ekleri

Bu şablon, Finance and Operations ile diğer Dynamics 365 uygulamaları arasında müşterilere ve satıcılara ilişkin ad ekleri referans verilerini eşitler.

<!-- ![](media/dual-write-name-affixes.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AFFIX | = | msdyn\_affix
TÜR | \>\< | msdyn\_affixtype
AÇIKLAMA | = | msdyn\_description
