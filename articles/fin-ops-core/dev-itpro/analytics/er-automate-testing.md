---
title: Elektronik raporlama ile testi otomatikleştirme
description: Bu konu, işlevsellik testini otomatikleştirmek için Elektronik raporlama (ER) çerçevesinin temel özelliğini nasıl kullanabileceğinizi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 503d4ca562df5c60ee7c475ac146dffbe0edc0c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569057"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="7b3bb-103">Elektronik raporlama ile testi otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="7b3bb-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b3bb-104">Bu konu, işlevsellik testini otomatikleştirmek için Elektronik raporlama (ER) çerçevesini nasıl kullanabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="7b3bb-105">Bu konudaki örnekte, satıcı ödeme işlemi testinin nasıl otomatikleştirildiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="7b3bb-106">Uygulama, satıcı ödeme işlemi sırasında ödeme dosyaları ve ilgili belgeler oluşturmak için ER çerçevesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="7b3bb-107">ER çerçevesi, farklı ödeme tipleri ve farklı biçimlerdeki belgelerin oluşturulması için ödeme işlemeyi destekleyen bir veri modeli, model eşleme ve biçim bileşenlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="7b3bb-108">Bu bileşenler Microsoft Dynamics Lifecycle Services (LCS)'den yüklenebilir ve örneğe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="7b3bb-109">Ayrıca, her bir Microsoft bileşenini özelleştirebilir ve kendi özel bileşeninizin temeli olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="7b3bb-110">Özel bir sürüm oluşturarak, belirli gereksinimleri destekleyen değişiklikler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="7b3bb-111">Örneğin, müşteriye özel uygulama verilerine erişmek için ER veri modelini ve ER model eşleştirmesini ayarlayabilirsiniz veya bir ER. oluşturulan bir belgenin düzenini değiştirmek için bir ER biçimini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="7b3bb-112">Satıcı ödemeleri oluşturan ve ayrıca kontrol raporlarını işleyen ödeme dosyalarını işlemek için örneğinizdeki özelleştirilmiş ER biçimlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="7b3bb-113">Sürüm Oluşturma ER bileşenlerinde desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="7b3bb-114">Bu nedenle, Microsoft, satıcı ödeme işlemesi için ER çözümlerinin güncelleştirilmiş sürümlerini sağlayabilir ve güncelleştirilmiş sürümü otomatik olarak yeniden temelleyerek özelleştirilmiş bileşeniniz ile birleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="7b3bb-115">Ancak, beklediğiniz gibi çalıştığından emin olmak için yeniden temel sürümü test etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="7b3bb-116">ER veri modelleri ve ER model eşleştirmeleri, farklı türlerdeki ödemeleri işlemek ve ülkeye/bölgeye özel ödeme belgeleri oluşturmak için kullanılan birçok ER biçiminde ortaktır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="7b3bb-117">Bu nedenle, birden çok şirket için otomatik olarak gerçekleştirilmesi için kullanıcı kabulü ve tümleştirme testini otomatikleştirmek istenir, ancak her bir hedef şirketin ülke/bölge bağlamını dikkate alır, farklı veri kümeleri kullanır, vb. .</span><span class="sxs-lookup"><span data-stu-id="7b3bb-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="7b3bb-118">Bir yapılandırma sağlayıcısından aldığınız biçime göre bir biçimin özel sürümünün nasıl oluşturulduğu hakkında daha fazla bilgi için [ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.](./tasks/er-upgrade-format.md)'e bakın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="7b3bb-119">Kilit kavramlar</span><span class="sxs-lookup"><span data-stu-id="7b3bb-119">Key concepts</span></span>

<span data-ttu-id="7b3bb-120">İşlevsel yetkili kullanıcılar, kaynak kodu yazmak zorunda kalmadan kullanıcı kabul ve tümleştirme testini yazabilir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="7b3bb-121">Oluşturulan belgeleri ana kopyalara karşılaştırmak için ER temel özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="7b3bb-122">Daha fazla bilgi için [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md)'ya bakın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="7b3bb-123">Test olaylarını kaydetmek ve temel değerlendirmeyi dahil etmek için görev kaydediciyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="7b3bb-124">Daha fazla bilgi için bkz. [Görev kaydedici kaynakları](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="7b3bb-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="7b3bb-125">Gerekli test senaryoları için grup test durumları.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="7b3bb-126">Daha fazla bilgi için bkz. [Kullanıcı kabul testleri oluşturma ve otomatikleştirme](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="7b3bb-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="7b3bb-127">Kullanıcı kabul testleri için kitaplıklar oluşturmak amacıyla LCS'de İş süreci Modelleyicisi'ni (BPM) kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="7b3bb-128">Microsoft Azure DevOps Services (Azure DevOps) içinde bir test planı ve test paketleri oluşturmak için BPM test kitaplıklarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="7b3bb-129">İşlevsel yetkili kullanıcılar kullanıcı kabul ve bütünleştirme testlerini çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="7b3bb-130">İstenen test paketinin test çalışmalarını çalıştırmak için Regression Suite Automation Tool (RSAT)'u kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="7b3bb-131">Testin sonuçlarını Azure DevOps'a rapor edin ve bu sonuçları araştırmak için bu hizmeti kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7b3bb-132">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7b3bb-132">Prerequisites</span></span>

