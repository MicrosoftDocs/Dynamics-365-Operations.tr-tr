---
title: (RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma
description: Bu konu, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında dosyayı içe aktarmak için ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182198"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="06b55-103">(RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma</span><span class="sxs-lookup"><span data-stu-id="06b55-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06b55-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="06b55-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="06b55-105">Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="06b55-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="06b55-106">Başlamadan önce [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'nden IncomingDocumentToLearnHowToHandleOptionalAttributes.xml dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="06b55-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="06b55-107">**Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="06b55-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="06b55-108">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="06b55-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="06b55-109">Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="06b55-110">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="06b55-111">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="06b55-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="06b55-112">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="06b55-113">**Ad** alanına "XML dosyasını içe aktarma modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="06b55-114">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="06b55-115">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="06b55-116">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="06b55-117">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="06b55-118">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-118">Click **Add**.</span></span>
8.  <span data-ttu-id="06b55-119">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="06b55-120">**Ad** alanına "Liste" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="06b55-121">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="06b55-122">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-122">Click **Add**.</span></span>
12. <span data-ttu-id="06b55-123">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="06b55-124">**Ad** alanına "Kod" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="06b55-125">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="06b55-126">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-126">Click **Add**.</span></span>
16. <span data-ttu-id="06b55-127">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-127">Click **Save**.</span></span>
17. <span data-ttu-id="06b55-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-128">Close the page.</span></span>
18. <span data-ttu-id="06b55-129">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-129">Click **Change status**.</span></span>
19. <span data-ttu-id="06b55-130">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-130">Click **Complete**.</span></span>
20. <span data-ttu-id="06b55-131">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="06b55-132">Veri içe aktarma için biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="06b55-132">Create a format for data import</span></span>
1.  <span data-ttu-id="06b55-133">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="06b55-134">**Yeni** alanına, "Veri modeline bağlı biçim xml dosyası Modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="06b55-135">**Ad** alanına ' XML dosyasını içe aktarma biçimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="06b55-136">**Veri içe aktarmayı destekler** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="06b55-137">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="06b55-138">Gelen dosyayı XML biçiminde ayrıştırmak için biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="06b55-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="06b55-139">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="06b55-140">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="06b55-141">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="06b55-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="06b55-142">**Ad** alanına "kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="06b55-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-143">Click **OK**.</span></span>
6.  <span data-ttu-id="06b55-144">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="06b55-145">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="06b55-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="06b55-146">**Ad** alanına "belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="06b55-147">**Çokluluk** alanında **Bir fazla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="06b55-148">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-148">Click **OK**.</span></span>
11. <span data-ttu-id="06b55-149">Ağaçta **kök\belge** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="06b55-150">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="06b55-151">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="06b55-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="06b55-152">**Ad** alanına "Kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="06b55-153">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-153">Click **OK**.</span></span>
16. <span data-ttu-id="06b55-154">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="06b55-155">Ayrıştırılmış bilgileri veri modeline kaydetmek için bir biçim eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="06b55-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="06b55-156">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="06b55-157">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-157">Click **New**.</span></span>
3. <span data-ttu-id="06b55-158">**Tanım** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="06b55-159">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="06b55-160">**Ad** alanına "Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="06b55-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="06b55-161">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-161">Click **Save**.</span></span>
7. <span data-ttu-id="06b55-162">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-162">Click **Designer**.</span></span>
8. <span data-ttu-id="06b55-163">Ağaçta, **biçim**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="06b55-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="06b55-164">Ağaçta **biçim\root: XML Element(root)**'u genişletin.</span><span class="sxs-lookup"><span data-stu-id="06b55-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="06b55-165">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="06b55-166">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="06b55-166">(document)\*\*.</span></span>
11. <span data-ttu-id="06b55-167">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-167">Click **Bind**.</span></span>
12. <span data-ttu-id="06b55-168">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="06b55-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="06b55-169">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="06b55-169">(document)\*\*.</span></span>
13. <span data-ttu-id="06b55-170">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="06b55-171">(belge)\kimlik\*\*.</span><span class="sxs-lookup"><span data-stu-id="06b55-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="06b55-172">Ağaçta **List = format.root.document**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="06b55-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="06b55-173">Ağaçta **List = format.root.document\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="06b55-174">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-174">Click **Bind**.</span></span>
17. <span data-ttu-id="06b55-175">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-175">Click **Save**.</span></span>
18. <span data-ttu-id="06b55-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="06b55-177">Biçim eşlemeyi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="06b55-177">Run format mapping</span></span>
1. <span data-ttu-id="06b55-178">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-178">Click **Run**.</span></span>
2. <span data-ttu-id="06b55-179">**Gözat**düğmesine tıklayın ve **ıncomingdocumenttolearnhowtohandleoptionalattributes. xml**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="06b55-180">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="06b55-181">Biçim tasarımı "belge" öğesi için "kimlik" özniteliğinin varlığını kabul ederken, seçilen dosya içe aktarılmadı ama içe aktarılan dosya böyle bir öznitelik içermiyor.</span><span class="sxs-lookup"><span data-stu-id="06b55-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="06b55-182">Biçim yapısını XML özniteliğini isteğe bağlı olarak işleyecek şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="06b55-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="06b55-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="06b55-183">Close the page.</span></span>
2. <span data-ttu-id="06b55-184">Ağaçta **kök\belge** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="06b55-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="06b55-185">Ağaçta **kök\belge\kimlik** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="06b55-186">**Boş öznitelik alanı** alanı için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="06b55-187">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="06b55-188">Test değişikliklerinde biçim eşlemesi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="06b55-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="06b55-189">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="06b55-190">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-190">Click **Run**.</span></span>
3. <span data-ttu-id="06b55-191">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="06b55-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="06b55-192">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06b55-192">Click **OK**.</span></span>
5. <span data-ttu-id="06b55-193">Oluşturulan dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="06b55-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="06b55-194">Biçim tasarımı olarak içe aktarılan aynı dosya "belge" öğesi için "kimlik" özniteliğini isteğe bağlı olarak kabul etmektedir.</span><span class="sxs-lookup"><span data-stu-id="06b55-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
