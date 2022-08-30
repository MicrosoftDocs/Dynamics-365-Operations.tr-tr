---
title: Supply Chain Management için standart kayıtlı görünümler
description: Bu makalede, sunulan standart kayıtlı görünümler ve bunların nasıl etkinleştirileceği açıklanmaktadır.
author: kamaybac
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f94fffb9aa2c208b8c2c0005a2892853eda66a01
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334850"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Supply Chain Management için standart kayıtlı görünümler

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, gerektiği şekilde etkinleştirebileceğiniz ve kullanabileceğiniz kaydedilmiş görünümler içerir. Bu standart kayıtlı görünümlerin bazıları belirli bir rol veya görev için en iyi duruma getirilmiş ve adlandırılmıştır (ör. "Kalite kontrol" veya "Alma"). Diğerleri, Microsoft kullanım istatistiklerine göre müşteriler tarafından en çok kullanılan alanları ve ayarları içerecek şekilde en iyi duruma getirilmiştir. Bu kayıtlı görünümlere genellikle *basitleştirilmiş* görünümler adı verilir. Bu makalede, sunulan standart kayıtlı görünümler ve bunların nasıl etkinleştirileceği ve özelleştirileceği açıklanmaktadır.

Standart kayıtlı görünümler dahil olmak üzere kayıtlı görünümlerle nasıl çalışılacağı hakkında tüm ayrıntılar için bkz. [Kayıtlı görünümler](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Standart kayıtlı görünümleri özelleştirme

Kendi kaydedilmiş görünümlerinizi özelleştirebileceğiniz gibi, standart kayıtlı görünümleri de özelleştirebilirsiniz. Ancak standart kayıtlı görünümü özelleştirdiğinizde, özel sürümünüzü yeni bir adla kaydetmenizi önemle tavsiye ederiz. Aksi takdirde, Supply Chain Management'ı güncelleştirdiğinizde özelleştirmelerinizin üzerine yazılabilir.

Kayıtlı görünümleri özelleştirme ve yeniden adlandırma hakkında daha fazla bilgi için bkz. [Kayıtlı görünümler](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Kullanılabilir kayıtlı görünümler ve bunları etkinleştirme

Standart kayıtlı görünümleri kullanıp kullanmamanızdan bağımsız olarak kayıtlı görünümleri kullanmak için [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *Kayıtlı görünümler* özelliğini açmanız gerekir (10.0.21 sürümü itibarıyla bu özellik varsayılan olarak etkindir).

Bu makalenin kalan bölümlerinde, ilgili her modül için şu anda kullanılabilir olan standart kayıtlı görünümleri açıklayan tablolar bulunur. Her tabloda, kayıtlı görünümün adı, görünümü bulabileceğiniz sayfa ve açıklaması gösterilir. Ayrıca her tabloda, kayıtlı görünümü içeren özelliğin adı da gösterilir. Sisteminizde standart bir kayıtlı görünümü görmek için [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) belirtilen özelliği açmanız gerekir. Sürüm 10.0.25 itibarıyla, listelenen tüm görünümler varsayılan olarak açıktır.

## <a name="saved-views-for-the-inventory-management-module"></a>Stok yönetim modülü için kayıtlı görünümler

Aşağıdaki tabloda, Stok yönetimi modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Eldekilerin listesi | Finansal öğeler | Bu basitleştirilmiş görünüm, eldeki stoku yönetirken mali bilgilere odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Eldekilerin listesi | Kalite kontrol | Bu basitleştirilmiş görünüm, eldeki stoku yönetirken kalite kontrolüne odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Eldekilerin listesi | Teslim Alma | Bu basitleştirilmiş görünüm, eldeki stoku yönetirken teslim alma işlemlerine odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Eldekilerin listesi | Sevkiyat | Bu basitleştirilmiş görünüm, eldeki stoku yönetirken sevkiyat işlemlerine odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Hareketler | Basitleştirilmiş | Bu basitleştirilmiş görünüm, mali bilgiler ve daha az kullanılan diğer alanlarla vakit kaybetmeden stok durumunu incelemenizi sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Transfer emirleri | Sevkiyat | Bu basitleştirilmiş görünüm, transfer emirlerini yönetirken sevkiyat işlemlerine odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Transfer emirleri | Teslim Alma | Bu basitleştirilmiş görünüm, transfer emirlerini yönetirken alma işlemlerine odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Transfer emirleri | Kalite kontrol | Bu basitleştirilmiş görünüm, transfer emirlerini yönetirken kalite kontrolüne odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Transfer emirleri | Finansal değerler | Bu basitleştirilmiş görünüm, transfer emirlerini yönetirken mali bilgilere odaklanmanızı sağlar. | Stok yönetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |

## <a name="saved-views-for-the-master-planning-module"></a>Master planlama modülü için kayıtlı görünümler

Aşağıdaki tabloda, Master planlama modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Planlı siparişler: Planlı sipariş ayrıntıları sayfası | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca tek bir planlı siparişin ayrıntılarıyla çalışmak için en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Planlı siparişler için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Planlı siparişler: Planlı siparişler listesi sayfası | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca planlı siparişler listesiyle çalışmak için en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Planlı siparişler için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Tedarik ve kaynak atama için kayıtlı görünümler

Aşağıdaki tabloda, Tedarik ve kaynak atama modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Satın alma siparişi ayrıntıları | Sipariş oluşturma | Bu basitleştirilmiş görünüm, yeni satınalma siparişleri oluşturmak için en iyi duruma getirilmiştir. | Satın alma siparişleri için kayıtlı görünümler<br><br>10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Satın alma siparişi ayrıntıları | Stok Yönetimi | Bu basitleştirilmiş görünüm; alınan stokun takip edilmesi, stoku teslim alma, net gereksinimleri denetleme ve sipariş miktarlarını düzeltme gibi stokla ilgili etkinlikleri gerçekleştirmek için en iyi duruma getirilmiştir. | Satın alma siparişleri için kayıtlı görünümler<br><br>10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Satın alma siparişi ayrıntıları | Mali yönetim | Bu basitleştirilmiş görünüm, faturalamanın yanı sıra fiyatları, toplamları ve ücretleri denetleme gibi mali işlemlerle ilgili etkinlikleri gerçekleştirmek için en iyi duruma getirilmiştir. | Satın alma siparişleri için kayıtlı görünümler<br><br>10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Satın alma siparişi ayrıntıları | Sipariş onayı | Bu basitleştirilmiş görünüm, satınalma siparişlerini onaylamak için en iyi duruma getirilmiştir. | Satın alma siparişleri için kayıtlı görünümler<br><br>10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |

## <a name="saved-views-for-the-product-information-management-module"></a>Ürün bilgisi yönetim modülü için kayıtlı görünümler

Aşağıdaki tabloda, Ürün bilgisi yönetimi modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Serbest bırakılan ürün listesi | Ürün oluşturma | Ürün oluşturulurken gösterilen, yalnızca en sık kullanılan alanları içeren basitleştirilmiş bir sayfa görünümü. | Serbest bırakılan ürünler için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Serbest bırakılan ürün ayrıntıları | Ürün oluşturma | Ürün oluşturulurken gösterilen, yalnızca en sık kullanılan alanları içeren basitleştirilmiş bir sayfa görünümü. | Serbest bırakılan ürünler için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Serbest bırakılan ürün ayrıntıları | Lojistik bilgileri yönetimi | Ürünlere yönelik lojistik bilgileri yönetilirken gösterilen, yalnızca en sık kullanılan alanları içeren basitleştirilmiş bir sayfa görünümü. | Serbest bırakılan ürünler için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Serbest bırakılan ürün ayrıntıları | Satın alma bilgileri yönetimi | Ürünlere yönelik satın alma bilgileri yönetilirken gösterilen, yalnızca en sık kullanılan alanları içeren basitleştirilmiş bir sayfa görünümü. | Serbest bırakılan ürünler için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Serbest bırakılan ürün ayrıntıları | Satış bilgileri yönetimi | Ürünlere yönelik satışla ilgili bilgiler yönetilirken gösterilen, yalnızca en sık kullanılan alanları içeren basitleştirilmiş bir sayfa görünümü. | Serbest bırakılan ürünler için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |

## <a name="saved-views-for-the-production-control-module"></a>Üretim denetimi modülü için kayıtlı görünümler

Aşağıdaki tabloda, Üretim denetimi modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Üretim emri ürün reçetesi sayfası | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Üretim denetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Üretim emri ayrıntıları sayfası | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Üretim denetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Üretim emri malzeme çekme listesi sayfası | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Üretim denetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Üretim emirleri listesi sayfası | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Üretim denetimi için kayıtlı görünümler<br><br>(10.0.21 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Satış ve pazarlama modülü için kayıtlı görünümler

Aşağıdaki tabloda, Satış ve pazarlama modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Sevk irsaliyesi günlüğü | Günlük inceleme | Bu basitleştirilmiş görünüm, yalnızca sevk irsaliyesi günlüklerini incelemek için en sık kullanılan alanları içerir. | Satış ve pazarlama için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Satış siparişi | Sipariş oluşturma | Bu basitleştirilmiş görünüm, yalnızca satış siparişleri oluşturmak için en sık kullanılan alanları içerir. | Satış ve pazarlama için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Satış siparişi | Sipariş incelemesi | Bu basitleştirilmiş görünüm, yalnızca satış siparişlerini incelemek için en sık kullanılan alanları içerir. | Satış ve pazarlama için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Satış teklifi | Teklif oluşturma | Bu basitleştirilmiş görünüm, yalnızca satış teklifleri oluşturmak için en sık kullanılan alanları içerir. | Satış ve pazarlama için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |

## <a name="saved-views-for-the-warehouse-management-module"></a>Ambar yönetim modülü için kayıtlı görünümler

Aşağıdaki tabloda, Ambar yönetimi modülü için kullanılabilir kayıtlı görünümler açıklanmaktadır.

| Sayfa | Görünüm adı | Görünüm açıklaması | Özellik adı |
|---|---|---|---|
| Tüm yükler | Gelen işleme | Bu basitleştirilmiş görünüm, yalnızca gelen yükleri işlemek için en sık kullanılan alanları içerir. | Yük işleme için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Tüm yükler | Giden sevkiyat işleme | Bu basitleştirilmiş görünüm, yalnızca giden yükleri işlemek için en sık kullanılan alanları içerir. | Yük işleme için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Tüm sevkiyatlar | Gelen sevkiyat işleme | Bu basitleştirilmiş görünüm, yalnızca gelen sevkiyatları işlemek için en sık kullanılan alanları içerir. | Sevkiyat işleme için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Tüm sevkiyatlar | Giden sevkiyat işleme | Bu basitleştirilmiş görünüm, yalnızca giden sevkiyatları işlemek için en sık kullanılan alanları içerir. | Sevkiyat işleme için kayıtlı görünümler<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Tüm dalgalar | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Dalga işleme için kayıtlı görünüm<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| Yük planlama çalışma ekranı | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | Yük planlama çalışma ekranı için kayıtlı görünüm<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |
| İş ayrıntıları | Basitleştirilmiş | Bu basitleştirilmiş görünüm, yalnızca en sık kullanılan alanları içerir. Bu şekilde, daha hızlı bir genel bakış ve kolay bir iş süreci sağlar. | İş ayrıntıları sayfası için kayıtlı görünüm<br><br>(10.0.25 sürümü itibarıyla varsayılan olarak açık. Sürüm 10.0.29 itibarıyla zorunlu.) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]