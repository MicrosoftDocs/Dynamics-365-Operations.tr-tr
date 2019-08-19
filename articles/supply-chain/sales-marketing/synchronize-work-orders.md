---
title: Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme
description: Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843421"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme

[!include[banner](../includes/banner.md)]

Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kullanılan **İş Emirleri Proje ile (Field Service'ten Fin and Ops'a)** şablonu, **İş Emirleri (Field Service to Fin and Ops)** şablonuna dayanmaktadır. Dah af azla bilgi için bkz. [Field Service'daki iş emirlerini Finance and Operations'taki satış siparişleriyle eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Bu konu, yalnızca iki şablon arasındaki farkı açıklar:
- **Proje İle İş Emirleri (Field Service'tan Fin and Ops'a)**
- **Proje Emirleri (Field Service'tan Fin and Ops'a)**

Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Finance and Operations'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir. Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı:**

- Proje İle İş Emirleri (Field Service'tan Fin and Ops'a)

**Veri tümleştirme projesindeki görevin adı:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici Proje** alanı, İş Emri varlığına eklenmiştir. Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Finance and Operations içindeki bir Projeye bağlanacaktır. **Sistem Durumu** açık'tan değişenler – Sürmekte(690,970,000) daha yüksek bir durum **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderHeader

[![Veri tümleştirmede şablon eşleme](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderHeaderProject

[![Veri tümleştirmede şablon eşleme](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderProduct

[![Veri tümleştirmede şablon eşleme](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderService

[![Veri tümleştirmede şablon eşleme](./media/FSWOP4.png)](./media/FSWOP4.png)
