--- 
title: "Satış siparişi faturaları oluşturma"
description: "Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="72e46-103">Satış siparişi faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="72e46-103">Create sales order invoices</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72e46-104">Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="72e46-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="72e46-105">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="72e46-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="72e46-106">Satış siparişinden fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="72e46-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="72e46-107">Alacak hesapları > Siparişler > Sevk edilen ancak faturalanmayan satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="72e46-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="72e46-108">Listeden bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="72e46-109">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="72e46-110">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-110">Click Invoice.</span></span>
    * <span data-ttu-id="72e46-111">Bu satış siparişiyle ilişkilendirilmiş birden fazla sevk irsaliyesi bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="72e46-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="72e46-112">Sevk irsaliyesi numarası yerine <multiple> sözcüğü görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="72e46-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="72e46-113">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="72e46-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="72e46-114">Faturanın deftere nakledilebilmesi için Nakil öğesinin Evet olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="72e46-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="72e46-115">Deftere nakli devre dışı bırakıp yalnızca faturayı yazdırmayı da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72e46-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="72e46-116">Ancak, fatura yerine bir proforma fatura hazırlayarak da aynı sonucu elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72e46-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="72e46-117">Bu seçenek, toplu işler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="72e46-117">This option is used for batch jobs.</span></span> <span data-ttu-id="72e46-118">Toplu iş çalıştırıldığında, sorgu çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="72e46-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="72e46-119">Yazdırma alanında 'Sonra'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="72e46-120">Fatura yazdır için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="72e46-121">Yazdırma yönetimi, faturanın birden çok kopyasını yazdırabilir ve aynı zamanda faturayı bir PDF dosyası olarak e-posta yoluyla gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="72e46-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="72e46-122">Giderleri yazdır alanında 'Özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="72e46-123">Kredi limitini denetle alanına 'Bakiye'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="72e46-124">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="72e46-125">Siparişleri tek bir faturada birleştirme</span><span class="sxs-lookup"><span data-stu-id="72e46-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="72e46-126">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="72e46-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="72e46-127">Birden fazla açık faturası olan bir müşteri bulun.</span><span class="sxs-lookup"><span data-stu-id="72e46-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="72e46-128">Açık bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-128">Select an open sales order.</span></span>
4. <span data-ttu-id="72e46-129">Aynı müşteri için başka bir açık satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="72e46-130">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="72e46-131">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-131">Click Invoice.</span></span>
7. <span data-ttu-id="72e46-132">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="72e46-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="72e46-133">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="72e46-134">Genel bakış sekmesinde iki fatura bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="72e46-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="72e46-135">Şimdi bunları tek bir faturada birleştirin.</span><span class="sxs-lookup"><span data-stu-id="72e46-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="72e46-136">Özet güncelleştirme kapsamı alanında 'Fatura'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="72e46-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="72e46-137">Satış siparişlerini tek bir faturada birleştirmek için Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="72e46-138">İki satış siparişi artık tek bir fatura birleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="72e46-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="72e46-139">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-139">Click Cancel.</span></span>
12. <span data-ttu-id="72e46-140">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="72e46-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="72e46-141">Faturaları toplu işte deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="72e46-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="72e46-142">Alacak hesapları > Faturalar > Toplu faturalama > Fatura'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="72e46-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="72e46-143">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-143">Click Select.</span></span>
3. <span data-ttu-id="72e46-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-144">Click OK.</span></span>
4. <span data-ttu-id="72e46-145">Toplu iş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-145">Click Batch.</span></span>
5. <span data-ttu-id="72e46-146">Toplu işlem'i açmak için Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="72e46-147">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-147">Click Recurrence.</span></span>
7. <span data-ttu-id="72e46-148">Günler'i seçin</span><span class="sxs-lookup"><span data-stu-id="72e46-148">Select Days</span></span>
8. <span data-ttu-id="72e46-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-149">Click OK.</span></span>
9. <span data-ttu-id="72e46-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-150">Click OK.</span></span>
10. <span data-ttu-id="72e46-151">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72e46-151">Click Cancel.</span></span>
11. <span data-ttu-id="72e46-152">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="72e46-152">Click Yes.</span></span>


