---
title: Derecelendirme ve incelemeleri yapılandırma
description: Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002209"
---
# <a name="configure-ratings-and-reviews"></a>Derecelendirme ve incelemeleri yapılandırma


[!include [banner](includes/banner.md)]

Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.

## <a name="overview"></a>Genel Bakış

E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce, bu ürünler hakkındaki diğer müşterilerin ne düşündüğünü göstererek, ürünler hakkında bilgi edinmesine yardımcı olur. E-ticaret web sitelerinde, derecelendirmeler ve incelemeler, ürünler hakkında müşteri geribildirimi toplamaya yönelik bir mekanizmadır. 

Derecelendirmeler, ürün listesi sayfalarında, kategori listesi sayfalarında, arama sonuçları sayfalarında ve diğer site sayfalarında gösterilir. Derecelendirme çubuk grafikleri ve ürün değerlendirmeleri, ürün ayrıntıları sayfalarında (PDPs) gösterilir. **Gözden geçirme yazma** düğmesi müşterilerin bir ürün için derecelendirme ve İnceleme göndermelerini sağlar.

## <a name="ratings-and-reviews-modules-on-pdps"></a>PDP'lerde derecelendirmelere ve inceleme modülleri 

Üç modül, PDP'ler üzerinde derecelendirme ve İnceleme özetini gösterir:

- Gözden geçirme yazma modülü
- Ürün değerlendirmeleri liste modülü
- Derecelendirme çubuk grafik modülü
 
Aşağıdaki şekil, bir PDP'de derecelendirmelerin ve gözden geçirme modüllerinin nasıl göründüğünü gösterir.

