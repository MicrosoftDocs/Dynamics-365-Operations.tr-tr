---
title: Stok transferlerini ve düzeltmelerini Field Service'ten Supply Chain Management'a eşitleme
description: Bu konu stok düzeltmelerini ve aktarmalarını Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
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
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439183"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Stok transferlerini ve düzeltmelerini Field Service'ten Supply Chain Management'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu stok düzeltmelerini ve aktarmalarını Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve temel görevler, stok düzeltmelerini ve transferlerini Field Service'ten Supply Chain Management'a eşitlemede kullanılır.

**Veri Tümleştirmesindeki Şablonlar**
- Stok Düzeltmesi (Field Service'ten Supply Chain Management'a)
- Stok Transferleri (Field Service'ten Supply Chain Management'a)

**Veri tümleştirme projelerindeki görevler**
- Stok Düzeltmeleri
- Stok Transferleri

## <a name="entity-set"></a>Varlık kümesi
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS Stok ayarlama günlüğü başlıkları ve satırları |
| msdyn_inventoryadjustmentproducts | CDS stok transfer günlüğü başlıkları ve satırları   |

## <a name="entity-flow"></a>Varlık akışı
Field Service'ta gerçekleştirilen stok düzeltmeleri ve transferleri, **Deftere nakil durumu**, **Oluşturuldu**'dan **Deftere Nakledildi**'ye değiştirildikten sonra Supply Chain Management'a eşitlenecektir. Bu durumda, ayarlama veya transfer emri kilitlenir ve salt okunur olur. Bu, düzeltmelerin ve transferlerin Supply Chain Management'ta deftere nakledilebileceği, ancak değiştirilemeyeceği anlamına gelir. Supply Chain Management'ta, tümleştirme ile oluşturulmuş düzeltmeler ve hareketler sırasında stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz. Toplu işi etkinleştirmenin ayrıntıları için aşağıdaki önkoşullara bakın.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü 
**Stok birimi** alanı, **Ürün** varlığına eklendi. Bu alan, Satış ve Stok birimi her zaman Supply Chain Management'ta olmadığından ve Stok Birimi, Supply Chain Management'ta Ambar Stoku için gereklidir.
Hem stok ayarlama hem de stok aktarma için bir ürünü bir stok ayarlama ürünü üzerinde ayarladığınızda, birim, stok ürün değerinden alınır. **Birim** alanında bir değer bulunursa, alan Stok ayarlama ürününde kilitlenir.

**Deftere Nakil Durumu** alanı, hem **Stok Ayarlama** varlığına hem de **Stok aktarma** varlığına eklenmiştir. Bu alan, Supply Chain Management'a bir düzeltme veya transfer gönderildiğinde filtre olarak kullanılır. Bu alan için varsayılan değer Oluşturuldu'dur (1) ancak Supply Chain Management'a gönderilmemiştir. Değeri Deftere Nakledildi (2) olarak güncelleştirirseniz Supply Chain Management'a gönderilir ancak bundan sonra düzeltme ve transfer edemezsiniz veya yeni satırlar ekleyemezsiniz.

**Numara serisi** alanı, **Stok ayarlama ürünü** varlığına eklenmiştir. Bu alan, tümleştirmenin benzersiz bir numaraya sahip olmasını sağlar, böylece tümleştirme düzeltmeyi oluşturabilir ve güncelleştirebilir. İlk stok ayarlama ürününüzü oluşturduğunuzda, **P2C AutoNumber** varlığında yeni bir kayıt oluşturarak numara serisini ve kullanılan öneki korur.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="supply-chain-management"></a>Supply Chain Management
Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş kullanarak otomatik olarak deftere nakledilebilir. Bu, şuradan etkinleştirilir: **Stok yönetimi > Periyodik görevler > CDS tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri**.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Stok düzeltmesi (Field Service'ten Supply Chain Management'a): Stok düzeltmesi

[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Stok transferi (Field Service'ten Supply Chain Management'a): Stok transferi

[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]