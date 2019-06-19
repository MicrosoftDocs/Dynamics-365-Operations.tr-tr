---
title: Performans sorunlarını gidermek için ER biçimi yürütülmesini izle
description: Bu konu, performans sorunlarını gidermek amacıyla elektronik raporlama (ER) içindeki performans izleme özelliğinin nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576558"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="5fbec-103">Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izle</span><span class="sxs-lookup"><span data-stu-id="5fbec-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5fbec-104">Elektronik raporlama (ER) konfigürasyonlarının elektronik belgeler oluşturmak amacıyla tasarlanması işleminin bir parçası olarak, Microsoft Dynamics 365 for Finance and Operations içerisinden veri elde etmek ve oluşturulan çıktıya girmek için kullanılan yöntemi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="5fbec-105">ER performans izleme özelliği, ER biçim yürütmesi ve performans sorunlarını gidermek için onları kullanma ile ilgili zamanı ve maliyeti önemli ölçüde azaltmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="5fbec-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="5fbec-106">Bu kılavuz, Finance and Operations içinde yürütülmüş ER biçimleri için performans izlemelerinin nasıl alınacağı ve performansın artırılmasına yardımcı olmak amacıyla bu izlemelerin nasıl kullanılacağı hakkında yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="5fbec-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5fbec-107">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="5fbec-107">Prerequisites</span></span>

<span data-ttu-id="5fbec-108">Bu kılavuzdaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5fbec-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="5fbec-109">Aşağıdaki rollerden biri için Finance and Operations'a erişim:</span><span class="sxs-lookup"><span data-stu-id="5fbec-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="5fbec-110">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="5fbec-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="5fbec-111">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="5fbec-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5fbec-112">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="5fbec-112">System administrator</span></span>

- <span data-ttu-id="5fbec-113">Aşağıdaki rollerden biri için, Finance and Operations olarak aynı kiracı için sağlanan Regulatory Configuration Services (RCS) örneğine erişim:</span><span class="sxs-lookup"><span data-stu-id="5fbec-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="5fbec-114">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="5fbec-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="5fbec-115">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="5fbec-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5fbec-116">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="5fbec-116">System administrator</span></span>

<span data-ttu-id="5fbec-117">Ayrıca, aşağıdaki dosyaları da indirip yerel olarak depolamalısınız.</span><span class="sxs-lookup"><span data-stu-id="5fbec-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="5fbec-118">Dosya</span><span class="sxs-lookup"><span data-stu-id="5fbec-118">File</span></span>                                  | <span data-ttu-id="5fbec-119">İçerik</span><span class="sxs-lookup"><span data-stu-id="5fbec-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="5fbec-120">Performans izleme modeli sürüm 1</span><span class="sxs-lookup"><span data-stu-id="5fbec-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="5fbec-121">Örnek ER verisi modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5fbec-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="5fbec-122">Performans izleme meta veri sürüm 1</span><span class="sxs-lookup"><span data-stu-id="5fbec-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="5fbec-123">Örnek ER meta verisi yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5fbec-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="5fbec-124">Performans izleme eşleştirme sürümü 1.1</span><span class="sxs-lookup"><span data-stu-id="5fbec-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="5fbec-125">Örnek ER model eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5fbec-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="5fbec-126">Performans izleme biçimi sürümü 1.1</span><span class="sxs-lookup"><span data-stu-id="5fbec-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="5fbec-127">Örnek ER biçim yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5fbec-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="5fbec-128">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5fbec-128">Configure ER parameters</span></span>

