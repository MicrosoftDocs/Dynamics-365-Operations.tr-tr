--- 
title: "Veritabanı düzeyinde toplam hesaplamalar için bir model eşleme yapılandırması kullanma (ER)"
description: "Bu yordam yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlama ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanma hakkında bilgiler sağlar."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1dfb0d62f87f4bfdf4916fe2348bee5019841e93
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="a2002-103">Veritabanı düzeyinde toplam hesaplamalar için bir model eşleme yapılandırması kullanma (ER)</span><span class="sxs-lookup"><span data-stu-id="a2002-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2002-104">Bu yordam yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlama ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanma hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2002-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="a2002-105">Bu yordamda, Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="a2002-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="a2002-106">Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="a2002-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="a2002-107">Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a2002-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="a2002-108">Bu adımları tamamlamak için ilk olarak “ER, toplam hesaplamaları veritabanı düzeyinde gerçekleştirerek bunların verimliliğini artırır (Bölüm 1: Yapılandırmaları hazırlama)” yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a2002-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="a2002-109">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="a2002-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a2002-110">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="a2002-111">Ağaçta, 'Intrastat modeli\Intrastat örnek eşlemesi''ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="a2002-112">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-112">Click Designer.</span></span>
5. <span data-ttu-id="a2002-113">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-113">Click Designer.</span></span>
6. <span data-ttu-id="a2002-114">Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="a2002-115">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-115">Click Add root.</span></span>
    * <span data-ttu-id="a2002-116">Gruplamak istediğiniz kayıtları temsil eden yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a2002-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="a2002-117">İsim alanına, 'Hareketler' yazın.</span><span class="sxs-lookup"><span data-stu-id="a2002-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="a2002-118">Hareketler</span><span class="sxs-lookup"><span data-stu-id="a2002-118">Transactions</span></span>  
9. <span data-ttu-id="a2002-119">Tablo alanına 'Intrastat' yazın.</span><span class="sxs-lookup"><span data-stu-id="a2002-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="a2002-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="a2002-120">Intrastat</span></span>  
10. <span data-ttu-id="a2002-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-121">Click OK.</span></span>
11. <span data-ttu-id="a2002-122">Ağaçta 'İşleveler\Grupla'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="a2002-123">Bu veri kaynağı türü çalışma zamanında kayıtları gruplandırmak ve istenen toplamları hesaplamak için yeni bir veri kaynağı sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2002-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="a2002-124">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-124">Click Add root.</span></span>
13. <span data-ttu-id="a2002-125">Ad alanına 'TransactionsGroups' yazın.</span><span class="sxs-lookup"><span data-stu-id="a2002-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="a2002-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="a2002-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="a2002-127">Grubu buna göre düzenle'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-127">Click Edit group by.</span></span>
15. <span data-ttu-id="a2002-128">Ağaçta, 'Hareketler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="a2002-129">Gruplandırmak istediğiniz kayıtları temsil eden 'Kayıt listesi' türündeki eklenen veri kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="a2002-130">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-130">Click Add field to.</span></span>
17. <span data-ttu-id="a2002-131">Neler gruplanacak'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-131">Click What to group.</span></span>
18. <span data-ttu-id="a2002-132">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="a2002-133">Ağaçta, 'Hareketler\Yön''ü seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="a2002-134">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-134">Click Add field to.</span></span>
21. <span data-ttu-id="a2002-135">Gruplandırılmış alanlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="a2002-136">Gruplandırma düzeyi belirtmek için alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="a2002-137">Bu seçimi temel alınarak, veri kaynağı çalışma zamanında Instrastat tablosunda karşılanacak yön kodlarında ne kadar hareket grubu varsa bunları döndürecektir.</span><span class="sxs-lookup"><span data-stu-id="a2002-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="a2002-138">Ağaçta, 'Hareketler\Fatura tutarı(AmountMST)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="a2002-139">Toplam hesaplama için kaynağı belirtmek üzere alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="a2002-140">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-140">Click Add field to.</span></span>
24. <span data-ttu-id="a2002-141">Toplam alanları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="a2002-142">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a2002-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="a2002-143">Yöntem alanında 'Toplam' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="a2002-144">Toplam türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="a2002-145">Ad alanına 'SumOfAmountMST' yazın.</span><span class="sxs-lookup"><span data-stu-id="a2002-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="a2002-146">Yapılandırılan veri kaynağında bu toplamın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a2002-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="a2002-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-147">Click Save.</span></span>
    * <span data-ttu-id="a2002-148">'Yürütme konumu' alanının bu gruplandırmanın çalışma zamanında SQL veritabanında gerçekleştirileceğini belirttiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="a2002-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-149">Close the page.</span></span>
