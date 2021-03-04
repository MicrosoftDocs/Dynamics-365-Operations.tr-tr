---
title: Kişiselleştirilmiş önerilerden vazgeçme
description: Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'ta kişiselleştirilmiş öneriler almamasına nasıl izin verileceğini açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6a64b45e1326673dd84c3c705491c9c100cdd069
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416398"
---
# <a name="opt-out-of-personalized-recommendations"></a>Kişiselleştirilmiş önerilerden vazgeçme

[!include [banner](includes/banner.md)]

Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'ta kişiselleştirilmiş öneriler almamasına nasıl izin verileceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Hesap oluşturma sırasında, yeni müşteriler otomatik olarak kişiselleştirilmiş öneriler almak için ayarlanır. Ancak, Dynamics 365 Commerce perakendeciler için kullanıcıların bu önerileri almalarını ve kişisel verilerinin işlenmesini kısıtlamalarını sağlamak amacıyla çeşitli yollar sunar. Kişiselleştirilmiş Önerileri almaya çalışan kimliği doğrulanmış kullanıcılar, kişiselleştirilmiş listeleri hemen görmeyi durdurur. Ek olarak, kişiselleştirme için toplanan tüm kişisel veriler kişiselleştirilmiş öneri modellerinden kaldırılacaktır.

Kişiselleştirilmiş ürün önerileri hakkında bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştir](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Bir tercih çıkış deneyimi uygulamak için perakendecilere yolları

Bir tercih çıkış deneyimi uygulamak için perakendecilerin üç yolu vardır.

### <a name="opting-out-on-behalf-of-users"></a>Kullanıcılar adına vazgeçme

Commerce arka ofiste hesap yönetiminde, perakendeciler Kullanıcı adına geri alabilir.

1. Arka ofis ana sayfasında, **tüm müşterileri** arayın.
1. Müşteri arayıp seçin ve sonra **perakende** hızlı sekmesini seçin.

    ![Perakende hızlı sekmesi](./media/Disablepersonalizationpart1.png)

1. **Gizlilik**'in altında, **kişiselleştirmeyi devre dışı bırak** seçeneğini **Evet** olarak ayarlayın.

    ![Gizlilik ayarları](./media/Disablepersonalizationpart2.png)

1. **Kaydet**'i seçip sayfayı kapatın.

### <a name="module-based-opt-out-experience"></a>Modül tabanlı geri çevirme deneyimi

Perakendeciler, kimlik doğrulaması yapılmış kullanıcıların kendi kendilerine ait kişiselleştirilmiş öneriler dışında çalışmasına izin verebilir. Bu çıkış deneyimini sağlamak için, müşteri hesap profili sayfalarına Kullanıcı geri çevirme modülünü ekleyin.

### <a name="custom-extensions"></a>Özel uzatmalar

Perakendeciler, kullanıcılar için geri çevirme deneyimini yönetmek amacıyla kendi uzantılarını oluşturabilir. Daha fazla bilgi için, bkz. [Perakende Sunucu API'lerini çağır](e-commerce-extensibility/call-retail-server-apis.md) ve [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Kimliği doğrulanmış bir kullanıcı adına kişiselleştirilmiş öneri verilerinin dijital kopyasını al

Müşteriler, kişisel verilerinin dijital bir kopyasını elde etmek ve ayrıca öneriler sonuçlarının dışa aktarılan görünümünü görmek isteyebilir. Bir müşteri bu bilgileri isterse, satıcının, müşteri müşteri kimliğine göre, **Sizin için seçilen** liste için tam sonuçlar için Perakende Sunucu Uygulaması Programlama Arayüzü (API) ve sorguları çağıran özelleştirilmiş bir uzantı oluşturması gerekir. Sonuçlar daha sonra, virgülle ayrılmış değerler (CSV) biçiminde dışa aktarılabilir ve müşteriyle paylaşılabilir.

Aşağıdaki örnek, bir perakendecin bu görevi nasıl yerine getirebileceği gösterir.

1. Perakende, Kullanıcı adına kişisel öneri verileri çekmek için özel bir uzantı oluşturur. Modül oluşturma, varolan modülleri kopyalama, Retail Server API'leri arama ve veri eylemleri arama hakkında bilgi için, bkz [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).
2. Özel uzantı **Tavsiyeler al** çekirdek verileri eylemine bir çağrı yapar ve listenin gereksinimlerine göre gerekli bilgileri geçirir. **Sizin için seçilen** liste için yapılan çekmeler durumunda, uzantı doğru liste adını ve müşteri kodunu veri eylemine iletmelidir.

    Özel uzantıyı oluşturmanın bir yolu, öneri sonuçlarını döndürmek için kullanılan varolan ürün koleksiyonu modülünü klonlamaktır. Bu varolan modülü klonlayarak, bir satıcı varolan kodu değiştirebilir ve öneri sonuçlarını bir CSV dosyasına dışa aktarır yeni bir düğme ekleyebilir. Daha fazla bilgi için, bkz. [Modül kitaplığı modülünü kopyalama](e-commerce-extensibility/clone-starter-module.md) ve [Ürün koleksiyon modülü](product-collection-module-overview.md).

    Retail Server API kitaplığının tam görünümü için, [Retail Server müşteri ve tüketici API'leri](dev-itpro/retail-server-customer-consumer-api.md) konularına bakın.

3. Özel uzantı oluşturulduktan sonra, satıcı, kimliği doğrulanan kullanıcının benzersiz müşteri koduna göre tüm öneri sonuçlarının CSV dosyasını dışa aktarabilir.
4. Satıcı, kimliği doğrulanmış kullanıcıyla önerilen ürünlerin tam kişiselleştirilmiş listesini içeren dışa aktarılan CSV dosyasını paylaşabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]