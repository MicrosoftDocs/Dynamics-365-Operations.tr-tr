---
title: Tümleşik satıcı aslı
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında satıcı verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 272962b58d8d654c2640a51ef2dbdcd1b05cf8c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560325"
---
# <a name="integrated-vendor-master"></a>Tümleşik satıcı aslı

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



*Satıcı* terimi, bir tedarikçi organizasyonunu veya bir işletmeye mal veya servis sağlayan tek bir sahip anlamına gelir. *Satıcı* Microsoft Dynamics 365 Supply Chain Management'da yerleşik bir kavram olmasına karşın Dynamics 365'teki model temelli uygulamalarda satıcı kavramı yoktur. Ancak, satıcı bilgilerini depolamak üzere **Hesap/İlgili Kişi** tablosuna aşırı yükleme yapabilirsiniz. Tümleşik satıcı Yöneticisi, Dynamics 365 ' te model temelli uygulamalarda açık bir satıcı kavramı tanıtır. **Hesap/İlgili Kişi** tablosundaki yeni satıcı tasarımını kullanabilir veya satıcı verilerini depolayabilirsiniz. Çift yazım, her iki yaklaşımdan destekler.

Her iki yaklaşımdan satıcı verileri, Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service ve Power Apps portalları arasında tümleştirilir. Supply Chain Management'ta, veriler satınalma talepleri ve satınalma siparişleri gibi iş akışlarında kullanılabilir.

## <a name="vendor-data-flow"></a>Satıcı veri akışı

Dataverse'teki **Hesap/İlgili Kişi** tablosunda satıcı verilerini saklamak istemiyorsanız yeni satıcı tasarımını kullanabilirsiniz.

![Satıcı veri akışı](media/dual-write-vendor-data-flow.png)

**Hesap/İlgili Kişi** tablosunda satıcı verilerini saklamaya devam etmek istiyorsanız genişletilmiş satıcı tasarımını kullanabilirsiniz. Genişletilmiş satıcı tasarımını kullanmak için çift yazan çözüm paketindeki satıcı iş akışlarını konfigüre etmelisiniz. Daha fazla bilgi için, bkz. [Satıcı tasarımları arasında geçiş yap](vendor-switch.md).

![Genişletilmiş satıcı veri akışı](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Self Servis satıcıları için Power Apps portalları kullanıyorsanız, satıcı bilgileri doğrudan Finance and Operations uygulamalara akabilir.

## <a name="templates"></a>Şablonlar

Satıcı verileri, satıcıyla ilgili satıcı grubu, adresler, iletişim bilgileri, ödeme profili ve fatura profili gibi tüm bilgileri içerir. Tablo eşlemeleri koleksiyonu, aşağıdaki tabloda gösterildiği gibi satıcı veri etkileşimi sırasında birlikte çalışır.

Finance and Operations uygulamaları | Diğer Dynamics 365 uygulamaları     | Tanım
----------------------------|-----------------------------|------------
Satıcı V2                   | Hesap                     | Satıcı bilgilerini depolamak için Hesap tablosunu kullanan işletmeler, aynı şekilde kullanmaya devam edebilir. Ayrıca, Finance and Operations uygulamaları tümleştirmesi nedeniyle gelen açık satıcı işlevlerinden de yararlanabilir.
Satıcı V2                   | Msdyn\_vendors              | Satıcılar için özel bir çözüm kullanan işletmeler, Finance and Operations uygulamaları tümleştirmesi nedeniyle Dataverse'da sunulmakta olan kullanıma hazır satıcı kavramından yararlanabilir. 
Satıcı grupları               | msdyn\_vendorgroups         | Bu şablon satıcı grubu bilgilerini eşitler.
Satıcı ödeme yöntemi       | msdyn\_vendorpaymentmethods | Bu şablon, satıcı ödeme yöntemi bilgilerini eşitler.
CDS İlgili Kişileri V2             | ilgili kişiler                    | [İlgili kişiler](customer-mapping.md#cds-contacts-v2-to-contacts) şablonu, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.
Ödeme planı satırları      | msdyn\_paymentschedulelines | [Ödeme planı satırları](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) şablonu, müşterilerin ve satıcıların referans verilerini eşitler.
Ödeme planı            | msdyn\_paymentschedules     | [Ödeme planları](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) şablonu, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.
Ödeme günü satırları CDS V2    | msdyn\_paymentdaylines      | [Ödeme günü satırları](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) şablonu, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.
Ödeme günleri CDS            | msdyn\_paymentdays          | [Ödeme günleri](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) şablonu, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.
Ödeme koşulları            | msdyn\_paymentterms         | [Ödeme koşulları](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) şablonu, müşterilerin ve satıcıların ödeme koşulları referans verilerini eşitler.
Ad ekleri                | msdyn\_nameaffixes          | [Ad ekleri](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) şablonu, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]