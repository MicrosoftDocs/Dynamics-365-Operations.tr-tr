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
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748653"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="0e68c-103">Orders ile OrderLines tablolarının eşitlenmesini önelemek için şirketlerarası siparişleri filtreleme</span><span class="sxs-lookup"><span data-stu-id="0e68c-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e68c-104">**Orders** ile **OrderLines** tablolarının eşitlenmemesi için şirketlerarası siparişleri filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e68c-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="0e68c-105">Bazı senaryolarda, şirketlerarası sipariş ayrıntıları müşteri etkileşimi uygulamasında zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="0e68c-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="0e68c-106">Her standart Dataverse tablosu, **IntercompanyOrder** sütununa başvurular aracılığıyla genişletilir ve çift yazma eşlemeleri filtrelerdeki ek sütunlara başvuracak şekilde değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0e68c-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="0e68c-107">Bu sayede, şirketlerarası siparişler artık eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="0e68c-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="0e68c-108">Bu işlem, müşteri etkileşimi uygulamasında gereksiz verileri önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0e68c-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="0e68c-109">**IntercompanyOrder** sütununa başvuru ekleyerek **CDS Satış Siparişi Başlıkları** tablosunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="0e68c-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="0e68c-110">Bu sütun yalnızca şirketlerarası siparişlerde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="0e68c-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="0e68c-111">**IntercompanyOrder** sütunu, **SalesTable** tablosunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0e68c-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS Satış Siparişi Başlıkları için hazırlamayı hedef sayfasıyla eşleme":::

2. <span data-ttu-id="0e68c-113">**CDS Satış Siparişi Başlıkları** genişletildikten sonra **IntercompanyOrder** sütunu eşlemede kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="0e68c-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="0e68c-114">Sorgu dizesi `INTERCOMPANYORDER == ""` olan bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CD Satış Siparişi Başlıkları için sorgu iletişim kutusu düzenleme":::

3. <span data-ttu-id="0e68c-116">**IntercompanyInventTransId** sütununa başvuru ekleyerek **CDS Satış Siparişi Satırları** tablosunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="0e68c-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="0e68c-117">Bu sütun yalnızca şirketlerarası siparişlerde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="0e68c-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="0e68c-118">**InterCompanyInventTransId** sütunu, **SalesLine** tablosunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0e68c-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS Satış Siparişi Satırları için hazırlamayı hedef sayfasıyla eşleme":::

4. <span data-ttu-id="0e68c-120">**CDS Satış Siparişi Satırları** genişletildikten sonra **IntercompanyInventTransId** sütunu eşlemede kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="0e68c-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="0e68c-121">Sorgu dizesi `INTERCOMPANYINVENTTRANSID == ""` olan bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CD Satış Siparişi Satırları için sorgu iletişim kutusu düzenleme":::

5. <span data-ttu-id="0e68c-123">**Satış Faturası Başlığı V2** tablosunu genişletmek ve filtre sorgusu eklemek için 1. ve 2. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="0e68c-124">Bu durumda, filtre için sorgu dizesi olarak `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Satış Faturası Başlığı V2 için hazırlamayı hedef sayfasıyla eşleme":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Satış Faturası Başlığı V2 için sorgu iletişim kutusu düzenleme":::

6. <span data-ttu-id="0e68c-127">**Satış Faturası Satırları V2** tablosunu genişletmek ve filtre sorgusu eklemek için 3. ve 4. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="0e68c-128">Bu durumda, filtre için sorgu dizesi olarak `INTERCOMPANYINVENTTRANSID == ""` öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Satış Faturası Satırları V2 için sorgu iletişim kutusu düzenleme":::

7. <span data-ttu-id="0e68c-130">**Teklifler** tablosunun şirketlerarası ilişkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="0e68c-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="0e68c-131">Bir kullanıcı, şirketlerarası müşterilerinizden biri için teklif oluşturursa, bu müşterilerin tümünü bir müşteri grubunda bir araya getirmek için **CustGroup** sütununu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e68c-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="0e68c-132">**CustGroup** sütununu ekleyerek başlığı ve satırları genişletebilir ve ardından grubun dahil edilmemesi için filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e68c-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS Satış Teklifi Başlığı için hazırlamayı hedef sayfasıyla eşleme":::

8. <span data-ttu-id="0e68c-134">**Teklifler** genişletildikten sonra, sorgu dizesi `CUSTGROUP != "<company>"` olan bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="0e68c-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS Satış Teklifi Başlığı için sorgu iletişim kutusu düzenleme":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]