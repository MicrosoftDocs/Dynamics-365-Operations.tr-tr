---
title: "Stok düzeyi bilgisini Finance and Operations'tan Field Service'a eşitlemek"
description: "Bu konu, stok düzeyi bilgisini Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Stok düzeyi bilgisini Finance and Operations'tan Field Service'a eşitlemek 

[!include[banner](../includes/banner.md)]

Bu konu, stok düzeyi bilgisini Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon, stok eldeki düzeyleri eşitlemelerini Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

**Veri tümleştirmesindeki şablonun adı:**
- Ürün Stoku (Finance and Operations'tan Field Service'a)
  
**Veri tümleştirme projesindeki görevlerin adları:**
- Ürün stoku

Aşağıdaki eşitleme görevlerinin, stok düzeylerinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:
- Ambarlar (Finance and Operations'tan Field Service'a) 
- Stok birimli Field Service Ürünleri (Finance and Operations'tan Sales'a) 

## <a name="entity-set"></a>Varlık kümesi

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS ambara göre eldeki stok     |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'tan stok seviyesi bilgisi Field Service'a seçilen ürünler için gönderilir. Düzey Stok bilgileri şunları içerir: 
- Eldeki miktarı (geçerli kayıtlı fiziksel olarak ambarda miktar)
- Sipariş miktarı (toplam kaydedilen siparişindeki miktar - başka bir deyişle Satış siparişleri)
- Sipariş edilen toplam miktar (toplam kaydedilen sipariş tutarı - başka bir deyişle satınalma siparişleri)

Bu bilgiler her ambar için serbest bırakılan ürün başına yakalanan ve stok düzeyini değiştiğinde, değişiklik izlemeyi dayalı eşitlenmiş.

Field Service servis düzeyleri ve Finance and Operations işlemleri eşleştirmek için düzeyin almak için delta Stok günlüklerini tümleştirme çözümü oluşturun.

Finance and Operations, stok düzeyleri için üst görevi görür. Bu nedenle Field Service'tan Finance and Operations'a iş emirleri, aktarmalar ve ayarlamalar için kurulum tümleştirmesi, bu özellik Field Service'ta Finance and Operations'tan stok düzeyleri eşitlemesi ile kullanılıyorsa, önemlidir.

Stok düzeylerinin Finance and Operations'tan üstlenildiği ürünler ve ambarlar, Gelişmiş Sorgu ve Filtreleme (Power Query) ile kontrol edilebilir.

Not: Field Service'ta birden fazla ambar (Harici Korunan = Hayır) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür. Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır. Bu durumda Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır. Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede ve Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek istiyorsanız ek bilgiye bakın.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
Harici ürün bilgisi yalnızca arka uç içinde tümleştirme için kullanılan yeni bir varlık bir varlıktır. Finance and Operations ve stok düzeyi değerlerinin birleştirilmesinde alır ve daha sonra bu ambarı stok ürünler sonra değişen Manuel Stok günlüklerini değerlere dönüştürür. 

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="in-the-data-integration-project"></a>Veri Tümleştirme projesinde
Gelişmiş Sorgu ve Filtreleme ile filtreler uygulayın, böylece yalnızca istenilen ürünler ve ambarlar stok düzeyi bilgisine Finance and Operations'tan Field Service'a gönderilir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Ürün Stoku (Finance and Operations'tan Field Service'a): Ürün stoku

[![Veri tümleştirmede şablon eşleme](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

