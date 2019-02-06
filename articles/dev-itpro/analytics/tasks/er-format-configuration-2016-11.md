--- 
title: "ER Biçim yapılandırması oluşturma (Kasım 2016)"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: tr-tr
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="fc680-103">ER Biçim yapılandırması oluşturma (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="fc680-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc680-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir.</span><span class="sxs-lookup"><span data-stu-id="fc680-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="fc680-105">Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fc680-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="fc680-106">Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc680-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="fc680-107">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc680-107">Create a new format configuration</span></span>
1. <span data-ttu-id="fc680-108">**Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="fc680-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="fc680-109">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="fc680-110">Ağaçta, **Ödemeler (Basitleştirilmiş model)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="fc680-111">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="fc680-112">**Yapılandırma oluştur**'u görmüyorsanız, tasarım modunu **Elektronik raporlama parametreleri** sayfasında etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc680-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="fc680-113">**Yeni** alanına, **Biçim veri modeline PaymentModel dayalı** girin.</span><span class="sxs-lookup"><span data-stu-id="fc680-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="fc680-114">**İsim** alanına, **BACS (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="fc680-115">**Açıklama** alanına, **BACS Satıcı ödeme biçimi (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="fc680-116">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="fc680-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="fc680-117">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="fc680-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="fc680-118">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="fc680-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="fc680-119">Elektronik belgenin belirli bir biçimi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fc680-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="fc680-120">Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="fc680-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="fc680-121">**Veri modeli tanımı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="fc680-122">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-122">Click **Create configuration**.</span></span> <span data-ttu-id="fc680-123">Yeni bir yapılandırma oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="fc680-123">A new configuration has been created.</span></span> <span data-ttu-id="fc680-124">Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fc680-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="fc680-125">**Yapılandırma oluştur**'u görmüyorsanız, tasarım modunu **Elektronik raporlama parametreleri** sayfasında etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc680-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="fc680-126">Elektronik belgenin biçimini tasarlayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="fc680-127">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-127">Click **Designer**.</span></span>
2. <span data-ttu-id="fc680-128">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="fc680-129">Ağaçta seçin **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="fc680-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="fc680-130">**İsim** alanına **Xml** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="fc680-131">**Kodlama** alanına **UTF-8** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="fc680-132">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-132">Click **OK**.</span></span>
7. <span data-ttu-id="fc680-133">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-133">Click **Add**.</span></span>
8. <span data-ttu-id="fc680-134">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="fc680-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="fc680-135">**İsim** alanına **Mesaj** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="fc680-136">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-136">Click **OK**.</span></span>
11. <span data-ttu-id="fc680-137">Ağaçta, **Xml\İleti** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="fc680-138">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="fc680-139">**İsim** alanında **ProcessingDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="fc680-140">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-140">Click **OK**.</span></span>
15. <span data-ttu-id="fc680-141">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="fc680-142">İsim alanına **MessageId** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="fc680-143">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-143">Click **OK**.</span></span>
18. <span data-ttu-id="fc680-144">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="fc680-145">**İsim** alanına **Ödemeler** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="fc680-146">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-146">Click **OK**.</span></span>
21. <span data-ttu-id="fc680-147">Ağaçta, **Xml\İleti\Ödemeler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="fc680-148">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="fc680-149">**İsim** alanına **Öğe** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="fc680-150">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-150">Click **OK**.</span></span>
25. <span data-ttu-id="fc680-151">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="fc680-152">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-152">Click **Add**.</span></span>
27. <span data-ttu-id="fc680-153">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="fc680-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="fc680-154">İsim alanına **Kimlik** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="fc680-155">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-155">Click **OK**.</span></span>
30. <span data-ttu-id="fc680-156">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-156">Click **Add**.</span></span>
31. <span data-ttu-id="fc680-157">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="fc680-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="fc680-158">İsim alanına bir **Satıcı** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="fc680-159">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-159">Click **OK**.</span></span>
34. <span data-ttu-id="fc680-160">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="fc680-161">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="fc680-162">İsim alanında **İsim** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="fc680-163">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-163">Click **OK**.</span></span>
38. <span data-ttu-id="fc680-164">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="fc680-165">**İsim** alanına **Banka** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="fc680-166">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-166">Click **OK**.</span></span>
41. <span data-ttu-id="fc680-167">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="fc680-168">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="fc680-169">**İsim** alanına **RoutingNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="fc680-170">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-170">Click **OK**.</span></span>
45. <span data-ttu-id="fc680-171">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="fc680-172">**İsim** alanına **AccountNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="fc680-173">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-173">Click **OK**.</span></span>
48. <span data-ttu-id="fc680-174">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="fc680-175">**Kopyala**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-175">Click **Copy**.</span></span>
50. <span data-ttu-id="fc680-176">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="fc680-177">**Yapıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-177">Click **Paste**.</span></span>
52. <span data-ttu-id="fc680-178">**İsim** alanına **Ödeyen** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="fc680-179">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="fc680-180">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="fc680-181">**İsim** alanına **Para birimi** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="fc680-182">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-182">Click **OK**.</span></span>
57. <span data-ttu-id="fc680-183">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="fc680-184">**İsim** alanına **Açıklama** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="fc680-185">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-185">Click **OK**.</span></span>
60. <span data-ttu-id="fc680-186">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="fc680-187">İsim alanına **TransDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="fc680-188">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-188">Click **OK**.</span></span>
63. <span data-ttu-id="fc680-189">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="fc680-190">İsim alanına **Tutar** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="fc680-191">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="fc680-192">Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın</span><span class="sxs-lookup"><span data-stu-id="fc680-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="fc680-193">Ağaçta, **Xml\İleti\ProcessingDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="fc680-194">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="fc680-195">Ağaçta, **Metin\DateTime** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="fc680-196">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="fc680-197">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-197">Click **OK**.</span></span>
6. <span data-ttu-id="fc680-198">Ağaçta, **Xml\İleti\Ödemeler\Madde\TransDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="fc680-199">**Tarih/Saat Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="fc680-200">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="fc680-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="fc680-201">**DateTime** türü alanında **Tarih** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="fc680-202">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-202">Click **OK**.</span></span>
11. <span data-ttu-id="fc680-203">Ağaçta, **Xml\İleti\MessageId** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="fc680-204">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="fc680-205">Ağaçta seçin **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="fc680-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="fc680-206">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-206">Click **OK**.</span></span>
15. <span data-ttu-id="fc680-207">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="fc680-208">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-208">Click **Add String**.</span></span>
17. <span data-ttu-id="fc680-209">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-209">Click **OK**.</span></span>
18. <span data-ttu-id="fc680-210">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="fc680-211">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-211">Click **Add String**.</span></span>
20. <span data-ttu-id="fc680-212">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-212">Click **OK**.</span></span>
21. <span data-ttu-id="fc680-213">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="fc680-214">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-214">Click **Add String**.</span></span>
23. <span data-ttu-id="fc680-215">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-215">Click **OK**.</span></span>
24. <span data-ttu-id="fc680-216">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="fc680-217">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-217">Click **Add String**.</span></span>
26. <span data-ttu-id="fc680-218">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-218">Click **OK**.</span></span>
27. <span data-ttu-id="fc680-219">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="fc680-220">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-220">Click **Add String**.</span></span>
29. <span data-ttu-id="fc680-221">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-221">Click **OK**.</span></span>
30. <span data-ttu-id="fc680-222">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="fc680-223">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-223">Click **Add String**.</span></span>
32. <span data-ttu-id="fc680-224">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-224">Click **OK**.</span></span>
33. <span data-ttu-id="fc680-225">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="fc680-226">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-226">Click **Add String**.</span></span>
35. <span data-ttu-id="fc680-227">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-227">Click **OK**.</span></span>
36. <span data-ttu-id="fc680-228">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="fc680-229">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-229">Click **Add String**.</span></span>
38. <span data-ttu-id="fc680-230">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-230">Click **OK**.</span></span>
39. <span data-ttu-id="fc680-231">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc680-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="fc680-232">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-232">Click **Add String**.</span></span>
41. <span data-ttu-id="fc680-233">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-233">Click **OK**.</span></span>
42. <span data-ttu-id="fc680-234">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc680-234">Click **Save**.</span></span>
43. <span data-ttu-id="fc680-235">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fc680-235">Close the page.</span></span>


