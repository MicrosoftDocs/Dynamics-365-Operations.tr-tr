--- 
title: "ER model eşlemelerini tanımlama ve bunlar için veri kaynaklarını seçme"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının bir Elektronik Raporlama (ER) veri modeli için veri kaynaklar seçebilir."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 2beda3555274fee3f17ad13c54c6823307216385
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="bab94-103">ER model eşlemelerini tanımlama ve bunlar için veri kaynaklarını seçme</span><span class="sxs-lookup"><span data-stu-id="bab94-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bab94-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının bir Elektronik Raporlama (ER) veri modeli için veri kaynaklar seçebilir.</span><span class="sxs-lookup"><span data-stu-id="bab94-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="bab94-105">Veri kaynakları, tasarım zamanında seçilen veri modelinin ayrı ayrı bileşenlerine bağlanır ve çalışma süresinde bu veri modeli için iş verilerini doldurur.</span><span class="sxs-lookup"><span data-stu-id="bab94-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="bab94-106">Bu örnekte, Litware, Inc. örnek şirketi için oluşturulan, mevcut bir veri modeli için veri kaynaklarını seçeceksiniz. Bu adımları tamamlamak için öncelikle "Yeni veri modeli oluştur" prosedürü altındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bab94-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="bab94-107">Elektronik Raporlama yapılandırmaları ağacını açın</span><span class="sxs-lookup"><span data-stu-id="bab94-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="bab94-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="bab94-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="bab94-109">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="bab94-110">Yeni bir model eşlemesi ekle</span><span class="sxs-lookup"><span data-stu-id="bab94-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="bab94-111">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="bab94-112">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-112">Click Designer.</span></span>
3. <span data-ttu-id="bab94-113">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="bab94-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-114">Click New.</span></span>
    * <span data-ttu-id="bab94-115">Bu, veri kaynaklarına bir veri modeli eşlemek için yeni bir kayıt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bab94-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="bab94-116">Bu örnekte tercih edilen ödeme türü olan Kredi transferi için veri kaynaklarına veri modelinin eşlemesin yapacaksınız.</span><span class="sxs-lookup"><span data-stu-id="bab94-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="bab94-117">Belirli bir veri modeli için birden fazla eşleme tasarlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="bab94-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="bab94-118">Örneğin, doğrudan borç veya kredi transferi gibi farklı ödeme türleri için eşlemeler oluşturacaktınız.</span><span class="sxs-lookup"><span data-stu-id="bab94-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="bab94-119">Bu örnekte, kredi transferleri için bir eşleme oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="bab94-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="bab94-120">İsim alanına 'CT eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="bab94-121">CT eşleme</span><span class="sxs-lookup"><span data-stu-id="bab94-121">CT mapping</span></span>  
6. <span data-ttu-id="bab94-122">Açıklama alanına, 'ödeme modeli CT eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="bab94-123">Ödeme modeli CT eşleme</span><span class="sxs-lookup"><span data-stu-id="bab94-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="bab94-124">Tanım alanına, "CustomerCreditTransferInitiation" yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="bab94-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="bab94-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="bab94-126">Tanımı ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="bab94-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="bab94-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="bab94-128">Geçerli model eşleme için gereken veri kaynaklarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="bab94-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="bab94-129">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-129">Click Designer.</span></span>
2. <span data-ttu-id="bab94-130">Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="bab94-131">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-131">Click Add root.</span></span>
    * <span data-ttu-id="bab94-132">Ödeme hareketlerine erişmek için bu veri kaynağı girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="bab94-133">İsim alanına, 'Hareketler' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="bab94-134">Hareketler</span><span class="sxs-lookup"><span data-stu-id="bab94-134">Transactions</span></span>  
