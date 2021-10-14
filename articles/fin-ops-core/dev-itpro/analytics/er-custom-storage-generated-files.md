---
title: Oluşturulan belgeler için özel depolama konumları belirtme
description: Bu konu, Elektronik raporlama (ER) biçimleri tarafından oluşturulan belgeler için depolama konumlarının listesini genişletmeyi açıklar.
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 337e760f28161721d886c7bbec09b5ff8dbfad45
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594921"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Oluşturulan belgeler için özel depolama konumları belirtme

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) çerçevesinin Uygulama programlama arabirimi (API), ER biçimlerinin oluşturduğu depolama konumlarını genişletmenize olanak sağlar. Bu konuda, ER hedefleri oluşturma görevini varsayılan hedef fabrikasına aktarıp kendi hedef mantığı olan özel bir sınıf uygulayarak, oluşturulan belgeler için özel bir depolama konumu ekleme açıklanır.

## <a name="prerequisites"></a>Önkoşullar

Sürekli derlemeyi destekleyen bir topoloji dağıtın. Daha fazla bilgi için, [Sürekli yapılandırma ve test otomasyonu destekleyen topolojiler dağıtın](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Bu topoloji, aşapıdaki rollerden biri için erişim izniniz olmalıdır:

- Elektronik raporlama geliştirici
- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

Bu topoloji için geliştirme ortamına da erişiminiz olması gerekir.

Bu konudaki tüm görevler **USMF** şirketinde tamamlanabilir.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Sabit kıymet ileri taşıma ER biçimini içeri aktarma

Özel bir depolama konumu eklemeyi planladığınız belgeleri oluşturmak için geçerli topolojiye **Sabit kıymet ileri taşıma** ER biçimini [içeri aktarın](er-download-configurations-global-repo.md).

![Yapılandırma deposu sayfası.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Sabit kıymet ileri taşıma raporunu çalıştırma

1. **Sabit kıymetler** \> **Sorgular ve raporlar** \> **İşlem raporları** \> **Sabit kıymet ileri taşıma** öğesine gidin.
2. **Başlangıç tarihi** alanına **1/1/2017** (1 Ocak 2017) tarihini girin.
3. **Bitiş tarihi** alanına **1/31/2017** (31 Ocak 2017) tarihini girin.
4. **Para birimi** alanında **Muhasebe para birimi**'ni seçin.
5. **Biçim eşleme** alanında, **Sabit kıymet ileri taşıma**'yı seçin.
6. **Tamam**'ı seçin.

![Sabit kıymet ileri taşıma raporu için çalışma zamanı iletişim kutusu.](./media/er-custom-storage-generated-files-runtime-dialog.png)

Microsoft Excel'de, oluşturulan ve indirmeye hazır olan giden belgeyi inceleyin. Bu davranış, hiçbir [hedefin](electronic-reporting-destinations.md) yapılandırılmadığı ve etkileşimli modda çalıştırılan bir ER biçimi için [varsayılan davranıştır](electronic-reporting-destinations.md#default-behavior).

## <a name="review-the-source-code"></a>Kaynak kodu inceleme

`AssetRollForwardService` sınıfının `generateReportByGER()` yönteminin kodunu inceleyin. `Run()` yönteminin ER çerçevesini çağırmak ve **Sabit kıymet ileri taşıma** raporunu oluşturmak için kullanılmasına dikkat edin.

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

## <a name="modify-the-source-code"></a>Kaynak kodu değiştirme

1. Visual Studio projenizde, yeni bir sınıf ekleyin (bu örnekte `AssetRollForwardDestination`) ve oluşturulan **Sabit kıymet ileri taşıma** raporlarına özel hedefinizi uygulamak için bir kod yazın.

    - `new()` yöntemi, özgün ER hedefi nesnesini ve oluşturulan raporların depolanması gereken özel konumu belirten uygulama mantık temelli parametresini almak için tasarlanmıştır. Bu örnekte, özel konum Uygulama Nesne Sunucusu (AOS) hizmetini çalıştıran sunucunun yerel dosya sistemindeki klasör adıdır.
    - `saveFile()` yöntemi, oluşturulan bir belgeyi AOS hizmetini çalıştıran sunucunun yerel dosya sistemindeki bir klasöre kaydetmek için tasarlanmıştır.

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

2. Visual Studio projenizde, yeni bir sınıf ekleyin (bu örnekte `AssetRollForwardDestinationFactory`) ve hedef oluşturma görevini varsayılan hedef fabrikasına aktaran özel bir hedef fabrikası oluşturmak ve bir dosya hedefini kendi hedefinizle sarmalamak için bir kod yazın.

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

3. Mevcut `AssetRollForwardService` sınıfını değiştirin ve rapor çalıştırıcısı için özel bir hedef fabrikası ayarlamak amacıyla bir kod yazın. Özel bir hedef fabrikası oluşturulduğunda, hedef klasörü belirten uygulama temelli parametreye geçilir. Bu şekilde, bu hedef klasör oluşturulan dosyaları depolamak için kullanılır.

    > [!NOTE] 
    > Belirtilen klasörün (bu örnekte **c:\\0**) AOS hizmetini çalıştıran sunucunun yerel dosya sisteminde mevcut olduğundan emin olun. Aksi takdirde, çalışma zamanında [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception) özel durumu oluşturulur.

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

4. Projenizi yeniden inşa edin.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Sabit kıymet ileri taşıma raporunu yeniden çalıştırma

1. **Sabit kıymetler** \> **Sorgular ve raporlar** \> **İşlem raporları** \> **Sabit kıymet ileri taşıma** öğesine gidin.
2. **Başlangıç tarihi** alanına **1/1/2017** tarihini girin.
3. **Bitiş tarihi** alanına **1/31/2017** tarihini girin.
4. **Para birimi** alanında **Muhasebe para birimi**'ni seçin.
5. **Biçim eşleme** alanında, **Sabit kıymet ileri taşıma**'yı seçin.
6. **Tamam**'ı seçin.
7. Oluşturulan dosyayı bulmak için yerel **C:\\0** klasörüne göz atın.

> [!NOTE]
> Bu örnekte `AssetRollForwardDestination` nesnesinde `originDestination` nesnesi kullanılmadığı için ER biçim [hedefleri](electronic-reporting-destinations.md) ile ilgili yapılandırmalar çalışma zamanında yok sayılacaktır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
- [Genişletilebilirlik giriş sayfası](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]