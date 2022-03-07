---
title: Stok ayarlarını uygula
description: Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4ba3e67cf9c72b9a9606528c02f9e57d19a74c1f
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647596"
---
# <a name="apply-inventory-settings"></a>Stok ayarlarını uygula

[!include [banner](includes/banner.md)]

Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .

Stok ayarları alışveriş için ürün sepetine eklenmeden önce stokun denetlenip işaretlenmeyeceğini belirtir. Ayrıca, "stokta" ve "yalnızca birkaç soldaki" gibi, stokla ilgili Merchandising iletileri de tanımlarlar. Bu ayarlar, ürünün stokta bulunduğu durumda satın alınmamasını sağlar.

Dynamics 365 Commerce ürünler için eldeki kullanılabilir kullanılabilirlik tahminleri sağlar. Tahmini eldeki stok kullanılabilirliğinin nasıl hesaplandığı hakkında bilgi için bkz [perakende kanalları için envanter kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md).

Commerce Site Builder 'da stok eşikleri ve aralıkları bir ürün ya da kategori için tanımlanabilir. Stokta, düşük stokta veya stok dışı olduğu gibi sınıflandırılabileceği belirlenir. Ayrıntılar için bkz [Envanter tamponları ve envanter düzeylerini yapılandırma](inventory-buffers-levels.md).

> [!NOTE]
> Stok eşikleri ve aralıkları için destek Dynamics 365 Commerce 10.0.12 sürümünde bulunabilir.

## <a name="inventory-settings"></a>Envanter ayarları

Commerce'da stok ayarları, site oluşturucuda **Site Ayarlar \> Uzantılar \> Envanter yönetimi** tanımlanır . Altı stok ayarı vardır; bunlardan biri eskidir (kullanım dışı):

- **Uygulama üzerinde stok denetimini etkinleştir** – Bu ayar, ürün envanteri denetimini açar. Mağaza modüllerinde satın alma kutusu, alışveriş sepeti ve çekme için ürün stoğu kontrol edilir ve yalnızca stok varsa alışveriş sepetine bir ürün eklenmesine izin verilir.
- **Stok düzeyi temeli** - Bu ayar, stok düzeylerinin nasıl hesaplandığını tanımlar. Kullanılabilir değerler **Toplam kullanılabilir**, **fiziksel kullanılabilir** ve **stok dışı eşikler** dir. Commerce'da stok eşikleri ve aralıkları her ürün ya da kategori için tanımlanabilir. Stok API'Leri **Toplam kullanılabilir** özelliğin ve **fiziksel kullanılabilir** özelliğin ürün stok bilgilerini döndürür. Perakende, **kullanılabilen toplam** veya **fiziksel kullanılabilir** değerin stok sayısını ve stokta bulunmayan ve stok dışı durumları için bunlara karşılık gelen aralıkları belirlemek için kullanılabilir olup olmadığına karar verir.

    **Stok düzeyi ayar temel alınarak** ayarının **stokta bulunmayan eşik değeri** eski (eski), kullanımdan kalktı değeridir. Seçildiği zaman, stok sayımı **Toplam kullanılabilir** değerin sonuçlarından belirlenir , ancak eşik, daha sonra açıklanan **stok dışı eşiği** sayısal ayarı tarafından tanımlanır. Bu eşik ayarı bir e-ticaret sitesi içindeki tüm ürünlere uygulanır. Stok eşik numarasının altındaysa, bir ürün Stokta yer alır. Aksi takdirde stokta olduğu düşünülür. **Stok dışı eşik** değerinin yetenekleri sınırlıdır ve bunu sürüm 10.0.12 ve sonraki sürümlerde kullanmanızı önermeyiz.

