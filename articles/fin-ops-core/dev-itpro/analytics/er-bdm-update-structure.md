---
title: İş belgesi şablonunun yapısını güncelleştirme
description: Bu konu başlığında, İş belgesi yönetimi özelliği kullanılarak iş belgesi şablonunun yapısının nasıl güncelleştirileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd279b28c43e22bec6bf814845fe97828bc96d81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681340"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="5255d-103">İş belgesi şablonunun yapısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5255d-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5255d-104">[İş belgesi yönetimi](er-business-document-management.md) şablon düzenleyicisinin **Şablon yapısı** bölmesinde, Microsoft Excel'de bir şablona [yeni alanlar ekleyerek](er-bdm-add-field-to-excel-template.md) iş belgesi şablonunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5255d-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="5255d-105">Ardından şablonun yapısı, Dynamics 365 Finance'ta **Şablon yapısı** bölmesinde yaptığınız değişiklikleri yansıtacak şekilde otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5255d-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="5255d-106">Ayrıca, şablonu Office 365 çevrimiçi işlevini kullanarak da değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5255d-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="5255d-107">Örneğin, düzenlenebilir çalışma sayfasına resim veya şekil gibi yeni bir adlandırılmış öğe ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5255d-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="5255d-108">Bu durumda, şablonun yapısı Finance'te otomatik olarak güncelleştirilmez ve eklediğiniz öğe **Şablon yapısı** bölmesinde gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="5255d-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="5255d-109">Şablon düzenleyicisi sayfasında **Yapıyı güncelleştir**'i seçerek Finance'teki şablon yapısını el ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5255d-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="5255d-110">Bu özellik hakkında daha fazla bilgi için aşağıdaki örneği tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="5255d-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="5255d-111">Örnek: İş belgesi şablonunun yapısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5255d-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="5255d-112">Bu örnekte, şablon Office Online'da değiştirildikten sonra sistem yöneticisinin iş belgesi şablonunun yapısını nasıl güncelleştirebileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5255d-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="5255d-113">Aşağıdaki bölümlerde ilgili adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5255d-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="5255d-114">Düzenleme için bir iş belgesi şablonu hazırlama</span><span class="sxs-lookup"><span data-stu-id="5255d-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="5255d-115">[İş belgesi yönetimine genel bakış](er-business-document-management.md)'ta aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="5255d-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="5255d-116">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5255d-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="5255d-117">ER çözümlerini çe aktar</span><span class="sxs-lookup"><span data-stu-id="5255d-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="5255d-118">İş belgesi yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5255d-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="5255d-119">Parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5255d-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="5255d-120">İş belgesi şablonu düzenleme</span><span class="sxs-lookup"><span data-stu-id="5255d-120">Edit a business document template</span></span>

1. <span data-ttu-id="5255d-121">**İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="5255d-122">**Yeni şablon oluştur** sayfasında, **Serbest metin faturası (ER örneği) (Excel)** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="5255d-123">**Belge oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-123">Select **Create document**.</span></span>
4. <span data-ttu-id="5255d-124">**Başlık** alanına **FTI sample Litware** başlığını girin.</span><span class="sxs-lookup"><span data-stu-id="5255d-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="5255d-125">Yeni şablonu oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5255d-126">Henüz Office Online'da oturum açmadıysanız [Office 365 oturum açma sayfasına yönlendirilirsiniz](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span><span class="sxs-lookup"><span data-stu-id="5255d-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span></span> <span data-ttu-id="5255d-127">Finance ortamınıza dönmek için tarayıcınızda **Geri** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="5255d-128">Yeni şablon, şablon düzenleyicisi sayfasındaki Excel Online eklenmiş denetiminde düzenlenmek üzere açılır.</span><span class="sxs-lookup"><span data-stu-id="5255d-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="5255d-129">[![İş belgesi şablonunu düzenlemeye başlamak için İş belgesi yönetimi çalışma alanını kullanma](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="5255d-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="5255d-130">Düzenlenebilir şablonun geçerli yapısını inceleme</span><span class="sxs-lookup"><span data-stu-id="5255d-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="5255d-131">Excel Online'daki şeritte, **Görünüm** sekmesinde, **Göster** grubunda **Kılavuz çizgileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="5255d-132">Düzenlenebilir şablonda, şablon başlığının üstündeki dikdörtgeni seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="5255d-133">Bu dikdörtgen, **rptHeaderCompLogo** adlı bir resimdir.</span><span class="sxs-lookup"><span data-stu-id="5255d-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="5255d-134">**Şablon yapısı** bölmesi gizliyse **Yapıyı göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="5255d-135">**Şablon yapısı** bölmesinde **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5255d-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="5255d-136">Finance'teki şablon yapısında **rptHeaderCompLogo** öğesnini, **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesinin alt öğesi olarak sunulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5255d-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="5255d-137">[![Düzenlenebilir şablonun geçerli yapısını incelemek için İş belgesi yönetimi çalışma alanını kullanma](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="5255d-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="5255d-138">Bir resim silerek iş belgesi şablonunun yapısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5255d-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="5255d-139">Excel Online'da, düzenlenebilir şablonda, **rptheadercomplogo** resmini seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="5255d-140">Seçili resmi düzenlenebilir şablondan silmek için aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="5255d-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="5255d-141">Klavyenizde **Delete** tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="5255d-142">Resmi seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Kes**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5255d-143">Bu durumda, **rptHeaderCompLogo** öğesi Finance'teki şablon yapısında bulunmaya devam etse de artık Excel şablosunda yer almaz.</span><span class="sxs-lookup"><span data-stu-id="5255d-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="5255d-144">Excel ve Finance'teki şablon yapısını eşitlemek **Yapıyı güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="5255d-145">**Şablon yapısı** bölmesinde **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5255d-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="5255d-146">**rptHeaderCompLogo** öğesinin, artık Finance'teki şablon yapısında yer almadığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5255d-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="5255d-147">[![İş belgesi şablonundan bir resim silmek için İş belgesi yönetimi çalışma alanını kullanma](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="5255d-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="5255d-148">Bir resim ekleyerek iş belgesi şablonunun yapısını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5255d-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="5255d-149">Excel Online'daki şeritte, **Ekle** sekmesinde, **Çizimler** grubunda **Resim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="5255d-150">**Dosya seç**'i belirleyin, eklemek istediğiniz resme göz atın, resmi seçin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="5255d-151">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-151">Select **Insert**.</span></span>
4. <span data-ttu-id="5255d-152">Yeni resmi doğru yere gelene kadar taşıyın.</span><span class="sxs-lookup"><span data-stu-id="5255d-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="5255d-153">Varsayılan olarak, Excel resmi adlandırır.</span><span class="sxs-lookup"><span data-stu-id="5255d-153">By default, Excel names the picture.</span></span> <span data-ttu-id="5255d-154">Örneğin, resim **Resim 2** olarak adlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="5255d-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="5255d-155">Excel ve Finance'teki şablon yapısını eşitlemek **Yapıyı güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5255d-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="5255d-156">**Şablon yapısı** bölmesinde **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5255d-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="5255d-157">Yeni resimin, artık Finance'teki şablon yapısında öğe olarak yer aldığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5255d-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="5255d-158">[![İş belgesi şablonuna resim eklemek için İş belgesi yönetimi çalışma alanını kullanma](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="5255d-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="5255d-159">İlgili bağlantılar</span><span class="sxs-lookup"><span data-stu-id="5255d-159">Related links</span></span>

[<span data-ttu-id="5255d-160">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="5255d-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5255d-161">İş belgesi yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5255d-161">Business document management overview</span></span>](er-business-document-management.md)
