---
title: Satış siparişi faturaları oluşturma
description: Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 984bb482f357e35dcfa4c08597a6be9e39817b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837117"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="58821-103">Satış siparişi faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="58821-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58821-104">Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="58821-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="58821-105">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="58821-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="58821-106">Satış siparişinden fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="58821-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="58821-107">**Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Sevk edilen ancak faturalanmayan satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="58821-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="58821-108">Listeden bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="58821-109">**Eylem Bölmesinde**, **Fatura > Oluştur > Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="58821-110">Bu satış siparişiyle ilişkilendirilmiş birden fazla sevk irsaliyesi bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="58821-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="58821-111">Sevk irsaliyesi numarası yerine <multiple> sözcüğü görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="58821-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="58821-112">**Parametreler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="58821-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="58821-113">Faturanın deftere nakledilebilmesi için Nakil öğesinin Evet olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="58821-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="58821-114">Deftere nakli devre dışı bırakıp yalnızca faturayı yazdırmayı da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58821-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="58821-115">Ancak, fatura yerine bir proforma fatura hazırlayarak da aynı sonucu elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58821-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="58821-116">Bu seçenek, toplu işler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="58821-116">This option is used for batch jobs.</span></span> <span data-ttu-id="58821-117">Toplu iş çalıştırıldığında, sorgu çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="58821-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="58821-118">**Yazdırma** alanında 'Sonra'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="58821-119">**Fatura yazdır** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="58821-120">Yazdırma yönetimi, faturanın birden çok kopyasını yazdırabilir ve aynı zamanda faturayı bir PDF dosyası olarak e-posta yoluyla gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="58821-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="58821-121">**Masrafları yazdır** alanında 'Özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="58821-122">**Kredi limitini denetle** alanında 'Bakiye'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="58821-123">**İptal**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="58821-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="58821-124">Siparişleri tek bir faturada birleştirme</span><span class="sxs-lookup"><span data-stu-id="58821-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="58821-125">**Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="58821-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="58821-126">Birden fazla açık faturası olan bir müşteri bulun.</span><span class="sxs-lookup"><span data-stu-id="58821-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="58821-127">Aynı müşterideki birden çok açık satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="58821-128">**Eylem Bölmesinde**, **Fatura > Oluştur > Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="58821-129">**Parametreler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="58821-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="58821-130">**Miktar** alanında "Tümü"nü seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="58821-131">Genel bakış sekmesinde iki fatura bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="58821-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="58821-132">Şimdi bunları tek bir faturada birleştirin.</span><span class="sxs-lookup"><span data-stu-id="58821-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="58821-133">**Özet güncelleştirme kapsamı** alanında 'Fatura hesabı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="58821-134">Satış siparişlerini tek bir faturada birleştirmek için **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="58821-135">İki satış siparişi artık tek bir fatura birleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="58821-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="58821-136">**İptal**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="58821-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="58821-137">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58821-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="58821-138">Faturaları toplu işte deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="58821-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="58821-139">**Gezinti bölmesi > Modüller > Alacak hesapları > Faturalar > Toplu faturalama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="58821-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="58821-140">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-140">Click **Select**.</span></span>
3. <span data-ttu-id="58821-141">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-141">Click **OK**.</span></span>
4. <span data-ttu-id="58821-142">**Toplu iş** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-142">Click **Batch**.</span></span>
5. <span data-ttu-id="58821-143">**Toplu işlem** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58821-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="58821-144">**Yineleme**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="58821-145">**Günler**'i seçin</span><span class="sxs-lookup"><span data-stu-id="58821-145">Select **Days**.</span></span>
8. <span data-ttu-id="58821-146">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-146">Click **OK**.</span></span>
9. <span data-ttu-id="58821-147">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58821-147">Click **OK**.</span></span>
10. <span data-ttu-id="58821-148">**İptal**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="58821-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="58821-149">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58821-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]