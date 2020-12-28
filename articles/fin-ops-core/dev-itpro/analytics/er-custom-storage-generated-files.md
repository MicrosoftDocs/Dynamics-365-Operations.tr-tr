---
title: Oluşturulan belgeler için özel depolama konumları belirtme
description: Bu konu, Elektronik raporlama (ER) biçimleri tarafından oluşturulan belgeler için depolama konumlarının listesini genişletmeyi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680770"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="10b4c-103">Oluşturulan belgeler için özel depolama konumları belirtme</span><span class="sxs-lookup"><span data-stu-id="10b4c-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10b4c-104">Elektronik raporlama (ER) çerçevesinin Uygulama programlama arabirimi (API), ER biçimlerinin oluşturduğu depolama konumlarını genişletmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="10b4c-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="10b4c-105">Bu konuda, ER hedefleri oluşturma görevini varsayılan hedef fabrikasına aktarıp kendi hedef mantığı olan özel bir sınıf uygulayarak, oluşturulan belgeler için özel bir depolama konumu ekleme açıklanır.</span><span class="sxs-lookup"><span data-stu-id="10b4c-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="10b4c-106">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="10b4c-106">Prerequisites</span></span>

<span data-ttu-id="10b4c-107">Sürekli derlemeyi destekleyen bir topoloji dağıtın.</span><span class="sxs-lookup"><span data-stu-id="10b4c-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="10b4c-108">Daha fazla bilgi için, [Sürekli yapılandırma ve test otomasyonu destekleyen topolojiler dağıtın](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="10b4c-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="10b4c-109">Bu topoloji, aşapıdaki rollerden biri için erişim izniniz olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="10b4c-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="10b4c-110">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="10b4c-110">Electronic reporting developer</span></span>
- <span data-ttu-id="10b4c-111">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="10b4c-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="10b4c-112">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="10b4c-112">System administrator</span></span>

