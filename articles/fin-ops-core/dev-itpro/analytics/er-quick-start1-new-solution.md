---
title: Özel rapor yazdırmak için yeni bir ER çözümü tasarlama
description: Bu konu, özel rapor yazdırmak için bir Elektronik raporlama (ER) çözümünün nasıl tasarlanacağını açıklamaktadır.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90e5381c2d30753e3ad82a38d7361b411f1d7a87
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304405"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="2b021-103">Özel rapor yazdırmak için yeni bir ER çözümü tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b021-104">Aşağıdaki adımlarda Sistem Yöneticisi, Elektronik Raporlama Geliştiricisi veya Elektronik Raporlama İşlevsel Danışmanı rolüne sahip bir kullanıcının ER çerçevesinin parametrelerini nasıl yapılandırabileceği, belirli bir iş etki alanının verilerine erişmek için yeni bir ER çözümünün gerekli ER yapılandırmalarını nasıl tasarlayabileceği ve nasıl Microsoft Office biçiminde özel rapor oluşturabileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2b021-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="2b021-105">Bu adımlar **USMF** şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="2b021-106">ER altyapısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="2b021-107">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="2b021-108">ER yapılandırma sağlayıcısı etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="2b021-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="2b021-109">ER yapılandırma sağlayıcıları listesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="2b021-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="2b021-110">Yeni bir ER yapılandırması sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="2b021-111">ER yapılandırma sağlayıcısı etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="2b021-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="2b021-112">Etki alanına özel veri modeli tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="2b021-113">Yeni bir veri modeli yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="2b021-114">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="2b021-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="2b021-115">Veri modelini adlandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="2b021-116">Veri modeli alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="2b021-117">Veri modelinin tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="2b021-118">Yapılandırılan veri modeli için bir model eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="2b021-119">Yeni bir model eşlemesi yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="2b021-120">Yeni model eşleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b021-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="2b021-121">Yeni bir model eşleme bileşeni tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="2b021-122">Uygulama tablolarına erişmek için veri kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="2b021-123">Uygulama numaralandırmalarına erişmek için veri kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="2b021-124">Belirtilen dilde rapor oluşturmak için ER etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="2b021-125">Numaralandırma değerlerini karşılaştırma sonuçlarını bir metin değerine dönüştürmek için veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="2b021-126">Veri modeli alanlarına veri kaynakları bağlama</span><span class="sxs-lookup"><span data-stu-id="2b021-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="2b021-127">Model eşleme tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="2b021-128">Özel rapor için şablon tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="2b021-129">Bir biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="2b021-130">Tasarlanan biçim yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="2b021-131">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b021-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="2b021-132">Rapor şablonunu içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="2b021-133">Biçim yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="2b021-134">Rapor başlığı için veri bağlamayı tanımlama</span><span class="sxs-lookup"><span data-stu-id="2b021-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="2b021-135">Model veri kaynağını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="2b021-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="2b021-136">Biçim öğelerini veri kaynağı alanlarına bağlama</span><span class="sxs-lookup"><span data-stu-id="2b021-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="2b021-137">ER'den tasarlanan biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="2b021-138">Tasarlanan biçimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="2b021-139">Oluşturulan belgenin adını değiştirmek için bir biçimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="2b021-140">Soruların sırasını değiştirmek için bir biçimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="2b021-141">ER'den değiştirilmiş biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="2b021-142">Biçim tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="2b021-143">Tasarlanan raporu çağırmak için uygulama artefaktları geliştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="2b021-144">Kaynak kodu değiştir</span><span class="sxs-lookup"><span data-stu-id="2b021-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="2b021-145">Veri sözleşmesi sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="2b021-146">UI oluşturucu sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="2b021-147">Veri sağlayıcı sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="2b021-148">Etiket dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="2b021-149">Rapor hizmeti sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="2b021-150">Rapor denetleyicisi sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="2b021-151">Menü öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="2b021-152">Menüye menü öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="2b021-153">Visual Studio projesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b021-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="2b021-154">Uygulamadan bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="2b021-155">Tasarlanan ER çözümünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="2b021-156">Model eşlemesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="2b021-157">Veri sözleşmesi nesnesine erişmek için veri kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="2b021-158">ER biçim eşleme kayıtlarına erişmek için veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="2b021-159">Çalışan bir ER biçimin biçim eşleme kaydına erişmek için veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="2b021-160">Çalışan ER biçiminin adını veri modeline girme</span><span class="sxs-lookup"><span data-stu-id="2b021-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="2b021-161">Model eşleme tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="2b021-162">Biçim değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="2b021-163">Yeni bir biçim öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="2b021-164">Eklenen biçim öğesini bağlama</span><span class="sxs-lookup"><span data-stu-id="2b021-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="2b021-165">Biçim tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="2b021-166">Uygulamadan bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="2b021-167">ER'den bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="2b021-168">Ekran önizleme için biçim hedefi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="2b021-169">PDF belgesi olarak önizlemek için uygulamadan bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="2b021-170">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2b021-170">Additional resources</span></span>](#References)

<span data-ttu-id="2b021-171">Bu örnekte, [Soru formu](../../../human-resources/hr-learning-questionnaires.md) modülü için yeni bir ER çözümü oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2b021-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="2b021-172">Bu yeni ER çözümü, bir Microsoft Excel çalışma sayfasını şablon olarak kullanarak rapor tasarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2b021-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="2b021-173">Daha sonra, mevcut SQL Server Reporting Services (SSRS) raporunu oluşturmaya ek olarak, **Soru formu** raporunu Excel veya PDF biçiminde oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="2b021-174">Ayrıca, yeni raporu daha sonra istek üzerine değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="2b021-175">Kodlama gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2b021-175">No coding is required.</span></span>

1. <span data-ttu-id="2b021-176">Mevcut raporu çalıştırmak için **Soru formu** \> **Tasarım** \> **Soru formları raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Mevcut SSRS raporunu çalıştırmak için Soru Formu modülündeki Soru formları raporu menü öğesini seçme](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="2b021-178">**Soru formları raporu** iletişim kutusunda seçim ölçütü belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b021-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="2b021-179">Rapor yalnızca **SBCCrsExam** soru formunu içerecek şekilde filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Soru formları raporu iletişim kutusunda seçim ölçütü belirtme](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="2b021-181">Aşağıdaki şekilde **SBCCrsExam** soru formu için oluşturulan SSRS raporu sürümü gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2b021-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Oluşturulan SSRS raporu](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="2b021-183">ER altyapısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-183">Configure the ER framework</span></span>

<span data-ttu-id="2b021-184">Elektronik Raporlama Geliştiricisi rolüne sahip bir kullanıcı olarak, yeni ER çözümünüzü tasarlamak için ER çerçevesini kullanmaya başlamak için minimum ER parametleri kümesini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="2b021-185">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-185">Configure ER parameters</span></span>

1. <span data-ttu-id="2b021-186">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b021-187">**Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="2b021-188">**Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="2b021-189">**Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2b021-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="2b021-190">**Yapılandırmalar** alanını, **USMF** şirketi için **Dosya** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="2b021-191">**İş arşivi**, **Geçici**, **Temel** ve **Diğer** alanlarını **Dosya** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="2b021-192">ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="2b021-193">ER yapılandırma sağlayıcısı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="2b021-194">Her ER yapılandırması bir ER yapılandırma sağlayıcısı tarafından sahiplenildi olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="2b021-195">Bu nedenle, ER yapılandırmalarını eklemeye veya düzenlemeye başlamadan önce, **Elektronik raporlama** çalışma alanında bir ER yapılandırma sağlayıcısını etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="2b021-196">Yalnızca ER yapılandırmasının sahibi bunu düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="2b021-197">Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2b021-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="2b021-198">ER yapılandırma sağlayıcıları listesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="2b021-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="2b021-199">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b021-200">**Elektronik raporlama** çalışma alanında, **İlgili bağlantılar**  bölümünde, **Yapılandırma sağlayıcıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="2b021-201">**Yapılandırma sağlayıcıları** sayfasında, her yapılandırma sağlayıcı kaydının benzersiz bir adı ve URL'si vardır.</span><span class="sxs-lookup"><span data-stu-id="2b021-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="2b021-202">Bu sayfanın içeriğini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-202">Review the contents of this page.</span></span> <span data-ttu-id="2b021-203">**Litware, Inc.** (`https://www.litware.com`) için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleyin](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="2b021-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="2b021-204">Yeni bir ER yapılandırması sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="2b021-205">**Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="2b021-206">**Ad** alanına **Litware, Inc.** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="2b021-207">**İnternet adresi** alanına `https://www.litware.com` girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="2b021-208">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="2b021-209">ER yapılandırma sağlayıcısı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="2b021-210">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b021-211">**Elektronik raporlama** çalışma alanında, **Litware, Inc.** yapılandırma sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="2b021-212">**Etkin olarak ayarla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-212">Select **Set active**.</span></span>

<span data-ttu-id="2b021-213">ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="2b021-214">Etki alanına özel veri modeli tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-214">Design a domain-specific data model</span></span>

<span data-ttu-id="2b021-215">**Soru formu** iş etki alanı için [veri modeli](general-electronic-reporting.md#data-model-and-model-mapping-components) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="2b021-216">Bu veri modeli daha sonra **Soru formu** raporu oluşturmak üzere bir ER biçimi tasarlarken veri kaynağı olarak kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="2b021-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="2b021-217">[Yeni veri modeli yapılandırmasını içe aktarma](#ImportDataModel) bölümündeki adımları izleyerek gerekli veri modelini sağlanan XML dosyasından içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="2b021-218">Alternatif olarak, bu veri modelini sıfırdan tasarlamak için [Yeni veri modeli yapılandırması oluştur](#DesignDataModel) bölümündeki adımları tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="2b021-219">Yeni bir veri modeli yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="2b021-220">[Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2b021-220">Download the [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="2b021-221">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="2b021-222">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="2b021-223">Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="2b021-224">**Gözat**'ı seçin ve **Questionnaires model.version.1.xml** dosyasını bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="2b021-225">Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="2b021-226">Devam etmek için sonraki yordamı atlayın, [Yeni bir veri modeli yapılandırması oluşturma](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="2b021-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="2b021-227">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="2b021-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="2b021-228">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b021-229">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="2b021-230">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="2b021-231">Açılır menüdeki iletişim kutusunda, **Ad** alanına **Soru formu modeli** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="2b021-232">Yapılandırma oluşturmak için **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="2b021-233">Veri modelini adlandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-233">Name the data model</span></span>

1. <span data-ttu-id="2b021-234">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="2b021-235">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-235">Select **Designer**.</span></span>
3. <span data-ttu-id="2b021-236">**Veri modeli tasarımcısı** sayfasında, **Genel** hızlı sekmesinde, **Ad** alanına <a name="DataModeName"></a>**Soru formları** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="2b021-237">Yeni veri modeli alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-237">Add new data model fields</span></span>

1. <span data-ttu-id="2b021-238">**Veri modeli tasarımcısı** sayfasında **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="2b021-239">Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-240">Yeni düğümün türü olarak **Model kökü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="2b021-241">**Ad** alanına, <a name="RootDefinitionName"></a>**Kök** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="2b021-242">Yeni düğüm eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="2b021-243">Bu kök tanımlayıcısı, **Soru formu** raporuna veri sağlamak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="2b021-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="2b021-244">Tek bir veri modeli birden çok tanımlayıcıya sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="2b021-245">Her bir tanımlayıcı, tek bir ER biçimi için, raporu oluşturmak üzere gereken verileri tanımlamak amacıyla belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="2b021-246">Tekrar **Yeni**'yi seçin ve veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-247">Yeni düğümün türü olarak **Etkin bir düğümün alt öğesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="2b021-248">**Ad** alanına, **CompanyName** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="2b021-249">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="2b021-250">Yeni alan eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="2b021-251">Bu alan, geçerli şirketin adını bu veri modelini veri kaynağı olarak kullanan bir ER raporuna geçirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2b021-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="2b021-252">Tekrar **Yeni**'yi seçin ve veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-253">Yeni düğümün türü olarak **Etkin bir düğümün alt öğesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="2b021-254">**Ad** alanına, **Soru formu** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="2b021-255">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="2b021-256">Yeni alan eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="2b021-257">Bu alan, soru formları listesini bu veri modelini veri kaynağı olarak kullanan bir ER raporuna geçirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b021-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="2b021-258">**Soru formu** düğümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="2b021-259">Aşağıdaki veri modeli yapısını tamamlayana kadar düzenlenebilir veri modeli için gerekli alanları aynı şekilde eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="2b021-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="2b021-260">Alan yolu</span><span class="sxs-lookup"><span data-stu-id="2b021-260">Field path</span></span>                                                    | <span data-ttu-id="2b021-261">Veri türü</span><span class="sxs-lookup"><span data-stu-id="2b021-261">Data type</span></span>   | <span data-ttu-id="2b021-262">Alan ataması/iade edilen değer</span><span class="sxs-lookup"><span data-stu-id="2b021-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="2b021-263">Kök</span><span class="sxs-lookup"><span data-stu-id="2b021-263">Root</span></span>                                                          |             | <span data-ttu-id="2b021-264">Soru formu verilerini istemek için referans noktası.</span><span class="sxs-lookup"><span data-stu-id="2b021-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="2b021-265">Kök\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="2b021-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="2b021-266">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-266">String</span></span>      | <span data-ttu-id="2b021-267">Geçerli şirketin adı.</span><span class="sxs-lookup"><span data-stu-id="2b021-267">The name of the current company.</span></span> |
    | <span data-ttu-id="2b021-268">Kök\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="2b021-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="2b021-269">Kaydet</span><span class="sxs-lookup"><span data-stu-id="2b021-269">Record</span></span>      | <span data-ttu-id="2b021-270">Biçim yürütme ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="2b021-270">Format execution details.</span></span> |
    | <span data-ttu-id="2b021-271">Kök\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="2b021-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="2b021-272">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-272">String</span></span>      | <span data-ttu-id="2b021-273">Çalıştırılmakta olan ER biçiminin adı.</span><span class="sxs-lookup"><span data-stu-id="2b021-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="2b021-274">Kök\\Soru formu</span><span class="sxs-lookup"><span data-stu-id="2b021-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="2b021-275">Kayıt listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-275">Record list</span></span> | <span data-ttu-id="2b021-276">Soru formları listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="2b021-277">Kök\\Soru formu\\Etkin</span><span class="sxs-lookup"><span data-stu-id="2b021-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="2b021-278">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-278">String</span></span>      | <span data-ttu-id="2b021-279">Geçerli soru formunun durumu.</span><span class="sxs-lookup"><span data-stu-id="2b021-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-280">Kök\\Soru formu\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="2b021-281">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-281">String</span></span>      | <span data-ttu-id="2b021-282">Geçerli soru formunun kodu.</span><span class="sxs-lookup"><span data-stu-id="2b021-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-283">Kök\\Soru formu\\Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b021-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="2b021-284">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-284">String</span></span>      | <span data-ttu-id="2b021-285">Geçerli soru formunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="2b021-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-286">Kök\\Soru formu\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="2b021-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="2b021-287">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-287">String</span></span>      | <span data-ttu-id="2b021-288">Geçerli soru formunun türü.</span><span class="sxs-lookup"><span data-stu-id="2b021-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-289">Kök\\Soru formu\\QuestionnaireOrder</span><span class="sxs-lookup"><span data-stu-id="2b021-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="2b021-290">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-290">String</span></span>      | <span data-ttu-id="2b021-291">Geçerli soru formunun sayısal sırası.</span><span class="sxs-lookup"><span data-stu-id="2b021-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-292">Kök\\Soru formu\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="2b021-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="2b021-293">Kaydet</span><span class="sxs-lookup"><span data-stu-id="2b021-293">Record</span></span>      | <span data-ttu-id="2b021-294">Geçerli soru formunun sonuç parametreleri.</span><span class="sxs-lookup"><span data-stu-id="2b021-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-295">Kök\\Soru formu\\ResultsGroup\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="2b021-296">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-296">String</span></span>      | <span data-ttu-id="2b021-297">Geçerli sonuç grubunun tanımlama kodu.</span><span class="sxs-lookup"><span data-stu-id="2b021-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="2b021-298">Kök\\Soru formu\\ResultsGroup\\Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b021-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="2b021-299">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-299">String</span></span>      | <span data-ttu-id="2b021-300">Geçerli sonuç grubunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="2b021-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="2b021-301">Kök\\Soru formu\\ResultsGroup \\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="2b021-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="2b021-302">Gerçek</span><span class="sxs-lookup"><span data-stu-id="2b021-302">Real</span></span>        | <span data-ttu-id="2b021-303">Kazanılabilecek en fazla puan sayısı.</span><span class="sxs-lookup"><span data-stu-id="2b021-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="2b021-304">Kök\\Soru formu\\Soru</span><span class="sxs-lookup"><span data-stu-id="2b021-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="2b021-305">Kayıt listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-305">Record list</span></span> | <span data-ttu-id="2b021-306">Geçerli soru formu için soruların listesi.</span><span class="sxs-lookup"><span data-stu-id="2b021-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="2b021-307">Kök\\Soru formu\\Soru\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="2b021-308">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="2b021-308">Integer</span></span>     | <span data-ttu-id="2b021-309">Geçerli yanıt koleksiyonunun sıra numarası.</span><span class="sxs-lookup"><span data-stu-id="2b021-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="2b021-310">Kök\\Soru formu\\Soru\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="2b021-311">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-311">String</span></span>      | <span data-ttu-id="2b021-312">Geçerli sorunun tanımlama kodu.</span><span class="sxs-lookup"><span data-stu-id="2b021-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="2b021-313">Kök\\Soru formu\\Soru\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="2b021-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="2b021-314">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-314">String</span></span>      | <span data-ttu-id="2b021-315">Geçerli sorunun yanıtlanıp yanıtlanmaması gerektiğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="2b021-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="2b021-316">Kök\\Soru formu\\Soru\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="2b021-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="2b021-317">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-317">String</span></span>      | <span data-ttu-id="2b021-318">Geçerli sorunun birincil olup olmadığını belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="2b021-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="2b021-319">Kök\\Soru formu\\Soru\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="2b021-320">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="2b021-320">Integer</span></span>     | <span data-ttu-id="2b021-321">Geçerli sorunun sıra numarası.</span><span class="sxs-lookup"><span data-stu-id="2b021-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="2b021-322">Kök\\Soru formu\\Soru\\Metin</span><span class="sxs-lookup"><span data-stu-id="2b021-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="2b021-323">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-323">String</span></span>      | <span data-ttu-id="2b021-324">Geçerli sorunun metni.</span><span class="sxs-lookup"><span data-stu-id="2b021-324">The text of the current question.</span></span> |
    | <span data-ttu-id="2b021-325">Kök\\Soru formu\\Soru\\Yanıt</span><span class="sxs-lookup"><span data-stu-id="2b021-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="2b021-326">Kayıt listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-326">Record list</span></span> | <span data-ttu-id="2b021-327">Geçerli soru için yanıtların listesi.</span><span class="sxs-lookup"><span data-stu-id="2b021-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="2b021-328">Kök\\Soru formu\\Soru\\Yanıt\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="2b021-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="2b021-329">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-329">String</span></span>      | <span data-ttu-id="2b021-330">Geçerli yanıtın doğru olup olmadığını belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="2b021-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="2b021-331">Kök\\Soru formu\\Soru\\Yanıt\\Puanlar</span><span class="sxs-lookup"><span data-stu-id="2b021-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="2b021-332">Gerçek</span><span class="sxs-lookup"><span data-stu-id="2b021-332">Real</span></span>        | <span data-ttu-id="2b021-333">Geçerli yanıt seçildiğinde kazanılan puanlar.</span><span class="sxs-lookup"><span data-stu-id="2b021-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="2b021-334">Kök\\Soru formu\\Soru\\Yanıt\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="2b021-335">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="2b021-335">Integer</span></span>     | <span data-ttu-id="2b021-336">Geçerli yanıtın sıra numarası.</span><span class="sxs-lookup"><span data-stu-id="2b021-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="2b021-337">Kök\\Soru formu\\Soru\\Yanıt\\Metin</span><span class="sxs-lookup"><span data-stu-id="2b021-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="2b021-338">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-338">String</span></span>      | <span data-ttu-id="2b021-339">Geçerli yanıtın metni.</span><span class="sxs-lookup"><span data-stu-id="2b021-339">The text of the current answer.</span></span> |

    <span data-ttu-id="2b021-340">Aşağıdaki şekil, **Veri modeli tasarımcısı** sayfasındaki tamamlanan düzenlenebilir veri modelini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b021-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![ER veri modeli tasarımcısında yapılandırılmış veri modeli](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="2b021-342">Değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2b021-342">Save your changes.</span></span>
8. <span data-ttu-id="2b021-343">**Veri modeli tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="2b021-344">Veri modelinin tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="2b021-345">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-346">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="2b021-347">**Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="2b021-348">**Durumu değiştir** \> **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="2b021-349">Bu yapılandırmanın sürüm 1 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b021-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="2b021-350">Sürüm 1 artık değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2b021-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="2b021-351">Bu sürüm yapılandırılmış veri modeli içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="2b021-352">Bu yapılandırma için sürüm 2 oluşturuldu ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="2b021-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="2b021-353">**Soru formu** veri modelini ayarlamak için bu sürümü düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Yapılandırmalar sayfasındaki düzenlenebilir yapılandırmanın sürümleri](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="2b021-355">ER yapılandırmaları için sürüm oluşturma hakkında daha fazla bilgi için bkz. [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="2b021-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="2b021-356">Yapılandırılan veri modeli, **Soru formu** iş etki alanının soyut gösterimidir ve Microsoft Dynamics 365 Finance'a özel artefaktlarla herhangi bir ilişki içermez.</span><span class="sxs-lookup"><span data-stu-id="2b021-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="2b021-357">Yapılandırılan veri modeli için bir model eşlemesi tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="2b021-358">Elektronik Raporlama Geliştirici rolünde bir kullanıcı olarak, **Soru formu** veri modeli için bir [model eşleme](general-electronic-reporting.md#data-model-and-model-mapping-components) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="2b021-359">Bu bileşen Finance için yapılandırılmış veri modelini uyguladığı için, Finance'a özgüdür.</span><span class="sxs-lookup"><span data-stu-id="2b021-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="2b021-360">Model eşleme bileşenini, yapılandırılan veri modelini çalışma zamanında uygulama verileriyle doldurmak için kullanılması gereken uygulama nesnelerini belirtecek şekilde yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="2b021-361">Bu görevi tamamlamak için, Finance'ta **Soru formu** iş etki alanının veri yapısı uygulama ayrıntılarını bilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="2b021-362">[Yeni model eşleme yapılandırmasını içe aktarma](#ImportModelMapping) bölümündeki adımları izleyerek gerekli model eşleme yapılandırmasını sağlanan XML dosyasından içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="2b021-363">Alternatif olarak, bu model eşlemesini sıfırdan tasarlamak için [Yeni model eşleme yapılandırması oluştur](#CreateModelMapping) bölümündeki adımları tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="2b021-364">Yeni bir model eşlemesi yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="2b021-365">[Questionnaires mapping.version.1.1xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2b021-365">Download the [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="2b021-366">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="2b021-367">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="2b021-368">Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="2b021-369">**Gözat**'ı seçin ve **Questionnaires mapping.version.1.1.xml** dosyasını bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="2b021-370">Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="2b021-371">Devam etmek için sonraki yordamı atlayın, [Yeni bir model eşleme yapılandırması oluşturma](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="2b021-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="2b021-372">Yeni model eşleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b021-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="2b021-373">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-374">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="2b021-375">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="2b021-376">Açılan iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-377">**Yeni** alanına, **Soru formları veri modeline dayalı Model Eşlemesi** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="2b021-378">**Ad** alanına **Soru eşleme** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="2b021-379">**Veri modeli tanımı** alanında, **Kök** tanımını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="2b021-380">Yapılandırma oluşturmak için **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="2b021-381">Yeni bir model eşleme bileşeni tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="2b021-382">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="2b021-383">Eşleme listesini açmak için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="2b021-384">**Kök** tanımı için otomatik olarak eklenen **Soru formları eşleme** eşlemesini seçin</span><span class="sxs-lookup"><span data-stu-id="2b021-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="2b021-385">Seçili eşlemeyi yapılandırmak için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="2b021-386">**Kök** tanımı için yeni bir eşleme otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="2b021-387">Bu eşleme **Modele** yönüne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2b021-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="2b021-388">Bu nedenle, bir veri modelini gerekli verilerle doldurmak için bu eşleme kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="2b021-389">Uygulama tablolarına erişmek için veri kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-389">Add data sources to access application tables</span></span>

<span data-ttu-id="2b021-390">Soru formu ayrıntılarını içeren uygulama tablolarına erişmek için veri kaynaklarını yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="2b021-391">**Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="2b021-392">Her bir kaydın tek bir soru formunu temsil ettiği KMCollection tablosuna erişmek için kullanılacak yeni bir veri kaynağı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="2b021-393">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-394">İletişim kutusunda, **Ad** alanına **Soru formu** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="2b021-395">**Tablo** alanına, **KMCollection** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="2b021-396">**Sorgu iste** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="2b021-397">Bu tablo için [filtreleme](../../fin-ops/get-started/advanced-filtering-query-options.md) seçeneklerini sistem sorgusu iletişim kutusunda çalışma zamanında belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="2b021-398">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="2b021-399">**Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="2b021-400">Her bir kaydın soru formundaki tek bir soruyu temsil ettiği KMQuestion tablosuna erişmek için kullanılacak yeni bir veri kaynağı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="2b021-401">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-402">İletişim kutusunda, **Ad** alanına **Soru** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="2b021-403">**Tablo** alanına, **KMQuestion** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="2b021-404">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="2b021-405">**Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="2b021-406">Her bir kaydın soru formundaki bir sorunun tek bir yanıtını temsil ettiği KMAnswer tablosuna erişmek için kullanılacak yeni bir veri kaynağı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="2b021-407">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-408">**Ad** alanına, **Yanıt** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="2b021-409">**Tablo** alanına, **KMAnswer** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="2b021-410">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="2b021-411">**Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="2b021-412">Üst KMCollection tablosunun her kaydından KMQuestionResultGroup tablosunun bir kaydına erişmek için kullanılacak yeni bir hesaplanan alan ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="2b021-413">**Veri kaynakları** bölmesinde **Soru formu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="2b021-414">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-414">Select **Add**.</span></span>
    3. <span data-ttu-id="2b021-415">İletişim kutusunda, **Ad** alanına **\$ResultGroup** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="2b021-416">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="2b021-417">[ER formül düzenleyicisinde](general-electronic-reporting-formula-designer.md) **Formül** alanında KMCollection ile KMQuestionResultGroup tabloları arasındaki bir-çok ilişkisinin [yolunu](er-formula-language.md#Paths) kullanmak için **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#Paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="2b021-418">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="2b021-419">Yeni hesaplanan alanı eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="2b021-420">**Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="2b021-421">Üst KMCollectionQuestion tablosunun her kaydından KMQuestion tablosunun soru kayıtlarına erişmek için kullanılacak yeni bir hesaplanan alan ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="2b021-422">**Veri kaynakları** bölmesinde **Soru formu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="2b021-423">KMCollection tablosunun bir-çok ilişkilerini içeren **\<İlişkiler** düğümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b021-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="2b021-424">İlgili **KMCollectionQuestion** tablosunu ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="2b021-425">İletişim kutusunda, **Ad** alanına **\$Soru** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="2b021-426">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="2b021-427">KMQuestion tablosundan uygun soru kayıtlarını döndürmek için formül düzenleyicisindeki **Formül** alanına **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="2b021-428">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="2b021-429">Yeni hesaplanan alanı eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="2b021-430">**Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="2b021-431">Üst KMQuestion tablosunun her kaydından KMAnswer tablosunun yanıt kayıtlarına erişmek için kullanılacak yeni bir hesaplanan alan ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="2b021-432">**Veri kaynakları** bölmesinde **Soru formu.\<Relations.KMCollectionQuestion.\$Soru**'yu ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="2b021-433">İletişim kutusunda, **Ad** alanına **\$Yanıt** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="2b021-434">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="2b021-435">KMAnswer tablosundan uygun yanıt kayıtlarını döndürmek için formül düzenleyicisindeki **Formül** alanına **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="2b021-436">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="2b021-437">Yeni hesaplanan alanı eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="2b021-438">**Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="2b021-439">CompanyInfo tablosundaki yöntemlere erişmek için kullanılacak yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="2b021-440">Bu tablonun **find()** yönteminin, bu eşlemenin bağlamında çağrıldığı geçerli Finance kurulumunun bir şirketini temsil eden bir kayıt döndürdüğünü unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="2b021-441">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-442">İletişim kutusunda, **Ad** alanına **CompanyInfo** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="2b021-443">**Tablo** alanına, **CompanyInfo** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="2b021-444">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="2b021-445">Uygulama numaralandırmalarına erişmek için veri kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="2b021-446">Uygulama numaralandırmalara erişmek ve değerlerini uygulama tablolarındaki **Numaralandırma** türündeki alanların değerleriyle karşılaştırmak için veri kaynakları yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="2b021-447">Veri modelinin uygun alanlarını doldurmak için karşılaştırma sonucunu kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="2b021-448">**Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Numaralandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="2b021-449">**EnumAppNoYes** numaralandırmasındaki değerlere erişmek için kullanılacak yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="2b021-450">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-451">İletişim kutusunda, **Ad** alanına **EnumAppNoYes** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="2b021-452">**Numaralandırma** alanına **NoYes** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="2b021-453">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="2b021-454">**Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Numaralandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="2b021-455">**KMCollectionQuestionMode** numaralandırmasındaki değerlere erişmek için kullanılacak yeni bir veri kaynağı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="2b021-456">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-457">İletişim kutusunda, **Ad** alanına **EnumAppQuestionOrder** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="2b021-458">**Numaralandırma** alanına **KMCollectionQuestionMode** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="2b021-459">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="2b021-460">Belirtilen dilde rapor oluşturmak için ER etiketleri ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="2b021-461">Bazı veri kaynaklarınızı, model eşlemesinin çağrısı bağlamında tanımlanan dile bağlı değerleri döndürmek üzere yapılandırmak için ER etiketleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="2b021-462">**Model eşleme tasarımcısı** sayfasında, **Veri kaynakları** bölmesinde, **Yanıt**'ı ve ardından **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="2b021-463">**Etiket** alanını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="2b021-464">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-464">Select **Translate**.</span></span>
4. <span data-ttu-id="2b021-465">**Metin çevirisi** iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-466">**Etiket Kodu** alanına, **PositiveAnswer** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="2b021-467">**Varsayılan dilde metin** alanına **Evet** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="2b021-468">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="2b021-469">**Etiket kodu** alanına, **NegativeAnswer** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="2b021-470">**Varsayılan dilde metin** alanına **Hayır** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="2b021-471">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-471">Select **Translate**.</span></span>

5. <span data-ttu-id="2b021-472">**Metin çevirisi** iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="2b021-473">**İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-473">Select **Cancel**.</span></span>

![Düzenlenebilir model eşlemesi için ER etiketleri ekleme](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="2b021-475">Yalnızca varsayılan dil için ER etiketleri girdiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="2b021-476">ER etiketlerinin diğer dillere nasıl çevrilebileceği hakkında bilgi için bkz. [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="2b021-477">Numaralandırma değerlerini karşılaştırma sonuçlarını bir metin değerine dönüştürmek için veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="2b021-478">Numaralandırma değerleri ile metin değerleri arasındaki karşılaştırmanın sonuçlarını farklı kaynaklar için birkaç kez dönüştürmeniz gerektiğinden, bu mantığı tek bir veri kaynağı olarak yapılandırmak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="2b021-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="2b021-479">Ancak, bu veri kaynağını yeniden kullanılabilir hale getirmek için parametreli veri kaynağı olarak yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2b021-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="2b021-480">Daha fazla bilgi için bkz. [Hesaplanan alan türüne göre ER veri kaynaklarının parametreli çağrılarını destekleme](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="2b021-481">**Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Genel\\Boş kapsayıcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="2b021-482">Yeni kapsayıcı veri kaynağı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="2b021-483">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="2b021-484">İletişim kutusunda, **Ad** alanına **Yardımcı** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="2b021-485">Yeni kapsayıcı veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="2b021-486">**Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="2b021-487">Yeni bir veri kaynağı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-487">Add a new data source:</span></span>

    1. <span data-ttu-id="2b021-488">**Veri kaynakları** bölmesinde **Yardımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="2b021-489">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-489">Select **Add**.</span></span>
    3. <span data-ttu-id="2b021-490">İletişim kutusunda, **Ad** alanına **NoYesEnumToString** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="2b021-491">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="2b021-492">Formül düzenleyicide, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="2b021-493">Yapılandırılan deyimin parametrelerini belirtmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="2b021-494">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-494">Select **New**.</span></span>
        2. <span data-ttu-id="2b021-495">İletişim kutusunda, **Ad** alanına **Bağımsız değişken** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="2b021-496">**Tür** alanında **Boole** veri türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="2b021-497">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-497">Select **OK**.</span></span>

    7. <span data-ttu-id="2b021-498">Belirtilen parametrenin değeri ve yürütme bağlamının diline bağlı olarak uygun ER etiketi metnini döndürmek için **Formül** alanına **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="2b021-499">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="2b021-500">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-500">Select **OK** to add the new data source.</span></span>

![ER model eşleme tasarımcısında yapılandırılmış model eşlemesi](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="2b021-502">Veri modeli alanlarına veri kaynakları bağlama</span><span class="sxs-lookup"><span data-stu-id="2b021-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="2b021-503">Veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulacağını belirtmek için yapılandırılan veri kaynaklarını veri modeli alanlarına bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="2b021-504">**Model eşleme tasarımcısı** sayfasında, **Veri modeli** bölmesinde, **CompanyName** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="2b021-505">**Veri kaynakları** bölmesinde **CompanyInfo** öğesini genişletin ve sonra aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="2b021-506">CompanyInfo tablosunun **find()** yöntemini temsil eden **CompanyInfo.find()** düğümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b021-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="2b021-507">**CompanyInfo.find().Name** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="2b021-508">Yapılandırılan model eşlemesinin çalışma zamanında bağlamında çağrıldığı şirketin adını doldurmak için **Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="2b021-509">**Veri modeli** bölmesinde **Soru formu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="2b021-510">**Veri kaynakları** bölmesinde **Soru formu**'nu ve ardından soru formu kayıtlarını doldurmak için **Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="2b021-511">**Veri modeli** bölmesinde **Soru formu** öğesini genişletin ve sonra aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="2b021-512">**Veri modeli** bölmesinde **Etkin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="2b021-513">**Veri modeli** bölmesinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="2b021-514">Numaralandırma değerleri arasındaki metne bağımlı veya dile bağımlı karşılaştırma sonucunu doldurmak için **Formül** alanına **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="2b021-515">Aşağıdaki sonuca ulaşıncaya kadar veri kaynaklarını veri modeli alanlarına bağlamaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="2b021-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="2b021-516">Alan yolu</span><span class="sxs-lookup"><span data-stu-id="2b021-516">Field path</span></span>                                              | <span data-ttu-id="2b021-517">Veri türü</span><span class="sxs-lookup"><span data-stu-id="2b021-517">Data type</span></span>   | <span data-ttu-id="2b021-518">Eylem</span><span class="sxs-lookup"><span data-stu-id="2b021-518">Action</span></span> | <span data-ttu-id="2b021-519">Bağlama ifadesi</span><span class="sxs-lookup"><span data-stu-id="2b021-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="2b021-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="2b021-520">CompanyName</span></span>                                             | <span data-ttu-id="2b021-521">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-521">String</span></span>      | <span data-ttu-id="2b021-522">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-522">Bind</span></span>   | <span data-ttu-id="2b021-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="2b021-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="2b021-524">Soru formu</span><span class="sxs-lookup"><span data-stu-id="2b021-524">Questionnaire</span></span>                                           | <span data-ttu-id="2b021-525">Kayıt listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-525">Record list</span></span> | <span data-ttu-id="2b021-526">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-526">Bind</span></span>   | <span data-ttu-id="2b021-527">Soru formu</span><span class="sxs-lookup"><span data-stu-id="2b021-527">Questionnaire</span></span> |
    | <span data-ttu-id="2b021-528">Soru formu\\Etkin</span><span class="sxs-lookup"><span data-stu-id="2b021-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="2b021-529">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-529">String</span></span>      | <span data-ttu-id="2b021-530">Düzenle</span><span class="sxs-lookup"><span data-stu-id="2b021-530">Edit</span></span>   | <span data-ttu-id="2b021-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="2b021-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="2b021-532">Soru formu\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="2b021-533">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-533">String</span></span>      | <span data-ttu-id="2b021-534">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-534">Bind</span></span>   | <span data-ttu-id="2b021-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="2b021-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="2b021-536">Soru formu\\Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b021-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="2b021-537">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-537">String</span></span>      | <span data-ttu-id="2b021-538">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-538">Bind</span></span>   | <span data-ttu-id="2b021-539">\@.Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b021-539">\@.Description</span></span> |
    | <span data-ttu-id="2b021-540">Soru formu\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="2b021-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="2b021-541">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-541">String</span></span>      | <span data-ttu-id="2b021-542">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-542">Bind</span></span>   | <span data-ttu-id="2b021-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="2b021-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="2b021-544">Soru formu\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="2b021-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="2b021-545">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-545">String</span></span>      | <span data-ttu-id="2b021-546">Düzenle</span><span class="sxs-lookup"><span data-stu-id="2b021-546">Edit</span></span>   | <span data-ttu-id="2b021-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="2b021-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="2b021-548">EnumAppQuestionOrder.Conditional, "Koşullu",</span><span class="sxs-lookup"><span data-stu-id="2b021-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="2b021-549">EnumAppQuestionOrder.Random, "Rasgele (soru formundaki yüzde)",</span><span class="sxs-lookup"><span data-stu-id="2b021-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="2b021-550">EnumAppQuestionOrder.RandomGroup, "Rasgele (sonuç gruplarındaki yüzde)",</span><span class="sxs-lookup"><span data-stu-id="2b021-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="2b021-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="2b021-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="2b021-552">"")</span><span class="sxs-lookup"><span data-stu-id="2b021-552">"")</span></span> |
    | <span data-ttu-id="2b021-553">Soru formu\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="2b021-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="2b021-554">Kaydet</span><span class="sxs-lookup"><span data-stu-id="2b021-554">Record</span></span>      |        | |
    | <span data-ttu-id="2b021-555">Soru formu\\ResultsGroup\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="2b021-556">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-556">String</span></span>      | <span data-ttu-id="2b021-557">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-557">Bind</span></span>   | <span data-ttu-id="2b021-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="2b021-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="2b021-559">Soru formu\\ResultsGroup\\Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b021-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="2b021-560">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-560">String</span></span>      | <span data-ttu-id="2b021-561">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-561">Bind</span></span>   | <span data-ttu-id="2b021-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="2b021-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="2b021-563">Soru formu\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="2b021-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="2b021-564">Gerçek</span><span class="sxs-lookup"><span data-stu-id="2b021-564">Real</span></span>        | <span data-ttu-id="2b021-565">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-565">Bind</span></span>   | <span data-ttu-id="2b021-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="2b021-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="2b021-567">Soru formu\\Soru</span><span class="sxs-lookup"><span data-stu-id="2b021-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="2b021-568">Kayıt listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-568">Record list</span></span> | <span data-ttu-id="2b021-569">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-569">Bind</span></span>   | <span data-ttu-id="2b021-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="2b021-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="2b021-571">Soru formu\\Soru\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="2b021-572">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="2b021-572">Integer</span></span>     | <span data-ttu-id="2b021-573">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-573">Bind</span></span>   | <span data-ttu-id="2b021-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="2b021-575">Soru formu\\Soru\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="2b021-576">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-576">String</span></span>      | <span data-ttu-id="2b021-577">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-577">Bind</span></span>   | <span data-ttu-id="2b021-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="2b021-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="2b021-579">Soru formu\\Soru\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="2b021-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="2b021-580">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-580">String</span></span>      | <span data-ttu-id="2b021-581">Düzenle</span><span class="sxs-lookup"><span data-stu-id="2b021-581">Edit</span></span>   | <span data-ttu-id="2b021-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="2b021-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="2b021-583">Soru formu\\Soru\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="2b021-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="2b021-584">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-584">String</span></span>      | <span data-ttu-id="2b021-585">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-585">Bind</span></span>   | <span data-ttu-id="2b021-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="2b021-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="2b021-587">Soru formu\\Soru\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="2b021-588">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="2b021-588">Integer</span></span>     | <span data-ttu-id="2b021-589">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-589">Bind</span></span>   | <span data-ttu-id="2b021-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="2b021-591">Soru formu\\Soru\\Metin</span><span class="sxs-lookup"><span data-stu-id="2b021-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="2b021-592">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-592">String</span></span>      | <span data-ttu-id="2b021-593">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-593">Bind</span></span>   | <span data-ttu-id="2b021-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="2b021-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="2b021-595">Soru formu\\Soru\\Yanıt</span><span class="sxs-lookup"><span data-stu-id="2b021-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="2b021-596">Kayıt listesi</span><span class="sxs-lookup"><span data-stu-id="2b021-596">Record list</span></span> | <span data-ttu-id="2b021-597">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-597">Bind</span></span>   | <span data-ttu-id="2b021-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="2b021-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="2b021-599">Soru formu\\Soru\\Yanıt\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="2b021-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="2b021-600">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-600">String</span></span>      | <span data-ttu-id="2b021-601">Düzenle</span><span class="sxs-lookup"><span data-stu-id="2b021-601">Edit</span></span>   | <span data-ttu-id="2b021-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="2b021-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="2b021-603">Soru formu\\Soru\\Yanıt\\Puanlar</span><span class="sxs-lookup"><span data-stu-id="2b021-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="2b021-604">Gerçek</span><span class="sxs-lookup"><span data-stu-id="2b021-604">Real</span></span>        | <span data-ttu-id="2b021-605">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-605">Bind</span></span>   | <span data-ttu-id="2b021-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="2b021-606">\@.point</span></span> |
    | <span data-ttu-id="2b021-607">Soru formu\\Soru\\Yanıt\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="2b021-608">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="2b021-608">Integer</span></span>     | <span data-ttu-id="2b021-609">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-609">Bind</span></span>   | <span data-ttu-id="2b021-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="2b021-611">Soru formu\\Soru\\Yanıt\\Metin</span><span class="sxs-lookup"><span data-stu-id="2b021-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="2b021-612">Dize</span><span class="sxs-lookup"><span data-stu-id="2b021-612">String</span></span>      | <span data-ttu-id="2b021-613">Bağla</span><span class="sxs-lookup"><span data-stu-id="2b021-613">Bind</span></span>   | <span data-ttu-id="2b021-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="2b021-614">\@.text</span></span> |

    <span data-ttu-id="2b021-615">Aşağıdaki şekil, **Model eşleme tasarımcısı** sayfasındaki yapılandırılmış model eşlemesinin son durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b021-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![ER model eşleme tasarımcısında tamamen yapılandırılmış model eşlemesi](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="2b021-617">Değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2b021-617">Save your changes.</span></span>
8. <span data-ttu-id="2b021-618">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="2b021-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="2b021-619">Model eşleme tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="2b021-620">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-621">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="2b021-622">**Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="2b021-623">**Durumu değiştir** \> **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="2b021-624">Bu yapılandırmanın sürüm 1.1 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b021-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="2b021-625">Sürüm 1.1 artık değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2b021-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="2b021-626">Bu sürüm yapılandırılmış model eşlemesini içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="2b021-627">Bu yapılandırma için sürüm 1.2 oluşturuldu ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="2b021-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="2b021-628">**Soru formu eşleme** yapılandırmasını ayarlamak için bu sürümü düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Yapılandırmalar sayfasındaki düzenlenebilir ER yapılandırmasının sürümleri](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="2b021-630">Yapılandırılan model eşlemesi, **Soru formu** iş etki alanını temsil eden soyur veri modelinin Finance kurulumunuza özgü uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="2b021-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="2b021-631">Özel rapor için şablon tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-631">Design a template for a custom report</span></span>

<span data-ttu-id="2b021-632">ER çerçevesi, Microsoft Office (Excel çalışma kitapları veya Word belgeleri) biçimlerinde raporlar oluşturmak için önceden tanımlanmış şablonları kullanır.</span><span class="sxs-lookup"><span data-stu-id="2b021-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="2b021-633">Gerekli rapor oluşturulurken, yapılandırılmış veri akışına göre bir şablon gerekli verilerle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="2b021-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="2b021-634">Bu nedenle, özel raporunuz için önce bir şablon tasarmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2b021-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="2b021-635">Bu şablon özel bir raporun düzenini temsil eden yapıdaki bir Excel çalışma kitabı olarak tasarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b021-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="2b021-636">Gerekli verilerle doldurmak istediğiniz tüm Excel öğelerini adlandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="2b021-637">[Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) dosyasını indirin ve yerel bilgisayarınıza kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2b021-637">Download the [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="2b021-638">Dosyayı Excel'de açın ve çalışma kitabının yapısını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="2b021-639">Aşağıdaki çizimin gösterdiği gibi, indirilen şablon, bir soru formunun sorularını uygun yanıtlarla birlikte görüntüleyen belirtilen soru formlarını yazdıracak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b021-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Belirtilen soru formlarını yazdırmak için Excel şablonu](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="2b021-641">Soru formu ayrıntılarını doldurmak üzere bu şablona Excel adları eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b021-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="2b021-642">Excel adlarını gözden geçirmek için Ad Yöneticisi'ni kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-642">You can use Name Manager to review the Excel names.</span></span>

![Sağlanan Excel şablonundaki Excel adlarını gözden geçirmek için Ad Yöneticisi'ni kullanma](./media/er-quick-start1-template-names.png)

<span data-ttu-id="2b021-644">Rapor etiketleri İngilizce dilinde sabit metin olarak eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b021-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="2b021-645">Yapılandırılan model eşlemesinde dile bağlı ifadelerde yaptığınız gibi, ER biçim [etiketlerini](#AddMmLabels) kullanarak, rapor etiketlerini dile bağlı metinle doldurmak için kullanılan yeni Excel adlarıyla değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="2b021-646">Bu durumda, ER etiketlerinin düzenlenebilir ER biçiminde eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="2b021-647">Aşağıdaki çizimde gösterildiği gibi, Excel'in sayfalandırma yapmasına olanak tanımak için özel rapor başlığı belirtilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2b021-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Sağlanan Excel şablonundaki özel rapor başlığı](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="2b021-649">Bir biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-649">Design a format</span></span>

<span data-ttu-id="2b021-650">Elektronik Raporlama İşlev Danışmanı rolündeki bir kullanıcı olarak, bir [biçim](general-electronic-reporting.md#FormatComponentOutbound) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="2b021-651">Bir rapor şablonunun çalışma zamanında gerekli verilerle nasıl doldurulacağını belirtmek için biçim bileşenini yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2b021-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="2b021-652">[Tasarlanmış biçim yapılandırmasını içe aktarma](#FormatImport) bölümündeki adımları izleyerek gerekli biçimi sağlanan XML dosyasından içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="2b021-653">Alternatif olarak, bu biçimi sıfırdan tasarlamak için [Yeni biçim yapılandırması oluştur](#FormatCreate) bölümündeki adımları tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="2b021-654">Tasarlanan biçim yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="2b021-655">[Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2b021-655">Download the [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="2b021-656">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="2b021-657">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="2b021-658">Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="2b021-659">**Gözat**'ı seçin ve **Questionnaires format.version.1.1.xml** dosyasını bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="2b021-660">Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="2b021-661">Devam etmek için sonraki yordamı atlayın, [Yeni bir biçim yapılandırması oluşturma](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="2b021-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="2b021-662">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b021-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="2b021-663">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-664">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="2b021-665">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="2b021-666">Açılan iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-667">**Yeni** alanına, **Soru formları veri modeline dayalı biçim** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="2b021-668">**Ad** alanına **Soru formu raporu** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="2b021-669">**Veri modeli sürümü** alanında **1**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="2b021-670">Temel veri modelinin belirli bir sürümünü seçerseniz, ilgili veri modeli sürümünün yapısı size, oluşturulan biçimdeki **Model** veri kaynağının yapısı olarak gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="2b021-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="2b021-671">Bu alanı boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-671">You can leave this field blank.</span></span> <span data-ttu-id="2b021-672">Bu durumda, veri modelinin **Taslak** sürümünün yapısı, oluşturulan biçimdeki **Model** veri kaynağının yapısı olarak size sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="2b021-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="2b021-673">Daha sonra modelinizi ayarlayabilir ve biçiminizde bu düzeltmeleri hemen görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="2b021-674">Bu yaklaşım veri modelinizi, model eşlemeyi ve biçimi eşzamanlı olarak yapılandırdığınızda ER çözüm tasarımının verimliliğini artırabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="2b021-675">Temel veri modelinin belirli bir sürümünü seçerseniz, daha sonra bir biçimi düzenlemeye başladığınızda **Taslak** sürümü kullanmaya geçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="2b021-676">**Veri modeli tanımı** alanında, **Kök** tanımını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="2b021-677">Yapılandırma oluşturmak için **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="2b021-678">Rapor şablonunu içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2b021-678">Import a report template</span></span>

1. <span data-ttu-id="2b021-679">**Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="2b021-680">Özel biçim yapılandırmak için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="2b021-681">**Biçim tasarımcısı** sayfasında, Eylem Panosu üzerinde, **İçeri aktar** \> **Excel'den aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="2b021-682">İletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-683">**Şablon ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="2b021-684">Yerel olarak kaydedilmiş **Questionnaires report template.xslx** dosyasını bulup seçin ve **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="2b021-685">Şablonu içe aktarmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-685">Select **OK** to import the template.</span></span>

    ![Rapor şablonunu içe aktarma](./media/er-quick-start1-template-import.png)

<span data-ttu-id="2b021-687">**Excel\\Dosya** biçimi öğesi, otomatik olarak düzenlenebilir biçime kök öğesi olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="2b021-688">Ek olarak, **Excel\\Aralık** biçim öğesi veya **Excel\\Hücre** biçim öğesi içe aktarılan şablonun her tanınan Excel adı için otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="2b021-689">İç içe geçmiş **dize** öğesi bulunan **Excel\\Başlık** biçimi , içe aktarılan şablonun başlık ayarlarını yansıtmak için otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![ER İşlemi tasarımcısına otomatik olarak eklenen öğeleri içeren yapıyı biçimlendirme](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="2b021-691">Biçim yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-691">Configure a format</span></span>

1. <span data-ttu-id="2b021-692">**Biçim Tasarımcısı** sayfasında, biçim ağacında, **Excel** kök öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="2b021-693">Sayfanın sağ tarafındaki **Biçim** sekmesinde, **Ad** alanına <a name="AddFormatRootElement"></a>**Rapor** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="2b021-694">**Dil tercihi** alanında, raporu kullanıcının tercih ettiği dilde çalıştırmak için **Kullanıcı tercihi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="2b021-695">**Kültür tercihi** alanında, raporu kullanıcının tercih ettiği kültürde çalıştırmak için **Kullanıcı tercihi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="2b021-696">Bir ER işlemi için dil ve kültür bağlamlarının nasıl belirtileceği konusunda bilgi için bkz. [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![ER İşlem tasarımcısında tasarlanan rapor için dil ve kültür ayarları yapılandırma](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="2b021-698">Biçim ağacında, kök düğümü genişletin ve sonra **ResultsGroup** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="2b021-699">Tek bir soru formu için birden fazla sonuç grubu olmasını beklemediğinizden **Biçim** sekmesinde **Çoğaltma yönü** alanında  **Çoğaltma yok** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![ER İşlem tasarımcısında Aralık biçimi öğeleri için çoğaltma yönünü tanımlama](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="2b021-701">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="2b021-702">Rapor başlığı için veri bağlamayı tanımlama</span><span class="sxs-lookup"><span data-stu-id="2b021-702">Define the data binding for a report title</span></span>

<span data-ttu-id="2b021-703">Oluşturulan bir raporun başlığını doldurmak için kullanılan bir biçim öğesi için veri bağlaması belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="2b021-704">**Biçim tasarımcısı** sayfasında sağdaki **Eşleme** sekmesinde, **Rapor\\ReportTitle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="2b021-705">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="2b021-706">Formül düzenleyicide, **Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="2b021-707">**Metin çevirisi** iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2b021-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="2b021-708">**Etiket Kodu** alanına, **ReportTitle** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="2b021-709">**Varsayılan dilde metin** alanına **Soru formları raporu** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="2b021-710">**Çevir** i seçin ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="2b021-711">**Metin çevirisi** iletişim kutusunu kapatmak için **Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="2b021-712">Formül düzenleyiciyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-712">Close the formula editor.</span></span>

    ![Oluşturulmuş bir raporun başlığını doldurmak için bağlamayı yapılandırma](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="2b021-714">Geçerli şablon diline bağımlı tüm diğer etiketleri oluşturmak için bu tekniği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="2b021-715">Tek bir ER yapılandırmasının eklenen etiketlerinin tüm desteklenen dillere nasıl çevrilebileceği hakkında bilgi için bkz. [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="2b021-716">Model veri kaynağını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="2b021-716">Review model data source</span></span>

1. <span data-ttu-id="2b021-717">**Biçim tasarımcısı** sayfasındaki **Eşleme** sekmesinde, bu ER biçiminin temel veri modelini temsil eden <a name="ModelDSName"></a>**model** veri kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="2b021-718">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-718">Select **Edit**.</span></span>
3. <span data-ttu-id="2b021-719">**Veri kaynağı özellikleri** iletişim kutusundaki bilgileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="2b021-720">Bu veri kaynağı **Soru formu modeli** yapılandırmasında bulunan **Soru formu** veri modeli bileşeni sürüm 1'i temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2b021-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![ER İşlemi tasarımcısındaki model veri kaynağının özellikleri](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="2b021-722">Biçim öğelerini veri kaynağı alanlarına bağlama</span><span class="sxs-lookup"><span data-stu-id="2b021-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="2b021-723">Çalışma zamanında bir şablonun nasıl doldurulacağını belirtmek için, uygun bir Excel adıyla ilişkilendirilmiş her bir biçim öğesini bu biçimin veri kaynağının tek bir alanına bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="2b021-724">**Biçim Tasarımcısı** sayfasında, biçim ağacında, **Rapor\\CompanyName** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="2b021-725">**Eşleme** sekmesinde **Dize** türünün **model.CompanyName** veri kaynağı alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="2b021-726">Şablona şirket adı girmek için **Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="2b021-727">Biçim ağacında, **Rapor\\Soru formu** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="2b021-728">**Eşleme** sekmesinde **Kayıt listesi** türünün **model.Questionnaire** veri kaynağı alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="2b021-729">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-729">Select **Bind**.</span></span>
7. <span data-ttu-id="2b021-730">Biçim öğeleri ile ilgili daha fazla ayrıntı görmek için **Ayrıntıları göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="2b021-731">**Soru formu** aralığı biçim öğesi dikey olarak yinelenmiş olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="2b021-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="2b021-732">**Kayıt listesi** türünde bir veri kaynağına bağlı olduğunda bağlı veri kaynağının her kaydı için Excel şablonunun uygun **Soru formu** aralığı yinelenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Soru formu aralığı biçim öğesini ER İşlemi tasarımcısında uygun Kayıt listesi veri kaynaklarına bağlama](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="2b021-734">Excel şablonunun **Soru formu** aralığı 5 ile 14 arasındaki satırlar arasında tanımlandığı için, bu satırlar bildirilen her soru formu için yinelenir.</span><span class="sxs-lookup"><span data-stu-id="2b021-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Kayıt listesi veri kaynaklarının her kaydı için oluşturulan raporda tekrarlanacak olan Excel şablonundaki satırlar](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="2b021-736">Aşağıdaki tabloda açıklandığı gibi, kalan biçim öğeleri için benzer bağlamaları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b021-737">Bu tabloda, "Veri kaynağı yolu" sütunundaki bilgiler [göreli yol](relative-path-data-bindings-er-models-format.md) ER özelliğinin açık olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="2b021-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="2b021-738">Biçim öğesi yolu</span><span class="sxs-lookup"><span data-stu-id="2b021-738">Format element path</span></span>                                      | <span data-ttu-id="2b021-739">Veri kaynağı yolu</span><span class="sxs-lookup"><span data-stu-id="2b021-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="2b021-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="2b021-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="2b021-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="2b021-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="2b021-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="2b021-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="2b021-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="2b021-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="2b021-744">Excel\\Soru formu</span><span class="sxs-lookup"><span data-stu-id="2b021-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="2b021-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="2b021-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="2b021-746">Excel\\Soru formu\\Etkin</span><span class="sxs-lookup"><span data-stu-id="2b021-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="2b021-747">**\@.Active**, burada **\@**, **model.Questionnaire** olur</span><span class="sxs-lookup"><span data-stu-id="2b021-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="2b021-748">Excel\\Soru formu\\Kod</span><span class="sxs-lookup"><span data-stu-id="2b021-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="2b021-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="2b021-749">**\@.Code**</span></span> |
    | <span data-ttu-id="2b021-750">Excel\\Soru formu\\Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b021-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="2b021-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="2b021-751">**\@.Description**</span></span> |
    | <span data-ttu-id="2b021-752">Excel\\Soru formu\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="2b021-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="2b021-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="2b021-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="2b021-754">Excel\\Soru formu\\QuestionnaireOrder</span><span class="sxs-lookup"><span data-stu-id="2b021-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="2b021-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="2b021-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="2b021-756">Excel\\Soru formu\\ResultsGroup\\Kod\_</span><span class="sxs-lookup"><span data-stu-id="2b021-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="2b021-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="2b021-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="2b021-758">Excel\\Soru formu\\ResultsGroup\\Açıklama\_</span><span class="sxs-lookup"><span data-stu-id="2b021-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="2b021-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="2b021-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="2b021-760">Excel\\Soru formu\\ResultsGroup \\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="2b021-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="2b021-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="2b021-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="2b021-762">Excel\\Soru formu\\Soru</span><span class="sxs-lookup"><span data-stu-id="2b021-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="2b021-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="2b021-763">**\@.Question**</span></span> |
    | <span data-ttu-id="2b021-764">Excel\\Soru formu\\Soru\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="2b021-765">**\@.CollectionSequenceNumber**, (burada **\@**, **model.Questionnaire.Question** olur)</span><span class="sxs-lookup"><span data-stu-id="2b021-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="2b021-766">Excel\\Soru formu\\Soru\\Kimlik</span><span class="sxs-lookup"><span data-stu-id="2b021-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="2b021-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="2b021-767">**\@.Id**</span></span> |
    | <span data-ttu-id="2b021-768">Excel\\Soru formu\\Soru\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="2b021-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="2b021-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="2b021-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="2b021-770">Excel\\Soru formu\\Soru\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="2b021-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="2b021-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="2b021-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="2b021-772">Excel\\Soru formu\\Soru\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="2b021-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="2b021-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="2b021-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="2b021-774">Excel\\Soru formu\\Soru\\Metin</span><span class="sxs-lookup"><span data-stu-id="2b021-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="2b021-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="2b021-775">**\@.Text**</span></span> |
    | <span data-ttu-id="2b021-776">Excel\\Soru formu\\Soru\\Yanıt</span><span class="sxs-lookup"><span data-stu-id="2b021-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="2b021-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="2b021-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="2b021-778">Excel\\Soru formu\\Soru\\Yanıt\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="2b021-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="2b021-779">**\@.CorrectAnswer**, (burada **\@**, **model.Questionnaire.Answer** olur)</span><span class="sxs-lookup"><span data-stu-id="2b021-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="2b021-780">Excel\\Soru formu\\Soru\\Yanıt\\Puanlar</span><span class="sxs-lookup"><span data-stu-id="2b021-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="2b021-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="2b021-781">**\@.Points**</span></span> |
    | <span data-ttu-id="2b021-782">Excel\\Soru formu\\Soru\\Yanıt\\Metin</span><span class="sxs-lookup"><span data-stu-id="2b021-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="2b021-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="2b021-783">**\@.Text**</span></span> |

9. <span data-ttu-id="2b021-784">Tamamladıktan sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="2b021-785">Aşağıdaki şekil, **Biçim tasarımcısı** sayfasındaki yapılandırılmış veri bağlamalarının son durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b021-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![ER İşlemi tasarımcısında yapılandırılmış veri bağlamaları](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="2b021-787">Belirtilen tüm veri kaynakları ve bağlamalarının tüm koleksiyonu, yapılandırılmış biçimin biçim eşleme bileşenini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2b021-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="2b021-788">Bu biçim eşlemesi, rapor oluşturmak üzere yapılandırılmış biçimi çalıştırdığınızda çağrılır.</span><span class="sxs-lookup"><span data-stu-id="2b021-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="2b021-789">ER'den tasarlanan biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-789">Run a designed format from ER</span></span>

<span data-ttu-id="2b021-790">Şimdi, **Yapılandırmalar** sayfasından test amaçlı olarak tasarlanmış bir biçim çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="2b021-791">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-792">**Yapılandırma** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="2b021-793">**Taslak** durumundaki biçim sürümü için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="2b021-794">**Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="2b021-795">**ER parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="2b021-796">Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="2b021-797">Raporu çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="2b021-798">Oluşturulan raporu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-798">Review the generated report.</span></span>

<span data-ttu-id="2b021-799">[Varsayılan](electronic-reporting-destinations.md#default-behavior) olarak, oluşturulmuş bir rapor indirebileceğiniz bir Excel dosyası olarak teslim edilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="2b021-800">Aşağıdaki çizimler Excel biçiminde oluşturulan raporun iki sayfasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b021-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Excel biçiminde oluşturulmuş rapor örneği, sayfa 1](./media/er-quick-start1-report1a.png)

![Excel biçiminde oluşturulmuş rapor örneği, sayfa 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="2b021-803">Tasarlanan biçimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="2b021-804">Oluşturulan belgenin adını değiştirmek için bir biçimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="2b021-805">Varsayılan olarak, oluşturulan bir belge, geçerli kullanıcının diğer adı kullanılarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="2b021-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="2b021-806">Biçimi değiştirerek, bu davranışı oluşturulan bir belgenin özel mantığınıza göre adlandırılması için değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="2b021-807">Örneğin, oluşturulan bir belgenin adı geçerli oturum tarihi ve saatini ve raporun başlığını temel alabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="2b021-808">**Biçim tasarımcısı** sayfasında **Rapor** kök öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="2b021-809">**Eşleme** sekmesinde **Dosya adını düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="2b021-810">**Formül** alanına, **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="2b021-811">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="2b021-812">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="2b021-813">Soruların sırasını değiştirmek için bir biçimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="2b021-814">Sorular oluşturulmuş bir raporda doğru olarak sıralanmaz.</span><span class="sxs-lookup"><span data-stu-id="2b021-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="2b021-815">Biçimi değiştirerek sırayı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="2b021-816">**Biçim tasarımcısı** sayfasında **Rapor** kök öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="2b021-817">**Eşleme** sekmesinde bulunan biçim ağacında, **Rapor\\Soru formu\\Soru** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b021-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![ER İşlem tasarımcısındaki Aralık türündeki soru biçimi öğesi](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="2b021-819">**Eşleme** sekmesinde **model.Questionnaire** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="2b021-820">**Ekle** \> **İşlevler\\Hesaplanan alan**'ı seçin ve ardından **Ad** alanına **OrderedQuestions** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="2b021-821">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="2b021-822">Formül düzenleyicisinde, **Formül** alanında, geçerli soru formunun soru listesini seri sıra numarasına göre sıralamak için **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="2b021-823">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="2b021-824">Yeni bir hesaplanan alan girişini tamamlamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="2b021-825">**Eşleme** sekmesinde **model.Questionnaire.OrderedQuestions** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="2b021-826">Biçim ağacında **Excel\\Soru formu\\Soru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="2b021-827">**Bağla**'yı seçin ve ardından geçerli **model.Questionnaire.Questions** yolunun iç içe geçmiş öğelerin tüm bağlamalarında yeni **model.Questionnaire.OrderedQuestions** yoluyla değiştirileceğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="2b021-828">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-828">Select **Save**.</span></span>

![ER İşlem tasarımcısında Soru biçimi öğesini yapılandırılan OrderedQuestions veri kaynağına bağlama](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="2b021-830">ER'den değiştirilmiş biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-830">Run a modified format from ER</span></span>

<span data-ttu-id="2b021-831">Artık, ER çerçevesinden test amacıyla değiştirilmiş bir biçim çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="2b021-832">**Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="2b021-833">**ER parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="2b021-834">Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="2b021-835">Raporu çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="2b021-836">Oluşturulan raporu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-836">Review the generated report.</span></span>

<span data-ttu-id="2b021-837">Aşağıdaki şekil, soruların doğru şekilde sıralandığı Excel biçiminde oluşturulmuş bir raporu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b021-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Soruların doğru olarak sıralandığı Excel biçiminde oluşturulmuş rapor](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="2b021-839">Biçim tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-839">Complete the format design</span></span>

1. <span data-ttu-id="2b021-840">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-841">**Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="2b021-842">**Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="2b021-843">**Durumu değiştir** \> **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="2b021-844">Bu yapılandırmanın sürüm 1.1 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b021-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="2b021-845">Sürüm 1.1 artık değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2b021-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="2b021-846">Bu sürüm yapılandırılmış biçimi içerir ve özel raporunuzu yazdırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="2b021-847">Bu yapılandırma için sürüm 1.2 oluşturuldu ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="2b021-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="2b021-848">**Soru formu** raporunuzun biçimini ayarlamak için bu sürümü düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Yapılandırmalar sayfasındaki düzenlenebilir ER yapılandırması](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="2b021-850">Yapılandırılan biçim, **Soru formu** raporu tasarımınızdır ve Finance'a özgü en artefaktlara ilişki içermez.</span><span class="sxs-lookup"><span data-stu-id="2b021-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="2b021-851">Tasarlanan raporu çağırmak için uygulama artefaktları geliştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="2b021-852">Sistem Yöneticisi rolündeki bir kullanıcı olarak, yapılandırılan ER biçiminin özel raporunuzu oluşturmak üzere uygulama kullanıcı arabiriminden (UI) çağrılabilmesi için yeni bir mantık geliştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="2b021-853">Şu anda, ER bu tür mantık yapılandırmak için herhangi bir yetenek sunmaz.</span><span class="sxs-lookup"><span data-stu-id="2b021-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="2b021-854">Bu nedenle, bazı mühendislik çalışmaları gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2b021-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="2b021-855">Yeni mantığı geliştirmek için sürekli yapılandırma destekleyen bir topoloji dağıtmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="2b021-856">Daha fazla bilgi için, [Sürekli yapılandırma ve test otomasyonu destekleyen topolojiler dağıtın](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="2b021-857">Bu topoloji için geliştirme ortamına da erişiminiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="2b021-858">Kullanılabilir ER API'sı hakkında daha fazla bilgi için, bkz. [ER çerçevesi API'sı](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="2b021-859">Kaynak kodu değiştir</span><span class="sxs-lookup"><span data-stu-id="2b021-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="2b021-860">Veri sözleşmesi sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-860">Add a data contract class</span></span>

<span data-ttu-id="2b021-861">Yeni **QuestionnairesErReportContract** sınıfını Microsoft Visual Studio projenize ekleyin ve yapılandırılan ER biçimini çalıştırmak için kullanılması gereken veri sözleşmesini belirten kodu yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="2b021-862">UI oluşturucu sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-862">Add a UI builder class</span></span>

<span data-ttu-id="2b021-863">Yeni **QuestionnairesErReportUIBuilder** sınıfını Visual Studio projenize ekleyin ve çalıştırılması gereken ER biçiminin biçim eşlemesi kimliğini aramak için kullanılacak çalışma zamanı iletişim kutusunu oluşturmak üzere kod yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="2b021-864">Sağlanan kod, yalnızca **[Kök](#RootDefinitionName)** tanımını kullanarak **[Soru formları](#DataModeName)** veri modeline başvuran **Veri modeli** türünde bir veri kaynağı içeren ER biçimlerini arar.</span><span class="sxs-lookup"><span data-stu-id="2b021-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="2b021-865">Alternatif olarak, ER biçimlerini filtrelemek için ER tümleştirme noktalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="2b021-866">Daha fazla bilgi için, bkz. [Biçim eşleme aramasını göstermek için API](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="2b021-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="2b021-867">Veri sağlayıcı sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-867">Add a data provider class</span></span>

<span data-ttu-id="2b021-868">Yeni **QuestionnairesErReportDP** sınıfını Microsoft Visual Studio projenize ekleyin ve yapılandırılan ER biçimini çalıştırmak için kullanılması gereken veri sağlayıcısını belirten kodu yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="2b021-869">Sağlanan kod yalnızca bu veri sağlayıcısına ait veri sözleşmesini içerir.</span><span class="sxs-lookup"><span data-stu-id="2b021-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="2b021-870">Etiket dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-870">Add a labels file</span></span>

<span data-ttu-id="2b021-871">Yeni **QuestionnairesErReportLabels\_en-US** etiket dosyalarını Visual Studio projenize ekleyin ve yeni UI kaynakları için aşağıdaki etiketleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="2b021-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="2b021-872">Şu metni ABD İngilizce (en-US) dilinde içeren yeni menü öğesi için **\@QuestionnairesReport** etiketi: **Soru formları raporu (ER tarafından desteklenir)**</span><span class="sxs-lookup"><span data-stu-id="2b021-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="2b021-873">Seçili bir ER biçimi toplu iş olarak yürütülmek üzere zamanlanırsa, toplu iş başlığı için **\@QuestionnairesReportBatchJobDescription** etiketi</span><span class="sxs-lookup"><span data-stu-id="2b021-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="2b021-874">Rapor hizmeti sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-874">Add a report service class</span></span>

<span data-ttu-id="2b021-875">Yeni **QuestionnairesErReportService** sınıfını Visual Studio projenize ekleyin ve ER biçimini çağıran, bunu bir biçim eşleme kimliğiyle tanımlayan ve parametre olarak bir veri sözleşmesi sağlayan kodu yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="2b021-876">Uygulama verilerini çalıştıran bir ER biçimi kullanmanız gerektiğinde, biçim eşlemesinde **Veri modeli** türünde veri kaynağı yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="2b021-877">Bu veri kaynağı, tek bir kök tanımı kullanılarak belirtilen veri modelinin belirli bir bölümüne başvurur.</span><span class="sxs-lookup"><span data-stu-id="2b021-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="2b021-878">ER biçimi çalıştırıldığında, belirli bir model ve kök tanımı için yapılandırılmış uygun ER model eşlemeye erişmek için bu veri kaynağını çağırır.</span><span class="sxs-lookup"><span data-stu-id="2b021-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="2b021-879">Kaynak kodda hazırlayabileceğiniz ve veri sözleşmesinin bir parçası olarak saklayabileceğiniz tüm bilgiler, bu türdeki ER model eşlemesi kullanılarak çalışan ER biçimine geçirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="2b021-880">ER model eşlemesinde, **[QuestionnairesErReportContract](#DataContractClass)** sınıfına başvuran **Nesne** türünde bir veri kaynağı yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="2b021-881">Bir model eşlemesi tanımlamak için bu model eşlemesini çağıran bir veri kaynağı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="2b021-882">Sağlanan kodda, bu veri kaynağı, **[model](#ModelDSName)** değeri olan **ERModelDataSourceName** sabit değeri tarafından belirtilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="2b021-883">Model eşlemesinde veri sözleşmesini göstermek için hangi veri kaynağının kullanıldığını tanımlamak üzere bir veri kaynağı adı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="2b021-884">Sağlanan kodda, bu ad, <a name="DataContractDSName"></a>**RunTimeParameters** değeri olan **ParametersDataSourceName** sabit değeri tarafından belirtilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="2b021-885">Yeni bir ortamda, ER model eşleme tasarımcısında bu tür sınıfın kullanılabilir olması için ER meta verilerini yenilemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="2b021-886">Daha fazla bilgi için bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="2b021-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="2b021-887">Rapor denetleyicisi sınıfı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-887">Add a report controller class</span></span>

<span data-ttu-id="2b021-888">Yeni **QuestionnairesErReportController** sınıfını Visual Studio projenize ekleyin ve sağlanan **QuestionnairesErReportUIBuilder** sınıfının mantığını temel alarak oluşturulan iletişim kutusunda ER biçimini tercihinize göre zaman uyumlu modda veya toplu işlem modunda çalıştıran kodu yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="2b021-889">Menü öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-889">Add a menu item</span></span>

<span data-ttu-id="2b021-890">Yeni **QuestionnairesErReport** menü öğesini Visual Studio projenize ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="2b021-891">**Nesne** özelliğinde, bu menü öğesi **QuestionnairesErReportController** sınıfına başvurur ve bir ER biçimini seçmek ve çalıştırmak için bir kullanıcı izni belirtmek üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b021-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="2b021-892">**Etiket** özelliğinde, bu menü öğesi daha önce oluşturduğunuz **\@QuestionnairesReport** etiketine başvurur; böylece uygulama kullanıcı arabiriminde doğru metin gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="2b021-893">Menüye menü öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-893">Add a menu item to a menu</span></span>

<span data-ttu-id="2b021-894">Varolan **KM** menüsünü Visual Studio projenize ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="2b021-895">Bu menüye **Çıktı** türünde yeni bir **QuestionnairesErReport** öğesi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="2b021-896">Bu öğenin önceki bölümde açıklanan **QuestionnairesErReport** menü öğesine başvurması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b021-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="2b021-897">Visual Studio projesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b021-897">Build a Visual Studio project</span></span>

<span data-ttu-id="2b021-898">Yeni bir menü öğesini kullanıcıların kullanabilmesini sağlamak için projenizi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2b021-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="2b021-899">Uygulamadan bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-899">Run a format from the application</span></span>

1. <span data-ttu-id="2b021-900">**Soru formu** \> **Tasarım** \> **Soru formu raporu (ER tarafından desteklenir)** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Yapılandırılan ER biçimini çalıştırmak için Soru Formu modülündeki Soru formları raporu (ER tarafından desteklenir) menü öğesini seçme](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="2b021-902">İletişim kutusunda, **Biçim eşleme** alanında, **Soru formları raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="2b021-903">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-903">Select **OK**.</span></span>
4. <span data-ttu-id="2b021-904">**Elektronik rapor parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="2b021-905">Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="2b021-906">Raporu çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-906">Select **OK** to run the report.</span></span>

    ![Elektronik rapor iletişim kutusunda seçim ölçütünü belirtme](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="2b021-908">Oluşturulan raporu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="2b021-909">Tasarlanan ER çözümünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-909">Tune a designed ER solution</span></span>

<span data-ttu-id="2b021-910">Yapılandırılan ER çözümünü, çalışan ER biçiminin ayrıntılarına erişmek için geliştirdiğiniz veri sağlayıcı sınıfını kullanacak ve oluşturulan rapora bu ER biçiminin adını girecek şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="2b021-911">Model eşlemesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="2b021-912">Veri sözleşmesi nesnesine erişmek için veri kaynakları ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="2b021-913">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-914">**Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="2b021-915">**Veri kaynağı eşleme modeli** sayfasını açmak için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="2b021-916">Model eşleme tasarımcısında seçilen eşlemeyi açmak için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="2b021-917">**Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Nesne**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="2b021-918">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="2b021-919">İletişim kutusunda, **Ad** alanına, **QuestionnairesErReportService** sınıfının kaynak kodunda tanımlandığı şekilde **[RunTimeParameters](#DataContractDSName)** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="2b021-920">**Sınıf** alanına daha önce kodlanmış olan **[QuestionnairesErReportContract](#DataContractClass)** öğesini girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="2b021-921">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-921">Select **OK**.</span></span>
10. <span data-ttu-id="2b021-922">**RunTimeParameters** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b021-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="2b021-923">Eklenen veri kaynağı, çalışan ER biçim eşlemesinin kayıt kodu ile ilgili bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2b021-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![ER model eşleme tasarımcısında eklenen veri kaynağı](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="2b021-925">ER biçim eşleme kayıtlarına erişmek için veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="2b021-926">ER biçim eşleme kayıtlarına erişmek üzere bir veri kaynağı ekleyerek seçili model eşlemesini düzenlemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="2b021-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="2b021-927">**Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="2b021-928">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="2b021-929">İletişim kutusunda, **Ad** alanına **ER1** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="2b021-930">**Tablo** alanına, **ERFormatMappingTable** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="2b021-931">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="2b021-932">Çalışan bir ER biçimin biçim eşleme kaydına erişmek için veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="2b021-933">Çalışan ER biçiminin eşleme kaydına erişmek üzere bir veri kaynağı ekleyerek seçili model eşlemesini düzenlemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="2b021-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="2b021-934">**Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="2b021-935">**Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="2b021-936">İletişim kutusunda, **Ad** alanına **ER2** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="2b021-937">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="2b021-938">Formül Düzenleyicisinde, **Formül** alanına **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="2b021-939">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="2b021-940">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="2b021-941">Çalışan ER biçiminin adını veri modeline girme</span><span class="sxs-lookup"><span data-stu-id="2b021-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="2b021-942">Seçili model eşlemesini, veri modelinde çalışan ER biçimi adı girilmiş olacak şekilde düzenlemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="2b021-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="2b021-943">**Model eşleme tasarımcısı** sayfasında, **Veri modeli** bölmesinde, **ExecutionContext** öğesini genişletin ve **ExecutionContext\\FormatName** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="2b021-944">**Veri modeli** bölmesinde, seçili veri modeli alanı için bir veri bağlamayı yapılandırmak üzere **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="2b021-945">Formül düzenleyicisinde, **Formül** alanına **FIRSTORNULL (ER2.'\>Relations'.Format).Name** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="2b021-946">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="2b021-947">**FormatName** alanını kullandığınız için, yapılandırılan model eşlemesi, yürütme sırasında bu model eşlemesini çağıran bir ER biçimi adı ortaya çıkarır.</span><span class="sxs-lookup"><span data-stu-id="2b021-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Veri modeli alanını, ER model eşleme tasarımcısındaki eklenen veri kaynağı yöntemine bağlama](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="2b021-949">Model eşleme tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="2b021-950">**Model eşleme tasarımcısı** sayfasında **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="2b021-951">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-951">Close the page.</span></span>
3. <span data-ttu-id="2b021-952">Model eşlemeleri sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="2b021-953">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Soru formu eşleme** yapılandırmasının hala seçili olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2b021-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="2b021-954">Ardından, **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="2b021-955">**Durumu değiştir** \> **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="2b021-956">Bu yapılandırmanın sürüm 1.2 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b021-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="2b021-957">Sürüm 1.2 artık değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2b021-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="2b021-958">Bu sürüm yapılandırılmış model eşlemesini içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="2b021-959">Bu yapılandırma için sürüm 1.3 oluşturuldu ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="2b021-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="2b021-960">**Soru formu** model eşlemesini ayarlamak için bu sürümü düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="2b021-961">Biçim değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b021-961">Modify a format</span></span>

<span data-ttu-id="2b021-962">Yapılandırılmış ER biçimini adı, ER biçimi çalıştırıldığında oluşturulan bir raporun altbilgisi olarak gösterilecek şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="2b021-963">Yeni bir biçim öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b021-963">Add a new format element</span></span>

1. <span data-ttu-id="2b021-964">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-965">**Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="2b021-966">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-966">Select **Designer**.</span></span>
4. <span data-ttu-id="2b021-967">**Biçim tasarımcısı** sayfasında **Rapor** kök öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="2b021-968">Seçili **Rapor** kök öğesi için yeni bir iç içe biçim öğesi eklemek üzere **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="2b021-969">**Excel \\Alt bilgi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="2b021-970">**Ad** alanına, **Alt bilgi** yazın.</span><span class="sxs-lookup"><span data-stu-id="2b021-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="2b021-971">**Rapor\Alt bilgi**'yi ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="2b021-972">**Metin\\Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="2b021-973">Eklenen biçim öğesini bağlama</span><span class="sxs-lookup"><span data-stu-id="2b021-973">Bind the added format element</span></span>

1. <span data-ttu-id="2b021-974">**Biçim tasarımcısı** sayfasındaki **Eşleme** sekmesinde, biçim ağacında, **Alt bilgi\\Dize** öğesi için **Formülü düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="2b021-975">Formül düzenleyicisinde **Formül** alanına **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** girin.</span><span class="sxs-lookup"><span data-stu-id="2b021-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="2b021-976">**Kaydet**'i seçip formül düzenleyicisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="2b021-977">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-977">Select **Save**.</span></span>

<span data-ttu-id="2b021-978">Yapılandırılmış biçim şimdi, adı **Altbilgi\\Dize** öğesi kullanılarak oluşturulan bir raporun altbilgisine girilecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b021-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![ER İşlem tasarımcısında, yapılandırılmış biçime Alt bilgi biçim öğesi ekleme](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="2b021-980">Biçim tasarımını tamamlama</span><span class="sxs-lookup"><span data-stu-id="2b021-980">Complete the format design</span></span>

1. <span data-ttu-id="2b021-981">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b021-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="2b021-982">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Soru formu raporu** yapılandırmasının hala seçili olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2b021-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="2b021-983">Ardından, **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="2b021-984">**Durumu değiştir** \> **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="2b021-985">Bu yapılandırmanın sürüm 1.2 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b021-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="2b021-986">Sürüm 1.2 artık değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2b021-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="2b021-987">Bu sürüm yapılandırılmış biçim içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b021-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="2b021-988">Bu yapılandırma için sürüm 1.3 oluşturuldu ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="2b021-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="2b021-989">**Soru formu** raporunu ayarlamak için bu sürümü düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b021-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="2b021-990">Uygulamadan bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-990">Run a format from the application</span></span>

1. <span data-ttu-id="2b021-991">**Soru formu** \> **Tasarım** \> **Soru formu raporu (ER tarafından desteklenir)** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="2b021-992">İletişim kutusunda, **Biçim eşleme** alanında, **Soru formları raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="2b021-993">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-993">Select **OK**.</span></span>
4. <span data-ttu-id="2b021-994">**ER parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="2b021-995">Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="2b021-996">Raporu çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="2b021-997">Excel biçiminde oluşturulan raporu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="2b021-998">Oluşturulan raporun altbilgisi, bunu oluşturmak için kullanılan ER biçiminin adını içerir.</span><span class="sxs-lookup"><span data-stu-id="2b021-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Excel biçiminde oluşturulan rapor](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="2b021-1000">ER'den bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-1000">Run a format from ER</span></span>

1. <span data-ttu-id="2b021-1001">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b021-1002">**Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="2b021-1003">Eylem Bölmesinde, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="2b021-1004">**Elektronik rapor parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="2b021-1005">Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="2b021-1006">Raporu çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="2b021-1007">Excel biçiminde oluşturulan raporu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="2b021-1008">Oluşturulan raporun altbilgisi, oluşturulduğu sırada çalıştırılan ER biçimi tarafından çağrıldığında, veri sözleşme nesnesi çalışan model eşlemesine geçirilmediği için, bunu oluşturmak için kullanılan ER biçiminin adını içermez.</span><span class="sxs-lookup"><span data-stu-id="2b021-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="2b021-1009">Ekran önizleme için biçim hedefi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b021-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="2b021-1010">Sırasıyla **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama hedefi** seçimlerini yapın.</span><span class="sxs-lookup"><span data-stu-id="2b021-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="2b021-1011">**Elektronik raporlama hedefi** sayfasında, yapılandırılan **Soru formu raporu** ER biçimi için bir hedef kayıt ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="2b021-1012">**Dosya hedefi** hızlı sekmesinde, yapılandırılan **Soru formu raporu** ER biçiminin kök öğesi olarak [eklenmiş](#AddFormatRootElement) olan **Rapor** biçim bileşeni için **Ekran** [hedefini](er-destination-type-screen.md) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b021-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="2b021-1013">**PDF dönüştürme ayarları** hızlı sekmesinde, bir raporu **Yatay** sayfa yönünü kullanan bir [PDF biçimine](electronic-reporting-destinations.md#OutputConversionToPDF) dönüştürmek için hedefi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Elektronik raporlama hedef sayfasındaki ER biçimi için özel Ekran hedefi yapılandırma](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="2b021-1015">PDF belgesi olarak önizlemek için uygulamadan bir biçim çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2b021-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="2b021-1016">**Soru formu** \> **Tasarım** \> **Soru formu raporu (ER tarafından desteklenir)** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="2b021-1017">İletişim kutusunda, **Biçim eşleme** alanında, **Soru formları raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="2b021-1018">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1018">Select **OK**.</span></span>
4. <span data-ttu-id="2b021-1019">**Elektronik rapor parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2b021-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="2b021-1020">Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="2b021-1021">**Hedefler** hızlı sekmesinde, **Çıktı** alanının **Ekran** olarak ayarlanmış olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="2b021-1022">Yapılandırılan hedefi değiştirmek istiyorsanız, **Değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Yapılandırılan hedefi değiştirebileceğiniz ER raporu çalışma zamanı iletişim kutusu](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="2b021-1024">Raporu çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="2b021-1025">PDF biçiminde oluşturulan raporu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="2b021-1025">Review the generated report in PDF format.</span></span>

    ![PDF biçiminde oluşturulan raporunun ekran önizlemesi](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="2b021-1027">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2b021-1027">Additional resources</span></span>

- [<span data-ttu-id="2b021-1028">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="2b021-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2b021-1029">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="2b021-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="2b021-1030">Çok dilli raporlar tasarlama</span><span class="sxs-lookup"><span data-stu-id="2b021-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="2b021-1031">ER çerçevesi API'si</span><span class="sxs-lookup"><span data-stu-id="2b021-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="2b021-1032">CASE işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="2b021-1033">CONCATENATE işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="2b021-1034">DATETIMEFORMAT işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="2b021-1035">FILTER işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="2b021-1036">FIRSTORNULL işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="2b021-1037">FORMAT işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="2b021-1038">IF işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="2b021-1039">ORDERBY işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="2b021-1040">SESSIONNOW işlevi</span><span class="sxs-lookup"><span data-stu-id="2b021-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
