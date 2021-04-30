---
title: İş belgesi yönetiminde Microsoft Office stili kullanıcı arabirimi
description: Bu konu, Elektronik raporlama (ER) çerçevesinin İş belgesi yönetimi özelliğindeki yeni kullanıcı arabiriminin nasıl kullanılacağı hakkında bilgi vermektedir.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881048"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="c98c2-103">İş belgesi yönetiminde Microsoft Office stili kullanıcı arabirimi</span><span class="sxs-lookup"><span data-stu-id="c98c2-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c98c2-104">İş belgesi yönetimi iş kullanıcılarının Microsoft 365 hizmeti veya uygun Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="c98c2-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="c98c2-105">Düzenlemeler tasarım değişiklikleri veya yeni dağıtımlar içerebilir ya da kullanıcılar kaynak kodunu değiştirmeden ek veri eklemek için yer tutucular ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="c98c2-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="c98c2-106">İş belgesi yönetimiyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="c98c2-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="c98c2-107">Yeni kullanıcı arabirimi (UI) daha net ve kullanımı daha rahat.</span><span class="sxs-lookup"><span data-stu-id="c98c2-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="c98c2-108">**İş belgesi** alanı, yalnızca, geçerli sağlayıcı için kullanılabilen şablonları gösterir.</span><span class="sxs-lookup"><span data-stu-id="c98c2-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="c98c2-109">Önceki kullanıcı arabiriminde, **Şablon** sekmesi sağlayıcılar için kullanılabilir olan tüm şablonları listeliyordu.</span><span class="sxs-lookup"><span data-stu-id="c98c2-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="c98c2-110">Aynı role sahip herhangi bir kullanıcı tarafından oluşturulan ve düzenlenen tüm şablonları da gösteriyordu.</span><span class="sxs-lookup"><span data-stu-id="c98c2-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="c98c2-111">**Yeni belge** düğmesini, başka bir sağlayıcı tarafından sağlanan bir Elektronik raporlama (ER) biçimi yapılandırmasında şablon oluşturmak ve düzenlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="c98c2-112">Bu konudaki örnekte sağlayıcı Microsoft'tur.</span><span class="sxs-lookup"><span data-stu-id="c98c2-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="c98c2-113">Alternatif olarak, kendi şablonunuzu Excel biçiminde karşıya yükleyerek bir şablon oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="c98c2-114">[İş belgesi yönetimi kullanarak yeni iş belgesi oluşturma](https://youtu.be/gAIYl-mM_pw) videosu (yukarıda gösterilir) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c98c2-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="c98c2-115">İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanıma açma</span><span class="sxs-lookup"><span data-stu-id="c98c2-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="c98c2-116">İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanmaya başlamak için,**Özellik yönetimi** çalışma alanındaki **İş belgesi yönetimi için Office benzeri arabirim deneyimi** özelliğini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c98c2-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="c98c2-117">Bu özelliği tüm tüzel kişilikler için açmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="c98c2-118">**Özellik yönetimi** çalışma alanında, **Tümü** sekmesinde, listeden **İş belgesi yönetimi için Office benzeri arabirim deneyimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="c98c2-119">Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="c98c2-120">Yeni özelliğe erişmek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="c98c2-121">Sahibi diğer sağlayıcılar olan düzenleme şablonları</span><span class="sxs-lookup"><span data-stu-id="c98c2-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="c98c2-122">**İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![İş belgesi yönetimi çalışma alanı](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="c98c2-124">**Seç** sekmesinde, şablon olarak kullanılacak belgeyi ve ardından **Belge oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![İş belgeleri iletişim kutusu](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="c98c2-126">Yeni iletişim kutusunda, **Başlık** alanında, başlığı gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="c98c2-127">Başlık metni, otomatik olarak oluşturulan yeni ER biçimi yapılandırmasını adlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="c98c2-128">Bu yapılandırmanın taslak sürümü (**Müşteri FTI raporu (GER) kopyası**) düzenlenen şablonu içerir ve bu ER biçimini geçerli kullanıcı için çalıştırmak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="c98c2-129">Temel ER biçimi yapılandırmasındaki özgün şablon, diğer kullanıcıların tümü için bu ER biçimini çalıştırmada kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="c98c2-130">**Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="c98c2-131">**Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak revizyonuna için yorumları güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="c98c2-132">Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Belge oluşturma iletişim kutusu](./media/BDM_overview_new_template3.png)

