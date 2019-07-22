---
title: RCS ve ER için uygulamaya özel meta verileri hazırlama
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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a6fc1e54444584895aa75ae91d39143f27e34d8
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726587"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="b6be9-103">RCS ve ER için uygulamaya özel meta verileri hazırlama</span><span class="sxs-lookup"><span data-stu-id="b6be9-103">Prepare application-specific metadata for RCS and ER</span></span>

<span data-ttu-id="b6be9-104">XML biçiminde gelen elektronik belgeleri ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6be9-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="b6be9-105">XML öğelerinin belirli öznitelikleri, tasarlanan ER biçiminde isteğe bağlı olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="b6be9-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="b6be9-106">Bu tür XML özniteliklerine sahip olan ve olmayan gelen dosyaları doğru şekilde kullanmanıza izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="b6be9-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="b6be9-107">Bunun ardından, uygulama verilerini güncelleştirmek için bu dosyalardaki içeriği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6be9-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="b6be9-108">Bu özellik hakkında daha fazla bilgi edinmek için, 7.5.4.3 BT Al/Geliştir hizmet/çözüm bileşenleri (10677) iş sürecinin bir parçası olan [RCS Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma](tasks/import-files-xml-format-optional-attributes.md) öğesindeki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="b6be9-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="b6be9-109">Bu görev kılavuzu dosyalarını ve ilişkili örnekleri [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6be9-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="b6be9-110">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="b6be9-110">Content description</span></span>       | <span data-ttu-id="b6be9-111">Dosya</span><span class="sxs-lookup"><span data-stu-id="b6be9-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b6be9-112">XML biçiminde örnek dosya</span><span class="sxs-lookup"><span data-stu-id="b6be9-112">Sample file in XML format</span></span> | <span data-ttu-id="b6be9-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="b6be9-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="b6be9-114">Görev kılavuzu</span><span class="sxs-lookup"><span data-stu-id="b6be9-114">Task guide</span></span>                | <span data-ttu-id="b6be9-115">RCS Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma.axtr</span><span class="sxs-lookup"><span data-stu-id="b6be9-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="b6be9-116">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b6be9-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="b6be9-117">Bu adımları tamamlamak için önce [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="b6be9-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="b6be9-118">Başlamadan önce IncomingDocumentToLearnHowToHandleOptionalAttributes.xml dosyasını Microsoft İndirme Merkezi(https://go.microsoft.com/fwlink/?linkid=874684 )nden indirin ve yerel olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="b6be9-119">**Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="b6be9-120">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b6be9-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="b6be9-121">Bu konudaki yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="b6be9-122">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b6be9-123">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="b6be9-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="b6be9-124">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="b6be9-125">**Ad** alanına "XML dosyasını içe aktarma modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="b6be9-126">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="b6be9-127">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-127">Click **Designer**.</span></span>
5. <span data-ttu-id="b6be9-128">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="b6be9-129">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="b6be9-130">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-130">Click **Add**.</span></span>
8. <span data-ttu-id="b6be9-131">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="b6be9-132">**Ad** alanına "Liste" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="b6be9-133">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="b6be9-134">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-134">Click **Add**.</span></span>
12. <span data-ttu-id="b6be9-135">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="b6be9-136">**Ad** alanına "Kod" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="b6be9-137">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="b6be9-138">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-138">Click **Add**.</span></span>
16. <span data-ttu-id="b6be9-139">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-139">Click **Save**.</span></span>
17. <span data-ttu-id="b6be9-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-140">Close the page.</span></span>
18. <span data-ttu-id="b6be9-141">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-141">Click **Change status**.</span></span>
19. <span data-ttu-id="b6be9-142">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-142">Click **Complete**.</span></span>
20. <span data-ttu-id="b6be9-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="b6be9-144">Veri içe aktarma için biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="b6be9-144">Create a format for data import</span></span>
1. <span data-ttu-id="b6be9-145">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="b6be9-146">**Yeni** alanına, "Veri modeline bağlı biçim xml dosyası Modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="b6be9-147">**Ad** alanına ' XML dosyasını içe aktarma biçimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="b6be9-148">**Veri içe aktarmayı destekler** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="b6be9-149">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="b6be9-150">Gelen dosyayı XML biçiminde ayrıştırmak için biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="b6be9-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="b6be9-151">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-151">Click **Designer**.</span></span>
2. <span data-ttu-id="b6be9-152">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="b6be9-153">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="b6be9-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="b6be9-154">**Ad** alanına "kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="b6be9-155">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-155">Click **OK**.</span></span>
6. <span data-ttu-id="b6be9-156">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="b6be9-157">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="b6be9-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="b6be9-158">**Ad** alanına "belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="b6be9-159">**Çokluluk** alanında **Bir fazla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="b6be9-160">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-160">Click **OK**.</span></span>
11. <span data-ttu-id="b6be9-161">Ağaçta **kök\belge** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="b6be9-162">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="b6be9-163">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="b6be9-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="b6be9-164">**Ad** alanına "kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="b6be9-165">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-165">Click **OK**.</span></span>
16. <span data-ttu-id="b6be9-166">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="b6be9-167">Ayrıştırılmış bilgileri veri modeline kaydetmek için bir biçim eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="b6be9-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="b6be9-168">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="b6be9-169">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-169">Click **New**.</span></span>
3.  <span data-ttu-id="b6be9-170">**Tanım** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="b6be9-171">**Ad** alanına "Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="b6be9-172">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-172">Click **Save**.</span></span>
6.  <span data-ttu-id="b6be9-173">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="b6be9-174">Ağaçta, **biçim**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="b6be9-175">Ağaçta **biçim\root: XML Element(root)**'u genişletin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="b6be9-176">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b6be9-177">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="b6be9-177">(document)\*\*.</span></span>
10. <span data-ttu-id="b6be9-178">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-178">Click **Bind**.</span></span>
11. <span data-ttu-id="b6be9-179">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b6be9-180">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="b6be9-180">(document)\*\*.</span></span>
12. <span data-ttu-id="b6be9-181">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b6be9-182">(belge)\kimlik\*\*.</span><span class="sxs-lookup"><span data-stu-id="b6be9-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="b6be9-183">Ağaçta **List = format.root.document**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="b6be9-184">Ağaçta **List = format.root.document\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="b6be9-185">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-185">Click **Bind**.</span></span>
16. <span data-ttu-id="b6be9-186">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-186">Click **Save**.</span></span>
17. <span data-ttu-id="b6be9-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="b6be9-188">Biçim eşlemeyi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b6be9-188">Run format mapping</span></span>
1. <span data-ttu-id="b6be9-189">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-189">Click **Run**.</span></span>
2. <span data-ttu-id="b6be9-190">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="b6be9-191">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="b6be9-192">Biçim tasarımı "belge" öğesi için "kimlik" özniteliğinin varlığını kabul ederken, seçilen dosya içe aktarılmadı ama içe aktarılan dosya böyle bir öznitelik içermiyor.</span><span class="sxs-lookup"><span data-stu-id="b6be9-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="b6be9-193">Biçim yapısını XML özniteliğini isteğe bağlı olarak işleyecek şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="b6be9-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="b6be9-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-194">Close the page.</span></span>
2. <span data-ttu-id="b6be9-195">Ağaçta **kök\belge** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="b6be9-196">Ağaçta **kök\belge\kimlik** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="b6be9-197">**Boş öznitelik alanı** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="b6be9-198">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="b6be9-199">Test değişikliklerinde biçim eşlemesi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="b6be9-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="b6be9-200">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="b6be9-201">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-201">Click **Run**.</span></span>
3. <span data-ttu-id="b6be9-202">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="b6be9-203">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b6be9-203">Click **OK**.</span></span>
5. <span data-ttu-id="b6be9-204">Oluşturulan dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="b6be9-204">Review the generated file.</span></span> <span data-ttu-id="b6be9-205">Biçim tasarımı olarak içe aktarılan aynı dosya "belge" öğesi için "kimlik" özniteliğini isteğe bağlı olarak kabul etmektedir.</span><span class="sxs-lookup"><span data-stu-id="b6be9-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
