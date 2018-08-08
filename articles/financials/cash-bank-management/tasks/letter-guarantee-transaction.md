--- 
title: Teminat mektubu hareketi
description: "Bu yöntem Teminat Mektubu sürecini anlatmaktadır."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 182b6eb0f9aa1ceffd2336ecb217d3e29e3046d6
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="28491-103">Teminat mektubu hareketi</span><span class="sxs-lookup"><span data-stu-id="28491-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28491-104">Bu yöntem Teminat Mektubu sürecini anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="28491-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="28491-105">Bu yordamı tamamlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir:</span><span class="sxs-lookup"><span data-stu-id="28491-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="28491-106">Teminat mektubu için banka tesisleri ve deftere nakil profilleri ayarlama.</span><span class="sxs-lookup"><span data-stu-id="28491-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="28491-107">Teminat mektubu için banka tesisi anlaşması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="28491-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="28491-108">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="28491-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="28491-109">Teminat mektubu ile satış emri yaratın</span><span class="sxs-lookup"><span data-stu-id="28491-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="28491-110">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="28491-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-111">Click New.</span></span>
3. <span data-ttu-id="28491-112">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="28491-113">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28491-113">Expand the General section.</span></span>
5. <span data-ttu-id="28491-114">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="28491-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="28491-116">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="28491-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="28491-118">Banka belge türü alanında Teminat Mektubu'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="28491-119">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-119">Click OK.</span></span>
11. <span data-ttu-id="28491-120">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="28491-121">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="28491-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="28491-122">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28491-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="28491-123">Teslimat sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="28491-124">Not: Teslimat tarihi kontrolünü seçin = Yok</span><span class="sxs-lookup"><span data-stu-id="28491-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="28491-125">Talep edilen sevk tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28491-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="28491-126">Teyit edilen sevk tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="28491-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="28491-127">Teminat mektubu isteği işlemden geçirin.</span><span class="sxs-lookup"><span data-stu-id="28491-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="28491-128">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="28491-129">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="28491-130">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="28491-131">İletişim kutusu formunu açmak için talep seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="28491-132">Tür alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="28491-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="28491-134">Değer alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="28491-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="28491-135">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="28491-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="28491-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-136">Click OK.</span></span>
10. <span data-ttu-id="28491-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28491-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="28491-138">Teminat mektubunu bankaya işleyin bankaya gönderin</span><span class="sxs-lookup"><span data-stu-id="28491-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="28491-139">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="28491-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="28491-141">Bankaya gönder kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="28491-142">Banka hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="28491-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="28491-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="28491-145">Bankadan teminat mektubunu alın işleyin</span><span class="sxs-lookup"><span data-stu-id="28491-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="28491-146">Bankadan al kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="28491-147">Banka numarası alanına alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="28491-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="28491-148">Hesaplanan marj ve gider alanları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="28491-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-149">Click OK.</span></span>
4. <span data-ttu-id="28491-150">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28491-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="28491-151">'Bankadan alma' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="28491-152">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="28491-153">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-153">Click Lines.</span></span>
    * <span data-ttu-id="28491-154">Günlük girişlerinin kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="28491-155">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28491-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="28491-156">Teminat mektubu lehtara vermeyi işleyin</span><span class="sxs-lookup"><span data-stu-id="28491-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="28491-157">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="28491-158">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="28491-159">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="28491-160">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="28491-161">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="28491-162">Tahsildara gönder kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="28491-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-163">Click OK.</span></span>
8. <span data-ttu-id="28491-164">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="28491-165">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="28491-166">Tahsildara gönder kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="28491-167">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-167">Click OK.</span></span>
12. <span data-ttu-id="28491-168">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28491-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="28491-169">'Lehtara ver' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="28491-170">Teminat mektubunun değerini artırmayı işleyin</span><span class="sxs-lookup"><span data-stu-id="28491-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="28491-171">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="28491-172">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="28491-173">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="28491-174">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="28491-175">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="28491-176">Değeri artır kutusu formunu açmak için tıklayın</span><span class="sxs-lookup"><span data-stu-id="28491-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="28491-177">Eklenecek alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="28491-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="28491-178">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-178">Click OK.</span></span>
9. <span data-ttu-id="28491-179">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="28491-180">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="28491-181">Değeri artır kutusu formunu açmak için tıklayın</span><span class="sxs-lookup"><span data-stu-id="28491-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="28491-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-182">Click OK.</span></span>
13. <span data-ttu-id="28491-183">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28491-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="28491-184">'Değer artır' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="28491-185">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="28491-186">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="28491-187">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-187">Click Lines.</span></span>
    * <span data-ttu-id="28491-188">Mevcut günlük girişlerinin kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="28491-189">Teminat mektubunu nakde çevirmeyi işleyin</span><span class="sxs-lookup"><span data-stu-id="28491-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="28491-190">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="28491-191">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="28491-192">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="28491-193">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="28491-194">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="28491-195">Nakte çevir kutusu formunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="28491-196">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-196">Click OK.</span></span>
8. <span data-ttu-id="28491-197">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="28491-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="28491-198">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="28491-199">Nakte çevir kutusu formunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="28491-200">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-200">Click OK.</span></span>
12. <span data-ttu-id="28491-201">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28491-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="28491-202">'Nakte çevirme' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="28491-203">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="28491-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="28491-204">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28491-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="28491-205">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28491-205">Click Lines.</span></span>
    * <span data-ttu-id="28491-206">Mevcut günlük girişlerinin kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="28491-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="28491-207">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28491-207">Close the page.</span></span>


