---
title: Arama sonuçları modülü
description: Bu makale arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: d10e9ed78dfc90833ff3c09021f863f6ef0b80d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286823"
---
# <a name="search-results-module"></a>Arama sonuçları modülü

[!include [banner](includes/banner.md)]

Bu makale arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

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

Site oluşturucuda bir kategoriye arama sonuçları modülünü eklemek için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusuna **Arama sonuçları** adını girin ve **Tamam**'ı seçin.
1. **Gövde** alanında, üç nokta (...) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Varsayılan Sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülündeki **Ana** alanında, üç nokta düğmesini (...) ve ardından **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (...) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.
1. **İçerik haritası** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin.
1. **Konteyner** alanında, üç nokta (...) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda, **Arama sonuçları** modülünü seçin ve **Tamam**'ı seçin.
1. **Arama sonuçları** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin ve arama sonuçları modülü için gerekli diğer özellikleri ayarlayın. Şablonda bu özellikleri ayarlayarak, belirli bir kategori sayfasındaki özelleştirmelerin bu ayarları otomatik olarak içermesini sağlayabilirsiniz.
1. **Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusunda **Sayfa adı** altında, **Kategori sayfası**'nı girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, oluşturduğunuz **Arama sonuçları** şablonunu seçin ve sonra **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Arama sonuçları modülü için stok farkındalığını etkinleştirme

Müşteriler genellikle bir e-ticaret web sitesinin göz atma deneyiminin tamamında stok bilinçli olmasını bekler, böylece bir ürün için stok olmadığında ne yapılacağına karar verebilirsiniz. Arama sonuçları modülü, envanter verilerini içerecek ve aşağıdaki deneyimleri sağlayacak şekilde yapılandırılabilir:

- Ürünle birlikte stok kullanılabilirliği etiketini göster.
- Stok dışı ürünleri ürün listesinden gizleyin.
- Ürün listesinin sonundaki stok dışı ürünleri gösterin.
- Arama sonuçlarındaki ürünleri stok düzeyine göre filtreleyin.

Bu deneyimleri etkinleştirmek için, öncelikle **Stok duyarlılığı özelliğine sahip gelişmiş e-ticaret ürün bulma** özelliğini, **Özellik yönetimi** çalışma alanında etkinleştirmeniz gerekir.

> [!NOTE]
> **Stok duyarlılığı özelliğine sahip gelişmiş e-ticaret ürün bulma** özelliği, Commerce sürüm 10.0.20 ve sonrasında kullanılabilir.

Stok duyarlı ürün arama, stok kullanılabilirlik bilgilerini elde etmek için ürün özniteliklerini kullanır. Özellik için ön koşul olarak, adanmış ürün öznitelikleri oluşturulmalıdır, bunlar için stok verileri girilmelidir ve bunlar çevrimiçi kanala eklenmelidir. 

Stok duyarlı arama sonuçları modülünü desteklemek üzere adanmış ürün öznitelikleri oluşturmak için aşağıdaki adımları izleyin.

1. Headquarters'da **Perakende ve Ticaret \> Perakende ve Ticaret BT \> Ürünler ve stok** bölümüne gidin.
1. **Ürün özniteliklerini stok düzeyiyle doldur**'u seçin ve açın.
1. İletişim kutusuna, aşağıdaki bilgileri girin:

    1. **Ürün özniteliği ve tür adı** alanında, stok verilerini yakalamak için oluşturulacak adanmış ürün özniteliği için bir ad belirtin.
    1. **Stok kullanılabilirliği ölçütü** alanında, stok düzeyi hesaplamasının temel alınması gereken (örneğin, **Kullanılabilir fiziksel**) miktar türünü seçin. 

1. İşi arka planda çalıştırın. Ürün stoku çok yönlü kanal ortamında sürekli olarak değiştiği için, bu işi, toplu işlem olarak planlamanızı öneririz.

> [!NOTE]
> Sayfalar ve modüller arasında, e-ticaret web sitenizdeki tutarlı stok düzeyi hesaplaması için, Commerce genel merkezinde hem **Stok kullanılabilirliği ölçütü** hem de Commerce site oluşturucudaki ayara göre **Stok düzeyi ölçütü** miktar türünü seçtiğinizden emin olun. Site oluşturucuda stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).

Çevrimiçi kanalın ürün özniteliklerini yapılandırmak için aşağıdaki adımları izleyin. 

1. Headquarters'da **Retail ve Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. Modül için stok duyarlı arama sonuçlarını etkinleştirmek üzere bir çevrimiçi kanal seçin.
1. İlişkili bir öznitelik grubunu seçin ve açın, ardından yeni oluşturulan ürün özniteliğini buna ekleyin.
1. 10.0.27 sürümünden önceki Commerce sürümleri için, **Öznitelik meta verilerini ayarla**'yı seçin, yeni eklenen ürün özniteliğini seçin ve sonra **Özniteliği kanal üzerinde göster**, **Alınabilir**, **Ayrıntılandırılabilir** ve **Sorgulanabilir** seçeneklerini etkinleştirin.
1. **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım planı**'na gidin ve **1150 (Katalog)** işini yürütün. **Ürün özniteliklerini, stok düzeyiyle doldur** işini toplu işlem olarak zamanlarsanız, 1150 işini ayrıca aynı frekansta çalışacak bir toplu işlem olarak zamanlamanızı öneririz.

> [!NOTE]
> Arama sonuçları modülünde gösterilen ürünler için, stok düzeyi bağımsız değişken düzeyi yerine ana ürün düzeyinde gösterilir. Yalnızca iki olası değere sahiptir: "kullanılabilir" ve "stokta yok". Değerin gerçek etiketi, [Stok düzeyi profili](inventory-buffers-levels.md) tanımından alınır. Bir ana ürün, yalnızca tüm varyantlar stokta olmadığı zaman stokta değil olarak değerlendirilir.

Önceki tüm yapılandırma adımları tamamlandıktan sonra, arama sonuçları sayfalarındaki iyileştiriciler stok tabanlı filtre gösterecektir ve arama sonuçları modülü arka plandaki stok verilerini geri alır. Daha sonra, Commerce site oluşturucuda **Ürün listesi sayfaları ayarı için stok ayarlarını**, arama sonuçları modülünün stok dışı ürünleri nasıl göstereceğini denetlemek üzere konfigüre edebilirsiniz. Daha fazla bilgi için, [Envanter ayarları uygula](inventory-settings.md) konusuna bakın.

## <a name="additional-resources"></a>Ek kaynaklar

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Hızlı görünüm modülü](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