- **Çoklu ambarlar için stok düzeyi** – Bu ayar, stok düzeyinin varsayılan ambar veya çoklu ambarlara göre hesaplanmasını sağlar. **Tekli ambar seçeneğine göre** seçeneği, stok düzeylerini varsayılan ambara dayalı olarak hesaplar. Alternatif olarak bir e-ticaret sitesi, karşılamayı kolaylaştırmak için birden çok ambara işaret edebilir. Bu durumda, **Teslimat ve Malzeme Çekme ambarları için toplamaya göre** seçeneği, stok kullanılabilirliğini belirtmek için kullanılır. Örneğin, bir müşteri bir öğe satın aldığında ve teslimat modu olarak "sevkiyat" seçeneğini seçtiğinde, söz konusu öğe, karşılama grubundaki kullanılabilir stok bulunan herhangi bir ambardan sevk edilebilir. Ürün ayrıntıları sayfası (PDP), karşılama grubunda herhangi bir kullanılabilir sevkiyat ambarında stok varsa sevkiyat için "Stokta" iletisini gösterecektir. 

    > [!IMPORTANT] 
    > **Birden çok ambar için stok düzeyi**, Commerce sürüm 10.0.19'dan itibaren mevcuttur. Commerce'ün eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir. Talimatlar için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Ürün listesi sayfaları için stok ayarları** – Bu ayar, ürün toplama ve arama sonuçları modülleri tarafından işlenen ürün listelerinde stok dışı ürünlerin nasıl gösterileceğini tanımlar. Kullanılabilir değerler: **Diğer ürünlerle aynı sırada görüntülenir**, **Listeden stokta bulunan ürünleri gizler** ve **Listenin sonunda stok dışı ürünleri görüntüler**. Bu ayarı kullanmak için, önce Commerce Headquarters'da bazı önkoşul ayarlarını konfigüre etmelisiniz. Daha fazla bilgi için bkz. [Arama sonuçları modülü için stok farkındalığını etkinleştirme](search-result-module.md#enable-inventory-awareness-for-the-search-results-module).

    > [!IMPORTANT] 
    > **Ürün listesi sayfaları için envanter ayarları**, Commerce sürüm 10.0.20'dan itibaren mevcuttur. Commerce'ün eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir. Talimatlar için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Stok aralıkları** – Bu ayar, site modüllerinde iletinin gösterildiği stok aralıklarını tanımlar. Yalnızca, **Toplam kullanılabilir** değer veya **stok düzeyi ayar temel alınarak** ayarı için **fiziksel kullanılabilir** değer seçildiğinde uygulanabilir. Kullanılabilir değerler **tümü**, **düşük ve stok dışı** ve **Stok dışında**.

    - **Tümü** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) stokta değil ("stok dışı" iletisi) görüntülenir.
    - **Düşük ve stok dışı** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) görüntülenir.
    - **Stokta bulunmayan** seçildiğinde , yalnızca "stok dışı" iletisi gösterilir.

- **Stok dışı eşiği** – Bu eski sayısal ayar , yalnızca **stok düzeyi ayar temel alınarak** ayarı **stok dışı eşik** değeri seçildiğinde etkili olur.

> [!IMPORTANT] 
> Bu ayarlar Dynamics 365 Commerce 10.0.12 sürümünde bulunmaktadır. Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir. AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Stok ayarlarını kullanan modüller

Satınalma kutusu, istek listesi, mağaza Seçicisi, sepet ve sepet simgesi modülleri stok aralıklarını ve iletilerini göstermek için stok ayarlarını kullanır.

Aşağıdaki resimde yer alan örnekte, bir PDP stokta ("Kullanılabilir") iletisini göstermektedir.

![Stokta bir ileti bulunan PDP modülü örneği.](./media/pdp-InStock.png)

Aşağıdaki resimde yer alan örnekte, bir PDP "Stokta yok" iletisini göstermektedir.

![Stok dışı bir ileti bulunan PDP modülü örneği.](./media/pdp-outofstock.png)

Aşağıdaki resimde yer alan örnekte, bir sepet stokta ("Kullanılabilir") iletisini göstermektedir.

![Stokta bir ileti bulunan sepet modülü örneği.](./media/cart-instock.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Stok arabellekleri ve stok düzeyleri yapılandırma](inventory-buffers-levels.md)

[Sepet modülü](add-cart-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Hesap yönetimi sayfaları ve modülleri](account-management.md)

[Mağaza seçicisi modülü](store-selector.md)

[SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
