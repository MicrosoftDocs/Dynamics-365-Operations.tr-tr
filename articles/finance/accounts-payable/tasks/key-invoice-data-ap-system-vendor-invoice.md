---
title: Satıcı faturası kullanarak fatura verilerini AP sistemine gir
description: Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7abae6d680d899a0294ad3c298a4b0264ba01d0b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189442"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="fcf63-103">Satıcı faturası kullanarak fatura verilerini AP sistemine gir</span><span class="sxs-lookup"><span data-stu-id="fcf63-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcf63-104">Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="fcf63-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="fcf63-105">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcf63-105">Create a purchase order</span></span>
1. <span data-ttu-id="fcf63-106">Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Tüm satın alma siparişleri** öpesine gidin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="fcf63-107">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-107">Click **New**.</span></span>
3. <span data-ttu-id="fcf63-108">**Satıcı hesabı** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fcf63-109">Seçmek üzere bir satıcı bulun.</span><span class="sxs-lookup"><span data-stu-id="fcf63-109">Find a vendor to select.</span></span> <span data-ttu-id="fcf63-110">Örneğin aşağıya kayarak ABD-104'e gelin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="fcf63-111">Satıcı ABD-104'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="fcf63-112">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-112">Click **OK**.</span></span>
7. <span data-ttu-id="fcf63-113">**Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="fcf63-114">Bir stok maddesi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-114">Select an inventory item.</span></span> <span data-ttu-id="fcf63-115">Örneğin, madde numarası olarak 1000 seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="fcf63-116">**Satır ayrıntıları** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="fcf63-117">**Kurulum** sekmesine tıklayın. Eşleştirme ilkesini eşleştirme kullanmamak, 2 yönlü eşleştirme ya da 3 yönlü eşleştirme kullanmak üzere geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fcf63-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="fcf63-118">Eylem Bölmesinde, **Satınalma** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="fcf63-119">**Onayla**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="fcf63-120">Ürünleri alma</span><span class="sxs-lookup"><span data-stu-id="fcf63-120">Receive the products</span></span>
1. <span data-ttu-id="fcf63-121">Eylem Bölmesinde, **Teslim al** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="fcf63-122">**Ürün girişi** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="fcf63-123">**Ürün girişi** alanına ürün giriş numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="fcf63-124">Örneğin PR123 yazın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="fcf63-125">Ürün girişini deftere nakletmek için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="fcf63-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="fcf63-127">Satıcı faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcf63-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="fcf63-128">Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Alınan ancak faturalanmayan satınalma siparişleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="fcf63-129">Oluşturduğunuz satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="fcf63-130">Eylem Bölmesinde **Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="fcf63-131">**Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="fcf63-132">**Numara** alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="fcf63-133">**Fatura açıklaması** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="fcf63-134">**Fatura tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="fcf63-135">**Birim fiyatı** alanına 1200 yazın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="fcf63-136">**Satır ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-136">Click **Add line**.</span></span>
10. <span data-ttu-id="fcf63-137">**Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="fcf63-138">Listede kurulum masrafı madde numarasını bulun.</span><span class="sxs-lookup"><span data-stu-id="fcf63-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="fcf63-139">Örneğin S0001</span><span class="sxs-lookup"><span data-stu-id="fcf63-139">For example, S0001</span></span>
12. <span data-ttu-id="fcf63-140">Kurulum masrafı madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-140">Select the installation charge item number.</span></span> <span data-ttu-id="fcf63-141">Yaptığınız değişikliklerden sonra eşleştirme yapılmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="fcf63-142">**Eşleştirme durumunu güncelleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="fcf63-143">Eylem Bölmesinde, **Gözden geçir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="fcf63-144">**Eşleşme ayrıntıları** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-144">Click **Matching details**.</span></span> <span data-ttu-id="fcf63-145">Hizmetlerin bulunduğu yeni satırın eşleştirilmesi gerekmediği için durumu "Gerçekleştirilmedi" olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="fcf63-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="fcf63-146">Aldığınız stok maddesi için ürün girişini seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="fcf63-147">Ürün girişini içeren satır eşleştirildi ancak miktar veya fiyat uyuşmazlığı olduğundan başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="fcf63-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="fcf63-148">**Birim fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="fcf63-149">Artık birim fiyatı eşleştiğinden durum Başarılı olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fcf63-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="fcf63-150">İlkeniz uyuşmazlıklara izin veriyorsa veya eşleşme yalnızca bir uyarıysa, faturayı deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fcf63-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="fcf63-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-151">Close the page.</span></span>
19. <span data-ttu-id="fcf63-152">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-152">Click **Post**.</span></span>
20. <span data-ttu-id="fcf63-153">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="fcf63-153">Close the form.</span></span> <span data-ttu-id="fcf63-154">Satınalma siparişinin artık alındı ancak faturalanmadı olarak listelenmediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="fcf63-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

