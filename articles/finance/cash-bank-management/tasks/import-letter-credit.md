---
title: İthalat kredi mektubu
description: Bu yordam, bir kredi mektubunun içeri alınması sürecini adım adım anlatır.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac0b1aacbf0e5dbe69a8125dc0a1373de0957d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225405"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="9d0fd-103">İthalat kredi mektubu</span><span class="sxs-lookup"><span data-stu-id="9d0fd-103">Import letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d0fd-104">Bu yordam, bir kredi mektubunun içeri alınması sürecini adım adım anlatır.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="9d0fd-105">Bu yöntemi tamamlamadan önce aşağıdakiler ayarlanmış olmalıdır: Banka tesisleri, deftere nakil profilleri, bir banka tesisi anlaşması ve satıcı bankası.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="9d0fd-106">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="9d0fd-107">Akreditif Mektubu ile satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9d0fd-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="9d0fd-108">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9d0fd-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-109">Click New.</span></span>
3. <span data-ttu-id="9d0fd-110">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="9d0fd-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9d0fd-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9d0fd-113">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-113">Expand the General section.</span></span>
7. <span data-ttu-id="9d0fd-114">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="9d0fd-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9d0fd-116">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="9d0fd-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9d0fd-118">Muhasebe tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="9d0fd-119">Teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="9d0fd-120">Not: 'Banka belge türü' alanında 'Kredi Mektubu' değeri seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="9d0fd-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-121">Click OK.</span></span>
14. <span data-ttu-id="9d0fd-122">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="9d0fd-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="9d0fd-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9d0fd-125">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="9d0fd-126">Teslimat sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="9d0fd-127">Teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="9d0fd-128">Teyit edilmiş teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="9d0fd-129">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="9d0fd-130">Kredi mektubunun ayrıntılarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="9d0fd-131">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="9d0fd-132">Kredi mektubu/ithalat tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="9d0fd-133">Uygulama tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="9d0fd-134">'Banka hesabı' alanının, uygulama tarihini baz alan, varsayılan etkin banka hesabı değerinde olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="9d0fd-135">Banka belgesi numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="9d0fd-136">Teslim alma tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="9d0fd-137">Banka belgesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="9d0fd-138">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="9d0fd-139">Banka ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="9d0fd-140">Muhbir banka alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="9d0fd-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="9d0fd-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-142">Click Save.</span></span>
33. <span data-ttu-id="9d0fd-143">Satınalma siparişi sevkiyatlarını al.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="9d0fd-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-144">Close the page.</span></span>
35. <span data-ttu-id="9d0fd-145">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="9d0fd-146">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-146">Click Confirm.</span></span>
37. <span data-ttu-id="9d0fd-147">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="9d0fd-148">Kredi mektubu/ithalat tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="9d0fd-149">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-149">Click Process.</span></span>
40. <span data-ttu-id="9d0fd-150">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-150">Click Confirm.</span></span>
    * <span data-ttu-id="9d0fd-151">Tesis bakiyesinin satın alma sipariş miktarını azalttığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="9d0fd-152">Bu örnekte, satın alma tutarı = 500,00,  tesis sınırı 10000,00,  bu nedenle, tesis Bakiyesi = 9500,00 =.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="9d0fd-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-153">Close the page.</span></span>
42. <span data-ttu-id="9d0fd-154">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="9d0fd-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-155">Click Save.</span></span>
44. <span data-ttu-id="9d0fd-156">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="9d0fd-157">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-157">Click Confirm.</span></span>
    * <span data-ttu-id="9d0fd-158">Akreditif Mektubunu, birim fiyat değişikliği nedeniyle düzeltmek.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="9d0fd-159">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="9d0fd-160">Kredi mektubu/ithalat tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="9d0fd-161">Akreditif Mektubunu, Satınalma birim fiyatı değişikliği nedeniyle düzeltmek.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="9d0fd-162">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-162">Click Process.</span></span>
49. <span data-ttu-id="9d0fd-163">Düzeltme'ye tıkla.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-163">Click Amend.</span></span>
50. <span data-ttu-id="9d0fd-164">Kaldır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-164">Click Remove.</span></span>
51. <span data-ttu-id="9d0fd-165">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-165">Click Yes.</span></span>
52. <span data-ttu-id="9d0fd-166">Satınalma siparişi sevkiyatlarını al.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="9d0fd-167">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-167">Click Process.</span></span>
54. <span data-ttu-id="9d0fd-168">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-168">Click Confirm.</span></span>
    * <span data-ttu-id="9d0fd-169">Tesis bakiyesinin satın alma sipariş miktarını azalttığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="9d0fd-170">Bu örnekte, değiştirilmiş satın alma tutarı = 600,00,  tesis sınırı 10000,00,  bu nedenle, tesis Bakiyesi = 9400,00 =</span><span class="sxs-lookup"><span data-stu-id="9d0fd-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="9d0fd-171">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="9d0fd-172">Sevk irsaliyesini deftere naklet</span><span class="sxs-lookup"><span data-stu-id="9d0fd-172">Post Packing slip</span></span>
