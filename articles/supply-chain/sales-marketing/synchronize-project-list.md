---
title: Proje listesini Supply Chain Management'tan Field Service'e eşitleme
description: Bu makale projeleri Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
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
ms.openlocfilehash: 71c0580953f01c2d29e99fa2928a0b4a3937d5c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899367"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Proje listesini Supply Chain Management'tan Field Service'e eşitleme

[!include[banner](../includes/banner.md)]

Bu makale projeleri Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler
Aşağıdaki şablon ve temel görevler, projelerin Supply Chain Management'tan Field Service'e eşitlemesini çalıştırmak için kullanılır.

**Veri Tümleştirmesindeki Şablon**
- Projeler (Supply Chain Management'tan Field Service'e)

**Veri tümleştirme projesindeki görev**
- Projeler

Aşağıdaki eşitleme görevlerinin, proje listesinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:
- Hesaplar (Sales'den Supply Chain Management'a) 

## <a name="entity-set"></a>Varlık kümesi
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projeler                |

## <a name="entity-flow"></a>Varlık akışı
Projeler Supply Chain Management'ta oluşturulur. **Proje türü**, **Zaman ve malzeme**'ye ayarlanır ve **Proje aşaması**, **İşlevde olan** projelere ayarlanır, Field Service'ta **Harici Proje** varlığına eşitlenir, Proje numarası, Proje adı, Proje aşaması ve Müşteri hesap bilgisi de dahil. **Harici Proje** listesi, Field Service iş emirlerini Supply Chain Management projeleriyle eşleştirmede kullanılır.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici Proje** varlığı, tüm projeleri Supply Chain Management'tan alır. **Harici Proje** alanı, **İş Emri** varlığına eklenmiştir. Bu bir arama alanıdır ve bu yüzden, iş emrinizi bir proje ile etiketleyerek, satış siparişi Supply Chain Management içindeki bir projeye bağlanacaktır. **Sistem Durumu**, **Açık – Sürmekte(690,970,000)** daha yüksek bir duruma değiştikten sonra, **Harici Proje** alanı kilitlenir ve değeri artık ekleyemez, kaldıramaz veya değiştiremezsiniz.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu
### <a name="supply-chain-management"></a>Supply Chain Management
Veri varlığı projeleri için izlemeyi etkinleştir

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projeler (Supply Chain Management'tan Field Service'e): Projeler

[![Veri tümleştirmede şablon eşleme.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]