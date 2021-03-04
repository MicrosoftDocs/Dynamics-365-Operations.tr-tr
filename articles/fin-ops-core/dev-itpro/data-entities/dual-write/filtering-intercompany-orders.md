---
title: Orders ile OrderLines eşitlemekten kaçınmak için şirketlerarası siparişleri filtreleme
description: Bu konuda, Orders ile OrderLines eşitlemekten kaçınmak için şirketlerarası siparişlerin nasıl filtreleneceği açıklanmaktadır.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701045"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Orders ile OrderLines eşitlemekten kaçınmak için şirketlerarası siparişleri filtreleme

[!include [banner](../../includes/banner.md)]

**Orders** ile **OrderLines** varlıklarını eşitlemekten kaçınmak için şirketlerarası siparişleri filtreleyebilirsiniz. Bazı senaryolarda, şirketlerarası sipariş ayrıntıları müşteri etkileşimi uygulamasında gerekli değildir.

Standart Common Data Service varlıklarından her biri, **IntercompanyOrder** başvurularıyla genişletilir ve çift yazma eşlemeleri filtrelerdeki ek alanlara başvuracak şekilde değiştirilir. Bunun sonucunda şirketlerarası siparişler artık eşitlenmez. Bu işlem, müşteri etkileşimi uygulamasında gereksiz verileri engeller.

1. **CDS Satış Siparişi Başlıkları**'na **IntercompanyOrder** başvurusu ekleyin. Bu, yalnızca şirketlerarası siparişlerde doldurulur. **IntercompanyOrder** alanı, **SalesTable** öğesinde bulunur.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Hazırlamayı hedefe eşle, SalesOrderHeader":::
    
2. **CDS Satış Siparişi Başlıkları** genişletildikten sonra **IntercompanyOrder** alanı eşlemede kullanılabilir hale gelir. Sorgu dizesi olarak `INTERCOMPANYORDER == ""` ile bir filtre uygulayın.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Satış siparişi başlıkları, düzenleme sorgusu":::

3. **CDS Satış Siparişi Satırları**'na **IntercompanyInventTransId** başvurusu ekleyin.  Bu, yalnızca şirketlerarası siparişlerde doldurulur. **InterCompanyInventTransID** alanı, **SalesLine** öğesinde bulunur.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Hazırlamayı hedefe eşle, SalesOrderLine":::

4. **CDS Satış Siparişi Satırları** genişletildikten sonra **IntercompanyInventTransId** alanı eşlemede kullanılabilir hale gelir. Sorgu dizesi olarak `INTERCOMPANYINVENTTRANSID == ""` ile bir filtre uygulayın.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Satış siparişi satırları, düzenleme sorgusu":::

5. 1. ve 2. adımda Common Data Service varlıklarını genişlettiğiniz şekilde **Satış Faturası Başlığı V2** ve **Satış Faturası Satırları V2** öğelerini genişletin. Ardından filtre sorgularını ekleyin. **Satış Faturası Başlığı V2** için filtre sorgusu `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` sorgusudur. **Satış Faturası Satırları V2** için filtre sorgusu `INTERCOMPANYINVENTTRANSID == ""` sorgusudur.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Hazırlamayı hedefe eşle, Satış Faturası Başlıkları":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Satış faturası başlıkları, düzenleme sorgusu":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Satış faturası satırları, düzenleme sorgusu":::

6. **Teklifler** varlığının şirketlerarası ilişkisi yoktur. Bir kullanıcı, şirketlerarası müşterilerinizden biri için teklif oluşturursa, **CustGroup** alanını kullanarak bu müşterilerin tümünü bir müşteri grubunda bir araya getirebilirsiniz.  Başlık ve satırlar, **CustGroup** alanını ekleyip bu grubu dahil etmeyecek şekilde filtre uygulamak için genişletilebilir.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Hazırlamayı hedefe eşle, Satış Teklifi Başlığı":::

7. **Teklifler** varlığını genişlettikten sonra, sorgu dizesi olarak `CUSTGROUP !=  "<company>"` ile bir filtre uygulayın.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Satış Teklifi Başlığı, düzenleme sorgusu":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]