1. <span data-ttu-id="9d0fd-173">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="9d0fd-174">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-174">Click Product receipt.</span></span>
3. <span data-ttu-id="9d0fd-175">PurchParmTable_Num alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="9d0fd-176">Akreditif Mektubuna ilişkin oluşturulan sevk irsaliyesi numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="9d0fd-177">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9d0fd-178">Ürün alındı alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="9d0fd-179">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-179">Click OK.</span></span>
7. <span data-ttu-id="9d0fd-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-180">Close the page.</span></span>
8. <span data-ttu-id="9d0fd-181">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="9d0fd-182">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="9d0fd-183">Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="9d0fd-184">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9d0fd-185">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9d0fd-186">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="9d0fd-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-187">Close the page.</span></span>
5. <span data-ttu-id="9d0fd-188">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="9d0fd-189">Satınalma faturasını deftere naklet</span><span class="sxs-lookup"><span data-stu-id="9d0fd-189">Post purchase invoice</span></span>
1. <span data-ttu-id="9d0fd-190">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="9d0fd-191">Kredi mektubu ile oluşturulan satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="9d0fd-192">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9d0fd-193">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9d0fd-194">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="9d0fd-195">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-195">Click Invoice.</span></span>
6. <span data-ttu-id="9d0fd-196">Numara alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="9d0fd-197">Sevkiyat numarası alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="9d0fd-198">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9d0fd-199">Fatura tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="9d0fd-200">Eşleştirme durumunu güncelleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-200">Click Update match status.</span></span>
11. <span data-ttu-id="9d0fd-201">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-201">Click Post.</span></span>
12. <span data-ttu-id="9d0fd-202">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-202">Close the page.</span></span>
13. <span data-ttu-id="9d0fd-203">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="9d0fd-204">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="9d0fd-205">Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="9d0fd-206">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9d0fd-207">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9d0fd-208">İthalat kredi mektubu2'yi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="9d0fd-209">Doğrula:  Sevkiyat durumu = Faturalanan  banka tesisi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="9d0fd-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="9d0fd-210">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-210">Click View.</span></span>
5. <span data-ttu-id="9d0fd-211">Başvuruyu yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-211">Click Print application.</span></span>
6. <span data-ttu-id="9d0fd-212">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-212">Click OK.</span></span>
    * <span data-ttu-id="9d0fd-213">Akreditif Mektubu uygulama yazdırılmaz doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="9d0fd-214">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-214">Close the page.</span></span>
8. <span data-ttu-id="9d0fd-215">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-215">Close the page.</span></span>
9. <span data-ttu-id="9d0fd-216">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="9d0fd-217">Kredi mektubu ile oluşturulmuş satınalma faturası için satıcı ödeme günlüğünü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="9d0fd-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="9d0fd-218">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9d0fd-219">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-219">Click New.</span></span>
3. <span data-ttu-id="9d0fd-220">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="9d0fd-221">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9d0fd-222">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-222">Click Lines.</span></span>
6. <span data-ttu-id="9d0fd-223">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="9d0fd-224">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="9d0fd-225">Hareketleri kapat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="9d0fd-226">Toplamlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="9d0fd-227">Göster alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="9d0fd-228">Banka belge numarası ve sevk irsaliyesi numarası alanlarının güncelleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="9d0fd-229">İşaret onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="9d0fd-230">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-230">Click OK.</span></span>
13. <span data-ttu-id="9d0fd-231">Ödeme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="9d0fd-232">Banka belge numarası ve sevk irsaliyesi numarası alanlarının güncelleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="9d0fd-233">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-233">Click Post.</span></span>
15. <span data-ttu-id="9d0fd-234">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-234">Close the page.</span></span>
16. <span data-ttu-id="9d0fd-235">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="9d0fd-236">Öndemiş faturadan sonra Kredi Mektubu durumunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="9d0fd-237">Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="9d0fd-238">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9d0fd-239">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9d0fd-240">İthalat kredi mektubunun durumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="9d0fd-241">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="9d0fd-242">Banka hizmet limiti ve kullanım raporu doğrula</span><span class="sxs-lookup"><span data-stu-id="9d0fd-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="9d0fd-243">Nakit ve Banka yönetimi > Sorgular ve raporlar > Kredi veya teminat mektupları > Banka tesisleri ve kullanım raporu'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="9d0fd-244">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="9d0fd-245">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-245">Click Filter.</span></span>
    * <span data-ttu-id="9d0fd-246">Gerekli banka hesabıyla ilgili ölçüt alanını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="9d0fd-247">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="9d0fd-248">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9d0fd-249">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-249">Click OK.</span></span>
7. <span data-ttu-id="9d0fd-250">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-250">Click OK.</span></span>
    * <span data-ttu-id="9d0fd-251">Hareketleri listeleyen raporu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="9d0fd-252">Hareketleri banka belge numarası, tesis sınırı, kullanılan tutar ve tesis bakiye tutarı ile rapor listeleri doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="9d0fd-253">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9d0fd-253">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]