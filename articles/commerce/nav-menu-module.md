---
title: Gezinti menüsü modülleri
description: Bu makale gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281521"
---
# <a name="navigation-menu-module"></a>Gezinti menüsü modülleri

[!include [banner](includes/banner.md)]

Bu makale gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Gezinti menüsü modüllerinin başlıca amacı, site kullanıcılarının Dynamics 365 Commerce yönetim merkezinde tanımlanan kanal gezinti hiyerarşisine göre ürün ve site sayfalarına göz atmasına olanak sağlamaktır. Bir gezinti menüsü modülünde yapılandırılan öğeler site üstbilgisi gezintisi olarak görünür. Gezinti menüsü modülleri, bir e-ticaret sitesindeki diğer sayfalara bağlantı sağlayan statik menü öğelerini de destekler.

Gezinti menüsü modülü bir sayfanın üst bilgi modülüne eklenebilir. Fabrikam temasında, gezinti menüsü varsayılan olarak iki düzey gösterir. Starter temasında, gezinti menüsü varsayılan olarak üç düzey gösterir. Düzey sayısını değiştirmek için temada bir görünüm uzantısı gereklidir.

Aşağıdaki çizimde, iki düzey kategori hiyerarşisi ve bazı statik menü öğeleri bulunan Fabrikam sitesi için bir gezinti menüsü örneği gösterilmektedir.
![Gezinti menüsü modülü örneği.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Gezinti menüsü modüllerinin özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Kaynak                  | **Perakende**, **El ile yazma**, **Perakende ve el ile yazma** | **Perakende** değeri, Commerce yönetim merkezinde kanal gezinme hiyerarşisinin gezinti menüsünde görüntülenmesini sağlar. **El ile yazma** değeri statik menü öğelerinin oluşturulmasına izin verir. **Perakende ve el ile yazma** değeri, her ikisinin karışımına izin verir. |
| Kategori resimlerini göster | **Doğru** veya **yanlış**    | Etkinleştirildiğinde, bu özellik gezinti menüsündeki kategori resimlerini her kategori için Commerce yönetim merkezinde tanımlandığı şekilde görüntüler. Commerce sürüm 10.0.14'e eklendi. |
| Promosyon görüntülerini göster | **Doğru** veya **yanlış** | Bu özellik etkinleştirildiğinde, promosyonlar resimler, bağlantılar ve metin kullanılarak yapılandırılabilir. Bu özellik, Commerce 10.0.17 sürümüne eklenmiştir. |
|Kategori promosyon içeriği ekleme | Metin görüntü veya bağlantı | **Promosyon görüntülerini göster** özelliği etkinleştirildiğinde, gezinti menüsünde promosyon içeriği olarak metin, görüntü veya bağlantı ekleyebilirsiniz. |
| Çok düzeyli gezinti menüsünü etkinleştir | **Doğru** veya **yanlış** | Bu özellik etkinleştirildiğinde, gezinti menüsü gezinti hiyerarşisinin birden çok düzeyini gösterebilir. Bu özellik Commerce 10.0.15 sürümünde bulunur. |
| Düzey sayısı | tamsayı | Bu özellik, **çok düzeyli gezinti menüsünü etkinleştir** özelliği **true** olarak ayarlandığında gösterilmesi gereken düzey sayısını tanımlar. |
| Statik menü öğesi| Değerler dizisi| Bir menü öğesi adını statik site sayfasının bağlantısıyla ilişkilendiren statik menü öğeleri. Menü öğelerini diğer menü öğelerinin altında oluşturabilirsiniz. Varsayılan olarak, statik menüler kök düzeyinde görünür ve varsa kanal gezinme hiyerarşisine eklenir. |
| Kök menüyü göster | **Doğru** veya **yanlış** | Bu özellik etkinleştirildiğinde, gezinti menüsü özel bir kök altında tanımlanabilir (örneğin, **Şimdi alışveriş yap**). Bu özellik Dynamics 365 Commerce sürüm 10.0.15'de kullanılabilir. |
| Kök menü | dize | Bu özellik, **kök menüyü göster** özelliği **true** olarak ayarlandığında özel bir köke ait metni tanımlamak için kullanılabilir. |

Aşağıdaki çizimde, Fabrikam sitesinin gezinti menüsünde görüntülenen kategori resmi örneği gösterilmektedir.
![Kategori resimlerine sahip bir gezinti menüsü modülü örneği.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Üstbilgi modülüne gezinti menüsü modülü ekleme

Bir üstbilgi modülüne gezinti menüsü modülü ekleme hakkında ayrıntılar için, bkz. [Üstbilgi modülü](author-header-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[İçerik haritası modülü](add-breadcrumb.md)

[Site seçicisi modülü](site-selector.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)

[Üst bilgi modülü](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
