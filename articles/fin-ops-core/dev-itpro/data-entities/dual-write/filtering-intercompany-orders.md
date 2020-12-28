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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="507c7-103">Orders ile OrderLines eşitlemekten kaçınmak için şirketlerarası siparişleri filtreleme</span><span class="sxs-lookup"><span data-stu-id="507c7-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="507c7-104">**Orders** ile **OrderLines** varlıklarını eşitlemekten kaçınmak için şirketlerarası siparişleri filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="507c7-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="507c7-105">Bazı senaryolarda, şirketlerarası sipariş ayrıntıları müşteri etkileşimi uygulamasında gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="507c7-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="507c7-106">Standart Common Data Service varlıklarından her biri, **IntercompanyOrder** başvurularıyla genişletilir ve çift yazma eşlemeleri filtrelerdeki ek alanlara başvuracak şekilde değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="507c7-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="507c7-107">Bunun sonucunda şirketlerarası siparişler artık eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="507c7-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="507c7-108">Bu işlem, müşteri etkileşimi uygulamasında gereksiz verileri engeller.</span><span class="sxs-lookup"><span data-stu-id="507c7-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="507c7-109">**CDS Satış Siparişi Başlıkları**'na **IntercompanyOrder** başvurusu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="507c7-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="507c7-110">Bu, yalnızca şirketlerarası siparişlerde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="507c7-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="507c7-111">**IntercompanyOrder** alanı, **SalesTable** öğesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="507c7-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Hazırlamayı hedefe eşle, SalesOrderHeader":::
    
2. <span data-ttu-id="507c7-113">**CDS Satış Siparişi Başlıkları** genişletildikten sonra **IntercompanyOrder** alanı eşlemede kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="507c7-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="507c7-114">Sorgu dizesi olarak `INTERCOMPANYORDER == ""` ile bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="507c7-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Satış siparişi başlıkları, düzenleme sorgusu":::

3. <span data-ttu-id="507c7-116">**CDS Satış Siparişi Satırları**'na **IntercompanyInventTransId** başvurusu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="507c7-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="507c7-117">Bu, yalnızca şirketlerarası siparişlerde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="507c7-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="507c7-118">**InterCompanyInventTransID** alanı, **SalesLine** öğesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="507c7-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Hazırlamayı hedefe eşle, SalesOrderLine":::

4. <span data-ttu-id="507c7-120">**CDS Satış Siparişi Satırları** genişletildikten sonra **IntercompanyInventTransId** alanı eşlemede kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="507c7-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="507c7-121">Sorgu dizesi olarak `INTERCOMPANYINVENTTRANSID == ""` ile bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="507c7-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Satış siparişi satırları, düzenleme sorgusu":::

5. <span data-ttu-id="507c7-123">1. ve 2. adımda Common Data Service varlıklarını genişlettiğiniz şekilde **Satış Faturası Başlığı V2** ve **Satış Faturası Satırları V2** öğelerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="507c7-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="507c7-124">Ardından filtre sorgularını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="507c7-124">Then add the filter queries.</span></span> <span data-ttu-id="507c7-125">**Satış Faturası Başlığı V2** için filtre sorgusu `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` sorgusudur.</span><span class="sxs-lookup"><span data-stu-id="507c7-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="507c7-126">**Satış Faturası Satırları V2** için filtre sorgusu `INTERCOMPANYINVENTTRANSID == ""` sorgusudur.</span><span class="sxs-lookup"><span data-stu-id="507c7-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Hazırlamayı hedefe eşle, Satış Faturası Başlıkları":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Satış faturası başlıkları, düzenleme sorgusu":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Satış faturası satırları, düzenleme sorgusu":::

6. <span data-ttu-id="507c7-130">**Teklifler** varlığının şirketlerarası ilişkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="507c7-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="507c7-131">Bir kullanıcı, şirketlerarası müşterilerinizden biri için teklif oluşturursa, **CustGroup** alanını kullanarak bu müşterilerin tümünü bir müşteri grubunda bir araya getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="507c7-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="507c7-132">Başlık ve satırlar, **CustGroup** alanını ekleyip bu grubu dahil etmeyecek şekilde filtre uygulamak için genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="507c7-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Hazırlamayı hedefe eşle, Satış Teklifi Başlığı":::

7. <span data-ttu-id="507c7-134">**Teklifler** varlığını genişlettikten sonra, sorgu dizesi olarak `CUSTGROUP !=  "<company>"` ile bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="507c7-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Satış Teklifi Başlığı, düzenleme sorgusu":::
