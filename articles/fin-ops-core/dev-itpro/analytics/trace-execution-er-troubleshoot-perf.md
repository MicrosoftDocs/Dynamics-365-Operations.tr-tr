---
title: Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme
description: Bu konu, performans sorunlarını gidermek amacıyla elektronik raporlama (ER) içindeki performans izleme özelliğinin nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295585"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="60221-103">Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izle</span><span class="sxs-lookup"><span data-stu-id="60221-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="60221-104">Elektronik raporlama (ER) konfigürasyonlarının elektronik belgeler oluşturmak amacıyla tasarlanması işleminin bir parçası olarak, uygulamadan veri elde etmek ve oluşturulan çıktıya girmek için kullanılan yöntemi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="60221-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="60221-105">ER performans izleme özelliği, ER biçim yürütmesi ve performans sorunlarını gidermek için onları kullanma ile ilgili zamanı ve maliyeti önemli ölçüde azaltmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="60221-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="60221-106">Bu kılavuz, yürütülen ER biçimleri için performans izlemelerinin nasıl alınacağı ve performansın artırılmasına yardımcı olmak amacıyla bu izlemelerin nasıl kullanılacağı hakkında yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="60221-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="60221-107">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="60221-107">Prerequisites</span></span>

<span data-ttu-id="60221-108">Bu kılavuzdaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="60221-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="60221-109">Aşağıdaki rollerden birine erişim:</span><span class="sxs-lookup"><span data-stu-id="60221-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="60221-110">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="60221-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="60221-111">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="60221-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="60221-112">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="60221-112">System administrator</span></span>

- <span data-ttu-id="60221-113">Aşağıdaki rollerden biri için, uygulamanınkiyle aynı kiracı için sağlanan Regulatory Configuration Services (RCS) örneğine erişim:</span><span class="sxs-lookup"><span data-stu-id="60221-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="60221-114">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="60221-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="60221-115">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="60221-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="60221-116">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="60221-116">System administrator</span></span>

<span data-ttu-id="60221-117">Ayrıca, aşağıdaki dosyaları da indirip yerel olarak depolamalısınız.</span><span class="sxs-lookup"><span data-stu-id="60221-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="60221-118">Dosya</span><span class="sxs-lookup"><span data-stu-id="60221-118">File</span></span>                                  | <span data-ttu-id="60221-119">İçerik</span><span class="sxs-lookup"><span data-stu-id="60221-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="60221-120">Performans izleme modeli sürüm 1</span><span class="sxs-lookup"><span data-stu-id="60221-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="60221-121">Örnek ER verisi modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="60221-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="60221-122">Performans izleme meta veri sürüm 1</span><span class="sxs-lookup"><span data-stu-id="60221-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="60221-123">Örnek ER meta verisi yapılandırması</span><span class="sxs-lookup"><span data-stu-id="60221-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="60221-124">Performans izleme eşleştirme sürümü 1.1</span><span class="sxs-lookup"><span data-stu-id="60221-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="60221-125">Örnek ER model eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="60221-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="60221-126">Performans izleme biçimi sürümü 1.1</span><span class="sxs-lookup"><span data-stu-id="60221-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="60221-127">Örnek ER biçim yapılandırması</span><span class="sxs-lookup"><span data-stu-id="60221-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="60221-128">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="60221-128">Configure ER parameters</span></span>

<span data-ttu-id="60221-129">Uygulamada oluşturulan her bir ER performans izleme, yürütme günlükleri kaydının bir eki olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="60221-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="60221-130">Belge yönetimi (DM) çerçevesi, bu ekleri yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="60221-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="60221-131">Performans izlemelerini iliştirmek için kullanılması gereken DM belge türünü belirtmek için ER parametrelerini önceden yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="60221-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="60221-132">**Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="60221-133">Sonra, **Elektronik raporlama parametreleri** sayfasında, **Ekler** sekmesinde, **Diğerleri** alanında, performans izlemeleri için kullanılacak DM belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektronik raporlama parametreleri sayfası](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="60221-135">**Diğer** arama alanında kullanılabilmesi için bir DM belgesi türünün aşağıdaki şekilde **Belge türleri** sayfasında yapılandırılması gerekir (**Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**):</span><span class="sxs-lookup"><span data-stu-id="60221-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="60221-136">**Sınıf:** Dosya iliştir</span><span class="sxs-lookup"><span data-stu-id="60221-136">**Class:** Attach file</span></span>
- <span data-ttu-id="60221-137">**Grup:** Dosya</span><span class="sxs-lookup"><span data-stu-id="60221-137">**Group:** File</span></span>

