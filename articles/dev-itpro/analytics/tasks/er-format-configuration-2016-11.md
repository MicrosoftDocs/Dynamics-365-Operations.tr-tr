--- 
title: "Elektronik raporlama (ER) biçim yapılandırmaları oluşturma"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="5c7c1-103">Elektronik raporlama (ER) biçim yapılandırmaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c7c1-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c7c1-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="5c7c1-105">Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="5c7c1-106">Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="5c7c1-107">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c7c1-107">Create a new format configuration</span></span>
1. <span data-ttu-id="5c7c1-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5c7c1-109">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5c7c1-110">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="5c7c1-111">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="5c7c1-112">Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="5c7c1-113">İsim alanına, "BACS (UK hayali)" yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="5c7c1-114">BACS (UK hayali)</span><span class="sxs-lookup"><span data-stu-id="5c7c1-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="5c7c1-115">Açıklama alanına, 'BACS Satıcı ödeme biçimi (UK hayali)' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="5c7c1-116">BACS Satıcı ödeme biçimi (UK hayali)</span><span class="sxs-lookup"><span data-stu-id="5c7c1-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="5c7c1-117">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5c7c1-118">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5c7c1-119">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="5c7c1-120">Elektronik belgenin belirli bir biçimi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="5c7c1-121">Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="5c7c1-122">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="5c7c1-123">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-123">Click Create configuration.</span></span>
    * <span data-ttu-id="5c7c1-124">Yeni bir yapılandırma oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-124">A new configuration has been created.</span></span> <span data-ttu-id="5c7c1-125">Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="5c7c1-126">Elektronik belgenin biçimini tasarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-126">Design format of electronic document</span></span>
