--- 
title: "Elektronik raporlamada (ER) sayım ve toplama yapmak için hesaplamaları yapılandırma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7b9035d8e7baf3c7ecb063b104b9a567be60840
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="configure-computations-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="877a9-103">Elektronik raporlamada (ER) sayım ve toplama yapmak için hesaplamaları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="877a9-103">Configure computations to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="877a9-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="877a9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="877a9-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="877a9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="877a9-106">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 1): Biçim oluşturma" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="877a9-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="877a9-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="877a9-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="877a9-108">Sayım ve toplama ayrıntıları eklemek için bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="877a9-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="877a9-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="877a9-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="877a9-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="877a9-111">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="877a9-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="877a9-112">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="877a9-113">Microsoft tarafından sağlanan biçimi, Intrastat raporunun sonunda özet ayrıntıları olan satırlar ekleyerek özelleştirmeniz gerektiğini varsayalım.</span><span class="sxs-lookup"><span data-stu-id="877a9-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="877a9-114">Değişiklikler yapabilmek için bunu kendi Intrastat yapılandırmanızı Microsoft örneğinden türeterek yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="877a9-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="877a9-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="877a9-116">Yeni alanında "İsimden Türet: Intrastat (DE), Microsoft" girin.</span><span class="sxs-lookup"><span data-stu-id="877a9-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="877a9-117">Ad alanında "Sayım ve toplama ile Intrastat (DE)" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="877a9-118">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="877a9-119">Çıkış ayrıntılarına göre sayım ve toplama yapmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="877a9-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="877a9-120">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-120">Click Designer.</span></span>
2. <span data-ttu-id="877a9-121">Çıkış ayrıntılarını topla alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="877a9-122">Bu bayrak, Intrastat dosyası oluşturmak için çıktı ayrıntılarını toplama işlemini çalışma zamanında etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="877a9-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="877a9-123">Farklı Intrastat yönleri için sayım yapmanız gerekir. Bu nedenle, bu biçim yapılandırmasının veri kaynakları listesine özel model numaralandırması ekleyin.</span><span class="sxs-lookup"><span data-stu-id="877a9-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="877a9-124">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="877a9-125">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="877a9-126">Ağaçta, "Veri modeli\Numaralandırma" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="877a9-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="877a9-127">Ad alanına "Yön" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="877a9-128">Model numaralandırma alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="877a9-129">Değer olarak Yön'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="877a9-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-130">Click OK.</span></span>
9. <span data-ttu-id="877a9-131">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="877a9-132">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="877a9-133">Ad alanına, '$BlockName' yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="877a9-134">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-134">Click Edit formula.</span></span>
13. <span data-ttu-id="877a9-135">Formül alanına "blok" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="877a9-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-136">Click Save.</span></span>
15. <span data-ttu-id="877a9-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-137">Close the page.</span></span>
16. <span data-ttu-id="877a9-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-138">Click OK.</span></span>
17. <span data-ttu-id="877a9-139">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="877a9-140">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="877a9-141">Ad alanına "$RecName" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="877a9-142">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-142">Click Edit formula.</span></span>
21. <span data-ttu-id="877a9-143">Formül alanına "kayıt" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="877a9-144">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-144">Click Save.</span></span>
23. <span data-ttu-id="877a9-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-145">Close the page.</span></span>
24. <span data-ttu-id="877a9-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-146">Click OK.</span></span>
25. <span data-ttu-id="877a9-147">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="877a9-148">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="877a9-149">Ad alanına "$InvName" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="877a9-150">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-150">Click Edit formula.</span></span>
29. <span data-ttu-id="877a9-151">Formül alanına "InvoicedAmountEUR" yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="877a9-152">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-152">Click Save.</span></span>
31. <span data-ttu-id="877a9-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-153">Close the page.</span></span>
32. <span data-ttu-id="877a9-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-154">Click OK.</span></span>
33. <span data-ttu-id="877a9-155">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="877a9-156">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="877a9-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="877a9-157">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-157">Click Add data source.</span></span>
    * <span data-ttu-id="877a9-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="877a9-158">$BlockName</span></span>  
36. <span data-ttu-id="877a9-159">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-159">Click Save.</span></span>
37. <span data-ttu-id="877a9-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-160">Close the page.</span></span>
38. <span data-ttu-id="877a9-161">Toplanan veri anahtarı değeri alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="877a9-162">Formül alanına, "EĞER(Intrastat.CommodityRecord.Direction=Direction.Import, "İthalat", "İhracat")' yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="877a9-163">EĞER(Intrastat.CommodityRecord.Direction=Direction.Import, "İthalat", "İhracat")</span><span class="sxs-lookup"><span data-stu-id="877a9-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="877a9-164">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-164">Click Save.</span></span>
41. <span data-ttu-id="877a9-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-165">Close the page.</span></span>
    * <span data-ttu-id="877a9-166">Bu dizinin satırlarını sayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-166">Count the lines of this sequence.</span></span> <span data-ttu-id="877a9-167">Sonuçlar, farklı yönler için ayrı ayrı "blok" adıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="877a9-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="877a9-168">Her varış Intrastat hareketi için "İthalat" değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="877a9-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="877a9-169">Her sevk Intrastat hareketi için "İhracat" değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="877a9-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="877a9-170">Bunu sanal bir Excel elektronik tablosu olarak düşünün.</span><span class="sxs-lookup"><span data-stu-id="877a9-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="877a9-171">Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="877a9-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="877a9-172">Ağaçta "Intrastat\Veri:Sıra" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="877a9-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="877a9-173">Ağaçta, "Intrastat\Veri:Sıra\Gelen?" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="877a9-174">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="877a9-175">Bu dizinin satırlarını sayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-175">Count the lines of this sequence.</span></span> <span data-ttu-id="877a9-176">Sonuçlar "kayıt" adı kullanılarak belleğe alınır.</span><span class="sxs-lookup"><span data-stu-id="877a9-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="877a9-177">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="877a9-178">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-178">Click Add data source.</span></span>
