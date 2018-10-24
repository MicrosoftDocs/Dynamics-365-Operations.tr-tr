--- 
title: "ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="84835-103">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3: Çıktıyı hazırlamak için işlemleri kullanma)</span><span class="sxs-lookup"><span data-stu-id="84835-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84835-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="84835-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="84835-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="84835-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="84835-106">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 2: Hesaplamaları yapılandırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="84835-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="84835-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="84835-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="84835-108">Sayım ve toplama bilgisini kullanmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="84835-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="84835-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="84835-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="84835-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="84835-111">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="84835-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="84835-112">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="84835-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="84835-113">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="84835-114">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-114">Click Designer.</span></span>
7. <span data-ttu-id="84835-115">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="84835-116">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="84835-117">Belleğe alınan blokların listesini almak için yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="84835-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="84835-118">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="84835-119">Ad alanına "$BlocksList" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="84835-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="84835-120">$BlocksList</span></span>  
11. <span data-ttu-id="84835-121">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-121">Click Edit formula.</span></span>
12. <span data-ttu-id="84835-122">Ağaçta, "Veri toplama işlevleri\TOPLANANLİSTE" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="84835-123">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-123">Click Add function.</span></span>
14. <span data-ttu-id="84835-124">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-124">Click Add data source.</span></span>
15. <span data-ttu-id="84835-125">Formül alanına "TOPLANANLİSTE('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="84835-126">TOPLANANLİSTE ('$BlockName ',</span><span class="sxs-lookup"><span data-stu-id="84835-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="84835-127">Formül alanına "TOPLANANLİSTE('$BlockName', "\*")" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="84835-128">TOPLANANLİSTE('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="84835-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="84835-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-129">Click Save.</span></span>
    * <span data-ttu-id="84835-130">"\*" modeli, bu kaydın listesine tüm blokların dahil olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="84835-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="84835-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84835-131">Close the page.</span></span>
19. <span data-ttu-id="84835-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-132">Click OK.</span></span>
20. <span data-ttu-id="84835-133">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-133">Click the Format tab.</span></span>
21. <span data-ttu-id="84835-134">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="84835-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="84835-136">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="84835-137">Ad alanına 'Bloklara göre toplamlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="84835-138">Bloklara göre toplamlar</span><span class="sxs-lookup"><span data-stu-id="84835-138">Totals by blocks</span></span>  
25. <span data-ttu-id="84835-139">Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="84835-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-140">Click OK.</span></span>
27. <span data-ttu-id="84835-141">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="84835-142">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="84835-143">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="84835-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="84835-144">Ad alanına "Blok kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="84835-145">Blok kodu</span><span class="sxs-lookup"><span data-stu-id="84835-145">Block code</span></span>  
31. <span data-ttu-id="84835-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-146">Click OK.</span></span>
32. <span data-ttu-id="84835-147">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-147">Click Add String.</span></span>
33. <span data-ttu-id="84835-148">Ad alanına "Satır sayımı" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="84835-149">Satır sayımı</span><span class="sxs-lookup"><span data-stu-id="84835-149">Lines counting</span></span>  
34. <span data-ttu-id="84835-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-150">Click OK.</span></span>
35. <span data-ttu-id="84835-151">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-151">Click Add String.</span></span>
36. <span data-ttu-id="84835-152">Ad alanına "Toplam tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="84835-153">Toplam tutar</span><span class="sxs-lookup"><span data-stu-id="84835-153">Total amount</span></span>  
37. <span data-ttu-id="84835-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-154">Click OK.</span></span>
38. <span data-ttu-id="84835-155">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="84835-156">Ağaçta, "$BlocksList" metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="84835-157">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-157">Click Bind.</span></span>
    * <span data-ttu-id="84835-158">Belleğe alınan her blok için bir özet satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="84835-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="84835-159">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-159">Click the Format tab.</span></span>
42. <span data-ttu-id="84835-160">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Blok kodu" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="84835-161">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="84835-162">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-162">Click Edit formula.</span></span>
45. <span data-ttu-id="84835-163">Formül alanına ""Blok kodu: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="84835-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="84835-164">"Blok kodu: " &</span><span class="sxs-lookup"><span data-stu-id="84835-164">"Block id: " &</span></span>  
46. <span data-ttu-id="84835-165">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="84835-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="84835-166">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="84835-167">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-167">Click Add data source.</span></span>
49. <span data-ttu-id="84835-168">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-168">Click Save.</span></span>
50. <span data-ttu-id="84835-169">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84835-169">Close the page.</span></span>
51. <span data-ttu-id="84835-170">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-170">Click the Format tab.</span></span>
52. <span data-ttu-id="84835-171">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar\Satır sayımı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="84835-172">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="84835-173">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-173">Click Edit formula.</span></span>
    * <span data-ttu-id="84835-174">Bu raporda sunulan her bloktaki satır sayıları için çıkış oluşturun.</span><span class="sxs-lookup"><span data-stu-id="84835-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="84835-175">Formül alanına ""Bu bloktaki satır sayısı: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="84835-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="84835-176">"Bu bloktaki satır sayısı: " &</span><span class="sxs-lookup"><span data-stu-id="84835-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="84835-177">Formül alanına ""Bu bloktaki satır sayısı: " & TEXT (" metnini girin.</span><span class="sxs-lookup"><span data-stu-id="84835-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="84835-178">"Bu bloktaki satır sayısı: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="84835-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="84835-179">Ağaçta, "Veri toplama işlevleri\ÇOKEĞERSAY" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="84835-180">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-180">Click Add function.</span></span>
59. <span data-ttu-id="84835-181">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-181">Click Add data source.</span></span>
60. <span data-ttu-id="84835-182">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="84835-183">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="84835-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="84835-184">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="84835-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="84835-185">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="84835-186">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-186">Click Add data source.</span></span>
64. <span data-ttu-id="84835-187">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, " yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="84835-188">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer,</span><span class="sxs-lookup"><span data-stu-id="84835-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="84835-189">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="84835-190">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-190">Click Add data source.</span></span>
67. <span data-ttu-id="84835-191">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="84835-192">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="84835-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="84835-193">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-193">Click Save.</span></span>
69. <span data-ttu-id="84835-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84835-194">Close the page.</span></span>
70. <span data-ttu-id="84835-195">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-195">Click the Format tab.</span></span>
71. <span data-ttu-id="84835-196">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Toplam tutar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84835-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="84835-197">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84835-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="84835-198">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-198">Click Edit formula.</span></span>
    * <span data-ttu-id="84835-199">Bu raporda sunulan her bloğun faturalanan tutar toplamı olacak çıkışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="84835-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="84835-200">Formül alanına ""Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKEĞERSAY('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="84835-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="84835-201">"Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKETOPLA('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="84835-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="84835-202">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-202">Click Save.</span></span>
76. <span data-ttu-id="84835-203">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84835-203">Close the page.</span></span>
77. <span data-ttu-id="84835-204">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84835-204">Click Save.</span></span>
78. <span data-ttu-id="84835-205">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84835-205">Close the page.</span></span>


