---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)
description: Bu konuda, önceden oluşturulmuş metin çıktısının verilerine dayalı olarak sayma ve toplama işlemi yapmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (3. Bölüm)
author: NickSelin
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
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749009"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="98220-104">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)</span><span class="sxs-lookup"><span data-stu-id="98220-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98220-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="98220-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="98220-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="98220-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="98220-107">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 2: Hesaplamaları yapılandırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="98220-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="98220-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="98220-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="98220-109">Sayım ve toplama bilgisini kullanmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="98220-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="98220-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="98220-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="98220-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="98220-112">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="98220-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="98220-113">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="98220-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="98220-114">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="98220-115">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-115">Click Designer.</span></span>
7. <span data-ttu-id="98220-116">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="98220-117">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="98220-118">Belleğe alınan blokların listesini almak için yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="98220-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="98220-119">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="98220-120">Ad alanına "$BlocksList" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="98220-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="98220-121">$BlocksList</span></span>  
11. <span data-ttu-id="98220-122">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-122">Click Edit formula.</span></span>
12. <span data-ttu-id="98220-123">Ağaçta, "Veri toplama işlevleri\TOPLANANLİSTE" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="98220-124">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-124">Click Add function.</span></span>
14. <span data-ttu-id="98220-125">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-125">Click Add data source.</span></span>
15. <span data-ttu-id="98220-126">Formül alanına "TOPLANANLİSTE('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="98220-127">TOPLANANLİSTE ('$BlockName ',</span><span class="sxs-lookup"><span data-stu-id="98220-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="98220-128">Formül alanına "TOPLANANLİSTE('$BlockName', "\*")" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="98220-129">TOPLANANLİSTE('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="98220-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="98220-130">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-130">Click Save.</span></span>
    * <span data-ttu-id="98220-131">"\*" modeli, bu kaydın listesine tüm blokların dahil olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="98220-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="98220-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="98220-132">Close the page.</span></span>
19. <span data-ttu-id="98220-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-133">Click OK.</span></span>
20. <span data-ttu-id="98220-134">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-134">Click the Format tab.</span></span>
21. <span data-ttu-id="98220-135">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="98220-136">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="98220-137">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="98220-138">Ad alanına 'Bloklara göre toplamlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="98220-139">Bloklara göre toplamlar</span><span class="sxs-lookup"><span data-stu-id="98220-139">Totals by blocks</span></span>  
25. <span data-ttu-id="98220-140">Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="98220-141">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-141">Click OK.</span></span>
27. <span data-ttu-id="98220-142">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="98220-143">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="98220-144">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="98220-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="98220-145">Ad alanına "Blok kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="98220-146">Blok kodu</span><span class="sxs-lookup"><span data-stu-id="98220-146">Block code</span></span>  
31. <span data-ttu-id="98220-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-147">Click OK.</span></span>
32. <span data-ttu-id="98220-148">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-148">Click Add String.</span></span>
33. <span data-ttu-id="98220-149">Ad alanına "Satır sayımı" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="98220-150">Satır sayımı</span><span class="sxs-lookup"><span data-stu-id="98220-150">Lines counting</span></span>  
34. <span data-ttu-id="98220-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-151">Click OK.</span></span>
35. <span data-ttu-id="98220-152">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-152">Click Add String.</span></span>
36. <span data-ttu-id="98220-153">Ad alanına "Toplam tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="98220-154">Toplam tutar</span><span class="sxs-lookup"><span data-stu-id="98220-154">Total amount</span></span>  
37. <span data-ttu-id="98220-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-155">Click OK.</span></span>
38. <span data-ttu-id="98220-156">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="98220-157">Ağaçta, "$BlocksList" metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="98220-158">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-158">Click Bind.</span></span>
    * <span data-ttu-id="98220-159">Belleğe alınan her blok için bir özet satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="98220-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="98220-160">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-160">Click the Format tab.</span></span>
42. <span data-ttu-id="98220-161">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Blok kodu" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="98220-162">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="98220-163">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-163">Click Edit formula.</span></span>
45. <span data-ttu-id="98220-164">Formül alanına ""Blok kodu: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="98220-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="98220-165">"Blok kodu: " &</span><span class="sxs-lookup"><span data-stu-id="98220-165">"Block id: " &</span></span>  
46. <span data-ttu-id="98220-166">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="98220-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="98220-167">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="98220-168">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-168">Click Add data source.</span></span>
49. <span data-ttu-id="98220-169">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-169">Click Save.</span></span>
50. <span data-ttu-id="98220-170">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="98220-170">Close the page.</span></span>
51. <span data-ttu-id="98220-171">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-171">Click the Format tab.</span></span>
52. <span data-ttu-id="98220-172">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar\Satır sayımı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="98220-173">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="98220-174">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-174">Click Edit formula.</span></span>
    * <span data-ttu-id="98220-175">Bu raporda sunulan her bloktaki satır sayıları için çıkış oluşturun.</span><span class="sxs-lookup"><span data-stu-id="98220-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="98220-176">Formül alanına ""Bu bloktaki satır sayısı: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="98220-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="98220-177">"Bu bloktaki satır sayısı: " &</span><span class="sxs-lookup"><span data-stu-id="98220-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="98220-178">Formül alanına ""Bu bloktaki satır sayısı: " & TEXT (" metnini girin.</span><span class="sxs-lookup"><span data-stu-id="98220-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="98220-179">"Bu bloktaki satır sayısı: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="98220-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="98220-180">Ağaçta, "Veri toplama işlevleri\ÇOKEĞERSAY" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="98220-181">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-181">Click Add function.</span></span>
59. <span data-ttu-id="98220-182">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-182">Click Add data source.</span></span>
60. <span data-ttu-id="98220-183">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="98220-184">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="98220-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="98220-185">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="98220-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="98220-186">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="98220-187">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-187">Click Add data source.</span></span>
64. <span data-ttu-id="98220-188">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, " yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="98220-189">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer,</span><span class="sxs-lookup"><span data-stu-id="98220-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="98220-190">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="98220-191">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-191">Click Add data source.</span></span>
67. <span data-ttu-id="98220-192">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="98220-193">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="98220-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="98220-194">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-194">Click Save.</span></span>
69. <span data-ttu-id="98220-195">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="98220-195">Close the page.</span></span>
70. <span data-ttu-id="98220-196">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-196">Click the Format tab.</span></span>
71. <span data-ttu-id="98220-197">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Toplam tutar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98220-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="98220-198">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98220-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="98220-199">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-199">Click Edit formula.</span></span>
    * <span data-ttu-id="98220-200">Bu raporda sunulan her bloğun faturalanan tutar toplamı olacak çıkışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="98220-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="98220-201">Formül alanına ""Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKEĞERSAY('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="98220-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="98220-202">"Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKETOPLA('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="98220-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="98220-203">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-203">Click Save.</span></span>
76. <span data-ttu-id="98220-204">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="98220-204">Close the page.</span></span>
77. <span data-ttu-id="98220-205">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98220-205">Click Save.</span></span>
78. <span data-ttu-id="98220-206">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="98220-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]