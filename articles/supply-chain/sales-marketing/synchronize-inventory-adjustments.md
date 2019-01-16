---
title: "Stok hareketlerini ve ayarlamaları Field Service'tan Finance and Operations'a eşitlemek"
description: "Bu konu, stok ayarlamaları ve aktarmaları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Stok ayarlamalarını Field Service'tan Finance and Operations'a eşitlemek

[!include[banner](../includes/banner.md)]

Bu konu, stok ayarlamaları ve aktarmaları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon, stok ayarlamaları ve aktarmaları eşitlemelerini Microsoft Dynamics 365 for Field Service'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

**Veri tümleştirmesindeki şablonların adı:**
- Stok Ayarlama (Field Service'ten Finance and Operations'a)
- Stok Aktarma (Field Service'ten Finance and Operations'a)

**Veri tümleştirme projelerindeki görevlerin adları:**
- Stok Düzeltmeleri
- Stok Transferleri

## <a name="entity-set"></a>Varlık kümesi
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS Stok ayarlama günlüğü başlıkları ve satırları |
| msdyn_inventoryadjustmentproducts | CDS stok transfer günlüğü başlıkları ve satırları   |

## <a name="entity-flow"></a>Varlık akışı
Field Service'ta gerçekleştirilen stok düzeltmeleri ve aktarmaları, **Deftere nakil durumu**, Oluşturuldu'dan Deftere Nakledildi'ye değiştirildiğinde Finance and Operations'a eşitlenecektir. Bu gerçekleştiğinde, ayarlama veya aktarma emri kilitlenir ve salt okunur olur çünkü ayarlamalar ve aktarmalar Finance and Operations'a deftere nakledilebilir ve bu nedenle değiştirilemeyebilir.
Finance and Operations'ta, tümleştirme ile oluşturulmuş ayarlamalar ve hareketler stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz. Toplu işi etkinleştirmek hakkında ayrıntılar için gereksinimleri aşağıda görüntüleyin.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü 
Stok Birimi alanı, Ürün varlığına eklendi. Bu alan, Satış ve Stok Birimi her zaman aynı Operasyonlarda olmadığı için gereklidir ve operasyonlardaki Ambar Stoku için Stok Biriminine ihtiyaç duyarız.
Hem Stok Ayarlama hem de Stok Aktarma için bir Ürünü bir Stok Ayarlama Ürünü üzerinde ayarladığınızda, Birim, Ürünler Stok Ürün değerinden alınır. Birim alanında bir değer bulunursa, alan Stok Ayarlama Ürününde kilitlenir

Deftere Nakil Durumu alanı, hem Stok Ayarlama varlığına hem de Stok Aktarma varlığına eklenmiştir. Bu alan, bir ayarlama veya aktarma Operasyonlara gönderildiğinde filtre olarak kullanılır. Bu alan Oluşturuldu (1) olarak varsayılan alınır ve Operasyonlara gönderilmez. Değiştirdikleriniz, Deftere Nakledildi (2) olur, operasyonlara gönderilir ancak Ayarlama veya Aktarmada hiçbir şey değiştiremezsiniz veya buna yeni satırlar ekleyemezsiniz.
Stok Ayarlama Ürün varlığına Numara Serisi alanı eklenmiştir. Bu alan, tümleştirmenin Benzersiz bir sayıya sahip olmasına yardımcı olur, böylece tümleştirme oluşturmaları ve güncelleştirmeleri ne zaman yapacağını bilir. İlk Stok Ayarlama Ürününüzü oluşturduğunuzda, P2C AutoNumber varlığında yeni bir kayıt oluşturarak numara serisini ve kullanılan öneki korur.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="in-finance-and-operations"></a>Finance and Operations'ta
Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş ile otomatik olarak deftere nakledilebilir. Bu, şuradan etkinleştirilir: Stok yönetimi > Periyodik görevler > CDS tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Stok Ayarlama (Field Service'tan Finance and Operations'a): Stok Ayarlama

[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Stok Aktarma (Field Service'tan Finance and Operations'a): Stok Aktarma

[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)

