---
title: Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma
description: Bu konu, gelen elektronik belgelerin XML biçiminde ayrıştırılacağı XML özniteliklerini belirleyen ER biçimleri tasarlama hakkında bilgi sağlar.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd5add18f2f1588cef02afae052d29dc1a28face
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748281"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="727b7-103">Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma</span><span class="sxs-lookup"><span data-stu-id="727b7-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="727b7-104">XML biçiminde gelen elektronik belgeleri ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="727b7-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="727b7-105">XML öğelerinin belirli öznitelikleri, tasarlanan ER biçiminde isteğe bağlı olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="727b7-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="727b7-106">Bu tür XML özniteliklerine sahip olan ve olmayan gelen dosyaları doğru şekilde kullanmanıza izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="727b7-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="727b7-107">Bunun ardından, uygulama verilerini güncelleştirmek için bu dosyalardaki içeriği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="727b7-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="727b7-108">Bu özellik hakkında daha fazla bilgi edinmek için 7.5.4.3 BT Al/Geliştir hizmet/çözüm bileşenleri (10677) iş sürecinin bir parçası olan [(RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma](tasks/import-files-xml-format-optional-attributes.md) konusundaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="727b7-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="727b7-109">Bu görev kılavuzu dosyalarını ve ilişkili örnekleri [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="727b7-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="727b7-110">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="727b7-110">Content description</span></span>       | <span data-ttu-id="727b7-111">Dosya</span><span class="sxs-lookup"><span data-stu-id="727b7-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="727b7-112">XML biçiminde örnek dosya</span><span class="sxs-lookup"><span data-stu-id="727b7-112">Sample file in XML format</span></span> | <span data-ttu-id="727b7-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="727b7-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="727b7-114">Görev kılavuzu</span><span class="sxs-lookup"><span data-stu-id="727b7-114">Task guide</span></span>                | <span data-ttu-id="727b7-115">RCS Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma.axtr</span><span class="sxs-lookup"><span data-stu-id="727b7-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="727b7-116">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="727b7-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="727b7-117">Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="727b7-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="727b7-118">Başlamadan önce IncomingDocumentToLearnHowToHandleOptionalAttributes.xml dosyasını Microsoft İndirme Merkezi(https://go.microsoft.com/fwlink/?linkid=874684 )nden indirin ve yerel olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="727b7-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="727b7-119">**Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="727b7-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="727b7-120">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="727b7-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="727b7-121">Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="727b7-122">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="727b7-123">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="727b7-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="727b7-124">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="727b7-125">**Ad** alanına "XML dosyasını içe aktarma modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="727b7-126">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="727b7-127">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-127">Click **Designer**.</span></span>
5. <span data-ttu-id="727b7-128">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="727b7-129">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="727b7-130">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-130">Click **Add**.</span></span>
8. <span data-ttu-id="727b7-131">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="727b7-132">**Ad** alanına "Liste" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="727b7-133">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="727b7-134">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-134">Click **Add**.</span></span>
12.    <span data-ttu-id="727b7-135">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="727b7-136">**Ad** alanına "Kod" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="727b7-137">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="727b7-138">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-138">Click **Add**.</span></span>
16.    <span data-ttu-id="727b7-139">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-139">Click **Save**.</span></span>
17.    <span data-ttu-id="727b7-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-140">Close the page.</span></span>
18.    <span data-ttu-id="727b7-141">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="727b7-142">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="727b7-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="727b7-144">Veri içe aktarma için biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="727b7-144">Create a format for data import</span></span>
1. <span data-ttu-id="727b7-145">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="727b7-146">**Yeni** alanına, "Veri modeline bağlı biçim xml dosyası Modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="727b7-147">**Ad** alanına ' XML dosyasını içe aktarma biçimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-147">In the **Nam** e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="727b7-148">**Veri içe aktarmayı destekler** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="727b7-149">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="727b7-150">Gelen dosyayı XML biçiminde ayrıştırmak için biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="727b7-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="727b7-151">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-151">Click **Designer**.</span></span>
2. <span data-ttu-id="727b7-152">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="727b7-153">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="727b7-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="727b7-154">**Ad** alanına "kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="727b7-155">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-155">Click **OK**.</span></span>
6. <span data-ttu-id="727b7-156">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="727b7-157">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="727b7-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="727b7-158">**Ad** alanına "belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="727b7-159">**Çokluluk** alanında **Bir fazla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="727b7-160">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-160">Click **OK**.</span></span>
11.    <span data-ttu-id="727b7-161">Ağaçta **kök\belge** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="727b7-162">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="727b7-163">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="727b7-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="727b7-164">**Ad** alanına "kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="727b7-165">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-165">Click **OK**.</span></span>
16.    <span data-ttu-id="727b7-166">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="727b7-167">Ayrıştırılmış bilgileri veri modeline kaydetmek için bir biçim eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="727b7-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="727b7-168">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="727b7-169">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-169">Click **New**.</span></span>
3.    <span data-ttu-id="727b7-170">**Tanım** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="727b7-171">**Ad** alanına "Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="727b7-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="727b7-172">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-172">Click **Save**.</span></span>
6.    <span data-ttu-id="727b7-173">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="727b7-174">Ağaçta, **biçim**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="727b7-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="727b7-175">Ağaçta **biçim\root: XML Element(root)**'u genişletin.</span><span class="sxs-lookup"><span data-stu-id="727b7-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="727b7-176">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="727b7-177">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="727b7-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="727b7-178">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="727b7-179">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="727b7-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="727b7-180">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="727b7-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="727b7-181">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="727b7-182">(belge)\kimlik\*\*.</span><span class="sxs-lookup"><span data-stu-id="727b7-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="727b7-183">Ağaçta **List = format.root.document**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="727b7-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="727b7-184">Ağaçta **List = format.root.document\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="727b7-185">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="727b7-186">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-186">Click **Save**.</span></span>
17.    <span data-ttu-id="727b7-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="727b7-188">Biçim eşlemeyi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="727b7-188">Run format mapping</span></span>
1. <span data-ttu-id="727b7-189">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-189">Click **Run**.</span></span>
2. <span data-ttu-id="727b7-190">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="727b7-191">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="727b7-192">Biçim tasarımı 'belge' öğesi için 'kimlik' özniteliğinin varlığını kabul ederken, seçilen dosya içe aktarılmadı ama içe aktarılan dosya böyle bir öznitelik içermiyor.</span><span class="sxs-lookup"><span data-stu-id="727b7-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="727b7-193">Biçim yapısını XML özniteliğini isteğe bağlı olarak işleyecek şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="727b7-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="727b7-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="727b7-194">Close the page.</span></span>
2. <span data-ttu-id="727b7-195">Ağaçta **kök\belge** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="727b7-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="727b7-196">Ağaçta **kök\belge\kimlik** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="727b7-197">**Boş öznitelik alanı** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="727b7-198">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="727b7-199">Test değişikliklerinde biçim eşlemesi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="727b7-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="727b7-200">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="727b7-201">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-201">Click **Run**.</span></span>
3. <span data-ttu-id="727b7-202">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="727b7-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="727b7-203">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="727b7-203">Click **OK**.</span></span>
5. <span data-ttu-id="727b7-204">Oluşturulan dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="727b7-204">Review the generated file.</span></span> <span data-ttu-id="727b7-205">Biçim tasarımı olarak içe aktarılan aynı dosya 'belge' öğesi için 'kimlik' özniteliğini isteğe bağlı olarak kabul etmektedir.</span><span class="sxs-lookup"><span data-stu-id="727b7-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]