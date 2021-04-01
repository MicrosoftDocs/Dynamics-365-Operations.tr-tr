---
title: Stok düzeyi bilgilerini Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu stok düzey bilgisini Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 0822bf4bdbb687e040e2ce04842ef263b8dc0e1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243093"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Stok düzeyi bilgilerini Supply Chain Management'tan Field Service'e eşitleme 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu stok düzey bilgisini Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve temel görevler, eldeki stok düzeylerini Supply Chain Management'tan Field Service'e eşitlemede kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Ürün Stoku (Supply Chain Management'tan Field Service'e)
  
**Veri tümleştirme projesindeki görev**
- Ürün stoku

Aşağıdaki eşitleme görevlerinin, stok düzeylerinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:
- Ambarlar (Supply Chain Management'tan Field Service'e) 
- Stok birimli Field Service ürünleri (Supply Chain Management'tan Sales'e) 

## <a name="entity-set"></a>Varlık kümesi

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Dataverse ambara göre eldeki stok     |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'tan stok seviyesi bilgisi Field Service'a seçilen ürünler için gönderildi. Düzey Stok bilgileri şunları içerir: 
- Eldeki miktarı (geçerli kayıtlı fiziksel olarak ambarda miktar)
- Sipariş miktarı (toplam kaydedilen siparişindeki miktar - satış siparişleri gibi)
- Sipariş edilen toplam miktar (toplam kaydedilen sipariş tutarı - satınalma siparişleri gibi)

Bu bilgiler her ambar için serbest bırakılan ürün başına yakalanan ve stok düzeyini değiştiğinde, değişiklik izlemeyi dayalı eşitlenmiş.

Field Service'teki düzeylerin Supply Chain Management'taki düzeylerle eşleşmesi için, Field Service'te, tümleştirme çözümü, delta için stok günlükleri oluşturur.

Supply Chain Management, stok düzeyleri için üst görevi görür. Bu nedenle Field Service'ten Supply Chain Management'a iş emirleri, aktarmalar ve ayarlamalar için kurulum tümleştirmesi, bu özellik Field Service'te Supply Chain Management'tan stok düzeyleri eşitlemesi ile kullanılıyorsa, önemlidir.

Stok düzeylerinin Supply Chain Management'tan üstlenildiği ürünler ve ambarlar, Gelişmiş Sorgu ve Filtreleme (Power Query) ile denetlenebilir.

> [!NOTE]
> Field Services'te birden fazla ambar (**Harici Korunan = Hayır**) oluşturmak ve bunları Supply Chain Management'ta tek bir ambara eşlemek Gelişmiş sorgu ve filtreleme işlevleriyle mümkündür. Bu, Field Service'in ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Supply Chain Management'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda, Field Service, Supply Chain Management'tan stok düzeyi güncelleştirmeleri almayacaktır. Daha fazla bilgi için bkz. [Field Service'ten Supply Chain Management'a stok ayarlamalarını eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Field Service'teki iş emirlerini Supply Chain Management'taki projeyle bağlantılı satış siparişlerine eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici ürün stoku** varlığı yalnızca arka uç tümleştirmesinde kullanılır. Bu varlık tümleştirmedeki Supply Chain Management'tan stok düzeyi değerlerini alır ve bu değerleri, Ambardaki Stok ürünlerini değiştiren Manuel stok günlüklerine dönüştürür.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="data-integration"></a>Veri tümleştirmesi
Projenin çalışması için, Tümleştirme anahtarının msdynce_externalproductinventories için güncelleştirilmiş olduğundan emin olmanız gerekir.
1.  **Veri tümleştirmesi > Bağlantı kümeleri**'ne gidin.
2.  Kullanılan Bağlantı kümesini seçin.
3.  **Tümleştirme anahtarı** sekmesinde, aşağıdaki anahtarların msdynce_externalproductinventories öğesine eklendiğinden emin olun:
      - msdynce_productnumber (Ürün Numarası)
      - msdynce_warehouseid (Ambar Kodu)
      
### <a name="data-integration-project"></a>Veri tümleştirme projesi
Gelişmiş Sorgu ve Filtreleme ile filtreler uygulayarak yalnızca belirli ürünler ve ambarların Supply Chain Management'tan Field Service'e stok düzeyi bilgileri göndermesini sağlayabilirsiniz.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Ürün stoku (Supply Chain Management'tan Field Service'e): Ürün stoku

[![Veri tümleştirmede şablon eşleme](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]