<span data-ttu-id="c98c2-134">**Yeni belge** düğmesi, kullanıcıların başka bir sağlayıcı tarafından sağlanan bir ER biçimi yapılandırmasında şablon oluşturmak ve düzenlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="c98c2-135">Bu örnekte sağlayıcı Microsoft'tur.</span><span class="sxs-lookup"><span data-stu-id="c98c2-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="c98c2-136">**Yeni belge**'yi seçtiğiniz zaman, sahibi geçerli ve diğer sağlayıcılar olan tüm şablonları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="c98c2-137">Siz şablonu seçtikten sonra şablon düzenleme için açılır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="c98c2-138">Düzenlenen şablon daha sonra otomatik olarak oluşturulan yeni bir ER biçim yapılandırması içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="c98c2-139">Varolan Excel biçimini kullanan bir şablonu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="c98c2-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="c98c2-140">Bir şablonu karşıya yüklemeden önce gerekli bilgileri sağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="c98c2-141">**İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![İş belgesi yönetimi çalışma alanı](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="c98c2-143">**Yeni şablon oluştur** sayfasında, **Yükle** sekmesindeki **Şablon** sekmesinde şablon olarak kullanmak istediğiniz Excel dosyasını bulmak ve seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="c98c2-144">**Şablon** bölümünde, **Başlık** ve **Açıklama** alanları otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="c98c2-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="c98c2-145">Bunlar otomatik olarak oluşturulan yeni ER biçimi yapılandırmasının adını ve açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c98c2-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="c98c2-146">Bu alanları istediğiniz şekilde düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="c98c2-147">**Belge Türü** bölümünde, **Ad** alanında iş belgesinin türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="c98c2-148">Bu değer, doğru veri kaynağını (ER model konfigürasyonu) aramak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Şablon sekmesi](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="c98c2-150">**Veri kaynağı** sekmesinde, **Filtre** hızlı sekmesinde **Filtreyi uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="c98c2-151">**Veri kaynağı** bölümünde, **Ad** alanı otomatik olarak doldurulur veya el ile bir değer seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="c98c2-152">Uygun veri kaynağı adını ad, açıklama, ülke/bölge kodu ve iş belgesi türü ile aramak için filtre kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Veri kaynağı sekmesi](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="c98c2-154">**Filtre** hızlı sekmesi, doğru veri kaynağını (ER model konfigürasyonu) aramak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="c98c2-155">Karşıya yüklediğiniz belge için en uygun veri kaynağını bulmak üzere tüm filtre alanlarını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="c98c2-156">**Filtre** hızlı sekmesindeki koşullar **VEYA** koşulları olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="c98c2-157">**Eşleme** sekmesinde **Otomatik algıla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="c98c2-158">**Kök tanımı** alanı otomatik olarak doldurulur veya el ile bir değer seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="c98c2-159">Bu sekme, şablondan ve modelden gelen öğelerin bitiş eşlemesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c98c2-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Eşleme sekmesi](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="c98c2-161">**Şablon yapısı** bölümündeki eşleme, kullanıcının dilindeki ve şablondaki hücre adındaki etiket veya açıklamaların tam eşleşmesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c98c2-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="c98c2-162">Bir şablon oluşturmak ve düzenleme işlemini başlatmak istediğinizi onaylamak için **Belge oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="c98c2-163">Daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="c98c2-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="c98c2-164">Elektronik raporlamada bir sağlayıcı yoksa, oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="c98c2-165">Etkin sağlayıcı yoksa, etkinleştirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c98c2-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="c98c2-166">Sağlayıcı oluşturmak için, **Ad** alanında sağlayıcının adını değiştirin, **İnternet adresi** alanında yeni sağlayıcının internet adresini güncelleştirin ve onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![BDM'de yeni sağlayıcı oluşturma](./media/bdm_create_provider.png)
    
- <span data-ttu-id="c98c2-168">Mevcut sağlayıcıyı etkinleştirmek için **Yapılandırma sağlayıcısı** alanında sağlayıcının adını seçin ve ardından sağlayıcıyı etkin olarak ayarlamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c98c2-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![BDM'de sağlayıcıyı etkinleştirme](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="c98c2-170">Her BDM şablonu yapılandırmanın yazarı olarak sağlayıcıya başvurur.</span><span class="sxs-lookup"><span data-stu-id="c98c2-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="c98c2-171">Bu nedenle şablon için etkin bir sağlayıcı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c98c2-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