<span data-ttu-id="7b3bb-133">Bu konudaki görevleri tamamlayabilmek için önce aşağıdaki ön koşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="7b3bb-134">Test otomasyonunu destekleyen bir topoloji dağıtın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="7b3bb-135">**Sistem Yöneticisi** rolü Için bu topolojinin örneğine erişiminizin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="7b3bb-136">Bu topoloji, bu örnekte kullanılacak demo verilerini içermelidir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="7b3bb-137">Daha fazla bilgi için bkz. [Sürekli oluşturma ve test otomasyonunu destekleyen bir ortam dağıtma ve kullanma](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="7b3bb-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="7b3bb-138">Kullanıcı kabul ve tümleştirme testlerini otomatik olarak çalıştırmak için RSAT'ı kullandığınız topolojiye yüklemeli ve uygun şekilde yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="7b3bb-139">RSAT'ı yükleme ve Finance and Operations uygulamaları ve Azure DevOps ile birlikte çalışacak şekilde yapılandırma hakkında daha fazla bilgi için bkz. [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="7b3bb-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="7b3bb-140">Aracı kullanma ile ilgili ön koşullara dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="7b3bb-141">Aşağıdaki çizim, RSAT ayarları örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="7b3bb-142">Mavi dikdörtgen, Azure DevOps'a erişimi belirleyen parametreleri barındırır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="7b3bb-143">Yeşil dikdörtgen, örneğe erişimi belirten parametreleri barındırır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="7b3bb-144">![RSAT ayarları](media/GER-Configure.png "RSAT Ayarları iletişim kutusunun ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="7b3bb-145">Daha fazla raporlama ve inceleme için test olaylarının günlüklerini toplayabilmek amacıyla, paketlerdeki test yürütmelerini, doğru yürütme sırasının sağlanmasına yardımcı olmak için organize etmek amacıyla, topolojiden dağıtılmış Azure DevOps'a erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="7b3bb-146">Bu konudaki örneği tamamlamak için [RSAT testleri için ER kullanımı](https://go.microsoft.com/fwlink/?linkid=874684)'nı indirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="7b3bb-147">Bu zip dosyası aşağıdaki görev kılavuzlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="7b3bb-148">İçerik</span><span class="sxs-lookup"><span data-stu-id="7b3bb-148">Content</span></span>                                           | <span data-ttu-id="7b3bb-149">Dosya adı ve yer</span><span class="sxs-lookup"><span data-stu-id="7b3bb-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="7b3bb-150">Test için veri hazırlamak üzere örnek görev kaydı</span><span class="sxs-lookup"><span data-stu-id="7b3bb-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="7b3bb-151">\\Recording.xml hazırlama</span><span class="sxs-lookup"><span data-stu-id="7b3bb-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="7b3bb-152">Satıcı ödemesini işlemek için örnek görev kaydı</span><span class="sxs-lookup"><span data-stu-id="7b3bb-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="7b3bb-153">\\Recording.xml işleme</span><span class="sxs-lookup"><span data-stu-id="7b3bb-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="7b3bb-154">Borç hesapları modülünü, satıcı ödemelerini işleyecek şekilde hazırlayın</span><span class="sxs-lookup"><span data-stu-id="7b3bb-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="7b3bb-155">Örneğinizde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="7b3bb-156">LCS deposundan aşağıdaki ER yapılandırmalarını indirme.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="7b3bb-157">Yönergeler için [ER Lifecycle Services'tan bir yapılandırmayı içe aktarma](./tasks/er-import-configuration-lifecycle-services.md)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="7b3bb-158">**Ödeme modelil** ER modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7b3bb-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="7b3bb-159">**Ödeme modeli eşleme 1611** ER modeli eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7b3bb-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="7b3bb-160">**BACS (İNG)** ER formatı yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7b3bb-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="7b3bb-161">![Elektronik raporlama yapılandırmaları](media/GER-Configurations.png "Elektronik raporlamada Yapılandırmalar sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="7b3bb-162">**GBSI** Büyük Britanya'da ülke/bölge bağlamı bulunan demo veri şirketini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="7b3bb-163">Borç hesapları parametrelerini yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="7b3bb-164">**Borç hesapları \> Ödeme kurulumu \> Ödeme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="7b3bb-165">Ödeme yöntemleri için **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="7b3bb-166">Seçili ödeme yöntemini, satıcı ödeme işlemesi için daha önce yüklediğiniz **BACS (İNG.)** ER biçimini kullanacak şekilde yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="7b3bb-167">**Dosya formatları** Hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="7b3bb-168">**Biçim yapılandırmasını dışa aktarma** alanında, **BACS (İNG)**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="7b3bb-169">![Ödeme yöntemleri sayfası](media/GER-APParameters.png "Ödeme yöntemleri sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b3bb-170">Bu ER biçiminin, özelleştirmeleri desteklemek üzere oluşturulan türetilmiş sürümü varsa **Elektronik** ödeme yönteminde bu yapılandırmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="7b3bb-171">Örnek bir satıcı ödemesi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="7b3bb-172">**Borç hesapları \> Ödemeler \> Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="7b3bb-173">Ödeme günlüğünü deftere nakletmediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="7b3bb-174">![Ödeme günlüğü sayfası](media/GER-APJournal.png "Ödeme günlüğü sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="7b3bb-175">**Satırlar**'ı seçin ve aşağıdaki bilgiye sahip satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="7b3bb-176">Alan</span><span class="sxs-lookup"><span data-stu-id="7b3bb-176">Field</span></span>               | <span data-ttu-id="7b3bb-177">Örnek değer</span><span class="sxs-lookup"><span data-stu-id="7b3bb-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="7b3bb-178">Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="7b3bb-178">Vendor name</span></span>         | <span data-ttu-id="7b3bb-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="7b3bb-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="7b3bb-180">Borç</span><span class="sxs-lookup"><span data-stu-id="7b3bb-180">Debit</span></span>               | <span data-ttu-id="7b3bb-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7b3bb-181">1,000.00</span></span>        |
        | <span data-ttu-id="7b3bb-182">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="7b3bb-182">Currency</span></span>            | <span data-ttu-id="7b3bb-183">GBP</span><span class="sxs-lookup"><span data-stu-id="7b3bb-183">GBP</span></span>             |
        | <span data-ttu-id="7b3bb-184">Mahsup hesabı türü</span><span class="sxs-lookup"><span data-stu-id="7b3bb-184">Offset account type</span></span> | <span data-ttu-id="7b3bb-185">Banka</span><span class="sxs-lookup"><span data-stu-id="7b3bb-185">Bank</span></span>            |
        | <span data-ttu-id="7b3bb-186">Mahsup hesabı</span><span class="sxs-lookup"><span data-stu-id="7b3bb-186">Offset account</span></span>      | <span data-ttu-id="7b3bb-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="7b3bb-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="7b3bb-188">Ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="7b3bb-188">Method of payment</span></span>   | <span data-ttu-id="7b3bb-189">Elektronik</span><span class="sxs-lookup"><span data-stu-id="7b3bb-189">Electronic</span></span>      |

    <span data-ttu-id="7b3bb-190">![Satıcı ödemeleri sayfası](media/GER-APJournalLines.png "Satıcı ödemeleri sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="7b3bb-191">Satıcı ödeme işlemini test etmek için ER çerçevesini hazırlayın</span><span class="sxs-lookup"><span data-stu-id="7b3bb-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="7b3bb-192">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7b3bb-192">Configure ER parameters</span></span>

1. <span data-ttu-id="7b3bb-193">**Organizasyon yönetimi \> Elektronik raporlama \> Elektronik raporlama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="7b3bb-194">**Ekler** sekmesinde, **Temel** alanında **Dosya**'yı Belge yönetimi (DM) çerçevesinin, temel özelliklerle ilgili belgeleri DM ekleri olarak tutmak için kullandığı belge türü olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="7b3bb-195">![Elektronik raporlama parametreleri sayfası](media/GER-ERParameters.png "Elektronik raporlama parametreleri sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="7b3bb-196">Satıcı ödemesiyle ilgili belgelerin temel kopyalarını oluştur</span><span class="sxs-lookup"><span data-stu-id="7b3bb-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="7b3bb-197">**Borç hesapları \> Ödemeler \> Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="7b3bb-198">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-198">Select **Lines**.</span></span>
3. <span data-ttu-id="7b3bb-199">**Ödemeleri oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="7b3bb-200">Ödeme yöntemleri için **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="7b3bb-201">**GBSI OPER** banka hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="7b3bb-202">**Kontrol raporu yazdır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="7b3bb-203">Oluşturulan çıktıyı bir ZIP dosyası olarak indirin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="7b3bb-204">İndirilen dosyayı açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="7b3bb-205">İndirilen dosyadan aşağıdaki dosyaları ayıklayın:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="7b3bb-206">**Dosya** metin biçiminde ödeme dosyası</span><span class="sxs-lookup"><span data-stu-id="7b3bb-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="7b3bb-207">**ERVendOutPaymControlReport** kontrol rapor dosyası XLSX biçiminde</span><span class="sxs-lookup"><span data-stu-id="7b3bb-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="7b3bb-208">![Ayıklanan dosyalar](media/GER-APJournalProcessed.png "Windows gezgininde ayıklanan dosya adlarının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="7b3bb-209">ER temel özelliğini açın</span><span class="sxs-lookup"><span data-stu-id="7b3bb-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="7b3bb-210">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="7b3bb-211">Eylem Bölmesindeki **Yapılandırmalar** sekmesinde, **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="7b3bb-212">**Hata ayıklama modu** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="7b3bb-213">**Hata ayıklama modu** parametresini etkinleştirerek, ER çerçevesini, giden belgeleri oluşturan herhangi bir ER formatının yürütülmesinden sonra aşağıdaki işlemleri yapmaya zorlarsınız:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="7b3bb-214">Bir temelin yürütülen ER formatının herhangi bir bileşeni için yapılandırılmış olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="7b3bb-215">Yapılandırılan her temelin geçerli koşullarda (oturum açmış şirketin şirket kodu, oluşturulan çıkışın dosya adı ve dosya adı uzantısı vb.) uygulanabilir olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="7b3bb-216">Geçerli her temel için, aşağıdaki eylemleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="7b3bb-217">ER biçiminin yürütülmesi sırasında oluşturulan çıktıyı ilgili temelle karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="7b3bb-218">Karşılaştırma sonuçlarını ER yapılandırmaları hata ayıklama günlüğünde saklayın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="7b3bb-219">Satıcı ödeme işlemi için ER temellerini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="7b3bb-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="7b3bb-220">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="7b3bb-221">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="7b3bb-222">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-222">Select **New**.</span></span>
4. <span data-ttu-id="7b3bb-223">**Referans** alanında, **BACS (İNG)** formatını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="7b3bb-224">**Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="7b3bb-225">Satıcı ödeme dosyası için yeni bir temel ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="7b3bb-226">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-226">Select **New**.</span></span>
    2. <span data-ttu-id="7b3bb-227">**Tür** alanında temel yapıları depolamak için ER parametrelerinde yapılandırdığıız **Dosya** DM belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="7b3bb-228">Yerel olarak kaydedilmiş **Dosya** ödeme dosyasını metin biçiminde seçmek için gözatın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="7b3bb-229">**Açıklama** alanına **Ödeme TXT dosyası** girin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="7b3bb-230">Satıcı ödemesine kontrol raporu için yeni bir temel ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="7b3bb-231">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-231">Select **New**.</span></span>
    2. <span data-ttu-id="7b3bb-232">**Tür** alanında temel yapıları depolamak için ER parametrelerinde yapılandırdığıız **Dosya** DM belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="7b3bb-233">Yerel olarak kaydedilmiş **ERVendOutPaymControlReport** kontrol raporu dosyasını XLSX formatında kaydetmek için gözatın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="7b3bb-234">**Açıklama** alanına **Ödeme XLSX dosyası kontrol raporu** girin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="7b3bb-235">![Satıcı ödeme dosyası ve kontrol raporu için temeller](media/GER-BaselineAttachments.png "Seçilen Ödeme XLSX dosyası kontrol raporu ile Yapılandırma sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="7b3bb-236">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-236">Close the page.</span></span>
9. <span data-ttu-id="7b3bb-237">**Temeller** hızlı sekmesinde ödeme dosyasına bir temel yapılandırmak için **Yeni**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="7b3bb-238">Yeni satırı **Ödeme dosyası için temel ayarları** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="7b3bb-239">**Dosya bileşeni adı** alanında bu temeli BACS (İNG) metin formatı biçiminde ödeme dosyası oluşturan ER biçiminli bir çıktıya uygulamak için **dosya**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="7b3bb-240">**Şirketler** alanında **BACS (UK)** ER biçimi GBSI şirketinde çalıştırıldığında bu temeli uygulamak için **GBSI**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="7b3bb-241">**Dosya adı maskesi** alanında bu temeli sadece **.txt** dosya adı uzantılı **dosya** biçim bileşeni çıktılarına uygulamak için **\*.TXT** girin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="7b3bb-242">**Temel** alanında, **Ödeme TXT dosyası**'nı bu temel, ortaya çıkan sonucu karşılaştırması için seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="7b3bb-243">Kontrol raporu için temel yapılandırmak amacıyla **Yeni**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="7b3bb-244">Yeni satırı **Kontrol raporu için temel ayarları** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="7b3bb-245">**Dosya bileşeni adı** alanında bu temeli kontrol raporu oluşturan ER biçiminli bir çıktıya uygulamak için **ERVendOutPaymControlReport**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="7b3bb-246">**Şirketler** alanında **BACS (UK)** ER biçimi GBSI şirketinde çalıştırıldığında bu temeli uygulamak için **GBSI**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="7b3bb-247">**Dosya adı maskesi** alanında bu temeli sadece **.xslx** dosya adı uzantılı **ERVendOutPaymControlReport** biçim bileşeni çıktılarına uygulamak için **\*.XLSX** girin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="7b3bb-248">**Temel** alanında, **Ödeme XLSX konrol raporu**'nu bu temel, ortaya çıkan sonucu karşılaştırması için seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="7b3bb-249">![Yapılandırma sayfasında Temeller hızlı sekmesi](media/GER-BaselineRules.png "Yapılandırma sayfasında Temeller hızlı sekmesinin ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="7b3bb-250">Satıcı ödeme işlemini doğrulayacak testleri kaydedin</span><span class="sxs-lookup"><span data-stu-id="7b3bb-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="7b3bb-251">İşlevsel bir yetkili kullanıcı olarak satıcı ödeme işlemini test etmek için kendi adımlarınızı kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="7b3bb-252">Öceneden yüklediğiniz (ve gerektiği yerde düzenlediğiniz) **Hazırla\\Kayıt.xml** görev kaydının yürütülmesini öneririz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="7b3bb-253">Bu kayıt tüm test verilerinin doğru duruma ayarlanmasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="7b3bb-254">Test birçok kez yapıldığından ve her testin aynı durumda olan verileri kullanması gerektiğinden bu adım gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="7b3bb-255">Kullanıcı ayarlarını sıfırlayın</span><span class="sxs-lookup"><span data-stu-id="7b3bb-255">Reset user settings</span></span>

1. <span data-ttu-id="7b3bb-256">Varsayılan panoyu açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="7b3bb-257">**Ayarlar** düğmesini (çark simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="7b3bb-258">**Kıllanıcı seçenekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-258">Select **User options**.</span></span>
4. <span data-ttu-id="7b3bb-259">**Kullanım verileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="7b3bb-260">**Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-260">Select **Reset**.</span></span>
6. <span data-ttu-id="7b3bb-261">Kullanım verilerini sıfırlamak istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="7b3bb-262">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="7b3bb-263">Test için veri hazırlamak adına adımları kaydedin</span><span class="sxs-lookup"><span data-stu-id="7b3bb-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="7b3bb-264">**Ayarlar** düğmesini (çark simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="7b3bb-265">**Görev kaydedici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="7b3bb-266">**Kayıt yürüt**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="7b3bb-267">**Bu bilgisayardan aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="7b3bb-268">**Gözat**'ı seçin ve , yerel olarak kaydet **Hazırla\\Kayıt.xml** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="7b3bb-269">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-269">Select **Start**.</span></span>
7. <span data-ttu-id="7b3bb-270">Kayıttaki tüm adımlar yürütülünceye kadar **Sonraki beklemedeki adımı yürüt**'ü seçmeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="7b3bb-271">Bu görev kaydı performansı aşağıdaki eylemleri gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="7b3bb-272">İşlenmiş ödeme satırının durumunu **Yok** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="7b3bb-273">![Görev kaydetme adım 3-4](media/GER-Recording1Review1.png "Görev kaydetme adım 3-4'ün ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="7b3bb-274">**Hata ayıklama modu** ER kullanıcı parametrelerini açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="7b3bb-275">![Görev kaydetme adım 9-10](media/GER-Recording1Review2.png "Görev kaydetme adım 9-10'un ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="7b3bb-276">Oluşturulan dosyaların temellerinin karşılaştırılmasını içeren ER hata ayıklama günlüğünü temizleyin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="7b3bb-277">![Görev kaydetme adım 13-15](media/GER-Recording1Review3.png "Görev kaydetme adım 13-15'in ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="7b3bb-278">Satıcı ödeme işlemini test edecek adımları kaydedin</span><span class="sxs-lookup"><span data-stu-id="7b3bb-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="7b3bb-279">Öceneden yüklediğiniz (ve gerektiği yerde düzenlediğiniz) **İşle\\Kayıt.xml** görev kaydının yürütülmesini öneririz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="7b3bb-280">Bu kayıt, satıcı ödemelerini işlemek ve oluşturulan belgelerin ilgili temellerinin karşılaştırmasının sonuçlarını doğrulamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="7b3bb-281">**Ayarlar** düğmesini (çark simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="7b3bb-282">**Görev kaydedici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="7b3bb-283">**Kayıt yürüt**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="7b3bb-284">**Bu bilgisayardan aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="7b3bb-285">**Gözat**'ı seçin ve , yerel olarak kaydedildi **İşle\\Kayıt.xml** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="7b3bb-286">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-286">Select **Start**.</span></span>
7. <span data-ttu-id="7b3bb-287">Kayıttaki tüm adımlar yürütülünceye kadar **Sonraki beklemedeki adımı yürüt**'ü seçmeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="7b3bb-288">Bu görev kaydı performansı aşağıdaki eylemleri gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="7b3bb-289">Satıcı ödeme işlemini başlat</span><span class="sxs-lookup"><span data-stu-id="7b3bb-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="7b3bb-290">Doğru çalışma zamanı parametrelerini seçin ve kontrol raporu oluşturmayı açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="7b3bb-291">![Görev kaydetme adım 3-8](media/GER-Recording2Review1.png "Görev kaydetme adım 3-8'in ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="7b3bb-292">Oluşturulan çıktıların karşılık gelen temellerle karşılaştırılmasının sonuçlarını kaydetmek için ER hata ayıklama günlüğüne erişin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="7b3bb-293">ER hata ayıklama günlüğünde, karşılaştırmanın sonuçları **Oluşturulan metin** alanında görünür.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="7b3bb-294">**Biçim bileşeni** ve **Günlük girişine neden olan format biçimi yolu** oluşturulan çıktının temelleriyle karşılaştırıldığı dosya bileşenine referansta bulunur.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="7b3bb-295">![Elektronik raporlama çalıştırma günlüklerindeki girişler sayfası](media/GER-ERDebugLog.png "Elektronik raporlama çalıştırma günlüklerdeki girişler sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="7b3bb-296">Geçerli çıktının satır temelleriyle karşılaştırılması, görev kaydedicisini **Doğrula** seçeneği kullanılarak ve **Geçerli Değer** seçilerek kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="7b3bb-297">![Geçerli değerle karşılaştırmak için Doğrula seçeneğini kullanma](media/GER-TRRecordValidation.png "Geçerli değerle karşılaştırmak için Doğrula seçeneğini kullanmanın ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="7b3bb-298">Aşağıdaki resim, kaydedilen doğrulama adımlarının görev kaydında nasıl göründüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="7b3bb-299">![Görev kaydetme adım 13-15](media/GER-Recording2Review2.png "Görev kaydetme adım 13-15'in ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="7b3bb-300">Kaydedilmiş testleri Azure DevOps'a ekle</span><span class="sxs-lookup"><span data-stu-id="7b3bb-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="7b3bb-301">Azure DevOps ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="7b3bb-302">[Aracı yapılandırdığınızda ](#prerequisites) RSAT parametrelerinde tanımladığınız projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="7b3bb-303">[Aracı yapılandırdığınızda ](#prerequisites) RSAT parametrelerinde tanımladığınız test planını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="7b3bb-304">Seçilen test planı için yeni bir test olayını seçin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="7b3bb-305">Test olayını **Satıcının elektronik ödeme işlemini test etmek için verileri hazırla** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="7b3bb-306">**Kayıt.xml** dosyasını daha önce yüklediğiniz **Hazırla** dosyasına iliştirin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="7b3bb-307">Seçilen test planı için yeni bir test olayını seçin:</span><span class="sxs-lookup"><span data-stu-id="7b3bb-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="7b3bb-308">Test olayını **ER formatı BACS (İNG) kullanarak satıcı ödemelerini test etme** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="7b3bb-309">**Kayıt.xml** dosyasını daha önce yüklediğiniz **İşle** dosyasına iliştirin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="7b3bb-310">![Seçilen test planı için yeni test olayları](media/GER-RSAT-DevOps-Tests-Passed.png "Seçilen test planı için yeni test olaylarının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="7b3bb-311">Eklenen testlerin yürütme sırasının doğru olup olmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="7b3bb-312">Kaydedilmiş testleri çalıştırmak için RSAT'yi hazırlayın</span><span class="sxs-lookup"><span data-stu-id="7b3bb-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="7b3bb-313">Testleri Azure DevOps'dan yükleyin</span><span class="sxs-lookup"><span data-stu-id="7b3bb-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="7b3bb-314">Geçerli topolojide yerel RSAT uygulamasını açın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="7b3bb-315">Azure DevOps'da mevcut olan testleri RSAT'a yüklemek için **Yükle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="7b3bb-316">![RSAT'a yüklenen testler](media/GER-RSAT-RSAT-Tests-Loaded.png "RSAT'a yüklenen testlerin ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="7b3bb-317">Otomasyon ve parametre dosyaları oluşturun</span><span class="sxs-lookup"><span data-stu-id="7b3bb-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="7b3bb-318">RSAT'da, Azure DevOps'dan yüklediğiniz testleri seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="7b3bb-319">RSAT otomasyonu ve parametre dosyaları yaratmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="7b3bb-320">![RSAT otomasyonu ve RSAT'ta oluşturulmuş parametreler dosyaları](media/GER-RSAT-RSAT-Tests-Initiated.png "RSAT otomasyonu ve RSAT'ta oluşturulmuş parametreler dosyalarının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="7b3bb-321">Parametre dosyalarını değiştirin</span><span class="sxs-lookup"><span data-stu-id="7b3bb-321">Modify the parameters files</span></span>

1. <span data-ttu-id="7b3bb-322">RSAT'ta **Satıcının elektronik ödeme işlemini test etmek için verileri hazırla** test olayını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="7b3bb-323">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-323">Select **Edit**.</span></span>
3. <span data-ttu-id="7b3bb-324">Açılan Microsoft Excel çalışma sayfasında **Genel** çalışma sayfasında şirket kodunu **GBSI** olarak değiştirin, çünkü bu şirket test çalışması olarak kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="7b3bb-325">RSAT'ta **ER formatı BACS (İNG) kullanarak satıcı ödemelerini test etme** test olayını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="7b3bb-326">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-326">Select **Edit**.</span></span>
6. <span data-ttu-id="7b3bb-327">Açılan Excel çalışma kitabında, **Genel** çalışma sayfasında şirket kodunu **GBSI** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="7b3bb-328">**Erformatmappingrunlogtable** çalışma sayfası üzerinde, çalışma sayfasında, A:3 ve C:3 hücrelerinin, ER hata ayıklama günlüğü tablosundaki alanların, çıktının temeliyle karşılaştırmasının sonuçlarını doğrulamak için kullanılan alanların metnini içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="7b3bb-329">Bu metinler, test yürütmesi sırasında oluşturulan ER hata ayıklama günlükleri kayıtlarını değerlendirmek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="7b3bb-330">![ERFormatMappingRunLogTable çalışma sayfası](media/GER-RSAT-RSAT-ExcelParameters.png "ERFormatMappingRunLogTable çalışma sayfasının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="7b3bb-331">Testleri çalıştırın ve sonuçları analiz edin</span><span class="sxs-lookup"><span data-stu-id="7b3bb-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="7b3bb-332">RSAT içindeki testleri çalıştırma</span><span class="sxs-lookup"><span data-stu-id="7b3bb-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="7b3bb-333">RSAT'da, yüklenen testleri seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="7b3bb-334">**Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-334">Select **Run**.</span></span>

<span data-ttu-id="7b3bb-335">Test çalışmalarının bir web tarayıcısı kullanarak uygulamada otomatik olarak çalıştırılmalarına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="7b3bb-336">Test yürütmesi sonuçlarını analiz et</span><span class="sxs-lookup"><span data-stu-id="7b3bb-336">Analyze the results of test execution</span></span>

<span data-ttu-id="7b3bb-337">Test yürütmesinin sonuçları RSAT'da depolanır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="7b3bb-338">Her iki testin da geçtiğine emin olun.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="7b3bb-339">![RSAT'ta geçen testler](media/GER-RSAT-RSAT-Tests-Passed.png "RSAT'ta geçen testlerin ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="7b3bb-340">Daha fazla analiz yapabilmeniz için Azure DevOps test yürütmesi sonuçlarının da gönderilip gönderilmediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="7b3bb-341">![Azure DevOps'taki test çalışmasının sonuçları](media/GER-RSAT-DevOps-Tests-Added.png "Azure DevOps'taki test çalışmasının sonuçlarının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="7b3bb-342">Testlerin başarısız olduğu bir durum benzetimi</span><span class="sxs-lookup"><span data-stu-id="7b3bb-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="7b3bb-343">Oluşturulan çıktılardan en az biri ilgili temelle eşleşmediğinde bu test paketinin başarısız olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="7b3bb-344">Bu durumu başarmak için, ilgili temelden farklı içeriğe sahip bir ödeme dosyası oluşturacak **BACS (İNG)** biçiminin türetilmiş sürümünü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="7b3bb-345">Bu durumun benzetimini yapmak için aynı **BACS (İNG)** biçimini kullanabilir, ancak işlenmiş ödeme satırındaki ödeme tutarını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="7b3bb-346">Uygulamayı açın ve **Borç hesapları \> Ödemeler \> Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="7b3bb-347">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-347">Select **Lines**.</span></span>
3. <span data-ttu-id="7b3bb-348">Ödeme satırını seçin ve **Ödeme durumu \> Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="7b3bb-349">**Borç** alanında, değeri **1,000.00** 'den **2,000.00**'e değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="7b3bb-350">Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="7b3bb-351">RSAT içindeki testleri çalıştırma</span><span class="sxs-lookup"><span data-stu-id="7b3bb-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="7b3bb-352">RSAT'da, yüklenen testleri seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="7b3bb-353">**Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-353">Select **Run**.</span></span>

<span data-ttu-id="7b3bb-354">Test çalışmalarının bir web tarayıcısı kullanarak uygulamada otomatik olarak çalıştırılmalarına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="7b3bb-355">Test yürütmesi sonuçlarını analiz et</span><span class="sxs-lookup"><span data-stu-id="7b3bb-355">Analyze the results of test execution</span></span>

<span data-ttu-id="7b3bb-356">Test yürütmesinin sonuçları RSAT'da depolanır.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="7b3bb-357">İkinci testin ikinci yürütme esnasında başarısız olup olmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="7b3bb-358">![RSAT'taki başarısız test sonuçları](media/GER-RSAT-RSAT-Tests-Failed.png "RSAT'taki başarısız test sonuçlarının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="7b3bb-359">Daha fazla analiz yapabilmeniz için Azure DevOps test yürütmesi sonuçlarının da gönderilip gönderilmediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="7b3bb-360">![Azure DevOps'taki başarısız test sonuçları](media/GER-RSAT-DevOps-Tests-Failed.png "Azure DevOps'taki başarısız test sonuçlarının ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="7b3bb-361">Her testin durumuna erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-361">You can access the status of each test.</span></span> <span data-ttu-id="7b3bb-362">Ayrıca yürütme günlüğüne erişerek herhangi bir hatanın nedenini çözümleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="7b3bb-363">Aşağıdaki resimde, yürütme günlüğünde oluşturulan ödeme dosyası ve onun temeli arasındaki içerikteki fark nedeniyle hatanın oluştuğu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="7b3bb-364">![Azure DevOps'taki hataları analiz etmek için yürütme günlüğü](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Azure DevOps'taki hataları analiz etmek için yürütme günlüğünün ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="7b3bb-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="7b3bb-365">Bu nedenle, gördüğünüz gibi, herhangi bir ER biçiminin çalışması, test platformu gibi RSAT ve ER temel özelliğini kullanan görev kaydedici tabanlı test çalışmaları kullanılarak otomatik olarak değerlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b3bb-366">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7b3bb-366">Additional resources</span></span>

- [<span data-ttu-id="7b3bb-367">Görev kaydedici kaynakları</span><span class="sxs-lookup"><span data-stu-id="7b3bb-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="7b3bb-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="7b3bb-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="7b3bb-369">Kullanıcı kabul testleri oluşturma ve otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="7b3bb-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="7b3bb-370">Sürekli oluşturma ve test otomasyonunu destekleyen bir ortam dağıtma ve kullanma</span><span class="sxs-lookup"><span data-stu-id="7b3bb-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="7b3bb-371">Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma</span><span class="sxs-lookup"><span data-stu-id="7b3bb-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="7b3bb-372">ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.</span><span class="sxs-lookup"><span data-stu-id="7b3bb-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="7b3bb-373">ER Lifecycle Services'tan bir yapılandırmayı içe aktarma</span><span class="sxs-lookup"><span data-stu-id="7b3bb-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]