<span data-ttu-id="10b4c-113">Bu topoloji için geliştirme ortamına da erişiminiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="10b4c-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="10b4c-114">Bu konudaki tüm görevler **USMF** şirketinde tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="10b4c-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="10b4c-115">Sabit kıymet ileri taşıma ER biçimini içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="10b4c-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="10b4c-116">Özel bir depolama konumu eklemeyi planladığınız belgeleri oluşturmak için geçerli topolojiye **Sabit kıymet ileri taşıma** ER biçimini [içeri aktarın](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="10b4c-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Yapılandırma havuzu sayfası](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="10b4c-118">Sabit kıymet ileri taşıma raporunu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="10b4c-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="10b4c-119">**Sabit kıymetler** \> **Sorgular ve raporlar** \> **İşlem raporları** \> **Sabit kıymet ileri taşıma** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="10b4c-120">**Başlangıç tarihi** alanına **1/1/2017** (1 Ocak 2017) tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="10b4c-121">**Bitiş tarihi** alanına **1/31/2017** (31 Ocak 2017) tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="10b4c-122">**Para birimi** alanında **Muhasebe para birimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="10b4c-123">**Biçim eşleme** alanında, **Sabit kıymet ileri taşıma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="10b4c-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-124">Select **OK**.</span></span>

![Sabit kıymet ileri taşıma raporu için çalışma zamanı iletişim kutusu](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="10b4c-126">Microsoft Excel'de, oluşturulan ve indirmeye hazır olan giden belgeyi inceleyin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="10b4c-127">Bu davranış, hiçbir [hedefin](electronic-reporting-destinations.md) yapılandırılmadığı ve etkileşimli modda çalıştırılan bir ER biçimi için [varsayılan davranıştır](electronic-reporting-destinations.md#default-behavior).</span><span class="sxs-lookup"><span data-stu-id="10b4c-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="10b4c-128">Kaynak kodu inceleme</span><span class="sxs-lookup"><span data-stu-id="10b4c-128">Review the source code</span></span>

<span data-ttu-id="10b4c-129">`AssetRollForwardService` sınıfının `generateReportByGER()` yönteminin kodunu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="10b4c-130">`Run()` yönteminin ER çerçevesini çağırmak ve **Sabit kıymet ileri taşıma** raporunu oluşturmak için kullanılmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
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

## <a name="modify-the-source-code"></a><span data-ttu-id="10b4c-131">Kaynak kodu değiştirme</span><span class="sxs-lookup"><span data-stu-id="10b4c-131">Modify the source code</span></span>

1. <span data-ttu-id="10b4c-132">Visual Studio projenizde, yeni bir sınıf ekleyin (bu örnekte `AssetRollForwardDestination`) ve oluşturulan **Sabit kıymet ileri taşıma** raporlarına özel hedefinizi uygulamak için bir kod yazın.</span><span class="sxs-lookup"><span data-stu-id="10b4c-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="10b4c-133">`new()` yöntemi, özgün ER hedefi nesnesini ve oluşturulan raporların depolanması gereken özel konumu belirten uygulama mantık temelli parametresini almak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="10b4c-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="10b4c-134">Bu örnekte, özel konum Uygulama Nesne Sunucusu (AOS) hizmetini çalıştıran sunucunun yerel dosya sistemindeki klasör adıdır.</span><span class="sxs-lookup"><span data-stu-id="10b4c-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="10b4c-135">`saveFile()` yöntemi, oluşturulan bir belgeyi AOS hizmetini çalıştıran sunucunun yerel dosya sistemindeki bir klasöre kaydetmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="10b4c-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="10b4c-136">Visual Studio projenizde, yeni bir sınıf ekleyin (bu örnekte `AssetRollForwardDestinationFactory`) ve hedef oluşturma görevini varsayılan hedef fabrikasına aktaran özel bir hedef fabrikası oluşturmak ve bir dosya hedefini kendi hedefinizle sarmalamak için bir kod yazın.</span><span class="sxs-lookup"><span data-stu-id="10b4c-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="10b4c-137">Mevcut `AssetRollForwardService` sınıfını değiştirin ve rapor çalıştırıcısı için özel bir hedef fabrikası ayarlamak amacıyla bir kod yazın.</span><span class="sxs-lookup"><span data-stu-id="10b4c-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="10b4c-138">Özel bir hedef fabrikası oluşturulduğunda, hedef klasörü belirten uygulama temelli parametreye geçilir.</span><span class="sxs-lookup"><span data-stu-id="10b4c-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="10b4c-139">Bu şekilde, bu hedef klasör oluşturulan dosyaları depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10b4c-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="10b4c-140">Belirtilen klasörün (bu örnekte **c:\\0**) AOS hizmetini çalıştıran sunucunun yerel dosya sisteminde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="10b4c-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="10b4c-141">Aksi takdirde, çalışma zamanında [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) özel durumu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="10b4c-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
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

4. <span data-ttu-id="10b4c-142">Projenizi yeniden inşa edin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="10b4c-143">Sabit kıymet ileri taşıma raporunu yeniden çalıştırma</span><span class="sxs-lookup"><span data-stu-id="10b4c-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="10b4c-144">**Sabit kıymetler** \> **Sorgular ve raporlar** \> **İşlem raporları** \> **Sabit kıymet ileri taşıma** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="10b4c-145">**Başlangıç tarihi** alanına **1/1/2017** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="10b4c-146">**Bitiş tarihi** alanına **1/31/2017** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="10b4c-147">**Para birimi** alanında **Muhasebe para birimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="10b4c-148">**Biçim eşleme** alanında, **Sabit kıymet ileri taşıma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="10b4c-149">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10b4c-149">Select **OK**.</span></span>
7. <span data-ttu-id="10b4c-150">Oluşturulan dosyayı bulmak için yerel **C:\\0** klasörüne göz atın.</span><span class="sxs-lookup"><span data-stu-id="10b4c-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="10b4c-151">Bu örnekte `AssetRollForwardDestination` nesnesinde `originDestination` nesnesi kullanılmadığı için ER biçim [hedefleri](electronic-reporting-destinations.md) ile ilgili yapılandırmalar çalışma zamanında yok sayılacaktır.</span><span class="sxs-lookup"><span data-stu-id="10b4c-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10b4c-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="10b4c-152">Additional resources</span></span>

- [<span data-ttu-id="10b4c-153">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="10b4c-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="10b4c-154">Genişletilebilirlik giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="10b4c-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
