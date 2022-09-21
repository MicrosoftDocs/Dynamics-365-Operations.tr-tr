---
title: Öneriler için alternatif bir veri akışı ayarlama
description: Bu makalede, öneriler hizmetine veri sağlamak için alternatif bir veri akışı kullanarak bir ortamın nasıl yapılandırılacağı açıklanmaktadır.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460172"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Öneriler için alternatif bir veri akışı ayarlama

[!include [banner](includes/banner.md)]

Bu makalede, öneriler hizmetine veri sağlamak için alternatif bir veri akışı kullanarak bir ortamın nasıl yapılandırılacağı açıklanmaktadır.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Kullanıma hazır veri akışının alternatif veri akışıyla karşılaştırılması

Aşağıdaki çizimde, bir ortamdaki kullanıma hazır veri akışı gösterilmektedir.

![Bir ortamda kullanıma hazır veri akışı](media/reco-out-of-the-box-dataflow-2.png)

Aşağıdaki çizimde, varlık deposu eşitleme toplu işinin alternatif veri akışı adımlarıyla değiştirildiği alternatif bir veri akışı gösterilmektedir.

![Bir ortamda alternatif veri akışı](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Varsayımlar

- Bu makalede, ortamınız için öneriler hizmetini zaten etkinleştirdiğiniz varsayılmaktadır. Daha fazla bilgi için bkz. [Ürün önerilerini etkinleştirme](enable-product-recommendations.md).
- Microsoft Azure Data Lake Storage hesabındaki dosya ve klasörlerle çalışırken:

    - Azure web portalı arabirimini veya Azure Depolama Gezgini uygulamasını kullanabilirsiniz.
    - Dosya ve klasörlerle çalışmanın başlangıç noktaları, ortam URL'nizle eşleşecek şekilde adlandırılan klasörün altında bulunan **dynamics365-financeandoperations** kapsayıcısındadır.
    - Korumalı alan ortamınızın adı **MyUAT** ise ortam temel URL'si `myuat.sandbox.operations.dynamics.com` olur.
    - Aynı depolama hesabına birden fazla ortam bağlıysa her ortamın kendi kök klasörü olur.

## <a name="prerequisites"></a>Ön Koşullar

Alternatif veri akışı yaklaşımını uygulayabilmeniz için aşağıdaki ön koşulların karşılanması gerekir.

### <a name="set-up-microsoft-power-platform"></a>Microsoft Power Platform ayarla

Microsoft Power Platform'u ayarlamak için [Microsoft Power Platform tümleştirmesini etkinleştirme](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) yönergeleri izleyin.

### <a name="install-the-export-to-data-lake-add-in"></a>Data Lake'e Dışarı Aktarma eklentisini yükleme

Data Lake'e Dışarı Aktarma eklentisini yüklemek için [Azure Data Lake'e Dışarı Aktarma eklentisini yükleme](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) bölümündeki yönergeleri izleyin.

> [!NOTE]
> Yapılandırma değerlerini not edin çünkü aşağıdaki adımlardan bazıları için bunlara ihtiyacınız olacaktır.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Dynamics 365'te dışarı aktarılacak tabloları yapılandırma

Dynamics 365'ten Azure Data Lake Storage'a tablo eşitlemesi, **Data Lake'e Dışarı Aktar** sayfasından yönetilir. Bu sayfanın şu anda bir menü öğesi olmadığından, yalnızca **Sistem Yöneticisi** güvenlik rolündeki kullanıcılar sayfayı açabilir.

Dynamics 365'te dışarı aktarılacak tabloları yapılandırmak için aşağıdaki adımları izleyin.

1. **Data Lake'e Dışarı Aktar** sayfasını açmak için `?mi=DataFeedsDefinitionWorkspace` dizesini aşağıdaki örnekte gösterildiği gibi ortamın temel URL'sine ekleyin:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. **Data Lake'e Dışarı Aktar** sayfasında, bu makalenin [RetailSales küp tabloları listesi](#list-of-retailsales-cube-tables) bölümünde listelenen tabloları kopyalayın.
1. **Sistem Adı** sütununda, filtre seçenekleri listesini genişletin.
1. Filtre türü için aşağıdakilerden **birini** seçin. Ardından imleci metin kutusuna getirin ve **Data Lake'e Dışarı Aktar** sayfasından kopyaladığınız tabloların listesini yapıştırın.
1. Filtre seçenekleri listesinin en altındaki **Uygula**'yı seçin.
1. Kılavuzdaki tüm satırları seçin ve ardından **Etkinleştir**'i seçin.

