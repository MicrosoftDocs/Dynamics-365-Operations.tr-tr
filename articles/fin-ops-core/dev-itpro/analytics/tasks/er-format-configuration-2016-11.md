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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4cd3960594ab37ca867792c655cfd28dc332fa9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684775"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="7ac30-103">ER Biçim yapılandırması oluşturma (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="7ac30-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ac30-104">Bu konu, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının nasıl Elektronik Raporlama (ER) için bir format yapılandırması oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="7ac30-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="7ac30-105">Bu format yapılandırması, ödemelerin işlenmesi için kullanılan elektronik belgelerin formatını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7ac30-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="7ac30-106">Bu örnekte, Litware, Inc. örnek şirketi için bir format yapılandırması oluşturacaksınız. Bu adımları tamamlamak için öncelikle "Modeli seçilen veri kaynaklarına eşleştir" prosedürü altındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7ac30-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="7ac30-107">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ac30-107">Create a new format configuration</span></span>
1. <span data-ttu-id="7ac30-108">**Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="7ac30-109">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="7ac30-110">Ağaçta, **Ödemeler (Basitleştirilmiş model)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="7ac30-111">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7ac30-112">**Yapılandırma oluştur**'u görmüyorsanız, tasarım modunu **Elektronik raporlama parametreleri** sayfasında etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7ac30-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="7ac30-113">**Yeni** alanına, **Biçim veri modeline PaymentModel dayalı** girin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="7ac30-114">**İsim** alanına, **BACS (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="7ac30-115">**Açıklama** alanına, **BACS Satıcı ödeme biçimi (UK hayali)** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="7ac30-116">Etkin yapılandırma sağlayıcısı otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="7ac30-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="7ac30-117">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7ac30-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="7ac30-118">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="7ac30-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="7ac30-119">Elektronik belgenin belirli bir biçimi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7ac30-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="7ac30-120">Çalışma zamanında bir biçim seçmek isterseniz, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="7ac30-121">**Veri modeli tanımı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="7ac30-122">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-122">Click **Create configuration**.</span></span> <span data-ttu-id="7ac30-123">Yeni bir yapılandırma oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="7ac30-123">A new configuration has been created.</span></span> <span data-ttu-id="7ac30-124">Taslak sürümü, elektronik belgeleri yönetmek için tasarım biçimini saklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7ac30-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="7ac30-125">Elektronik belgenin biçimini tasarlayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="7ac30-126">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-126">Click **Designer**.</span></span>
2. <span data-ttu-id="7ac30-127">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="7ac30-128">Ağaçta seçin **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="7ac30-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="7ac30-129">**İsim** alanına **Xml** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="7ac30-130">**Kodlama** alanına **UTF-8** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="7ac30-131">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-131">Click **OK**.</span></span>
7. <span data-ttu-id="7ac30-132">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-132">Click **Add**.</span></span>
8. <span data-ttu-id="7ac30-133">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="7ac30-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="7ac30-134">**İsim** alanına **Mesaj** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="7ac30-135">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-135">Click **OK**.</span></span>
11. <span data-ttu-id="7ac30-136">Ağaçta, **Xml\İleti** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="7ac30-137">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="7ac30-138">**İsim** alanında **ProcessingDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="7ac30-139">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-139">Click **OK**.</span></span>
15. <span data-ttu-id="7ac30-140">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="7ac30-141">İsim alanına **MessageId** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="7ac30-142">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-142">Click **OK**.</span></span>
18. <span data-ttu-id="7ac30-143">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="7ac30-144">**İsim** alanına **Ödemeler** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="7ac30-145">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-145">Click **OK**.</span></span>
21. <span data-ttu-id="7ac30-146">Ağaçta, **Xml\İleti\Ödemeler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="7ac30-147">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="7ac30-148">**İsim** alanına **Öğe** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="7ac30-149">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-149">Click **OK**.</span></span>
25. <span data-ttu-id="7ac30-150">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="7ac30-151">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-151">Click **Add**.</span></span>
27. <span data-ttu-id="7ac30-152">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="7ac30-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="7ac30-153">İsim alanına **Kimlik** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="7ac30-154">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-154">Click **OK**.</span></span>
30. <span data-ttu-id="7ac30-155">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-155">Click **Add**.</span></span>
31. <span data-ttu-id="7ac30-156">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="7ac30-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="7ac30-157">İsim alanına bir **Satıcı** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="7ac30-158">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-158">Click **OK**.</span></span>
34. <span data-ttu-id="7ac30-159">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="7ac30-160">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="7ac30-161">İsim alanında **İsim** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="7ac30-162">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-162">Click **OK**.</span></span>
38. <span data-ttu-id="7ac30-163">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="7ac30-164">**İsim** alanına **Banka** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="7ac30-165">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-165">Click **OK**.</span></span>
41. <span data-ttu-id="7ac30-166">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="7ac30-167">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="7ac30-168">**İsim** alanına **RoutingNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="7ac30-169">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-169">Click **OK**.</span></span>
45. <span data-ttu-id="7ac30-170">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="7ac30-171">**İsim** alanına **AccountNumber** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="7ac30-172">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-172">Click **OK**.</span></span>
48. <span data-ttu-id="7ac30-173">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="7ac30-174">**Kopyala**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-174">Click **Copy**.</span></span>
50. <span data-ttu-id="7ac30-175">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="7ac30-176">**Yapıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-176">Click **Paste**.</span></span>
52. <span data-ttu-id="7ac30-177">**İsim** alanına **Ödeyen** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="7ac30-178">Ağaçta, **Xml\İleti\Ödemeler\Madde** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="7ac30-179">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="7ac30-180">**İsim** alanına **Para birimi** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="7ac30-181">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-181">Click **OK**.</span></span>
57. <span data-ttu-id="7ac30-182">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="7ac30-183">**İsim** alanına **Açıklama** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="7ac30-184">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-184">Click **OK**.</span></span>
60. <span data-ttu-id="7ac30-185">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="7ac30-186">İsim alanına **TransDate** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="7ac30-187">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-187">Click **OK**.</span></span>
63. <span data-ttu-id="7ac30-188">**Öğe Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="7ac30-189">İsim alanına **Tutar** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="7ac30-190">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="7ac30-191">Format bileşenlerini veri modeli öğelerine eşleme için hazırlayın</span><span class="sxs-lookup"><span data-stu-id="7ac30-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="7ac30-192">Ağaçta, **Xml\İleti\ProcessingDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="7ac30-193">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="7ac30-194">Ağaçta, **Metin\DateTime** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="7ac30-195">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="7ac30-196">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-196">Click **OK**.</span></span>
6. <span data-ttu-id="7ac30-197">Ağaçta, **Xml\İleti\Ödemeler\Madde\TransDate** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="7ac30-198">**Tarih/Saat Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="7ac30-199">**Biçim** alanına **gün-ay-yıl** yazın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="7ac30-200">**DateTime** türü alanında **Tarih** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="7ac30-201">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-201">Click **OK**.</span></span>
11. <span data-ttu-id="7ac30-202">Ağaçta, **Xml\İleti\MessageId** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="7ac30-203">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="7ac30-204">Ağaçta seçin **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="7ac30-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="7ac30-205">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-205">Click **OK**.</span></span>
15. <span data-ttu-id="7ac30-206">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="7ac30-207">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-207">Click **Add String**.</span></span>
17. <span data-ttu-id="7ac30-208">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-208">Click **OK**.</span></span>
18. <span data-ttu-id="7ac30-209">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="7ac30-210">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-210">Click **Add String**.</span></span>
20. <span data-ttu-id="7ac30-211">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-211">Click **OK**.</span></span>
21. <span data-ttu-id="7ac30-212">Ağaçta, **Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="7ac30-213">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-213">Click **Add String**.</span></span>
23. <span data-ttu-id="7ac30-214">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-214">Click **OK**.</span></span>
24. <span data-ttu-id="7ac30-215">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Ad** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="7ac30-216">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-216">Click **Add String**.</span></span>
26. <span data-ttu-id="7ac30-217">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-217">Click **OK**.</span></span>
27. <span data-ttu-id="7ac30-218">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="7ac30-219">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-219">Click **Add String**.</span></span>
29. <span data-ttu-id="7ac30-220">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-220">Click **OK**.</span></span>
30. <span data-ttu-id="7ac30-221">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="7ac30-222">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-222">Click **Add String**.</span></span>
32. <span data-ttu-id="7ac30-223">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-223">Click **OK**.</span></span>
33. <span data-ttu-id="7ac30-224">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Para Birimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="7ac30-225">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-225">Click **Add String**.</span></span>
35. <span data-ttu-id="7ac30-226">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-226">Click **OK**.</span></span>
36. <span data-ttu-id="7ac30-227">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Açıklama** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="7ac30-228">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-228">Click **Add String**.</span></span>
38. <span data-ttu-id="7ac30-229">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-229">Click **OK**.</span></span>
39. <span data-ttu-id="7ac30-230">Ağaçta, **Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\Tutar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ac30-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="7ac30-231">**Dize Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-231">Click **Add String**.</span></span>
41. <span data-ttu-id="7ac30-232">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-232">Click **OK**.</span></span>
42. <span data-ttu-id="7ac30-233">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-233">Click **Save**.</span></span>
43. <span data-ttu-id="7ac30-234">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7ac30-234">Close the page.</span></span>

