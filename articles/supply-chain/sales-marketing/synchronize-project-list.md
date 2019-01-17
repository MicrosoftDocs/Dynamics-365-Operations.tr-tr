---
title: "Finance and Operations'tan Field Service'a proje listelerini eşitleme"
description: "Bu konu, projeleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Finance and Operations'tan Field Service'a proje listelerini eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, projeleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve görevleri, projeleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemeyi açıklar.

**Veri tümleştirmesindeki şablonun adı:**
- Projeler (Finance and Operations'tan Field Service'a)

**Veri tümleştirme projesindeki görevlerin adları:**
- Projeler

Aşağıdaki eşitleme görevlerinin, proje listesinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:
- Hesaplar (Sales'tan Finance and Operations'a) 

## <a name="entity-set"></a>Varlık kümesi
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projeler                |

## <a name="entity-flow"></a>Varlık akışı
Finance and Operations'ta oluşturulan projeler. **Proje türü** Zaman ve malzeme ve **Proje aşaması** işlevde olan projeler, Field Service'ta **Harici Proje** varlığına eşitlenir, Proje numarası, Proje adı, Proje aşaması ve Müşteri hesap bilgisi de dahil. **Harici Proje** listesi, Field Service İş Emirlerini, Finance and Operations projeleriyle eşleştirmekte kullanılır.
Field Service CRM çözümü Harici Proje, Operations'tan tüm Projeleri alan yeni bir varlıktır.
Harici Proje alanı, İş Emri varlığına eklenmiştir. Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Operations içindeki bir Projeye bağlanacaktır. Sistem Durumu Açık olarak değişenler – Sürmekte(690,970,000) daha yüksek bir durum Harici Proje alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu
### <a name="in-finance-and-operations"></a>Finance and Operations'ta
Veri varlığı Projeleri için izlemeyi etkinleştir

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projeler (Finance and Operations'tan Field Service'a): Projeler

[![Veri tümleştirmede şablon eşleme](./media/FSProject1.png)](./media/FSProject1.png)

