---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 2 - İşlemleri yapılandırma)
description: Bu konuda, önceden oluşturulmuş metin çıktısının verilerine dayalı olarak sayma ve toplama işlemi yapmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (2. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565178"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="27848-104">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 2 - İşlemleri yapılandırma)</span><span class="sxs-lookup"><span data-stu-id="27848-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27848-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="27848-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="27848-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="27848-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="27848-107">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 1): Biçim oluşturma" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="27848-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="27848-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="27848-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="27848-109">Sayım ve toplama ayrıntıları eklemek için bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="27848-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="27848-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="27848-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="27848-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="27848-112">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="27848-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="27848-113">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="27848-114">Microsoft tarafından sağlanan biçimi, Intrastat raporunun sonunda özet ayrıntıları olan satırlar ekleyerek özelleştirmeniz gerektiğini varsayalım.</span><span class="sxs-lookup"><span data-stu-id="27848-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="27848-115">Değişiklikler yapabilmek için bunu kendi Intrastat yapılandırmanızı Microsoft örneğinden türeterek yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="27848-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="27848-116">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="27848-117">Yeni alanında "İsimden Türet: Intrastat (DE), Microsoft" girin.</span><span class="sxs-lookup"><span data-stu-id="27848-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="27848-118">Ad alanında "Sayım ve toplama ile Intrastat (DE)" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="27848-119">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="27848-120">Çıkış ayrıntılarına göre sayım ve toplama yapmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="27848-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="27848-121">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-121">Click Designer.</span></span>
2. <span data-ttu-id="27848-122">Çıkış ayrıntılarını topla alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="27848-123">Bu bayrak, Intrastat dosyası oluşturmak için çıktı ayrıntılarını toplama işlemini çalışma zamanında etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="27848-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="27848-124">Farklı Intrastat yönleri için sayım yapmanız gerekir. Bu nedenle, bu biçim yapılandırmasının veri kaynakları listesine özel model numaralandırması ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27848-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="27848-125">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="27848-126">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="27848-127">Ağaçta, "Veri modeli\Numaralandırma" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="27848-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="27848-128">Ad alanına "Yön" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="27848-129">Model numaralandırma alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="27848-130">Değer olarak Yön'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="27848-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-131">Click OK.</span></span>
9. <span data-ttu-id="27848-132">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="27848-133">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="27848-134">Ad alanına, '$BlockName' yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="27848-135">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-135">Click Edit formula.</span></span>
13. <span data-ttu-id="27848-136">Formül alanına "blok" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="27848-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-137">Click Save.</span></span>
15. <span data-ttu-id="27848-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-138">Close the page.</span></span>
16. <span data-ttu-id="27848-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-139">Click OK.</span></span>
17. <span data-ttu-id="27848-140">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="27848-141">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="27848-142">Ad alanına "$RecName" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="27848-143">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-143">Click Edit formula.</span></span>
21. <span data-ttu-id="27848-144">Formül alanına "kayıt" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="27848-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-145">Click Save.</span></span>
23. <span data-ttu-id="27848-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-146">Close the page.</span></span>
24. <span data-ttu-id="27848-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-147">Click OK.</span></span>
25. <span data-ttu-id="27848-148">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="27848-149">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="27848-150">Ad alanına "$InvName" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="27848-151">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-151">Click Edit formula.</span></span>
29. <span data-ttu-id="27848-152">Formül alanına "InvoicedAmountEUR" yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="27848-153">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-153">Click Save.</span></span>
31. <span data-ttu-id="27848-154">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-154">Close the page.</span></span>
32. <span data-ttu-id="27848-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-155">Click OK.</span></span>
33. <span data-ttu-id="27848-156">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="27848-157">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="27848-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="27848-158">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-158">Click Add data source.</span></span>
    * <span data-ttu-id="27848-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="27848-159">$BlockName</span></span>  
36. <span data-ttu-id="27848-160">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-160">Click Save.</span></span>
37. <span data-ttu-id="27848-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-161">Close the page.</span></span>
38. <span data-ttu-id="27848-162">Toplanan veri anahtarı değeri alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="27848-163">Formül alanına, "EĞER(Intrastat.CommodityRecord.Direction=Direction.Import, "İthalat", "İhracat")' yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="27848-164">EĞER(Intrastat.CommodityRecord.Direction=Direction.Import, "İthalat", "İhracat")</span><span class="sxs-lookup"><span data-stu-id="27848-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="27848-165">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-165">Click Save.</span></span>
41. <span data-ttu-id="27848-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-166">Close the page.</span></span>
    * <span data-ttu-id="27848-167">Bu dizinin satırlarını sayın.</span><span class="sxs-lookup"><span data-stu-id="27848-167">Count the lines of this sequence.</span></span> <span data-ttu-id="27848-168">Sonuçlar, farklı yönler için ayrı ayrı "blok" adıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27848-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="27848-169">Her varış Intrastat hareketi için "İthalat" değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27848-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="27848-170">Her sevk Intrastat hareketi için "İhracat" değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27848-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="27848-171">Bunu sanal bir Excel elektronik tablosu olarak düşünün.</span><span class="sxs-lookup"><span data-stu-id="27848-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="27848-172">Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="27848-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="27848-173">Ağaçta "Intrastat\Veri:Sıra" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="27848-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="27848-174">Ağaçta, "Intrastat\Veri:Sıra\Gelen?" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="27848-175">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="27848-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="27848-176">Bu dizinin satırlarını sayın.</span><span class="sxs-lookup"><span data-stu-id="27848-176">Count the lines of this sequence.</span></span> <span data-ttu-id="27848-177">Sonuçlar "kayıt" adı kullanılarak belleğe alınır.</span><span class="sxs-lookup"><span data-stu-id="27848-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="27848-178">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="27848-179">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-179">Click Add data source.</span></span>
47. <span data-ttu-id="27848-180">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-180">Click Save.</span></span>
48. <span data-ttu-id="27848-181">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-181">Close the page.</span></span>
49. <span data-ttu-id="27848-182">"Toplanan veri anahtarı değeri" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="27848-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="27848-183">Formül alanına, 'Intrastat.CommodityRecord.CommodityCode' yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="27848-184">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-184">Click Save.</span></span>
52. <span data-ttu-id="27848-185">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-185">Close the page.</span></span>
    * <span data-ttu-id="27848-186">Bu dizinin satırlarını sayın.</span><span class="sxs-lookup"><span data-stu-id="27848-186">Count the lines of this sequence.</span></span> <span data-ttu-id="27848-187">Sonuçlar, farklı emtia kodları için ayrı ayrı "kayıt" adıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27848-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="27848-188">Bunu sanal bir Excel elektronik tablosu olarak düşünün.</span><span class="sxs-lookup"><span data-stu-id="27848-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="27848-189">Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur ve ikinci "kayıt" bloğu emtia kodu değeri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="27848-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="27848-190">Ağaçta, "Intrastat\Veri:Sıra\Sevkler?" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="27848-191">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="27848-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="27848-192">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="27848-193">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-193">Click Add data source.</span></span>
57. <span data-ttu-id="27848-194">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-194">Click Save.</span></span>
58. <span data-ttu-id="27848-195">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-195">Close the page.</span></span>
59. <span data-ttu-id="27848-196">"Toplanan veri anahtarı değeri" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="27848-197">Formül alanına, 'Intrastat.CommodityRecord.CommodityCode' yazın.</span><span class="sxs-lookup"><span data-stu-id="27848-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="27848-198">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-198">Click Save.</span></span>
62. <span data-ttu-id="27848-199">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-199">Close the page.</span></span>
63. <span data-ttu-id="27848-200">Ağaçta, "Intrastat\Veri:Sıra\Sevkler:Sıra?" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="27848-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="27848-201">Ağaçta "Intrastat\Veri:Sıra\Sevkler:Sıra?\Kayıt =  Intrastat.CommodityRecord" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="27848-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="27848-202">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-202">Click the Format tab.</span></span>
66. <span data-ttu-id="27848-203">Ağaçta, "Intrastat\Veri\Sevkler\Kayıt\Fatura tutarı EUR" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="27848-204">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="27848-205">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="27848-206">Ağaçta, "$InvName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="27848-207">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-207">Click Add data source.</span></span>
71. <span data-ttu-id="27848-208">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-208">Click Save.</span></span>
72. <span data-ttu-id="27848-209">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-209">Close the page.</span></span>
    * <span data-ttu-id="27848-210">Bu dizinin satırları için faturalanan tutar değerlerini özetleyin.</span><span class="sxs-lookup"><span data-stu-id="27848-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="27848-211">Sonuçlar, farklı Intrastat yönleri ve emtia kodları için ayrı ayrı "InvoicedAmountEUR" adıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27848-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="27848-212">Bunu, Excel elektronik tablosunda sanal bir oluşturma olarak düşünün.</span><span class="sxs-lookup"><span data-stu-id="27848-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="27848-213">Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="27848-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="27848-214">İkinci "kayıt" bloğu emtia kodu değeri ile doldurulur ve üçüncü "InvoicedAmountEUR" bloğu fatura tutarı değeri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="27848-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="27848-215">Ağaçta "Intrastat\Veri\Gelen?" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="27848-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="27848-216">Ağaçta, "Intrastat\Veri\Gelen?\Kayıt =  Intrastat.CommodityRecord" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="27848-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="27848-217">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-217">Click the Format tab.</span></span>
76. <span data-ttu-id="27848-218">Ağaçta, "Intrastat\Veri\Gelen\Kayıt\Fatura tutarı EUR" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="27848-219">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27848-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="27848-220">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="27848-221">Ağaçta, "$InvName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27848-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="27848-222">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-222">Click Add data source.</span></span>
81. <span data-ttu-id="27848-223">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-223">Click Save.</span></span>
82. <span data-ttu-id="27848-224">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-224">Close the page.</span></span>
83. <span data-ttu-id="27848-225">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27848-225">Click Save.</span></span>
84. <span data-ttu-id="27848-226">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27848-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]