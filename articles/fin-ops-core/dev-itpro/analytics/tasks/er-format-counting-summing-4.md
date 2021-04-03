---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 4 - Biçimi çalıştırma)
description: Bu konuda, önceden oluşturulmuş metin çıktısının verilerine dayalı olarak sayma ve toplama işlemi yapmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (4. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ca8449581edc06016b6e387880aad91087b67f1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565429"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="c21d1-104">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 4 - Biçimi çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="c21d1-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c21d1-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c21d1-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c21d1-106">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c21d1-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c21d1-107">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 3: Çıkış yapmak için hesaplamaları kullanma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="c21d1-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="c21d1-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="c21d1-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="c21d1-109">Intrastat raporlarını oluşturmak için bu yapılandırmayı sınama</span><span class="sxs-lookup"><span data-stu-id="c21d1-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="c21d1-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c21d1-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c21d1-112">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="c21d1-113">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="c21d1-114">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="c21d1-115">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="c21d1-116">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-116">Click User parameters.</span></span>
8. <span data-ttu-id="c21d1-117">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="c21d1-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-118">Click OK.</span></span>
10. <span data-ttu-id="c21d1-119">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-119">Click Edit.</span></span>
11. <span data-ttu-id="c21d1-120">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="c21d1-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-121">Click Save.</span></span>
13. <span data-ttu-id="c21d1-122">Vergi > Kurulum > Dış Ticaret > Dış Ticaret parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="c21d1-123">Elektronik raporlama bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="c21d1-124">“Sayım ve toplama ile Intrastat (DE)” yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="c21d1-125">“Sayım ve toplama ile Intrastat (DE)” yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="c21d1-126">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-126">Click Save.</span></span>
18. <span data-ttu-id="c21d1-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-127">Close the page.</span></span>
19. <span data-ttu-id="c21d1-128">Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="c21d1-129">Çıkış düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-129">Click Output.</span></span>
21. <span data-ttu-id="c21d1-130">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-130">Click Report.</span></span>
    * <span data-ttu-id="c21d1-131">Intrastat raporu oluşturma işlemini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="c21d1-132">Form tarihi alanında, tarihi '01-01-2000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="c21d1-133">Formda var olan hareketleri içeren raporlama döneminin başlangıç ve bitiş tarihlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="c21d1-134">Bitiş tarihi alanında tarihi "31.12.2022" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="c21d1-135">Formda var olan hareketleri içeren raporlama döneminin başlangıç ve bitiş tarihlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="c21d1-136">Yön alanında "Gelen öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="c21d1-137">Dosya oluştur alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="c21d1-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-138">Click OK.</span></span>
    * <span data-ttu-id="c21d1-139">Sondaki özet satırlarıyla oluşturulan çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="c21d1-140">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-140">Click New.</span></span>
28. <span data-ttu-id="c21d1-141">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="c21d1-142">Yön alanından "Sevkler" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="c21d1-143">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="c21d1-144">Emtia alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="c21d1-145">Ağırlığı "10" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="c21d1-146">Fatura tutarını "10.000" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="c21d1-147">İstatistiksel tutarı "10.000" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="c21d1-148">Çıkış düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-148">Click Output.</span></span>
36. <span data-ttu-id="c21d1-149">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-149">Click Report.</span></span>
37. <span data-ttu-id="c21d1-150">Yön alanından "Sevkler" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="c21d1-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-151">Click OK.</span></span>
    * <span data-ttu-id="c21d1-152">Sondaki özet satırlarıyla oluşturulan çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="c21d1-153">İlk çalıştırmayla karşılaştırıldığında değiştirildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="c21d1-154">Toplanan sayımı ve veri toplamayı gözden geçirmek için bu yapılandırmayı hata ayıklama modunda çalıştırma</span><span class="sxs-lookup"><span data-stu-id="c21d1-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="c21d1-155">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="c21d1-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c21d1-156">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="c21d1-157">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="c21d1-158">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="c21d1-159">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="c21d1-160">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-160">Click User parameters.</span></span>
7. <span data-ttu-id="c21d1-161">Hata ayıklama modunda çalıştır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="c21d1-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-162">Click OK.</span></span>
9. <span data-ttu-id="c21d1-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-163">Close the page.</span></span>
10. <span data-ttu-id="c21d1-164">Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="c21d1-165">Çıkış düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-165">Click Output.</span></span>
12. <span data-ttu-id="c21d1-166">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-166">Click Report.</span></span>
13. <span data-ttu-id="c21d1-167">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-167">Click OK.</span></span>
14. <span data-ttu-id="c21d1-168">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-168">Close the page.</span></span>
15. <span data-ttu-id="c21d1-169">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="c21d1-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="c21d1-170">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="c21d1-171">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="c21d1-172">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="c21d1-173">Hata ayıklama günlükleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-173">Click Debug logs.</span></span>
    * <span data-ttu-id="c21d1-174">Seçili yapılandırmanın yürütme işlemi için bir hata ayıklama günlüğü kaydı oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="c21d1-175">İliştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-175">Click Attach.</span></span>
21. <span data-ttu-id="c21d1-176">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c21d1-176">Click Open.</span></span>
    * <span data-ttu-id="c21d1-177">Seçili yapılandırmanın yürütmesi sırasında toplanan sayım ve toplama ayrıntılarını içeren, yeni oluşturulan XML dosyasını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c21d1-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]