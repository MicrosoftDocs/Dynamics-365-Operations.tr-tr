---
title: Satış siparişi faturaları oluşturma
description: Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "353322"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="244d8-103">Satış siparişi faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="244d8-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="244d8-104">Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="244d8-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="244d8-105">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="244d8-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="244d8-106">Satış siparişinden fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="244d8-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="244d8-107">Alacak hesapları > Siparişler > Sevk edilen ancak faturalanmayan satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="244d8-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="244d8-108">Listeden bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="244d8-109">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="244d8-110">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-110">Click Invoice.</span></span>
    * <span data-ttu-id="244d8-111">Bu satış siparişiyle ilişkilendirilmiş birden fazla sevk irsaliyesi bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="244d8-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="244d8-112">Sevk irsaliyesi numarası yerine <multiple> sözcüğü görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="244d8-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="244d8-113">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="244d8-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="244d8-114">Faturanın deftere nakledilebilmesi için Nakil öğesinin Evet olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="244d8-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="244d8-115">Deftere nakli devre dışı bırakıp yalnızca faturayı yazdırmayı da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="244d8-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="244d8-116">Ancak, fatura yerine bir proforma fatura hazırlayarak da aynı sonucu elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="244d8-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="244d8-117">Bu seçenek, toplu işler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="244d8-117">This option is used for batch jobs.</span></span> <span data-ttu-id="244d8-118">Toplu iş çalıştırıldığında, sorgu çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="244d8-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="244d8-119">Yazdırma alanında 'Sonra'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="244d8-120">Fatura yazdır için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="244d8-121">Yazdırma yönetimi, faturanın birden çok kopyasını yazdırabilir ve aynı zamanda faturayı bir PDF dosyası olarak e-posta yoluyla gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="244d8-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="244d8-122">Giderleri yazdır alanında 'Özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="244d8-123">Kredi limitini denetle alanına 'Bakiye'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="244d8-124">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="244d8-125">Siparişleri tek bir faturada birleştirme</span><span class="sxs-lookup"><span data-stu-id="244d8-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="244d8-126">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="244d8-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="244d8-127">Birden fazla açık faturası olan bir müşteri bulun.</span><span class="sxs-lookup"><span data-stu-id="244d8-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="244d8-128">Açık bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-128">Select an open sales order.</span></span>
4. <span data-ttu-id="244d8-129">Aynı müşteri için başka bir açık satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="244d8-130">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="244d8-131">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-131">Click Invoice.</span></span>
7. <span data-ttu-id="244d8-132">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="244d8-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="244d8-133">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="244d8-134">Genel bakış sekmesinde iki fatura bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="244d8-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="244d8-135">Şimdi bunları tek bir faturada birleştirin.</span><span class="sxs-lookup"><span data-stu-id="244d8-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="244d8-136">Özet güncelleştirme kapsamı alanında 'Fatura'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="244d8-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="244d8-137">Satış siparişlerini tek bir faturada birleştirmek için Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="244d8-138">İki satış siparişi artık tek bir fatura birleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="244d8-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="244d8-139">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-139">Click Cancel.</span></span>
12. <span data-ttu-id="244d8-140">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="244d8-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="244d8-141">Faturaları toplu işte deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="244d8-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="244d8-142">Alacak hesapları > Faturalar > Toplu faturalama > Fatura'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="244d8-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="244d8-143">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-143">Click Select.</span></span>
3. <span data-ttu-id="244d8-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-144">Click OK.</span></span>
4. <span data-ttu-id="244d8-145">Toplu iş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-145">Click Batch.</span></span>
5. <span data-ttu-id="244d8-146">Toplu işlem'i açmak için Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="244d8-147">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-147">Click Recurrence.</span></span>
7. <span data-ttu-id="244d8-148">Günler'i seçin</span><span class="sxs-lookup"><span data-stu-id="244d8-148">Select Days</span></span>
8. <span data-ttu-id="244d8-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-149">Click OK.</span></span>
9. <span data-ttu-id="244d8-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-150">Click OK.</span></span>
10. <span data-ttu-id="244d8-151">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244d8-151">Click Cancel.</span></span>
11. <span data-ttu-id="244d8-152">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="244d8-152">Click Yes.</span></span>

