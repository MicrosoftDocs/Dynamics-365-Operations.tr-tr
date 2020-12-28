---
title: Microsoft Excel'de iş belgesi şablonuna yeni alanlar ekleme
description: Bu konuda, İş belgesi yönetimi özelliğini kullanarak Microsoft Excel'de iş belgesi şablonuna yeni alanlar ekleme hakkında bilgiler sağlanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: fcfbcb021b192cef75d59b0db1796e994f3dc27d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681388"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="946e1-103">Microsoft Excel'de iş belgesi şablonuna yeni alanlar ekleme</span><span class="sxs-lookup"><span data-stu-id="946e1-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="946e1-104">İş belgelerini Microsoft Excel biçiminde oluşturmak için kullanılan şablona yeni alanlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="946e1-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="946e1-105">Bu alanlar, oluşturulan belgeleri uygulamadaki gerekli bilgilerle doldurmak için kullanılan yer tutucular olarak eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="946e1-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="946e1-106">Eklediğiniz alanlara yönelik olarak, şablon iş belgeleri oluşturmak üzere kullanıldığında alana hangi uygulama verilerinin girileceğini belirlemek için veri kaynaklarına bir bağlama belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="946e1-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="946e1-107">Bu özellik hakkında daha fazla bilgi edinmek için bu konudaki örneği tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="946e1-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="946e1-108">Bu örnekte, oluşturulan serbest metin faturası formlarındaki alanları dolduracak şekilde bir şablonun nasıl güncelleştirileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="946e1-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="946e1-109">Şablonları düzenlemek için İş belge yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="946e1-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="946e1-110">İş belgesi yönetimi (BDM) [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md) çerçevesi üzerine kurulu olduğundan BDM ile çalışmaya başlayabilmeniz için gerekli ER ve BDM parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="946e1-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="946e1-111">Microsoft Dynamics 365 Finance kurulumunda sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="946e1-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="946e1-112">[İş belgesi yönetimine genel bakış](er-business-document-management.md) konusundaki örneğin aşağıdaki adımlarını tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="946e1-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="946e1-113">ER parametrelerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="946e1-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="946e1-114">BDM'yi açın.</span><span class="sxs-lookup"><span data-stu-id="946e1-114">Turn on BDM.</span></span>