> [!NOTE]
> Sonraki adıma geçmeden önce, tüm satırların **Çalışıyor** durumuna güncelleştirilmesi gerekir. Hataları gerektiği gibi giderin ve çözün.

### <a name="create-a-synapse-workspace"></a>Synapse çalışma alanı oluşturma

Henüz bir Synapse çalışma alanınız yoksa oluşturmak için [Hızlı Başlangıç: Synapse çalışma alanı oluşturma](/azure/synapse-analytics/quickstart-create-workspace) bölümündeki yönergeleri izleyin.

Azure kaynaklarınızı düzenli tutmak için Data Lake Storage hesabını ve Synapse çalışma alanını Azure'daki bir kaynak grubunda bir araya getirmenizi öneririz. Data Lake'e Dışarı Aktar eklentisini yüklediğinizde oluşturduğunuz depolama hesabını yeniden kullanabilirsiniz.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Öneri verilerini işlemek için Synapse'te veritabanı oluşturma

Common Data Model yardımcı program konsol uygulamasını (CDMUtil_ConsoleApp) kullanarak Synapse çalışma alanınızda bir veritabanı oluşturun ve bunu Data Lake Storage'daki Common Data Model tablolarından doldurun. Herhangi bir uzantı olması ihtimaline karşı, Common Data Model yardımcı programını veritabanınızla birlikte bir geliştirme ortamında kullanmanızı öneririz.

> [!NOTE]
> Aşağıdaki adımlarda, RetailSales küpüne hiçbir uzantı verisi eklenmediği varsayılmaktadır.

Synapse'ta veritabanı oluşturmak için aşağıdaki adımları izleyin.

1. [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app)'a gidin ve **CDMUtilConsoleApp.zip** dosyasını indirmek için adımları izleyin.
1. Sıkıştırılmış dosyayı yerel bir klasöre çıkarın.
1. **CDMUtil_ConsoleApp.dll.config** dosyasını bir metin düzenleyicisinde açın ve aşağıdaki değerleri güncelleştirin:

    1. **Kiracı Kimliği** değerini (Azure kiracı kimliği) ayarlayın.
    1. **Erişim anahtarı** değerini (Data Lake Storage hesabının erişim anahtarı) ayarlayın.

        1. Azure portalında depolama hesabınızı açın.
        1. Sayfanın sol tarafındaki menüden **Erişim anahtarları**'nı seçin.
        1. Sayfanın üst kısmında **Anahtarları göster**'i seçin.
        1. İki anahtar alanından biri için kopyala düğmesini seçin ve ardından değeri yapılandırma dosyasındaki çift tırnak işaretleri arasına yapıştırın.

    1. **ManifestURL** değerini Azure Data Lake Storage'daki **Tables.manifest.cdm.json** dosyanızın URL'sine ayarlayın. URL'yi edinmek için Azure portalında dosyaya gidin, görünümün sağ tarafındaki üç noktayı (**...**) seçin ve ardından **Özellikler**'i seçin. URL, **Genel Bakış** sekmesinde gösterilen ilk özelliktir.
    1. **TargetDbConnectionString** değerini, Synapse çalışma alanınızın yerleşik sunucusuz SQL havuzu için bağlantı dizesine ayarlayın.

        1. Synapse çalışma alanında **Yönet** sekmesini seçin.
        1. Alt menüde **SQL havuzları**'nı seçin.
        1. Havuzun özelliklerini görüntülemek için **Yerleşik** adını seçin.
        1. Özellikler iletişim kutusunda, kullanmak istediğiniz ADO.NET bağlantı türünü seçin. Ardından bağlantı dizesi değerini kopyalayın ve yapılandırma dosyasındaki çift tırnak işaretleri arasına yapıştırın.

        > [!NOTE]
        > Veritabanı oluşturma izninizin olması gerekir. Kullanım kolaylığı için yerleşik **sqladminuser** yönetici hesabını kullanabilirsiniz.

    1. **ProcessEntities** düğümünün açıklamasını kaldırın ve değerini **doğru** olarak ayarlayın (örneğin `<add key="ProcessEntities" value ="true"/>`).

