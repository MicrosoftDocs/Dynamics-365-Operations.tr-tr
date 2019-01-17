---
title: "Finance and Operations'tan Field Service'a ambarları eşitleme"
description: "Bu konu, ambarları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevlerini ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Finance and Operations'tan Field Service'a ambarları eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, ambarları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevlerini ve şablonları açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve görevleri, ambarları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemeyi açıklar.

**Veri tümleştirmesindeki şablonun adı:**
- Ambarlar (Finance and Operations'tan Field Service'a)

**Veri tümleştirme projesindeki görevlerin adları:**
- Ambar

## <a name="entity-set"></a>Varlık kümesi
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Ambarlar                             |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'taki oluşturulan ve korunan ambarlar Field Service'a br Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir. Field Service'a eşitlenen istenen ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler. Finance and Operations'tan eşitlenen ambarlar, Harici olarak korunuyor alanının Evet olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service için oluşturulur.
Field Service CRM çözümü Field Service ile Finance and Operations arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir. Çözüm aşağıdaki değişiklikleri içerir.
**Harici Korunuyor** alanı, **Ambar (msdyn_warehouses)** varlığına eklendi. Bu alan, Ambarın Operations'tan mı yönetildiğini yoksa yalnızca Field Service'ta mı mevcut olduğunu tanımlamaya yardımcı olur.
- Evet – Ambar, Finance and Operations'tan gelir ve Sales'ta düzenlenebilir olmaz.
- Hayır – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.

**Harici Korunuyor** alanı, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur. Yalnızca **Harici Korunan** ambarlar = Evet, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir. 

Not: Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür. Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır. Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede ve Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek istiyorsanız ek bilgiye bakın.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu
### <a name="in-the-data-integration-project"></a>Veri Tümleştirme projesinde
Ambarların eşitlenmesinden önce, Gelişmiş sorgu ve filtrelemenin proje üzerinde yalnızca Finance and Operations'tan Field Service'a getirdiğiniz ambarları dahil ettiğinden emin olun. İş emirleri, ayarlamalar ve aktarmalarda uygulayabilmek için ambara Field Service'ta ihtiyacınız olacağını unutmayın.  

**msdyn_warehouses** için **Tümleştirme anahtarı** bulunduğundan emin olun
1. Veri Tümleştirme'ye gidin
2. **Bağlantı Kümesi** sekmesini seçin
3. İş emri eşitlemede kullanılacak Bağlantı kümesini seçin
4. **Tümleştirme anahtarı** sekmesini seçin
5. msdyn_warehouses öğesini bulun ve **msdyn_name (adı)** anahtarının eklendiğini kontrol edin. Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin sayfanın üst kısmındaki **Kaydet**'e tıklayın

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Ambarlar (Finance and Operations'tan Field Service'a): Ambar

[![Veri tümleştirmede şablon eşleme](./media/Warehouse1.png)](./media/Warehouse1.png)

