---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 59c83409ede5e006ddf030d396934eeb6cd8df76
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010138"
---
# <a name="enable-product-recommendations"></a>Ürün önerilerini etkinleştirme

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="recommendations-pre-check"></a>Öneriler ön kontrolü

Etkinleştirmeden önce ürün önerilerinin, depolama alanını Azure Data Lake Storage kullanarak geçirmiş olan Commerce müşterileri için desteklendiğini unutmayın. 

Öneriler etkinleştirilmeden önce aşağıdaki yapılandırmalar arka ofiste etkinleştirilmelidir:

1. Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olun. Daha fazla bilgi için bkz. [Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olma](enable-ADLS-environment.md).
2. Varlık deposu yenilemenin otomatik olarak yapıldığından emin olun. Daha fazla bilgi için bkz. [Varlık deposu yenilemesinin otomatik yapıldığından emin olun](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Azure AD Kimlik yapılandırmasının Öneriler için bir giriş içerdiğini onaylayın. Bu eylemin nasıl yapılacağı ile ilgili daha fazla bilgi aşağıda verilmektedir.

Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun. Bu ayar işlemi hakkında daha fazla bilgi edinmek için bkz. [Ölçümlerle çalışma](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD Kimlik yapılandırması

Bu adım, Hizmet olarak alt yapı (IaaS) yapılandırması çalıştıran tüm müşteriler için gereklidir. Service Fabric (SF) üzerinde çalışan müşteriler için bu adım otomatik olmalıdır ve ayarın beklendiği şekilde yapılandırıldığını doğrulamanız önerilir.

### <a name="setup"></a>Ayar

1. Arka ofisten, **Azure Active Directory uygulamaları** sayfasını arayın.
2. "RecommendationSystemApplication-1" için bir giriş olup olmadığını doğrulayın.

Giriş yoksa, aşağıdaki bilgilerle yeni bir giriş ekleyin:

- **İstemcı Kodu** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Ad** - RecommendationSystemApplication-1
- **Kullanıcı Kimliği** - RetailServiceAccount

Sayfayı kaydet ve kapatın 

## <a name="turn-on-recommendations"></a>Önerileri açın

Ürün önerilerini açmak için aşağıdaki adımları izleyin.

1. Commerce Headquarters'ta **Özellik Yönetimi**'ni arayın.
1. Kullanılabilir özelliklerin listesini görmek için **Tümü**'nü seçin. 
1. Arama kutusuna **Öneriler** yazın.
1. **Ürün önerileri** özelliğini seçin.
1. **Ürün önerileri** özellikler bölmesinde **Şimdi etkinleştir**'i seçin.

![Önerileri açma](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır. Dynamics 365 Commerce'ta veya satış noktasında (POS) listelerin kullanılabilmesi ve görüntülenmesi için birkaç saat gerekli olabilir.

## <a name="configure-recommendation-list-parameters"></a>Öneri listesi parametrelerini konfigüre et

Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar. Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz. Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.

## <a name="show-recommendations-on-pos-devices"></a>POS cihazlarındaki önerileri göster

Commerce arka ofisinde önerileri etkinleştirdikten sonra, öneriler panelinin düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir. Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Kişiselleştirilmiş önerileri etkinleştirme

Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir. Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında dahil edilebilir. Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.

Kişiselleştirilmiş ürün önerileri hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]