30. <span data-ttu-id="a2002-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-150">Click OK.</span></span>
31. <span data-ttu-id="a2002-151">Ağaçta 'Toplamlar' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="a2002-152">Ağaçta 'TransactionsGroups' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="a2002-153">Ağaçta, 'TransactionsGroups\toplanan' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="a2002-154">Ağaçta, 'TransactionsGroups\toplanan\SumOfAmountMST' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="a2002-155">Ağaçta 'Toplamlar\Toplam fatura değeri(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="a2002-156">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-156">Click Bind.</span></span>
    * <span data-ttu-id="a2002-157">Bu ayarı temel alarak, bu veri kaynağı her hareket grubu için ‘AmountMST’ alanındaki değerlerin toplamını hesaplayacaktır.</span><span class="sxs-lookup"><span data-stu-id="a2002-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="a2002-158">Bu toplam hesaplaması TransactionsGroups.aggregated.TotalAmount öğesi olarak kullanılabilecektir.</span><span class="sxs-lookup"><span data-stu-id="a2002-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="a2002-159">Ağaçta 'TransactionsGroups' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="a2002-160">Ağaçta 'TransactionsGroups' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="a2002-161">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-161">Click Edit.</span></span>
40. <span data-ttu-id="a2002-162">Grubu buna göre düzenle'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-162">Click Edit group by.</span></span>
41. <span data-ttu-id="a2002-163">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="a2002-164">Ağaçta, 'Hareketler\Fatura tutarı(AmountMST)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="a2002-165">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-165">Click Add field to.</span></span>
44. <span data-ttu-id="a2002-166">Toplam alanları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="a2002-167">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a2002-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="a2002-168">Yöntem alanında 'Maks' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="a2002-169">Ad alanına 'MaxOfAmountMST' yazın.</span><span class="sxs-lookup"><span data-stu-id="a2002-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="a2002-170">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-170">Click Save.</span></span>
    * <span data-ttu-id="a2002-171">Şu anda, GROUPBY veri kaynaklarını yürütme işlemi bazı kısıtlamalarla SQL veritabanı düzeyine çevrilebilir.</span><span class="sxs-lookup"><span data-stu-id="a2002-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="a2002-172">Çeviri ‘Kayıt listesi’ türündeki veri kaynakları veya FİLTRE işlevi kullanılarak bir ifade olarak temsil edilen veri kaynakları için yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="a2002-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="a2002-173">Ayrıca, tek bir gruplandırma kayıtları alanı için yalnızca bir toplam yapılandırıldığında da yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="a2002-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="a2002-174">AmountMST alanı için birden fazla toplam yapılandırılmış olsa bile ‘Yürütme konumu’ alanı bu gruplamanın çalışma zamanında SQL veri tabanında gerçekleştirileceğini belirtmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="a2002-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="a2002-175">Bunun nedeni, veri modeli öğesine yalnızca bir toplamın bağlanmış olması ve bunun çalışma zamanında bu veri kaynağından verileri çekmek için kullanılacak olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="a2002-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="a2002-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-176">Close the page.</span></span>
50. <span data-ttu-id="a2002-177">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-177">Click OK.</span></span>
51. <span data-ttu-id="a2002-178">Ağaçta 'TransactionsGroups' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="a2002-179">Ağaçta, 'TransactionsGroups\toplanan' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="a2002-180">Ağaçta, 'TransactionsGroups\toplanan\MaxOfAmountMST' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="a2002-181">Ağaçta, 'Toplamlar\Toplam istatistiksel değer(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="a2002-182">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-182">Click Bind.</span></span>
56. <span data-ttu-id="a2002-183">Ağaçta 'TransactionsGroups' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a2002-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="a2002-184">Ağaçta 'TransactionsGroups' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="a2002-185">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-185">Click Edit.</span></span>
59. <span data-ttu-id="a2002-186">Grubu buna göre düzenle'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-186">Click Edit group by.</span></span>
    * <span data-ttu-id="a2002-187">Aynı alandaki her iki toplam da veri modeli öğelerine bağlı olduğundan 'Yürütme konumu' alanının bu gruplamanın çalışma zamanında bellekte gerçekleştirileceğini gösterdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="a2002-188">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a2002-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="a2002-189">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-189">Click Delete.</span></span>
62. <span data-ttu-id="a2002-190">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-190">Click Yes.</span></span>
63. <span data-ttu-id="a2002-191">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-191">Click Delete.</span></span>
64. <span data-ttu-id="a2002-192">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-192">Click Yes.</span></span>
65. <span data-ttu-id="a2002-193">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2002-193">Click Add field to.</span></span>
66. <span data-ttu-id="a2002-194">Neler gruplanacak'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-194">Click What to group.</span></span>
67. <span data-ttu-id="a2002-195">Ağaçta 'Emtia kaydı(Intrastat)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a2002-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="a2002-196">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2002-196">Click Save.</span></span>
    * <span data-ttu-id="a2002-197">Tanımlanan toplamlar olmamasına ve 'Tablo kayıtları' türündeki seçilen veri kaynağı aynı 'Intrastat' tablosuna başvuruda bulunmasına rağmen 'Yürütme konumu' alanı bu gruplamanın çalışma zamanında bellekte gerçekleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2002-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="a2002-198">Bunun nedeni, veri kaynağının henüz SQL veritabanı düzeyine çevrilmemiş olan bazı hesaplanmış alanlar içermesidir.</span><span class="sxs-lookup"><span data-stu-id="a2002-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  


