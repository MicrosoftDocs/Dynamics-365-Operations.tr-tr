---
title: Tümleşik müşteri aslı
description: Bu konu, Finance and Operations ve Common Data Service arasındaki müşteri verileri tümleştirmesini açıklar.
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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020063"
---
# <a name="integrated-customer-master"></a>Tümleşik müşteri aslı

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Müşteri kayıtlarının birden fazla uygulamada hakim olmasına yönelik tipik bir uygulamadır. Örneğin, satış etkinliği bir Satış uygulaması üzerinden ticari müşteri kayıtlarını getirebilir ve e-Ticaret veya perakende satışlar Finance and Operations uygulaması aracılığıyla müşteri kayıtlarını getirebilir. Müşteri kaydının kaynağından bağımsız olarak, uygulama sınırları ve altyapı farklılıklarının sahne arkasına entegre edilmiştir. Tümleşik müşteri hakimiyeti çoklu hakimiyet senaryolarını işlemeye yardımcı olur ve Dynamics 365 uygulama paketine kapsamlı bir müşteri görünümü sağlar.

## <a name="customer-data-flow"></a>Müşteri veri akışı

*Müşteri*, uygulamalarda iyi tanımlanmış bir kavramdır. Bu nedenle, müşteri verileri tümleştirmesi yalnızca iki uygulama arasındaki müşteri kavramını uyumlu hale getirmeyi içerir. Aşağıdaki örnekte, müşteri verisi akışı gösterilmektedir.

![Müşteri veri akışı](media/dual-write-customer-data-flow.png)

Müşteriler, geniş anlamda iki türde sınıflandırılabilir: ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar. Bu iki tür müşteri Finance and Operations ve Common Data Service uygulamasında farklı şekilde saklanır ve işlenir.

Finance and Operations'ta, ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar **CustTable** (CustomerCustomerV3Entity) adlı tek bir tabloda yönetilir ve **Tür** özniteliğine göre sınıflandırılır. ( **Tür** **Kuruluş** olarak ayarlanırsa, müşteri ticari/kuruluş müşterisidir; **Tür** **Kişi** olarak ayarlanırsa, müşteri bir tüketici/son kullanıcıdır.) Birincil ilgili kişi bilgileri SMMContactPersonEntity varlığı aracılığıyla işlenir.

Common Data Service'ta, ticari/kuruluş müşterileri Hesap varlığında yönetilir ve **RelationshipType** özniteliği **Müşteri** olarak ayarlandığında, müşteri olarak tanımlanır. Hem tüketiciler/son kullanıcılar hem de ilgili kişi, İlgili Kişi varlığı ile temsil edilir. Bir tüketici/son Kullanıcı ve bir ilgili kişi arasında net bir ayrım sağlamak için **İlgili Kişi** varlığında **satış yapılabilir** adlı bir Boole bayrağı bulunur. **Satış yapılabilir** için değer **Doğru** olduğunda, ilgili kişi bir tüketici/son kullanıcıdır ve bu ilgili kişi için teklifler ve siparişler oluşturulabilir. **Satış yapılabilir** için değer **Yanlış** olduğunda, ilgili kişi yalnızca bir müşterinin birincil ilgili kişisidir.

Satış yapılabilir olmayan bir ilgili kişi bir teklif veya sipariş sürecine katıldığında,  **Satış yapılabilir** alanı ilgili kişiyi satış yapılabilir kişi olarak işaretlemek üzere **Doğru** değerine ayarlanır. Satış yapılabilir ilgili kişi haline gelen bir ilgili kişi satış yapılabilir ilgili kişi olarak kalır.

## <a name="templates"></a>Şablonlar

Müşteri verileri, müşteriyle ilgili müşteri grubu, adresler, iletişim bilgileri, ödeme profili, fatura profili ve bağlılık durumu gibi tüm bilgileri içerir. Varlık eşlemeleri topluluğu, aşağıdaki tabloda gösterildiği gibi, müşteri veri etkileşimi sırasında birlikte çalışır.

Finance and Operations uygulamaları | Diğer Dynamics 365 uygulamaları         | Tanım
----------------------------|---------------------------------|------------
CDS İlgili Kişileri V2             | ilgili kişiler                        | Bu şablon, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.
Müşteri grupları             | msdyn_customergroups            | Bu şablon müşteri grubu bilgilerini eşitler.
Müşteri ödeme yöntemi     | msdyn_customerpaymentmethods    | Bu şablon, müşteri ödeme yöntemi bilgilerini eşitler.
Müşteriler V3                | hesaplar                        | Bu şablon, ticari ve kurumsal müşterilere ilişkin müşteri ana bilgilerini eşitler.
Müşteriler V3                | ilgili kişiler                        | Bu şablon tüketicilere ve son kullanıcılara ilişkin müşteri ana verilerini eşitler.
Bağlılık programı kartı                | msdyn_loyaltycards              | Bu şablon müşteri bağlılık programı kartı bilgilerini eşitler.
Ad ekleri                | msdyn_nameaffixes               | Bu şablon, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.
Ödeme günü satırları CDS V2    | msdyn_paymentdaylines           | Bu şablon, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.
Ödeme günleri CDS            | msdyn_paymentdays               | Bu şablon, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.
Ödeme planı satırları      | msdyn_paymentschedulelines      | Müşterilerin ve satıcıların ödeme planı satırları referans verilerini eşitler.
Ödeme planı            | msdyn_paymentschedules          | Bu şablon, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.
Ödeme koşulları            | msdyn_paymentterms              | Bu şablon, müşterilerin ve satıcıların ödeme koşulları (ödeme koşulları) referans verilerini eşitler.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
