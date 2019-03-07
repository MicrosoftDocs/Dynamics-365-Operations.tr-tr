---
title: İthalat kredi mektubu
description: Bu yordam, bir kredi mektubunun içeri alınması sürecini adım adım anlatır.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1768494182a79d7a33044498c1e768e61d937d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "313578"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="28762-103">İthalat kredi mektubu</span><span class="sxs-lookup"><span data-stu-id="28762-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28762-104">Bu yordam, bir kredi mektubunun içeri alınması sürecini adım adım anlatır.</span><span class="sxs-lookup"><span data-stu-id="28762-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="28762-105">Bu yöntemi tamamlamadan önce aşağıdakiler ayarlanmış olmalıdır: Banka tesisleri, deftere nakil profilleri, bir banka tesisi anlaşması ve satıcı bankası.</span><span class="sxs-lookup"><span data-stu-id="28762-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="28762-106">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="28762-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="28762-107">Akreditif Mektubu ile satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="28762-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="28762-108">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="28762-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="28762-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-109">Click New.</span></span>
3. <span data-ttu-id="28762-110">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="28762-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="28762-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="28762-113">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28762-113">Expand the General section.</span></span>
7. <span data-ttu-id="28762-114">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="28762-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="28762-116">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="28762-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="28762-118">Muhasebe tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="28762-119">Teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="28762-120">Not: 'Banka belge türü' alanında 'Kredi Mektubu' değeri seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="28762-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="28762-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-121">Click OK.</span></span>
14. <span data-ttu-id="28762-122">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="28762-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="28762-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="28762-125">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28762-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="28762-126">Teslimat sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="28762-127">Teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="28762-128">Teyit edilmiş teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="28762-129">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="28762-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="28762-130">Kredi mektubunun ayrıntılarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="28762-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="28762-131">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="28762-132">Kredi mektubu/ithalat tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="28762-133">Uygulama tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="28762-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="28762-134">'Banka hesabı' alanının, uygulama tarihini baz alan, varsayılan etkin banka hesabı değerinde olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="28762-135">Banka belgesi numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="28762-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="28762-136">Teslim alma tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="28762-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="28762-137">Banka belgesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28762-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="28762-138">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="28762-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="28762-139">Banka ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28762-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="28762-140">Muhbir banka alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="28762-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="28762-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-142">Click Save.</span></span>
33. <span data-ttu-id="28762-143">Satınalma siparişi sevkiyatlarını al.</span><span class="sxs-lookup"><span data-stu-id="28762-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="28762-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-144">Close the page.</span></span>
35. <span data-ttu-id="28762-145">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="28762-146">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-146">Click Confirm.</span></span>
37. <span data-ttu-id="28762-147">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="28762-148">Kredi mektubu/ithalat tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="28762-149">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-149">Click Process.</span></span>
40. <span data-ttu-id="28762-150">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-150">Click Confirm.</span></span>
    * <span data-ttu-id="28762-151">Tesis bakiyesinin satın alma sipariş miktarını azalttığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="28762-152">Bu örnekte, satın alma tutarı = 500,00,  tesis sınırı 10000,00,  bu nedenle, tesis Bakiyesi = 9500,00 =.</span><span class="sxs-lookup"><span data-stu-id="28762-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="28762-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-153">Close the page.</span></span>
42. <span data-ttu-id="28762-154">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="28762-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="28762-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-155">Click Save.</span></span>
44. <span data-ttu-id="28762-156">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="28762-157">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-157">Click Confirm.</span></span>
    * <span data-ttu-id="28762-158">Akreditif Mektubunu, birim fiyat değişikliği nedeniyle düzeltmek.</span><span class="sxs-lookup"><span data-stu-id="28762-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="28762-159">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="28762-160">Kredi mektubu/ithalat tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="28762-161">Akreditif Mektubunu, Satınalma birim fiyatı değişikliği nedeniyle düzeltmek.</span><span class="sxs-lookup"><span data-stu-id="28762-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="28762-162">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-162">Click Process.</span></span>
49. <span data-ttu-id="28762-163">Düzeltme'ye tıkla.</span><span class="sxs-lookup"><span data-stu-id="28762-163">Click Amend.</span></span>
50. <span data-ttu-id="28762-164">Kaldır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-164">Click Remove.</span></span>
51. <span data-ttu-id="28762-165">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-165">Click Yes.</span></span>
52. <span data-ttu-id="28762-166">Satınalma siparişi sevkiyatlarını al.</span><span class="sxs-lookup"><span data-stu-id="28762-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="28762-167">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-167">Click Process.</span></span>
54. <span data-ttu-id="28762-168">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-168">Click Confirm.</span></span>
    * <span data-ttu-id="28762-169">Tesis bakiyesinin satın alma sipariş miktarını azalttığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="28762-170">Bu örnekte, değiştirilmiş satın alma tutarı = 600,00,  tesis sınırı 10000,00,  bu nedenle, tesis Bakiyesi = 9400,00 =</span><span class="sxs-lookup"><span data-stu-id="28762-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="28762-171">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="28762-172">Sevk irsaliyesini deftere naklet</span><span class="sxs-lookup"><span data-stu-id="28762-172">Post Packing slip</span></span>
