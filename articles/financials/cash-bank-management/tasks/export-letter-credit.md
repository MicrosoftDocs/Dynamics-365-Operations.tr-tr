--- 
title: "Kredi mektubunu dışa aktarma"
description: "Bu yordam, bir ihracat kredi mektubu sürecini adım adım anlatır."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa4b57825bcf81778d91ee01484511bb40f6bd7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="ca9fc-103">Kredi mektubunu dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="ca9fc-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca9fc-104">Bu yordam, bir ihracat kredi mektubu sürecini adım adım anlatır.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="ca9fc-105">Bir kredi mektubu, bir banka tarafından verilen ve bu bankanın, alıcı ve satıcı arasındaki sözleşmenin koşullarını yerine getirilirse, alıcı adına ödeme yapmayı kabul ettiği bir anlaşmadır.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="ca9fc-106">'Önce 'Kredi Mektubu_Banka tesisi anlaşması yarat' yordamını, daha sonra da 'Banka tesisleri ve nakil profillerini ayarlama' yordamını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="ca9fc-107">Bu yordamın başarıyla çalışması için, USMF demo şirketi seçili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="ca9fc-108">İhraç kredi mektubu için satış siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca9fc-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="ca9fc-109">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ca9fc-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-110">Click New.</span></span>
3. <span data-ttu-id="ca9fc-111">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ca9fc-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ca9fc-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ca9fc-114">Genel bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="ca9fc-115">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ca9fc-116">İhraç edilecek maddenin stoğunun nerede tutulduğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="ca9fc-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ca9fc-118">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ca9fc-119">İhraç edilecek maddenin stoğunun hangi ardiye tutulduğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="ca9fc-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ca9fc-121">Not: 'Banka belge türü' alanında 'Kredi Mektubu' değerinin seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="ca9fc-122">Banka belge türü alanında Kredi Mektubu'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="ca9fc-123">Teslimat bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="ca9fc-124">Teslimat tarihi kontrolünü seçin = Yok.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="ca9fc-125">Talep edilen teslim alma tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="ca9fc-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-126">Click OK.</span></span>
15. <span data-ttu-id="ca9fc-127">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ca9fc-128">Verilmek/Satılmak için gerekli maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="ca9fc-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ca9fc-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ca9fc-131">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="ca9fc-132">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="ca9fc-133">Teslimat sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="ca9fc-134">Talep edilen sevk tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="ca9fc-135">Teyit edilen sevk tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="ca9fc-136">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="ca9fc-137">Kredi mektubu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="ca9fc-138">Banka belgesi numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="ca9fc-139">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="ca9fc-140">Banka detayları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="ca9fc-141">Amir banka alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="ca9fc-142">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="ca9fc-143">Muhabir banka alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="ca9fc-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="ca9fc-145">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="ca9fc-146">Satış siparişi sevkiyatlarını al'a tıkla.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="ca9fc-147">Banka belgesini yayımla'ya tıkla.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="ca9fc-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="ca9fc-149">Sevk irsaliyesini deftere naklet</span><span class="sxs-lookup"><span data-stu-id="ca9fc-149">Post Packing slip</span></span>
1. <span data-ttu-id="ca9fc-150">Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="ca9fc-151">Sevk irsaliyesini deftere naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="ca9fc-152">Parametreler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="ca9fc-153">Miktar alanında 'Tümü'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="ca9fc-154">Kurulum bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="ca9fc-155">Sevk irsaliyesi tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="ca9fc-156">Sevkiyat numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="ca9fc-157">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ca9fc-158">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-158">Click OK.</span></span>
10. <span data-ttu-id="ca9fc-159">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="ca9fc-160">Satış faturası deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="ca9fc-160">Post sales invoice</span></span>
1. <span data-ttu-id="ca9fc-161">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="ca9fc-162">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-162">Click Invoice.</span></span>
3. <span data-ttu-id="ca9fc-163">Genel bakış bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="ca9fc-164">Sevkiyat numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="ca9fc-165">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ca9fc-166">Kurulum bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="ca9fc-167">Fatura tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="ca9fc-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-168">Click OK.</span></span>
9. <span data-ttu-id="ca9fc-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="ca9fc-170">Sevkiyat belgeleri gönderim durumu</span><span class="sxs-lookup"><span data-stu-id="ca9fc-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="ca9fc-171">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="ca9fc-172">Kredi mektubu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="ca9fc-173">Satırlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="ca9fc-174">Not: 'Gönderilen belge' alanı 'Evet' olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="ca9fc-175">İhracat kredi mektubunu onaylayın</span><span class="sxs-lookup"><span data-stu-id="ca9fc-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="ca9fc-176">Nakit ve Banka yönetimi > Kredi mektupları > İhracat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="ca9fc-177">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ca9fc-178">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ca9fc-179">Ihracat kredi mektubu sevkiyat durumunun 'Faturalandı' olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="ca9fc-180">Müşteri ödemesi</span><span class="sxs-lookup"><span data-stu-id="ca9fc-180">Customer payment</span></span>
1. <span data-ttu-id="ca9fc-181">Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ca9fc-182">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-182">Click New.</span></span>
3. <span data-ttu-id="ca9fc-183">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ca9fc-184">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ca9fc-185">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ca9fc-186">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-186">Click Lines.</span></span>
7. <span data-ttu-id="ca9fc-187">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="ca9fc-188">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="ca9fc-189">Kapatma öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-189">Click Settlement.</span></span>
10. <span data-ttu-id="ca9fc-190">Toplam başlığındaki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="ca9fc-191">Not: Göster alanını 'Kredi mektubu' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="ca9fc-192">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ca9fc-193">İşaret onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="ca9fc-194">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-194">Click OK.</span></span>
14. <span data-ttu-id="ca9fc-195">Ödeme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="ca9fc-196">Banka belge numarası ve sevk irsaliyesi numarası ayrıntılarını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="ca9fc-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="ca9fc-197">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="ca9fc-198">İhracat kredi mektubunu ödeme sonrasında doğrulayın</span><span class="sxs-lookup"><span data-stu-id="ca9fc-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="ca9fc-199">Nakit ve Banka yönetimi > Kredi mektupları > İhracat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="ca9fc-200">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ca9fc-201">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ca9fc-202">Sevkiyat durumu'nun = Ödeme alındı ve bakiye tutarı'nın = 0,00 olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

