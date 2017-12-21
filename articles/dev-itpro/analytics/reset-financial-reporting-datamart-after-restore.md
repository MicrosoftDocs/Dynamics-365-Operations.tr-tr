---
title: "Mali raporlama veri reyonunu sıfırlama"
description: "Bu konuda Mali raporlama veri reyonunun nasıl sıfırlanacağı açıklanmaktadır."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: tr-tr
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Mali raporlama veri reyonunu sıfırlama

[!include[banner](../includes/banner.md)]

Bu konu Mali raporlama veri reyonunun aşağıdaki sürümler için nasıl sıfırlanacağını açıklar:

- Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürüm 7.2.6.0 veya üstü
- Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürüm 7.0.10000.4 veya üstü
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (şirket içi)

Finance and Operations Mali raporlama sürüm 7.2.6.0'ı edinmek için <https://support.microsoft.com/en-us/help/4052514> adresinden KB 4052514'ü indirebilirsiniz.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Finance and Operations Mali raporlama sürüm 7.2.6.0 ve üstü için Mali raporlama veri reyonunu sıfırlama

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Mali raporlama veri reyonunu Rapor tasarımcısından sıfırlama

> [!NOTE]
> Bu işlemdeki adımlar, Finance and Operations Mali raporlama sürüm 7.2.6.0 ve üstü için desteklenmektedir. Önceki bir sürüme sahipseniz, Yardım için Destek ekibine başvurun.

Belirli senaryolarda, Mali raporlama için veri reyonunu sıfırlamanız gerekebilir. Rapor Tasarımcısı istemcisinde bu görevi gerçekleştirebilirsiniz. Veri merkezini sıfırlamanızı gerektirebilecek bazı senaryolar aşağıda verilmiştir:

- Finance and Operations veri tabanı geri yüklendir, ancak veri reyonu veri tabanı geri yüklenmedi.
- Bir dönem için yanlış veriler görüyorsunuz.
- Destek, sorun giderme işleminin bir adımı olarak veri reyonunu sıfırlamanızı söylüyor.

Veri reyonu sıfırlama yalnızca veritabanındaki işlem gerçekleştirme miktarı küçük olduğunda yapılmalıdır. Mali raporlama sıfırlama işlemi sırasında kullanılamaz.

#### <a name="reset-the-data-mart"></a>Veri reyonunu sıfırlama

Veri reyonunu sıfırlamak için Rapor tasarımcısında, **Araçlar** menüsünden **Veri Reyonunu Sıfırla**'yı seçin. Görüntülenen iletişim kutusunda iki bölüm vardır: **İstatistikler** ve **Sıfırla**.

