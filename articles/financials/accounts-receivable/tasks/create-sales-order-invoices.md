--- 
title: "Satış siparişi faturaları oluşturma"
description: "Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6f687816fc6393de2a587273a5350858b3503945
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="6bb7a-103">Satış siparişi faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="6bb7a-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6bb7a-104">Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="6bb7a-105">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="6bb7a-106">Satış siparişinden fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="6bb7a-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="6bb7a-107">Alacak hesapları > Siparişler > Sevk edilen ancak faturalanmayan satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="6bb7a-108">Listeden bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="6bb7a-109">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="6bb7a-110">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-110">Click Invoice.</span></span>
    * <span data-ttu-id="6bb7a-111">Bu satış siparişiyle ilişkilendirilmiş birden fazla sevk irsaliyesi bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="6bb7a-112">Sevk irsaliyesi numarası yerine <multiple> sözcüğü görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="6bb7a-113">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="6bb7a-114">Faturanın deftere nakledilebilmesi için Nakil öğesinin Evet olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="6bb7a-115">Deftere nakli devre dışı bırakıp yalnızca faturayı yazdırmayı da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="6bb7a-116">Ancak, fatura yerine bir proforma fatura hazırlayarak da aynı sonucu elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="6bb7a-117">Bu seçenek, toplu işler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-117">This option is used for batch jobs.</span></span> <span data-ttu-id="6bb7a-118">Toplu iş çalıştırıldığında, sorgu çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="6bb7a-119">Yazdırma alanında 'Sonra'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="6bb7a-120">Fatura yazdır için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="6bb7a-121">Yazdırma yönetimi, faturanın birden çok kopyasını yazdırabilir ve aynı zamanda faturayı bir PDF dosyası olarak e-posta yoluyla gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="6bb7a-122">Giderleri yazdır alanında 'Özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="6bb7a-123">Kredi limitini denetle alanına 'Bakiye'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="6bb7a-124">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="6bb7a-125">Siparişleri tek bir faturada birleştirme</span><span class="sxs-lookup"><span data-stu-id="6bb7a-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="6bb7a-126">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="6bb7a-127">Birden fazla açık faturası olan bir müşteri bulun.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="6bb7a-128">Açık bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-128">Select an open sales order.</span></span>
4. <span data-ttu-id="6bb7a-129">Aynı müşteri için başka bir açık satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="6bb7a-130">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="6bb7a-131">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-131">Click Invoice.</span></span>
7. <span data-ttu-id="6bb7a-132">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="6bb7a-133">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="6bb7a-134">Genel bakış sekmesinde iki fatura bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="6bb7a-135">Şimdi bunları tek bir faturada birleştirin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="6bb7a-136">Özet güncelleştirme kapsamı alanında 'Fatura'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="6bb7a-137">Satış siparişlerini tek bir faturada birleştirmek için Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="6bb7a-138">İki satış siparişi artık tek bir fatura birleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="6bb7a-139">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-139">Click Cancel.</span></span>
12. <span data-ttu-id="6bb7a-140">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="6bb7a-141">Faturaları toplu işte deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="6bb7a-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="6bb7a-142">Alacak hesapları > Faturalar > Toplu faturalama > Fatura'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="6bb7a-143">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-143">Click Select.</span></span>
3. <span data-ttu-id="6bb7a-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-144">Click OK.</span></span>
4. <span data-ttu-id="6bb7a-145">Toplu iş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-145">Click Batch.</span></span>
5. <span data-ttu-id="6bb7a-146">Toplu işlem'i açmak için Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="6bb7a-147">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-147">Click Recurrence.</span></span>
7. <span data-ttu-id="6bb7a-148">Günler'i seçin</span><span class="sxs-lookup"><span data-stu-id="6bb7a-148">Select Days</span></span>
8. <span data-ttu-id="6bb7a-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-149">Click OK.</span></span>
9. <span data-ttu-id="6bb7a-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-150">Click OK.</span></span>
10. <span data-ttu-id="6bb7a-151">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-151">Click Cancel.</span></span>
11. <span data-ttu-id="6bb7a-152">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6bb7a-152">Click Yes.</span></span>


