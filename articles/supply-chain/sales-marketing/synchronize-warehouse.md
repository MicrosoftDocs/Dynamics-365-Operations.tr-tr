---
title: Ambarları Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu ambarları Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: Henrikan
ms.date: 03/13/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: f38d2dfdba1f2afa1005bd740cba27afe9dcb0ec
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062148"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Ambarları Supply Chain Management'tan Field Service'e eşitleme

[!include[banner](../includes/banner.md)]



Bu konu ambarları Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve temel görevler, ambarların Supply Chain Management'tan Field Service'e eşitlemesini çalıştırmak için kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Ambarlar (Supply Chain Management'tan Field Service'e)

**Veri tümleştirme projesindeki görev**
- Ambar

## <a name="table-set"></a>Tablo kümesi
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Ambarlar                             |

## <a name="table-flow"></a>Tablo akışı
Supply Chain Management'ta oluşturulan ve korunan ambarlar, Field Service'e bir Microsoft Dataverse Veri tümleştirme projesi aracılığıyla eşitlenebilir. Field Service'a eşitlemek istediğiniz ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler. Supply Chain Management'tan eşitlenen ambarlar, **Harici olarak korunur** sütununun **Evet** olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service'te oluşturulur.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
Field Service ile Supply Chain Management arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir. Çözümde, **Harici Olarak Korunur** sütunu, **Ambar (msdyn_warehouses)** tablosuna eklendi. Bu sütun, ambarın Supply Chain Management'tan mı yönetildiğini yoksa yalnızca Field Service'te mi var olduğunu belirlemeye yardımcı olur. Bu sütunun ayarları arasında aşağıdakiler yer alır:
- **Evet** – Ambar, Supply Chain Management kaynaklıdır ve Sales'te düzenlenemez.
- **Hayır** – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.

**Harici Olarak Korunur** sütunu, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur. Yalnızca **Harici Korunan ambarlar**, **Evet** olarak ayarlanır, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir. 

> [!NOTE]
> Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür. Bu, Field Service'in ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Supply Chain Management'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda, Field Service, Supply Chain Management'tan stok düzeyi güncelleştirmeleri almayacaktır. Daha fazla bilgi için bkz. [Field Service'tan Finans ve Operasyon'a stok ayarlamalarını eşitlemede](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Finans ve Operasyon içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

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

[![Veri tümleştirmede şablon eşleme.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]