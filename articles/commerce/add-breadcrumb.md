---
title: İçerik haritası modülü
description: Bu konu içerik haritası modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c6d846686e3214e976a55271694382d7c5973ed
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417404"
---
# <a name="breadcrumb-module"></a>İçerik haritası modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu içerik haritası modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

İçerik haritası modülleri, site sayfalarında ikincil gezinti sağlamak için kullanılır. Bunlar genellikle sayfanın üst bölümünde, başlığın altında gösterilir. Herhangi bir sayfaya içerik haritası modülleri eklenebilse de, bunlar genellikle ürün kategori hiyerarşisini göstermek ve bir sitede dolaşmak için hızlı bir yol sağlamak amacıyla Ürün Ayrıntılar sayfalarında (PDPs) kullanılır. Bir içerik haritası modülü, kullanıcılar arama veya liste sayfasından bir PDP açtıklarında "sonuçları geri dön" bağlantısını göstermek için de kullanılabilir. Böylece, kullanıcılar alışverişe devam etmek için filtre uygulanmış liste sayfasına hızlıca dönebilir.

PDPs ve kategori sayfaları gibi ürün kategorisi bağlamı bulunan sayfalarda, içerik haritası modülleri kategori hiyerarşisini gösterir. Kategori bağlamına sahip olmayan sayfalarda, içerik haritası modülleri Varsayılan olarak **&lt;site kökü&gt; / &lt;Geçerli sayfasını&gt;** gösterir. İçerik haritası modülleri, sitedeki belirli sayfalara yönelik bağlantıları göstermek üzere diğer site sayfası türlerinde da el ile yapılandırılabilir.

Aşağıdaki resimde, bir PDP üzerinde kategori hiyerarşisini gösteren bir içerik haritası modülü örneği gösterilmektedir.

![içerik haritası modülü örneği](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>İçerik haritası modülü ayarları

İçerik haritası modülü, Site oluşturucuda **site ayarları \> Uzantılarda** tanımlanan **PDP ayarında içerik haritası görüntüleme** türüne dayanır. Bu seçenek üç olası değer vardır:

- **Kategori hiyerarşisini göster** – Bu değer seçildiğinde, içerik haritası modülü PDP 'de görüntülenen ürünün tam kategori hiyerarşisini gösterir.
- **Sonuçlara geri dön** – Bu değer seçildiğinde, içerik haritası modülü, Kullanıcı PDP'yi "geri dön" bağlantısına izin veren bir modülden açarsa bir PDP'de "sonuçları geri dön" bağlantısını gösterecektir. Kullanıcılar kategori, arama, liste ve öneri listeleri sayfalarından gezindiğinizde bu işlev kullanılabilir. Bu işlevi desteklemek için, ürün koleksiyonu ve arama sonuçları modülleri, **PDP 'deki sonuçlara yeniden izin ver** adında bir özelliğe sahiptir. Bu özellik, PDP 'deki "sonuçlara dön" bağlantı işlevini desteklemesi gereken modülleri tanımlama esnekliği sağlar. Örneğin, **içerik haritası modülünün PDP** ayarında içerik haritası görüntüleme türü için **sonuçlara geri döndüğünüzde** seçilir ve **arama sayfası arama sonuçları modülü için** PDP ile ilgili sonuçlara geri dönme olanağı varsa , kullanıcılar arama sayfasından bir PDP 'ye gezinirse "sonuçlara dön" bağlantısı görüntülenir.
- **Kategori hiyerarşisini göster ve sonuçlara dön** – Bu değer önceki iki değerin birleşimidir. Bu değer seçildiğinde, içerik haritası modülü bir PDP üzerinde hem tam kategori hiyerarşisini hem de "sonuçları geri" bağlantısı (yapılandırılmışsa) gösterir.

## <a name="breadcrumb-module-properties"></a>İçerik haritası modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Kök | Metin veya bağlantı| Bu isteğe bağlı özellik, içerik haritası site kökünün bağlantı metnini ve bağlantı hedefini belirtir. Bu özellik yapılandırılmazsa, kök tanımlanmayacaktır. |
| İçerik haritası bağlantısı | Bağla | Bu isteğe bağlı özellik, el ile konfigüre edilmiş bir içerik haritası için bağlantıları belirtir. Bağlantılar listelendikleri sırada görüntülenir. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Yeni sayfaya içerik haritası modülü ekleme

Bir PDP'ye içerik haritası modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Site ayarları /> uzantılarına** gidin ve **PDP ayarında içerik haritası görüntüleme türü** için **Kategori hiyerarşisini göster**'i seçin.
1. **Şablonlara** gidin ve PDP şablonunu seçin.
1. **Konteyner** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalara** gidin ve PDP şablonunu kullanan bir PDP açın. Bir PDP henüz oluşturulmamışsa, bir tane oluşturun.
1. **Konteyner** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.
1. **İçerik haritası** yuvasının Özellikler bölmesinde , **kök** altında **bağlantı metni** 'ni seçin.
1. **Bağlantı metni** iletişim kutusunda **giriş**'ı girin ve sonra **bağlantı hedefi** altında **bağlantı Ekle** 'yi seçin.
1. **Bağlantı ekle** iletişim kutusunda içerik haritası kökü bağlantısını seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[Ürün topluluğu modülleri](product-collection-module-overview.md)

[Satınalma kutusu modülü](add-buy-box.md)