5. <span data-ttu-id="bab94-135">Etiket alanına "Hareketler" girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="bab94-136">Hareketler</span><span class="sxs-lookup"><span data-stu-id="bab94-136">Transactions</span></span>  
6. <span data-ttu-id="bab94-137">Yardım alanına 'Genel muhasebe günlük satırları' girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="bab94-138">Genel muhasebe günlüğü satırları</span><span class="sxs-lookup"><span data-stu-id="bab94-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="bab94-139">Sorgu iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="bab94-140">Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-140">Select Yes.</span></span>  
8. <span data-ttu-id="bab94-141">Tablo alanına 'LedgerJournalTrans' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="bab94-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="bab94-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="bab94-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-143">Click OK.</span></span>
    * <span data-ttu-id="bab94-144">Geçerli veri modeli için bir veri kaynağı olarak LedgerJournalTrans tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="bab94-145">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="bab94-146">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-146">Click Add.</span></span>
    * <span data-ttu-id="bab94-147">Yeni bir hesaplanmış alan eklemek için Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="bab94-148">İsim alanına '$EndToEndID' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="bab94-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="bab94-149">$EndToEndID</span></span>  
13. <span data-ttu-id="bab94-150">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-150">Click Edit formula.</span></span>
14. <span data-ttu-id="bab94-151">Ağaçta 'String\CONCATENATE' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="bab94-152">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-152">Click Add function.</span></span>
16. <span data-ttu-id="bab94-153">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="bab94-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="bab94-154">Ağaçta, 'Transactions\Voucher' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="bab94-155">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-155">Click Add data source.</span></span>
19. <span data-ttu-id="bab94-156">Formül alanına "CONCATENATE(Transactions.Voucher, "-", " yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="bab94-157">Förmülün sonuna, [ , “-“, ] yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="bab94-158">Ağaçta 'String\TEXT' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="bab94-159">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-159">Click Add function.</span></span>
22. <span data-ttu-id="bab94-160">Ağaçta, 'Transactions\Record-ID(RecId)' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="bab94-161">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-161">Click Add data source.</span></span>
24. <span data-ttu-id="bab94-162">Formül alanına "CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))" yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="bab94-163">Formülün sonuna, [))] yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="bab94-164">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-164">Click Save.</span></span>
    * <span data-ttu-id="bab94-165">Oluşturulan formülde herhangi bir hata tespit edilmediğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="bab94-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="bab94-166">Formül düzenleyici denetimin altındaki HATALAR sekmesine bakın.</span><span class="sxs-lookup"><span data-stu-id="bab94-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="bab94-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-167">Close the page.</span></span>
27. <span data-ttu-id="bab94-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-168">Click OK.</span></span>
    * <span data-ttu-id="bab94-169">Bu veri kaynağına hesaplanan alan ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bab94-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="bab94-170">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-170">Click Add.</span></span>
    * <span data-ttu-id="bab94-171">Yeni bir hesaplanmış alan eklemek için Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="bab94-172">İsim alanına '$Amount' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="bab94-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="bab94-173">$Amount</span></span>  
30. <span data-ttu-id="bab94-174">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-174">Click Edit formula.</span></span>
31. <span data-ttu-id="bab94-175">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="bab94-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="bab94-176">Ağaçta, 'Transactions\Debit(AmountCurDebit)' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="bab94-177">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-177">Click Add data source.</span></span>
34. <span data-ttu-id="bab94-178">Formül alanına "Transactions.AmountCurDebit - " yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="bab94-179">Formün sonuna [ - ] yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="bab94-180">Ağaçta, 'Transactions\Credit(AmountCurCredit)' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="bab94-181">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-181">Click Add data source.</span></span>
37. <span data-ttu-id="bab94-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-182">Click Save.</span></span>
38. <span data-ttu-id="bab94-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-183">Close the page.</span></span>
39. <span data-ttu-id="bab94-184">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-184">Click OK.</span></span>
    * <span data-ttu-id="bab94-185">Bu, $Amount hesaplanan alanını, mevcut veri modeli için seçilen veri kaynağına ekleyecektir.</span><span class="sxs-lookup"><span data-stu-id="bab94-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="bab94-186">Ağaçta, 'Transactions\$Amount' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="bab94-187">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="bab94-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="bab94-188">Ağaçta, "Hareketler\$Tutar" öğesini genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="bab94-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="bab94-189">Ağaçta, "Hareketler" öğesini genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="bab94-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="bab94-190">Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="bab94-191">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-191">Click Add root.</span></span>
    * <span data-ttu-id="bab94-192">Şirketin banka hesap ayrıntılarına erişmek için bu veri kaynağı girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="bab94-193">İsim alanına 'BankAccount' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="bab94-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="bab94-194">BankAccount</span></span>  
