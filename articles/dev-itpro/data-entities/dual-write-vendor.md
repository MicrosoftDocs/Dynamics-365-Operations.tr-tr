---
title: Tümleşik satıcı aslı
description: Bu konu Finance and Operations ile Common Data Service arasında satıcı verisi tümleştirmesini açıklar.
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
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789255"
---
## <a name="integrated-vendor-master"></a>Tümleşik satıcı aslı

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

*Satıcı* terimi, tedarik zinciri sürecinin bir parçası olan ve işletme için mal sağlayan bir tedarikçi kuruluş veya tek bir sahip anlamına gelir. *Satıcı* Microsoft Dynamics 365 for Finance and Operations'da yerleşik bir kavram olmasına karşın Dynamics 365 for Customer Engagement'ta satıcı kavramı yoktur. Bunun yerine, bazı işletmeler hem müşteri bilgilerini hem de satıcı bilgilerini depolamak için Hesap varlığına aşırı yük yükler. Diğer işletmeler özel bir satıcı kavramı kullanır. Common Data Service tümleştirmesi bu her iki tasarımı da destekler. Bu nedenle, iş senaryosuna bağlı olarak tasarımlardan birini etkinleştirebilirsiniz.

Finance and Operations ile Customer Engagement arasında satıcı verileri tümleştirmesi verileri çoklu yönetmenize olanak tanır. Satıcı verisinin kaynağından bağımsız olarak, uygulama sınırları ve altyapı farklılıklarının sahne arkasına entegre edilmiştir. 

### <a name="vendor-data-flow"></a>Satıcı veri akışı

Satıcı yönetimi için Customer Engagement kullanmak ve satıcı bilgilerini müşteri bilgilerinden ayırmak istiyorsanız, yeni satıcı tasarımını kullanabilirsiniz.

![Satıcı veri akışı](media/dual-write-vendor-data-flow.png)

Satıcı yönetimi için Customer Engagement kullanmak ve satıcı bilgilerini depolamak için Hesap varlığını kullanmaya devam etmek istiyorsanız, yeni genişletilmiş satıcı tasarımını kullanabilirsiniz. Bu tasarımında, satıcı grubu ve satıcı deftere nakil profili gibi genişletilmiş satıcı bilgileri satıcı ayrıntılarına depolanır.

![Genişletilmiş satıcı veri akışı](media/dual-write-vendor-detail.jpg)

Satıcı iletişim bilgileri müşteri iletişim bilgilerine benzer. Sahne arkasında, ilgili kişinin bilgileri depolanır ve aynı varlıklardan alınır.

## <a name="templates"></a>Şablonlar

Satıcı verileri, satıcıyla ilgili satıcı grubu, adresler, iletişim bilgileri, ödeme profili ve fatura profili gibi tüm bilgileri içerir. Varlık eşlemeleri topluluğu, aşağıdaki tabloda gösterildiği gibi, satıcı veri etkileşimi sırasında birlikte çalışır.

Finance and Operations  | Customer Engagement uygulaması
------------------------|---------------------------------
Satıcı V2               | Hesap
Satıcı V2               | Msdyn\_vendors
CDS İlgili Kişileri V2         | Başvur
Satıcı grupları           | Msdyn\_vendorgroups
Satıcı Ödeme Yöntemi   | Msdyn\_vendorpaymentmethods
Ödeme Planı        | Msdyn\_paymentschedules
Ödeme Planı        | Msdyn\_paymentschedulelines
Ödeme günü CDS         | Msdyn\_paymentdays
Ödeme günü satırları CDS   | Msdyn\_paymentdaylines
Ödeme Şartları        | Msdyn\_paymentterms
Ad Ekleri            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Satıcı V2'den Hesaba 

Satıcı bilgilerini depolamak için Hesap varlığını kullanan işletmeler, aynı şekilde kullanmaya devam edebilir. Ayrıca, Finance and Operations tümleştirmesi nedeniyle gelen açık satıcı işlevlerinden de yararlanabilir.

## <a name="vendor-v2-and-msdyn_vendors"></a>Satıcı V2 ve Msdyn\_vendors

Satıcılar için özel bir çözüm kullanan işletmeler, Finance and Operations tümleştirmesi nedeniyle Common Data Service'da sunulmakta olan kullanıma hazır satıcı kavramından yararlanabilir. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>İlgili kişiler

Bu şablon, Finance and Operations ile Customer Engagement arasında müşterilere ve satıcılara ilişkin tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler. Varlık eşlemesinin ayrıntıları için bkz. [Tümleşik müşteri aslı](dual-write-customer.md#contacts)

## <a name="vendor-groups"></a>Satıcı Grupları

Bu şablon, Finance and Operations ile Customer Engagement arasında satıcı grubu bilgilerini eşitler.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
AÇIKLAMA | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Satıcı Ödeme Yöntemi

Bu şablon, Finance and Operations ile Customer Engagement arasında satıcı ödeme yöntemi bilgilerini eşitler.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
AD | = | msdyn\_name
AÇIKLAMA | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

