---
title: Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma
description: Bu konu, gelen elektronik belgelerin XML biçiminde ayrıştırılacağı XML özniteliklerini belirleyen ER biçimleri tasarlama hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182842"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="492bc-103">Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma</span><span class="sxs-lookup"><span data-stu-id="492bc-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="492bc-104">XML biçiminde gelen elektronik belgeleri ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="492bc-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="492bc-105">XML öğelerinin belirli öznitelikleri, tasarlanan ER biçiminde isteğe bağlı olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="492bc-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="492bc-106">Bu tür XML özniteliklerine sahip olan ve olmayan gelen dosyaları doğru şekilde kullanmanıza izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="492bc-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="492bc-107">Bunun ardından, uygulama verilerini güncelleştirmek için bu dosyalardaki içeriği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="492bc-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="492bc-108">Bu özellik hakkında daha fazla bilgi edinmek için, 7.5.4.3 BT Al/Geliştir hizmet/çözüm bileşenleri (10677) iş sürecinin bir parçası olan [RCS Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma](tasks/import-files-xml-format-optional-attributes.md) öğesindeki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="492bc-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="492bc-109">Bu görev kılavuzu dosyalarını ve ilişkili örnekleri [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="492bc-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="492bc-110">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="492bc-110">Content description</span></span>       | <span data-ttu-id="492bc-111">Dosya</span><span class="sxs-lookup"><span data-stu-id="492bc-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="492bc-112">XML biçiminde örnek dosya</span><span class="sxs-lookup"><span data-stu-id="492bc-112">Sample file in XML format</span></span> | <span data-ttu-id="492bc-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="492bc-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="492bc-114">Görev kılavuzu</span><span class="sxs-lookup"><span data-stu-id="492bc-114">Task guide</span></span>                | <span data-ttu-id="492bc-115">RCS Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma.axtr</span><span class="sxs-lookup"><span data-stu-id="492bc-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="492bc-116">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="492bc-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="492bc-117">Bu adımları tamamlamak için önce [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="492bc-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="492bc-118">Başlamadan önce IncomingDocumentToLearnHowToHandleOptionalAttributes.xml dosyasını Microsoft İndirme Merkezi(https://go.microsoft.com/fwlink/?linkid=874684 )nden indirin ve yerel olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="492bc-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="492bc-119">**Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="492bc-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="492bc-120">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="492bc-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="492bc-121">Bu konudaki yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="492bc-122">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="492bc-123">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="492bc-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="492bc-124">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="492bc-125">**Ad** alanına "XML dosyasını içe aktarma modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="492bc-126">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="492bc-127">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-127">Click **Designer**.</span></span>
5. <span data-ttu-id="492bc-128">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="492bc-129">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="492bc-130">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-130">Click **Add**.</span></span>
8. <span data-ttu-id="492bc-131">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="492bc-132">**Ad** alanına "Liste" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="492bc-133">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="492bc-134">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-134">Click **Add**.</span></span>
12. <span data-ttu-id="492bc-135">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="492bc-136">**Ad** alanına "Kod" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="492bc-137">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="492bc-138">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-138">Click **Add**.</span></span>
16. <span data-ttu-id="492bc-139">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-139">Click **Save**.</span></span>
17. <span data-ttu-id="492bc-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-140">Close the page.</span></span>
18. <span data-ttu-id="492bc-141">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-141">Click **Change status**.</span></span>
19. <span data-ttu-id="492bc-142">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-142">Click **Complete**.</span></span>
20. <span data-ttu-id="492bc-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="492bc-144">Veri içe aktarma için biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="492bc-144">Create a format for data import</span></span>
1. <span data-ttu-id="492bc-145">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="492bc-146">**Yeni** alanına, "Veri modeline bağlı biçim xml dosyası Modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="492bc-147">**Ad** alanına ' XML dosyasını içe aktarma biçimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="492bc-148">**Veri içe aktarmayı destekler** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="492bc-149">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="492bc-150">Gelen dosyayı XML biçiminde ayrıştırmak için biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="492bc-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="492bc-151">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-151">Click **Designer**.</span></span>
2. <span data-ttu-id="492bc-152">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="492bc-153">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="492bc-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="492bc-154">**Ad** alanına "kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="492bc-155">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-155">Click **OK**.</span></span>
6. <span data-ttu-id="492bc-156">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="492bc-157">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="492bc-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="492bc-158">**Ad** alanına "belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="492bc-159">**Çokluluk** alanında **Bir fazla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="492bc-160">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-160">Click **OK**.</span></span>
11. <span data-ttu-id="492bc-161">Ağaçta **kök\belge** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="492bc-162">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="492bc-163">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="492bc-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="492bc-164">**Ad** alanına "kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="492bc-165">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-165">Click **OK**.</span></span>
16. <span data-ttu-id="492bc-166">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="492bc-167">Ayrıştırılmış bilgileri veri modeline kaydetmek için bir biçim eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="492bc-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="492bc-168">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="492bc-169">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-169">Click **New**.</span></span>
3.  <span data-ttu-id="492bc-170">**Tanım** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="492bc-171">**Ad** alanına "Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="492bc-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="492bc-172">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-172">Click **Save**.</span></span>
6.  <span data-ttu-id="492bc-173">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="492bc-174">Ağaçta, **biçim**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="492bc-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="492bc-175">Ağaçta **biçim\root: XML Element(root)**'u genişletin.</span><span class="sxs-lookup"><span data-stu-id="492bc-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="492bc-176">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="492bc-177">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="492bc-177">(document)\*\*.</span></span>
10. <span data-ttu-id="492bc-178">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-178">Click **Bind**.</span></span>
11. <span data-ttu-id="492bc-179">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="492bc-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="492bc-180">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="492bc-180">(document)\*\*.</span></span>
12. <span data-ttu-id="492bc-181">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="492bc-182">(belge)\kimlik\*\*.</span><span class="sxs-lookup"><span data-stu-id="492bc-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="492bc-183">Ağaçta **List = format.root.document**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="492bc-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="492bc-184">Ağaçta **List = format.root.document\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="492bc-185">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-185">Click **Bind**.</span></span>
16. <span data-ttu-id="492bc-186">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-186">Click **Save**.</span></span>
17. <span data-ttu-id="492bc-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="492bc-188">Biçim eşlemeyi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="492bc-188">Run format mapping</span></span>
1. <span data-ttu-id="492bc-189">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-189">Click **Run**.</span></span>
2. <span data-ttu-id="492bc-190">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="492bc-191">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="492bc-192">Biçim tasarımı "belge" öğesi için "kimlik" özniteliğinin varlığını kabul ederken, seçilen dosya içe aktarılmadı ama içe aktarılan dosya böyle bir öznitelik içermiyor.</span><span class="sxs-lookup"><span data-stu-id="492bc-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="492bc-193">Biçim yapısını XML özniteliğini isteğe bağlı olarak işleyecek şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="492bc-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="492bc-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="492bc-194">Close the page.</span></span>
2. <span data-ttu-id="492bc-195">Ağaçta **kök\belge** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="492bc-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="492bc-196">Ağaçta **kök\belge\kimlik** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="492bc-197">**Boş öznitelik alanı** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="492bc-198">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="492bc-199">Test değişikliklerinde biçim eşlemesi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="492bc-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="492bc-200">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="492bc-201">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-201">Click **Run**.</span></span>
3. <span data-ttu-id="492bc-202">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="492bc-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="492bc-203">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492bc-203">Click **OK**.</span></span>
5. <span data-ttu-id="492bc-204">Oluşturulan dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="492bc-204">Review the generated file.</span></span> <span data-ttu-id="492bc-205">Biçim tasarımı olarak içe aktarılan aynı dosya "belge" öğesi için "kimlik" özniteliğini isteğe bağlı olarak kabul etmektedir.</span><span class="sxs-lookup"><span data-stu-id="492bc-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