47. <span data-ttu-id="bab94-195">Etiket alanına "Banka Hesabı" girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="bab94-196">Banka Hesabı</span><span class="sxs-lookup"><span data-stu-id="bab94-196">Bank Account</span></span>  
48. <span data-ttu-id="bab94-197">Yardım alanına "Banka Hesabı" girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="bab94-198">Banka Hesabı</span><span class="sxs-lookup"><span data-stu-id="bab94-198">Bank Account</span></span>  
49. <span data-ttu-id="bab94-199">Sorgu iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="bab94-200">Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-200">Select Yes.</span></span>  
50. <span data-ttu-id="bab94-201">Tablo alanına 'BankAccountTable' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="bab94-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="bab94-202">BankAccountTable</span></span>  
51. <span data-ttu-id="bab94-203">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-203">Click OK.</span></span>
    * <span data-ttu-id="bab94-204">Geçerli veri modeli için bir veri kaynağı olarak BankAccountTable tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="bab94-205">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-205">Click Add root.</span></span>
    * <span data-ttu-id="bab94-206">Şirketin koşullarına erişmek için bu veri kaynağı girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="bab94-207">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="bab94-208">Şirket</span><span class="sxs-lookup"><span data-stu-id="bab94-208">Company</span></span>  
54. <span data-ttu-id="bab94-209">Etiket alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="bab94-210">Şirket bilgileri</span><span class="sxs-lookup"><span data-stu-id="bab94-210">Company information</span></span>  
55. <span data-ttu-id="bab94-211">Yardım alanına 'Şirket bilgisi' girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="bab94-212">Şirket bilgileri</span><span class="sxs-lookup"><span data-stu-id="bab94-212">Company information</span></span>  
56. <span data-ttu-id="bab94-213">Sorgu iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="bab94-214">Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-214">Select Yes.</span></span>  
57. <span data-ttu-id="bab94-215">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="bab94-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="bab94-216">CompanyInfo</span></span>  
58. <span data-ttu-id="bab94-217">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-217">Click OK.</span></span>
    * <span data-ttu-id="bab94-218">Geçerli veri modeli için bir veri kaynağı olarak CompanyInfo tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="bab94-219">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="bab94-220">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-220">Click Add root.</span></span>
    * <span data-ttu-id="bab94-221">Hesaplanan bir alanı yeni bir veri kaynağı olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bab94-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="bab94-222">İsim alanına 'ProcessingDateTime' yazın.</span><span class="sxs-lookup"><span data-stu-id="bab94-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="bab94-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="bab94-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="bab94-224">Etiket alanına 'İşleme tarihi ve saati'ni girin.</span><span class="sxs-lookup"><span data-stu-id="bab94-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="bab94-225">İşleme tarihi ve saati</span><span class="sxs-lookup"><span data-stu-id="bab94-225">Processing date & time</span></span>  
63. <span data-ttu-id="bab94-226">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-226">Click Edit formula.</span></span>
64. <span data-ttu-id="bab94-227">Ağaçta, "Tarih saat\SESSIONNOW" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bab94-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="bab94-228">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-228">Click Add function.</span></span>
66. <span data-ttu-id="bab94-229">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-229">Click Save.</span></span>
67. <span data-ttu-id="bab94-230">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-230">Close the page.</span></span>
68. <span data-ttu-id="bab94-231">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-231">Click OK.</span></span>
    * <span data-ttu-id="bab94-232">Geçerli veri modeli için bir veri kaynağı olarak ProcessingDateTime hesaplanmış alanı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bab94-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="bab94-233">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bab94-233">Click Save.</span></span>
70. <span data-ttu-id="bab94-234">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-234">Close the page.</span></span>
71. <span data-ttu-id="bab94-235">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-235">Close the page.</span></span>
72. <span data-ttu-id="bab94-236">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bab94-236">Close the page.</span></span>


