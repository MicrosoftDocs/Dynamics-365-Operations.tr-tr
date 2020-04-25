---
title: Ambarları Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu ambarları Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6617b258a85a8f45b89a38f86919b44edc2100da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215896"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Ambarları Supply Chain Management'tan Field Service'e eşitleme

[!include[banner](../includes/banner.md)]

Bu konu ambarları Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve temel görevler, ambarların Supply Chain Management'tan Field Service'e eşitlemesini çalıştırmak için kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Ambarlar (Supply Chain Management'tan Field Service'e)

**Veri tümleştirme projesindeki görev**
- Ambar

## <a name="entity-set"></a>Varlık kümesi
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Ambarlar                             |

## <a name="entity-flow"></a>Varlık akışı
Supply Chain Management'ta oluşturulan ve korunan ambarlar Field Service'e bir Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla eşitlenebilir. Field Service'a eşitlemek istediğiniz ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler. Supply Chain Management'tan eşitlenen ambarlar, **Harici olarak korunuyor** alanının **Evet** olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service'te oluşturulur.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
Field Service ile Supply Chain Management arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir. Çözümde, **Harici Korunuyor** alanı, **Ambar (msdyn_warehouses)** varlığına eklendi. Bu alan, ambarın Supply Chain Management'tan mı yönetildiğini yoksa yalnızca Field Service'te mi varolduğunu belirlemeye yardımcı olur. Bu alan için ayarlara şunlar dahildir:
- **Evet** – Ambar, Supply Chain Management kaynaklıdır ve Sales'te düzenlenemez.
- **Hayır** – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.

**Harici Korunuyor** alanı, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur. Yalnızca **Harici Korunan ambarlar**, **Evet** olarak ayarlanır, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir. 

> [!NOTE]
> Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür. Bu, Field Service'in ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Supply Chain Management'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda, Field Service, Supply Chain Management'tan stok düzeyi güncelleştirmeleri almayacaktır. Daha fazla bilgi için bkz. [Field Service'tan Finance and Operations'a stok ayarlamalarını eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Field Service'taki iş emirlerini Finance and Operations'taki projeye bağlantısı olan satış siparişlerine eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu
### <a name="data-integration-project"></a>Veri Tümleştirme projesi
Ambarların eşitlenmesinden önce, Gelişmiş sorgu ve filtrelemenin proje üzerinde yalnızca Supply Chain Management'tan Field Service'e getirdiğiniz ambarları dahil ettiğinden emin olun. İş emirleri, ayarlamalar ve aktarmalarda uygulayabilmek için ambara Field Service'ta ihtiyacınız olacağını unutmayın.  

**msdyn_warehouses** için **Tümleştirme anahtarı** bulunduğundan emin olmak için:
1. Veri Tümleştirme'ye gidin.
2. **Bağlantı Kümesi** sekmesini seçin.
3. İş emri eşitlemede kullanılacak bağlantı kümesini seçin.
4. **Tümleştirme anahtarı** sekmesini seçin.
5. msdyn_warehouses öğesini bulun ve **msdyn_name (adı)** anahtarının eklendiğini doğrulayın. Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin ve sonra sayfanın üst kısmındaki **Kaydet**'e tıklayın.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görsel, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Ambarlar (Supply Chain Management'tan Field Service'e): Ambar

[![Veri tümleştirmede şablon eşleme](./media/Warehouse1.png)](./media/Warehouse1.png)