![PDP'de derecelendirmelere ve inceleme modülleri](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> PDP şablonlarını ve düzenlerini en iyi duruma getirme hakkında bilgi için (böylece e-ticaret sitenizde birden çok PDC arasındaki derecelendirme ve değerlendirme modülleriyle ilgili yapılandırmaları paylaşabilirsiniz) [şablonlar ve mizanpajlara genel bakış](templates-layouts-overview.md) konularına bakın.

Aşağıdaki şekil, **Modül Ekle** iletişim kutusunun Dynamics 365 Commerce'te derecelendirmeyi ve İnceleme modüllerini nasıl sunduğunu gösterir.

![Modül Ekle iletişim kutusu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Gözden geçirme yazma modülü

İnceleme yazma modülü, kullanıcıların bir ürünü oturum açmalarını, derecelendirmesine ve bir ürün incelemesi yazmalarına olanak tanıyan bir **inceleme yaz** düğmesi içerir. Bu modül ayrıca kullanıcıların daha önceden gönderdikleri bir derecelendirme veya gözden geçirmelerini sağlar. Bu modül, bir PDP üzerinde genellikle derecelendirme çubuk grafiği ve ürün incelemeleri liste modüllerinin üzerinde görünür.

Aşağıdaki şekil, bir müşteri **gözden geçirme yaz** 'ı seçtiğinde beliren bir **gözden geçirme yazma** iletişim kutusunu göstermektedir. Müşteri bu iletişim kutusunu, bir derecelendirme ve İnceleme göndermek için kullanabilir.

![Gözden geçirme iletişim kutusu yazma](media/rnr-eCommerce-write-review-module.png)

Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken yazma İnceleme modülünü gösterir.

| Özellik adı | Değer        | Özellik açıklaması                 |
|---------------|--------------|--------------------------------------|
| Dosya Adı          | İnceleme yaz | İnceleme yazma modülünün adı. |

### <a name="ratings-histogram-module"></a>Derecelendirme çubuk grafik modülü

Derecelendirmeler çubuk grafik modülü bir derecelendirme çubuk grafik gösterir. Bu modül tipik olarak, bir PDP üzerindeki İnceleme yazma modülü ile ürün değerlendirmeleri listesi modülü arasında görüntülenir.

Derecelendirme çubuk grafiği modülü için konfigürasyon gerekmez. Modülü PDP şablonuna eklemeniz yeterlidir. 

Aşağıdaki çizimler, PDP'lerde görüntülenmek üzere derecelendirmeler ve incelemeler modülleri yapılandırıldığında bir PDP şablonunun Dynamics 365 Commerce içinde nasıl göründüğünü gösterir.

![PDP'lerde görüntülenmek üzere derecelendirme ve İncelemeler yapılandırıldığında PDP şablonu](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Ürün değerlendirmeleri liste modülü

Ürün gözden geçirme listesi modülü sıralama, filtre ve sayfalandırma seçenekleriyle birlikte ürün incelemelerinin listesini gösterir. Bu modül, genel olarak bir PDP üzerindeki derecelendirme çubuk grafik modülünden sonra görüntülenir.

Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken ürün değerlendirmeleri listesi modülü özelliklerini gösterir.

| Özellik adı              | Değer | Özellik açıklaması |
|----------------------------|-------| ---------------------|
| her sayfada gösterilen incelemeler | 10    | PDP'de bir seferde gösterilmesi gereken gözden geçirme sayısı. Kullanıcıların gözden geçirme sayfalarında hareket edebilmesi için **sonraki** ve **önceki** düğmeler eklenmiştir. |

#### <a name="ratings-histogram--summary-view"></a>Derecelendirme çubuk grafiği – Özet görünümü

Ürün değerlendirmeleri listesi modülü, bir derecelendirme çubuk grafiği modülü ekleyebileceğiniz bir yuva içerir. Aşağıdaki şekil, Dynamics 365 Commerce'teki Ürün İncelemeleri listesi modülünde bir derecelendirme çubuk grafiği modülünü nasıl ekleyekullanabileceğinizi gösterir .

![Ürün eleştiriler listesi modülünde derecelendirme çubuk grafiği modülü ekleme](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Derecelendirme ve incelemeleri gösterecek site yapılandırma

Kiracı kimliği, metin uzunluğunu gözden geçirme ve Başlık uzunluğunu gözden geçirme gibi derecelendirmeler ve incelemelerde ilgili konfigürasyon değerleri site düzeyinde yapılandırılır. 

Derecelendirmeleri ve değerlendirmeleri göstermek üzere bir site yapılandırmak için, aşağıdaki adımları izleyin. 

1. **Ev \> Siteler**e gidin.
1. Sitenizin adını belirtin. 
1. **Site yönetimi \> Genişletilebilirliği** bölümüne gidin. 
1. **En fazla metni gözden geçir** alanına, metni İnceleme için gereken maksimum karakter sayısını (örneğin, **1000**) girin. 
1. **En fazla başlık gözden geçir** alanına, başlık İnceleme için gereken maksimum karakter sayısını (örneğin, **55**) girin. 
1. **kaydet ve yayınla**yı seçin. 

Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.

![Derecelendirme ve incelemeleri gösterecek site yapılandırma](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama

Ürün derecelendirmesi, PDP'nin en üstünde ürün başlığının altında gösterilir. Ürün derecelendirmesi, aynı PDP'nin **incelemeler** bölümüyle bağlantılı olacak şekilde konfigüre edilebilir. 

Bir ürün derecelendirmesini PDP 'nin **incelemeler** bölümüne bağlamak için aşağıdaki adımları izleyin.

1. PDP şablonu açın. 
1. **Satın alma kutusu konteyner modülü ayarlarına** git.
1. **Satınalma kutusu** altında, **ürün derecelendirmeleri**'ni seçin ve sonra **bağlantıyı tam gözden geçirme modülü için tıklatın** onay kutusunu seçin.

Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.

![Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Gizlilik ve ilke sayfası için bağlantıyı yapılandırın

Gizlilik ve ilke sayfası için bağlantıyı yapılandırmak için şu adımları izleyin.

1. **Ev \> Siteler**e gidin.
1. Sitenizin adını belirtin. 
1. **Site yönetimi \> Genişletilebilirliği** bölümüne gidin
1. **Rotalar** sekmesinde, **RNR Gizlilik ve ilke** altında **bağlantı ekle**'yi seçin. Zaten bir bağlantı girilmiş ve bunu değiştirmek istiyorsanız, bağlantıyı seçin. 
1. **Bağlantı ekle** iletişim kutusunda gizlilik ve ilke sayfası bağlantısını seçin ve **Tamam**'ı seçin. 
1. **kaydet ve yayınla**yı seçin. 

Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.

![Gizlilik ve ilke sayfası için bağlantıyı yapılandırın](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirme ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)
