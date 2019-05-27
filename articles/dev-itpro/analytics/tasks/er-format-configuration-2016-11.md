---
title: ER Biçim yapılandırması oluşturma (Kasım 2016)
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir.
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544783"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="e4528-103">ER Biçim yapılandırması oluşturma (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="e4528-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4528-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, Elektronik Raporlama (ER) için bir format yapılandırması seçebilir.</span><span class="sxs-lookup"><span data-stu-id="e4528-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="e4528-105">Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4528-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="e4528-106">Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4528-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="e4528-107">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4528-107">Create a new format configuration</span></span>
1. <span data-ttu-id="e4528-108">**Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="e4528-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="e4528-109">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="e4528-110">Ağaçta, **Ödemeler (Basitleştirilmiş model)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="e4528-111">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e4528-112">**Yapılandırma oluştur**'u görmüyorsanız, tasarım modunu **Elektronik raporlama parametreleri** sayfasında etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4528-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="e4528-113">**Yeni** alanına, **Biçim veri modeline PaymentModel dayalı** girin.</span><span class="sxs-lookup"><span data-stu-id="e4528-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="e4528-114">**İsim** alanına, **BACS (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="e4528-115">**Açıklama** alanına, **BACS Satıcı ödeme biçimi (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="e4528-116">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="e4528-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="e4528-117">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4528-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e4528-118">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="e4528-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="e4528-119">Elektronik belgenin belirli bir biçimi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e4528-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="e4528-120">Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="e4528-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="e4528-121">**Veri modeli tanımı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="e4528-122">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-122">Click **Create configuration**.</span></span> <span data-ttu-id="e4528-123">Yeni bir yapılandırma oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="e4528-123">A new configuration has been created.</span></span> <span data-ttu-id="e4528-124">Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4528-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="e4528-125">Elektronik belgenin biçimini tasarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="e4528-126">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-126">Click **Designer**.</span></span>
2. <span data-ttu-id="e4528-127">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="e4528-128">Ağaçta seçin **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="e4528-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="e4528-129">**İsim** alanına **Xml** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="e4528-130">**Kodlama** alanına **UTF-8** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="e4528-131">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-131">Click **OK**.</span></span>
7. <span data-ttu-id="e4528-132">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-132">Click **Add**.</span></span>
8. <span data-ttu-id="e4528-133">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="e4528-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="e4528-134">**İsim** alanına **Mesaj** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="e4528-135">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-135">Click **OK**.</span></span>
11. <span data-ttu-id="e4528-136">Ağaçta, **Xml\İleti** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="e4528-137">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="e4528-138">**İsim** alanında **ProcessingDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="e4528-139">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-139">Click **OK**.</span></span>
15. <span data-ttu-id="e4528-140">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="e4528-141">İsim alanına **MessageId** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="e4528-142">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-142">Click **OK**.</span></span>
18. <span data-ttu-id="e4528-143">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="e4528-144">**İsim** alanına **Ödemeler** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="e4528-145">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-145">Click **OK**.</span></span>
21. <span data-ttu-id="e4528-146">Ağaçta, **Xml\İleti\Ödemeler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="e4528-147">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="e4528-148">**İsim** alanına **Öğe** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="e4528-149">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-149">Click **OK**.</span></span>
25. <span data-ttu-id="e4528-150">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="e4528-151">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-151">Click **Add**.</span></span>
27. <span data-ttu-id="e4528-152">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="e4528-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="e4528-153">İsim alanına **Kimlik** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="e4528-154">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-154">Click **OK**.</span></span>
30. <span data-ttu-id="e4528-155">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-155">Click **Add**.</span></span>
31. <span data-ttu-id="e4528-156">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="e4528-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="e4528-157">İsim alanına bir **Satıcı** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="e4528-158">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-158">Click **OK**.</span></span>
34. <span data-ttu-id="e4528-159">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="e4528-160">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="e4528-161">İsim alanında **İsim** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="e4528-162">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-162">Click **OK**.</span></span>
38. <span data-ttu-id="e4528-163">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="e4528-164">**İsim** alanına **Banka** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="e4528-165">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-165">Click **OK**.</span></span>
41. <span data-ttu-id="e4528-166">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="e4528-167">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="e4528-168">**İsim** alanına **RoutingNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="e4528-169">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-169">Click **OK**.</span></span>
45. <span data-ttu-id="e4528-170">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="e4528-171">**İsim** alanına **AccountNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="e4528-172">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-172">Click **OK**.</span></span>
48. <span data-ttu-id="e4528-173">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="e4528-174">**Kopyala**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-174">Click **Copy**.</span></span>
50. <span data-ttu-id="e4528-175">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="e4528-176">**Yapıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-176">Click **Paste**.</span></span>
52. <span data-ttu-id="e4528-177">**İsim** alanına **Ödeyen** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="e4528-178">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="e4528-179">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="e4528-180">**İsim** alanına **Para birimi** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="e4528-181">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-181">Click **OK**.</span></span>
57. <span data-ttu-id="e4528-182">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="e4528-183">**İsim** alanına **Açıklama** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="e4528-184">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-184">Click **OK**.</span></span>
60. <span data-ttu-id="e4528-185">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="e4528-186">İsim alanına **TransDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="e4528-187">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-187">Click **OK**.</span></span>
63. <span data-ttu-id="e4528-188">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="e4528-189">İsim alanına **Tutar** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="e4528-190">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="e4528-191">Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın</span><span class="sxs-lookup"><span data-stu-id="e4528-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="e4528-192">Ağaçta, **Xml\İleti\ProcessingDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="e4528-193">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="e4528-194">Ağaçta, **Metin\DateTime** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="e4528-195">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="e4528-196">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-196">Click **OK**.</span></span>
6. <span data-ttu-id="e4528-197">Ağaçta, **Xml\İleti\Ödemeler\Madde\TransDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="e4528-198">**Tarih/Saat Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="e4528-199">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="e4528-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="e4528-200">**DateTime** türü alanında **Tarih** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="e4528-201">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-201">Click **OK**.</span></span>
11. <span data-ttu-id="e4528-202">Ağaçta, **Xml\İleti\MessageId** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="e4528-203">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="e4528-204">Ağaçta seçin **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="e4528-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="e4528-205">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-205">Click **OK**.</span></span>
15. <span data-ttu-id="e4528-206">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="e4528-207">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-207">Click **Add String**.</span></span>
17. <span data-ttu-id="e4528-208">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-208">Click **OK**.</span></span>
18. <span data-ttu-id="e4528-209">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="e4528-210">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-210">Click **Add String**.</span></span>
20. <span data-ttu-id="e4528-211">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-211">Click **OK**.</span></span>
21. <span data-ttu-id="e4528-212">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="e4528-213">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-213">Click **Add String**.</span></span>
23. <span data-ttu-id="e4528-214">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-214">Click **OK**.</span></span>
24. <span data-ttu-id="e4528-215">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="e4528-216">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-216">Click **Add String**.</span></span>
26. <span data-ttu-id="e4528-217">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-217">Click **OK**.</span></span>
27. <span data-ttu-id="e4528-218">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="e4528-219">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-219">Click **Add String**.</span></span>
29. <span data-ttu-id="e4528-220">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-220">Click **OK**.</span></span>
30. <span data-ttu-id="e4528-221">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="e4528-222">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-222">Click **Add String**.</span></span>
32. <span data-ttu-id="e4528-223">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-223">Click **OK**.</span></span>
33. <span data-ttu-id="e4528-224">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="e4528-225">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-225">Click **Add String**.</span></span>
35. <span data-ttu-id="e4528-226">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-226">Click **OK**.</span></span>
36. <span data-ttu-id="e4528-227">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="e4528-228">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-228">Click **Add String**.</span></span>
38. <span data-ttu-id="e4528-229">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-229">Click **OK**.</span></span>
39. <span data-ttu-id="e4528-230">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4528-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="e4528-231">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-231">Click **Add String**.</span></span>
41. <span data-ttu-id="e4528-232">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-232">Click **OK**.</span></span>
42. <span data-ttu-id="e4528-233">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4528-233">Click **Save**.</span></span>
43. <span data-ttu-id="e4528-234">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4528-234">Close the page.</span></span>

