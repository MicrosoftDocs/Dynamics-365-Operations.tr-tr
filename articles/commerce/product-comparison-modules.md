---
title: Ürün karşılaştırma modülleri
description: Bu makalede, ürün karşılaştırma modülleri ve müşterilerin Microsoft Dynamics 365 Commerce e-ticaret web sitelerinde ürün karşılaştırmaları yapabilmesi için bunların nasıl uygulanacağı anlatılmaktadır.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 6fd851ce6b32d0772c3fe23c4d7bd4dae2616fdc
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474139"
---
# <a name="product-comparison-modules"></a>Ürün karşılaştırma modülleri

[!include [banner](../includes/banner.md)]

Bu makalede, ürün karşılaştırma modülleri ve müşterilerin Microsoft Dynamics 365 Commerce e-ticaret web sitelerinde ürün karşılaştırmaları yapabilmesi için bunların nasıl uygulanacağı anlatılmaktadır.

> [!NOTE]
> Ürün karşılaştırma ve ürün karşılaştırma düğmesi modülleri Dynamics 365 Commerce 10.0.29 sürümü itibariyle kullanılabilir. Bunlar işletmeden tüketiciye (B2C) ve işletmeden işletmeye (B2B) web sitelerinde kullanılabilir.

Ürün karşılaştırma işlevi, tüketicilerin daha iyi satın alma kararları vermelerine yardımcı olmak için ürün karşılaştırma sayfasındaki ürün ayrıntılarını karşılaştırmalarını sağlar. Bu işlev, ürün karşılaştırma modülü kullanılarak Commerce site oluşturucuda yapılandırılır. Kategori sonuçları, arama sonuçları ve ürün koleksiyonları sayfaları gibi ürün listesi sayfalarında (PLP'ler), tüketicilerin karşılaştırma tepsisine ürün eklemesine olanak tanıyan ürün karşılaştırma düğmesi yapılandırabilirsiniz. Bu işlevsellik, [hızlı görüntüleme modülü](quick-view-module.md) gibi çalışan ürün karşılaştırma düğmesi modülü kullanılarak site oluşturucuda yapılandırılır.

Site kullanıcıları karşılaştırma yapılacak ürünleri ürün kutucukları üzerinden seçerek eklediğinde, sayfanın alt kısmında bir karşılaştırma tepsisi belirir. Karşılaştırma tepsisi, müşterinin şu anda karşılaştırdığı ürünleri ürünlerin kısa önizlemeleri ile birlikte gösterir. Site kullanıcıları ürün ayrıntıları sayfalarından (PDP'ler) da ürün ekleyebilir ve ana ürünlerle karşılaştırmak için belirli ürün çeşitleri ekleyebilirler.

Müşteriler karşılaştırma tepsisine birkaç ürün ekledikten sonra, bir ürün karşılaştırma sayfasına yeniden yönlendirilmek için **Karşılaştır**'ı seçebilir. Ürün karşılaştırma sayfası, müşterilerin resimleri, fiyatları, ürün boyutlarını (boyut, stil ve renk), toplu derecelendirme bilgilerini ve diğer ürün niteliklerini karşılaştırabilmesi için, her seçili ürün için ürün ayrıntılarını gösterir.

Aşağıdaki şekil, ürünü karşılaştır düğmesinin, karşılaştırmadan kaldır düğmesinin, karşılaştırma tepsisinin ve ürün karşılaştırma sayfasının örneklerini gösterir.

![Ürünü karşılaştır düğmesini, karşılaştırmadan kaldır düğmesini, karşılaştırma tepsisi panelini ve ürün karşılaştırma sayfasını gösteren ürün karşılaştırmaya genel bakış.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Ürün karşılaştırma sayfası varsayılan bir ürün özellikleri kümesini ve belirli bir ürün için bir PDP üzerinde görüntülenebilecek tüm öznitelikleri karşılaştırır.
> - Teslimat modu, eldeki stok ve ölçü birimi gibi özellikler bir ürün karşılaştırma sayfasında görüntülenemez.
> - Müşteriler, ürünlerin aynı katalogdan olması koşuluyla, farklı kategorilerden ürünleri karşılaştırma tepsisine ekleyebilir.
> - Ürün karşılaştırma işlevi şu anda tek bir katalogdaki ürünleri karşılaştırmayla sınırlıdır. Site kullanıcıları çapraz katalog karşılaştırmaları yapamaz.
> - Tüm ürün karşılaştırma modülleri için **Modül istemci tarafını işle** özelliğinin temizlenmiş olduğundan emin olmalısınız.
> - Ürün karşılaştırma modülünün kullanıldığı tüm sayfalar için sayfa düzeyinde önbelleğe almanın devre dışı bırakıldığından emin olmalısınız. Bu sayfalara PDP'ler, PLP'ler ve ürün karşılaştırma sayfaları dahildir. Daha fazla bilgi için bkz. [Sayfa önbelleğe alma işlemini yapılandırma](e-commerce-extensibility/page-caching.md).

Aşağıdaki şekilde bir ürün karşılaştırma sayfası örneği gösterilmiştir.

![Ürün karşılaştırma sayfası.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Ürün karşılaştırma modülünü yeni bir ürün karşılaştırma sayfasına ekleme

Bir sayfanın gövdesine ürün karşılaştırma modülü ekleyerek adanmış bir ürün karşılaştırma sayfası oluşturabilirsiniz. Müşterilerin farklı ürünlerle ilgili ürün ayrıntılarını karşılaştırmasını sağlamaya ek olarak, ürün karşılaştırma modülünü, müşterilere ürünleri karşılaştırdıktan sonra satın alımı hemen tamamlama seçeneği sunacak şekilde yapılandırabilirsiniz. Ürün karşılaştırma modülü ayrıca boş durumunu (örneğin, "Ürün karşılaştırmanız boş") açıklayan bir içerik bloğu modülü ekleyebileceğiniz bir **Boş karşılaştırma** yuvası da içerir.

Yeni bir ürün karşılaştırma sayfasına ürün karşılaştırma modülü eklemek için aşağıdaki adımları izleyin.

1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusundaki **Sayfa adı** altında, uygun bir sayfa adı (örneğin, **Ürün karşılaştırma**) girin ve ardından **İleri**'yi seçin.
1. **Şablon seç** bölümünde, uygun şablonu (örneğin, varsayılan kategori sayfanız tarafından kullanılan şablonu) seçin ve ardından **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin.
1. **Ana yuva** alanında üç nokta (**...**) düğmesini, ardından **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda, **Ürün karşılaştırma** modülünü seçin ve **Tamam**'ı seçin.
1. **Hızlı görünüm düğmesi** yuvasında üç noktayı (**...**) seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Ürün hızlı görünümü** modülünü seçin ve **Tamam**'ı seçin.
1. Sağdaki özellikler bölmesinde **Ürün hızlı görünümü** modülünün özelliklerini yapılandırın.
1. **Boş karşılaştırma** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **İçerik bloğu** modülünü seçin ve **Tamam**'ı seçin.
1. Sağdaki özellikler bölmesinde **İçerik bloğu** modülünün özelliklerini yapılandırın. 
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

Aşağıdaki çizimde, site oluşturucudaki boş karşılaştırma sayfası örneği gösterilmektedir.

![Ürün karşılaştırma modülü.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Arama ve kategori sonuçları sayfalarında ürün kutucuklarına bir ürün karşılaştırma düğmesi ekleme

Ürün karşılaştırma düğmesi, kullanıcıların bir liste sayfasında ürünlere göz attıklarında, bir ürünü karşılaştırma tepsisine hızlı bir şekilde eklemesine olanak tanır. Bir veya daha fazla ürünü, bir PDP'ye gitmeksizin liste sayfasından bir karşılaştırma tepsisine ekleyebilirler.

Ürün karşılaştırma düğmesi, ürün koleksiyonu, arama sonuçları ve PDP satın alma kutusu modülleri tarafından desteklenir.

Arama ve kategori sonuçları sayfalarında ürün kutucuklarına bir ürün karşılaştırma düğmesi eklemek için şu adımları izleyin.

1. Site oluşturucuda **Sayfalar**'a gidin ve ürün karşılaştırma düğmesi eklemek istediğiniz kategori sayfasını açın.
1. **Ana yuva** alanında üç nokta (**...**) düğmesini, ardından **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda, **Arama sonuçları** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sonuçlar** modülünün **Ürün karşılaştırma düğmesi** yuvasında üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda, **Ürün karşılaştırma düğmesi** modülünü seçin ve **Tamam**'ı seçin.
1. Sağdaki özellikler bölmesinde **Ürün karşılaştırma düğmesi** modülünün özelliklerini yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Karşılaştırma tepsisinde gösterilecek maksimum ürün sayısını belirtme

Site oluşturucudaki **Site ayarları \> Uzantılar**'a giderek karşılaştırma tepsisinde gösterilecek en fazla ürün sayısını belirtebilirsiniz. Masaüstü ve mobil/tablet görünümleri için ayrı maksimum sınırlar yapılandırabilirsiniz. Varsayılan olarak, maksimum sınır tanımlanmazsa hiçbir sınır uygulanmaz.

> [!NOTE]
> En iyi gözatma deneyimi için, gerekli yatay kaydırma miktarını azaltmak amacıyla, mobil görünüm pencereleri için karşılaştırma tepsisindeki maksimum ürün sayısını **2**'ye ve masaüstü görünüm pencereleri için **4**'e ayarlamanız önerilir.

Karşılaştırma tepsisindeki maksimum ürün sayısını belirtmek için şu adımları izleyin.

1. Site oluşturucuda **Site ayarları \> Uzantılar**'a gidin.
1. **Karşılaştırma sınırındaki ürünler - masaüstü aygıtları** özelliği için, masaüstü görünüm pencereleri için karşılaştırma tepsisinde gösterilmesi gereken maksimum ürün sayısını girin.
1. **Karşılaştırma sınırındaki ürünler - mobil ve tablet aygıtları** özelliği için, mobil ve tablet görünüm pencereleri için karşılaştırma tepsisinde gösterilmesi gereken maksimum ürün sayısını girin.
1. Komut çubuğunda, **Kaydet ve yayınla** öğesini seçin.

![Karşılaştırma tepsisindeki ürünleri sınırlamak için site ayarları.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