<span data-ttu-id="5fbec-129">Finance and Operations içinde oluşturulan her bir ER performans izleme, yürütme günlükleri kaydının bir eki olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="5fbec-130">Finance and Operations Belge yönetimi (DM) çerçevesi, bu ekleri yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="5fbec-131">Performans izlemelerini iliştirmek için kullanılması gereken DM belge türünü belirtmek için ER parametrelerini önceden yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5fbec-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="5fbec-132">Finance and Operations içinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="5fbec-133">Sonra, **Elektronik raporlama parametreleri** sayfasında, **Ekler** sekmesinde, **Diğerleri** alanında, performans izlemeleri için kullanılacak DM belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Finance and Operations içindeki elektronik raporlama parametreleri sayfası](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="5fbec-135">**Diğer** arama alanında kullanılabilmesi için bir DM belgesi türünün aşağıdaki şekilde **Belge türleri** sayfasında yapılandırılması gerekir (**Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**):</span><span class="sxs-lookup"><span data-stu-id="5fbec-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="5fbec-136">**Sınıf:** Dosya iliştir</span><span class="sxs-lookup"><span data-stu-id="5fbec-136">**Class:** Attach file</span></span>
- <span data-ttu-id="5fbec-137">**Grup:** Dosya</span><span class="sxs-lookup"><span data-stu-id="5fbec-137">**Group:** File</span></span>

![Finance and Operations içindeki belge türleri sayfası](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="5fbec-139">DM ekleri şirkete özgü olduğundan, seçilen belge türü geçerli Finance and Operations örneğinin tüm şirketlerinde kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="5fbec-140">RCS parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5fbec-140">Configure RCS parameters</span></span>

<span data-ttu-id="5fbec-141">Finance and Operations içinde oluşturulan performans izlemeleri, ER biçim Tasarımcısı ve ER eşleme Tasarımcısı kullanılarak analiz için RCS'ye aktarılır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="5fbec-142">ER performans izleri ER biçimiyle ilgili yürütme günlükleri kaydının ekleri olarak depolandığından, RCS parametrelerini önceden yapılandırmalısınız, böylece performans izlemelerini iliştirmek için kullanılacak DM belge türü belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="5fbec-143">Şirketiniz için sağlanmış olan RCS örneğinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="5fbec-144">Sonra, **Elektronik raporlama parametreleri** sayfasında, **Ekler** sekmesinde, **Diğerleri** alanında, performans izlemeleri için kullanılacak DM belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS içindeki Elektronik raporlama parametreleri sayfası](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="5fbec-146">**Diğer** arama alanında kullanılabilmesi için bir DM belgesi türünün aşağıdaki şekilde **Belge türleri** sayfasında yapılandırılması gerekir (**Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**):</span><span class="sxs-lookup"><span data-stu-id="5fbec-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="5fbec-147">**Sınıf:** Dosya iliştir</span><span class="sxs-lookup"><span data-stu-id="5fbec-147">**Class:** Attach file</span></span>
- <span data-ttu-id="5fbec-148">**Grup:** Dosya</span><span class="sxs-lookup"><span data-stu-id="5fbec-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="5fbec-149">Bir ER çözümü tasarla</span><span class="sxs-lookup"><span data-stu-id="5fbec-149">Design an ER solution</span></span>

<span data-ttu-id="5fbec-150">Satıcı hareketleri sunan yeni bir rapor oluşturmak üzere yeni bir ER çözümü tasarladığınızı varsayın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="5fbec-151">Şu anda, seçilen satıcı için hareketleri **Satıcı hareketleri** sayfasında bulabilirsiniz (**Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin, bir satıcı seçin ve Eylem Panosu üzerinde, **Satıcı** sekmesinde, **Hareketler** grubunda, **Hareketler**'i seçin).</span><span class="sxs-lookup"><span data-stu-id="5fbec-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="5fbec-152">Ancak, tüm satıcı hareketinin elektronik bir belgede XML biçiminde aynı anda olmasını istersiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="5fbec-153">Bu çözüm, gerekli veri modelini, meta verileri, model eşlemeyi ve biçim bileşenlerini içeren birkaç ER yapılandırmasından oluşur.</span><span class="sxs-lookup"><span data-stu-id="5fbec-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="5fbec-154">Şirketiniz için sağlanan RCS örneğine oturum açın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="5fbec-155">Bu kılavuzda, **Litware, Inc.** örnek şirket için yapılandırmalar oluşturacak ve değiştireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="5fbec-156">Bu nedenle, bu konfigürasyon sağlayıcısının RCS'ye eklenmiş olduğundan ve etkin olarak seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="5fbec-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="5fbec-157">Yönergeler için, bkz. [Yapılandırma sağlayıcıları oluşturmak ve bunları etkin olarak işaretlemek yordamına](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) bakın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="5fbec-158">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="5fbec-159">**Yapılandırmalar** sayfasında, önkoşul olarak karşıdan yüklediğiniz ER yapılandırmalarını aşağıdaki sırada içe aktarın: veri modeli, meta veriler, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="5fbec-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="5fbec-160">Her bir yapılandırma için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="5fbec-161">Eylem Panosunda, **Exchange \> XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="5fbec-162">Gerekli ER yapılandırması için XML biçiminde uygun dosyayı seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="5fbec-163">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-163">Select **OK**.</span></span>

    ![RCS içinde Yapılandırmalar sayfası](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="5fbec-165">Çalışmayı izlemek için ER çözümünü çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5fbec-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="5fbec-166">ER çözümünün ilk sürümünü tasarlamayı bitirdiğinizi varsayalım.</span><span class="sxs-lookup"><span data-stu-id="5fbec-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="5fbec-167">Şimdi bunu Finance and Operations örneğiniz içinde test etmek ve yürütme performansını analiz etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="5fbec-168">Bir ER yapılandırmasını RCS'ten Finance and Operations'a içe aktarın</span><span class="sxs-lookup"><span data-stu-id="5fbec-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="5fbec-169">Finance ve Operations kurulumunuzda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="5fbec-170">Bu kılavuzda, yapılandırmaları RCS örneğinizden (ER bileşenlerinizi tasarladığınız yerden) Finance and Operations örneğinize (test edeceğiniz ve son olarak kullanacağınız) içe aktarırsınız.</span><span class="sxs-lookup"><span data-stu-id="5fbec-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="5fbec-171">Bu nedenle, gerekli tüm yapıların hazırlandığından emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5fbec-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="5fbec-172">Talimatlar için bkz. [Düzenleyici Yapılandırma Hizmeti'nden (RCS) Elektronik raporlama (ER) yapılandırmalarını içe aktarma](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) yordamı.</span><span class="sxs-lookup"><span data-stu-id="5fbec-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="5fbec-173">Yapılandırmaları RCS'den Finance and Operations'a içe aktarmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="5fbec-174">**Elektronik raporlama** çalışma alanında, **Litware, Inc.** yapılandırma sağlayıcısının döşemesi üzerinde **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="5fbec-175">**Yapılandırma deposu** sayfasında, **RCS** türünün deposunu seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="5fbec-176">**Yapılandırmalar** hızlı sekmesinde, **Performans izleme biçimi** yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="5fbec-177">**Sürümler** hızlı sekmesinde seçilen yapılandırmanın sürüm **1.1**'ini ve sonra **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Finance and Operations içinde yapılandırma deposu sayfası](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="5fbec-179">Veri modeli ve model eşleme yapılandırmalarının ilgili sürümleri, içe aktarılan ER biçim konfigürasyonu için önkoşul olarak otomatik içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="5fbec-180">ER performans izlemesini aç</span><span class="sxs-lookup"><span data-stu-id="5fbec-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="5fbec-181">Finance and Operations içinde, **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="5fbec-182">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5fbec-183">**Kullanıcı parametreleri**iletişim kutusunda, **Yürütme izleme** bölümünde şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="5fbec-184">**Yürütme izleme biçimi** alanında, ER biçimi yürütme ayrıntılarını toplamaya başlamak için **İzleme biçimi sorun giderme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="5fbec-185">Bu değer seçildiğinde, performans izlemesi aşağıdaki eylemlerde harcanan süre hakkında bilgi toplar:</span><span class="sxs-lookup"><span data-stu-id="5fbec-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="5fbec-186">Her bir veri kaynağını veri almak için çağırılan model eşlemesinde çalıştırma</span><span class="sxs-lookup"><span data-stu-id="5fbec-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="5fbec-187">Oluşturulan çıktıya veri girmek için her biçim öğesini işlemek</span><span class="sxs-lookup"><span data-stu-id="5fbec-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="5fbec-188">**Yürütme izleme biçimi** alanını, yürütme ayrıntılarının ER biçimi ve eşleme öğeleri için depolandığı oluşturulan performans izlemesinin biçimini belirtmek için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="5fbec-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="5fbec-189">**İzleme biçimi hata ayıklama**'yı değer olarak seçerek, ER Operasyon tasarımcısı içindeki içeriği analiz edebilir ve izlemede bahsedilen ER biçimi veya eşleştirme öğelerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="5fbec-190">ER model eşleme ve ER biçimde bileşenlerinin yürütülmesine dair belirli ayrıntıları toplamak için aşağıdaki seçenekleri **Evet** olarak ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="5fbec-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="5fbec-191">**Sorgu istatistiklerini topla** – Bu seçenek etkinleştirildiğinde, performans izlemesi aşağıdaki bilgileri toplar:</span><span class="sxs-lookup"><span data-stu-id="5fbec-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="5fbec-192">Veri kaynakları tarafından yapılan veritabanı çağrılarının sayısı</span><span class="sxs-lookup"><span data-stu-id="5fbec-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="5fbec-193">Veritabanına yapılan yinelenen çağrıların sayısı</span><span class="sxs-lookup"><span data-stu-id="5fbec-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="5fbec-194">Veritabanı çağrılarını yapmak için kullanılan SQL deyimlerinin ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="5fbec-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="5fbec-195">**Önbelleğe alma erişimini izleme** – Bu seçenek açıldığında, performans izlemesi ER modeli eşlemesinin önbellek kullanımıyla ilgili bilgilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="5fbec-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="5fbec-196">**Veri erişimini izle** – Bu seçenek etkinleştirildiğinde, performans izlemesi kayıt listesi türünün yürütülmüş veri kaynakları için veritabanına yapılan çağrı sayısıyla ilgili bilgi toplar.</span><span class="sxs-lookup"><span data-stu-id="5fbec-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="5fbec-197">**Liste numaralandırmasını izle** – Bu seçenek etkinleştirildiğinde, performans izlemesi kayıt listesi türünün veri kaynakları için talep edilen kayıtların sayısı hakkında bilgi toplar.</span><span class="sxs-lookup"><span data-stu-id="5fbec-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5fbec-198">**Kullanıcı parametreleri** iletişim kutusundaki parametreler kullanıcıya ve geçerli şirkete özgüdür.</span><span class="sxs-lookup"><span data-stu-id="5fbec-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Finance and Operations içinde kullanıcı parametreleri iletişim kutusu](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="5fbec-200">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="5fbec-200">Run the ER format</span></span>

1. <span data-ttu-id="5fbec-201">Finance and Operations içinde, **DEMF** şirketini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="5fbec-202">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="5fbec-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="5fbec-203">**Yapılandırmalar** sayfasında, yapılandırma ağacında , **Performans izleme biçimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="5fbec-204">Eylem Bölmesinde, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="5fbec-205">Oluşturulan dosyanın altı satıcıda bulunan 265 hareketleri temsil ettiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="5fbec-206">Yürütme izlemesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="5fbec-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="5fbec-207">Oluşturulan izlemeyi Finance and Operations'tan dışa aktarın</span><span class="sxs-lookup"><span data-stu-id="5fbec-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="5fbec-208">Performans izlemeleri, kaynak ER biçiminden alınır ve harici bir ZIP dosyasına serileştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="5fbec-209">Finance and Operations içinde, **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırma hata ayıklama günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="5fbec-210">**Elektronik raporlama yürütme günlükleri** sayfasında, sol tarafta, **Yapılandırma adı** alanında, **Performans izleme biçimi**'ni seçerek, **Performans izleme biçimi** yapılandırması yürütülmesi tarafından oluşturulan günlük kayıtlarını bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="5fbec-211">Sayfanın sağ üst köşesindeki **Ekler** düğmesini (ataş simgesi) seçin veya **Ctrl+Shift+A**'ya basın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Finance and Operations içinde Elektronik raporlama yürütme günlükleri sayfasındaki ilgili ekler düğmesi](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="5fbec-213">**Elektronik raporlama yürütme günlükleri için ekler** sayfasında, Eylem Panosunda, **Aç**'ı seçerek performans izlemeyi bir zip dosyası olarak elde edin ve yerel olarak depolayın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Finance and Operations içinde Elektronik raporlama yürütme günlükleri sayfası için ekler](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="5fbec-215">Oluşturulan izleme, yalnızca **GUID** biçimindeki benzersiz bir rapor tanımlayıcısı aracılığıyla kaynak ER raporuna referans sağlar.</span><span class="sxs-lookup"><span data-stu-id="5fbec-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="5fbec-216">Biçimin sürüm numaralandırması dikkate alınmıyor.</span><span class="sxs-lookup"><span data-stu-id="5fbec-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="5fbec-217">Çalıştırılan ve ER model eşleme için oluşturulan performans izleme arasındaki ilişkinin, kullanılan kök tanımlayıcısını ve ortak veri modelini temel aldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="5fbec-218">Biçim ve model eşleşmesinin sürüm numaralandırması dikkate alınmıyor.</span><span class="sxs-lookup"><span data-stu-id="5fbec-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="5fbec-219">**Model eşleme için varsayılan** bayrağı ayarı da dikkate alınmıyor.</span><span class="sxs-lookup"><span data-stu-id="5fbec-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="5fbec-220">Oluşturulan izlemeyi RCS'ye içe aktarın</span><span class="sxs-lookup"><span data-stu-id="5fbec-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="5fbec-221">RCS içinde, **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="5fbec-222">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans izleme modeli** öğesini genişletin ve **Performans izleme biçimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="5fbec-223">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="5fbec-224">**Biçim tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="5fbec-225">**Performans izleme sonucu ayarları** iletişim kutusunda, **Performans izleme içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="5fbec-226">Finance and Operations'tan daha önce dışa aktarılan zip dosyasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="5fbec-227">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-227">Select **OK**.</span></span>

    ![RCS içindeki performans izleme sonuç ayarları iletişim kutusu](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="5fbec-229">RCS- Biçim yürütme içindeki analiz için performans izlemesini kullan</span><span class="sxs-lookup"><span data-stu-id="5fbec-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="5fbec-230">RCS içinde, **Biçim tasarımcısı** sayfasında, **Genişlet/daralt**'ı seçerek tüm biçim öğelerinin içeriğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="5fbec-231">Geçerli biçimin bazı öğeleri için ek bilgiler gösterdiğine dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="5fbec-232">Biçim öğesini kullanarak oluşturulan çıktıya veri girişi için harcanan gerçek süre</span><span class="sxs-lookup"><span data-stu-id="5fbec-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="5fbec-233">Aynı zaman, tüm çıktının oluşturulması için harcanan toplam sürenin yüzdesi olarak ifade edilen saat</span><span class="sxs-lookup"><span data-stu-id="5fbec-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS içinde biçim tasarımcısı sayfası](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="5fbec-235">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="5fbec-236">RCS- Model eşleme içindeki analiz için performans izlemesini kullan</span><span class="sxs-lookup"><span data-stu-id="5fbec-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="5fbec-237">RCS içinde, **Yapılandırmalar** sayfasında, yapılandırma ağacında , **Performans izleme eşleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="5fbec-238">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="5fbec-239">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-239">Select **Designer**.</span></span>
4. <span data-ttu-id="5fbec-240">**Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="5fbec-241">Daha önce içe aktardığınız izlemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="5fbec-242">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-242">Select **OK**.</span></span>

<span data-ttu-id="5fbec-243">Geçerli model eşleştirmesinin bazı veri kaynağı öğeleri için yeni bilgiler kullanılabilir hale geldiğini dikkate alın:</span><span class="sxs-lookup"><span data-stu-id="5fbec-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="5fbec-244">Veri kaynağı kullanılarak veri almada harcanan gerçek süre</span><span class="sxs-lookup"><span data-stu-id="5fbec-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="5fbec-245">Aynı zaman, tüm model eşleşmesinin yürütülmesi için harcanan toplam sürenin yüzdesi olarak ifade edilen saat</span><span class="sxs-lookup"><span data-stu-id="5fbec-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="5fbec-246">ER'ın, geçerli model eşlemesinin, VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağı yürütüldüğünde veritabanı isteklerini yinelediğine dair sizi bilgilendirdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="5fbec-247">Bu yineleme, satıcı hareketleri listesinin her tekrarlanmış satıcı kaydı için iki kez çağrılıyor olmasından kaynaklanır:</span><span class="sxs-lookup"><span data-stu-id="5fbec-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="5fbec-248">Yapılandırılmış bağlamalar temelinde, veri modelindeki her hareketin ayrıntılarını girmek için bir çağrı yapılır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="5fbec-249">Bir arama, veri modelindeki satıcı başına hesaplanan hareket sayısını girmek için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![RCS'de model eşleme tasarımcısı sayfasındaki yinelenen veritabanı istekleri hakkında ileti](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="5fbec-251">**\[Q:530\]** değeri, VendTrans tablosunun bu tablodan bir kaydı VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağına iade etmek için 530 kez adlandırdığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="5fbec-252">**\[530\]** değeri, VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağının bu veri kaynağından bir kayıt döndürmek ve bunu veri modeli içindeki ayrıntıları girmeleri için 530 defa çağrıldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="5fbec-253">265 hareketin ayrıntılarını elde etmek için yapılan çağrı sayısını azaltmak ve model eşlemesinin performansını artırmaya yardımcı olmak için VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağı için önbelleğe almayı kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="5fbec-254">LedgerTransTypeList veri kaynağına yapılan çağrıların sayısını azaltmak için de yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="5fbec-255">Bu veri kaynağı, **LedgerTransType** numaralandırmasının her bir değerini etiketiyle ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="5fbec-256">Bu veri kaynağını kullanarak, her bir satıcı hareketi için uygun bir etiket bulabilir ve bunu veri modeline girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="5fbec-257">Bu veri kaynağına yapılan çağrı sayısı (9.027), 265 hareket için oldukça yüksektir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS'de, veri kaynağına uygulanacak 9.027 çağrıyı gösteren model eşleme tasarımcısı sayfası](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="5fbec-259">Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirin</span><span class="sxs-lookup"><span data-stu-id="5fbec-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="5fbec-260">Model eşlemenin mantığını değiştirin</span><span class="sxs-lookup"><span data-stu-id="5fbec-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="5fbec-261">Veritabanına yinelenen aramaların engellenmesine yardımcı olmak amacıyla önbelleğe alma için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="5fbec-262">RCS'de, **Model eşleme tasarımcısı** sayfasında, **Veri kaynakları** bölmesinde, **VendTable** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="5fbec-263">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="5fbec-264">**VendTable** öğesini genişletin, VendTable veri kaynağı için bir-çok ilişkisi listesini genişletin (**\<İlişkiler** öğesi) ve **VendTrans.VendTable\_AccountNum** maddesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="5fbec-265">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-265">Select **Cache**.</span></span>

    ![Yinelenen çağrıların engellenmesine yardımcı olmak için kurulumu önbelleğe almak](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="5fbec-267">LedgerTransTypeList veri kaynağını VendTable veri kaynağının kapsamına getirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="5fbec-268">**Veri kaynağı türleri** bölmesinde, **İşlevler** öğesini genişletin ve **Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="5fbec-269">**Veri kaynakları** bölmesinde, **VendTable** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="5fbec-270">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-270">Select **Add**.</span></span>
    4. <span data-ttu-id="5fbec-271">**Ad** alanına, **\$TransType** girin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="5fbec-272">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="5fbec-273">**Formül** alanında, **LedgerTransTypeList** girin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="5fbec-274">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-274">Select **Save**.</span></span>
    8. <span data-ttu-id="5fbec-275">**Formül düzenleyici** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="5fbec-276">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-276">Click **OK**.</span></span>

3. <span data-ttu-id="5fbec-277">**\$TransType** alanının önbelleğe alınması için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="5fbec-278">**LedgerTransTypeList** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="5fbec-279">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="5fbec-280">**VendTable.\$TransType** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="5fbec-281">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-281">Select **Cache**.</span></span>

    ![$TransType alanı için önbelleğe alma kurulumu](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="5fbec-283">**\$TransTypeRecord** alanını, önbelleğe alınmış **\$TransType** alanını kullanmaya başlayacak şekilde değiştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="5fbec-284">**Veri kaynakları** bölmesinde **VendTable** öğesini genişletin, **\<İlişkiler** öğesini genişletin, **VendTrans.VendTable\_AccountNum** öğesini genişletin ve **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="5fbec-285">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="5fbec-286">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="5fbec-287">**Formül** alanında, aşağıdaki ifadeyi bulun:</span><span class="sxs-lookup"><span data-stu-id="5fbec-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="5fbec-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="5fbec-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="5fbec-289">**Formül** alanında, aşağıdaki ifadeyi girin:</span><span class="sxs-lookup"><span data-stu-id="5fbec-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="5fbec-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="5fbec-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="5fbec-291">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-291">Select **Save**.</span></span>
    7. <span data-ttu-id="5fbec-292">**Formül düzenleyici** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5fbec-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="5fbec-293">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-293">Select **OK**.</span></span>

5. <span data-ttu-id="5fbec-294">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-294">Select **Save**.</span></span>
6. <span data-ttu-id="5fbec-295">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="5fbec-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="5fbec-296">**Model eşlemeleri** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="5fbec-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="5fbec-297">ER model eşlemesinin değiştirilmiş sürümünü tamamlayın</span><span class="sxs-lookup"><span data-stu-id="5fbec-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="5fbec-298">RCS'de, **Yapılandırmalar** sayfasında, **Sürümler** hızlı sekmesinde, **Performans izleme eşleme** yapılandırmasının sürüm **1.2**'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="5fbec-299">**Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-299">Select **Change status**.</span></span>
3. <span data-ttu-id="5fbec-300">**Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="5fbec-301">Değiştirilen ER model eşleme yapılandırmasını RCS'den Finance and Operations'a içe aktar</span><span class="sxs-lookup"><span data-stu-id="5fbec-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="5fbec-302">**Performans izleme eşleşeme** yapılandırması sürüm 1.2'yi Finance and Operations'a içe aktarmak için [Bir ER yapılandırmasını RCS'den Finance and Operations içine aktar](#import-configuration) bölümü içindeki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="5fbec-303">Çalışmayı izlemek için değiştirilmiş ER çözümünü çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5fbec-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="5fbec-304">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="5fbec-304">Run the ER format</span></span>

<span data-ttu-id="5fbec-305">Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="5fbec-306">Yürütme izlemesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="5fbec-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="5fbec-307">Oluşturulan izlemeyi Finance and Operations'tan dışa aktarın</span><span class="sxs-lookup"><span data-stu-id="5fbec-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="5fbec-308">Yeni bir performans izlemesini yerel olarak kaydetmek için bu konuda daha önce işlenen [Finance and Operations'tan oluşturulan izlemeyi içe aktar](#export-trace) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="5fbec-309">Oluşturulan izlemeyi RCS'ye içe aktarın</span><span class="sxs-lookup"><span data-stu-id="5fbec-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="5fbec-310">Bu konuda daha önce işlenen [Oluşturulan izlemeyi RCS'ye içe aktar](#import-trace) bölümündeki adımları, yeni performans izlemesini RCS'ye içe aktarmak için tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="5fbec-311">RCS- Model eşleme içindeki analiz için performans izlemesini kullan</span><span class="sxs-lookup"><span data-stu-id="5fbec-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="5fbec-312">Bu konuda daha önce ele alınan [RCC - Model eşleme içindeki performans izlemeyi analiz için kullan](#use-trace) bölümündeki adımları en son performans izlemeyi analiz etmek için tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="5fbec-313">Model eşleştirmesinde yaptığınız ayarlamaların veritabanındaki yinelenen sorguları elediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="5fbec-314">Bu model eşleme için veritabanı tablolarına ve veri kaynaklarına yapılan çağrı sayısı da azaltılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5fbec-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="5fbec-315">Bu nedenle, tüm ER çözümü performansı iyileştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS'de VendTable veri kaynağı için Model eşleme tasarımcısı sayfasında izleme bilgisi](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="5fbec-317">İzleme bilgisinde, VendTable veri kaynağı için değer **\[12\]**, bu veri kaynağının 12 kere çağrıldığını ifade eder.</span><span class="sxs-lookup"><span data-stu-id="5fbec-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="5fbec-318">**\[Q:6\]**, VendTable tablosuna çağrıların altısının veritabanı çağrılarına dönüştürüldüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="5fbec-319">**\[C:6\]** değeri, veritabanından alınan kayıtların önbelleğe alınmış olduğunu ve başka altı çağrının önbellek kullanılarak işlendiğini ifade eder.</span><span class="sxs-lookup"><span data-stu-id="5fbec-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="5fbec-320">LedgerTransTypeList veri kaynağına yapılan çağrı sayısının 9.027'den 240'a kadar azaltıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS'de LedgerTransTypeList veri kaynağı için Model eşleme tasarımcısı sayfasında izleme bilgisi](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="5fbec-322">Finance and Operations içindeki yürütme izlemesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="5fbec-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="5fbec-323">RCS'ye ek olarak, Finance and Operations'ın bazı sürümleri bir ER çerçeve tasarımcısı deneyimi için yetenekler sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="5fbec-324">Finance and Operations'un bu sürümleri, açılabilir bir **Tasarım modunu etkinleştir** seçeneğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="5fbec-325">Bu seçeneği, **Elektronik raporlama** çalışma alanından açabileceğiniz **Elektronik raporlama parametreleri** sayfasının **Genel** sekmesinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Finance and Operations ile ilgili Elektronik raporlama parametreleri sayfasında tasarım moduna izin ver seçeneğini etkinleştirin](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="5fbec-327">Finance and Operations'un bu sürümlerinden birini kullanıyorsanız, oluşturulan performans izlemelerinin ayrıntılarını doğrudan Finance and Operations içerisinde analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="5fbec-328">Bunları Finance and Operations'tan dışa aktarmanız ve bunları RCS'ye almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="5fbec-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="5fbec-329">Yürütme izlemesini harici araçlar kullanarak gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="5fbec-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="5fbec-330">Kullanıcı parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5fbec-330">Configure user parameters</span></span>

1. <span data-ttu-id="5fbec-331">Finance and Operations içinde, **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="5fbec-332">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5fbec-333">**Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde, **Yürütme izleme biçimi** alanında **PerfView XML** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="5fbec-334">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="5fbec-334">Run the ER format</span></span>

<span data-ttu-id="5fbec-335">Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="5fbec-336">Web tarayıcısının karşıdan yüklenmek üzere bir zip dosyası sunduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5fbec-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="5fbec-337">Bu dosya, PerfView biçiminde performans izlemesini içerir.</span><span class="sxs-lookup"><span data-stu-id="5fbec-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="5fbec-338">Daha sonra, PerfView performans analizi aracını, ER biçimi yürütmesinin ayrıntılarını analiz etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbec-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>
