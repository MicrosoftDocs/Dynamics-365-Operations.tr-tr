---
title: Orders ile OrderLines tablolarının eşitlenmesini önelemek için şirketlerarası siparişleri filtreleme
description: Bu konuda, Orders ve OrderLines varlıklarının eşitlenmemesi için şirketlerarası siparişlere nasıl filtre uygulanacağı açıklanmaktadır.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5e7b0188d5c2dc4ee7691266aa4c857fc189d0f0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347260"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Orders ile OrderLines tablolarının eşitlenmesini önelemek için şirketlerarası siparişleri filtreleme

[!include [banner](../../includes/banner.md)]

**Orders** ile **OrderLines** tablolarının eşitlenmemesi için şirketlerarası siparişleri filtreleyebilirsiniz. Bazı senaryolarda, şirketlerarası sipariş ayrıntıları müşteri etkileşimi uygulamasında zorunlu değildir.

Her standart Dataverse tablosu, **IntercompanyOrder** sütununa başvurular aracılığıyla genişletilir ve çift yazma eşlemeleri filtrelerdeki ek sütunlara başvuracak şekilde değiştirilir. Bu sayede, şirketlerarası siparişler artık eşitlenmez. Bu işlem, müşteri etkileşimi uygulamasında gereksiz verileri önlemeye yardımcı olur.

1. **IntercompanyOrder** sütununa başvuru ekleyerek **CDS Satış Siparişi Başlıkları** tablosunu genişletin. Bu sütun yalnızca şirketlerarası siparişlerde doldurulur. **IntercompanyOrder** sütunu, **SalesTable** tablosunda kullanılabilir.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS Satış Siparişi Başlıkları için hazırlamayı hedef sayfasıyla eşleme.":::

2. **CDS Satış Siparişi Başlıkları** genişletildikten sonra **IntercompanyOrder** sütunu eşlemede kullanılabilir hale gelir. Sorgu dizesi `INTERCOMPANYORDER == ""` olan bir filtre uygulayın.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CD Satış Siparişi Başlıkları için sorgu iletişim kutusu düzenleme.":::

3. **IntercompanyInventTransId** sütununa başvuru ekleyerek **CDS Satış Siparişi Satırları** tablosunu genişletin. Bu sütun yalnızca şirketlerarası siparişlerde doldurulur. **InterCompanyInventTransId** sütunu, **SalesLine** tablosunda kullanılabilir.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS Satış Siparişi Satırları için hazırlamayı hedef sayfasıyla eşleme.":::

4. **CDS Satış Siparişi Satırları** genişletildikten sonra **IntercompanyInventTransId** sütunu eşlemede kullanılabilir hale gelir. Sorgu dizesi `INTERCOMPANYINVENTTRANSID == ""` olan bir filtre uygulayın.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CD Satış Siparişi Satırları için sorgu iletişim kutusu düzenleme.":::

5. **Satış Faturası Başlığı V2** tablosunu genişletmek ve filtre sorgusu eklemek için 1. ve 2. adımları tekrarlayın. Bu durumda, filtre için sorgu dizesi olarak `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` öğesini kullanın.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Satış Faturası Başlığı V2 için hazırlamayı hedef sayfasıyla eşleme.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Satış Faturası Başlığı V2 için sorgu iletişim kutusu düzenleme.":::

6. **Satış Faturası Satırları V2** tablosunu genişletmek ve filtre sorgusu eklemek için 3. ve 4. adımları tekrarlayın. Bu durumda, filtre için sorgu dizesi olarak `INTERCOMPANYINVENTTRANSID == ""` öğesini kullanın.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Satış Faturası Satırları V2 için sorgu iletişim kutusu düzenleme.":::

7. **Teklifler** tablosunun şirketlerarası ilişkisi yoktur. Bir kullanıcı, şirketlerarası müşterilerinizden biri için teklif oluşturursa, bu müşterilerin tümünü bir müşteri grubunda bir araya getirmek için **CustGroup** sütununu kullanabilirsiniz. **CustGroup** sütununu ekleyerek başlığı ve satırları genişletebilir ve ardından grubun dahil edilmemesi için filtre uygulayabilirsiniz.

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS Satış Teklifi Başlığı için hazırlamayı hedef sayfasıyla eşleme.":::

8. **Teklifler** genişletildikten sonra, sorgu dizesi `CUSTGROUP != "<company>"` olan bir filtre uygulayın.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS Satış Teklifi Başlığı için sorgu iletişim kutusu düzenleme.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]