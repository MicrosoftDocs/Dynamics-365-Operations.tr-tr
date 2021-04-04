---
title: (RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma
description: Bu konu, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında dosyayı içe aktarmak için ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef090270b2e521b870697bb238b50ea92d4f6958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565698"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="03e84-103">(RCS) Dosyaları isteğe bağlı özniteliklerle XML biçiminde içe aktarma</span><span class="sxs-lookup"><span data-stu-id="03e84-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03e84-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir kullanıcının isteğe bağlı öznitelikleri içeren XML formatında ER biçimine sahip yapılandırmayı tasarlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="03e84-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="03e84-105">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="03e84-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="03e84-106">Başlamadan önce [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'nden IncomingDocumentToLearnHowToHandleOptionalAttributes.xml dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="03e84-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="03e84-107">**Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="03e84-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="03e84-108">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="03e84-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="03e84-109">Bu yapılandırma sağlayıcısını göremiyorsanız[Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="03e84-110">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="03e84-111">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="03e84-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="03e84-112">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="03e84-113">**Ad** alanına "XML dosyasını içe aktarma modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="03e84-114">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="03e84-115">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="03e84-116">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="03e84-117">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="03e84-118">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-118">Click **Add**.</span></span>
8.    <span data-ttu-id="03e84-119">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="03e84-120">**Ad** alanına "Liste" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="03e84-121">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="03e84-122">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-122">Click **Add**.</span></span>
12.    <span data-ttu-id="03e84-123">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="03e84-124">**Ad** alanına "Kod" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="03e84-125">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="03e84-126">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-126">Click **Add**.</span></span>
16.    <span data-ttu-id="03e84-127">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-127">Click **Save**.</span></span>
17.    <span data-ttu-id="03e84-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-128">Close the page.</span></span>
18.    <span data-ttu-id="03e84-129">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="03e84-130">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="03e84-131">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="03e84-132">Veri içe aktarma için biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="03e84-132">Create a format for data import</span></span>
1.    <span data-ttu-id="03e84-133">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="03e84-134">**Yeni** alanına, "Veri modeline bağlı biçim xml dosyası Modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="03e84-135">**Ad** alanına ' XML dosyasını içe aktarma biçimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="03e84-136">**Veri içe aktarmayı destekler** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="03e84-137">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="03e84-138">Gelen dosyayı XML biçiminde ayrıştırmak için biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="03e84-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="03e84-139">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="03e84-140">İletişim kutusunu açmak için **Kök ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="03e84-141">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="03e84-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="03e84-142">**Ad** alanına "kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="03e84-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-143">Click **OK**.</span></span>
6.    <span data-ttu-id="03e84-144">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="03e84-145">Ağaçta seçin **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="03e84-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="03e84-146">**Ad** alanına "belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="03e84-147">**Çokluluk** alanında **Bir fazla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="03e84-148">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-148">Click **OK**.</span></span>
11.    <span data-ttu-id="03e84-149">Ağaçta **kök\belge** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="03e84-150">Açılır iletişim kutusunu açmak için **Ekle** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="03e84-151">Ağaçta seçin **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="03e84-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="03e84-152">**Ad** alanına "Kimlik" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="03e84-153">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-153">Click **OK**.</span></span>
16.    <span data-ttu-id="03e84-154">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="03e84-155">Ayrıştırılmış bilgileri veri modeline kaydetmek için bir biçim eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="03e84-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="03e84-156">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="03e84-157">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-157">Click **New**.</span></span>
3. <span data-ttu-id="03e84-158">**Tanım** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="03e84-159">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="03e84-160">**Ad** alanına "Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="03e84-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="03e84-161">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-161">Click **Save**.</span></span>
7. <span data-ttu-id="03e84-162">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-162">Click **Designer**.</span></span>
8. <span data-ttu-id="03e84-163">Ağaçta, **biçim**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="03e84-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="03e84-164">Ağaçta **biçim\root: XML Element(root)**'u genişletin.</span><span class="sxs-lookup"><span data-stu-id="03e84-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="03e84-165">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="03e84-166">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="03e84-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="03e84-167">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="03e84-168">Ağaçta \**biçim\root: XML Element(root)\document: XML Element 1..*'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="03e84-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="03e84-169">(belge)\*\*.</span><span class="sxs-lookup"><span data-stu-id="03e84-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="03e84-170">Ağaçta \**biçim\kök: XML Element(root)\document: XML Element 1..*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="03e84-171">(belge)\kimlik\*\*.</span><span class="sxs-lookup"><span data-stu-id="03e84-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="03e84-172">Ağaçta **List = format.root.document**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="03e84-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="03e84-173">Ağaçta **List = format.root.document\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="03e84-174">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="03e84-175">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-175">Click **Save**.</span></span>
18.    <span data-ttu-id="03e84-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="03e84-177">Biçim eşlemeyi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="03e84-177">Run format mapping</span></span>
1. <span data-ttu-id="03e84-178">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-178">Click **Run**.</span></span>
2. <span data-ttu-id="03e84-179">**Gözat** düğmesine tıklayın ve **ıncomingdocumenttolearnhowtohandleoptionalattributes. xml**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="03e84-180">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="03e84-181">Biçim tasarımı 'belge' öğesi için 'kimlik' özniteliğinin varlığını kabul ederken, seçilen dosya içe aktarılmadı ama içe aktarılan dosya böyle bir öznitelik içermiyor.</span><span class="sxs-lookup"><span data-stu-id="03e84-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="03e84-182">Biçim yapısını XML özniteliğini isteğe bağlı olarak işleyecek şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="03e84-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="03e84-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03e84-183">Close the page.</span></span>
2. <span data-ttu-id="03e84-184">Ağaçta **kök\belge** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="03e84-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="03e84-185">Ağaçta **kök\belge\kimlik** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="03e84-186">**Boş öznitelik alanı** alanı için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="03e84-187">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="03e84-188">Test değişikliklerinde biçim eşlemesi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="03e84-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="03e84-189">**Biçimi modelle eşle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="03e84-190">**Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-190">Click **Run**.</span></span>
3. <span data-ttu-id="03e84-191">**Gözat** düğmesine tıklayın ve **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="03e84-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="03e84-192">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03e84-192">Click **OK**.</span></span>
5. <span data-ttu-id="03e84-193">Oluşturulan dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="03e84-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="03e84-194">Biçim tasarımı olarak içe aktarılan aynı dosya "belge" öğesi için "kimlik" özniteliğini isteğe bağlı olarak kabul etmektedir.</span><span class="sxs-lookup"><span data-stu-id="03e84-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]