1. **CDMUtil_ConsoleApp.dll.config** dosyasını kaydedip kapatın.
1. **EntityList.json** dosyasını **/Manifest** dizinine kopyalayın.
1. Bir komut istemi penceresinde, **cdmutil_consoleapp.exe** dosyasını çalıştırın.

> [!NOTE]
> Çıktıyı incelediğinizde, 35 varlık/görünüm, en az 75 tablo olmalı ve hata olmamalıdır.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Data Lake RetailSales Toplam Ölçümleri dizinini hazırlama

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Geçerli RetailSales küpü verilerinizi Data Lake Storage'dan yedekleme

Geçerli RetailSales küpü verilerinizi yedeklemenin en kolay yolu, Data Lake Storage **RetailSales-backup** veya benzeri bir yerdeki **RetailSales** dizinini yeniden adlandırmaktır. Bu yöntem, daha sonra sorun gidermenin gerekli olması durumunda mevcut verileri korur.

**/RetailSales** küp klasörü aşağıdaki konumda bulunabilir:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Yeni bir RetailSales klasörü oluşturma ve model dosyasını yükleme

Yeni bir **RetailSales** dizini oluşturmak ve **model.json** dosyasını Data Lake Storage'a yüklemek için aşağıdaki adımları izleyin.

1. Önceki dizinle aynı düzeyde yeni bir boş dizin oluşturun ve bunu **RetailSales** olarak adlandırın.
1. **Model.json** dosyasını yeni dizine yükleyin.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>RetailSales küpü verilerini kopyalamak için işlem hattı oluşturma

İşlem hattı, RetailSales küp görünümlerini okur ve verileri Data Lake Storage'daki .csv dosyalarına aktarır.

RetailSales küpü verilerini kopyalamak üzere bir işlem hattı oluşturmak için aşağıdaki adımları izleyin.

