---
title: Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme
description: Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "329862"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme

[!include[banner](../includes/banner.md)]

Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kullanılan **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Finance and Operations'tan Sales'e) – Doğrudan** şablonunu temel alır. Daha fazla bilgi için bkz. [Ürünler (Finance and Operations'tan Sales'e) – Doğrudan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Bu konu yalnızca **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** ile **Field Service Ürünleri (Finance and Operations'tan Sales'e)** şablonları arasındaki farkları açıklar.

Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Finance and Operations'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir. Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı:**

- Proje İle İş Emirleri (Field Service'tan Finance and Operations'a)

**Veri tümleştirme projesindeki görevin adı:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü
**Harici Proje** alanı, İş Emri varlığına eklenmiştir. Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Finance and Operations içindeki bir Projeye bağlanacaktır. **Sistem Durumu** açık'tan değişenler – Sürmekte(690,970,000) daha yüksek bir durum **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderHeader

[![Veri tümleştirmede şablon eşleme](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderHeaderProject

[![Veri tümleştirmede şablon eşleme](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderProduct

[![Veri tümleştirmede şablon eşleme](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderService

[![Veri tümleştirmede şablon eşleme](./media/FSWOP4.png)](./media/FSWOP4.png)
