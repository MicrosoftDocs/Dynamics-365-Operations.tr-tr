---
title: Ürün önerilerini etkinleştir
description: Bu makale, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460034"
---
# <a name="enable-product-recommendations"></a>Ürün önerilerini etkinleştir

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="recommendations-pre-check"></a>Öneriler ön kontrolü

1. Geçerli bir Dynamics 365 Commerce Öneriler lisansına sahip olduğunuzdan emin olun.
1. Varlık deposunun müşteriye ait bir Azure Data Lake Storage Gen2 hesabına bağlı olduğundan emin olun. Daha fazla bilgi için bkz. [Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olma](enable-ADLS-environment.md).
1. Azure AD Kimlik yapılandırmasının Öneriler için bir giriş içerdiğini onaylayın. Bu eylemin nasıl yapılacağı ile ilgili daha fazla bilgi aşağıda verilmektedir.
1. Varlık deposunun Azure Data Lake Storage Gen2 için günlük yenilemesinin planlandığından emin olun. Daha fazla bilgi için bkz. [Varlık deposu yenilemesinin otomatik yapıldığından emin olun](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Varlık mağazası için RetailSale ölçümlerini etkinleştirin. Bu işlemin ayarlanması hakkında daha fazla bilgi için bkz. [Ölçümlerle çalışma](/dynamics365/ai/customer-insights/pm-measures).
1. Ortamınızın şu anda desteklenen bölgelerdeki servis ve pişirme bölgelerini aşağıdaki gibi yapılandırdığından emin olun:

    - **Desteklenen pişirme bölgeleri:** AB/ABD/CA/AU.
    - **Desteklenen hizmet bölgeleri:** ABD/CA/AU. Sunulan bölge mevcut desteklenen bölgelerden biriyle eşleşmiyorsa öneriler hizmeti desteklenen en yakın hizmet bölgesini seçer.

Yukarıdaki adımlar tamamlandıktan sonra, önerileri etkinleştirmeye hazır olursunuz.

> [!NOTE]
> Aşağıdaki adımlar tamamlandıktan sonra önerilerin görünmemesine yol açan bilinen bir sorun vardır. Bu sorun, ortamdaki veri akışı sorunları nedeniyle oluşur. Ortamınız öneri sonuçlarını göstermiyorsa [Öneriler için alternatif veri akışı ayarlama](set-up-alternate-data-flow.md) bölümündeki adımları izleyerek öneriler hizmeti için alternatif verileri yapılandırın. Bu adımları tamamlamak için Azure yöneticisi izinlerine sahip olmanız gerekir. Yardıma ihtiyacınız varsa FastTrack temsilcinizle iletişime geçin.

## <a name="azure-ad-identity-configuration"></a>Azure AD Kimlik yapılandırması

Bu adım yalnızca hizmet olarak altyapı (IaaS) yapılandırması çalıştıran müşteriler için gereklidir. Azure AD kimlik yapılandırması, Azure Service Fabric üzerinde çalışan müşteriler için otomatiktir ancak ayarın beklendiği gibi yapılandırıldığını doğrulamanız önerilir.

### <a name="setup"></a>Kurulum

1. Commerce genel merkezinde, **Azure Active Directory uygulamaları** sayfasını arayın.
1. **RecommendationSystemApplication-1** için bir giriş olup olmadığını kontrol edin. Bir giriş yoksa aşağıdaki bilgileri kullanarak bir tane oluşturun:

    - **İstemci Kimliği**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Ad**: RecommendationSystemApplication-1
    - **Kullanıcı Kimliği**: RetailServiceAccount

1. Sayfayı kaydet ve kapatın 

## <a name="turn-on-recommendations"></a>Önerileri açın

Ürün önerilerini açmak için aşağıdaki adımları izleyin.

1. Commerce Headquarters'ta **Özellik Yönetimi**'ni arayın.
1. Kullanılabilir özelliklerin listesini görmek için **Tümü**'nü seçin. 
1. Arama kutusuna **Öneriler** yazın.
1. **Ürün önerileri** özelliğini seçin.
1. **Ürün önerileri** özellikler bölmesinde **Şimdi etkinleştir**'i seçin.

![Önerileri açma.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Yukarıdaki yordam, ürün önerisi listeleri oluşturma işlemini başlatır. Dynamics 365 Commerce'ta veya satış noktasında (POS) listelerin kullanılabilmesi ve görüntülenmesi için birkaç saat gerekli olabilir.
> - Bu yapılandırma, tüm öneriler özelliklerini etkinleştirmez. Kişiselleştirilmiş öneriler, "benzer görünümdeki mağaza"" ve "benzer ürün açıklaması" gibi gelişmiş özellikler, özel özellik yönetimi girişleri tarafından kontrol edilir. Commerce genel merkezinde bu özellikleri etkinleştirme hakkında bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md), ["Benzer görünüme sahip ürünler" önerilerini etkinleştirme](shop-similar-looks.md) ve ["Benzer açıklamaya sahip ürünler" önerilerini etkinleştirme](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Öneri listesi parametrelerini konfigüre et

Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar. Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz. Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.

## <a name="include-recommendations-in-e-commerce-experiences"></a>E-ticaret deneyimlerine önerileri dahil etme

Commerce genel merkezinde öneriler etkinleştirildikten sonra, e-ticaret deneyimleri için öneri sonuçlarını görüntülemekte kullanılan Commerce modülleri yapılandırılmaya hazırdır. Daha fazla bilgi için bkz. [Ürün topluluğu modülleri](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>POS cihazlarındaki önerileri göster

Commerce genel merkezinde önerileri etkinleştirdikten sonra, öneriler panelinin, düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir. Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Kişiselleştirilmiş önerileri etkinleştirme

Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir. Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında dahil edilebilir. Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.

Kişiselleştirilmiş ürün önerileri hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Öneriler için alternatif veri akışı ayarlama](set-up-alternate-data-flow.md)

[Kişiselleştirilmiş önerileri etkinleştir](personalized-recommendations.md)

["Benzer görünümdeki mağaza" önerilerini etkinleştirme](shop-similar-looks.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
