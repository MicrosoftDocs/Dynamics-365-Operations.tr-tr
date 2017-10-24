--- 
title: "Sabit kıymet deftere nakil profilleri ayarlama"
description: "Bu görev kılavuzunda Sabit kıymet deftere nakil profilleri ayarlanacak."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="d917c-103">Sabit kıymet deftere nakil profilleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="d917c-103">Set up fixed asset posting profiles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d917c-104">Bu görev kılavuzunda Sabit kıymet deftere nakil profilleri ayarlanacak.</span><span class="sxs-lookup"><span data-stu-id="d917c-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="d917c-105">Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d917c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="d917c-106">Özel hesap planınız ve mali raporlama gereksinimleriniz için deftere nakil profilleri oluşturulması gerekmesine karşın, bu görev kılavuzunda verilen örnekler temel bir deftere nakil profiline aittir.</span><span class="sxs-lookup"><span data-stu-id="d917c-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="d917c-107">Sabit kıymetler > Kurulum > Sabit kıymet deftere nakil profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d917c-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="d917c-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d917c-108">Click New.</span></span>
3. <span data-ttu-id="d917c-109">Deftere nakil profili alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d917c-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="d917c-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d917c-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d917c-111">Sabit kıymetlerle çalışırken kullanacağınız her sabit kıymet hareket türü için bir nakil profili oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d917c-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="d917c-112">Bu görev kılavuzu Alım hareket türüyle başlayacak.</span><span class="sxs-lookup"><span data-stu-id="d917c-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="d917c-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-113">Click Add.</span></span>
6. <span data-ttu-id="d917c-114">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d917c-115">Gruplandırma alanı, deftere nakil profilini Tablo (her sabit kıymet için ayarlanmış bir hesap) veya Grup (her sabit kıymet grubu için ayarlanmış bir hesap) olarak tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="d917c-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="d917c-116">Bu görev kılavuzu için belirtilen Defterdeki tüm sabit kıymetlere uygulanmak üzere değeri "Tümü" olarak bırakacağım.</span><span class="sxs-lookup"><span data-stu-id="d917c-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="d917c-117">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d917c-118">Alımlar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d917c-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="d917c-119">Hareket türü alanında "Alım düzeltmesi"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="d917c-120">Alım düzeltme hareketleri için, Alım hareketlerinde kullanılan hesapları kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="d917c-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="d917c-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-121">Click Add.</span></span>
10. <span data-ttu-id="d917c-122">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="d917c-123">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d917c-124">Alım düzeltmeleri için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d917c-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="d917c-125">Hareket türü alanında "Amortisman"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="d917c-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-126">Click Add.</span></span>
14. <span data-ttu-id="d917c-127">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="d917c-128">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="d917c-129">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="d917c-130">Hareket türü alanında "Amortisman düzeltmesi"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="d917c-131">Amortisman düzeltme hareketleri için, Amortisman hareketlerinde kullanılan hesapları kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="d917c-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="d917c-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-132">Click Add.</span></span>
19. <span data-ttu-id="d917c-133">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="d917c-134">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="d917c-135">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="d917c-136">Hareket türü alanında "Satış çıkışı"nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="d917c-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-137">Click Add.</span></span>
24. <span data-ttu-id="d917c-138">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="d917c-139">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d917c-140">Elden çıkarmalar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d917c-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="d917c-141">Hareket türü alanında "Hurda çıkışı"nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="d917c-142">Satışla elden çıkarma ve Iskartaya çıkararak elden çıkarma için aynı hesapları kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="d917c-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="d917c-143">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-143">Click Add.</span></span>
28. <span data-ttu-id="d917c-144">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="d917c-145">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d917c-146">Elden çıkarmalar için bir mahsup hesap girebilir veya belirli bir hareket için doldurulmak üzere boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d917c-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="d917c-147">Elden çıkarma bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="d917c-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="d917c-148">Hem satış hem de ıskarta için elden çıkarma deftere nakil profilleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d917c-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="d917c-149">Elden çıkarma satış hareketleriyle başlayalım.</span><span class="sxs-lookup"><span data-stu-id="d917c-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="d917c-150">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-150">Click Add.</span></span>
32. <span data-ttu-id="d917c-151">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="d917c-152">Nakledilecek değer alanında "Alım değeri"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="d917c-153">Alım değeri, tüm yıllar için Alım ve Alım düzeltme değerlerini karşılayacak.</span><span class="sxs-lookup"><span data-stu-id="d917c-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="d917c-154">Bu hareket türleri için hesapları ayrı ayrı da tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d917c-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="d917c-155">Elden çıkarma sonuçlarının kar veya zarar olmasına bağlı olarak, elden çıkarma işlemini farklı hesaplar kullanacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d917c-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="d917c-156">Tüm elden çıkarma türlerinde aynı hesapları kullanmak üzere Satış değeri türünü "Tümü" yapacağız.</span><span class="sxs-lookup"><span data-stu-id="d917c-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="d917c-157">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="d917c-158">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="d917c-159">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-159">Click Add.</span></span>
37. <span data-ttu-id="d917c-160">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d917c-161">Nakledilecek değer alanında "Amortisman (önceki yıllar)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="d917c-162">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="d917c-163">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="d917c-164">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-164">Click Add.</span></span>
41. <span data-ttu-id="d917c-165">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="d917c-166">Nakledilecek değer alanında "Amortisman (bu yıl)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="d917c-167">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="d917c-168">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="d917c-169">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-169">Click Add.</span></span>
46. <span data-ttu-id="d917c-170">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="d917c-171">Nakledilecek değer alanında "Amortisman düzeltmeleri (önceki yıllar)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="d917c-172">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="d917c-173">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="d917c-174">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-174">Click Add.</span></span>
51. <span data-ttu-id="d917c-175">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="d917c-176">Nakledilecek değer alanında "Amortisman düzeltmeleri (bu yıl)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="d917c-177">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="d917c-178">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="d917c-179">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-179">Click Add.</span></span>
56. <span data-ttu-id="d917c-180">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="d917c-181">Nakledilecek değer alanında "Net defter değeri"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="d917c-182">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="d917c-183">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="d917c-184">Satış veya ıskartaya çıkarma alanında "Iskarta"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="d917c-185">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-185">Click Add.</span></span>
62. <span data-ttu-id="d917c-186">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="d917c-187">Nakledilecek değer alanında "Alım değeri"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="d917c-188">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="d917c-189">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="d917c-190">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-190">Click Add.</span></span>
67. <span data-ttu-id="d917c-191">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d917c-192">Nakledilecek değer alanında "Amortisman (önceki yıllar)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="d917c-193">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="d917c-194">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="d917c-195">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-195">Click Add.</span></span>
71. <span data-ttu-id="d917c-196">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="d917c-197">Nakledilecek değer alanında "Amortisman (bu yıl)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="d917c-198">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="d917c-199">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="d917c-200">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-200">Click Add.</span></span>
76. <span data-ttu-id="d917c-201">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="d917c-202">Nakledilecek değer alanında "Amortisman düzeltmeleri (önceki yıllar)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="d917c-203">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="d917c-204">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="d917c-205">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-205">Click Add.</span></span>
81. <span data-ttu-id="d917c-206">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="d917c-207">Nakledilecek değer alanında "Amortisman düzeltmeleri (bu yıl)"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="d917c-208">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="d917c-209">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="d917c-210">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d917c-210">Click Add.</span></span>
86. <span data-ttu-id="d917c-211">Defter alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="d917c-212">Nakledilecek değer alanında "Net defter değeri"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d917c-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="d917c-213">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="d917c-214">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d917c-214">In the Offset account field, specify the desired values.</span></span>