<span data-ttu-id="946e1-115">Artık iş belgesi şablonlarını düzenlemek için BDM kullanmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="946e1-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="946e1-116">Şablon içeren ER çözümlerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="946e1-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="946e1-117">Bu prosedürdeki örnekte, resmi olarak yayımlanan ER çözümü kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="946e1-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="946e1-118">Bu çözümün ER yapılandırmalarını geçerli Finance kurulumunuza içe aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="946e1-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="946e1-119">**Serbest metin faturası (Excel)** Bu çözümün ER biçim yapılandırması BDM kullanarak düzenlenebilen Excel biçiminde iş belgesi şablonu içerir.</span><span class="sxs-lookup"><span data-stu-id="946e1-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="946e1-120">Bu ER biçim yapılandırmasının en son sürümünü Microsoft Dynamics Lifecycle Service'tan (LCS) içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="946e1-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="946e1-121">İlgili ER veri modeli ve ER model eşleme yapılandırmaları otomatik olarak içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="946e1-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="946e1-122">ER yapılandırmalarını içe aktarma hakkında daha fazla bilgi içi bkz. [ER yapılandırması yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="946e1-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS Paylaşılan varlık kitaplığı sayfası](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="946e1-124">ER çözüm şablonunu düzenleme</span><span class="sxs-lookup"><span data-stu-id="946e1-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="946e1-125">**İş belgesi yönetimi** çalışma alanına erişimi olan bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="946e1-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="946e1-126">**İş belgesi yönetimi** çalışma alanı sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="946e1-126">Open the **Business document management** workspace.</span></span>

    ![İş belgesi yönetimi çalışma alanı](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="946e1-128">Kılavuzda, **Serbest metin faturası (Excel)** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="946e1-129">Sağ bölmede, seçili şablona dayalı yeni bir şablon oluşturmak için **Yeni şablon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="946e1-130">**Başlık** alanına, yeni şablonun başlığı olarak **Serbest metin faturası (Excel) Contoso** girin.</span><span class="sxs-lookup"><span data-stu-id="946e1-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="946e1-131">Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="946e1-132">BDM şablon düzenleyici sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="946e1-132">The BDM template editor page appears.</span></span> <span data-ttu-id="946e1-133">Microsoft 365 kullanarak, katıştırılmış denetimde seçili şablonu çevrimiçi olarak düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="946e1-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM şablon düzenleyicisi sayfası](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="946e1-135">Şablona yeni alan etiketini ekleme</span><span class="sxs-lookup"><span data-stu-id="946e1-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="946e1-136">BDM şablon düzenleyicisi sayfasında Excel şeridindeki **Görünüm** sekmesinde düzenlenebilir Excel şablonu için **Başlıklar ve Kılavuz Çizgileri** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Seçili Başlıklar ve Kılavuz Çizgileri onay kutuları](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="946e1-138">**E8:F8** hücrelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="946e1-139">Excel şeridindeki **Giriş** sekmesinde, seçilen hücreleri yeni birleştirilen **E8:F8** hücresinde birleştirmek için **Birleştir ve Ortala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="946e1-140">Birleştirilen **E8:F8** hücresine **URL**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="946e1-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="946e1-141">Birleştirilen **E7:F7** hücresini seçin, **Biçim boyacısı** seçeneğini belirleyin ve ardından birleştirilen **E8:F8** hücresini seçerek bunu birleştirilen **E7:F7** hücresiyle aynı şekilde biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="946e1-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Şablona eklenen yeni alan etiketi](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="946e1-143">Şablonu yeni alan için alan rezerve edecek şekilde biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="946e1-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="946e1-144">BDM şablon düzenleyicisi sayfasında, birleştirilen **G8:H8** hücresini seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="946e1-145">Excel şeridindeki **Giriş** sekmesinde, seçilen hücreleri yeni birleştirilen **G8:H8** hücresinde birleştirmek için **Birleştir ve Ortala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="946e1-146">Birleştirilen **G7:H7** hücresini seçin, **Biçim boyacısı** seçeneğini belirleyin ve ardından birleştirilen **G8:H8** hücresini seçerek bunu birleştirilen **G7:H7** hücresiyle aynı şekilde biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="946e1-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Yeni alan için rezerve edilen alan](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="946e1-148">**Ad** kutu alanında, **CompanyInfo**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="946e1-149">Geçerli Excel şablonunun **CompanyInfo** aralığı, satıcı taraf olarak geçerli şirketin ayrıntılarıyla oluşturulan raporun başlığını doldurmak için kullanılan tüm alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="946e1-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Seçili CompanyInfo aralığı](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="946e1-151">Şablona yeni alan ekleme</span><span class="sxs-lookup"><span data-stu-id="946e1-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="946e1-152">**BDM şablon düzenleyicisi** sayfasındaki Eylem Bölmesi'nde **Biçimlendirmeyi göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="946e1-153">**Şablon yapısı** bölmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="946e1-154">Yeni alan olarak kullanmak istediğiniz şablonun bölümünü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="946e1-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="946e1-155">Bu ayarlamayı birleştirilen **G8:H8** hücresini biçimlendirerek zaten yaptınız.</span><span class="sxs-lookup"><span data-stu-id="946e1-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Şablona yeni alan ekleme](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="946e1-157">**Excel\Hücre**'yi seçerek yeni alanı şablondaki bir hücre olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="946e1-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="946e1-158">Şablona yeni aralık eklemek isterseniz **Excel\Aralık**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="946e1-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="946e1-159">Girilen aralık birden fazla hücre içerebilir.</span><span class="sxs-lookup"><span data-stu-id="946e1-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="946e1-160">Bu hücreleri daha sonra ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="946e1-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="946e1-161">Eklediğiniz alan için geçerli şablon yapısındaki en uygun ana bileşen olduğundan **CompanyInfo** şablon bileşeninin **Şablon yapısı** bölmesinde otomatik olarak seçildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="946e1-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="946e1-162">**Excel aralığı** alanına **CompanyURL_Value** girin.</span><span class="sxs-lookup"><span data-stu-id="946e1-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="946e1-163">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-163">Select **OK**.</span></span>

    ![Şablon yapısına eklenen CompanyURL_Value alanı](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="946e1-165">**Şablon yapısı** bölmesinde, üç nokta düğmesini (...) seçin ve ardından **Bağlamaları göster** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="946e1-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Seçili bağlamaları göster](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="946e1-167">**Şablon yapısı** bölmesi artık temel alınan ER biçiminde kullanılabilen veri kaynaklarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="946e1-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="946e1-168">Temel alınan ER biçiminin veri kaynağına bağlamayı planladığınız alan olarak **CompanyInfo_Value**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="946e1-169">**Şablon yapısı** bölmesinin **Veri kaynakları** bölümünde **Model \> InvoiceBase \> CompanyInfo**'yu genişletin.</span><span class="sxs-lookup"><span data-stu-id="946e1-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="946e1-170">**CompanyInfo** altında **WebsiteURI** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Seçili WebsiteURI öğesi](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="946e1-172">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-172">Select **Bind**.</span></span>
11. <span data-ttu-id="946e1-173">**Şablon yapısı** bölmesinde **Kaydet**'i seçin ve ardından BDM şablon düzenleyicisi sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="946e1-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="946e1-174">**İş belgesi yönetimi** çalışma alanında sağ bölmedeki **Şablon** sekmesi, güncelleştirilen şablonu gösterir.</span><span class="sxs-lookup"><span data-stu-id="946e1-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="946e1-175">Kılavuzda, düzenlenen şablonun **Durum** alanının **Taslak** olarak değiştirildiğini ve **Revizyon** alanının artık boş olmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="946e1-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="946e1-176">Bu değişiklikler, bu şablonu düzenleme işleminin başlatıldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="946e1-176">These changes indicate that the process of editing this template has been started.</span></span>

![İş belgesi yönetimi çalışma alanında düzenlenen şablon](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="946e1-178">Şirket ayarlarını inceleme</span><span class="sxs-lookup"><span data-stu-id="946e1-178">Review company settings</span></span>

1.  <span data-ttu-id="946e1-179">**Kuruluş yönetimi \> Kuruluşlar \> Tüzel kişilikler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="946e1-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="946e1-180">**İletişim bilgileri** hızlı sekmesinde, şirket URL'sinin girildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="946e1-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Tüzel kişilikler sayfasına girilen şirket URL'si](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="946e1-182">Güncelleştirilen şablonu test etmek için iş belgeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="946e1-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="946e1-183">Uygulamada, şirketi **USMF** olarak değiştirin ve **Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="946e1-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="946e1-184">**FTI-00000002** faturasını seçin ve ardından **Yazdırma yönetimi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="946e1-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="946e1-185">Sol bölmede, **Modül - alacak hesapları \> Belgeler \> Serbest metin faturası**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="946e1-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="946e1-186">**Serbest metin faturası** altında, **Özgün belge** düzeyini seçerek işlenecek faturaların kapsamını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="946e1-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="946e1-187">Sağ bölmedeki **Rapor biçimi** alanında, belirtilen belge düzeyi için **Serbest metin faturası (Excel) Contoso** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="946e1-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Seçili serbest metin faturası (Excel) Contoso şablonu](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="946e1-189">Geçerli sayfayı kapatmak için **Esc** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="946e1-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="946e1-190">**Yazdır \> Seçilen**'i belirleyin.</span><span class="sxs-lookup"><span data-stu-id="946e1-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="946e1-191">Oluşturulan belgeyi indirin ve Excel'de açın.</span><span class="sxs-lookup"><span data-stu-id="946e1-191">Download the generated document, and open it in Excel.</span></span>

    ![Excel'de serbest metin faturası](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="946e1-193">Değiştirilen şablon, seçili madde için serbest metin faturası raporu oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="946e1-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="946e1-194">Bu raporun şablonda yaptığınız değişikliklerden nasıl etkilendiğini analiz etmek için başka bir uygulama oturumunda şablonu değiştirdikten sonra raporu hemen bir uygulama oturumunda çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="946e1-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="946e1-195">İlgili bağlantılar</span><span class="sxs-lookup"><span data-stu-id="946e1-195">Related links</span></span>

[<span data-ttu-id="946e1-196">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="946e1-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="946e1-197">İş belgesi yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="946e1-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="946e1-198">OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="946e1-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
