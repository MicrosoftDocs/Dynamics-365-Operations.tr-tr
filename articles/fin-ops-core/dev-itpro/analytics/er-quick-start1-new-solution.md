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
ms.openlocfilehash: 986beb6d46ac69192206c86fc3660c2e2345d6a9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743739"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Özel rapor yazdırmak için yeni bir ER çözümü tasarlama

[!include[banner](../includes/banner.md)]

Aşağıdaki adımlarda Sistem Yöneticisi, Elektronik Raporlama Geliştiricisi veya Elektronik Raporlama İşlevsel Danışmanı rolüne sahip bir kullanıcının ER çerçevesinin parametrelerini nasıl yapılandırabileceği, belirli bir iş etki alanının verilerine erişmek için yeni bir ER çözümünün gerekli ER yapılandırmalarını nasıl tasarlayabileceği ve nasıl Microsoft Office biçiminde özel rapor oluşturabileceği açıklanmaktadır. Bu adımlar **USMF** şirketinde gerçekleştirilebilir.

- [ER altyapısını yapılandırma](#ConfigureFramework)

    - [ER parametrelerini yapılandırma](#ConfigureParameters)
    - [ER yapılandırma sağlayıcısı etkinleştirin](#ActivateProvider)

        - [ER yapılandırma sağlayıcıları listesini gözden geçirin](#ReviewProvidersList)
        - [Yeni bir ER yapılandırması sağlayıcısı ekleme](#AddProvider)
        - [ER yapılandırma sağlayıcısı etkinleştirin](#ActivateAddedProvider)

- [Etki alanına özel veri modeli tasarlama](#DesignModel)

    - [Yeni bir veri modeli yapılandırmasını içe aktarma](#ImportDataModel)
    - [Yeni bir veri modeli yapılandırması oluşturun](#DesignDataModel)

        - [Veri modelini adlandırma](#NameDataModel)
        - [Veri modeli alanları ekleme](#FieldsEntry)
        - [Veri modelinin tasarımını tamamlama](#CompleteDataModel)

- [Yapılandırılan veri modeli için bir model eşlemesi tasarlama](#DesignMapping)

    - [Yeni bir model eşlemesi yapılandırmasını içe aktarma](#ImportModelMapping)
    - [Yeni model eşleme yapılandırması oluşturma](#CreateModelMapping)

        - [Yeni bir model eşleme bileşeni tasarlama](#DesignMappingComponent)
        - [Uygulama tablolarına erişmek için veri kaynakları ekleme](#AddMmDataSource1)
        - [Uygulama numaralandırmalarına erişmek için veri kaynakları ekleme](#AddMmDataSource2)
        - [Belirtilen dilde rapor oluşturmak için ER etiketleri ekleme](#AddMmLabels)
        - [Numaralandırma değerlerini karşılaştırma sonuçlarını bir metin değerine dönüştürmek için veri kaynağı ekleme](#AddMmDataSource3)
        - [Veri modeli alanlarına veri kaynakları bağlama](#AddMmBindings1)
        - [Model eşleme tasarımını tamamlama](#CompleteModelMapping)

- [Özel rapor için şablon tasarlama](#DesignReportTemplate)
- [Bir biçim tasarlama](#DesignFormat)

    - [Tasarlanan biçim yapılandırmasını içe aktarma](#FormatImport)
    - [Yeni bir biçim yapılandırması oluşturma](#FormatCreate)

        - [Rapor şablonunu içe aktarma](#ImportReportTemplate)
        - [Biçim yapılandırma](#ConfigureFormat)
        - [Rapor başlığı için veri bağlamayı tanımlama](#DefineFormatBindings)
        - [Model veri kaynağını gözden geçirme](#ReviewModelDataSource)
        - [Biçim öğelerini veri kaynağı alanlarına bağlama](#BindFormatElements)

    - [ER'den tasarlanan biçim çalıştırma](#RunFormatFromER)

- [Tasarlanan biçimi ayarlama](#TuneFormat)

    - [Oluşturulan belgenin adını değiştirmek için bir biçimi değiştirme](#ModifyToChangeName)
    - [Soruların sırasını değiştirmek için bir biçimi değiştirme](#ModifyToOrder)
    - [ER'den değiştirilmiş biçim çalıştırma](#RunFormatFromER2)
    - [Biçim tasarımını tamamlama](#CompleteFormat)

- [Tasarlanan raporu çağırmak için uygulama artefaktları geliştirme](#DevelopCustomCode)

    - [Kaynak kodu değiştir](#ModifySourceCode)

        - [Veri sözleşmesi sınıfı ekleme](#DataContractClass)
        - [UI oluşturucu sınıfı ekleme](#UIBuilderClass)
        - [Veri sağlayıcı sınıfı ekleme](#DataProviderClass)
        - [Etiket dosyası ekleme](#LabelsFile)
        - [Rapor hizmeti sınıfı ekleme](#ServiceClass)
        - [Rapor denetleyicisi sınıfı ekleme](#ControllerClass)
        - [Menü öğesi ekleme](#MenuItem)
        - [Menüye menü öğesi ekleme](#Menu)
        - [Visual Studio projesi oluşturma](#BuildVSProject)

    - [Uygulamadan bir biçim çalıştırma](#RunFormatFromApp)

- [Tasarlanan ER çözümünü ayarlama](#TuneSolution)

    - [Model eşlemesini değiştirme](#ModifyModelMapping)

        - [Veri sözleşmesi nesnesine erişmek için veri kaynakları ekleme](#AddDataSource1)
        - [ER biçim eşleme kayıtlarına erişmek için veri kaynağı ekleme](#AddDataSource2)
        - [Çalışan bir ER biçimin biçim eşleme kaydına erişmek için veri kaynağı ekleme](#AddDataSource3)
        - [Çalışan ER biçiminin adını veri modeline girme](#AddBinding)
        - [Model eşleme tasarımını tamamlama](#CompleteModelMapping2)

    - [Biçim değiştirme](#ModifyFormat)

        - [Yeni bir biçim öğesi ekleme](#AddFormatElement)
        - [Eklenen biçim öğesini bağlama](#BindAddedFormatElement)
        - [Biçim tasarımını tamamlama](#CompleteFormat2)

    - [Uygulamadan bir biçim çalıştırma](#RunFormatFromApp2)
    - [ER'den bir biçim çalıştırma](#RunFormatFromER3)
    - [Ekran önizleme için biçim hedefi yapılandırma](#ConfigureDestination)
    - [PDF belgesi olarak önizlemek için uygulamadan bir biçim çalıştırma](#RunFormatFromApp3)

- [Ek kaynaklar](#References)

Bu örnekte, [Soru formu](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) modülü için yeni bir ER çözümü oluşturacaksınız. Bu yeni ER çözümü, bir Microsoft Excel çalışma sayfasını şablon olarak kullanarak rapor tasarlamanıza olanak tanır. Daha sonra, mevcut SQL Server Reporting Services (SSRS) raporunu oluşturmaya ek olarak, **Soru formu** raporunu Excel veya PDF biçiminde oluşturabilirsiniz. Ayrıca, yeni raporu daha sonra istek üzerine değiştirebilirsiniz. Kodlama gerekmez.

1. Mevcut raporu çalıştırmak için **Soru formu** \> **Tasarım** \> **Soru formları raporu**'na gidin.

    ![Mevcut SSRS raporunu çalıştırmak için Soru Formu modülündeki Soru formları raporu menü öğesini seçme](./media/er-quick-start1-application-menu-origin.png)

2. **Soru formları raporu** iletişim kutusunda seçim ölçütü belirtin. Rapor yalnızca **SBCCrsExam** soru formunu içerecek şekilde filtre uygulayın.

    ![Soru formları raporu iletişim kutusunda seçim ölçütü belirtme](./media/er-quick-start1-ssrs-report-dialog.png)

Aşağıdaki şekilde **SBCCrsExam** soru formu için oluşturulan SSRS raporu sürümü gösterilmektedir.

![Oluşturulan SSRS raporu](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>ER altyapısını yapılandırma

Elektronik Raporlama Geliştiricisi rolüne sahip bir kullanıcı olarak, yeni ER çözümünüzü tasarlamak için ER çerçevesini kullanmaya başlamak için minimum ER parametleri kümesini yapılandırmanız gerekir.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>ER parametrelerini yapılandırma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısını seçin.
3. **Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.
4. **Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:

    - **Yapılandırmalar** alanını, **USMF** şirketi için **Dosya** olarak ayarlayın.
    - **İş arşivi**, **Geçici**, **Temel** ve **Diğer** alanlarını **Dosya** olarak ayarlayın.

ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

Her ER yapılandırması bir ER yapılandırma sağlayıcısı tarafından sahiplenildi olarak işaretlenir. Bu nedenle, ER yapılandırmalarını eklemeye veya düzenlemeye başlamadan önce, **Elektronik raporlama** çalışma alanında bir ER yapılandırma sağlayıcısını etkinleştirmelisiniz.

> [!NOTE]
> Yalnızca ER yapılandırmasının sahibi bunu düzenleyebilir. Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>ER yapılandırma sağlayıcıları listesini gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Elektronik raporlama** çalışma alanında, **İlgili bağlantılar**  bölümünde, **Yapılandırma sağlayıcıları**'nı seçin.
3. **Yapılandırma sağlayıcıları** sayfasında, her yapılandırma sağlayıcı kaydının benzersiz bir adı ve URL'si vardır. Bu sayfanın içeriğini gözden geçirin. **Litware, Inc.** (`https://www.litware.com`) için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleyin](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Yeni bir ER yapılandırması sağlayıcısı ekleme

1. **Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.
2. **Ad** alanına **Litware, Inc.** yazın.
3. **İnternet adresi** alanına `https://www.litware.com` girin.
4. **Kaydet**'i seçin.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Elektronik raporlama** çalışma alanında, **Litware, Inc.** yapılandırma sağlayıcısını seçin.
3. **Etkin olarak ayarla**'ya tıklayın.

ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Etki alanına özel veri modeli tasarlama

**Soru formu** iş etki alanı için [veri modeli](general-electronic-reporting.md#data-model-and-model-mapping-components) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bu veri modeli daha sonra **Soru formu** raporu oluşturmak üzere bir ER biçimi tasarlarken veri kaynağı olarak kullanılacaktır.

[Yeni veri modeli yapılandırmasını içe aktarma](#ImportDataModel) bölümündeki adımları izleyerek gerekli veri modelini sağlanan XML dosyasından içe aktarabilirsiniz. Alternatif olarak, bu veri modelini sıfırdan tasarlamak için [Yeni veri modeli yapılandırması oluştur](#DesignDataModel) bölümündeki adımları tamamlayabilirsiniz.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Yeni bir veri modeli yapılandırmasını içe aktarma

1. [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Questionnaires model.version.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

Devam etmek için sonraki yordamı atlayın, [Yeni bir veri modeli yapılandırması oluşturma](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Yeni bir veri modeli yapılandırması oluşturun

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
3. **Yapılandırma oluştur**'u seçin.
4. Açılır menüdeki iletişim kutusunda, **Ad** alanına **Soru formu modeli** girin.
5. Yapılandırma oluşturmak için **Yapılandırma oluştur**'u seçin.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Veri modelini adlandırma

1. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.
2. **Tasarımcı**’yı seçin.
3. **Veri modeli tasarımcısı** sayfasında, **Genel** hızlı sekmesinde, **Ad** alanına <a name="DataModeName"></a>**Soru formları** girin.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Yeni veri modeli alanları ekleme

1. **Veri modeli tasarımcısı** sayfasında **Yeni**'yi seçin.
2. Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. Yeni düğümün türü olarak **Model kökü**'nü seçin.
    2. **Ad** alanına, <a name="RootDefinitionName"></a>**Kök** girin.
    3. Yeni düğüm eklemek için **Ekle**'ye tıklayın.

    Bu kök tanımlayıcısı, **Soru formu** raporuna veri sağlamak için kullanılacaktır. Tek bir veri modeli birden çok tanımlayıcıya sahip olabilir. Her bir tanımlayıcı, tek bir ER biçimi için, raporu oluşturmak üzere gereken verileri tanımlamak amacıyla belirtilebilir.

3. Tekrar **Yeni**'yi seçin ve veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. Yeni düğümün türü olarak **Etkin bir düğümün alt öğesi**'ni seçin.
    2. **Ad** alanına, **CompanyName** girin.
    3. **Madde türü** alanında **Dize**'yi seçin.
    4. Yeni alan eklemek için **Ekle**'yi seçin.

    Bu alan, geçerli şirketin adını bu veri modelini veri kaynağı olarak kullanan bir ER raporuna geçirmek için gereklidir.

4. Tekrar **Yeni**'yi seçin ve veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. Yeni düğümün türü olarak **Etkin bir düğümün alt öğesi**'ni seçin.
    2. **Ad** alanına, **Soru formu** girin.
    3. **Madde türü** alanında **Kayıt listesi**'ni seçin.
    4. Yeni alan eklemek için **Ekle**'yi seçin.

    Bu alan, soru formları listesini bu veri modelini veri kaynağı olarak kullanan bir ER raporuna geçirmek için kullanılır.

5. **Soru formu** düğümünü seçin.
6. Aşağıdaki veri modeli yapısını tamamlayana kadar düzenlenebilir veri modeli için gerekli alanları aynı şekilde eklemeye devam edin.

    | Alan yolu                                                    | Veri türü   | Alan ataması/iade edilen değer |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Kök                                                          |             | Soru formu verilerini istemek için referans noktası. |
    | Kök\\CompanyName                                             | Dize      | Geçerli şirketin adı. |
    | Kök\\ExecutionContext                                        | Kaydet      | Biçim yürütme ayrıntıları. |
    | Kök\\ExecutionContext\\FormatName                            | Dize      | Çalıştırılmakta olan ER biçiminin adı. |
    | Kök\\Soru formu                                           | Kayıt listesi | Soru formları listesi |
    | Kök\\Soru formu\\Etkin                                   | Dize      | Geçerli soru formunun durumu. |
    | Kök\\Soru formu\\Kod                                     | Dize      | Geçerli soru formunun kodu. |
    | Kök\\Soru formu\\Açıklama                              | Dize      | Geçerli soru formunun açıklaması. |
    | Kök\\Soru formu\\QuestionnaireType                        | Dize      | Geçerli soru formunun türü. |
    | Kök\\Soru formu\\QuestionnaireOrder                            | Dize      | Geçerli soru formunun sayısal sırası. |
    | Kök\\Soru formu\\ResultsGroup                             | Kaydet      | Geçerli soru formunun sonuç parametreleri. |
    | Kök\\Soru formu\\ResultsGroup\\Kod                       | Dize      | Geçerli sonuç grubunun tanımlama kodu. |
    | Kök\\Soru formu\\ResultsGroup\\Açıklama                | Dize      | Geçerli sonuç grubunun açıklaması. |
    | Kök\\Soru formu\\ResultsGroup \\MaxNumberOfPoints          | Gerçek        | Kazanılabilecek en fazla puan sayısı. |
    | Kök\\Soru formu\\Soru                                 | Kayıt listesi | Geçerli soru formu için soruların listesi. |
    | Kök\\Soru formu\\Soru\\CollectionSequenceNumber       | Tamsayı     | Geçerli yanıt koleksiyonunun sıra numarası. |
    | Kök\\Soru formu\\Soru\\Kod                             | Dize      | Geçerli sorunun tanımlama kodu. |
    | Kök\\Soru formu\\Soru\\MustBeCompleted                | Dize      | Geçerli sorunun yanıtlanıp yanıtlanmaması gerektiğini belirten bayrak. |
    | Kök\\Soru formu\\Soru\\PrimaryQuestion                | Dize      | Geçerli sorunun birincil olup olmadığını belirten bayrak. |
    | Kök\\Soru formu\\Soru\\SequenceNumber                 | Tamsayı     | Geçerli sorunun sıra numarası. |
    | Kök\\Soru formu\\Soru\\Metin                           | Dize      | Geçerli sorunun metni. |
    | Kök\\Soru formu\\Soru\\Yanıt                         | Kayıt listesi | Geçerli soru için yanıtların listesi. |
    | Kök\\Soru formu\\Soru\\Yanıt\\CorrectAnswer          | Dize      | Geçerli yanıtın doğru olup olmadığını belirten bayrak. |
    | Kök\\Soru formu\\Soru\\Yanıt\\Puanlar                 | Gerçek        | Geçerli yanıt seçildiğinde kazanılan puanlar. |
    | Kök\\Soru formu\\Soru\\Yanıt\\SequenceNumber         | Tamsayı     | Geçerli yanıtın sıra numarası. |
    | Kök\\Soru formu\\Soru\\Yanıt\\Metin                   | Dize      | Geçerli yanıtın metni. |

    Aşağıdaki şekil, **Veri modeli tasarımcısı** sayfasındaki tamamlanan düzenlenebilir veri modelini gösterir.

    ![ER veri modeli tasarımcısında yapılandırılmış veri modeli](./media/er-quick-start1-model2.png)

7. Değişikliklerinizi kaydedin.
8. **Veri modeli tasarımcısı** sayfasını kapatın.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Veri modelinin tasarımını tamamlama

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.
3. **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.
4. **Durumu değiştir** \> **Tamamla**'yı seçin.

Bu yapılandırmanın sürüm 1 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi. Sürüm 1 artık değiştirilemez. Bu sürüm yapılandırılmış veri modeli içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir. Bu yapılandırma için sürüm 2 oluşturuldu ve **taslak** durumuna sahip. **Soru formu** veri modelini ayarlamak için bu sürümü düzenleyebilirsiniz.

![Yapılandırmalar sayfasındaki düzenlenebilir ER yapılandırmasının sürümleri](./media/er-quick-start1-model-configuration.png)

ER yapılandırmaları için sürüm oluşturma hakkında daha fazla bilgi için bkz. [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Yapılandırılan veri modeli, **Soru formu** iş etki alanının soyut gösterimidir ve Microsoft Dynamics 365 Finance'a özel artefaktlarla herhangi bir ilişki içermez.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Yapılandırılan veri modeli için bir model eşlemesi tasarlama

Elektronik Raporlama Geliştirici rolünde bir kullanıcı olarak, **Soru formu** veri modeli için bir [model eşleme](general-electronic-reporting.md#data-model-and-model-mapping-components) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bu bileşen Finance için yapılandırılmış veri modelini uyguladığı için, Finance'a özgüdür. Model eşleme bileşenini, yapılandırılan veri modelini çalışma zamanında uygulama verileriyle doldurmak için kullanılması gereken uygulama nesnelerini belirtecek şekilde yapılandırmanız gerekir. Bu görevi tamamlamak için, Finance'ta **Soru formu** iş etki alanının veri yapısı uygulama ayrıntılarını bilmeniz gerekir.

[Yeni model eşleme yapılandırmasını içe aktarma](#ImportModelMapping) bölümündeki adımları izleyerek gerekli model eşleme yapılandırmasını sağlanan XML dosyasından içe aktarabilirsiniz. Alternatif olarak, bu model eşlemesini sıfırdan tasarlamak için [Yeni model eşleme yapılandırması oluştur](#CreateModelMapping) bölümündeki adımları tamamlayabilirsiniz.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Yeni bir model eşlemesi yapılandırmasını içe aktarma

1. [Questionnaires mapping.version.1.1xml](https://go.microsoft.com/fwlink/?linkid=851448) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Questionnaires mapping.version.1.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

Devam etmek için sonraki yordamı atlayın, [Yeni bir model eşleme yapılandırması oluşturma](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Yeni model eşleme yapılandırması oluşturma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.
3. **Yapılandırma oluştur**'u seçin.
4. Açılan iletişim kutusunda şu adımları izleyin:

    1. **Yeni** alanına, **Soru formları veri modeline dayalı Model Eşlemesi** yazın.
    2. **Ad** alanına **Soru eşleme** girin.
    3. **Veri modeli tanımı** alanında, **Kök** tanımını seçin.
    4. Yapılandırma oluşturmak için **Yapılandırma oluştur**'u seçin.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Yeni bir model eşleme bileşeni tasarlama

1. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu eşleme**'yi seçin.
2. Eşleme listesini açmak için **Tasarımcı**'yı seçin.
3. **Kök** tanımı için otomatik olarak eklenen **Soru formları eşleme** eşlemesini seçin
4. Seçili eşlemeyi yapılandırmak için **Tasarımcı**'yı seçin.

**Kök** tanımı için yeni bir eşleme otomatik olarak eklenir. Bu eşleme **Modele** yönüne sahiptir. Bu nedenle, bir veri modelini gerekli verilerle doldurmak için bu eşleme kullanılabilir.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Uygulama tablolarına erişmek için veri kaynakları ekleme

Soru formu ayrıntılarını içeren uygulama tablolarına erişmek için veri kaynaklarını yapılandırmanız gerekir.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.
2. Her bir kaydın tek bir soru formunu temsil ettiği KMCollection tablosuna erişmek için kullanılacak yeni bir veri kaynağı ekleyin:

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **Soru formu** girin.
    3. **Tablo** alanına, **KMCollection** girin.
    4. **Sorgu iste** seçeneğini **Evet** olarak ayarlayın. Bu tablo için [filtreleme](../../fin-ops/get-started/advanced-filtering-query-options.md) seçeneklerini sistem sorgusu iletişim kutusunda çalışma zamanında belirtebilirsiniz.
    5. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

3. **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.
4. Her bir kaydın soru formundaki tek bir soruyu temsil ettiği KMQuestion tablosuna erişmek için kullanılacak yeni bir veri kaynağı ekleyin:

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **Soru** girin.
    3. **Tablo** alanına, **KMQuestion** girin.
    4. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

5. **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.
6. Her bir kaydın soru formundaki bir sorunun tek bir yanıtını temsil ettiği KMAnswer tablosuna erişmek için kullanılacak yeni bir veri kaynağı ekleyin:

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. **Ad** alanına, **Yanıt** yazın.
    3. **Tablo** alanına, **KMAnswer** girin.
    4. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

7. **Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.
8. Üst KMCollection tablosunun her kaydından KMQuestionResultGroup tablosunun bir kaydına erişmek için kullanılacak yeni bir hesaplanan alan ekleyin:

    1. **Veri kaynakları** bölmesinde **Soru formu**'nu seçin.
    2. **Ekle**'yi seçin.
    3. İletişim kutusunda, **Ad** alanına **\$ResultGroup** girin.
    4. **Formül düzenle**’yi seçin.
    5. [ER formül düzenleyicisinde](general-electronic-reporting-formula-designer.md) **Formül** alanında KMCollection ile KMQuestionResultGroup tabloları arasındaki bir-çok ilişkisinin [yolunu](er-formula-language.md#paths) kullanmak için **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** girin.
    6. **Kaydet**'i seçip formül düzenleyicisini kapatın.
    7. Yeni hesaplanan alanı eklemek için **Tamam**'ı seçin.

9. **Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.
10. Üst KMCollectionQuestion tablosunun her kaydından KMQuestion tablosunun soru kayıtlarına erişmek için kullanılacak yeni bir hesaplanan alan ekleyin:

    1. **Veri kaynakları** bölmesinde **Soru formu**'nu seçin.
    2. KMCollection tablosunun bir-çok ilişkilerini içeren **\<İlişkiler** düğümünü genişletin.
    3. İlgili **KMCollectionQuestion** tablosunu ve ardından **Ekle**'yi seçin.
    4. İletişim kutusunda, **Ad** alanına **\$Soru** girin.
    5. **Formül düzenle**’yi seçin.
    6. KMQuestion tablosundan uygun soru kayıtlarını döndürmek için formül düzenleyicisindeki **Formül** alanına **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** girin.
    7. **Kaydet**'i seçip formül düzenleyicisini kapatın.
    8. Yeni hesaplanan alanı eklemek için **Tamam**'ı seçin.

11. **Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.
12. Üst KMQuestion tablosunun her kaydından KMAnswer tablosunun yanıt kayıtlarına erişmek için kullanılacak yeni bir hesaplanan alan ekleyin:

    1. **Veri kaynakları** bölmesinde **Soru formu.\<Relations.KMCollectionQuestion.\$Soru**'yu ve ardından **Ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **\$Yanıt** girin.
    3. **Formül düzenle**’yi seçin.
    4. KMAnswer tablosundan uygun yanıt kayıtlarını döndürmek için formül düzenleyicisindeki **Formül** alanına **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** girin.
    5. **Kaydet**'i seçip formül düzenleyicisini kapatın.
    6. Yeni hesaplanan alanı eklemek için **Tamam**'ı seçin.

13. **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo**'yu seçin.
14. CompanyInfo tablosundaki yöntemlere erişmek için kullanılacak yeni bir veri kaynağı ekleyin. Bu tablonun **find()** yönteminin, bu eşlemenin bağlamında çağrıldığı geçerli Finance kurulumunun bir şirketini temsil eden bir kayıt döndürdüğünü unutmayın.

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **CompanyInfo** girin.
    3. **Tablo** alanına, **CompanyInfo** girin.
    4. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Uygulama numaralandırmalarına erişmek için veri kaynakları ekleme

Uygulama numaralandırmalara erişmek ve değerlerini uygulama tablolarındaki **Numaralandırma** türündeki alanların değerleriyle karşılaştırmak için veri kaynakları yapılandırmanız gerekir. Veri modelinin uygun alanlarını doldurmak için karşılaştırma sonucunu kullanmanız gerekir.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Numaralandırma**'yı seçin.
2. **EnumAppNoYes** numaralandırmasındaki değerlere erişmek için kullanılacak yeni bir veri kaynağı ekleyin.

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **EnumAppNoYes** girin.
    3. **Numaralandırma** alanına **NoYes** girin.
    4. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

3. **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Numaralandırma**'yı seçin.
4. **KMCollectionQuestionMode** numaralandırmasındaki değerlere erişmek için kullanılacak yeni bir veri kaynağı ekleyin.

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **EnumAppQuestionOrder** girin.
    3. **Numaralandırma** alanına **KMCollectionQuestionMode** girin.
    4. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Belirtilen dilde rapor oluşturmak için ER etiketleri ekleme

Bazı veri kaynaklarınızı, model eşlemesinin çağrısı bağlamında tanımlanan dile bağlı değerleri döndürmek üzere yapılandırmak için ER etiketleri ekleyebilirsiniz.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynakları** bölmesinde, **Yanıt**'ı ve ardından **Düzenle**'yi seçin.
2. **Etiket** alanını etkinleştirin.
3. **Çevir**'i seçin.
4. **Metin çevirisi** iletişim kutusunda şu adımları izleyin:

    1. **Etiket Kodu** alanına, **PositiveAnswer** yazın.
    2. **Varsayılan dilde metin** alanına **Evet** yazın.
    3. **Çevir**'i seçin.
    4. **Etiket kodu** alanına, **NegativeAnswer** yazın.
    5. **Varsayılan dilde metin** alanına **Hayır** yazın.
    6. **Çevir**'i seçin.

5. **Metin çevirisi** iletişim kutusunu kapatın.
6. **İptal**'i seçin.

![Düzenlenebilir model eşlemesi için ER etiketleri ekleme](./media/er-quick-start1-adding-labels.png)

Yalnızca varsayılan dil için ER etiketleri girdiniz. ER etiketlerinin diğer dillere nasıl çevrilebileceği hakkında bilgi için bkz. [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Numaralandırma değerlerini karşılaştırma sonuçlarını bir metin değerine dönüştürmek için veri kaynağı ekleme

Numaralandırma değerleri ile metin değerleri arasındaki karşılaştırmanın sonuçlarını farklı kaynaklar için birkaç kez dönüştürmeniz gerektiğinden, bu mantığı tek bir veri kaynağı olarak yapılandırmak iyi bir fikirdir. Ancak, bu veri kaynağını yeniden kullanılabilir hale getirmek için parametreli veri kaynağı olarak yapılandırmalısınız. Daha fazla bilgi için bkz. [Hesaplanan alan türüne göre ER veri kaynaklarının parametreli çağrılarını destekleme](er-calculated-field-type.md).

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Genel\\Boş kapsayıcı**'yı seçin.
2. Yeni kapsayıcı veri kaynağı ekleyin:

    1. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    2. İletişim kutusunda, **Ad** alanına **Yardımcı** girin.
    3. Yeni kapsayıcı veri kaynağını eklemek için **Tamam**'ı seçin.

3. **Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.
4. Yeni bir veri kaynağı ekleyin:

    1. **Veri kaynakları** bölmesinde **Yardımcı**'yı seçin.
    2. **Ekle**'yi seçin.
    3. İletişim kutusunda, **Ad** alanına **NoYesEnumToString** girin.
    4. **Formül düzenle**’yi seçin.
    5. Formül düzenleyicide, **Parametreler**'i seçin.
    6. Yapılandırılan deyimin parametrelerini belirtmek için aşağıdaki adımları izleyin:

        1. **Yeni**'yi seçin.
        2. İletişim kutusunda, **Ad** alanına **Bağımsız değişken** girin.
        3. **Tür** alanında **Boole** veri türünü seçin.
        4. **Tamam**'ı seçin.

    7. Belirtilen parametrenin değeri ve yürütme bağlamının diline bağlı olarak uygun ER etiketi metnini döndürmek için **Formül** alanına **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** girin.
    8. **Kaydet**'i seçip formül düzenleyicisini kapatın.
    9. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

![ER model eşleme tasarımcısında yapılandırılmış model eşlemesi](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Veri modeli alanlarına veri kaynakları bağlama

Veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulacağını belirtmek için yapılandırılan veri kaynaklarını veri modeli alanlarına bağlamanız gerekir.

1. **Model eşleme tasarımcısı** sayfasında, **Veri modeli** bölmesinde, **CompanyName** öğesini seçin.
2. **Veri kaynakları** bölmesinde **CompanyInfo** öğesini genişletin ve sonra aşağıdaki adımları izleyin:

    1. CompanyInfo tablosunun **find()** yöntemini temsil eden **CompanyInfo.find()** düğümünü genişletin.
    2. **CompanyInfo.find().Name** öğesini seçin.
    3. Yapılandırılan model eşlemesinin çalışma zamanında bağlamında çağrıldığı şirketin adını doldurmak için **Bağla**'yı seçin.

3. **Veri modeli** bölmesinde **Soru formu**'nu seçin.
4. **Veri kaynakları** bölmesinde **Soru formu**'nu ve ardından soru formu kayıtlarını doldurmak için **Bağla**'yı seçin.
5. **Veri modeli** bölmesinde **Soru formu** öğesini genişletin ve sonra aşağıdaki adımları izleyin:

    1. **Veri modeli** bölmesinde **Etkin**'i seçin.
    2. **Veri modeli** bölmesinde **Düzenle**'yi seçin.
    3. Numaralandırma değerleri arasındaki metne bağımlı veya dile bağımlı karşılaştırma sonucunu doldurmak için **Formül** alanına **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** girin.

6. Aşağıdaki sonuca ulaşıncaya kadar veri kaynaklarını veri modeli alanlarına bağlamaya devam edin.

    | Alan yolu                                              | Veri türü   | Eylem | Bağlama ifadesi |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Dize      | Bağla   | CompanyInfo.'find()'.Name |
    | Soru formu                                           | Kayıt listesi | Bağla   | Soru formu |
    | Soru formu\\Etkin                                   | Dize      | Düzenle   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Soru formu\\Kod                                     | Dize      | Bağla   | \@.kmCollectionId |
    | Soru formu\\Açıklama                              | Dize      | Bağla   | \@.Açıklama |
    | Soru formu\\QuestionnaireType                        | Dize      | Bağla   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Soru formu\\QuestionOrder                            | Dize      | Düzenle   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Koşullu",<br>EnumAppQuestionOrder.Random, "Rasgele (soru formundaki yüzde)",<br>EnumAppQuestionOrder.RandomGroup, "Rasgele (sonuç gruplarındaki yüzde)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Soru formu\\ResultsGroup                             | Kaydet      |        | |
    | Soru formu\\ResultsGroup\\Kod                       | Dize      | Bağla   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Soru formu\\ResultsGroup\\Açıklama                | Dize      | Bağla   | \@.'\$ResultGroup'.description |
    | Soru formu\\ResultsGroup\\MaxNumberOfPoints          | Gerçek        | Bağla   | \@.'\$ResultGroup'.maxPoint |
    | Soru formu\\Soru                                 | Kayıt listesi | Bağla   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Soru formu\\Soru\\CollectionSequenceNumber       | Tamsayı     | Bağla   | \@.answerCollectionSequenceNumber |
    | Soru formu\\Soru\\Kod                             | Dize      | Bağla   | \@.kmQuestionId |
    | Soru formu\\Soru\\MustBeCompleted                | Dize      | Düzenle   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Soru formu\\Soru\\PrimaryQuestion                | Dize      | Bağla   | \@.parentQuestionId |
    | Soru formu\\Soru\\SequenceNumber                 | Tamsayı     | Bağla   | \@.SequenceNumber |
    | Soru formu\\Soru\\Metin                           | Dize      | Bağla   | \@.'\$Question'.text |
    | Soru formu\\Soru\\Yanıt                         | Kayıt listesi | Bağla   | \@.'\$Question'.'\$Answer' |
    | Soru formu\\Soru\\Yanıt\\CorrectAnswer          | Dize      | Düzenle   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Soru formu\\Soru\\Yanıt\\Puanlar                 | Gerçek        | Bağla   | \@.point |
    | Soru formu\\Soru\\Yanıt\\SequenceNumber         | Tamsayı     | Bağla   | \@.sequenceNumber |
    | Soru formu\\Soru\\Yanıt\\Metin                   | Dize      | Bağla   | \@.text |

    Aşağıdaki şekil, **Model eşleme tasarımcısı** sayfasındaki yapılandırılmış model eşlemesinin son durumunu gösterir.

    ![ER model eşleme tasarımcısında tamamen yapılandırılmış model eşlemesi](./media/er-quick-start1-mapping2.png)

7. Değişikliklerinizi kaydedin.
8. **Model eşleme tasarımcısı** sayfasını kapatın

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Model eşleme tasarımını tamamlama

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu eşleme**'yi seçin.
3. **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.
4. **Durumu değiştir** \> **Tamamla**'yı seçin.

Bu yapılandırmanın sürüm 1.1 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi. Sürüm 1.1 artık değiştirilemez. Bu sürüm yapılandırılmış model eşlemesini içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir. Bu yapılandırma için sürüm 1.2 oluşturuldu ve **taslak** durumuna sahip. **Soru formu eşleme** yapılandırmasını ayarlamak için bu sürümü düzenleyebilirsiniz.

![Yapılandırmalar sayfasındaki düzenlenebilir ER yapılandırmasının sürümleri](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Yapılandırılan model eşlemesi, **Soru formu** iş etki alanını temsil eden soyur veri modelinin Finance kurulumunuza özgü uygulamasıdır.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Özel rapor için şablon tasarlama

ER çerçevesi, Microsoft Office (Excel çalışma kitapları veya Word belgeleri) biçimlerinde raporlar oluşturmak için önceden tanımlanmış şablonları kullanır. Gerekli rapor oluşturulurken, yapılandırılmış veri akışına göre bir şablon gerekli verilerle doldurulur. Bu nedenle, özel raporunuz için önce bir şablon tasarmalısınız. Bu şablon özel bir raporun düzenini temsil eden yapıdaki bir Excel çalışma kitabı olarak tasarlanmalıdır. Gerekli verilerle doldurmak istediğiniz tüm Excel öğelerini adlandırın.

1. [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. Dosyayı Excel'de açın ve çalışma kitabının yapısını gözden geçirin.

Aşağıdaki çizimin gösterdiği gibi, indirilen şablon, bir soru formunun sorularını uygun yanıtlarla birlikte görüntüleyen belirtilen soru formlarını yazdıracak şekilde tasarlanmıştır.

![Belirtilen soru formlarını yazdırmak için Excel şablonu](./media/er-quick-start1-template-layout.png)

Soru formu ayrıntılarını doldurmak üzere bu şablona Excel adları eklendi. Excel adlarını gözden geçirmek için Ad Yöneticisi'ni kullanabilirsiniz.

![Sağlanan Excel şablonundaki Excel adlarını gözden geçirmek için Ad Yöneticisi'ni kullanma](./media/er-quick-start1-template-names.png)

Rapor etiketleri İngilizce dilinde sabit metin olarak eklendi. Yapılandırılan model eşlemesinde dile bağlı ifadelerde yaptığınız gibi, ER biçim [etiketlerini](#AddMmLabels) kullanarak, rapor etiketlerini dile bağlı metinle doldurmak için kullanılan yeni Excel adlarıyla değiştirebilirsiniz. Bu durumda, ER etiketlerinin düzenlenebilir ER biçiminde eklenmesi gerekir.

Aşağıdaki çizimde gösterildiği gibi, Excel'in sayfalandırma yapmasına olanak tanımak için özel rapor başlığı belirtilmiştir.

![Sağlanan Excel şablonundaki özel rapor başlığı](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Bir biçim tasarlama

Elektronik Raporlama İşlev Danışmanı rolündeki bir kullanıcı olarak, bir [biçim](general-electronic-reporting.md#FormatComponentOutbound) bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bir rapor şablonunun çalışma zamanında gerekli verilerle nasıl doldurulacağını belirtmek için biçim bileşenini yapılandırmalısınız.

[Tasarlanmış biçim yapılandırmasını içe aktarma](#FormatImport) bölümündeki adımları izleyerek gerekli biçimi sağlanan XML dosyasından içe aktarabilirsiniz. Alternatif olarak, bu biçimi sıfırdan tasarlamak için [Yeni biçim yapılandırması oluştur](#FormatCreate) bölümündeki adımları tamamlayabilirsiniz.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Tasarlanan biçim yapılandırmasını içe aktarma

1. [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Questionnaires format.version.1.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

Devam etmek için sonraki yordamı atlayın, [Yeni bir biçim yapılandırması oluşturma](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Yeni bir biçim yapılandırması oluşturma
 
1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu modeli**'ni seçin.
3. **Yapılandırma oluştur**'u seçin.
4. Açılan iletişim kutusunda şu adımları izleyin:

    1. **Yeni** alanına, **Soru formları veri modeline dayalı biçim** yazın.
    2. **Ad** alanına **Soru formu raporu** girin.
    3. **Veri modeli sürümü** alanında **1**'i seçin.

        > [!NOTE]
        > - Temel veri modelinin belirli bir sürümünü seçerseniz, ilgili veri modeli sürümünün yapısı size, oluşturulan biçimdeki **Model** veri kaynağının yapısı olarak gösterilecektir.
        > - Bu alanı boş bırakabilirsiniz. Bu durumda, veri modelinin **Taslak** sürümünün yapısı, oluşturulan biçimdeki **Model** veri kaynağının yapısı olarak size sunulacaktır. Daha sonra modelinizi ayarlayabilir ve biçiminizde bu düzeltmeleri hemen görebilirsiniz. Bu yaklaşım veri modelinizi, model eşlemeyi ve biçimi eşzamanlı olarak yapılandırdığınızda ER çözüm tasarımının verimliliğini artırabilir.
        > - Temel veri modelinin belirli bir sürümünü seçerseniz, daha sonra bir biçimi düzenlemeye başladığınızda **Taslak** sürümü kullanmaya geçebilirsiniz.

    4. **Veri modeli tanımı** alanında, **Kök** tanımını seçin.

5. Yapılandırma oluşturmak için **Yapılandırma oluştur**'u seçin.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Rapor şablonunu içe aktarma

1. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Soru formu raporu**'nu seçin.
2. Özel biçim yapılandırmak için **Tasarımcı**'yı seçin.
3. **Biçim tasarımcısı** sayfasında, Eylem Panosu üzerinde, **İçeri aktar** \> **Excel'den aktar**'ı seçin.
4. İletişim kutusunda şu adımları izleyin:

    1. **Şablon ekle**'yi seçin.
    2. Yerel olarak kaydedilmiş **Questionnaires report template.xslx** dosyasını bulup seçin ve **Aç**'ı seçin.
    3. Şablonu içe aktarmak için **Tamam**'ı seçin.

    ![Rapor şablonunu içe aktarma](./media/er-quick-start1-template-import.png)

**Excel\\Dosya** biçimi öğesi, otomatik olarak düzenlenebilir biçime kök öğesi olarak eklenir. Ek olarak, **Excel\\Aralık** biçim öğesi veya **Excel\\Hücre** biçim öğesi içe aktarılan şablonun her tanınan Excel adı için otomatik olarak eklenir. İç içe geçmiş **dize** öğesi bulunan **Excel\\Başlık** biçimi , içe aktarılan şablonun başlık ayarlarını yansıtmak için otomatik olarak eklenir.

![ER İşlemi tasarımcısına otomatik olarak eklenen öğeleri içeren yapıyı biçimlendirme](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Biçim yapılandırma

1. **Biçim Tasarımcısı** sayfasında, biçim ağacında, **Excel** kök öğesini seçin.
2. Sayfanın sağ tarafındaki **Biçim** sekmesinde, **Ad** alanına <a name="AddFormatRootElement"></a>**Rapor** girin.
3. **Dil tercihi** alanında, raporu kullanıcının tercih ettiği dilde çalıştırmak için **Kullanıcı tercihi**'ni seçin.
4. **Kültür tercihi** alanında, raporu kullanıcının tercih ettiği kültürde çalıştırmak için **Kullanıcı tercihi**'ni seçin.

    Bir ER işlemi için dil ve kültür bağlamlarının nasıl belirtileceği konusunda bilgi için bkz. [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md).

    ![ER İşlem tasarımcısında tasarlanan rapor için dil ve kültür ayarları yapılandırma](./media/er-quick-start1-template-format-structure1.png)

5. Biçim ağacında, kök düğümü genişletin ve sonra **ResultsGroup** öğesini seçin.
6. Tek bir soru formu için birden fazla sonuç grubu olmasını beklemediğinizden **Biçim** sekmesinde **Çoğaltma yönü** alanında  **Çoğaltma yok** seçeneğini belirleyin.

    ![ER İşlem tasarımcısında Aralık biçimi öğeleri için çoğaltma yönünü tanımlama](./media/er-quick-start1-template-format-structure2.png)

7. **Kaydet**'i seçin.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Rapor başlığı için veri bağlamayı tanımlama

Oluşturulan bir raporun başlığını doldurmak için kullanılan bir biçim öğesi için veri bağlaması belirtmeniz gerekir.

1. **Biçim tasarımcısı** sayfasında sağdaki **Eşleme** sekmesinde, **Rapor\\ReportTitle** öğesini seçin.
2. **Formül düzenle**’yi seçin.
3. Formül düzenleyicide, **Çevir**'i seçin.
4. **Metin çevirisi** iletişim kutusunda şu adımları izleyin:

    1. **Etiket Kodu** alanına, **ReportTitle** yazın.
    2. **Varsayılan dilde metin** alanına **Soru formları raporu** yazın.
    3. **Çevir** i seçin ve sonra **Kaydet**'i seçin.
    4. **Metin çevirisi** iletişim kutusunu kapatmak için **Çevir**'i seçin.

5. Formül düzenleyiciyi kapatın.

    ![Oluşturulmuş bir raporun başlığını doldurmak için bağlamayı yapılandırma](./media/er-quick-start1-add-report-title-label.png)

Geçerli şablon diline bağımlı tüm diğer etiketleri oluşturmak için bu tekniği kullanabilirsiniz. Tek bir ER yapılandırmasının eklenen etiketlerinin tüm desteklenen dillere nasıl çevrilebileceği hakkında bilgi için bkz. [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Model veri kaynağını gözden geçirme

1. **Biçim tasarımcısı** sayfasındaki **Eşleme** sekmesinde, bu ER biçiminin temel veri modelini temsil eden <a name="ModelDSName"></a>**model** veri kaynağını seçin.
2. **Düzenle** öğesini seçin.
3. **Veri kaynağı özellikleri** iletişim kutusundaki bilgileri gözden geçirin. Bu veri kaynağı **Soru formu modeli** yapılandırmasında bulunan **Soru formu** veri modeli bileşeni sürüm 1'i temsil eder.

![ER İşlemi tasarımcısındaki model veri kaynağının özellikleri](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Biçim öğelerini veri kaynağı alanlarına bağlama

Çalışma zamanında bir şablonun nasıl doldurulacağını belirtmek için, uygun bir Excel adıyla ilişkilendirilmiş her bir biçim öğesini bu biçimin veri kaynağının tek bir alanına bağlamanız gerekir.

1. **Biçim Tasarımcısı** sayfasında, biçim ağacında, **Rapor\\CompanyName** biçim öğesini seçin.
2. **Eşleme** sekmesinde **Dize** türünün **model.CompanyName** veri kaynağı alanını seçin.
3. Şablona şirket adı girmek için **Bağla**'yı seçin.
4. Biçim ağacında, **Rapor\\Soru formu** öğesini seçin.
5. **Eşleme** sekmesinde **Kayıt listesi** türünün **model.Questionnaire** veri kaynağı alanını seçin.
6. **Bağla**'yı seçin.
7. Biçim öğeleri ile ilgili daha fazla ayrıntı görmek için **Ayrıntıları göster**'i seçin.

    **Soru formu** aralığı biçim öğesi dikey olarak yinelenmiş olarak yapılandırılır. **Kayıt listesi** türünde bir veri kaynağına bağlı olduğunda bağlı veri kaynağının her kaydı için Excel şablonunun uygun **Soru formu** aralığı yinelenir.
 
    ![Soru formu aralığı biçim öğesini ER İşlemi tasarımcısında uygun Kayıt listesi veri kaynaklarına bağlama](./media/er-quick-start1-bindings1.png)

    Excel şablonunun **Soru formu** aralığı 5 ile 14 arasındaki satırlar arasında tanımlandığı için, bu satırlar bildirilen her soru formu için yinelenir.

    ![Kayıt listesi veri kaynaklarının her kaydı için oluşturulan raporda tekrarlanacak olan Excel şablonundaki satırlar](./media/er-quick-start1-template-questionnaire-range.png)

8. Aşağıdaki tabloda açıklandığı gibi, kalan biçim öğeleri için benzer bağlamaları yapılandırın.

    > [!NOTE]
    > Bu tabloda, "Veri kaynağı yolu" sütunundaki bilgiler [göreli yol](relative-path-data-bindings-er-models-format.md) ER özelliğinin açık olduğunu varsayar.

    | Biçim öğesi yolu                                      | Veri kaynağı yolu |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Soru formu                                     | **model.Questionnaire** |
    | Excel\\Soru formu\\Etkin                             | **\@.Active**, burada **\@**, **model.Questionnaire** olur |
    | Excel\\Soru formu\\Kod                               | **\@.Code** |
    | Excel\\Soru formu\\Açıklama                        | **\@.Description** |
    | Excel\\Soru formu\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Soru formu\\QuestionnaireOrder                      | **\@.QuestionOrder** |
    | Excel\\Soru formu\\ResultsGroup\\Kod\_               | **\@.ResultsGroup.Code** |
    | Excel\\Soru formu\\ResultsGroup\\Açıklama\_        | **\@.ResultsGroup.Description** |
    | Excel\\Soru formu\\ResultsGroup \\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Soru formu\\Soru                           | **\@.Question** |
    | Excel\\Soru formu\\Soru\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, (burada **\@**, **model.Questionnaire.Question** olur) |
    | Excel\\Soru formu\\Soru\\Kimlik                       | **\@.Id** |
    | Excel\\Soru formu\\Soru\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Soru formu\\Soru\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Soru formu\\Soru\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Soru formu\\Soru\\Metin                     | **\@.Text** |
    | Excel\\Soru formu\\Soru\\Yanıt                   | **\@.Answer** |
    | Excel\\Soru formu\\Soru\\Yanıt\\CorrectAnswer    | **\@.CorrectAnswer**, (burada **\@**, **model.Questionnaire.Answer** olur) |
    | Excel\\Soru formu\\Soru\\Yanıt\\Puanlar           | **\@.Points** |
    | Excel\\Soru formu\\Soru\\Yanıt\\Metin             | **\@.Text** |

9. Tamamladıktan sonra **Kaydet**'i seçin.

Aşağıdaki şekil, **Biçim tasarımcısı** sayfasındaki yapılandırılmış veri bağlamalarının son durumunu gösterir.

![ER İşlemi tasarımcısında yapılandırılmış veri bağlamaları](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Belirtilen tüm veri kaynakları ve bağlamalarının tüm koleksiyonu, yapılandırılmış biçimin biçim eşleme bileşenini temsil eder. Bu biçim eşlemesi, rapor oluşturmak üzere yapılandırılmış biçimi çalıştırdığınızda çağrılır.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>ER'den tasarlanan biçim çalıştırma

Şimdi, **Yapılandırmalar** sayfasından test amaçlı olarak tasarlanmış bir biçim çalıştırabilirsiniz.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırma** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.
3. **Taslak** durumundaki biçim sürümü için **Tasarımcı**'yı seçin.
4. **Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.
5. **ER parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.
6. Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.
7. Raporu çalıştırmak için **Tamam**'ı seçin.
8. Oluşturulan raporu inceleyin.

[Varsayılan](electronic-reporting-destinations.md#default-behavior) olarak, oluşturulmuş bir rapor indirebileceğiniz bir Excel dosyası olarak teslim edilir. Aşağıdaki çizimler Excel biçiminde oluşturulan raporun iki sayfasını gösterir.

![Excel biçiminde oluşturulmuş rapor örneği, sayfa 1](./media/er-quick-start1-report1a.png)

![Excel biçiminde oluşturulmuş rapor örneği, sayfa 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Tasarlanan biçimi ayarlama

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Oluşturulan belgenin adını değiştirmek için bir biçimi değiştirme

Varsayılan olarak, oluşturulan bir belge, geçerli kullanıcının diğer adı kullanılarak adlandırılır. Biçimi değiştirerek, bu davranışı oluşturulan bir belgenin özel mantığınıza göre adlandırılması için değiştirebilirsiniz. Örneğin, oluşturulan bir belgenin adı geçerli oturum tarihi ve saatini ve raporun başlığını temel alabilir.

1. **Biçim tasarımcısı** sayfasında **Rapor** kök öğesini seçin.
2. **Eşleme** sekmesinde **Dosya adını düzenle**'yi seçin.
3. **Formül** alanına, **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))** girin.
4. **Kaydet**'i seçip formül düzenleyicisini kapatın.
5. **Kaydet**'i seçin.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Soruların sırasını değiştirmek için bir biçimi değiştirme

Sorular oluşturulmuş bir raporda doğru olarak sıralanmaz. Biçimi değiştirerek sırayı değiştirebilirsiniz.

1. **Biçim tasarımcısı** sayfasında **Rapor** kök öğesini seçin.
2. **Eşleme** sekmesinde bulunan biçim ağacında, **Rapor\\Soru formu\\Soru** öğesini genişletin.

    ![ER İşlem tasarımcısındaki Aralık türündeki soru biçimi öğesi](./media/er-quick-start1-bindings3.png)

3. **Eşleme** sekmesinde **model.Questionnaire** öğesini seçin.
4. **Ekle** \> **İşlevler\\Hesaplanan alan**'ı seçin ve ardından **Ad** alanına **OrderedQuestions** girin.
5. **Formül düzenle**’yi seçin.
6. Formül düzenleyicisinde, **Formül** alanında, geçerli soru formunun soru listesini seri sıra numarasına göre sıralamak için **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** girin.
7. **Kaydet**'i seçip formül düzenleyicisini kapatın.
8. Yeni bir hesaplanan alan girişini tamamlamak için **Tamam**'ı seçin.
9. **Eşleme** sekmesinde **model.Questionnaire.OrderedQuestions** öğesini seçin.
10. Biçim ağacında **Excel\\Soru formu\\Soru**'yu seçin.
11. **Bağla**'yı seçin ve ardından geçerli **model.Questionnaire.Questions** yolunun iç içe geçmiş öğelerin tüm bağlamalarında yeni **model.Questionnaire.OrderedQuestions** yoluyla değiştirileceğini onaylayın.
12. **Kaydet**'i seçin.

![ER İşlem tasarımcısında Soru biçimi öğesini yapılandırılan OrderedQuestions veri kaynağına bağlama](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>ER'den değiştirilmiş biçim çalıştırma

Artık, ER çerçevesinden test amacıyla değiştirilmiş bir biçim çalıştırabilirsiniz.

1. **Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.
2. **ER parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.
3. Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.
4. Raporu çalıştırmak için **Tamam**'ı seçin.
5. Oluşturulan raporu inceleyin.

Aşağıdaki şekil, soruların doğru şekilde sıralandığı Excel biçiminde oluşturulmuş bir raporu gösterir.

![Soruların doğru olarak sıralandığı Excel biçiminde oluşturulmuş rapor](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Biçim tasarımını tamamlama

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.
3. **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.
4. **Durumu değiştir** \> **Tamamla**'yı seçin.

Bu yapılandırmanın sürüm 1.1 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi. Sürüm 1.1 artık değiştirilemez. Bu sürüm yapılandırılmış biçimi içerir ve özel raporunuzu yazdırmak için kullanılabilir. Bu yapılandırma için sürüm 1.2 oluşturuldu ve **taslak** durumuna sahip. **Soru formu** raporunuzun biçimini ayarlamak için bu sürümü düzenleyebilirsiniz.

![Yapılandırmalar sayfasındaki düzenlenebilir ER yapılandırmasının sürümleri](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Yapılandırılan biçim, **Soru formu** raporu tasarımınızdır ve Finance'a özgü en artefaktlara ilişki içermez.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Tasarlanan raporu çağırmak için uygulama artefaktları geliştirme

Sistem Yöneticisi rolündeki bir kullanıcı olarak, yapılandırılan ER biçiminin özel raporunuzu oluşturmak üzere uygulama kullanıcı arabiriminden (UI) çağrılabilmesi için yeni bir mantık geliştirmeniz gerekir. Şu anda, ER bu tür mantık yapılandırmak için herhangi bir yetenek sunmaz. Bu nedenle, bazı mühendislik çalışmaları gereklidir. 

Yeni mantığı geliştirmek için sürekli yapılandırma destekleyen bir topoloji dağıtmanız gerekir. Daha fazla bilgi için, [Sürekli yapılandırma ve test otomasyonu destekleyen topolojiler dağıtın](../perf-test/continuous-build-test-automation.md). Bu topoloji için geliştirme ortamına da erişiminiz olması gerekir. Kullanılabilir ER API'sı hakkında daha fazla bilgi için, bkz. [ER çerçevesi API'sı](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Kaynak kodu değiştir

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Veri sözleşmesi sınıfı ekleme

Yeni **QuestionnairesErReportContract** sınıfını Microsoft Visual Studio projenize ekleyin ve yapılandırılan ER biçimini çalıştırmak için kullanılması gereken veri sözleşmesini belirten kodu yazın.

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

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>UI oluşturucu sınıfı ekleme

Yeni **QuestionnairesErReportUIBuilder** sınıfını Visual Studio projenize ekleyin ve çalıştırılması gereken ER biçiminin biçim eşlemesi kimliğini aramak için kullanılacak çalışma zamanı iletişim kutusunu oluşturmak üzere kod yazın. Sağlanan kod, yalnızca **[Kök](#RootDefinitionName)** tanımını kullanarak **[Soru formları](#DataModeName)** veri modeline başvuran **Veri modeli** türünde bir veri kaynağı içeren ER biçimlerini arar.

> [!NOTE]
> Alternatif olarak, ER biçimlerini filtrelemek için ER tümleştirme noktalarını kullanabilirsiniz. Daha fazla bilgi için, bkz. [Biçim eşleme aramasını göstermek için API](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

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

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Veri sağlayıcı sınıfı ekleme

Yeni **QuestionnairesErReportDP** sınıfını Microsoft Visual Studio projenize ekleyin ve yapılandırılan ER biçimini çalıştırmak için kullanılması gereken veri sağlayıcısını belirten kodu yazın. Sağlanan kod yalnızca bu veri sağlayıcısına ait veri sözleşmesini içerir.

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

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Etiket dosyası ekleme

Yeni **QuestionnairesErReportLabels\_en-US** etiket dosyalarını Visual Studio projenize ekleyin ve yeni UI kaynakları için aşağıdaki etiketleri belirtin:

- Şu metni ABD İngilizce (en-US) dilinde içeren yeni menü öğesi için **\@QuestionnairesReport** etiketi: **Soru formları raporu (ER tarafından desteklenir)**
- Seçili bir ER biçimi toplu iş olarak yürütülmek üzere zamanlanırsa, toplu iş başlığı için **\@QuestionnairesReportBatchJobDescription** etiketi

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Rapor hizmeti sınıfı ekleme

Yeni **QuestionnairesErReportService** sınıfını Visual Studio projenize ekleyin ve ER biçimini çağıran, bunu bir biçim eşleme kimliğiyle tanımlayan ve parametre olarak bir veri sözleşmesi sağlayan kodu yazın.

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

Uygulama verilerini çalıştıran bir ER biçimi kullanmanız gerektiğinde, biçim eşlemesinde **Veri modeli** türünde veri kaynağı yapılandırmanız gerekir. Bu veri kaynağı, tek bir kök tanımı kullanılarak belirtilen veri modelinin belirli bir bölümüne başvurur. ER biçimi çalıştırıldığında, belirli bir model ve kök tanımı için yapılandırılmış uygun ER model eşlemeye erişmek için bu veri kaynağını çağırır.

Kaynak kodda hazırlayabileceğiniz ve veri sözleşmesinin bir parçası olarak saklayabileceğiniz tüm bilgiler, bu türdeki ER model eşlemesi kullanılarak çalışan ER biçimine geçirilebilir. ER model eşlemesinde, **[QuestionnairesErReportContract](#DataContractClass)** sınıfına başvuran **Nesne** türünde bir veri kaynağı yapılandırmanız gerekir. Bir model eşlemesi tanımlamak için bu model eşlemesini çağıran bir veri kaynağı belirtmeniz gerekir. Sağlanan kodda, bu veri kaynağı, **[model](#ModelDSName)** değeri olan **ERModelDataSourceName** sabit değeri tarafından belirtilir. Model eşlemesinde veri sözleşmesini göstermek için hangi veri kaynağının kullanıldığını tanımlamak üzere bir veri kaynağı adı belirtmeniz gerekir. Sağlanan kodda, bu ad, <a name="DataContractDSName"></a>**RunTimeParameters** değeri olan **ParametersDataSourceName** sabit değeri tarafından belirtilir.

> [!NOTE]
> Yeni bir ortamda, ER model eşleme tasarımcısında bu tür sınıfın kullanılabilir olması için ER meta verilerini yenilemeniz gerekebilir. Daha fazla bilgi için bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Rapor denetleyicisi sınıfı ekleme

Yeni **QuestionnairesErReportController** sınıfını Visual Studio projenize ekleyin ve sağlanan **QuestionnairesErReportUIBuilder** sınıfının mantığını temel alarak oluşturulan iletişim kutusunda ER biçimini tercihinize göre zaman uyumlu modda veya toplu işlem modunda çalıştıran kodu yazın.

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

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Menü öğesi ekleme

Yeni **QuestionnairesErReport** menü öğesini Visual Studio projenize ekleyin. **Nesne** özelliğinde, bu menü öğesi **QuestionnairesErReportController** sınıfına başvurur ve bir ER biçimini seçmek ve çalıştırmak için bir kullanıcı izni belirtmek üzere kullanılır. **Etiket** özelliğinde, bu menü öğesi daha önce oluşturduğunuz **\@QuestionnairesReport** etiketine başvurur; böylece uygulama kullanıcı arabiriminde doğru metin gösterilir.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Menüye menü öğesi ekleme

Varolan **KM** menüsünü Visual Studio projenize ekleyin. Bu menüye **Çıktı** türünde yeni bir **QuestionnairesErReport** öğesi eklemeniz gerekir. Bu öğenin önceki bölümde açıklanan **QuestionnairesErReport** menü öğesine başvurması gerekir.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Visual Studio projesi oluşturma

Yeni bir menü öğesini kullanıcıların kullanabilmesini sağlamak için projenizi oluşturun.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Uygulamadan bir biçim çalıştırma

1. **Soru formu** \> **Tasarım** \> **Soru formu raporu (ER tarafından desteklenir)** öğesine gidin.

    ![Yapılandırılan ER biçimini çalıştırmak için Soru Formu modülündeki Soru formları raporu (ER tarafından desteklenir) menü öğesini seçme](./media/er-quick-start1-application-menu-modified.png)

2. İletişim kutusunda, **Biçim eşleme** alanında, **Soru formları raporu**'nu seçin.
3. **Tamam**'ı seçin.
4. **Elektronik rapor parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.
5. Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.
6. Raporu çalıştırmak için **Tamam**'ı seçin.

    ![Elektronik rapor iletişim kutusunda seçim ölçütünü belirtme](./media/er-quick-start1-report-run-dialog-page.png)

7. Oluşturulan raporu inceleyin.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Tasarlanan ER çözümünü ayarlama

Yapılandırılan ER çözümünü, çalışan ER biçiminin ayrıntılarına erişmek için geliştirdiğiniz veri sağlayıcı sınıfını kullanacak ve oluşturulan rapora bu ER biçiminin adını girecek şekilde değiştirebilirsiniz.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Model eşlemesini değiştirme

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Veri sözleşmesi nesnesine erişmek için veri kaynakları ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu eşleme**'yi seçin.
3. **Veri kaynağı eşleme modeli** sayfasını açmak için **Tasarımcı**'yı seçin.
4. Model eşleme tasarımcısında seçilen eşlemeyi açmak için **Tasarımcı**'yı seçin.
5. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Nesne**'yi seçin.
6. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
7. İletişim kutusunda, **Ad** alanına, **QuestionnairesErReportService** sınıfının kaynak kodunda tanımlandığı şekilde **[RunTimeParameters](#DataContractDSName)** girin.
8. **Sınıf** alanına daha önce kodlanmış olan **[QuestionnairesErReportContract](#DataContractClass)** öğesini girin.
9. **Tamam**'ı seçin.
10. **RunTimeParameters** öğesini genişletin.

Eklenen veri kaynağı, çalışan ER biçim eşlemesinin kayıt kodu ile ilgili bilgi sağlar.

![ER model eşleme tasarımcısında eklenen veri kaynağı](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>ER biçim eşleme kayıtlarına erişmek için veri kaynağı ekleme

ER biçim eşleme kayıtlarına erişmek üzere bir veri kaynağı ekleyerek seçili model eşlemesini düzenlemeye devam edin.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.
2. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
3. İletişim kutusunda, **Ad** alanına **ER1** girin.
4. **Tablo** alanına, **ERFormatMappingTable** girin.
5. **Tamam**'ı seçin.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Çalışan bir ER biçimin biçim eşleme kaydına erişmek için veri kaynağı ekleme

Çalışan ER biçiminin eşleme kaydına erişmek üzere bir veri kaynağı ekleyerek seçili model eşlemesini düzenlemeye devam edin.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **İşlevler\\Hesaplanan alan**'ı seçin.
2. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
3. İletişim kutusunda, **Ad** alanına **ER2** girin.
4. **Formül düzenle**’yi seçin.
5. Formül Düzenleyicisinde, **Formül** alanına **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** girin.
6. **Kaydet**'i seçip formül düzenleyicisini kapatın.
7. **Tamam**'ı seçin.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Çalışan ER biçiminin adını veri modeline girme

Seçili model eşlemesini, veri modelinde çalışan ER biçimi adı girilmiş olacak şekilde düzenlemeye devam edin.

1. **Model eşleme tasarımcısı** sayfasında, **Veri modeli** bölmesinde, **ExecutionContext** öğesini genişletin ve **ExecutionContext\\FormatName** öğesini seçin.
2. **Veri modeli** bölmesinde, seçili veri modeli alanı için bir veri bağlamayı yapılandırmak üzere **Düzenle**'yi seçin.
3. Formül düzenleyicisinde, **Formül** alanına **FIRSTORNULL (ER2.'\>Relations'.Format).Name** girin.
4. **Kaydet**'i seçip formül düzenleyicisini kapatın.

**FormatName** alanını kullandığınız için, yapılandırılan model eşlemesi, yürütme sırasında bu model eşlemesini çağıran bir ER biçimi adı ortaya çıkarır.

![Veri modeli alanını, ER model eşleme tasarımcısındaki eklenen veri kaynağı yöntemine bağlama](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Model eşleme tasarımını tamamlama

1. **Model eşleme tasarımcısı** sayfasında **Kaydet**'i seçin.
2. Sayfayı kapatın.
3. Model eşlemeleri sayfasını kapatın.
4. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Soru formu eşleme** yapılandırmasının hala seçili olduğundan emin olun. Ardından, **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.
5. **Durumu değiştir** \> **Tamamla**'yı seçin.

Bu yapılandırmanın sürüm 1.2 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi. Sürüm 1.2 artık değiştirilemez. Bu sürüm yapılandırılmış model eşlemesini içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir. Bu yapılandırma için sürüm 1.3 oluşturuldu ve **taslak** durumuna sahip. **Soru formu** model eşlemesini ayarlamak için bu sürümü düzenleyebilirsiniz.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Biçim değiştirme

Yapılandırılmış ER biçimini adı, ER biçimi çalıştırıldığında oluşturulan bir raporun altbilgisi olarak gösterilecek şekilde değiştirebilirsiniz.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Yeni bir biçim öğesi ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.
3. **Tasarımcı**’yı seçin.
4. **Biçim tasarımcısı** sayfasında **Rapor** kök öğesini seçin.
5. Seçili **Rapor** kök öğesi için yeni bir iç içe biçim öğesi eklemek üzere **Ekle**'yi seçin.
6. **Excel \\Alt bilgi**'yi seçin.
7. **Ad** alanına, **Alt bilgi** yazın.
8. **Rapor\Alt bilgi**'yi ve ardından **Ekle**'yi seçin.
9. **Metin\\Dize**'yi seçin.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Eklenen biçim öğesini bağlama

1. **Biçim tasarımcısı** sayfasındaki **Eşleme** sekmesinde, biçim ağacında, **Alt bilgi\\Dize** öğesi için **Formülü düzenle** öğesini seçin.
2. Formül düzenleyicisinde **Formül** alanına **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** girin.
3. **Kaydet**'i seçip formül düzenleyicisini kapatın.
4. **Kaydet**'i seçin.

Yapılandırılmış biçim şimdi, adı **Altbilgi\\Dize** öğesi kullanılarak oluşturulan bir raporun altbilgisine girilecek şekilde değiştirildi.

![ER İşlem tasarımcısında, yapılandırılmış biçime Alt bilgi biçim öğesi ekleme](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Biçim tasarımını tamamlama

1. **Biçim tasarımcısı** sayfasını kapatın.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Soru formu raporu** yapılandırmasının hala seçili olduğundan emin olun. Ardından, **Sürümler** hızlı sekmesinde durumu **Taslak** olan yapılandırma sürümünü seçin.
3. **Durumu değiştir** \> **Tamamla**'yı seçin.

Bu yapılandırmanın sürüm 1.2 durumu **Taslak** yerine **Tamamlandı** olarak değiştirildi. Sürüm 1.2 artık değiştirilemez. Bu sürüm yapılandırılmış biçim içerir ve diğer ER yapılandırmalarının temeli olarak kullanılabilir. Bu yapılandırma için sürüm 1.3 oluşturuldu ve **taslak** durumuna sahip. **Soru formu** raporunu ayarlamak için bu sürümü düzenleyebilirsiniz.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Uygulamadan bir biçim çalıştırma

1. **Soru formu** \> **Tasarım** \> **Soru formu raporu (ER tarafından desteklenir)** öğesine gidin.
2. İletişim kutusunda, **Biçim eşleme** alanında, **Soru formları raporu**'nu seçin.
3. **Tamam**'ı seçin.
4. **ER parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.
5. Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.
6. Raporu çalıştırmak için **Tamam**'ı seçin.
7. Excel biçiminde oluşturulan raporu gözden geçirin.

Oluşturulan raporun altbilgisi, bunu oluşturmak için kullanılan ER biçiminin adını içerir.

![Excel biçiminde oluşturulan rapor](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>ER'den bir biçim çalıştırma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında yapılandırma ağacında, **Soru formu modeli**'ni genişletin ve **Soru formu raporu**'nu seçin.
3. Eylem Bölmesinde, **Çalıştır**'ı seçin.
4. **Elektronik rapor parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.
5. Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.
6. Raporu çalıştırmak için **Tamam**'ı seçin.
7. Excel biçiminde oluşturulan raporu gözden geçirin.

Oluşturulan raporun altbilgisi, oluşturulduğu sırada çalıştırılan ER biçimi tarafından çağrıldığında, veri sözleşme nesnesi çalışan model eşlemesine geçirilmediği için, bunu oluşturmak için kullanılan ER biçiminin adını içermez.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Ekran önizleme için biçim hedefi yapılandırma

1. Sırasıyla **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama hedefi** seçimlerini yapın.
2. **Elektronik raporlama hedefi** sayfasında, yapılandırılan **Soru formu raporu** ER biçimi için bir hedef kayıt ekleyin.
3. **Dosya hedefi** hızlı sekmesinde, yapılandırılan **Soru formu raporu** ER biçiminin kök öğesi olarak [eklenmiş](#AddFormatRootElement) olan **Rapor** biçim bileşeni için **Ekran** [hedefini](er-destination-type-screen.md) ayarlayın.
4. **PDF dönüştürme ayarları** hızlı sekmesinde, bir raporu **Yatay** sayfa yönünü kullanan bir [PDF biçimine](electronic-reporting-destinations.md#OutputConversionToPDF) dönüştürmek için hedefi yapılandırın.

![Elektronik raporlama hedef sayfasındaki ER biçimi için özel Ekran hedefi yapılandırma](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>PDF belgesi olarak önizlemek için uygulamadan bir biçim çalıştırma

1. **Soru formu** \> **Tasarım** \> **Soru formu raporu (ER tarafından desteklenir)** öğesine gidin.
2. İletişim kutusunda, **Biçim eşleme** alanında, **Soru formları raporu**'nu seçin.
3. **Tamam**'ı seçin.
4. **Elektronik rapor parametreleri** iletişim kutusunda **Dahil edilecek kayıtlar** hızlı sekmesinde filtre uygulama seçeneğini yalnızca **SBCCrsExam** soru formu dahil edilecek şekilde yapılandırın.
5. Filtreleme seçeneğini onaylamak için **Tamam**'ı seçin.

    **Hedefler** hızlı sekmesinde, **Çıktı** alanının **Ekran** olarak ayarlanmış olduğuna dikkat edin. Yapılandırılan hedefi değiştirmek istiyorsanız, **Değiştir**'i seçin.

    ![Yapılandırılan hedefi değiştirebileceğiniz ER raporu çalışma zamanı iletişim kutusu](./media/er-quick-start1-run-settings.png)

6. Raporu çalıştırmak için **Tamam**'ı seçin.
7. PDF biçiminde oluşturulan raporu inceleyin.

    ![PDF biçiminde oluşturulan raporunun ekran önizlemesi](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik raporlamada formül dili](er-formula-language.md)
- [Çok dilli raporlar tasarlama](er-design-multilingual-reports.md)
- [ER çerçevesi API'si](er-apis-app73.md)
- [CASE işlevi](er-functions-logical-case.md)
- [CONCATENATE işlevi](er-functions-text-concatenate.md)
- [DATETIMEFORMAT işlevi](er-functions-datetime-datetimeformat.md)
- [FILTER işlevi](er-functions-list-filter.md)
- [FIRSTORNULL işlevi](er-functions-list-firstornull.md)
- [FORMAT işlevi](er-functions-text-format.md)
- [IF işlevi](er-functions-logical-if.md)
- [ORDERBY işlevi](er-functions-list-orderby.md)
- [SESSIONNOW işlevi](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]