![Belge türleri sayfası](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="60221-139">DM ekleri şirkete özgü olduğundan, seçilen belge türü, geçerli örneğin tüm şirketlerinde kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="60221-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="60221-140">RCS parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="60221-140">Configure RCS parameters</span></span>

<span data-ttu-id="60221-141">Oluşturulan ER performans izlemeleri, ER biçim Tasarımcısı ve ER eşleme Tasarımcısı kullanılarak analiz için RCS'ye aktarılır.</span><span class="sxs-lookup"><span data-stu-id="60221-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="60221-142">ER performans izleri ER biçimiyle ilgili yürütme günlükleri kaydının ekleri olarak depolandığından, RCS parametrelerini önceden yapılandırmalısınız, böylece performans izlemelerini iliştirmek için kullanılacak DM belge türü belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="60221-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="60221-143">Şirketiniz için sağlanmış olan RCS örneğinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="60221-144">Sonra, **Elektronik raporlama parametreleri** sayfasında, **Ekler** sekmesinde, **Diğerleri** alanında, performans izlemeleri için kullanılacak DM belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS içindeki Elektronik raporlama parametreleri sayfası](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="60221-146">**Diğer** arama alanında kullanılabilmesi için bir DM belgesi türünün aşağıdaki şekilde **Belge türleri** sayfasında yapılandırılması gerekir (**Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**):</span><span class="sxs-lookup"><span data-stu-id="60221-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="60221-147">**Sınıf:** Dosya iliştir</span><span class="sxs-lookup"><span data-stu-id="60221-147">**Class:** Attach file</span></span>
- <span data-ttu-id="60221-148">**Grup:** Dosya</span><span class="sxs-lookup"><span data-stu-id="60221-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="60221-149">Bir ER çözümü tasarla</span><span class="sxs-lookup"><span data-stu-id="60221-149">Design an ER solution</span></span>

<span data-ttu-id="60221-150">Satıcı hareketleri sunan yeni bir rapor oluşturmak üzere yeni bir ER çözümü tasarladığınızı varsayın.</span><span class="sxs-lookup"><span data-stu-id="60221-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="60221-151">Şu anda, seçilen satıcı için hareketleri **Satıcı hareketleri** sayfasında bulabilirsiniz (**Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin, bir satıcı seçin ve Eylem Panosu üzerinde, **Satıcı** sekmesinde, **Hareketler** grubunda, **Hareketler**'i seçin).</span><span class="sxs-lookup"><span data-stu-id="60221-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="60221-152">Ancak, tüm satıcı hareketinin elektronik bir belgede XML biçiminde aynı anda olmasını istersiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="60221-153">Bu çözüm, gerekli veri modelini, meta verileri, model eşlemeyi ve biçim bileşenlerini içeren birkaç ER yapılandırmasından oluşur.</span><span class="sxs-lookup"><span data-stu-id="60221-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="60221-154">Şirketiniz için sağlanan RCS örneğine oturum açın.</span><span class="sxs-lookup"><span data-stu-id="60221-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="60221-155">Bu kılavuzda, **Litware, Inc.** örnek şirket için yapılandırmalar oluşturacak ve değiştireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="60221-156">Bu nedenle, bu konfigürasyon sağlayıcısının RCS'ye eklenmiş olduğundan ve etkin olarak seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="60221-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="60221-157">Yönergeler için, bkz. [Yapılandırma sağlayıcıları oluşturmak ve bunları etkin olarak işaretlemek yordamına](tasks/er-configuration-provider-mark-it-active-2016-11.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="60221-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="60221-158">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="60221-159">**Yapılandırmalar** sayfasında, önkoşul olarak karşıdan yüklediğiniz ER yapılandırmalarını aşağıdaki sırada içe aktarın: veri modeli, meta veriler, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="60221-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="60221-160">Her bir yapılandırma için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="60221-161">Eylem Panosunda, **Exchange \> XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="60221-162">Gerekli ER yapılandırması için XML biçiminde uygun dosyayı seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="60221-163">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-163">Select **OK**.</span></span>

    ![RCS içinde Yapılandırmalar sayfası](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="60221-165">Çalışmayı izlemek için ER çözümünü çalıştırın</span><span class="sxs-lookup"><span data-stu-id="60221-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="60221-166">ER çözümünün ilk sürümünü tasarlamayı bitirdiğinizi varsayalım.</span><span class="sxs-lookup"><span data-stu-id="60221-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="60221-167">Şimdi bunu örneğinizde test etmek ve yürütme performansını analiz etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="60221-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="60221-168">ER yapılandırmalarını RCS'den Finance and Operations içine aktarma</span><span class="sxs-lookup"><span data-stu-id="60221-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="60221-169">Uygulama örneğinizde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="60221-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="60221-170">Bu kılavuzda, yapılandırmaları RCS örneğinizden (ER bileşenlerinizi tasarladığınız yerden) örneğinize (test edeceğiniz ve son olarak kullanacağınız) içe aktarırsınız.</span><span class="sxs-lookup"><span data-stu-id="60221-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="60221-171">Bu nedenle, gerekli tüm yapıların hazırlandığından emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="60221-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="60221-172">Talimatlar için bkz. [Düzenleyici Yapılandırma Hizmeti'nden (RCS) Elektronik raporlama (ER) yapılandırmalarını içe aktarma](rcs-download-configurations.md) yordamı.</span><span class="sxs-lookup"><span data-stu-id="60221-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="60221-173">Yapılandırmaları RCS'den uygulamada içe aktarmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="60221-174">**Elektronik raporlama** çalışma alanında, **Litware, Inc.** yapılandırma sağlayıcısının döşemesi üzerinde **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="60221-175">**Yapılandırma deposu** sayfasında, **RCS** türünün deposunu seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="60221-176">**Yapılandırmalar** hızlı sekmesinde, **Performans izleme biçimi** yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="60221-177">**Sürümler** hızlı sekmesinde seçilen yapılandırmanın sürüm **1.1**'ini ve sonra **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Yapılandırma havuzu sayfası](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="60221-179">Veri modeli ve model eşleme yapılandırmalarının ilgili sürümleri, içe aktarılan ER biçim konfigürasyonu için önkoşul olarak otomatik içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="60221-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="60221-180">ER performans izlemesini aç</span><span class="sxs-lookup"><span data-stu-id="60221-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="60221-181">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="60221-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="60221-182">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="60221-183">**Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="60221-184">**Yürütme izleme biçimi** alanda, yürütme ayrıntılarının ER biçimi ve eşleme öğelerinde depolanması gereken oluşturulmuş performans izlemesinin biçimini belirtin:</span><span class="sxs-lookup"><span data-stu-id="60221-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="60221-185">**Hata ayıklama izleme biçimi**: Kısa yürütme süresine sahip bir ER biçimini etkileşimli olarak çalıştırmayı planlıyorsanız bu değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="60221-186">Böylece, ER biçimi yürütme ile ilgili ayrıntılar topluluğu başlatılır.</span><span class="sxs-lookup"><span data-stu-id="60221-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="60221-187">Bu değer seçildiğinde, performans izlemesi aşağıdaki eylemlerde harcanan süre hakkında bilgi toplar:</span><span class="sxs-lookup"><span data-stu-id="60221-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="60221-188">Her bir veri kaynağını veri almak için çağırılan model eşlemesinde çalıştırma</span><span class="sxs-lookup"><span data-stu-id="60221-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="60221-189">Oluşturulan çıktıya veri girmek için her biçim öğesini işlemek</span><span class="sxs-lookup"><span data-stu-id="60221-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="60221-190">**Hata ayıklama izleme biçimi** değerini seçerseniz, izleme içeriğini ER İşlem tasarımcısında analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="60221-191">Burada, izlemede bahsedilen ER biçimini veya eşleme öğelerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="60221-192">**Toplama izleme biçimi**: Toplu iş modunda uzun yürütme süresine sahip bir ER biçimini çalıştırmayı planlıyorsanız bu değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="60221-193">Böylece, ER biçimi yürütme ile ilgili toplama ayrıntıları topluluğu başlatılır.</span><span class="sxs-lookup"><span data-stu-id="60221-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="60221-194">Bu değer seçildiğinde, performans izlemesi aşağıdaki eylemlerde harcanan süre hakkında bilgi toplar:</span><span class="sxs-lookup"><span data-stu-id="60221-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="60221-195">Her bir veri kaynağını veri almak için çağırılan model eşlemesinde çalıştırma</span><span class="sxs-lookup"><span data-stu-id="60221-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="60221-196">Her bir veri kaynağını veri almak için çağırılan biçim eşlemesinde çalıştırma</span><span class="sxs-lookup"><span data-stu-id="60221-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="60221-197">Oluşturulan çıktıya veri girmek için her biçim öğesini işlemek</span><span class="sxs-lookup"><span data-stu-id="60221-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="60221-198">**Toplu izleme biçimi** değeri Microsoft Dynamics 365 Finance Sürüm 10.0.20 ve sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="60221-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="60221-199">ER biçim tasarımcısı ve ER model eşleme tasarımcısında, tek bir bileşen için toplam yürütme süresini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="60221-200">Ek olarak izleme, yürütme sayısı ve tek bir yürütmenin minimum ve maksimum süresi gibi yürütme ayrıntılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="60221-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="60221-201">Bu izleme, izlenen bileşenler yoluna göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="60221-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="60221-202">Bu nedenle, tek bir üst bileşen birkaç adlandırılmamış alt bileşen içerdiğinde veya birden fazla alt bileşen aynı ada sahip olduğunda istatistikler yanlış olabilir.</span><span class="sxs-lookup"><span data-stu-id="60221-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="60221-203">ER model eşleme ve ER biçimde bileşenlerinin yürütülmesine dair belirli ayrıntıları toplamak için aşağıdaki seçenekleri **Evet** olarak ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="60221-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="60221-204">**Sorgu istatistiklerini topla** – Bu seçenek etkinleştirildiğinde, performans izlemesi aşağıdaki bilgileri toplar:</span><span class="sxs-lookup"><span data-stu-id="60221-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="60221-205">Veri kaynakları tarafından yapılan veritabanı çağrılarının sayısı</span><span class="sxs-lookup"><span data-stu-id="60221-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="60221-206">Veritabanına yapılan yinelenen çağrıların sayısı</span><span class="sxs-lookup"><span data-stu-id="60221-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="60221-207">Veritabanı çağrılarını yapmak için kullanılan SQL deyimlerinin ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="60221-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="60221-208">**Önbelleğe alma erişimini izleme** – Bu seçenek açıldığında, performans izlemesi ER modeli eşlemesinin önbellek kullanımıyla ilgili bilgilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="60221-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="60221-209">**Veri erişimini izle** – Bu seçenek etkinleştirildiğinde, performans izlemesi kayıt listesi türünün yürütülmüş veri kaynakları için veritabanına yapılan çağrı sayısıyla ilgili bilgi toplar.</span><span class="sxs-lookup"><span data-stu-id="60221-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="60221-210">**Liste numaralandırmasını izle** – Bu seçenek etkinleştirildiğinde, performans izlemesi kayıt listesi türünün veri kaynakları için talep edilen kayıtların sayısı hakkında bilgi toplar.</span><span class="sxs-lookup"><span data-stu-id="60221-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="60221-211">**Kullanıcı parametreleri** iletişim kutusundaki parametreler kullanıcıya ve geçerli şirkete özgüdür.</span><span class="sxs-lookup"><span data-stu-id="60221-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Kullanıcı parametreleri iletişim kutusu](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="60221-213">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="60221-213">Run the ER format</span></span>

1. <span data-ttu-id="60221-214">**DEMF** şirketini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="60221-215">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="60221-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="60221-216">**Yapılandırmalar** sayfasında, yapılandırma ağacında , **Performans izleme biçimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="60221-217">Eylem Bölmesinde, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="60221-218">Oluşturulan dosyanın altı satıcıda bulunan 265 hareketleri temsil ettiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="60221-219">Yürütme izlemesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="60221-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="60221-220">Oluşturulan izlemeyi uygulamadan dışa aktarın</span><span class="sxs-lookup"><span data-stu-id="60221-220">Export the generated trace from the application</span></span>

<span data-ttu-id="60221-221">Performans izlemeleri, kaynak ER biçiminden alınır ve harici bir ZIP dosyasına serileştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="60221-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="60221-222">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırma hata ayıklama günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="60221-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="60221-223">**Elektronik raporlama yürütme günlükleri** sayfasında, sol tarafta, **Yapılandırma adı** alanında, **Performans izleme biçimi**'ni seçerek, **Performans izleme biçimi** yapılandırması yürütülmesi tarafından oluşturulan günlük kayıtlarını bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="60221-224">Sayfanın sağ üst köşesindeki **Ekler** düğmesini (ataş simgesi) seçin veya **Ctrl+Shift+A**'ya basın.</span><span class="sxs-lookup"><span data-stu-id="60221-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Elektronik raporlama yürütme günlükleri sayfasındaki Ekler düğmesi](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="60221-226">**Elektronik raporlama yürütme günlükleri için ekler** sayfasında, Eylem Panosunda, **Aç**'ı seçerek performans izlemeyi bir zip dosyası olarak elde edin ve yerel olarak depolayın.</span><span class="sxs-lookup"><span data-stu-id="60221-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Elektronik raporlama yürütme günlükleri için ekler](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="60221-228">Oluşturulan izleme, yalnızca **GUID** biçimindeki benzersiz bir rapor tanımlayıcısı aracılığıyla kaynak ER raporuna referans sağlar.</span><span class="sxs-lookup"><span data-stu-id="60221-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="60221-229">Biçimin sürüm numaralandırması dikkate alınmıyor.</span><span class="sxs-lookup"><span data-stu-id="60221-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="60221-230">Çalıştırılan ve ER model eşleme için oluşturulan performans izleme arasındaki ilişkinin, kullanılan kök tanımlayıcısını ve ortak veri modelini temel aldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="60221-231">Biçim ve model eşleşmesinin sürüm numaralandırması dikkate alınmıyor.</span><span class="sxs-lookup"><span data-stu-id="60221-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="60221-232">**Model eşleme için varsayılan** bayrağı ayarı da dikkate alınmıyor.</span><span class="sxs-lookup"><span data-stu-id="60221-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="60221-233">Oluşturulan izlemeyi RCS'ye içe aktarın</span><span class="sxs-lookup"><span data-stu-id="60221-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="60221-234">RCS içinde, **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="60221-235">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans izleme modeli** öğesini genişletin ve **Performans izleme biçimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="60221-236">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="60221-237">**Biçim tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="60221-238">**Performans izleme sonucu ayarları** iletişim kutusunda, **Performans izleme içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="60221-239">**Gözat**'ı seçerek, daha önce içe aktardığınız zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="60221-240">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-240">Select **OK**.</span></span>

    ![RCS içindeki performans izleme sonuç ayarları iletişim kutusu](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="60221-242">RCS- Biçim yürütme içindeki analiz için performans izlemesini kullan</span><span class="sxs-lookup"><span data-stu-id="60221-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="60221-243">RCS içinde, **Biçim tasarımcısı** sayfasında, **Genişlet/daralt**'ı seçerek tüm biçim öğelerinin içeriğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="60221-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="60221-244">Geçerli biçimin bazı öğeleri için ek bilgiler gösterdiğine dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="60221-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="60221-245">Biçim öğesini kullanarak oluşturulan çıktıya veri girişi için harcanan gerçek süre</span><span class="sxs-lookup"><span data-stu-id="60221-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="60221-246">Aynı zaman, tüm çıktının oluşturulması için harcanan toplam sürenin yüzdesi olarak ifade edilen saat</span><span class="sxs-lookup"><span data-stu-id="60221-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS içinde biçim tasarımcısı sayfası](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="60221-248">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="60221-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="60221-249">RCS- Model eşleme içindeki analiz için performans izlemesini kullan</span><span class="sxs-lookup"><span data-stu-id="60221-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="60221-250">RCS içinde, **Yapılandırmalar** sayfasında, yapılandırma ağacında , **Performans izleme eşleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="60221-251">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="60221-252">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-252">Select **Designer**.</span></span>
4. <span data-ttu-id="60221-253">**Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="60221-254">Daha önce içe aktardığınız izlemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="60221-255">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-255">Select **OK**.</span></span>

<span data-ttu-id="60221-256">Geçerli model eşleştirmesinin bazı veri kaynağı öğeleri için yeni bilgiler kullanılabilir hale geldiğini dikkate alın:</span><span class="sxs-lookup"><span data-stu-id="60221-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="60221-257">Veri kaynağı kullanılarak veri almada harcanan gerçek süre</span><span class="sxs-lookup"><span data-stu-id="60221-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="60221-258">Aynı zaman, tüm model eşleşmesinin yürütülmesi için harcanan toplam sürenin yüzdesi olarak ifade edilen saat</span><span class="sxs-lookup"><span data-stu-id="60221-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="60221-259">ER'ın, geçerli model eşlemesinin, VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağı yürütüldüğünde veritabanı isteklerini yinelediğine dair sizi bilgilendirdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="60221-260">Bu yineleme, satıcı hareketleri listesinin her tekrarlanmış satıcı kaydı için iki kez çağrılıyor olmasından kaynaklanır:</span><span class="sxs-lookup"><span data-stu-id="60221-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="60221-261">Yapılandırılmış bağlamalar temelinde, veri modelindeki her hareketin ayrıntılarını girmek için bir çağrı yapılır.</span><span class="sxs-lookup"><span data-stu-id="60221-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="60221-262">Bir arama, veri modelindeki satıcı başına hesaplanan hareket sayısını girmek için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="60221-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![RCS'de model eşleme tasarımcısı sayfasındaki yinelenen veritabanı istekleri hakkında ileti](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="60221-264">**\[Q:530\]** değeri, VendTrans tablosunun bu tablodan bir kaydı VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağına iade etmek için 530 kez adlandırdığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60221-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="60221-265">**\[530\]** değeri, VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağının bu veri kaynağından bir kayıt döndürmek ve bunu veri modeli içindeki ayrıntıları girmeleri için 530 defa çağrıldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60221-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="60221-266">265 hareketin ayrıntılarını elde etmek için yapılan çağrı sayısını azaltmak ve model eşlemesinin performansını artırmaya yardımcı olmak için VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağı için önbelleğe almayı kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="60221-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="60221-267">LedgerTransTypeList veri kaynağına yapılan çağrıların sayısını azaltmak için de yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="60221-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="60221-268">Bu veri kaynağı, **LedgerTransType** numaralandırmasının her bir değerini etiketiyle ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="60221-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="60221-269">Bu veri kaynağını kullanarak, her bir satıcı hareketi için uygun bir etiket bulabilir ve bunu veri modeline girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="60221-270">Bu veri kaynağına yapılan çağrı sayısı (9.027), 265 hareket için oldukça yüksektir.</span><span class="sxs-lookup"><span data-stu-id="60221-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS'de, veri kaynağına uygulanacak 9.027 çağrıyı gösteren model eşleme tasarımcısı sayfası](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="60221-272">Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirin</span><span class="sxs-lookup"><span data-stu-id="60221-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="60221-273">Model eşlemenin mantığını değiştirin</span><span class="sxs-lookup"><span data-stu-id="60221-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="60221-274">Veritabanına yinelenen aramaların engellenmesine yardımcı olmak amacıyla önbelleğe alma için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="60221-275">RCS'de, **Model eşleme tasarımcısı** sayfasında, **Veri kaynakları** bölmesinde, **VendTable** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="60221-276">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="60221-277">**VendTable** öğesini genişletin, VendTable veri kaynağı için bir-çok ilişkisi listesini genişletin (**\<İlişkiler** öğesi) ve **VendTrans.VendTable\_AccountNum** maddesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="60221-278">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-278">Select **Cache**.</span></span>

    ![Yinelenen çağrıların engellenmesine yardımcı olmak için kurulumu önbelleğe almak](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="60221-280">LedgerTransTypeList veri kaynağını VendTable veri kaynağının kapsamına getirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="60221-281">**Veri kaynağı türleri** bölmesinde, **İşlevler** öğesini genişletin ve **Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="60221-282">**Veri kaynakları** bölmesinde, **VendTable** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="60221-283">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-283">Select **Add**.</span></span>
    4. <span data-ttu-id="60221-284">**Ad** alanına, **\$TransType** girin.</span><span class="sxs-lookup"><span data-stu-id="60221-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="60221-285">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="60221-286">**Formül** alanında, **LedgerTransTypeList** girin.</span><span class="sxs-lookup"><span data-stu-id="60221-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="60221-287">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-287">Select **Save**.</span></span>
    8. <span data-ttu-id="60221-288">**Formül düzenleyici** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="60221-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="60221-289">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60221-289">Click **OK**.</span></span>

3. <span data-ttu-id="60221-290">**\$TransType** alanının önbelleğe alınması için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="60221-291">**LedgerTransTypeList** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="60221-292">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="60221-293">**VendTable.\$TransType** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="60221-294">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-294">Select **Cache**.</span></span>

    ![$TransType alanı için önbelleğe alma kurulumu](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="60221-296">**\$TransTypeRecord** alanını, önbelleğe alınmış **\$TransType** alanını kullanmaya başlayacak şekilde değiştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="60221-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="60221-297">**Veri kaynakları** bölmesinde **VendTable** öğesini genişletin, **\<İlişkiler** öğesini genişletin, **VendTrans.VendTable\_AccountNum** öğesini genişletin ve **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="60221-298">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="60221-299">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="60221-300">**Formül** alanında, aşağıdaki ifadeyi bulun:</span><span class="sxs-lookup"><span data-stu-id="60221-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="60221-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="60221-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="60221-302">**Formül** alanında, aşağıdaki ifadeyi girin:</span><span class="sxs-lookup"><span data-stu-id="60221-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="60221-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="60221-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="60221-304">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-304">Select **Save**.</span></span>
    7. <span data-ttu-id="60221-305">**Formül düzenleyici** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="60221-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="60221-306">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-306">Select **OK**.</span></span>

5. <span data-ttu-id="60221-307">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-307">Select **Save**.</span></span>
6. <span data-ttu-id="60221-308">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="60221-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="60221-309">**Model eşlemeleri** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="60221-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="60221-310">ER model eşlemesinin değiştirilmiş sürümünü tamamlayın</span><span class="sxs-lookup"><span data-stu-id="60221-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="60221-311">RCS'de, **Yapılandırmalar** sayfasında, **Sürümler** hızlı sekmesinde, **Performans izleme eşleme** yapılandırmasının sürüm **1.2**'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="60221-312">**Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-312">Select **Change status**.</span></span>
3. <span data-ttu-id="60221-313">**Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="60221-314">Değiştirilen ER model eşleme yapılandırmasını RCS'den uygulamada içe aktarma</span><span class="sxs-lookup"><span data-stu-id="60221-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="60221-315">**Performans izleme eşleştirme** yapılandırması sürüm 1.2'yi içe aktarmak için bu konuda önceki [Bir ER yapılandırmasını RCS'den Finance and Operations içine aktar](#import-configuration) bölümündeki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="60221-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="60221-316">Çalışmayı izlemek için değiştirilmiş ER çözümünü çalıştırın</span><span class="sxs-lookup"><span data-stu-id="60221-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="60221-317">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="60221-317">Run the ER format</span></span>

<span data-ttu-id="60221-318">Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="60221-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="60221-319">Yürütme izlemesiyle çalışma</span><span class="sxs-lookup"><span data-stu-id="60221-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="60221-320">Oluşturulan izlemeyi uygulamadan dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="60221-320">Export the generated trace from the application</span></span>

<span data-ttu-id="60221-321">Yeni bir performans izlemesini yerel olarak kaydetmek için bu konuda daha önce işlenen [Uygulamadan oluşturulan izlemeyi içe aktar](#export-trace) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="60221-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="60221-322">Oluşturulan izlemeyi RCS'ye içe aktarın</span><span class="sxs-lookup"><span data-stu-id="60221-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="60221-323">Bu konuda daha önce işlenen [Oluşturulan izlemeyi RCS'ye içe aktar](#import-trace) bölümündeki adımları, yeni performans izlemesini RCS'ye içe aktarmak için tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="60221-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="60221-324">RCS- Model eşleme içindeki analiz için performans izlemesini kullan</span><span class="sxs-lookup"><span data-stu-id="60221-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="60221-325">Bu konuda daha önce ele alınan [RCC - Model eşleme içindeki performans izlemeyi analiz için kullan](#use-trace) bölümündeki adımları en son performans izlemeyi analiz etmek için tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="60221-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="60221-326">Model eşleştirmesinde yaptığınız ayarlamaların veritabanındaki yinelenen sorguları elediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="60221-327">Bu model eşleme için veritabanı tablolarına ve veri kaynaklarına yapılan çağrı sayısı da azaltılmıştır.</span><span class="sxs-lookup"><span data-stu-id="60221-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="60221-328">Bu nedenle, tüm ER çözümü performansı iyileştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="60221-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS'de VendTable veri kaynağı için Model eşleme tasarımcısı sayfasında izleme bilgisi](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="60221-330">İzleme bilgisinde, VendTable veri kaynağı için değer **\[12\]**, bu veri kaynağının 12 kere çağrıldığını ifade eder.</span><span class="sxs-lookup"><span data-stu-id="60221-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="60221-331">**\[Q:6\]**, VendTable tablosuna çağrıların altısının veritabanı çağrılarına dönüştürüldüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="60221-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="60221-332">**\[C:6\]** değeri, veritabanından alınan kayıtların önbelleğe alınmış olduğunu ve başka altı çağrının önbellek kullanılarak işlendiğini ifade eder.</span><span class="sxs-lookup"><span data-stu-id="60221-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="60221-333">LedgerTransTypeList veri kaynağına yapılan çağrı sayısının 9.027'den 240'a kadar azaltıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS'de LedgerTransTypeList veri kaynağı için Model eşleme tasarımcısı sayfasında izleme bilgisi](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="60221-335">Uygulamadaki yürütme izlemesini inceleyin</span><span class="sxs-lookup"><span data-stu-id="60221-335">Review the execution trace in the application</span></span>

<span data-ttu-id="60221-336">RCS'ye ek olarak, bazı sürümler bir ER çerçeve tasarımcısı deneyimi için yetenekler sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="60221-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="60221-337">Bu sürümlerde, açılabilir bir **Tasarım modunu etkinleştir** seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="60221-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="60221-338">Bu seçeneği, **Elektronik raporlama** çalışma alanından açabileceğiniz **Elektronik raporlama parametreleri** sayfasının **Genel** sekmesinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Elektronik raporlama parametreleri sayfasında Tasarım modunu etkinleştir seçeneği](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="60221-340">Bu sürümlerden birini kullanıyorsanız, oluşturulan performans izlemelerinin ayrıntılarını uygulamada doğrudan analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="60221-341">Bunları uygulamadan dışa aktarmanız ve RCS'de içe aktarmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="60221-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="60221-342">Yürütme izlemesini harici araçlar kullanarak gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="60221-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="60221-343">Kullanıcı parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="60221-343">Configure user parameters</span></span>

1. <span data-ttu-id="60221-344">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="60221-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="60221-345">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="60221-346">**Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde, **Yürütme izleme biçimi** alanında **PerfView XML** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="60221-347">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="60221-347">Run the ER format</span></span>

<span data-ttu-id="60221-348">Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="60221-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="60221-349">Web tarayıcısının karşıdan yüklenmek üzere bir zip dosyası sunduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="60221-350">Bu dosya, PerfView biçiminde performans izlemesini içerir.</span><span class="sxs-lookup"><span data-stu-id="60221-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="60221-351">Daha sonra, PerfView performans analizi aracını, ER biçimi yürütmesinin ayrıntılarını analiz etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![PerfView biçiminde performans izleme bilgileri](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="60221-353">Veritabanı sorgularını içeren bir yürütme izlemesini gözden geçirmek için harici araçlar kullanın</span><span class="sxs-lookup"><span data-stu-id="60221-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="60221-354">ER çerçevesinde yapılan geliştirmeler sayesinde, PerfView formatında oluşturulan performans izleme, şimdi ER biçimi yürütme hakkında daha ayrıntılı bilgi sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="60221-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="60221-355">Microsoft Dynamics 365 for Finance and Operations 10.0.4 sürümünde (2019 Temmuz) yürütülen bu izleme, SQL sorgularının ayrıntılarını uygulama veritabanına da ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="60221-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="60221-356">Kullanıcı parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="60221-356">Configure user parameters</span></span>

1. <span data-ttu-id="60221-357">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="60221-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="60221-358">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="60221-359">**Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="60221-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="60221-360">**Yürütme izleme biçimi** alanında, **PerfView XML** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60221-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="60221-361">**Sorgu istatistiklerini** topla seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="60221-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="60221-362">**Sorguyu izle** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="60221-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Yürütme izleme bölümü, Kullanıcı parametreleri iletişim kutusu](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="60221-364">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="60221-364">Run the ER format</span></span>

<span data-ttu-id="60221-365">Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="60221-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="60221-366">Web tarayıcısının karşıdan yüklenmek üzere bir zip dosyası sunduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="60221-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="60221-367">Bu dosya, PerfView biçiminde performans izlemesini içerir.</span><span class="sxs-lookup"><span data-stu-id="60221-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="60221-368">Daha sonra, PerfView performans analizi aracını, ER biçimi yürütmesinin ayrıntılarını analiz etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60221-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="60221-369">Bu izleme şimdi, ER biçiminin yürütülmesi sırasında SQL veritabanı erişimi ayrıntılarını içermektedir.</span><span class="sxs-lookup"><span data-stu-id="60221-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![PerfView'da yürütülen ER formatı için izleme bilgileri](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="60221-371">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="60221-371">Additional resources</span></span>

- [<span data-ttu-id="60221-372">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="60221-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="60221-373">Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme</span><span class="sxs-lookup"><span data-stu-id="60221-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
