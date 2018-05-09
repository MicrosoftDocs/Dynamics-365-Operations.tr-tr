--- 
title: "Sayım ve toplama çıktısı oluşturmak için hesaplamaları kullanma"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 34cd443b09f784ef3db7599b6b1ed030428bf692
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing"></a><span data-ttu-id="5c364-103">Sayım ve toplama çıktısı oluşturmak için hesaplamaları kullanma</span><span class="sxs-lookup"><span data-stu-id="5c364-103">Use computations to make the output for counting and summing</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c364-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="5c364-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="5c364-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5c364-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5c364-106">Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 2: Hesaplamaları yapılandırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="5c364-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="5c364-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="5c364-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="5c364-108">Sayım ve toplama bilgisini kullanmak için bu raporu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5c364-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="5c364-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="5c364-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5c364-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5c364-111">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5c364-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="5c364-112">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5c364-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="5c364-113">Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="5c364-114">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-114">Click Designer.</span></span>
7. <span data-ttu-id="5c364-115">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="5c364-116">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="5c364-117">Belleğe alınan blokların listesini almak için yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5c364-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="5c364-118">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="5c364-119">Ad alanına "$BlocksList" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="5c364-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="5c364-120">$BlocksList</span></span>  
11. <span data-ttu-id="5c364-121">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-121">Click Edit formula.</span></span>
12. <span data-ttu-id="5c364-122">Ağaçta, "Veri toplama işlevleri\TOPLANANLİSTE" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="5c364-123">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-123">Click Add function.</span></span>
14. <span data-ttu-id="5c364-124">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-124">Click Add data source.</span></span>
15. <span data-ttu-id="5c364-125">Formül alanına "TOPLANANLİSTE('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="5c364-126">TOPLANANLİSTE ('$BlockName ',</span><span class="sxs-lookup"><span data-stu-id="5c364-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="5c364-127">Formül alanına "TOPLANANLİSTE('$BlockName', "\*")" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="5c364-128">TOPLANANLİSTE('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="5c364-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="5c364-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-129">Click Save.</span></span>
    * <span data-ttu-id="5c364-130">"\*" modeli, bu kaydın listesine tüm blokların dahil olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="5c364-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="5c364-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-131">Close the page.</span></span>
19. <span data-ttu-id="5c364-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-132">Click OK.</span></span>
20. <span data-ttu-id="5c364-133">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-133">Click the Format tab.</span></span>
21. <span data-ttu-id="5c364-134">Ağaçta, "Intrastat\Veri" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="5c364-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="5c364-136">Ağaçta, "Metin\Sıra" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="5c364-137">Ad alanına 'Bloklara göre toplamlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="5c364-138">Bloklara göre toplamlar</span><span class="sxs-lookup"><span data-stu-id="5c364-138">Totals by blocks</span></span>  
25. <span data-ttu-id="5c364-139">Özel karakterler alanında "Yeni satır - Windows (CR LF)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="5c364-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-140">Click OK.</span></span>
27. <span data-ttu-id="5c364-141">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="5c364-142">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="5c364-143">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="5c364-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="5c364-144">Ad alanına "Blok kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="5c364-145">Blok kodu</span><span class="sxs-lookup"><span data-stu-id="5c364-145">Block code</span></span>  
31. <span data-ttu-id="5c364-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-146">Click OK.</span></span>
32. <span data-ttu-id="5c364-147">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-147">Click Add String.</span></span>
33. <span data-ttu-id="5c364-148">Ad alanına "Satır sayımı" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="5c364-149">Satır sayımı</span><span class="sxs-lookup"><span data-stu-id="5c364-149">Lines counting</span></span>  
34. <span data-ttu-id="5c364-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-150">Click OK.</span></span>
35. <span data-ttu-id="5c364-151">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-151">Click Add String.</span></span>
36. <span data-ttu-id="5c364-152">Ad alanına "Toplam tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="5c364-153">Toplam tutar</span><span class="sxs-lookup"><span data-stu-id="5c364-153">Total amount</span></span>  
37. <span data-ttu-id="5c364-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-154">Click OK.</span></span>
38. <span data-ttu-id="5c364-155">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="5c364-156">Ağaçta, "$BlocksList" metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="5c364-157">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-157">Click Bind.</span></span>
    * <span data-ttu-id="5c364-158">Belleğe alınan her blok için bir özet satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c364-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="5c364-159">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-159">Click the Format tab.</span></span>
42. <span data-ttu-id="5c364-160">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Blok kodu" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="5c364-161">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="5c364-162">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-162">Click Edit formula.</span></span>
45. <span data-ttu-id="5c364-163">Formül alanına ""Blok kodu: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="5c364-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="5c364-164">"Blok kodu: " &</span><span class="sxs-lookup"><span data-stu-id="5c364-164">"Block id: " &</span></span>  
46. <span data-ttu-id="5c364-165">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5c364-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="5c364-166">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="5c364-167">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-167">Click Add data source.</span></span>
49. <span data-ttu-id="5c364-168">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-168">Click Save.</span></span>
50. <span data-ttu-id="5c364-169">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-169">Close the page.</span></span>
51. <span data-ttu-id="5c364-170">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-170">Click the Format tab.</span></span>
52. <span data-ttu-id="5c364-171">Ağaçta, "Intrastat\Veri\Bloklara göre toplamlar\Satır sayımı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="5c364-172">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="5c364-173">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-173">Click Edit formula.</span></span>
    * <span data-ttu-id="5c364-174">Bu raporda sunulan her bloktaki satır sayıları için çıkış oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c364-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="5c364-175">Formül alanına ""Bu bloktaki satır sayısı: " & " metnini girin.</span><span class="sxs-lookup"><span data-stu-id="5c364-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="5c364-176">"Bu bloktaki satır sayısı: " &</span><span class="sxs-lookup"><span data-stu-id="5c364-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="5c364-177">Formül alanına ""Bu bloktaki satır sayısı: " & TEXT (" metnini girin.</span><span class="sxs-lookup"><span data-stu-id="5c364-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="5c364-178">"Bu bloktaki satır sayısı: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="5c364-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="5c364-179">Ağaçta, "Veri toplama işlevleri\ÇOKEĞERSAY" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="5c364-180">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-180">Click Add function.</span></span>
59. <span data-ttu-id="5c364-181">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-181">Click Add data source.</span></span>
60. <span data-ttu-id="5c364-182">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', " yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="5c364-183">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="5c364-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="5c364-184">Ağaçta, "$BlocksList" metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5c364-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="5c364-185">Ağaçta, "$BlocksList\Değer" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="5c364-186">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-186">Click Add data source.</span></span>
64. <span data-ttu-id="5c364-187">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, " yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="5c364-188">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer,</span><span class="sxs-lookup"><span data-stu-id="5c364-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="5c364-189">Ağaçta, "$RecName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="5c364-190">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-190">Click Add data source.</span></span>
67. <span data-ttu-id="5c364-191">Formül alanına ""Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="5c364-192">"Bu bloktaki satır sayısı: " & METNEÇEVİR(ÇOKEĞERSAY('$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="5c364-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="5c364-193">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-193">Click Save.</span></span>
69. <span data-ttu-id="5c364-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-194">Close the page.</span></span>
70. <span data-ttu-id="5c364-195">Formül sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-195">Click the Format tab.</span></span>
71. <span data-ttu-id="5c364-196">Ağaçta "Intrastat\Veri\Bloklara göre toplamlar\Toplam tutar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c364-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="5c364-197">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="5c364-198">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-198">Click Edit formula.</span></span>
    * <span data-ttu-id="5c364-199">Bu raporda sunulan her bloğun faturalanan tutar toplamı olacak çıkışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c364-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="5c364-200">Formül alanına ""Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKEĞERSAY('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c364-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="5c364-201">"Faturalanan tutar toplamı: " & METNEÇEVİR(ÇOKETOPLA('$InvName', '$BlockName', '$BlocksList'.Değer, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="5c364-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="5c364-202">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-202">Click Save.</span></span>
76. <span data-ttu-id="5c364-203">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-203">Close the page.</span></span>
77. <span data-ttu-id="5c364-204">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c364-204">Click Save.</span></span>
78. <span data-ttu-id="5c364-205">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c364-205">Close the page.</span></span>


