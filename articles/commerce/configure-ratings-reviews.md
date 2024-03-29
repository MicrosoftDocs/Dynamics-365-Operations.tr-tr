---
title: Derecelendirme ve incelemeleri yapılandırma
description: Bu makalede, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 27b1beddd474a2ca4db73f8e344b2d85934c43b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276878"
---
# <a name="configure-ratings-and-reviews"></a>Derecelendirme ve incelemeleri yapılandırma

[!include [banner](includes/banner.md)]

Bu makalede, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.

E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce, bu ürünler hakkındaki diğer müşterilerin ne düşündüğünü göstererek, ürünler hakkında bilgi edinmesine yardımcı olur. E-ticaret web sitelerinde, derecelendirmeler ve incelemeler, ürünler hakkında müşteri geribildirimi toplamaya yönelik bir mekanizmadır. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Derecelendirme ve incelemeleri gösterecek site yapılandırma

Kiracı kimliği, metin uzunluğunu gözden geçirme ve Başlık uzunluğunu gözden geçirme gibi derecelendirmeler ve incelemelerde ilgili konfigürasyon değerleri site düzeyinde yapılandırılır. 

Derecelendirmeleri ve değerlendirmeleri göstermek üzere bir site yapılandırmak için, aşağıdaki adımları izleyin. 

1. **Ev \> Siteler** e gidin.
1. Sitenizin adını belirtin. 
1. **Site ayarları \> uzantılarına** gidin. 
1. **En fazla metni gözden geçir** alanına, metni İnceleme için gereken maksimum karakter sayısını (örneğin, **1000**) girin. 
1. **En fazla başlık gözden geçir** alanına, başlık İnceleme için gereken maksimum karakter sayısını (örneğin, **55**) girin. 
1. **kaydet ve yayınla** yı seçin. 

Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.

![Derecelendirme ve incelemeleri gösterecek site yapılandırma.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama

Ürün derecelendirmesi, PDP'nin en üstünde ürün başlığının altında gösterilir. Ürün derecelendirmesi, aynı PDP'nin **incelemeler** bölümüyle bağlantılı olacak şekilde konfigüre edilebilir. 

Bir ürün derecelendirmesini PDP 'nin **incelemeler** bölümüne bağlamak için aşağıdaki adımları izleyin.

1. PDP şablonu açın. 
1. **Satın alma kutusu konteyner modülü ayarlarına** git.
1. **Satınalma kutusu** altında, **ürün derecelendirmeleri**'ni seçin ve sonra **bağlantıyı tam gözden geçirme modülü için tıklatın** onay kutusunu seçin.

Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.

![Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Gizlilik ve ilke sayfası için bağlantıyı yapılandırın

Gizlilik ve ilke sayfası için bağlantıyı yapılandırmak için şu adımları izleyin.

1. **Ev \> Siteler** e gidin.
1. Sitenizin adını belirtin. 
1. **Site ayarları \> uzantılarına** gidin.
1. **Rotalar** sekmesinde, **RNR Gizlilik ve ilke** altında **bağlantı ekle**'yi seçin. Zaten bir bağlantı girilmiş ve bunu değiştirmek istiyorsanız, bağlantıyı seçin. 
1. **Bağlantı ekle** iletişim kutusunda gizlilik ve ilke sayfası bağlantısını seçin ve **Tamam**'ı seçin. 
1. **kaydet ve yayınla** yı seçin. 

Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.

![Gizlilik ve ilke sayfası için bağlantıyı yapılandırın.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Ürün ayrıntıları sayfalarındaki derecelendirme ve İnceleme modüllerini konfigüre edin

Ürün Ayrıntıları sayfalarındaki derecelendirmeleri konfigüre etme ve modüllerin modüllerini İnceleme hakkında bilgi için bkz [Derecelendirme ve incelemeler](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)

[Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme](manual-publish-rating-reviews.md)

[Derecelendirmeleri ve değerlendirmeleri içe ve dışa aktarma](import-export-reviews.md)

[Hizmetten hizmete kimlik doğrulamasını yapılandırma](service-to-service-auth.md)

[Derecelendirmeler ve incelemelerle ilgili SSS](ratings-reviews-faq.md)

[Derecelendirme ve inceleme modülleri](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
