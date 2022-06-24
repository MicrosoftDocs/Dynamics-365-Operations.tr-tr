---
title: Proje içeren iş emirlerini Field Service'ten Supply Chain Management'a eşitleme
description: Bu makale iş emirlerini Dynamics 365 Field Service bir proje numarasına üzerinden Dynamics 365 Supply Chain Management üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: Henrikan
ms.date: 03/12/2019
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
ms.openlocfilehash: a43a7f7e900205bdb23fb9a35ca1518369683a42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860507"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Proje içeren iş emirlerini Field Service'ten Supply Chain Management'a eşitleme

[!include[banner](../includes/banner.md)]

Bu makale iş emirlerini Dynamics 365 Field Service bir proje numarasına üzerinden Dynamics 365 Supply Chain Management üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kullanılan **Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a)** şablonu, **İş Emirleri (Field Service'ten Supply Chain Management'a)** şablonuna dayanmaktadır. Daha fazla bilgi için bkz. [Field Service'teki iş emirlerini Supply Chain Management'taki satış siparişlerine eşitleme](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Bu makale, yalnızca iki şablon arasındaki farkı açıklar:
- **Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a)**
- **İş Emirleri (Field Service'ten Supply Chain Management'a)**

Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Supply Chain Management'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir. Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı:**

- Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a)

**Veri tümleştirme projesindeki görevin adı:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici Proje** alanı, İş Emri varlığına eklenmiştir. Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Supply Chain Management içindeki bir Projeye bağlanacaktır. **Sistem Durumu** Açık – Devam Ediyor'dan (690,970,000) daha yüksek bir duruma geçince **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderHeader

[![Veri tümleştirmede şablon eşleme, Proje İle İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderHeaderProject

[![Veri tümleştirmede şablon eşleme, Proje İle İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderProduct

[![Veri tümleştirmede şablon eşleme, Proje İle İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderService

[![Veri tümleştirmede şablon eşleme, Proje İle İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]