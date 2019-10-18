---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 2 - Model eşleme)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eedb8321b43ab5f5d9cb56166b68d6e9508c104f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182474"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a><span data-ttu-id="13e5e-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 2: Model eşleme)</span><span class="sxs-lookup"><span data-stu-id="13e5e-103">ER Use financial dimensions as a data source (Part 2: Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13e5e-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="13e5e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="13e5e-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="13e5e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="13e5e-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 1: Veri modeli tasarlama)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="13e5e-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="13e5e-107">Gerekli veri kaynaklarını model eşlemeye ekleme</span><span class="sxs-lookup"><span data-stu-id="13e5e-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="13e5e-108">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="13e5e-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="13e5e-109">Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="13e5e-110">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-110">Click Designer.</span></span>
4. <span data-ttu-id="13e5e-111">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="13e5e-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-112">Click New.</span></span>
6. <span data-ttu-id="13e5e-113">Tanım alanında Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="13e5e-114">Ad alanına 'Boyut verileri eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="13e5e-115">Açıklama alanına 'Boyut verileri eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="13e5e-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-116">Click Save.</span></span>
10. <span data-ttu-id="13e5e-117">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-117">Click Designer.</span></span>
11. <span data-ttu-id="13e5e-118">Ağaçta, 'Dynamics 365 for Operations\Tablo' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="13e5e-119">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-119">Click Add root.</span></span>
13. <span data-ttu-id="13e5e-120">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="13e5e-121">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="13e5e-122">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-122">Click OK.</span></span>
16. <span data-ttu-id="13e5e-123">Ağaçta, 'İşlevler\Mali boyutların ayrıntıları' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="13e5e-124">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-124">Click Add root.</span></span>
    * <span data-ttu-id="13e5e-125">Bu veri kaynağı, mali boyutların kapsamının veri kaynağı olarak bu modeli kullanacak tüm raporlar için nasıl tanımlanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13e5e-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="13e5e-126">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="13e5e-127">Boyutları iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="13e5e-128">Kullanıcının Kullanıcı iletişim formunda çalışma zamanında boyutları seçmesine izin vermek için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="13e5e-129">Bu seçenek Hayır olarak ayarlandığında, geçerli kurulumun tüm mali boyutları varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="13e5e-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="13e5e-130">Mali boyutlar seçimi alanında, 'Tüzel kişilik'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="13e5e-131">Kullanıcının Arama alanında geçerli kurulum için istenen boyutları seçmesine izin vermek için Tümü'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="13e5e-132">Kullanıcının Arama alanında şirket için istenen boyutları seçmesine izin vermek için Tüzel kişilik'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="13e5e-133">Kullanıcının tek bir boyut kümesi kullanan boyutları seçmesine izin vermek için Boyut'u seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="13e5e-134">Ana hesap iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="13e5e-135">Kullanıcıların ana hesabı boyutlar listesinin bir parçası olarak seçmesine izin vermek için 'Ana hesabı iste' seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="13e5e-136">Bu seçenek Hayır olarak ayarlandığında, ana hesap boyutlar listesine dahil edilmez ve 'Ana hesap zorunlu' seçeneği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="13e5e-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="13e5e-137">"Ana hesap zorunlu" seçeneği Evet olarak ayarlandığında, kullanıcının seçiminden bağımsız olarak, ana hesabı boyutlar listesine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="13e5e-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-138">Click OK.</span></span>