[![Veri Reyonunu Sıfırla iletişim kutusu](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>Tümleştirme denemeleri

**Tümleştirme denemeleri** kılavuzu sistemin hareketleri tümleştirmek için kaç kez girişimde bulunduğunu gösterir. Sistem ilk birkaç deneme başarılı olmazsa verileri birkaç günlük bir dönem içinde tümleştirmeyi denemeye devam eder. Deneme sayısının 8 veya üzerinde olması ve biçok Boyut kombinasyonu veya Hareket kaydı bulunması durumunda veri reyonunun sıfırlanması gerekir. Bu durumda, veriler rapor edilmeyecektir.

##### <a name="data-status"></a>Veri durumu

**Veri durumu** kılavuzu, veri reyonundaki hareketlerin, döviz kurlarının ve boyut değerlerinin anlık görüntüsünü sağlar. Çok sayıda eski kayıt kayıtlara çok sayıda güncelleştirme yapıldığını gösterir. Bu durum daha yavaş rapor oluşturma sürelerine neden olabilir.

##### <a name="misaligned-main-account-categories"></a>Yanlış düzenlenmiş ana hesap kategorileri

Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürümü 7.2.1'den daha eski bir sürüm kullanıyorsanız, hesapları yeniden adlandırmanız ve hesapları hesap kategorileri arasında taşımanız durumunda veri reyonunu sıfırlamanız gerekebilir. Bu eylemler ana hesap kategorilerinin hatalı düzenlenmiş duruma gelmesine neden olabilir. **Yanlış düzenlenmiş ana hesap kategorileri** alanı, bu sorunla karşı karşıya olup olmadığınızı gösterir.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Finance and Operations Mali raporlama sürümü 7.2.6.0'da veri reyonunu sıfırlama

Finance and Operations Mali raporlama sürümü 7.2.6.0'da veya öncesinde veri reyonunu sıfırlamak için **Veri Reyonunu Sıfırla** iletişim kutusunda, **Veri reyonunu sıfırla** onay kutusunu ve ardından **Tamam**'ı seçin. Veri reyonunu yalnızca planlanmış bir kesinti sırasında sıfırlamanız gerekir.

[![Veri reyonunu sıfırla onay kutusu](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Microsoft Dynamics 365 for Finance and Operations Mali raporlama sürümü 7.3.0'da veri reyonunu sıfırlama ve bir neden seçme

Veri reyonunun sıfırlanmasının gerekli olduğunu belirlerseniz, **Veri reyonunu sıfırla** onay kutusunu işaretleyin ve sonra **Neden** alanından bir neden seçin. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Eksik veya yanlış veri** – İstatistiklere bağlı olarak, verilerin eksik olabileceğini saptadınız. Devam etmeden önce, temel nedeni belirlemek için Destek birimi ile birlikte çalışmanızı öneririz.
- **Veritabanını sıfırlama**  – Finance and Operations veri tabanı geri yüklendi ancak Mali raporlama veri reyonu için veritabanı geri yüklenmedi.
- **Diğer** – Veri reyonunu başka bir nedenle sıfırlıyorsunuz. Bir sorun olduğundan endişe duyuyorsanız, sorunu belirlemek için Desteğe başvurun.

> [!NOTE]
> Adımları tamamlamadan önce mevcut tüm görevlerin tümleştirme işlemlerini tamamladığını doğrulayın. Tümleştirme durumu **Araçlar** &gt; **Tümleştirme durumu**'nu seçerek görüntüleyebilirsiniz.

#### <a name="clear-users-and-companies"></a>Kullanıcıları ve şirketleri temizle

Veritabanınızı geri yüklediyseniz ancak daha sonra kullanıcılar veya şirketlerde değişiklik yaptıysanız **Kullanıcıları ve şirketleri temizle** onay kutusunu işaretleyin. Bu onay kutusunu çok nadir olarak işaretlemeniz gerekir.

Sıfırlama işlemini başlatmaya hazır olduğunuzda, **Tamam**'ı seçin. İşlemi başlatmak için hazır olduğunuzu onaylamanız istenir. Mali raporlamanın sıfırlama ve daha sonra oluşan ilk veri tümleştirme sırasında kullanılamayacağını unutmayın.

Tümleştirme durumunu gözden geçirmek isterseniz, tümleştirmenin en son çalıştırıldığı zamanı ve durumu görüntülemek için **Araçlar** &gt; **Tümleştirme durumu**'nu seçin.

[![Tümleştirmenin durumunu görüntüleme](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Finance and Operations Mali raporlama sürüm 7.0.10000.4 ve üstü için Mali raporlama veri reyonunu sıfırlama

Finance and Operations veritabanınızı bir yedekten kurtarırsanız veya veritabanını bir ortamdan diğerine kopyalarsanız, Mali raporlama veri reyonunun Finance and Operations veritabanını doğru kullandığından emin olmak için bu bölümdeki adımları izleyin.

> [!NOTE]
> Bu işlemdeki adımların Microsoft Dynamics AX uygulaması 7.0.1 (Mayıs 2016) sürümü (uygulama derlemesi 7.0.1265.23014 ve Mali raporlama derlemesi 7.0.10000.4) ve daha yeni sürümler için desteklendiğini unutmayın. Finance and Operations'ın önceki bir sürümüne sahipseniz, yardım için Destek ekibine başvurun.

### <a name="export-report-definitions"></a>Rapor tanımlarını dışa aktarma

İlk olarak, rapor tasarımlarını Rapor tasarımcısından aktarmak için bu adımları izleyin.

1. Rapor tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.
2. Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'ı seçin.

    > [!NOTE]
    > Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.

3. Dışa aktarılacak rapor tanımlarını seçin:

    - Tüm rapor tanımlarınızı ve ilişkili yapı taşlarını dışa aktarmak için **Tümünü Seç**'i seçin.
    - Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için, ilgili sekmeyi ve ardından dışa aktarılacak maddeleri seçin. Bir sekmede birden fazla öğeyi seçmek için Ctrl tuşunu basılı tutun. Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.

4. **Dışa Aktar**'ı seçin.
5. Bir dosya adı girin ve dışarı aktarılan rapor tanımlarını kaydetmek için istediğiniz güvenli bir konumu seçin.
6. **Kaydet**'i seçin.

Dosyayı güvenli bir konuma kopyalayabilir veya yükleyebilirsiniz. Bu şekilde, dosya daha sonra farklı bir ortama alınabilir. Microsoft Azure depolama hesabını kullanma hakkındaki daha fazla bilgi için bkz. [AzCopy Komut Satırı Yardımcı Programı ile veri transferi](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft, Finance and Operations sözleşmenizin bir parçası olarak bir depolama hesabı sağlamaz. Bir depolama hesabı satın almanız veya ayrı bir Azure aboneliğine ait bir depolama hesabını kullanmanız gerekir.

> [!WARNING]
> Azure Sanal Makineler'de (VM) D sürücüsünün davranışını dikkate alın. Dışa aktarılan yapı taşı gruplarınızı kalıcı olarak D sürücüsünde depolamayın. Geçici sürücüler hakkında daha fazla bilgi için bkz. [Windows Azure Sanal Makinelerdeki geçici sürücüleri anlama](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Hizmetleri durdurma

Aşağıdaki Microsoft Windows hizmetlerinin Finance and Operations veritabanına açık bağlantıları olacaktır. Bu nedenle, ortamdaki tüm bilgisayarlara bağlanmak ve services.msc'yi kullanarak bu hizmetleri durdurmak için Microsoft Uzak Masaüstü'nü kullanmanız gerekir:

- World wide web publishing service (tüm Uygulama Nesnesi Sunucuları [AOS] bilgisayarlarda)
- Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)
- Management Reporter 2012 İşlem Hizmeti (yalnızca İş zekası [BI] bilgisayarlarınızda)

### <a name="reset"></a>Sıfırla

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>En güncel MinorVersionDataUpgrade.zip paketini indirin.

En güncel MinorVersionDataUpgrade.zip paketini indirin. Veri yükseltme paketinin doğru sürümünü bulma ve indirme ile ilgili yönergeler için bkz. [En son veri yükseltme dağıtılabilir paketini indirme](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). MinorVersionDataUpgrade.zip paketini indirmek için bir yükseltme gerekli değildir. Bu nedenle, bu konudaki "En son veri yükseltme dağıtılabilir paketini indirme" bölümündeki adımları izlemeniz yeterlidir. Konu içindeki tüm diğer adımları atlayabilirsiniz.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Finance and Operations veritabanı için komut dosyalarını çalıştırma

Aşağıdaki komut dosyalarını Finance and Operations veritabanı için çalıştırın (Mali raporlama veritabanı için değil):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Bu komut dosyaları kullanıcıların, rollerin ve değişiklik izleme ayarlarının doğru olmasını sağlamaya yardımcı olur.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Veritabanı sıfırlamak için bir Windows PowerShell komutu çalıştırma

AOS bilgisayarda Microsoft Windows PowerShell'i yönetici olarak başlatın ve Finance and Operations ve Mali raporlama tümleştirmesini sıfırlamak için aşağıdaki komutları çalıştırın.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

**Reset-DatamartIntegration** komutundaki parametrelerin açıklamasını aşağıda bulabilirsiniz:

- **-Reason** için geçerli değeler şunlardır: **SERVICING**, **BADDATA** ve **OTHER**.
- **-ReasonDetail** parametresi serbest metindir.
- Neden ve neden ayrıntısı telemetri/ortam izlemede kaydedilecektir.

> [!NOTE]
> Komutları çalıştırıldıktan sonra **Y** girerek veritabanını sıfırlamak istediğinizi onaylamanız istenir.

#### <a name="restart-services"></a>Hizmetleri yeniden başlatma

Daha önce durdurduğunuz hizmetleri yeniden başlatmak için services.msc'yi kullanın:

- World wide web publishing service (tüm AOS bilgisayarlarda)
- Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)
- Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)

#### <a name="import-report-definitions"></a>Rapor tanımlarını içe aktarma

Rapor tasarımcısındaki rapor tasarımlarınızı dışa aktarma sırasında oluşturulan dosyayı kullanarak içe aktarın.

1. Rapor tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.
2. Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'ı seçin.

    > [!NOTE]
    > Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.

3. **Varsayılan** yapı bloğunu seçin ve **İçe Aktar**'ı seçin.
4. Dışa aktarılan rapor tanımlarını içeren dosyayı ve ardından **Aç**'ı seçin.
5. **İçe Aktar** iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:

    - Tüm rapor tanımlarını ve ilişkili yapı taşlarını içe aktarmak için **Tümünü Seç**'i seçin.
    - Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.

6. **İçe aktar**'ı seçin.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Finance and Operations (şirket içi) için Mali raporlama veri reyonunu sıfırlama

1. Tüm kullanıcılardan Rapor Tasarımcısı'ndan ve Finance and Operations'ın Mali raporlama alanından çıkmalarını isteyin.
2. Mali raporlama veritabanında (MRDB) aşağıdaki komut dosyasını çalıştırın.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Finance and Operations veritabanındaki (AXDB) FINANCIALREPORTS tablosundan tüm kayıtları kesin veya silin.
4. Tablo Finance and Operations veritabanında varsa, FINANCIALREPORTVERSION tablosundan tüm kayıtları kesin veya silin. Tablo Finance and Operations veritabanında yoksa bu adımı atlayın.
5. Mali raporlama veritabanı için **ResetDatamart.sql** komut dosyasını çalıştırın. Bu komut dosyası veri merkezi tümleştirmesini devre dışı bırakır, tüm veri merkezi verilerini siler ve veri reyonu tümleştirmesini yeniden etkinleştirir.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Sıfırlamadan sonra, Finansal raporlama veritabanı için aşağıdaki sorguyu çalıştırarak verileri yeniden yüklemeyi el ile doğrulayabilirsiniz.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Tüm satırların **LastRunTime** değerine sahip olduğunu ve **StateType** değerinin **5** olarak ayarlandığını doğrulayın. **5** olarak ayarlanan **StateType** değeri verilerin başarılı şekilde yüklendiğini gösterir.  **7** değeri hatalı bir durumu gösterir. Bazı durumlarda, Kuruluş Hiyerarşisi eşlemesi ilk kez çalıştığında bu duruma sahip olur. Bununla birlikte, hatalı durum otomatik olarak giderilmelidir.

