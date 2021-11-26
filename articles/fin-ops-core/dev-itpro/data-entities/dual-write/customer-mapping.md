---
title: Tümleşik müşteri aslı
description: Bu konu, Finance and Operations ve Dataverse arasındaki müşteri verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48070628aafd7daac65327a484c87dc01ffb3954
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781702"
---
# <a name="integrated-customer-master"></a>Tümleşik müşteri aslı

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Müşteri verileri birden fazla Dynamics 365 uygulamasında ana kopyalı olabilir. Örneğin, bir müşteri Dynamics 365 Sales (müşteri etkileşimi uygulaması) satış aktivitesinde ortaya çıkabilir veya bir satır Dynamics 365 Commerce'teki (finans ve operasyon uygulaması) perakende aktivitesi aracılığıyla ortaya çıkabilir. Müşteri verilerinin kaynaklandığı yerden bağımsız olarak, arka planda tümleştirilir. Tümleşik Müşteri Yöneticisi, herhangi bir Dynamics 365 uygulamasındaki ana müşteri verilerine esneklik sağlar ve Dynamics 365 uygulama paketi arasında müşterinin kapsamlı bir görünümünü sağlar.

## <a name="customer-data-flow"></a>Müşteri veri akışı

*Müşteri*, uygulamalarda iyi tanımlanmış bir kavramdır. Bu nedenle, müşteri verileri tümleştirmesi yalnızca iki uygulama arasındaki müşteri kavramını uyumlu hale getirmeyi içerir. Aşağıdaki örnekte, müşteri verisi akışı gösterilmektedir.

![Müşteri veri akışı.](media/dual-write-customer-data-flow.png)

Müşteriler, geniş anlamda iki türde sınıflandırılabilir: ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar. Bu iki tür müşteri Finance and Operations ve Dataverse uygulamasında farklı şekilde saklanır ve işlenir.

Finance and Operations uygulamasında, ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar **CustTable** (CustomerCustomerV3Entity) adlı tek bir tabloda yönetilir ve **Tür** özniteliğine göre sınıflandırılır. ( **Tür** **Kuruluş** olarak ayarlanırsa, müşteri ticari/kurumsal müşteridir; **Tür** **Kişi** olarak ayarlanırsa, müşteri bir tüketici/son kullanıcıdır.) Birincil ilgili kişi bilgileri SMMContactPersonEntity tablosu aracılığıyla işlenir.

Dataverse'te, ticari/kurumsal müşteriler Hesap tablosunda yönetilir ve **RelationshipType** özniteliği **Müşteri** olarak ayarlandığında, müşteri olarak tanımlanır. Hem tüketiciler/son kullanıcılar hem de ilgili kişi, İlgili Kişi tablosuyla temsil edilir. Bir tüketici/son kullanıcı ve bir ilgili kişi arasında net bir ayrım sağlamak için **İlgili Kişi** tablosunda **Satış yapılabilir** adlı bir Boole bayrağı bulunur. **Satış yapılabilir** için değer **Doğru** olduğunda, ilgili kişi bir tüketici/son kullanıcıdır ve bu ilgili kişi için teklifler ve siparişler oluşturulabilir. **Satış yapılabilir** için değer **Yanlış** olduğunda, ilgili kişi yalnızca bir müşterinin birincil ilgili kişisidir.

Satış yapılabilir olmayan bir ilgili kişi bir teklif veya sipariş sürecine katıldığında,  **Satış yapılabilir** alanı ilgili kişiyi satış yapılabilir kişi olarak işaretlemek üzere **Doğru** değerine ayarlanır. Satış yapılabilir ilgili kişi haline gelen bir ilgili kişi satış yapılabilir ilgili kişi olarak kalır.

## <a name="templates"></a>Şablonlar

Müşteri verileri, müşteriyle ilgili müşteri grubu, adresler, iletişim bilgileri, ödeme profili, fatura profili ve bağlılık durumu gibi tüm bilgileri içerir. Tablo eşlemeleri koleksiyonu, aşağıdaki tabloda gösterildiği gibi, müşteri veri etkileşimi sırasında birlikte çalışır.

Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları         | Tanım
----------------------------|---------------------------------|------------
[CDS İlgili Kişileri V2](mapping-reference.md#115) | ilgili kişiler | Bu şablon, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.
[Müşteri grupları](mapping-reference.md#126) | msdyn_customergroups | Bu şablon müşteri grubu bilgilerini eşitler.
[Müşteri ödeme yöntemi](mapping-reference.md#127) | msdyn_customerpaymentmethods | Bu şablon, müşteri ödeme yöntemi bilgilerini eşitler.
[Müşteriler V3](mapping-reference.md#101) | hesaplar | Bu şablon, ticari ve kurumsal müşterilere ilişkin müşteri ana bilgilerini eşitler.
[Müşteriler V3](mapping-reference.md#116) | ilgili kişiler | Bu şablon tüketicilere ve son kullanıcılara ilişkin müşteri ana verilerini eşitler.
[Ad ekleri](mapping-reference.md#155) | msdyn_nameaffixes | Bu şablon, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.
[Ödeme günü satırları CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Bu şablon, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.
[Ödeme günleri CDS](mapping-reference.md#158) | msdyn_paymentdays | Bu şablon, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.
[Ödeme planı satırları](mapping-reference.md#159) | msdyn_paymentschedulelines | Müşterilerin ve satıcıların ödeme planı satırları referans verilerini eşitler.
[Ödeme planı](mapping-reference.md#160) | msdyn_paymentschedules | Bu şablon, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.
[Ödeme koşulları](mapping-reference.md#161) | msdyn_paymentterms | Bu şablon, müşterilerin ve satıcıların ödeme koşulları (ödeme koşulları) referans verilerini eşitler.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
