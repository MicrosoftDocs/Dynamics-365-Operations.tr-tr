---
title: ER Biçim yapılandırması oluşturma (Kasım 2016)
description: Bu konu, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının nasıl Elektronik Raporlama (ER) için bir format yapılandırması oluşturabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: af2899da843967bfaaa8f3c66906fc8e3765b573
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142513"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="dd336-103">ER Biçim yapılandırması oluşturma (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="dd336-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd336-104">Bu konu, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının nasıl Elektronik Raporlama (ER) için bir format yapılandırması oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="dd336-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="dd336-105">Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="dd336-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="dd336-106">Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd336-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="dd336-107">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd336-107">Create a new format configuration</span></span>
1. <span data-ttu-id="dd336-108">**Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="dd336-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="dd336-109">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="dd336-110">Ağaçta, **Ödemeler (Basitleştirilmiş model)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="dd336-111">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="dd336-112">**Yapılandırma oluştur**'u görmüyorsanız, tasarım modunu **Elektronik raporlama parametreleri** sayfasında etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd336-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="dd336-113">**Yeni** alanına, **Biçim veri modeline PaymentModel dayalı** girin.</span><span class="sxs-lookup"><span data-stu-id="dd336-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="dd336-114">**İsim** alanına, **BACS (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="dd336-115">**Açıklama** alanına, **BACS Satıcı ödeme biçimi (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="dd336-116">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="dd336-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="dd336-117">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="dd336-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="dd336-118">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="dd336-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="dd336-119">Elektronik belgenin belirli bir biçimi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="dd336-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="dd336-120">Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="dd336-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="dd336-121">**Veri modeli tanımı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="dd336-122">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-122">Click **Create configuration**.</span></span> <span data-ttu-id="dd336-123">Yeni bir yapılandırma oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="dd336-123">A new configuration has been created.</span></span> <span data-ttu-id="dd336-124">Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dd336-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="dd336-125">Elektronik belgenin biçimini tasarlayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="dd336-126">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-126">Click **Designer**.</span></span>
2. <span data-ttu-id="dd336-127">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="dd336-128">Ağaçta seçin **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="dd336-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="dd336-129">**İsim** alanına **Xml** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="dd336-130">**Kodlama** alanına **UTF-8** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="dd336-131">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-131">Click **OK**.</span></span>
7. <span data-ttu-id="dd336-132">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-132">Click **Add**.</span></span>
8. <span data-ttu-id="dd336-133">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="dd336-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="dd336-134">**İsim** alanına **Mesaj** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="dd336-135">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-135">Click **OK**.</span></span>
11. <span data-ttu-id="dd336-136">Ağaçta, **Xml\İleti** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="dd336-137">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="dd336-138">**İsim** alanında **ProcessingDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="dd336-139">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-139">Click **OK**.</span></span>
15. <span data-ttu-id="dd336-140">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="dd336-141">İsim alanına **MessageId** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="dd336-142">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-142">Click **OK**.</span></span>
18. <span data-ttu-id="dd336-143">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="dd336-144">**İsim** alanına **Ödemeler** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="dd336-145">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-145">Click **OK**.</span></span>
21. <span data-ttu-id="dd336-146">Ağaçta, **Xml\İleti\Ödemeler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="dd336-147">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="dd336-148">**İsim** alanına **Öğe** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="dd336-149">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-149">Click **OK**.</span></span>
25. <span data-ttu-id="dd336-150">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="dd336-151">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-151">Click **Add**.</span></span>
27. <span data-ttu-id="dd336-152">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="dd336-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="dd336-153">İsim alanına **Kimlik** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="dd336-154">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-154">Click **OK**.</span></span>
30. <span data-ttu-id="dd336-155">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-155">Click **Add**.</span></span>
31. <span data-ttu-id="dd336-156">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="dd336-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="dd336-157">İsim alanına bir **Satıcı** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="dd336-158">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-158">Click **OK**.</span></span>
34. <span data-ttu-id="dd336-159">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="dd336-160">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="dd336-161">İsim alanında **İsim** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="dd336-162">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-162">Click **OK**.</span></span>
38. <span data-ttu-id="dd336-163">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="dd336-164">**İsim** alanına **Banka** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="dd336-165">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-165">Click **OK**.</span></span>
41. <span data-ttu-id="dd336-166">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="dd336-167">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="dd336-168">**İsim** alanına **RoutingNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="dd336-169">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-169">Click **OK**.</span></span>
45. <span data-ttu-id="dd336-170">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="dd336-171">**İsim** alanına **AccountNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="dd336-172">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-172">Click **OK**.</span></span>
48. <span data-ttu-id="dd336-173">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="dd336-174">**Kopyala**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-174">Click **Copy**.</span></span>
50. <span data-ttu-id="dd336-175">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="dd336-176">**Yapıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-176">Click **Paste**.</span></span>
52. <span data-ttu-id="dd336-177">**İsim** alanına **Ödeyen** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="dd336-178">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="dd336-179">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="dd336-180">**İsim** alanına **Para birimi** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="dd336-181">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-181">Click **OK**.</span></span>
57. <span data-ttu-id="dd336-182">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="dd336-183">**İsim** alanına **Açıklama** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="dd336-184">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-184">Click **OK**.</span></span>
60. <span data-ttu-id="dd336-185">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="dd336-186">İsim alanına **TransDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="dd336-187">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-187">Click **OK**.</span></span>
63. <span data-ttu-id="dd336-188">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="dd336-189">İsim alanına **Tutar** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="dd336-190">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="dd336-191">Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın</span><span class="sxs-lookup"><span data-stu-id="dd336-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="dd336-192">Ağaçta, **Xml\İleti\ProcessingDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="dd336-193">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="dd336-194">Ağaçta, **Metin\DateTime** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="dd336-195">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="dd336-196">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-196">Click **OK**.</span></span>
6. <span data-ttu-id="dd336-197">Ağaçta, **Xml\İleti\Ödemeler\Madde\TransDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="dd336-198">**Tarih/Saat Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="dd336-199">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="dd336-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="dd336-200">**DateTime** türü alanında **Tarih** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="dd336-201">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-201">Click **OK**.</span></span>
11. <span data-ttu-id="dd336-202">Ağaçta, **Xml\İleti\MessageId** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="dd336-203">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="dd336-204">Ağaçta seçin **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="dd336-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="dd336-205">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-205">Click **OK**.</span></span>
15. <span data-ttu-id="dd336-206">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="dd336-207">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-207">Click **Add String**.</span></span>
17. <span data-ttu-id="dd336-208">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-208">Click **OK**.</span></span>
18. <span data-ttu-id="dd336-209">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="dd336-210">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-210">Click **Add String**.</span></span>
20. <span data-ttu-id="dd336-211">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-211">Click **OK**.</span></span>
21. <span data-ttu-id="dd336-212">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="dd336-213">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-213">Click **Add String**.</span></span>
23. <span data-ttu-id="dd336-214">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-214">Click **OK**.</span></span>
24. <span data-ttu-id="dd336-215">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="dd336-216">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-216">Click **Add String**.</span></span>
26. <span data-ttu-id="dd336-217">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-217">Click **OK**.</span></span>
27. <span data-ttu-id="dd336-218">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="dd336-219">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-219">Click **Add String**.</span></span>
29. <span data-ttu-id="dd336-220">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-220">Click **OK**.</span></span>
30. <span data-ttu-id="dd336-221">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="dd336-222">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-222">Click **Add String**.</span></span>
32. <span data-ttu-id="dd336-223">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-223">Click **OK**.</span></span>
33. <span data-ttu-id="dd336-224">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="dd336-225">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-225">Click **Add String**.</span></span>
35. <span data-ttu-id="dd336-226">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-226">Click **OK**.</span></span>
36. <span data-ttu-id="dd336-227">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="dd336-228">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-228">Click **Add String**.</span></span>
38. <span data-ttu-id="dd336-229">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-229">Click **OK**.</span></span>
39. <span data-ttu-id="dd336-230">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dd336-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="dd336-231">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-231">Click **Add String**.</span></span>
41. <span data-ttu-id="dd336-232">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-232">Click **OK**.</span></span>
42. <span data-ttu-id="dd336-233">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd336-233">Click **Save**.</span></span>
43. <span data-ttu-id="dd336-234">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dd336-234">Close the page.</span></span>

