---
title: Tümleşik satıcı aslı
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında satıcı verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0f3e4a2267dd80c0631f9d09e12907dd9a6b517b503b1c549d28c95b0789cab0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747553"
---
# <a name="integrated-vendor-master"></a>Tümleşik satıcı aslı

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

*Satıcı* terimi, bir tedarikçi organizasyonunu veya bir işletmeye mal veya servis sağlayan tek bir sahip anlamına gelir. *Satıcı*, Microsoft Dynamics 365 Supply Chain Management'ta yerleşik bir kavram olmasına rağmen, müşteri etkileşimi uygulamalarında satıcı kavramı yoktur. Ancak, satıcı bilgilerini depolamak üzere **Hesap/İlgili Kişi** tablosuna aşırı yükleme yapabilirsiniz. Tümleşik satıcı yöneticisi, müşteri etkileşimi uygulamalarında açık bir satıcı konsepti sunar. **Hesap/İlgili Kişi** tablosundaki yeni satıcı tasarımını kullanabilir veya satıcı verilerini depolayabilirsiniz. Çift yazım, her iki yaklaşımdan destekler.

Her iki yaklaşımdan satıcı verileri, Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service ve Power Apps portalları arasında tümleştirilir. Supply Chain Management'ta, veriler satınalma talepleri ve satınalma siparişleri gibi iş akışlarında kullanılabilir.

## <a name="vendor-data-flow"></a>Satıcı veri akışı

Dataverse'teki **Hesap/İlgili Kişi** tablosunda satıcı verilerini saklamak istemiyorsanız yeni satıcı tasarımını kullanabilirsiniz.

![Satıcı veri akışı.](media/dual-write-vendor-data-flow.png)

**Hesap/İlgili Kişi** tablosunda satıcı verilerini saklamaya devam etmek istiyorsanız genişletilmiş satıcı tasarımını kullanabilirsiniz. Genişletilmiş satıcı tasarımını kullanmak için çift yazan çözüm paketindeki satıcı iş akışlarını konfigüre etmelisiniz. Daha fazla bilgi için, bkz. [Satıcı tasarımları arasında geçiş yap](vendor-switch.md).

![Genişletilmiş satıcı veri akışı.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Self Servis satıcıları için Power Apps portalları kullanıyorsanız, satıcı bilgileri doğrudan Finance and Operations uygulamalara akabilir.

## <a name="templates"></a>Şablonlar

Satıcı verileri, satıcıyla ilgili satıcı grubu, adresler, iletişim bilgileri, ödeme profili ve fatura profili gibi tüm bilgileri içerir. Tablo eşlemeleri koleksiyonu, aşağıdaki tabloda gösterildiği gibi satıcı veri etkileşimi sırasında birlikte çalışır.

Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları     | Tanım
----------------------------|-----------------------------|------------
[CDS İlgili Kişileri V2](mapping-reference.md#115) | ilgili kişiler | Bu şablon, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.
[Ad ekleri](mapping-reference.md#155) | msdyn_nameaffixes | Bu şablon, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.
[Ödeme günü satırları CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Bu şablon, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.
[Ödeme günleri CDS](mapping-reference.md#158) | msdyn_paymentdays | Bu şablon, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.
[Ödeme planı satırları](mapping-reference.md#159) | msdyn_paymentschedulelines | Müşterilerin ve satıcıların ödeme planı satırları referans verilerini eşitler.
[Ödeme planı](mapping-reference.md#160) | msdyn_paymentschedules | Bu şablon, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.
[Ödeme koşulları](mapping-reference.md#161) | msdyn_paymentterms | Bu şablon, müşterilerin ve satıcıların ödeme koşulları (ödeme koşulları) referans verilerini eşitler.
[Satıcılar V2](mapping-reference.md#202) | msdyn_vendors | Satıcılar için özel bir çözüm kullanan işletmeler, Finance and Operations uygulamaları tümleştirmesi nedeniyle Dataverse'da sunulmakta olan kullanıma hazır satıcı kavramından yararlanabilir.
[Satıcı grupları](mapping-reference.md#200) | msdyn_vendorgroups | Bu şablon satıcı grubu bilgilerini eşitler.
[Satıcı ödeme yöntemi](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Bu şablon, satıcı ödeme yöntemi bilgilerini eşitler.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