23. <span data-ttu-id="13e5e-139">Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="13e5e-140">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-140">Click Add root.</span></span>
25. <span data-ttu-id="13e5e-141">Ad alanına 'LedgerJournal' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="13e5e-142">Sorgu iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="13e5e-143">Tablo alanına 'LedgerJournalTable' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="13e5e-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="13e5e-145">Veri modeli öğelerini eklenen veri kaynaklarına eşleme</span><span class="sxs-lookup"><span data-stu-id="13e5e-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="13e5e-146">Ağaçta, 'Günlük' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="13e5e-147">Ağaçta, 'Günlük\Hareket' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="13e5e-148">Ağaçta, 'Günlük\Hareket\Boyut verileri' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="13e5e-149">Ağaçta, 'Boyutlar ayarı' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="13e5e-150">Ağaçta, 'LedgerJournal' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="13e5e-151">Ağaçta, 'LedgerJournal\<İlişkiler' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="13e5e-152">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="13e5e-153">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Fiş' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="13e5e-154">Ağaçta, 'Günlük\Hareket\Fiş' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="13e5e-155">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-155">Click Bind.</span></span>
11. <span data-ttu-id="13e5e-156">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="13e5e-157">Örneğin LedgerDimension olarak ayarlanmış mali boyutlara yapılan tüm referansları için bunlara karşılık gelen bir veri kaynağının (LedgerDimension.Dimension) bulunduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="13e5e-158">Bu veri kaynağı öğesi bu boyutlar kümesinin mali boyutlarını kaydın listesi olarak sunar.</span><span class="sxs-lookup"><span data-stu-id="13e5e-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="13e5e-159">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="13e5e-160">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="13e5e-161">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="13e5e-162">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Tanım' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="13e5e-163">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Tanım\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="13e5e-164">Ağaçta, 'Günlük\Hareket\Boyut verileri\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="13e5e-165">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-165">Click Bind.</span></span>
19. <span data-ttu-id="13e5e-166">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer\Açıklama' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="13e5e-167">Ağaçta, 'Günlük\Hareket\Boyut verileri\Açıklama' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="13e5e-168">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-168">Click Bind.</span></span>
22. <span data-ttu-id="13e5e-169">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer\Kod' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="13e5e-170">Ağaçta, 'Günlük\Hareket\Boyut verileri\Kod' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="13e5e-171">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-171">Click Bind.</span></span>
25. <span data-ttu-id="13e5e-172">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="13e5e-173">Ağaçta, 'Günlük\Hareket\Boyut verileri' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="13e5e-174">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-174">Click Bind.</span></span>
28. <span data-ttu-id="13e5e-175">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="13e5e-176">Ağaçta, 'Günlük\Hareket\Borç' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="13e5e-177">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-177">Click Bind.</span></span>
31. <span data-ttu-id="13e5e-178">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="13e5e-179">Ağaçta, 'Günlük\Hareket\Tarih' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="13e5e-180">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-180">Click Bind.</span></span>
34. <span data-ttu-id="13e5e-181">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="13e5e-182">Ağaçta, 'Günlük\Hareket\Para Birimi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="13e5e-183">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-183">Click Bind.</span></span>
37. <span data-ttu-id="13e5e-184">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="13e5e-185">Ağaçta, 'Günlük\Hareket\Alacak' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="13e5e-186">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-186">Click Bind.</span></span>
40. <span data-ttu-id="13e5e-187">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="13e5e-188">Ağaçta, 'Günlük\Hareket' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="13e5e-189">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-189">Click Bind.</span></span>
43. <span data-ttu-id="13e5e-190">Ağaçta, 'LedgerJournal\Günlük toplu iş numarası (JournalNum)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="13e5e-191">Ağaçta, 'Günlük\Toplu İş' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="13e5e-192">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-192">Click Bind.</span></span>
46. <span data-ttu-id="13e5e-193">Ağaçta, 'LedgerJournal' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="13e5e-194">Ağaçta, 'Günlük' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="13e5e-195">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-195">Click Bind.</span></span>
49. <span data-ttu-id="13e5e-196">Ağaçta, 'Boyutlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="13e5e-197">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="13e5e-198">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="13e5e-199">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="13e5e-200">Ağaçta, 'Boyutlar ayarı\Kod' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="13e5e-201">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-201">Click Bind.</span></span>
55. <span data-ttu-id="13e5e-202">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım\Rapor sütunu adı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="13e5e-203">Ağaçta, 'Boyutlar ayarı\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="13e5e-204">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-204">Click Bind.</span></span>
58. <span data-ttu-id="13e5e-205">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="13e5e-206">Ağaçta, 'Boyutlar ayarı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="13e5e-207">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-207">Click Bind.</span></span>
61. <span data-ttu-id="13e5e-208">Ağaçta, 'Şirket' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13e5e-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="13e5e-209">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-209">Click Edit.</span></span>
63. <span data-ttu-id="13e5e-210">expressionAsStringText alanına 'Company.'find()'.'name()'' yazın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="13e5e-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="13e5e-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="13e5e-212">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-212">Click Save.</span></span>
65. <span data-ttu-id="13e5e-213">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-213">Close the page.</span></span>
66. <span data-ttu-id="13e5e-214">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-214">Click Save.</span></span>
67. <span data-ttu-id="13e5e-215">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="13e5e-216">Bu taslak modelin sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="13e5e-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="13e5e-217">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-217">Close the page.</span></span>
2. <span data-ttu-id="13e5e-218">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-218">Close the page.</span></span>
3. <span data-ttu-id="13e5e-219">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-219">Click Change status.</span></span>
4. <span data-ttu-id="13e5e-220">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-220">Click Complete.</span></span>
5. <span data-ttu-id="13e5e-221">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13e5e-221">Click OK.</span></span>

