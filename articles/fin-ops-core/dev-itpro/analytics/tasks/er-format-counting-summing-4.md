---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 4 - Biçimi çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f37fc3c611e9c5328f4d99be8c7c63ab59b2f08
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684655"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="99af4-103">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 4 - Biçimi çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="99af4-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99af4-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="99af4-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="99af4-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="99af4-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="99af4-106">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 3: Çıkış yapmak için hesaplamaları kullanma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="99af4-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="99af4-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="99af4-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="99af4-108">Intrastat raporlarını oluşturmak için bu yapılandırmayı sınama</span><span class="sxs-lookup"><span data-stu-id="99af4-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="99af4-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="99af4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="99af4-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="99af4-111">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="99af4-112">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="99af4-113">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="99af4-114">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="99af4-115">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-115">Click User parameters.</span></span>
8. <span data-ttu-id="99af4-116">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="99af4-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-117">Click OK.</span></span>
10. <span data-ttu-id="99af4-118">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-118">Click Edit.</span></span>
11. <span data-ttu-id="99af4-119">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="99af4-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-120">Click Save.</span></span>
13. <span data-ttu-id="99af4-121">Vergi > Kurulum > Dış Ticaret > Dış Ticaret parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99af4-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="99af4-122">Elektronik raporlama bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="99af4-123">“Sayım ve toplama ile Intrastat (DE)” yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-123">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="99af4-124">“Sayım ve toplama ile Intrastat (DE)” yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="99af4-125">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="99af4-125">Click Save.</span></span>
18. <span data-ttu-id="99af4-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99af4-126">Close the page.</span></span>
19. <span data-ttu-id="99af4-127">Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="99af4-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="99af4-128">Çıkış düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-128">Click Output.</span></span>
21. <span data-ttu-id="99af4-129">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-129">Click Report.</span></span>
    * <span data-ttu-id="99af4-130">Intrastat raporu oluşturma işlemini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="99af4-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="99af4-131">Form tarihi alanında, tarihi '01-01-2000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="99af4-132">Formda var olan hareketleri içeren raporlama döneminin başlangıç ve bitiş tarihlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="99af4-133">Bitiş tarihi alanında tarihi "31.12.2022" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="99af4-134">Formda var olan hareketleri içeren raporlama döneminin başlangıç ve bitiş tarihlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="99af4-135">Yön alanında "Gelen öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="99af4-136">Dosya oluştur alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="99af4-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-137">Click OK.</span></span>
    * <span data-ttu-id="99af4-138">Sondaki özet satırlarıyla oluşturulan çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="99af4-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="99af4-139">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-139">Click New.</span></span>
28. <span data-ttu-id="99af4-140">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="99af4-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="99af4-141">Yön alanından "Sevkler" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="99af4-142">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="99af4-143">Emtia alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="99af4-144">Ağırlığı "10" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="99af4-145">Fatura tutarını "10.000" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="99af4-146">İstatistiksel tutarı "10.000" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="99af4-147">Çıkış düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-147">Click Output.</span></span>
36. <span data-ttu-id="99af4-148">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-148">Click Report.</span></span>
37. <span data-ttu-id="99af4-149">Yön alanından "Sevkler" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="99af4-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-150">Click OK.</span></span>
    * <span data-ttu-id="99af4-151">Sondaki özet satırlarıyla oluşturulan çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="99af4-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="99af4-152">İlk çalıştırmayla karşılaştırıldığında değiştirildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="99af4-153">Toplanan sayımı ve veri toplamayı gözden geçirmek için bu yapılandırmayı hata ayıklama modunda çalıştırma</span><span class="sxs-lookup"><span data-stu-id="99af4-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="99af4-154">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="99af4-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="99af4-155">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="99af4-156">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="99af4-157">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="99af4-158">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="99af4-159">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-159">Click User parameters.</span></span>
7. <span data-ttu-id="99af4-160">Hata ayıklama modunda çalıştır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="99af4-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-161">Click OK.</span></span>
9. <span data-ttu-id="99af4-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99af4-162">Close the page.</span></span>
10. <span data-ttu-id="99af4-163">Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="99af4-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="99af4-164">Çıkış düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-164">Click Output.</span></span>
12. <span data-ttu-id="99af4-165">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-165">Click Report.</span></span>
13. <span data-ttu-id="99af4-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-166">Click OK.</span></span>
14. <span data-ttu-id="99af4-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99af4-167">Close the page.</span></span>
15. <span data-ttu-id="99af4-168">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="99af4-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="99af4-169">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="99af4-170">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="99af4-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="99af4-171">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99af4-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="99af4-172">Hata ayıklama günlükleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-172">Click Debug logs.</span></span>
    * <span data-ttu-id="99af4-173">Seçili yapılandırmanın yürütme işlemi için bir hata ayıklama günlüğü kaydı oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="99af4-174">İliştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-174">Click Attach.</span></span>
21. <span data-ttu-id="99af4-175">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99af4-175">Click Open.</span></span>
    * <span data-ttu-id="99af4-176">Seçili yapılandırmanın yürütmesi sırasında toplanan sayım ve toplama ayrıntılarını içeren, yeni oluşturulan XML dosyasını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="99af4-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

