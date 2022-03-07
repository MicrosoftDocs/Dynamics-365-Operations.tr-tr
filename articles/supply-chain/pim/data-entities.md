---
title: Ürün veri varlıkları
description: Bu konu, ürün verilerini içe aktarmak ve vermek için kullanılabilecek farklı varlıklar hakkında bilgi sağlar.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 2784e552d7984bbea9c74ad800c6305ab2a216e9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567163"
---
# <a name="product-data-entities"></a>Ürün veri varlıkları

[!include [banner](../includes/banner.md)]

Ürün verileri içe ve dışa aktarmak için veri varlıklarını kullanın. Aşağıdaki tabloda, ürün veri varlıklarıyla ilgili ayrıntılar verilmektedir ve her birinin amacı açıklanmıştır.

| Varlık | Uygulama Nesne Ağacı (AOT) adı (türü) | Notlar |
|--------|-------------------------------------------|-------|
| Ürünler V2 | `EcoResProductV2Entity` | Bu varlık, paylaşılan ürünler-farklı ürünler ve Ürün asılları almak ve vermek için kullanılır. Güncelleştirmelere izin verir. Bu, ayarlanan tabanlı SQL işlemlerini desteklemez. Açık Veri Protokolü (OData) için etkinleştirildi. |
| Serbest bırakılan ürünler V2 | `EcoResReleasedProductV2Entity` | Bu varlık, kullanıma sunulan ürünler-farklı ürünler ve Ürün asılları almak ve vermek için kullanılır. Güncelleştirmelere izin verir. Paylaşılan ürünün önceden oluşturulmuş olmasını gerektirir. Yeni yayınlanmış bir ürün alındığında, paylaşılan ürünün bir sürümü oluşur. Ayrıca, serbest bırakılan ürün asıllarını içe ve serbest bırakılmış farklı varyantlar almak ve vermek için kullanılabilecek ayrı birer varlık vardır. Bu varlık, ayarlanan tabanlı SQL işlemlerini veya silme işlemlerini desteklemez. OData için etkin. |
| Serbest bırakılan ürün oluşturma V2 | `EcoResReleasedProductCreationV2Entity` | Bu varlık, paylaşılan ürünleri ve serbest bırakılan ürünleri tek bir adımda almak için kullanılır. Varlığın amacı ürün oluşturma olduğundan, dışarı aktarımları desteklemekle birlikte, bu kullanım önerilmez. Güncelleştirmeleri desteklemiyor. Sınırlı sayıda alan kümesini (ürün oluşturma iletişim kutusunda bulunan alanlar) destekler. Bu, ayarlanan tabanlı SQL işlemlerini desteklemez. OData aracılığıyla gösterilmez. |
| Ürün çeşitleri | `EcoResProductVariantEntity` | Bu varlık paylaşılan ürün çeşitlerini içe aktarmak ve vermek için kullanılır. Güncelleştirmelere izin verir. Boyut değerlerinin önceden oluşturulmasını gerekli kılıyor. Tümleştirme anahtarı ürün yöneticisinin artı ürün boyutlarıdır. Bu varlık, ayarlanan tabanlı SQL işlemlerini desteklemez. OData için etkin. Silme işlemlerini destekler. Yeni ürün boyutları ek olarak genişletilemez. |
| Ürün numarası koduna göre ürün çeşitleri | `EcoResProductNumberIdentifiedProductVariantEntity` | Bu varlık paylaşılan ürün çeşitlerini içe aktarmak ve vermek için kullanılır. Güncelleştirmelere izin verir. Boyut değerlerinin önceden oluşturulmasını gerekli kılıyor. Tümleştirme anahtarı ürün numarasıdır ( **ürün çeşitleri** varlığı için tümleştirme anahtarı üretim yöneticisi artı ürün boyutları). |
| Serbest bırakılan ürün çeşitleri | `EcoResReleasedProductVariantEntity` | Bu varlık kullanıma sunulan ürün çeşitlerini içe aktarmak ve vermek için kullanılır. Güncelleştirmelere izin verir. Paylaşılan ürün çeşitlerinin önceden oluşturulmuş olmasını gerektirir. Yeni yayınlanmış bir ürün değişkeni alındığında, paylaşılan ürünün bir sürümü oluşur. Bu varlık, ayarlanan tabanlı SQL işlemlerini desteklemez. OData için etkin. Silme işlemlerini desteklemekle birlikte, geçerli platformdaki bir hata nedeniyle o anki kullanım veri bozulmasına neden olur. Bu varlık Yeni ürün boyutları ek olarak genişletilemez. |
| Ürün numarası koduna göre serbest bırakılan ürün çeşitleri | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | Bu varlık, **Kullanıma sunulan ürün değişkenleri** varlığına benzer, tümleştirme anahtarı ürün numarasıdır ( ürün çeşitleri varlığı için tümleştirme anahtarı üretim yöneticisi artı ürün boyutları). Yeni ürün boyutları ek olarak genişletilemez. |
| Satış yapılabilir serbest bırakılan ürünler | `EcoResSellableReleasedProductEntity` | Bu varlık yalnızca satış yapılabilir ürünleri dışa aktarmak için kullanılır. Satış yapılabilir ürünler, bir satış siparişinde kullanılmak üzere gerekli bilgilere sahip olan ürünlerdir. Aynı kurallar, bir ürün **Serbest bırakılan ürünler** sayfasında **Doğrula** işleviyle doğrulanıyorsa da geçerlidir. |
| Serbest bırakılan farklı ürünler V2 | `EcoResDistinctProductV2Entity` | Bu varlık farklı ürünleri dışa aktarmak için kullanılır. Bu ayrı ürünler ürün, alt tür ürünleri ve tüm ürün çeşitlerini ifade eder. |
| Serbest bırakılan ana ürünler V2 | `EcoResProductMasterV2Entity` | Bu varlık ana ürünleri içe aktarmak ve vermek için kullanılır. Veri yönetimi için etkin değil. |
| Madde - barkod | `EcoResProductBarcodeEntityV3` | Bu varlık ürünleri ve barkodları dışa aktarmak için kullanılır. Bu varlık, değişiklik izleme, güncelleştirme veya silme işlemlerine izin vermiyor. Barkodlar üzerinde değişiklik izleme, güncelleştirme veya silme işlemlerini kullanmak için **Madde - barkod ilişkilendirmesi** varlığını kullanın. |
| Madde - barkod ilişkilendirmesi | `EcoResProductBarcodeAssociationEntity` | Bu varlık ürünleri ve barkodları dışa aktarmak için kullanılır. Değişiklik izleme, güncelleştirme ve silme işlemine izin verir. Varlığı kullanmak için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *Madde - barkod geliştirmeleri* etkinleştirilmiş olmalıdır. Barkod ile ürün arasındaki ilişkiyi oluşturan varlık anahtarı `AssociationID` anahtarıdır. Bu anahtara yönelik destek eklemek için özelliği açtığınızda `InventitemBarcodeAssociation` tablosu, var olan madde barkodu için doldurulur. Tablo, toplu iş kullanılarak doldurulur ve barkod tablonuzda çok sayıda kayıt varsa toplu işlemi çalıştırmak uzun zaman alabilir. Bu nedenle, özelliği etkinleştirmeyi planlamanız ve toplu işi iş programınıza uygun bir zamanda çalıştırmanız önerilir. |
| Ürün yaşam döngüsü durumları | `EcoResProductLifecycleSateEntity` | Bu varlık, bir ürüne atanabilecek farklı ürün yaşam döngüsü durumlarını içe aktarmak ve dışa aktarmak için kullanılır. |

> [!NOTE]
> Ürünleri sisteme aktarmak için **yayınlanan ürünler v2** veri varlığını yalnızca paylaşılan ürün zaten oluşturulmuşsa kullanabilirsiniz. Aksi durumda, ürünleri sisteme içe aktarmak için **ürün oluşturma** veri varlığını kullanmanız gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]