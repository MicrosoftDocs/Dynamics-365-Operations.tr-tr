---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 2 - Model eşleme)
description: Bu konuda, ER raporları için veri kaynağı olarak mali boyutları kullanmak üzere Elektronik raporlama (ER) modelinin nasıl yapılandırılacağı açıklanmaktadır. (2. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093249"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="c8ac8-104">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 2 - Model eşleme)</span><span class="sxs-lookup"><span data-stu-id="c8ac8-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8ac8-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c8ac8-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="c8ac8-107">Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 1: Veri modeli tasarlama)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="c8ac8-108">Gerekli veri kaynaklarını model eşlemeye ekleme</span><span class="sxs-lookup"><span data-stu-id="c8ac8-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="c8ac8-109">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c8ac8-110">Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c8ac8-111">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-111">Click Designer.</span></span>
4. <span data-ttu-id="c8ac8-112">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="c8ac8-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-113">Click New.</span></span>
6. <span data-ttu-id="c8ac8-114">Tanım alanında Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="c8ac8-115">Ad alanına 'Boyut verileri eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="c8ac8-116">Açıklama alanına 'Boyut verileri eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="c8ac8-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-117">Click Save.</span></span>
10. <span data-ttu-id="c8ac8-118">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-118">Click Designer.</span></span>
11. <span data-ttu-id="c8ac8-119">Ağaçta, 'Dynamics 365 for Operations\Tablo' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="c8ac8-120">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-120">Click Add root.</span></span>
13. <span data-ttu-id="c8ac8-121">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="c8ac8-122">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="c8ac8-123">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-123">Click OK.</span></span>
16. <span data-ttu-id="c8ac8-124">Ağaçta, 'İşlevler\Mali boyutların ayrıntıları' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="c8ac8-125">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-125">Click Add root.</span></span>
    * <span data-ttu-id="c8ac8-126">Bu veri kaynağı, mali boyutların kapsamının veri kaynağı olarak bu modeli kullanacak tüm raporlar için nasıl tanımlanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="c8ac8-127">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="c8ac8-128">Boyutları iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="c8ac8-129">Kullanıcının Kullanıcı iletişim formunda çalışma zamanında boyutları seçmesine izin vermek için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="c8ac8-130">Bu seçenek Hayır olarak ayarlandığında, geçerli kurulumun tüm mali boyutları varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="c8ac8-131">Mali boyutlar seçimi alanında, 'Tüzel kişilik'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="c8ac8-132">Kullanıcının Arama alanında geçerli kurulum için istenen boyutları seçmesine izin vermek için Tümü'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="c8ac8-133">Kullanıcının Arama alanında şirket için istenen boyutları seçmesine izin vermek için Tüzel kişilik'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="c8ac8-134">Kullanıcının tek bir boyut kümesi kullanan boyutları seçmesine izin vermek için Boyut'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="c8ac8-135">Ana hesap iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="c8ac8-136">Kullanıcıların ana hesabı boyutlar listesinin bir parçası olarak seçmesine izin vermek için 'Ana hesabı iste' seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="c8ac8-137">Bu seçenek Hayır olarak ayarlandığında, ana hesap boyutlar listesine dahil edilmez ve 'Ana hesap zorunlu' seçeneği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="c8ac8-138">"Ana hesap zorunlu" seçeneği Evet olarak ayarlandığında, kullanıcının seçiminden bağımsız olarak, ana hesabı boyutlar listesine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="c8ac8-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-139">Click OK.</span></span>