1. <span data-ttu-id="5c7c1-127">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-127">Click Designer.</span></span>
2. <span data-ttu-id="5c7c1-128">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="5c7c1-129">Ağaçta seçin 'Common\File'.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="5c7c1-130">İsim alanına bir 'Xml' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="5c7c1-131">Xml</span><span class="sxs-lookup"><span data-stu-id="5c7c1-131">Xml</span></span>  
5. <span data-ttu-id="5c7c1-132">Kodlama alanına 'UTF-8' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="5c7c1-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="5c7c1-133">UTF-8</span></span>  
6. <span data-ttu-id="5c7c1-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-134">Click OK.</span></span>
7. <span data-ttu-id="5c7c1-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="5c7c1-136">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="5c7c1-137">İsim alanına 'Mesaj' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="5c7c1-138">İleti</span><span class="sxs-lookup"><span data-stu-id="5c7c1-138">Message</span></span>  
10. <span data-ttu-id="5c7c1-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-139">Click OK.</span></span>
11. <span data-ttu-id="5c7c1-140">Ağaçta, "Xml\İleti" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="5c7c1-141">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-141">Click Add Element.</span></span>
13. <span data-ttu-id="5c7c1-142">İsim alanında 'ProcessingDate' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="5c7c1-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="5c7c1-143">ProcessingDate</span></span>  
14. <span data-ttu-id="5c7c1-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-144">Click OK.</span></span>
15. <span data-ttu-id="5c7c1-145">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-145">Click Add Element.</span></span>
16. <span data-ttu-id="5c7c1-146">İsim alanına 'MessageId' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="5c7c1-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="5c7c1-147">MessageId</span></span>  
17. <span data-ttu-id="5c7c1-148">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-148">Click OK.</span></span>
18. <span data-ttu-id="5c7c1-149">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-149">Click Add Element.</span></span>
19. <span data-ttu-id="5c7c1-150">İsim alanına 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="5c7c1-151">Ödemeler</span><span class="sxs-lookup"><span data-stu-id="5c7c1-151">Payments</span></span>  
20. <span data-ttu-id="5c7c1-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-152">Click OK.</span></span>
21. <span data-ttu-id="5c7c1-153">Ağaçta, "Xml\İleti\Ödemeler" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="5c7c1-154">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-154">Click Add Element.</span></span>
23. <span data-ttu-id="5c7c1-155">İsim alanına 'Madde' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="5c7c1-156">Madde</span><span class="sxs-lookup"><span data-stu-id="5c7c1-156">Item</span></span>  
24. <span data-ttu-id="5c7c1-157">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-157">Click OK.</span></span>
25. <span data-ttu-id="5c7c1-158">Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="5c7c1-159">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="5c7c1-160">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="5c7c1-161">İsim alanına 'Kimlik' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="5c7c1-162">Kod</span><span class="sxs-lookup"><span data-stu-id="5c7c1-162">Id</span></span>  
29. <span data-ttu-id="5c7c1-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-163">Click OK.</span></span>
30. <span data-ttu-id="5c7c1-164">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="5c7c1-165">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="5c7c1-166">İsim alanına bir 'Satıcı' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="5c7c1-167">Satıcı</span><span class="sxs-lookup"><span data-stu-id="5c7c1-167">Vendor</span></span>  
33. <span data-ttu-id="5c7c1-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-168">Click OK.</span></span>
34. <span data-ttu-id="5c7c1-169">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="5c7c1-170">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-170">Click Add Element.</span></span>
36. <span data-ttu-id="5c7c1-171">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="5c7c1-172">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="5c7c1-172">Name</span></span>  
37. <span data-ttu-id="5c7c1-173">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-173">Click OK.</span></span>
38. <span data-ttu-id="5c7c1-174">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-174">Click Add Element.</span></span>
39. <span data-ttu-id="5c7c1-175">İsim alanına 'Banka' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="5c7c1-176">Banka</span><span class="sxs-lookup"><span data-stu-id="5c7c1-176">Bank</span></span>  
40. <span data-ttu-id="5c7c1-177">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-177">Click OK.</span></span>
41. <span data-ttu-id="5c7c1-178">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="5c7c1-179">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-179">Click Add Element.</span></span>
43. <span data-ttu-id="5c7c1-180">İsim alanına 'RoutingNumber' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="5c7c1-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="5c7c1-181">RoutingNumber</span></span>  
44. <span data-ttu-id="5c7c1-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-182">Click OK.</span></span>
45. <span data-ttu-id="5c7c1-183">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-183">Click Add Element.</span></span>
46. <span data-ttu-id="5c7c1-184">İsim alanına 'AccountNumber' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="5c7c1-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="5c7c1-185">AccountNumber</span></span>  
47. <span data-ttu-id="5c7c1-186">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-186">Click OK.</span></span>
48. <span data-ttu-id="5c7c1-187">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="5c7c1-188">Kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-188">Click Copy.</span></span>
50. <span data-ttu-id="5c7c1-189">Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="5c7c1-190">Yapıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-190">Click Paste.</span></span>
52. <span data-ttu-id="5c7c1-191">İsim alanına 'Ödeyen' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="5c7c1-192">Ödeyen</span><span class="sxs-lookup"><span data-stu-id="5c7c1-192">Payer</span></span>  
53. <span data-ttu-id="5c7c1-193">Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="5c7c1-194">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-194">Click Add Element.</span></span>
55. <span data-ttu-id="5c7c1-195">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="5c7c1-196">Para birimi</span><span class="sxs-lookup"><span data-stu-id="5c7c1-196">Currency</span></span>  
56. <span data-ttu-id="5c7c1-197">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-197">Click OK.</span></span>
57. <span data-ttu-id="5c7c1-198">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-198">Click Add Element.</span></span>
58. <span data-ttu-id="5c7c1-199">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="5c7c1-200">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5c7c1-200">Description</span></span>  
59. <span data-ttu-id="5c7c1-201">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-201">Click OK.</span></span>
60. <span data-ttu-id="5c7c1-202">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-202">Click Add Element.</span></span>
61. <span data-ttu-id="5c7c1-203">İsim alanına 'TransDate' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="5c7c1-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="5c7c1-204">TransDate</span></span>  
62. <span data-ttu-id="5c7c1-205">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-205">Click OK.</span></span>
63. <span data-ttu-id="5c7c1-206">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-206">Click Add Element.</span></span>
64. <span data-ttu-id="5c7c1-207">İsim alanına 'Tutar' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="5c7c1-208">Tutar</span><span class="sxs-lookup"><span data-stu-id="5c7c1-208">Amount</span></span>  
65. <span data-ttu-id="5c7c1-209">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="5c7c1-210">Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın</span><span class="sxs-lookup"><span data-stu-id="5c7c1-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="5c7c1-211">Ağaçta, "Xml\İleti\ProcessingDate" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="5c7c1-212">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="5c7c1-213">Ağaçta, "Metin\DateTime" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="5c7c1-214">Biçim alanına 'gün-ay-yıl' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="5c7c1-215">gg.AA.yyyy</span><span class="sxs-lookup"><span data-stu-id="5c7c1-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="5c7c1-216">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-216">Click OK.</span></span>
6. <span data-ttu-id="5c7c1-217">Ağaçta, "Xml\İleti\Ödemeler\Madde\TransDate" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="5c7c1-218">Tarih/Saat Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="5c7c1-219">Biçim alanına 'gün-ay-yıl' yazın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="5c7c1-220">gg.AA.yyyy</span><span class="sxs-lookup"><span data-stu-id="5c7c1-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="5c7c1-221">Tarih/Saat türü alanında "Tarih" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="5c7c1-222">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-222">Click OK.</span></span>
11. <span data-ttu-id="5c7c1-223">Ağaçta, "Xml\İleti\MessageId" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="5c7c1-224">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="5c7c1-225">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="5c7c1-226">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-226">Click OK.</span></span>
15. <span data-ttu-id="5c7c1-227">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="5c7c1-228">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-228">Click Add String.</span></span>
17. <span data-ttu-id="5c7c1-229">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-229">Click OK.</span></span>
18. <span data-ttu-id="5c7c1-230">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="5c7c1-231">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-231">Click Add String.</span></span>
20. <span data-ttu-id="5c7c1-232">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-232">Click OK.</span></span>
21. <span data-ttu-id="5c7c1-233">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="5c7c1-234">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-234">Click Add String.</span></span>
23. <span data-ttu-id="5c7c1-235">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-235">Click OK.</span></span>
24. <span data-ttu-id="5c7c1-236">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Ad" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="5c7c1-237">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-237">Click Add String.</span></span>
26. <span data-ttu-id="5c7c1-238">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-238">Click OK.</span></span>
27. <span data-ttu-id="5c7c1-239">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="5c7c1-240">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-240">Click Add String.</span></span>
29. <span data-ttu-id="5c7c1-241">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-241">Click OK.</span></span>
30. <span data-ttu-id="5c7c1-242">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="5c7c1-243">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-243">Click Add String.</span></span>
32. <span data-ttu-id="5c7c1-244">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-244">Click OK.</span></span>
33. <span data-ttu-id="5c7c1-245">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="5c7c1-246">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-246">Click Add String.</span></span>
35. <span data-ttu-id="5c7c1-247">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-247">Click OK.</span></span>
36. <span data-ttu-id="5c7c1-248">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="5c7c1-249">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-249">Click Add String.</span></span>
38. <span data-ttu-id="5c7c1-250">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-250">Click OK.</span></span>
39. <span data-ttu-id="5c7c1-251">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="5c7c1-252">Dize Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-252">Click Add String.</span></span>
41. <span data-ttu-id="5c7c1-253">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-253">Click OK.</span></span>
42. <span data-ttu-id="5c7c1-254">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-254">Click Save.</span></span>
43. <span data-ttu-id="5c7c1-255">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c7c1-255">Close the page.</span></span>


