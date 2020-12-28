---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b26a7f50a2237e0d3d756f8eebf2e4cd81f24683
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684679"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="4f712-103">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 3 - Çıktıyı hazırlamak için işlemleri kullanma)</span><span class="sxs-lookup"><span data-stu-id="4f712-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f712-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="4f712-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="4f712-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4f712-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4f712-106">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 2: Hesaplamaları yapılandırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="4f712-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="4f712-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="4f712-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="4f712-108">Sayım ve toplama bilgisini kullanmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4f712-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="4f712-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="4f712-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4f712-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4f712-111">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4f712-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="4f712-112">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4f712-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="4f712-113">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="4f712-114">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-114">Click Designer.</span></span>
7. <span data-ttu-id="4f712-115">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="4f712-116">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="4f712-117">Belleğe alınan blokların listesini almak için yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4f712-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="4f712-118">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="4f712-119">Ad alanına "$BlocksList" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="4f712-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="4f712-120">$BlocksList</span></span>  
11. <span data-ttu-id="4f712-121">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-121">Click Edit formula.</span></span>
12. <span data-ttu-id="4f712-122">Ağaçta, "Veri toplama işlevleri\TOPLANANLİSTE" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="4f712-123">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-123">Click Add function.</span></span>
14. <span data-ttu-id="4f712-124">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-124">Click Add data source.</span></span>
15. <span data-ttu-id="4f712-125">Formül alanına "TOPLANANLİSTE('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="4f712-126">TOPLANANLİSTE ('$BlockName ',</span><span class="sxs-lookup"><span data-stu-id="4f712-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="4f712-127">Formül alanına "TOPLANANLİSTE('$BlockName', "\*")" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="4f712-128">TOPLANANLİSTE('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="4f712-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="4f712-129">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-129">Click Save.</span></span>
    * <span data-ttu-id="4f712-130">"\*" modeli, bu kaydın listesine tüm blokların dahil olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4f712-130">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="4f712-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-131">Close the page.</span></span>
19. <span data-ttu-id="4f712-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-132">Click OK.</span></span>
20. <span data-ttu-id="4f712-133">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-133">Click the Format tab.</span></span>
21. <span data-ttu-id="4f712-134">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="4f712-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="4f712-136">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="4f712-137">Ad alanına 'Bloklara göre toplamlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="4f712-138">Bloklara göre toplamlar</span><span class="sxs-lookup"><span data-stu-id="4f712-138">Totals by blocks</span></span>  
25. <span data-ttu-id="4f712-139">Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="4f712-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-140">Click OK.</span></span>
27. <span data-ttu-id="4f712-141">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="4f712-142">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="4f712-143">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="4f712-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="4f712-144">Ad alanına "Blok kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="4f712-145">Blok kodu</span><span class="sxs-lookup"><span data-stu-id="4f712-145">Block code</span></span>  
31. <span data-ttu-id="4f712-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-146">Click OK.</span></span>
32. <span data-ttu-id="4f712-147">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-147">Click Add String.</span></span>
33. <span data-ttu-id="4f712-148">Ad alanına "Satır sayımı" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="4f712-149">Satır sayımı</span><span class="sxs-lookup"><span data-stu-id="4f712-149">Lines counting</span></span>  
34. <span data-ttu-id="4f712-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-150">Click OK.</span></span>
35. <span data-ttu-id="4f712-151">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-151">Click Add String.</span></span>
36. <span data-ttu-id="4f712-152">Ad alanına "Toplam tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="4f712-153">Toplam tutar</span><span class="sxs-lookup"><span data-stu-id="4f712-153">Total amount</span></span>  
37. <span data-ttu-id="4f712-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-154">Click OK.</span></span>
38. <span data-ttu-id="4f712-155">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="4f712-156">Ağaçta, "$BlocksList" metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="4f712-157">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-157">Click Bind.</span></span>
    * <span data-ttu-id="4f712-158">Belleğe alınan her blok için bir özet satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4f712-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="4f712-159">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-159">Click the Format tab.</span></span>
42. <span data-ttu-id="4f712-160">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Blok kodu" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="4f712-161">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="4f712-162">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-162">Click Edit formula.</span></span>
45. <span data-ttu-id="4f712-163">Formül alanına ""Blok kodu: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="4f712-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="4f712-164">"Blok kodu: " &</span><span class="sxs-lookup"><span data-stu-id="4f712-164">"Block id: " &</span></span>  
46. <span data-ttu-id="4f712-165">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4f712-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="4f712-166">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="4f712-167">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-167">Click Add data source.</span></span>
49. <span data-ttu-id="4f712-168">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-168">Click Save.</span></span>
50. <span data-ttu-id="4f712-169">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-169">Close the page.</span></span>
51. <span data-ttu-id="4f712-170">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-170">Click the Format tab.</span></span>
52. <span data-ttu-id="4f712-171">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar\Satır sayımı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="4f712-172">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="4f712-173">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-173">Click Edit formula.</span></span>
    * <span data-ttu-id="4f712-174">Bu raporda sunulan her bloktaki satır sayıları için çıkış oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4f712-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="4f712-175">Formül alanına ""Bu bloktaki satır sayısı: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="4f712-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="4f712-176">"Bu bloktaki satır sayısı: " &</span><span class="sxs-lookup"><span data-stu-id="4f712-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="4f712-177">Formül alanına ""Bu bloktaki satır sayısı: " & TEXT (" metnini girin.</span><span class="sxs-lookup"><span data-stu-id="4f712-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="4f712-178">"Bu bloktaki satır sayısı: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="4f712-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="4f712-179">Ağaçta, "Veri toplama işlevleri\ÇOKEĞERSAY" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="4f712-180">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-180">Click Add function.</span></span>
59. <span data-ttu-id="4f712-181">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-181">Click Add data source.</span></span>
60. <span data-ttu-id="4f712-182">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="4f712-183">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4f712-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="4f712-184">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4f712-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="4f712-185">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="4f712-186">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-186">Click Add data source.</span></span>
64. <span data-ttu-id="4f712-187">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, " yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="4f712-188">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer,</span><span class="sxs-lookup"><span data-stu-id="4f712-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="4f712-189">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="4f712-190">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-190">Click Add data source.</span></span>
67. <span data-ttu-id="4f712-191">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="4f712-192">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="4f712-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="4f712-193">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-193">Click Save.</span></span>
69. <span data-ttu-id="4f712-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-194">Close the page.</span></span>
70. <span data-ttu-id="4f712-195">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-195">Click the Format tab.</span></span>
71. <span data-ttu-id="4f712-196">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Toplam tutar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f712-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="4f712-197">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="4f712-198">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-198">Click Edit formula.</span></span>
    * <span data-ttu-id="4f712-199">Bu raporda sunulan her bloğun faturalanan tutar toplamı olacak çıkışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4f712-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="4f712-200">Formül alanına ""Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKEĞERSAY('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="4f712-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="4f712-201">"Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKETOPLA('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="4f712-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="4f712-202">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-202">Click Save.</span></span>
76. <span data-ttu-id="4f712-203">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-203">Close the page.</span></span>
77. <span data-ttu-id="4f712-204">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f712-204">Click Save.</span></span>
78. <span data-ttu-id="4f712-205">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4f712-205">Close the page.</span></span>

