---
title: Teminat mektubu hareketi
description: Bu yöntem Teminat Mektubu sürecini anlatmaktadır.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f13ea1f9acd48cc1e7dce794369e89901bdb582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976350"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="be2c3-103">Teminat mektubu hareketi</span><span class="sxs-lookup"><span data-stu-id="be2c3-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be2c3-104">Bu yöntem Teminat Mektubu sürecini anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="be2c3-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="be2c3-105">Bu yordamı tamamlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir:</span><span class="sxs-lookup"><span data-stu-id="be2c3-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="be2c3-106">Teminat mektubu için banka tesisleri ve deftere nakil profilleri ayarlama.</span><span class="sxs-lookup"><span data-stu-id="be2c3-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="be2c3-107">Teminat mektubu için banka tesisi anlaşması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="be2c3-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="be2c3-108">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="be2c3-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="be2c3-109">Teminat mektubu ile satış emri yaratın</span><span class="sxs-lookup"><span data-stu-id="be2c3-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="be2c3-110">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="be2c3-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-111">Click New.</span></span>
3. <span data-ttu-id="be2c3-112">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="be2c3-113">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-113">Expand the General section.</span></span>
5. <span data-ttu-id="be2c3-114">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="be2c3-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="be2c3-116">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="be2c3-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="be2c3-118">Banka belge türü alanında Teminat Mektubu'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="be2c3-119">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-119">Click OK.</span></span>
11. <span data-ttu-id="be2c3-120">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="be2c3-121">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="be2c3-122">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="be2c3-123">Teslimat sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="be2c3-124">Not: Teslimat tarihi kontrolünü seçin = Yok</span><span class="sxs-lookup"><span data-stu-id="be2c3-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="be2c3-125">Talep edilen sevk tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="be2c3-126">Teyit edilen sevk tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="be2c3-127">Teminat mektubu isteği işlemden geçirin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="be2c3-128">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="be2c3-129">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="be2c3-130">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="be2c3-131">İletişim kutusu formunu açmak için talep seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="be2c3-132">Tür alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="be2c3-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="be2c3-134">Değer alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="be2c3-135">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="be2c3-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-136">Click OK.</span></span>
10. <span data-ttu-id="be2c3-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="be2c3-138">Teminat mektubunu bankaya işleyin bankaya gönderin</span><span class="sxs-lookup"><span data-stu-id="be2c3-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="be2c3-139">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="be2c3-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="be2c3-141">Bankaya gönder kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="be2c3-142">Banka hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="be2c3-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="be2c3-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="be2c3-145">Bankadan teminat mektubunu alın işleyin</span><span class="sxs-lookup"><span data-stu-id="be2c3-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="be2c3-146">Bankadan al kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="be2c3-147">Banka numarası alanına alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="be2c3-148">Hesaplanan marj ve gider alanları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="be2c3-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-149">Click OK.</span></span>
4. <span data-ttu-id="be2c3-150">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="be2c3-151">'Bankadan alma' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="be2c3-152">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="be2c3-153">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-153">Click Lines.</span></span>
    * <span data-ttu-id="be2c3-154">Günlük girişlerinin kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="be2c3-155">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="be2c3-156">Teminat mektubu lehtara vermeyi işleyin</span><span class="sxs-lookup"><span data-stu-id="be2c3-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="be2c3-157">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="be2c3-158">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="be2c3-159">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="be2c3-160">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="be2c3-161">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="be2c3-162">Tahsildara gönder kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="be2c3-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-163">Click OK.</span></span>
8. <span data-ttu-id="be2c3-164">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="be2c3-165">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="be2c3-166">Tahsildara gönder kutusunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="be2c3-167">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-167">Click OK.</span></span>
12. <span data-ttu-id="be2c3-168">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="be2c3-169">'Lehtara ver' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="be2c3-170">Teminat mektubunun değerini artırmayı işleyin</span><span class="sxs-lookup"><span data-stu-id="be2c3-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="be2c3-171">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="be2c3-172">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="be2c3-173">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="be2c3-174">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="be2c3-175">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="be2c3-176">Değeri artır kutusu formunu açmak için tıklayın</span><span class="sxs-lookup"><span data-stu-id="be2c3-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="be2c3-177">Eklenecek alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="be2c3-178">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-178">Click OK.</span></span>
9. <span data-ttu-id="be2c3-179">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="be2c3-180">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="be2c3-181">Değeri artır kutusu formunu açmak için tıklayın</span><span class="sxs-lookup"><span data-stu-id="be2c3-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="be2c3-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-182">Click OK.</span></span>
13. <span data-ttu-id="be2c3-183">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="be2c3-184">'Değer artır' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="be2c3-185">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="be2c3-186">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="be2c3-187">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-187">Click Lines.</span></span>
    * <span data-ttu-id="be2c3-188">Mevcut günlük girişlerinin kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="be2c3-189">Teminat mektubunu nakde çevirmeyi işleyin</span><span class="sxs-lookup"><span data-stu-id="be2c3-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="be2c3-190">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="be2c3-191">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="be2c3-192">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="be2c3-193">Teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="be2c3-194">Eylem bölmesinde, teminat mektubuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="be2c3-195">Nakte çevir kutusu formunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="be2c3-196">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-196">Click OK.</span></span>
8. <span data-ttu-id="be2c3-197">Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="be2c3-198">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="be2c3-199">Nakte çevir kutusu formunu açmak için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="be2c3-200">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-200">Click OK.</span></span>
12. <span data-ttu-id="be2c3-201">Eylemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="be2c3-202">'Nakte çevirme' kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="be2c3-203">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="be2c3-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="be2c3-204">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="be2c3-205">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-205">Click Lines.</span></span>
    * <span data-ttu-id="be2c3-206">Mevcut günlük girişlerinin kaydını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="be2c3-207">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="be2c3-207">Close the page.</span></span>

