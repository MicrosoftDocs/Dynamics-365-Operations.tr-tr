---
title: Finance and Operations'tan Field Service'a ambarları eşitleme
description: Bu konu ambarları Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "340327"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Ambarları Finance and Operations'dan Field Service'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu ambarları Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve görevler, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine ambarların eşitlenmesinde kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Ambarlar (Finance and Operations'tan Field Service'a)

**Veri tümleştirme projesindeki görev**
- Ambar

## <a name="entity-set"></a>Varlık kümesi
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Ambarlar                             |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'taki oluşturulan ve korunan ambarlar Field Service'a br Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir. Field Service'a eşitlemek istediğiniz ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler. Finance and Operations'tan eşitlenen ambarlar, **Harici olarak korunuyor** alanının **Evet** olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service için oluşturulur.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
Field Service ile Finance and Operations arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir. Çözümde, **Harici Korunuyor** alanı, **Ambar (msdyn_warehouses)** varlığına eklendi. Bu alan, ambarın Finance and Operations'tan mı yönetildiğini yoksa yalnızca Field Service'ta mı mevcut olduğunu tanımlamaya yardımcı olur. Bu alan için ayarlara şunlar dahildir:
- **Evet** – Ambar, Finance and Operations'tan gelir ve Sales'ta düzenlenebilir olmaz.
- **Hayır** – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.

**Harici Korunuyor** alanı, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur. Yalnızca **Harici Korunan ambarlar**, **Evet** olarak ayarlanır, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir. 

> [!NOTE]
> Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür. Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda, Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır. Daha fazla bilgi için bkz. [Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu
### <a name="data-integration-project"></a>Veri Tümleştirme projesi
Ambarların eşitlenmesinden önce, Gelişmiş sorgu ve filtrelemenin proje üzerinde yalnızca Finance and Operations'tan Field Service'a getirdiğiniz ambarları dahil ettiğinden emin olun. İş emirleri, ayarlamalar ve aktarmalarda uygulayabilmek için ambara Field Service'ta ihtiyacınız olacağını unutmayın.  

**msdyn_warehouses** için **Tümleştirme anahtarı** bulunduğundan emin olmak için:
1. Veri Tümleştirme'ye gidin.
2. **Bağlantı Kümesi** sekmesini seçin.
3. İş emri eşitlemede kullanılacak bağlantı kümesini seçin.
4. **Tümleştirme anahtarı** sekmesini seçin.
5. msdyn_warehouses öğesini bulun ve **msdyn_name (adı)** anahtarının eklendiğini doğrulayın. Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin ve sonra sayfanın üst kısmındaki **Kaydet**'e tıklayın.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görsel, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Ambarlar (Finance and Operations'tan Field Service'a): Ambar

[![Veri tümleştirmede şablon eşleme](./media/Warehouse1.png)](./media/Warehouse1.png)
