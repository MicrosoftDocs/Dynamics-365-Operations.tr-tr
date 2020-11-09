---
title: Sayfa içeriği erişilebilirliğini doğrulama
description: Bu konuda, Microsoft Dynamics 365 Commerce sayfa içeriğinin erişilebilirliğini nasıl doğrulanacaklarını açıklanmaktadır.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fc3dca673510e1636f497bb7d5c295bebe025677
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015115"
---
# <a name="verify-page-content-accessibility"></a>Sayfa içeriği erişilebilirliğini doğrulama


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce sayfa içeriğinin erişilebilirliğini nasıl doğrulanacaklarını açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Bir sayfayı değiştirmeyi bitirdiğinizde, içeriğin Web'deki herkes tarafından erişilebilir olduğundan emin olun. Commerce geliştirme araçlarında, tümleşik [Microsoft Erişilebilirlik Öngörüler](https://accessibilityinsights.io/) hizmetini kullanarak sayfa içeriğinin erişilebilirliğini kolayca doğrulayabilirsiniz. Bu hizmet, sayfanızın içeriğini en son [World Wide Web Consortium (W3C) erişilebilirlik](https://www.w3.org/standards/webdesign/accessibility) yönergelerine göre doğrular.

[Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini kullanabilmeniz için önce kiracı veya site düzeyinde açık olmalıdır.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Kiracınızda bulunan tüm sitelerden Microsoft Erişilebilirlik Insights'ı açın

Kiracınızda bulunan tüm Commerce siteleri için [Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini açmak üzere aşağıdaki adımları izleyin.

> [!NOTE]
> Kiracı ayarlarına erişmek için, Commerce'te sistem yöneticisi olarak oturum açmanız gerekir.

1. Commerce'te sistem yöneticisi olarak oturum açın.
1. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).
1. **Kiracı ayarları** altında **Özellikler** dosyasını seçin.
1. **Erişilebilirlik denetimi** seçeneğini **açık** olarak ayarlayın.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Tek bir site için Microsoft Accessibility Insights'ı aç

Kiracınızda bulunan tek bir Commerce sitesi için [Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini açmak üzere aşağıdaki adımları izleyin.

1. **Siteler** altında, **Fabrikam** 'ı seçin (veya sitenizin adını).
1. Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.
1. **Site ayarları** altında **Özellikler** dosyasını seçin.
1. **Erişilebilirlik denetimi** seçeneğini **açık** olarak ayarlayın.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Giriş sayfasındaki içeriğin erişilebilirliğini doğrulayın

Ticari olarak giriş sayfanızın içeriğini taramak ve doğrulamak amacıyla tümleşik [Microsoft Accessibility Insights](https://accessibilityinsights.io/) hizmetini kullanmak için aşağıdaki adımları izleyin.

1. **Siteler** altında, **Fabrikam** 'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **Sayfalar** seçin.
1. Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.
1. Komut çubuğunda, **Erişilebilirliği kontrol et** öğesini seçin. **Erişilebilirlik denetle** sayfası görüntülenir.
1. Tarama tamamlandıktan sonra, raporun içeriğini gözden geçirin.
1. Herhangi bir kontrol başarısız olursa, daha fazla ayrıntı görüntüleyebilmek için, bunları genişletmek amacıyla her başarısız denetim öğesini seçin.
1. İncelemeyi tamamladıktan sonra raporu kapatmak için **erişilebilirliği kontrol et** sayfasının en altına gidip **Tamam** 'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)