<span data-ttu-id="c8ac8-140">![ER model eşleme tasarımcısı sayfası](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="c8ac8-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="c8ac8-141">Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="c8ac8-142">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-142">Click Add root.</span></span>
25. <span data-ttu-id="c8ac8-143">Ad alanına 'LedgerJournal' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="c8ac8-144">Sorgu iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="c8ac8-145">Tablo alanına 'LedgerJournalTable' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="c8ac8-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-146">Click OK.</span></span>
<span data-ttu-id="c8ac8-147">![ER model eşleme tasarımcısı sayfası](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="c8ac8-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="c8ac8-148">Veri modeli öğelerini eklenen veri kaynaklarına eşleme</span><span class="sxs-lookup"><span data-stu-id="c8ac8-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="c8ac8-149">Ağaçta, 'Günlük' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="c8ac8-150">Ağaçta, 'Günlük\Hareket' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="c8ac8-151">Ağaçta, 'Günlük\Hareket\Boyut verileri' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="c8ac8-152">Ağaçta, 'Boyutlar ayarı' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="c8ac8-153">Ağaçta, 'LedgerJournal' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="c8ac8-154">Ağaçta, 'LedgerJournal\<İlişkiler' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="c8ac8-155">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="c8ac8-156">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Fiş' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="c8ac8-157">Ağaçta, 'Günlük\Hareket\Fiş' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="c8ac8-158">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-158">Click Bind.</span></span>
11. <span data-ttu-id="c8ac8-159">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="c8ac8-160">Örneğin LedgerDimension olarak ayarlanmış mali boyutlara yapılan tüm referansları için bunlara karşılık gelen bir veri kaynağının (LedgerDimension.Dimension) bulunduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="c8ac8-161">Bu veri kaynağı öğesi bu boyutlar kümesinin mali boyutlarını kaydın listesi olarak sunar.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="c8ac8-162">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="c8ac8-163">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="c8ac8-164">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="c8ac8-165">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Tanım' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="c8ac8-166">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Tanım\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="c8ac8-167">Ağaçta, 'Günlük\Hareket\Boyut verileri\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="c8ac8-168">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-168">Click Bind.</span></span>
19. <span data-ttu-id="c8ac8-169">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer\Açıklama' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="c8ac8-170">Ağaçta, 'Günlük\Hareket\Boyut verileri\Açıklama' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="c8ac8-171">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-171">Click Bind.</span></span>
22. <span data-ttu-id="c8ac8-172">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar\Değer\Kod' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="c8ac8-173">Ağaçta, 'Günlük\Hareket\Boyut verileri\Kod' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="c8ac8-174">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-174">Click Bind.</span></span>
25. <span data-ttu-id="c8ac8-175">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Ana hesap ve boyutlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="c8ac8-176">Ağaçta, 'Günlük\Hareket\Boyut verileri' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="c8ac8-177">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-177">Click Bind.</span></span>
<span data-ttu-id="c8ac8-178">![ER model eşleme tasarımcısı sayfası](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="c8ac8-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="c8ac8-179">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="c8ac8-180">Ağaçta, 'Günlük\Hareket\Borç' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="c8ac8-181">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-181">Click Bind.</span></span>
31. <span data-ttu-id="c8ac8-182">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="c8ac8-183">Ağaçta, 'Günlük\Hareket\Tarih' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="c8ac8-184">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-184">Click Bind.</span></span>
34. <span data-ttu-id="c8ac8-185">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="c8ac8-186">Ağaçta, 'Günlük\Hareket\Para Birimi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="c8ac8-187">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-187">Click Bind.</span></span>
37. <span data-ttu-id="c8ac8-188">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="c8ac8-189">Ağaçta, 'Günlük\Hareket\Alacak' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="c8ac8-190">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-190">Click Bind.</span></span>
40. <span data-ttu-id="c8ac8-191">Ağaçta, 'LedgerJournal\<Relations\LedgerJournalTrans' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="c8ac8-192">Ağaçta, 'Günlük\Hareket' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="c8ac8-193">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-193">Click Bind.</span></span>
43. <span data-ttu-id="c8ac8-194">Ağaçta, 'LedgerJournal\Günlük toplu iş numarası (JournalNum)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="c8ac8-195">Ağaçta, 'Günlük\Toplu İş' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="c8ac8-196">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-196">Click Bind.</span></span>
46. <span data-ttu-id="c8ac8-197">Ağaçta, 'LedgerJournal' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="c8ac8-198">Ağaçta, 'Günlük' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="c8ac8-199">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-199">Click Bind.</span></span>
49. <span data-ttu-id="c8ac8-200">Ağaçta, 'Boyutlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="c8ac8-201">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="c8ac8-202">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="c8ac8-203">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="c8ac8-204">Ağaçta, 'Boyutlar ayarı\Kod' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="c8ac8-205">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-205">Click Bind.</span></span>
55. <span data-ttu-id="c8ac8-206">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar\Tanım\Rapor sütunu adı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="c8ac8-207">Ağaçta, 'Boyutlar ayarı\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="c8ac8-208">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-208">Click Bind.</span></span>
58. <span data-ttu-id="c8ac8-209">Ağaçta, 'Boyutlar\Ana hesap ve boyutlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="c8ac8-210">Ağaçta, 'Boyutlar ayarı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="c8ac8-211">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-211">Click Bind.</span></span>
61. <span data-ttu-id="c8ac8-212">Ağaçta, 'Şirket' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="c8ac8-213">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-213">Click Edit.</span></span>
63. <span data-ttu-id="c8ac8-214">expressionAsStringText alanına 'Company.'find()'.'name()'' yazın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="c8ac8-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="c8ac8-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="c8ac8-216">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-216">Click Save.</span></span>
<span data-ttu-id="c8ac8-217">![ER model eşleme tasarımcısı sayfası](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="c8ac8-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="c8ac8-218">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-218">Close the page.</span></span>
66. <span data-ttu-id="c8ac8-219">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-219">Click Save.</span></span>
67. <span data-ttu-id="c8ac8-220">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="c8ac8-221">Bu taslak modelin sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="c8ac8-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="c8ac8-222">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-222">Close the page.</span></span>
2. <span data-ttu-id="c8ac8-223">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-223">Close the page.</span></span>
3. <span data-ttu-id="c8ac8-224">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-224">Click Change status.</span></span>
4. <span data-ttu-id="c8ac8-225">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-225">Click Complete.</span></span>
5. <span data-ttu-id="c8ac8-226">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-226">Click OK.</span></span>
<span data-ttu-id="c8ac8-227">![ER model eşleme tasarımcısı sayfası](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="c8ac8-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
