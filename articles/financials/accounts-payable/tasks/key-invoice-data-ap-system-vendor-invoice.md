---
title: Satıcı faturası kullanarak fatura verilerini AP sistemine gir
description: Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569644"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="50acf-103">Satıcı faturası kullanarak fatura verilerini AP sistemine gir</span><span class="sxs-lookup"><span data-stu-id="50acf-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50acf-104">Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="50acf-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="50acf-105">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="50acf-105">Create a purchase order</span></span>
1. <span data-ttu-id="50acf-106">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="50acf-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="50acf-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-107">Click New.</span></span>
3. <span data-ttu-id="50acf-108">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="50acf-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="50acf-109">Seçmek üzere bir satıcı bulun.</span><span class="sxs-lookup"><span data-stu-id="50acf-109">Find a vendor to select.</span></span> <span data-ttu-id="50acf-110">Örneğin aşağıya kayarak ABD-104'e gelin.</span><span class="sxs-lookup"><span data-stu-id="50acf-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="50acf-111">Satıcı ABD-104'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="50acf-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="50acf-112">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="50acf-112">Click OK.</span></span>
7. <span data-ttu-id="50acf-113">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="50acf-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="50acf-114">Bir stok maddesi seçin.</span><span class="sxs-lookup"><span data-stu-id="50acf-114">Select an inventory item.</span></span> <span data-ttu-id="50acf-115">Örneğin, madde numarası olarak 1000 seçin.</span><span class="sxs-lookup"><span data-stu-id="50acf-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="50acf-116">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="50acf-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="50acf-117">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="50acf-118">Eşleştirme ilkesini eşleştirme kullanmamak, 2 yönlü eşleştirme ya da 3 yönlü eşleştirme kullanmak üzere geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50acf-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="50acf-119">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="50acf-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="50acf-120">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="50acf-121">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="50acf-122">Ürünleri alma</span><span class="sxs-lookup"><span data-stu-id="50acf-122">Receive the products</span></span>
1. <span data-ttu-id="50acf-123">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="50acf-124">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-124">Click Product receipt.</span></span>
3. <span data-ttu-id="50acf-125">Ürün girişi alanına ürün giriş numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="50acf-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="50acf-126">Örneğin PR123 yazın.</span><span class="sxs-lookup"><span data-stu-id="50acf-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="50acf-127">Ürün girişini deftere nakletmek için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="50acf-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="50acf-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="50acf-129">Satıcı faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="50acf-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="50acf-130">Alacak hesapları > Satınalma siparişleri > Alınan ancak faturalanmayan satınalma siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="50acf-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="50acf-131">Oluşturduğunuz satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="50acf-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="50acf-132">Eylem Bölmesinde Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="50acf-133">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-133">Click Invoice.</span></span>
5. <span data-ttu-id="50acf-134">Numara alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="50acf-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="50acf-135">Fatura açıklaması alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="50acf-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="50acf-136">Fatura tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="50acf-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="50acf-137">Birim fiyatı alanına 1200 yazın.</span><span class="sxs-lookup"><span data-stu-id="50acf-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="50acf-138">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-138">Click Add line.</span></span>
10. <span data-ttu-id="50acf-139">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="50acf-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="50acf-140">Listede kurulum masrafı madde numarasını bulun.</span><span class="sxs-lookup"><span data-stu-id="50acf-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="50acf-141">Örneğin S0001</span><span class="sxs-lookup"><span data-stu-id="50acf-141">For example, S0001</span></span>
12. <span data-ttu-id="50acf-142">Kurulum masrafı madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="50acf-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="50acf-143">Yaptığınız değişikliklerden sonra eşleştirme yapılmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="50acf-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="50acf-144">Eşleştirme durumunu güncelleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-144">Click Update match status.</span></span>
14. <span data-ttu-id="50acf-145">Eylem Bölmesinde, Gözden geçir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="50acf-146">Eşleşme ayrıntıları öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-146">Click Matching details.</span></span>
    * <span data-ttu-id="50acf-147">Hizmetlerin bulunduğu yeni satırın eşleştirilmesi gerekmediği için durumu "Gerçekleştirilmedi" olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="50acf-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="50acf-148">Aldığınız stok maddesi için ürün girişini seçin.</span><span class="sxs-lookup"><span data-stu-id="50acf-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="50acf-149">Ürün girişini içeren satır eşleştirildi ancak miktar veya fiyat uyuşmazlığı olduğundan başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="50acf-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="50acf-150">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="50acf-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="50acf-151">Artık birim fiyatı eşleştiğinden durum Başarılı olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="50acf-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="50acf-152">İlkeniz uyuşmazlıklara izin veriyorsa veya eşleşme yalnızca bir uyarıysa, faturayı deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50acf-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="50acf-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="50acf-153">Close the page.</span></span>
19. <span data-ttu-id="50acf-154">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="50acf-154">Click Post.</span></span>
20. <span data-ttu-id="50acf-155">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="50acf-155">Close the form.</span></span>
    * <span data-ttu-id="50acf-156">Satınalma siparişinin artık alındı ancak faturalanmadı olarak listelenmediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="50acf-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