1. Synapse çalışma alanında, **Tümleştir** sekmesini seçin.
1. Artı işaretini (**+**) ve ardından **İşlem hattı şablonundan içeri aktar**'ı seçin.
1. [ExportRetailSalesCubeViews.zip dosyasını](https://aka.ms/reco-alternate-dataflow-files) indirin ve seçin.
1. SQL veritabanı bağlı hizmetinizi seçin.
1. Depolama hesabı bağlı hizmetinizi seçin.
1. **Verileri Kopyala** aracını açın ve **Klasör yolu** özelliğini **\<environment_name\>/...** olarak değiştirin.

### <a name="test-execution-of-the-pipeline"></a>İşlem hattının yürütülmesini test etme

İşlem hattını yalnızca bir görünüm kullanarak test etmenizi öneririz. **RetailSales_RetailMediaTemplateView** görünümü genellikle 10'dan az satır içerdiğinden iyi çalışır.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>İşlem hattını yinelenen bir zamanlamada çalışacak şekilde planlama

İşlem hattı her çalıştığında Azure tüketimi gerçekleşir. Yürütmeleri 48 saat veya daha uzun aralıklarla zamanlamanızı öneririz. Verileri hemen eşitlemeniz gerekiyorsa işlem hattını her zaman el ile çalıştırabilirsiniz. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Dynamics 365'ten Data Lake Storage'a eşitleme için tablo listesi

Aşağıdaki tablo listesi, tüm RetailSales küpü için gerekli olan tüm tabloların bir alt kümesidir. RetailSales küpündeki görünümlerin yalnızca 15'i öneriler hizmeti tarafından kullanılır ve gerekli tabloların listesi buna göre filtrelenir.

### <a name="list-of-retailsales-cube-tables"></a>RetailSales küp tablolarının listesi

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Katalog
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Synapse işlem hattına aktarılacak parametre listesini görüntüleme

Aşağıdaki virgülle ayrılmış liste, işlem hattının üzerinde "seç" işlemi gerçekleştireceği RetailSales küp görünümlerini içerir. Daha sonra sonuçları Data Lake Storage'a kopyalar.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> İşlem hattı parametresi, tek virgülle ayrılmış görünüm adlarının bir listesi olmalıdır. Boşluk veya satır besleme olmamalıdır.

## <a name="environment-specific-fixes"></a>Ortama özgü düzeltmeler

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW düzeltmesi

**RETAILCHANNELVIEW** görünümü, "perakende kanalı" türündeki bir kuruluşu temsil eden sabit kodlanmış bir tamsayı içerir. Türün gerçek değeri ortamdan ortama veya kiracıdan kiracıya değişebilir.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Sabit kodlanmış tamsayıyı güncelleştirmek için şu adımları izleyin.

1. Dynamics 365'te, çevrimiçi kanalınız için **ChannelID** değerini arayın.
1. Synapse veritabanına bağlı bir SQL Server Management Studio (SSMS) örneğinde, aşağıdaki sorguyu çalıştırın.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. İlk sütundaki (**INSTANCERELATIONTYPE)** değeri kopyalayın ve görünüm tanımına yapıştırın.

## <a name="troubleshooting"></a>Sorun Giderme

### <a name="pipeline-task-fails"></a>İşlem hattı görevi başarısız oluyor

**CopyData** görevi için 15 işlem hattı görevi yürütmesi olmalıdır. Herhangi bir yürütme başarısız olursa tüm bağımlı SQL nesnelerinin var olduğunu ve sorguların çalıştığını doğrulamanız gerekir. Tüm bağımlılıklara ulaşmanın en kolay yolu, veritabanına bağlanmak için SSMS kullanmaktır. Daha sonra bir görünümü seçip basılı tutabilir (veya sağ tıklayabilir) ve **Yeni bir pencereye göre CREATE oluştur**'u seçebilirsiniz.

Hata iletisi aşağıdaki metni içerebilir:

- Hata: "Kaynak" tarafında hata oluştu
- Harici dosya işlemede hata: "Maksimum hata sayısı".
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Örnek senaryo

Bu örnekte, **RetailSales_RetailProductCategory** görevi başarısız olur ve "Maksimum hata sayısı" hatası alırsınız.

Bu hatayı ayıklamak için şu adımları izleyin.

1. **EntityList.json** dosyasını bir metin düzenleyicisinde açın (örneğin, Visual Studio Code).
1. **RetailSales_RetailProductCategory** için görünüm tanımını bulun.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Bu görünüm yalnızca bir başka görünüme bağlıdır: **RetailProductCategoryView** _. _*RetailProductCategoryView** için görünüm tanımını bulun.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Bu görünüm üç diğer görünüme bağlıdır: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** ve **RETAILCATEGORYEXPANDED**. Bu görünümlerin her birinin tanımını bulun ve bağımlılıklarını listeleyin. Tüm bağımlı görünümleri bulana kadar devam edin.

    Bağımlılık ağacı sırasına göre tüm liste burada verilmiştir. On üç görünüm doğrulanmalıdır.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. Excel'de, aşağıdaki 13 **select count(\*) from \<view_name\>** ifadesini oluşturun. Bu ifadeleri SSMS'de çalıştırın ve sonuçları metne gönderin. Ardından, görünümlerden herhangi birinin başarısız olup olmadığını görmek için sonuçlar arasında gezinin. İlk hata, görünümlerden en az birinin başarısız olacağını gösteriyor.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Baktığınız şeyi doğrulamanın bir yolu, SSMS'de görünüm tanımını oluşturmak için köke bağımlı bir görünüm oluşturmaktır. Ardından, **r.filepath** adlı bir Azure Data Lake dosya sütunu olduğunu doğrulayın. Bu sütunun varlığı, incelemekte olduğunuz görünümün Data Lake Storage'dan veri okuduğunu gösterir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
