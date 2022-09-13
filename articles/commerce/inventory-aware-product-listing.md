---
title: Stoğa duyarlı ürün listelemesi
description: Bu makalede, kuruluşların Microsoft Dynamics 365 Commerce e-ticaret web sitelerindeki ürün listeleme sayfalarını, stoğa duyarlı olacak şekilde nasıl yapılandırabileceği açıklanır.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: e33a4dd8650ee2e371c51c5a19e955f2d2bdade2
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405570"
---
# <a name="inventory-aware-product-listing"></a>Stoğa duyarlı ürün listelemesi

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makalede, kuruluşların Microsoft Dynamics 365 Commerce e-ticaret web sitelerindeki ürün listeleme sayfalarını, stoğa duyarlı olacak şekilde nasıl yapılandırabileceği açıklanır. Ürün listeleme sayfaları, kategori giriş sayfaları ve arama sonuçları sayfalarını içerir.

Alışverişçiler bir ürün stokta olmadığında ne yapacaklarına karar verebilmek için, genellikle ürün keşfinin e-ticaret sitesi genelinde stoğa duyarlı olmasını beklerler. [Commerce modül kitaplığı](starter-kit-overview.md) kategori ve arama sonuçları modülü, envanter verilerini içerecek şekilde yapılandırılabilir. Bu sayede aşağıdaki deneyimleri sağlayabilirler:

- Stok düzeyi etiketlerini ürünlerle birlikte görüntüleme.
- Stok dışı ürünleri ürün listesinden gizleyin.
- Stok dışı ürünleri gösterin ürün liste sayfalarının en altına taşıma.
- Stok tabanlı ürün filtrelemeyi destekleme.

Bu deneyimleri etkinleştirmek için, öncelikle Commerce headquarters'ta **Stoğa duyarlı olacak şekilde geliştirilmiş e-Ticaret ürün keşfi** özelliğini etkinleştirmeniz gerekir.

> [!NOTE]
> Commerce 10.0.29 ve üzeri sürümlerde, **Stoğa duyarlı olacak şekilde geliştirilmiş e-Ticaret ürün keşfi** özelliği varsayılan olarak etkindir.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Stok kullanılabilirliği için ürün özniteliğini ayarlama

Stoğa duyarlı ürün listelemesi, ürün öznitelikleri çerçevesini kullanır. Önkoşul olarak, stok kullanılabilirlik verilerini yakalamak için ayrılmış bir ürün özniteliği oluşturulmalıdır.

Commerce Headquarters'ta stok kullanılabilirliği için ürün özniteliğini ayarlamak üzere aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Retail ve Commerce BT \> Ürünler ve stok \> Ürün özniteliklerini stok düzeyiyle doldur**'a gidin.
1. **Ürün özniteliklerini stok düzeyiyle doldur** iletişim kutusunda, **Ürün özniteliği ve tür adı** alanına stok verilerini yakalamak üzere oluşturulacak ayrılmış ürün özniteliği için özel bir ad girin.
1. **Stok kullanılabilirliği ölçütü** alanında, stok düzeyi hesaplamasının temel alınması gereken miktar türünü seçin: **Kullanılabilir fiziksel** veya **Toplam kullanılabilir**.
1. **Toplu işleme** seçeneğini **Evet** olarak ayarlayın.
1. **Tamam**'ı seçin.

> [!NOTE]
> E-ticaret web sitenizin sayfaları arasında tutarlı stok düzeyi hesaplaması için, hem **Ürün özniteliklerini stok düzeyiyle doldur** işine yönelik **Stok kullanılabilirliği ölçütü** alanında hem de Commerce site oluşturucudaki **Stok düzeyi ölçütü**'nde aynı miktar türünü seçtiğinizden emin olun.

Ayrılmış ürün özniteliği oluşturulduktan sonra, bir sonraki adım çevrimiçi kanalın özniteliğini yapılandırmaktır.

Commerce Headquarters'ta çevrimiçi kanalın özniteliğini yapılandırmak için aşağıdaki adımları izleyin.

1. **Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. Stoğa duyarlı ürün listeleme deneyiminin etkinleştirileceği çevrimiçi kanalı seçin.
1. İlişkili bir öznitelik grubunu seçin ve açın, ardından yeni ürün özniteliğini buna ekleyin.
1. **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım planı**'na gidin ve **1150** (**Katalog**) işini yürütün. Bu işi **Ürün özniteliklerini stok düzeyiyle doldur** işiyle aynı sıklıkta çalışacak bir toplu iş olarak zamanlamanızı öneririz.

> [!NOTE]
> Commerce sürüm 10.0.26 ve önceki sürümlerde, bir öznitelik grubuna stok kullanılabilirliği ürün özniteliğini ekledikten sonra, **Öznitelik meta verilerini ayarla**'yı seçmeniz ve sonra yeni ürün özniteliği için **Özniteliği kanalda göster**, **Alınabilir**, **İyileştirilebilir** ve **Sorgulanabilir** seçeneklerini açmanız gerekir.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Ürün listeleme sayfalarında stok dışı ürünlerin görüntülenme davranışını yapılandırma

Önceki tüm yapılandırma adımları tamamlandıktan sonra, kategori ve arama sonuçları sayfalarındaki iyileştiriciler stok tabanlı filtre seçeneğine sahip olacaktır. Sayfada görünen her bir ürün kutucuğu için bir stok düzeyi etiketi görüntülenir.

Kategori ve arama sonuçları sayfası, ürünleri ürün çeşidi düzeyinde değil, ürün ana düzeyinde görüntüler. Her bir ürünle birlikte görüntülenen stok düzeyi, bir ürünün tüm çeşitlerinin stok düzeyiyle belirlenen toplu bir stok düzeyidir. Bir çeşidin stok düzeyi, Commerce Headquarters'daki çevrimiçi kanalın varsayılan ambarında o çeşidin eldeki stoğu temel alınarak hesaplanır. Bir ana ürünün stok düzeyi, stokta ve stok dışı durumlarını temsil eden iki olası değere sahiptir. Bir ana ürün, tüm çeşitleri stokta olmadığı zaman stokta değil olarak değerlendirilir. Aksi takdirde ürün, stokta olarak değerlendirilir. Değerin etiketi, [stok düzeyi](inventory-buffers-levels.md) tanımından alınır. Hiçbir stok düzeyi tanımlanmazsa, varsayılan etiketler (İngilizce olarak) **Kullanılabilir** ve **Stokta yok**'tur.

Commerce site oluşturucudaki **Ürün listesi sayfaları stok ayarları** ayarını, kategori ve arama sonuçları sayfasının stok dışı ürünleri nasıl göstereceğini denetlemek üzere yapılandırabilirsiniz. Daha fazla bilgi için, [Envanter ayarları uygula](inventory-settings.md) konusuna bakın.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
