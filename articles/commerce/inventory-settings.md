---
title: Stok ayarlarını uygula
description: Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 77a3bde12fd047e15d7730903416cdb5263a8cd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972821"
---
# <a name="apply-inventory-settings"></a>Stok ayarlarını uygula

[!include [banner](includes/banner.md)]

Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .

## <a name="overview"></a>Özet

Stok ayarları alışveriş için ürün sepetine eklenmeden önce stokun denetlenip işaretlenmeyeceğini belirtir. Ayrıca, "stokta" ve "yalnızca birkaç soldaki" gibi, stokla ilgili Merchandising iletileri de tanımlarlar. Bu ayarlar, ürünün stokta bulunduğu durumda satın alınmamasını sağlar.

Dynamics 365 Commerce ürünler için eldeki kullanılabilir kullanılabilirlik tahminleri sağlar. Tahmini eldeki stok kullanılabilirliğinin nasıl hesaplandığı hakkında bilgi için bkz [perakende kanalları için envanter kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md).

Commerce Site Builder 'da stok eşikleri ve aralıkları bir ürün ya da kategori için tanımlanabilir. Stokta, düşük stokta veya stok dışı olduğu gibi sınıflandırılabileceği belirlenir. Ayrıntılar için bkz [Envanter tamponları ve envanter düzeylerini yapılandırma](inventory-buffers-levels.md).

> [!NOTE]
> Stok eşikleri ve aralıkları için destek Dynamics 365 Commerce 10.0.12 sürümünde bulunabilir.

## <a name="inventory-settings"></a>Envanter ayarları

Commerce'da stok ayarları, site oluşturucuda **Site Ayarlar \> Uzantılar \> Envanter yönetimi** tanımlanır . Dört stok ayarı vardır; bunlardan biri eskidir (kullanım dışı):

- **Uygulama üzerinde stok denetimini etkinleştir** – Bu ayar, ürün envanteri denetimini açar. Mağaza modüllerinde satın alma kutusu, alışveriş sepeti ve çekme için ürün stoğu kontrol edilir ve yalnızca stok varsa alışveriş sepetine bir ürün eklenmesine izin verilir.
- **Stok düzeyi temeli** - Bu ayar, stok düzeylerinin nasıl hesaplandığını tanımlar. Kullanılabilir değerler **Toplam kullanılabilir**, **fiziksel kullanılabilir** ve **stok dışı eşikler** dir. Commerce'da stok eşikleri ve aralıkları her ürün ya da kategori için tanımlanabilir. Stok API'Leri **Toplam kullanılabilir** özelliğin ve **fiziksel kullanılabilir** özelliğin ürün stok bilgilerini döndürür. Perakende, **kullanılabilen toplam** veya **fiziksel kullanılabilir** değerin stok sayısını ve stokta bulunmayan ve stok dışı durumları için bunlara karşılık gelen aralıkları belirlemek için kullanılabilir olup olmadığına karar verir.

    **Stok düzeyi ayar temel alınarak** ayarının **stokta bulunmayan eşik değeri** eski (eski), kullanımdan kalktı değeridir. Seçildiği zaman, stok sayımı **Toplam kullanılabilir** değerin sonuçlarından belirlenir , ancak eşik, daha sonra açıklanan **stok dışı eşiği** sayısal ayarı tarafından tanımlanır. Bu eşik ayarı bir e-ticaret sitesi içindeki tüm ürünlere uygulanır. Stok eşik numarasının altındaysa, bir ürün Stokta yer alır. Aksi takdirde stokta olduğu düşünülür. **Stok dışı eşik** değerinin yetenekleri sınırlıdır ve bunu sürüm 10.0.12 ve sonraki sürümlerde kullanmanızı önermeyiz.

- **Stok aralıkları** – Bu ayar, site modüllerinde iletinin gösterildiği stok aralıklarını tanımlar. Yalnızca, **Toplam kullanılabilir** değer veya **stok düzeyi ayar temel alınarak** ayarı için **fiziksel kullanılabilir** değer seçildiğinde uygulanabilir. Kullanılabilir değerler **tümü**, **düşük ve stok dışı** ve **Stok dışında**.

    - **Tümü** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) stokta değil ("stok dışı" iletisi) görüntülenir.
    - **Düşük ve stok dışı** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) görüntülenir.
    - **Stokta bulunmayan** seçildiğinde , yalnızca "stok dışı" iletisi gösterilir.

- **Stok dışı eşiği** – Bu eski sayısal ayar , yalnızca **stok düzeyi ayar temel alınarak** ayarı **stok dışı eşik** değeri seçildiğinde etkili olur.

> [!IMPORTANT] 
> Bu ayarlar Dynamics 365 Commerce 10.0.12 sürümünde bulunmaktadır. Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir. AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Stok ayarlarını kullanan modüller

Satınalma kutusu, istek listesi, mağaza Seçicisi, sepet ve sepet simgesi modülleri stok aralıklarını ve iletilerini göstermek için stok ayarlarını kullanır.

Aşağıdaki resimde, stok içi ("kullanılabilir") iletiyi gösteren ürün ayrıntıları sayfası (PDP) örneği gösterilmektedir.

![Stokta bir ileti bulunan PDP modülü örneği](./media/pdp-InStock.png)

Aşağıdaki resimde, "stok dışı" iletiyi gösteren PDP örneği gösterilmektedir.

![Stok dışı bir ileti bulunan PDP modülü örneği](./media/pdp-outofstock.png)

Aşağıdaki resimde, stokta ("kullanılabilir") iletiyi gösteren sepet örneği gösterilmektedir.

![Stokta bir ileti bulunan sepet modülü örneği](./media/cart-instock.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Stok arabellekleri ve stok düzeyleri yapılandırma](inventory-buffers-levels.md)

[Sepet modülü](add-cart-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Hesap yönetimi sayfaları ve modülleri](account-management.md)

[Mağaza seçicisi modülü](store-selector.md)

[SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]