47. <span data-ttu-id="877a9-179">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-179">Click Save.</span></span>
48. <span data-ttu-id="877a9-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-180">Close the page.</span></span>
49. <span data-ttu-id="877a9-181">"Toplanan veri anahtarı değeri" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="877a9-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="877a9-182">Formül alanına, 'Intrastat.CommodityRecord.CommodityCode' yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="877a9-183">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-183">Click Save.</span></span>
52. <span data-ttu-id="877a9-184">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-184">Close the page.</span></span>
    * <span data-ttu-id="877a9-185">Bu dizinin satırlarını sayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-185">Count the lines of this sequence.</span></span> <span data-ttu-id="877a9-186">Sonuçlar, farklı emtia kodları için ayrı ayrı "kayıt" adıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="877a9-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="877a9-187">Bunu sanal bir Excel elektronik tablosu olarak düşünün.</span><span class="sxs-lookup"><span data-stu-id="877a9-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="877a9-188">Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur ve ikinci "kayıt" bloğu emtia kodu değeri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="877a9-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="877a9-189">Ağaçta, "Intrastat\Veri:Sıra\Sevkler?" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="877a9-190">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="877a9-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="877a9-191">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="877a9-192">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-192">Click Add data source.</span></span>
57. <span data-ttu-id="877a9-193">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-193">Click Save.</span></span>
58. <span data-ttu-id="877a9-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-194">Close the page.</span></span>
59. <span data-ttu-id="877a9-195">"Toplanan veri anahtarı değeri" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="877a9-196">Formül alanına, 'Intrastat.CommodityRecord.CommodityCode' yazın.</span><span class="sxs-lookup"><span data-stu-id="877a9-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="877a9-197">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-197">Click Save.</span></span>
62. <span data-ttu-id="877a9-198">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-198">Close the page.</span></span>
63. <span data-ttu-id="877a9-199">Ağaçta, "Intrastat\Veri:Sıra\Sevkler:Sıra?" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="877a9-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="877a9-200">Ağaçta "Intrastat\Veri:Sıra\Sevkler:Sıra?\Kayıt =  Intrastat.CommodityRecord" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="877a9-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="877a9-201">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-201">Click the Format tab.</span></span>
66. <span data-ttu-id="877a9-202">Ağaçta, "Intrastat\Veri\Sevkler\Kayıt\Fatura tutarı EUR" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="877a9-203">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="877a9-204">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="877a9-205">Ağaçta, "$InvName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="877a9-206">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-206">Click Add data source.</span></span>
71. <span data-ttu-id="877a9-207">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-207">Click Save.</span></span>
72. <span data-ttu-id="877a9-208">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-208">Close the page.</span></span>
    * <span data-ttu-id="877a9-209">Bu dizinin satırları için faturalanan tutar değerlerini özetleyin.</span><span class="sxs-lookup"><span data-stu-id="877a9-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="877a9-210">Sonuçlar, farklı Intrastat yönleri ve emtia kodları için ayrı ayrı "InvoicedAmountEUR" adıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="877a9-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="877a9-211">Bunu, Excel elektronik tablosunda sanal bir oluşturma olarak düşünün.</span><span class="sxs-lookup"><span data-stu-id="877a9-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="877a9-212">Her bir hareket için "blok" ilk sütunu, uygun şekilde "İthalat" ve "İhracat" değerleriyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="877a9-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="877a9-213">İkinci "kayıt" bloğu emtia kodu değeri ile doldurulur ve üçüncü "InvoicedAmountEUR" bloğu fatura tutarı değeri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="877a9-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="877a9-214">Ağaçta "Intrastat\Veri\Gelen?" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="877a9-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="877a9-215">Ağaçta, "Intrastat\Veri\Gelen?\Kayıt =  Intrastat.CommodityRecord" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="877a9-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="877a9-216">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-216">Click the Format tab.</span></span>
76. <span data-ttu-id="877a9-217">Ağaçta, "Intrastat\Veri\Gelen\Kayıt\Fatura tutarı EUR" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="877a9-218">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="877a9-219">"Toplanan veri anahtarı adı" alanı için Düzenle düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="877a9-220">Ağaçta, "$InvName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="877a9-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="877a9-221">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-221">Click Add data source.</span></span>
81. <span data-ttu-id="877a9-222">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-222">Click Save.</span></span>
82. <span data-ttu-id="877a9-223">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-223">Close the page.</span></span>
83. <span data-ttu-id="877a9-224">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="877a9-224">Click Save.</span></span>
84. <span data-ttu-id="877a9-225">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="877a9-225">Close the page.</span></span>

