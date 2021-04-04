---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)
description: Bu konuda, önceden oluşturulmuş metin çıktısının verilerine dayalı olarak sayma ve toplama işlemi yapmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (3. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af95399118b9059b9bead3a1b84203cf3b6e74c2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567128"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="28cb6-104">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)</span><span class="sxs-lookup"><span data-stu-id="28cb6-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28cb6-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="28cb6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="28cb6-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="28cb6-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="28cb6-107">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 2: Hesaplamaları yapılandırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="28cb6-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="28cb6-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="28cb6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="28cb6-109">Sayım ve toplama bilgisini kullanmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="28cb6-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="28cb6-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="28cb6-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="28cb6-112">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="28cb6-113">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="28cb6-114">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="28cb6-115">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-115">Click Designer.</span></span>
7. <span data-ttu-id="28cb6-116">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="28cb6-117">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="28cb6-118">Belleğe alınan blokların listesini almak için yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="28cb6-119">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="28cb6-120">Ad alanına "$BlocksList" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="28cb6-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="28cb6-121">$BlocksList</span></span>  
11. <span data-ttu-id="28cb6-122">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-122">Click Edit formula.</span></span>
12. <span data-ttu-id="28cb6-123">Ağaçta, "Veri toplama işlevleri\TOPLANANLİSTE" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="28cb6-124">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-124">Click Add function.</span></span>
14. <span data-ttu-id="28cb6-125">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-125">Click Add data source.</span></span>
15. <span data-ttu-id="28cb6-126">Formül alanına "TOPLANANLİSTE('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="28cb6-127">TOPLANANLİSTE ('$BlockName ',</span><span class="sxs-lookup"><span data-stu-id="28cb6-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="28cb6-128">Formül alanına "TOPLANANLİSTE('$BlockName', "\*")" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="28cb6-129">TOPLANANLİSTE('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="28cb6-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="28cb6-130">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-130">Click Save.</span></span>
    * <span data-ttu-id="28cb6-131">"\*" modeli, bu kaydın listesine tüm blokların dahil olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="28cb6-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="28cb6-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-132">Close the page.</span></span>
19. <span data-ttu-id="28cb6-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-133">Click OK.</span></span>
20. <span data-ttu-id="28cb6-134">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-134">Click the Format tab.</span></span>
21. <span data-ttu-id="28cb6-135">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="28cb6-136">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="28cb6-137">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="28cb6-138">Ad alanına 'Bloklara göre toplamlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="28cb6-139">Bloklara göre toplamlar</span><span class="sxs-lookup"><span data-stu-id="28cb6-139">Totals by blocks</span></span>  
25. <span data-ttu-id="28cb6-140">Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="28cb6-141">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-141">Click OK.</span></span>
27. <span data-ttu-id="28cb6-142">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="28cb6-143">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="28cb6-144">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="28cb6-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="28cb6-145">Ad alanına "Blok kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="28cb6-146">Blok kodu</span><span class="sxs-lookup"><span data-stu-id="28cb6-146">Block code</span></span>  
31. <span data-ttu-id="28cb6-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-147">Click OK.</span></span>
32. <span data-ttu-id="28cb6-148">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-148">Click Add String.</span></span>
33. <span data-ttu-id="28cb6-149">Ad alanına "Satır sayımı" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="28cb6-150">Satır sayımı</span><span class="sxs-lookup"><span data-stu-id="28cb6-150">Lines counting</span></span>  
34. <span data-ttu-id="28cb6-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-151">Click OK.</span></span>
35. <span data-ttu-id="28cb6-152">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-152">Click Add String.</span></span>
36. <span data-ttu-id="28cb6-153">Ad alanına "Toplam tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="28cb6-154">Toplam tutar</span><span class="sxs-lookup"><span data-stu-id="28cb6-154">Total amount</span></span>  
37. <span data-ttu-id="28cb6-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-155">Click OK.</span></span>
38. <span data-ttu-id="28cb6-156">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="28cb6-157">Ağaçta, "$BlocksList" metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="28cb6-158">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-158">Click Bind.</span></span>
    * <span data-ttu-id="28cb6-159">Belleğe alınan her blok için bir özet satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="28cb6-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="28cb6-160">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-160">Click the Format tab.</span></span>
42. <span data-ttu-id="28cb6-161">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Blok kodu" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="28cb6-162">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="28cb6-163">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-163">Click Edit formula.</span></span>
45. <span data-ttu-id="28cb6-164">Formül alanına ""Blok kodu: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="28cb6-165">"Blok kodu: " &</span><span class="sxs-lookup"><span data-stu-id="28cb6-165">"Block id: " &</span></span>  
46. <span data-ttu-id="28cb6-166">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="28cb6-167">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="28cb6-168">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-168">Click Add data source.</span></span>
49. <span data-ttu-id="28cb6-169">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-169">Click Save.</span></span>
50. <span data-ttu-id="28cb6-170">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-170">Close the page.</span></span>
51. <span data-ttu-id="28cb6-171">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-171">Click the Format tab.</span></span>
52. <span data-ttu-id="28cb6-172">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar\Satır sayımı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="28cb6-173">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="28cb6-174">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-174">Click Edit formula.</span></span>
    * <span data-ttu-id="28cb6-175">Bu raporda sunulan her bloktaki satır sayıları için çıkış oluşturun.</span><span class="sxs-lookup"><span data-stu-id="28cb6-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="28cb6-176">Formül alanına ""Bu bloktaki satır sayısı: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="28cb6-177">"Bu bloktaki satır sayısı: " &</span><span class="sxs-lookup"><span data-stu-id="28cb6-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="28cb6-178">Formül alanına ""Bu bloktaki satır sayısı: " & TEXT (" metnini girin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="28cb6-179">"Bu bloktaki satır sayısı: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="28cb6-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="28cb6-180">Ağaçta, "Veri toplama işlevleri\ÇOKEĞERSAY" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="28cb6-181">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-181">Click Add function.</span></span>
59. <span data-ttu-id="28cb6-182">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-182">Click Add data source.</span></span>
60. <span data-ttu-id="28cb6-183">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="28cb6-184">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="28cb6-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="28cb6-185">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="28cb6-186">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="28cb6-187">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-187">Click Add data source.</span></span>
64. <span data-ttu-id="28cb6-188">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, " yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="28cb6-189">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer,</span><span class="sxs-lookup"><span data-stu-id="28cb6-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="28cb6-190">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="28cb6-191">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-191">Click Add data source.</span></span>
67. <span data-ttu-id="28cb6-192">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="28cb6-193">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="28cb6-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="28cb6-194">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-194">Click Save.</span></span>
69. <span data-ttu-id="28cb6-195">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-195">Close the page.</span></span>
70. <span data-ttu-id="28cb6-196">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-196">Click the Format tab.</span></span>
71. <span data-ttu-id="28cb6-197">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Toplam tutar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28cb6-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="28cb6-198">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="28cb6-199">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-199">Click Edit formula.</span></span>
    * <span data-ttu-id="28cb6-200">Bu raporda sunulan her bloğun faturalanan tutar toplamı olacak çıkışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="28cb6-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="28cb6-201">Formül alanına ""Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKEĞERSAY('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="28cb6-202">"Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKETOPLA('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="28cb6-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="28cb6-203">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-203">Click Save.</span></span>
76. <span data-ttu-id="28cb6-204">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-204">Close the page.</span></span>
77. <span data-ttu-id="28cb6-205">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-205">Click Save.</span></span>
78. <span data-ttu-id="28cb6-206">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="28cb6-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]