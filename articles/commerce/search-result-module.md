---
title: Arama sonuçları modülü
description: Bu konu arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dc4a01e520379a74ca3b21c1d588531412e762be
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647524"
---
# <a name="search-results-module"></a>Arama sonuçları modülü

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

rama sonuçları modülü, ürün arama sonuçlarını ve ürünler için geçerli iyileştiricilerin bir listesini döndürür. Dynamics 365 Commerce sitelerindeki arama sonuçları modülleri, aşağıdaki senaryoların sayfalarını işlemek için kullanılabilir:

- Kullanıcı araması tarafından başlatılan arama sonuçları
- "Benzer ürün görünümleri" gibi belirli bir ürün kümesini gösteren arama sonuçları
- Belirli bir kategoriye ait olan ürün listeleri.

Kategori ve arama sonuçları sayfaları hakkında daha fazla bilgi için bkz. [Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md).

Aşağıdaki resimde Fabrikam sitesindeki bir kategori için arama sonuçları sayfası örneği gösterilmektedir.

![Fabrikam sitesindeki arama sonuçları sayfası örneği.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Arama sonuçları modülü özellikleri

Aşağıdaki tabloda, arama sonucu modüllerinin özellikleri, değerleri ve açıklamaları ile birlikte listelenmiştir.

| Özellik | Değerler | Tanım |
|----------|--------|-------------|
| Sayfa başına öğe sayısı | Tamsayı | Her sayfada gösterilen maddelerin sayısı. |
| PDP üzerinde yeniden izin ver | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, kullanıcı arama sonuçları sayfasında bir ürün seçtiğinde, açılan ürün ayrıntıları sayfasındaki (PDP) içerik haritası gezintisi "Sonuçlara geri dön" bağlantısını gösterir. |
| İyileştiricileri genişlet | **Tümü**, **1**, **2**, **3** veya **4** | Bir sayfa yüklendiğinde genişletilmesi gereken en iyi iyileştiricilerin sayısı. Örneğin, bu özellik **3** olarak ayarlanırsa, sayfadaki ilk üç iyileştirici genişletilir. |
| Kategori hiyerarşisi görüntüsünü gizle | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, sayfadaki kategori hiyerarşisi ekranı gizlenir. Kategori hiyerarşisini göstermek için [içerik haritası modülünü](add-breadcrumb.md) kullanıyorsanız bu özellik **Doğru** olarak ayarlanmalıdır.|
| Ürün özniteliklerini arama sonuçlarına dahil et | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, arama sonuçlarındaki ürünler için öznitelikler döndürülür. Bu öznitelikler bir Ticaret sitesinde gösterilebilse de, bir uzantı gereklidir.|
| İlişki fiyatlarını göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, oturum açmış bir kullanıcı sayfaya göz attığında, ürünlerin bağlı kuruluş fiyatları arama sonuçlarında gösterilir. |
| İyileştirici panelini güncelleştir | **Doğru** veya **yanlış** | Bu özellik **doğru** olarak ayarlanırsa, iyileştiriciler seçildiğinde iyileştirici paneli güncelleştirilir. Bu modda, bazı çok seçimli iyileştiriciler, iyileştirici paneli güncelleştirildiğinde tek seçimli iyileştiriciler gibi davranır. |

> [!IMPORTANT]
> Commerce 10.0.16 sürümünde ve sonrasında, **Bağlı kuruluş fiyatlarını göster** yapılandırması, sayfada bağlı kuruluş fiyatlarını göstermek için kullanılabilir.
>
> Commerce sürüm 10.0.20 sürümünde ve daha sonra, iyileştirici seçiminde iyileştiriciyi güncelleştirmek için kullanılabilen **İyileştirici panelini güncelleştir** yapılandırmasını güncelleştirmek için kullanılabilir.

## <a name="supported-modules"></a>Desteklenen modüller

Arama sonuçları modülü, kullanıcıların ürün bilgilerini görüntülemesine ve bir arama sonuçları sayfasından alışveriş sepetine ürün eklemesine olanak veren [hızlı görüntüleme modülünü](quick-view-module.md) destekler.

## <a name="add-a-search-results-module-to-a-category-page"></a>Kategori sayfasına arama sonuçları modülü ekleme

Kategori sayfasına arama sonuçları modülü eklemek için bu adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusuna **Arama sonuçları** adını girin ve **Tamam**'ı seçin.
1. **Gövde** bölmesi için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **Ana** bölmeyi seçin, üç nokta düğmesini (...) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.
1. **İçerik haritası** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin.
1. **Konteyner** yuvası için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda, **Arama sonuçları** modülünü seçin ve **Tamam**'ı seçin.
1. **Arama sonuçları** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin ve arama sonuçları modülü için gerekli diğer özellikleri ayarlayın. Şablonda bu özellikleri ayarlayarak, belirli bir kategori sayfasındaki özelleştirmelerin bu ayarları otomatik olarak içermesini sağlayabilirsiniz.
1. **Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda, oluşturduğunuz **Arama sonuçları** şablonunu seçin, **Sayfa adı** için **Kategori sayfası** girin ve sonra **Tamam**'ı seçin. Tüm değerler şablonda ayarlandığı için sayfa yayınlanmaya hazırdır.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Arama sonuçları modülü için stok farkındalığını etkinleştirme

Müşteriler genellikle bir e-ticaret sitesinin göz atma deneyiminin tamamında stok bilinçli olmasını bekler, böylece bir ürün için stok olmadığında ne yapılacağına karar verebilirsiniz. Arama sonuçları modülü, envanter verilerini içerecek ve aşağıdaki deneyimleri sağlayacak şekilde gelişmiş olabilir:

- Ürünlerle birlikte stok kullanılabilirliği etiketini göster.
- Stok dışı ürünleri gizleyin.
- Arama sonuçları listesinin sonundaki stok dışı ürünleri gösterin.
    
Bu deneyimleri etkinleştirmek için, Commerce Headquarters'ta aşağıdaki önkoşul ayarlarını konfigüre etmelisiniz.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Stoğa duyarlı olacak şekilde geliştirilmiş e-Ticaret ürün keşfi özelliğini etkinleştirme

> [!NOTE]
> **Stok duyarlılığı özelliğine sahip gelişmiş e-ticaret ürün bulma** özelliği, Commerce sürüm 10.0.20'den itibaren kullanılabilir.

**Stoğa duyarlı olacak şekilde geliştirilmiş e-Ticaret ürün keşif** özelliğini Commerce Headquarters'ta etkinleştirmek için aşağıdaki adımları izleyin.

1. **Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. **Stoğa duyarlı olacak şekilde geliştirilmiş e-Ticaret ürün keşfi özelliğini etkinleştirme** özelliğini bulup etkinleştirin.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Ürün özniteliklerini stok düzeyiyle doldur işini konfigüre edin

**Ürün özniteliklerini stok düzeyiyle doldur** işi, yeni bir ürün özniteliği oluşturarak stok kullanılabilirliğini yakalar ve ardından bu özniteliği her bir ana ürün için en yeni stok düzeyine ayarlar. Sürekli olarak satılan bir ürün veya sınıflama stok kullanılabilirliği olduğundan, işi toplu iş işlem olarak zamanlamanızı öneririz.

Commerce Headquarters'ta **Ürün özniteliklerini stok düzeyi işi ile doldur** işini konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Retail ve Commerce BT \> Ürünler ve stok**'a gidin.
1. **Ürün özniteliklerini stok düzeyiyle doldur**'u seçin.
1. **Ürün niteliklerini stok düzeyi ile doldur** iletişim kutusunda şu adımları izleyin:

    1. **Parametreler** altında, **Ürün özniteliği ve tür adı** alanında, stok kullanılabilirliğini yakalamak için oluşturulacak adanmış ürün özniteliği için bir ad belirtin.
    1. **Parametreler** altında, **Stok kullanılabilirliği ölçütü** alanında, stok düzeyi hesaplamasının temel alınması gereken (örneğin, **Kullanılabilir fiziksel**) miktarı seçin.
    1. **Arka planda çalıştır** altında, işi arka planda çalışacak şekilde konfigüre edin ve isteğe bağlı olarak **Toplu işleme** seçeneğini etkinleştirin. 

> [!NOTE]
> PDP'ler ve ürün listesi sayfaları arasında, e-ticaret sitenizdeki tutarlı stok düzeyi hesaplaması için, Commerce Headquarters'ta hem **Stok kullanılabilirliği ölçütü** hem de Commerce site oluşturucudaki ayara göre **Stok düzeyi ölçütü** miktar seçeneğini seçtiğinizden emin olun. Site oluşturucuda stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Yeni ürün özniteliğini konfigüre edin

**Ürün özniteliklerini stok düzeyi işiyle doldurun** işini çalıştırıldıktan sonra, arama sonuçları modülü için stok tanımayı etkinleştirmek istediğiniz yerdeki e-ticaret sitesinde yeni oluşturulan ürün özniteliğini konfigüre etmelisiniz.

Commerce Headquarters'ta yeni ürün özniteliğini konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin ve e-ticaret sitesini seçin.
1. İlişkili bir öznitelik grubunu seçin ve açın, yeni oluşturulan ürün özniteliğini buna ekleyin ve sonra sayfayı kapatın.
1. **Öznitelik meta verilerini ayarla**'yı seçin, yeni eklenen ürün özniteliğini seçin ve sonra **Özniteliği kanal üzerinde göster**, **Alınabilir**, **Ayrıntılandırılabilir** ve **Sorgulanabilir** seçeneklerini etkinleştirin.

> [!NOTE]
> Arama sonuçları modülünde gösterilen ürünler için, stok düzeyi bağımsız değişken düzeyi yerine ana ürün düzeyinde girilir. Yalnızca iki olası değere sahiptir: "kullanılabilir" ve "stokta yok". Değerlerin gerçek metni, [Stok düzeyi profili](inventory-buffers-levels.md) tanımından alınır. Bir ana ürün, yalnızca tüm varyantlar stokta olmadığı zaman stokta değil olarak değerlendirilir. Bir varyantın stok düzeyi, ürünün stok düzeyi profil tanımına göre belirlenir. 

Önceki tüm yapılandırma adımları tamamlandıktan sonra, arama sonuçları sayfalarındaki iyileştiriciler stok tabanlı filtre gösterecektir ve arama sonuçları modülü arka plandaki stok verilerini geri alır. Daha sonra, Commerce site oluşturucuda **Ürün listesi sayfaları ayarı için stok ayarlarını**, arama sonuçları modülünün stok dışı ürünleri nasıl göstereceğini denetlemek üzere konfigüre edebilirsiniz. Daha fazla bilgi için, [Envanter ayarları uygula](inventory-settings.md) konusuna bakın.

## <a name="additional-resources"></a>Ek kaynaklar

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Hızlı görünüm modülü](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
