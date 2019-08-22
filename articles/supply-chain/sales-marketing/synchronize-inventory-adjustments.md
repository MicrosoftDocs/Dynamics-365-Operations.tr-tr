---
title: Stok hareketlerini ve ayarlamaları Field Service'tan Finance and Operations'a eşitlemek
description: Bu konu stok düzeltmelerini ve aktarmalarını Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835730"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Stok ayarlamalarını Field Service'tan Finance and Operations'a eşitlemek

[!include[banner](../includes/banner.md)]

Bu konu stok düzeltmelerini ve aktarmalarını Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve altındaki görevler, stok düzeltmelerini ve aktarmalarını Microsoft Dynamics 365 for Field Service üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılır.

**Veri Tümleştirmesindeki Şablonlar**
- Stok Ayarlama (Field Service'ten Fin and Ops'a)
- Stok Aktarmaları (Field Service'ten Fin and Ops'a)

**Veri tümleştirme projelerindeki görevler**
- Stok Düzeltmeleri
- Stok Transferleri

## <a name="entity-set"></a>Varlık kümesi
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS Stok ayarlama günlüğü başlıkları ve satırları |
| msdyn_inventoryadjustmentproducts | CDS stok transfer günlüğü başlıkları ve satırları   |

## <a name="entity-flow"></a>Varlık akışı
Field Service'ta gerçekleştirilen stok düzeltmeleri ve aktarmaları, **Deftere nakil durumu**, **Oluşturuldu**'dan **Deftere Nakledildi**'ye değiştirildikten sonra Finance and Operations'a eşitlenecektir. Bu durumda, ayarlama veya transfer emri kilitlenir ve salt okunur olur. Bu, düzeltmelerin ve aktarmaların Finance and Operations içinde deftere nakledilebileceği, ancak değiştirilemez. Finance and Operations'ta, tümleştirme ile oluşturulmuş ayarlamalar ve hareketler sırasında stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz. Toplu işi etkinleştirmenin ayrıntıları için aşağıdaki önkoşullara bakın.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü 
**Stok birimi** alanı, **Ürün** varlığına eklendi. Bu alan, Satış ve Stok birimi her zaman Finance and Operations içinde olmadığından ve Stok Birimi, Finance and Operations içinde Ambar Stoku için gereklidir.
Hem stok ayarlama hem de stok aktarma için bir ürünü bir stok ayarlama ürünü üzerinde ayarladığınızda, birim, stok ürün değerinden alınır. **Birim** alanında bir değer bulunursa, alan Stok ayarlama ürününde kilitlenir.

**Deftere Nakil Durumu** alanı, hem **Stok Ayarlama** varlığına hem de **Stok aktarma** varlığına eklenmiştir. Bu alan, bir ayarlama veya aktarma Finance and Operations'a gönderildiğinde filtre olarak kullanılır. Bu alan için varsayılan Oluşturuldu (1), ancak Finance and Operations'a gönderilmemiştir. Değeri Deftere Nakledildi (2) olarak güncelleştirirseniz, Finance and Operations'a gönderilir, ancak bundan sonra düzeltme ve transfer edemeyeceksiniz veya yeni satırlar ekleyemeyeceksiniz.

**Numara serisi** alanı, **Stok ayarlama ürünü** varlığına eklenmiştir. Bu alan, tümleştirmenin benzersiz bir numaraya sahip olmasını sağlar, böylece tümleştirme düzeltmeyi oluşturabilir ve güncelleştirebilir. İlk stok ayarlama ürününüzü oluşturduğunuzda, **P2C AutoNumber** varlığında yeni bir kayıt oluşturarak numara serisini ve kullanılan öneki korur.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="finance-and-operations"></a>Finance and Operations
Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş kullanarak otomatik olarak deftere nakledilebilir. Bu, şuradan etkinleştirilir: **Stok yönetimi > Periyodik görevler > CDS tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri**.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Stok ayarlama (Field Service'tan Fin and Ops'a): Stok ayarlama

[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Stok aktarma (Field Service'tan Fin and Ops'a): Stok aktarma

[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)
