---
title: Tümleşik satıcı aslı
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında satıcı verisi tümleştirmesini açıklar.
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
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771010"
---
# <a name="integrated-vendor-master"></a>Tümleşik satıcı aslı

[!include [banner](../includes/banner.md)]

*Satıcı* terimi, tedarik zinciri sürecinin bir parçası olan ve işletme için mal sağlayan bir tedarikçi kuruluş veya tek bir sahip anlamına gelir. *Satıcı* Finance and Operations uygulamalarında yerleşik bir kavram olmasına karşın diğer Dynamics 365 uygulamalarında satıcı kavramı yoktur. Bunun yerine, bazı işletmeler hem müşteri bilgilerini hem de satıcı bilgilerini depolamak için Hesap varlığına aşırı yük yükler. Diğer işletmeler özel bir satıcı kavramı kullanır. Common Data Service tümleştirmesi bu her iki tasarımı da destekler. Bu nedenle, iş senaryosuna bağlı olarak tasarımlardan birini etkinleştirebilirsiniz.

Finance and Operations uygulamaları ile diğer Dynamics 365 uygulamaları arasında satıcı verilerinin tümleştirilmesi, verileri çoklu yönetmenize olanak tanır. Satıcı verisinin kaynağından bağımsız olarak, uygulama sınırları ve altyapı farklılıklarının sahne arkasına entegre edilmiştir. 

### <a name="vendor-data-flow"></a>Satıcı veri akışı

Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini müşteri bilgilerinden ayırmak istiyorsanız, yeni satıcı tasarımını kullanabilirsiniz.

![Satıcı veri akışı](media/dual-write-vendor-data-flow.png)

Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini depolamak için Hesap varlığını kullanmaya devam etmek istiyorsanız, yeni genişletilmiş satıcı tasarımını kullanabilirsiniz. Bu tasarımında, satıcı grubu ve satıcı deftere nakil profili gibi genişletilmiş satıcı bilgileri satıcı ayrıntılarına depolanır.

![Genişletilmiş satıcı veri akışı](media/dual-write-vendor-detail.jpg)

Satıcı iletişim bilgileri müşteri iletişim bilgilerine benzer. Sahne arkasında, ilgili kişinin bilgileri depolanır ve aynı varlıklardan alınır.

## <a name="templates"></a>Şablonlar

Satıcı verileri, satıcıyla ilgili satıcı grubu, adresler, iletişim bilgileri, ödeme profili ve fatura profili gibi tüm bilgileri içerir. Varlık eşlemeleri topluluğu, aşağıdaki tabloda gösterildiği gibi satıcı veri etkileşimi sırasında birlikte çalışır.

Finance and Operations uygulamaları | Diğer Dynamics 365 uygulamaları         | Tanım
----------------------------|---------------------------------|------------
Satıcı V2               | Hesap | Satıcı bilgilerini depolamak için Hesap varlığını kullanan işletmeler, aynı şekilde kullanmaya devam edebilir. Ayrıca, Finance and Operations uygulamaları tümleştirmesi nedeniyle gelen açık satıcı işlevlerinden de yararlanabilir.
Satıcı V2               | Msdyn\_vendors | Satıcılar için özel bir çözüm kullanan işletmeler, Finance and Operations uygulamaları tümleştirmesi nedeniyle Common Data Service'da sunulmakta olan kullanıma hazır satıcı kavramından yararlanabilir. 
Satıcı grupları | msdyn_vendorgroups | Bu şablon satıcı grubu bilgilerini eşitler.
Satıcı ödeme yöntemi | msdyn_vendorpaymentmethods | Bu şablon, satıcı ödeme yöntemi bilgilerini eşitler.
CDS İlgili Kişileri V2             | ilgili kişiler                        | [İlgili kişiler](dual-write-customer.md#cds-contacts-v2-to-contacts) şablonu, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.
Ödeme planı satırları      | msdyn_paymentschedulelines      | [Ödeme planı satırları](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) şablonu, müşterilerin ve satıcıların referans verilerini eşitler.
Ödeme planı            | msdyn_paymentschedules          | [Ödeme planları](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) şablonu, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.
Ödeme günü satırları CDS V2    | msdyn_paymentdaylines           | [Ödeme günü satırları](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) şablonu, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.
Ödeme günleri CDS            | msdyn_paymentdays               | [Ödeme günleri](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) şablonu, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.
Ödeme koşulları            | msdyn_paymentterms              | [Ödeme koşulları](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) şablonu, müşterilerin ve satıcıların ödeme koşulları referans verilerini eşitler.
Ad ekleri                | msdyn_nameaffixes               | [Ad ekleri](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) şablonu, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