1. <span data-ttu-id="28762-173">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="28762-174">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-174">Click Product receipt.</span></span>
3. <span data-ttu-id="28762-175">PurchParmTable_Num alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="28762-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="28762-176">Akreditif Mektubuna ilişkin oluşturulan sevk irsaliyesi numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="28762-177">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="28762-178">Ürün alındı alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="28762-179">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-179">Click OK.</span></span>
7. <span data-ttu-id="28762-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-180">Close the page.</span></span>
8. <span data-ttu-id="28762-181">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="28762-182">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="28762-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="28762-183">Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="28762-184">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="28762-185">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="28762-186">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="28762-186">Verify the Import letter of credit status.</span></span>    
    *   
4. <span data-ttu-id="28762-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-187">Close the page.</span></span>
5. <span data-ttu-id="28762-188">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="28762-189">Satınalma faturasını deftere naklet</span><span class="sxs-lookup"><span data-stu-id="28762-189">Post purchase invoice</span></span>
1. <span data-ttu-id="28762-190">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="28762-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="28762-191">Kredi mektubu ile oluşturulan satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="28762-192">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="28762-193">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="28762-194">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="28762-195">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-195">Click Invoice.</span></span>
6. <span data-ttu-id="28762-196">Numara alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="28762-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="28762-197">Sevkiyat numarası alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="28762-198">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="28762-199">Fatura tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="28762-200">Eşleştirme durumunu güncelleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-200">Click Update match status.</span></span>
11. <span data-ttu-id="28762-201">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-201">Click Post.</span></span>
12. <span data-ttu-id="28762-202">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-202">Close the page.</span></span>
13. <span data-ttu-id="28762-203">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="28762-204">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="28762-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="28762-205">Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="28762-206">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="28762-207">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="28762-208">İthalat kredi mektubu2'yi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="28762-209">Doğrula:  Sevkiyat durumu = Faturalanan  banka tesisi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="28762-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="28762-210">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-210">Click View.</span></span>
5. <span data-ttu-id="28762-211">Başvuruyu yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-211">Click Print application.</span></span>
6. <span data-ttu-id="28762-212">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-212">Click OK.</span></span>
    * <span data-ttu-id="28762-213">Akreditif Mektubu uygulama yazdırılmaz doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="28762-214">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-214">Close the page.</span></span>
8. <span data-ttu-id="28762-215">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-215">Close the page.</span></span>
9. <span data-ttu-id="28762-216">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="28762-217">Kredi mektubu ile oluşturulmuş satınalma faturası için satıcı ödeme günlüğünü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="28762-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="28762-218">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="28762-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="28762-219">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-219">Click New.</span></span>
3. <span data-ttu-id="28762-220">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="28762-221">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="28762-222">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28762-222">Click Lines.</span></span>
6. <span data-ttu-id="28762-223">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28762-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="28762-224">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="28762-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="28762-225">Hareketleri kapat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="28762-226">Toplamlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28762-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="28762-227">Göster alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="28762-228">Banka belge numarası ve sevk irsaliyesi numarası alanlarının güncelleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="28762-229">İşaret onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="28762-230">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-230">Click OK.</span></span>
13. <span data-ttu-id="28762-231">Ödeme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="28762-232">Banka belge numarası ve sevk irsaliyesi numarası alanlarının güncelleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="28762-233">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-233">Click Post.</span></span>
15. <span data-ttu-id="28762-234">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-234">Close the page.</span></span>
16. <span data-ttu-id="28762-235">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="28762-236">Öndemiş faturadan sonra Kredi Mektubu durumunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="28762-237">Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="28762-238">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="28762-239">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="28762-240">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="28762-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="28762-241">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="28762-242">Banka hizmet limiti ve kullanım raporu doğrula</span><span class="sxs-lookup"><span data-stu-id="28762-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="28762-243">Nakit ve Banka yönetimi > Sorgular ve raporlar > Kredi veya teminat mektupları > Banka tesisleri ve kullanım raporu'na gidin.</span><span class="sxs-lookup"><span data-stu-id="28762-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="28762-244">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28762-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="28762-245">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-245">Click Filter.</span></span>
    * <span data-ttu-id="28762-246">Gerekli banka hesabıyla ilgili ölçüt alanını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="28762-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="28762-247">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="28762-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="28762-248">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="28762-249">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-249">Click OK.</span></span>
7. <span data-ttu-id="28762-250">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28762-250">Click OK.</span></span>
    * <span data-ttu-id="28762-251">Hareketleri listeleyen raporu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="28762-252">Hareketleri banka belge numarası, tesis sınırı, kullanılan tutar ve tesis bakiye tutarı ile rapor listeleri doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28762-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="28762-253">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28762-253">Close the page.</span></span>

