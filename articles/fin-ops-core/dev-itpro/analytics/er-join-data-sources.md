---
title: Birden çok uygulama tablosundan veri almak için ER model eşlemelerinde BİRLEŞTİRME veri kaynaklarını kullanma
description: Bu makalede, Elektronik raporlamada (ER) JOIN türü veri kaynaklarını nasıl kullanabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 0994c19ad79a3e73dc787ef8d82716db637f9ab0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845555"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Birden çok uygulama tablosundan veri almak için Elektronik raporlama (ER model) eşlemelerinde BİRLEŞTİRME veri kaynaklarını kullanma

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) modeli eşlemelerini veya biçimlerini yapılandırırken **Birleştirme** türündeki gerekli veri kaynaklarını [ekleyebilirsiniz](#review). Tasarım zamanında, **Birleştirme** veri kaynağı her biri kayıt listesi döndüren birkaç veri kaynağı kümesi olarak yapılandırılır. İlki dışında her veri kaynağı için, geçerli ve önceki veri kaynaklarındaki kayıtlara katılmak üzere gerekli koşulları tanımlamanız gerekir. Çalışma zamanında, **Birleştirme** türündeki yapılandırılmış veri kaynağı, iç içe gerçmiş veri kaynağı kayıtlarından alanlar içeren tek bir birleştirilmiş kayıt listesi [döndürür](#executeERformat).

Şu anda aşağıdaki birleştirme türleri desteklenmektedir:

- Dış (sol) birleştirme:
    - Birinci (en sol) veri kaynağının tüm kayıtlarını ve sonra da ikinci (en sağ) veri kaynağının yapılandırılmış koşul kayıtlarına uygun şekilde eşleşen tüm kayıtlarını birleştirin.
- İç (sağ) birleştirme:
    - Yalnızca birinci (en sol) veri kaynağının kayıtlarını ve sonra da yalnızca ikinci (en sağ) veri kaynağının yapılandırılmış koşullara uygun şekilde eşleşen kayıtlarını birleştirin.

Yapılandırılan **Birleştir** veri kaynağında, tüm veri kaynakları **Tablo kayıtları** türünde olduğunda, Birleştir veri kaynağını yürütme işlemi tek bir SQL deyimi kullanılarak [veritabanı düzeyinde gerçekleştirilebilir](#analyze). Bu ifade, veritabanı çağrılarının sayısını azaltarak model eşleme performansını artırır. Aksi durumda, **Birleştir** veri kaynağının yürütülmesi bellekte gerçekleştirilir.

> [!NOTE]
> Birleştir türünün veri kaynaklarındak kayıtları birleştirmek için koşulları belirten ER ifadelerinde **VALUEIN** işlevinin kullanılması henüz desteklenmemektedir. Bu işlev hakkında daha fazla ayrıntı için [Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md) sayfasını ziyaret edin.

Bu özellik hakkında daha fazla bilgi edinmek için bu makaledeki örneği tamamlayın.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Örnek: ER model eşlemelerinde BIRLEŞTIRME veri kaynaklarını kullanma

Aşağıdaki adımlarda, veri erişimi performansını geliştirmek üzere Sistem Yöneticisi veya Elektronik raporlama geliştiricisinin **Birleştirme** türü veri kaynaklarını kullanarak bir seferde çoklu uygulama tablolarından veri almak üzere nasıl Elektronik raporlama (ER) model eşlemesi yapılandırabileceği anlatılmaktadır. Bu adımlar herhangi bir Dynamics 365 Finance şirketi veya Regulatory Configuration Services (RCS) için gerçekleştirilebilir.

### <a name="prerequisites"></a>Ön Koşullar

Bu makaledeki örnekleri tamamlamak için, bu adımları tamamlamak amacıyla hangi hizmetin kullanıldığına bağlı olarak aşağıdakilerden birine erişiminizin olması gerekir:

**Aşağıdaki rollerden biri için Finance'a erişim:**

- Elektronik raporlama geliştirici
- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

**Aşağıdaki rollerden biri için RCS'ye erişim:**

- Elektronik raporlama geliştirici
- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

Ayrıca, öncelikle [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlamanız gerekir.

Önceden, aşağıdaki örnek ER yapılandırma dosyalarını da indirip kaydetmeniz gerekir:

| **İçerik açıklaması**  | **Dosya adı**   |
|--------------------------|-----------------|
| Örnekler için veri kaynağı olarak kullanılan **ER veri kaynağı** yapılandırma dosyası.| [Model to learn JOIN data sources.version.1.1.xml](https://download.microsoft.com/download/5/c/1/5c1d8a57-6ebd-425b-bc5d-c71dde92c6af/ModeltolearnJOINdatasources.version.1.xml) |
| Örnekler için ER veri modelini uygulayan örnek **ER model eşleme** yapılandırma dosyası. | [Mapping to learn JOIN data sources.version.1.1.xml](https://download.microsoft.com/download/9/2/f/92f339ca-41fc-4f5e-b458-6983c957d3dd/MappingtolearnJOINdatasources.version.1.1.xml)|
| Örnek **ER biçimi** yapılandırma dosyası. Bu dosya, örnekler için ER biçim bileşenini doldurmak üzere verileri tanımlar. | [Format to learn JOIN data sources.version.1.1.xml](https://download.microsoft.com/download/f/f/8/ff8f1b48-14d0-4c73-9145-bcdf8b5265bc/FormattolearnJOINdatasources.version.1.1.xml) |

### <a name="activate-a-configurations-provider"></a>Bir yapılandırma sağlayıcısını etkinleştirme

1. Web tarayıcınızın ilk oturumunda Finance veya RCS'ye erişin.
2. **Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.
3. **Yerelleştirme yapılandırmaları** sayfasındaki **Yapılandırma sağlayıcıları** bölümünde, [Litware, Inc.](http://www.litware.com) örnek şirketine ait yapılandırma sağlayıcısının listelendiğinden ve **Etkin** olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) adımlarını takip edin.

    ![Elektronik raporlama çalışma alanı.](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Örnek ER biçimi yapılandırma dosyalarını içe aktarma

1. **Raporlama yapılandırmaları**'nı seçin.
2. ER veri modeli yapılandırma dosyasını içe aktarın.
    1. **Döviz**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. **Model to learn JOIN data sources.version.1.1.xml** dosyasını bulmak için **Gözat**'ı seçin.
    4. **Tamam**'ı seçin.
3. ER model eşleme yapılandırma dosyasını içeri aktarın.
    1. **Döviz**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. **Mapping to learn JOIN data sources.version.1.1.xml** dosyasını bulmak için **Gözat**'ı seçin.
    4. **Tamam**'ı seçin.
4. ER biçimi yapılandırma dosyasını içe aktarın.
    1. **Döviz**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. **Format to learn JOIN data sources.version.1.1.xml** dosyasını bulmak için **Gözat**'ı seçin.
    4. **Tamam**'ı seçin.
5. Yapılandırmalar ağacında, **BİRLEŞTİR veri kaynaklarını öğrenme modeli** öğesini ve diğer model öğelerini (varsa) genişletin.
6. Ağaçtaki ER yapılandırmalarının listesini ve **Sürümler** hızlı sekmesindeki sürüm ayrıntılarını inceleyin: bunlar, örnek raporunuz için veri kaynağı olarak kullanılırlar.

    ![Elektronik raporlama yapılandırmaları sayfası.](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Yürütme izleme seçeneklerini açma

1. **YAPILANDIRMALAR**'ı seçin.
2. **Kullanıcı parametreleri**'ni seçin.
3. Yürütme izleme parametrelerini aşağıdaki ekran görüntüsünde gösterildiği gibi ayarlayın.

    ![Elektronik raporlama kullanıcı parametreleri sayfası.](./media/GER-JoinDS-Parameters.PNG)

    Bu parametreler açık olduğunda, içe aktarılan ER biçim dosyasını her yürütme işlemi için yürütme izlemesi oluşturulur. Oluşturulan yürütme izlemenin ayrıntılarını kullanarak, ER biçiminin ve ER model eşleme bileşenlerinin yürütülmesini çözümleyebilirsiniz. ER yürütme izleme özelliği hakkında daha fazla ayrıntı için [Performans sorunlarını gidermek için ER biçimi yürütmesini izleme](trace-execution-er-troubleshoot-perf.md) sayfasını ziyaret edin.

### <a name="review-er-model-mapping-part-1"></a>ER model eşlemesini gözden geçirme (Bölüm 1)

ER model eşleme bileşeninin ayarlarını inceleyin. Bileşen, **Birleştirme** türünün veri kaynaklarını kullanmadan ER yapılandırmalarının, yapılandırma ayrıntılarının ve yapılandırma sağlayıcılarının sürümleriyle ilgili bilgilere erişmek için yapılandırılmıştır.

1. **Mapping to learn JOIN data sources** yapılandırmasını seçin.
2. Eşleme listesini açmak için **Tasarımcı**'yı seçin.
3. Eşleme ayrıntılarını gözden geçirmek için **Tasarımcı**'yı seçin.
4. **Ayrıntıları göster**'i seçin.
5. Yapılandırmalar ağacında,**Set1** ve **Set1.Details** veri modeli öğelerini genişletin:

    1. Bağlama **Ayrıntılar: Kayıt listesi = Sürümler** **Set1.Details** öğesinin, **ERSolutionVersionTable** tablosunun kayıtlarını döndüren **Sürümler** veri kaynağına bağlı olduğunu gösterir. Bu tablonun her kaydı bir ER yapılandırmasının tek bir sürümünü temsil eder. Bu tablonun içeriği, **Yapılandırmalar** sayfasındaki **Sürümler** hızlı sekmesinde gösterilir.
    2. **ConfigurationVersion: String = @.PublicVersionNumber** bağlamasıher ER yapılandırması sürümünün genel sürümünün değerinin **ERSolutionVersionTable** tablosunun **PublicVersionNumber** alanından alındığı ve **ConfigurationVersion** öğesine yerleştirildiği anlamına gelir.
    3. **ConfigurationTitle: String = @.'>Relations'.Solution.Name** bağlaması, ER yapılandırması adının **ERSolutionTable** tablosunun **Ad** alanından alındığı ve (**'>İlişkiler'**) ile **ERSolutionVersionTable** ve **ERSolutionTable** tabloları arasında çoktan bire ilişkisinin kullanıldığı anlamına gelir. Geçerli uygulama örneğinin ER yapılandırmalarının adları, **Yapılandırmalar** sayfasındaki yapılandırmalar ağacında gösterilir.
    4. **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** bağlaması, geçerli yapılandırmanın sahibi olan yapılandırma sağlayıcısı adının **ERVendorTable** tablosunun **Ad** alanından alındığı ve **ERSolutionTable** ile **ERVendorTable** tabloları arasında çoktan bire ilişkisinin kullanıldığı anlamına gelir. ER yapılandırma sağlayıcısı adları, her yapılandırmanın sayfa başlığında **Yapılandırmalar** sayfasındaki yapılandırmalar ağacında gösterilir. Tüm ER yapılandırma sağlayıcıları listesi, **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırma sağlayıcısı** tablosu sayfasında bulunabilir.

    ![ER model eşleme tasarımcısı sayfası, bağlı veri modeli öğeleri.](./media/GER-JoinDS-Set1Review.PNG)

6. Yapılandırmalar ağacında, **Set1.Summary** veri modeli öğesini genişletin:

    1. **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** bağlaması, **Set1.Summary.VersionsNumber** öğesinin, **Versions**  veri kaynağı aracılığıyla **ERSolutionVersionTable** tablosunun kayıt sayısını döndürmek üzere yapılandırılan **GroupBy** türündeki  **VersionsSummary** veri kaynağının **VersionsNumber** toplam alanına bağlı olduğunu gösterir.

    !["Gruplandırma Ölçütü" parametreleri sayfasını düzenleme.](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. Sayfayı kapatın.

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a> ER model eşlemesini gözden geçirme (Bölüm 2)

ER model eşleme bileşeninin ayarlarını inceleyin. Bileşen, **Birleştirme** türü veri kaynağı kullanılarak ER yapılandırmalarının, yapılandırma ayrıntılarının ve yapılandırma sağlayıcılarının sürümleriyle ilgili bilgilere erişmek için yapılandırılmıştır.

1. Yapılandırmalar ağacında,**Set2** ve **Set2.Details** veri modeli öğelerini genişletin: **Details: Record list = Details** bağlaması **Set2.Details** öğesinin **Birleştir** türünün veri kaynağı olarak yapılandırılan **Ayrıntılar** veri kaynağına bağlı olduğunu belirtir.

    ![Genişletilmiş Set2:Record veri modeli öğelerini gösteren ER model eşleme tasarımcı sayfası.](./media/GER-JoinDS-Set2Review.PNG)

    **Birleştir** veri kaynağı, **Functions\Join** veri kaynağı seçilerek eklenebilir:

    ![ER model eşleme tasarımcı sayfası, Join veri kaynağı türü.](./media/GER-JoinDS-AddJoinDS.PNG)

2. **Ayrıntılar** veri kaynağını seçin.
3. **Veri kaynakları** bölmesinde **Düzenle**'yi seçin.
4. **Birleştirmeyi düzenle** öğesini seçin.
5. **Ayrıntıları göster**'i seçin.

    ![BİRLEŞTİR veri kaynağı parametreleri sayfası.](./media/GER-JoinDS-JoinDSEditor.PNG)

    Bu sayfa, **Birleştirme türünün** gerekli veri kaynağını tasarlamak için kullanılır. Bu veri kaynağı çalışma zamanında, **Birleştirilmiş liste** kılavuzundaki veri kaynaklarından alınan tek bir birleşik kayıt listesi oluşturur. Kayıtların birleştirilmesi, kılavuzda ilk olarak bulunan **ConfigurationProviders** veri kaynağından başlar ( **Tür** sütunu boştur). Diğer tüm veri kaynağı kayıtları, sonuç olarak bu kılavuzdaki sırasına dayalı olarak üst veri kaynağının kayıtlarına birleştirilir. Birleşen her bir veri kaynağı hedef veri kaynağı altında iç içe geçmiş bir veri kaynağı olarak yapılandırılmalıdır (`1Versions` veri kaynağı `1Configurations` bir altında iç içe geçmiştir; `1Configurations` veri kaynağı **ConfigurationProviders** bir altında iç içe geçmiştir). Yapılandırılan her veri kaynağının birleşim koşullarını içermesi gerekir. Bu özel **birleştirme** için veri kaynağında aşağıdaki birleştirmeler tanımlanmıştır:

    - **ConfigurationProviders** veri kaynağının her kaydı (**ERVendorTable** tablosuna başvuruda bulunulan) yalnızca **1Configurations** bir kayıtlarıyla (**ERSolutionTable** tablosunda başvuruda bulunulan) birleştirilir, **SolutionVendor** ve **RecId** alanlarında ayrı değer bulunur. **İç birleştirme** türü, bu birleşim için ve aynı zamanda eşleşen kayıtlar için aşağıdaki koşulları kullanır:

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - **1Configurations** veri kaynağının her kaydı (**ERSolutionTable** tablosuna başvuruda bulunulan) yalnızca **1Versions** bir kayıtlarıyla (**ERSolutionVersionTable** tablosunda başvuruda bulunulan) birleştirilir, **Solution** ve **RecId** alanlarında ayrı değer bulunur. **İç birleştirme** türü, bu birleşim için ve aynı zamanda eşleşen kayıtlar için aşağıdaki koşulları kullanır:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - **Yürüt** seçeneği **Sorgu** olarak yapılandırılmıştır; bu birleştirme veri kaynağının doğrudan SQL çağrısı olarak veritabanı düzeyinde çalışma zamanında yürütüleceği anlamına gelir.

    Uygulama tablolarını temsil eden veri kaynaklarının kayıtlarının birleştirilmesi için, bu tablolar arasındaki AOT ilişkilerini açıklayan mevcut koşullar dışında alan çiftlerini kullanarak birleştirme koşulları belirtebilirsiniz. Bu birleşim türü veritabanı düzeyinde de yürütülecek şekilde yapılandırılabilir.

6. Sayfayı kapatın.
7. **İptal**'i seçin.
8. Yapılandırmalar ağacında, **Set2.Summary** veri modeli öğesini genişletin:

    - **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** bağlaması, **Set2.Summary.VersionsNumber** öğesinin, **Join** türünün **Ayrıntılar** veri kaynağının birleştirilmiş kayıt sayısını döndürmek üzere yapılandırılmış **GroupBy** türündeki **DetailsSummary** veri kaynağının **DetailsSummary** toplam alanına bağlı olduğunu gösterir.
    - **Yürüt** konumu **Sorgu** olarak yapılandırılmıştır. Bu **GroupBy** veri kaynağının doğrudan SQL çağrısı olarak veritabanı düzeyinde çalışma zamanında çalıştırılacağı anlamına gelir. Bu davranış, **Birleştirme** türünün temel veri kaynağı **Ayrıntılar** veritabanı düzeyinde yürütülmek üzere yapılandırıldığı için mümkündür.

    ![GROUPBY veri kaynağı parametreleri sayfası.](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. Sayfayı kapatın.
10. **İptal**'i seçin.

### <a name="execute-er-format"></a><a name="executeERformat"></a> ER biçimi yürüt

1. Web tarayıcınızın ikinci oturumunda, ilk oturumda olduğu gibi aynı kimlik bilgilerini ve şirketi kullanarak Finance veya RCS'ye erişin.
2. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
3. **Model to learn JOIN data sources** yapılandırmasını genişletin.
4. **Format to learn JOIN data sourcesl** yapılandırmasını seçin.
5. **Tasarımcı**’yı seçin.
6. **Ayrıntıları göster**'i seçin.
7. **Eşleme**'yi seçin.
8. **Genişlet/Daralt**'ı seçin.

    Bu biçim, ER yapılandırmasının her sürümü için yeni bir satırla (**Sürüm** sırası) oluşturulan bir metin dosyasını doldurmak üzere tasarlanmıştır. Oluşturulan her satır, geçerli yapılandırmanın sahibi olan yapılandırma sağlayıcısının adını, yapılandırma adını ve noktalı virgülle ayrılmış yapılandırma sürümünü içerir. Oluşturulan dosyanın son satırı, ER yapılandırmalarının keşfedilen sürümlerinin sayısını (**Özet** sırası) içerecektir.

    ![ER biçimi tasarım sayfası, Biçim sekmesi.](./media/GER-JoinDS-FormatReview.PNG)

    **Veri** ve **Özet** veri kaynakları, oluşturulan dosyada yapılandırma sürümü ayrıntılarını doldurmak için kullanılır:

    - **Set1** veri modelinden alınan bilgiler, ER biçimini çalıştırırken Kullanıcı iletişim kutusu sayfasındaki çalışma zamanından **Seçici** veri kaynağı için **Hayır**'ı seçtiğinizde kullanılır.
    - **Set2** veri modelinden alınan bilgiler, Kullanıcı iletişim kutusu sayfasındaki çalışma zamanından **Seçici** veri kaynağı için **Evet**'i seçtiğinizde kullanılır.

    ![ER biçimi tasarım sayfası, Eşleme sekmesi.](./media/GER-JoinDS-FormatMappingReview.PNG)

9. **Çalıştır**'ı seçin.
10. İletişim sayfasında, **BİRLEŞTİR veri kaynağını kullan** alanında **Hayır**'ı seçin.
11. **Tamam**'ı seçin.
12. Oluşturulan dosyaları gözden geçirin.

    ![JOIN veri kaynağı kullanılmadan, elektronik rapor parametreleriyle oluşturulan dosya.](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>ER biçimi yürütme izlemesini analiz etme

1. Finance veya RCS'nin ilk oturumunda **Tasarımcı**'yı seçin.
2. **Performans izleme**'yi seçin.
3. **Performans izleme** kılavuzunda, geçerli model eşleme bileşenini kullanan bir ER biçiminin en son yürütme izlemesini en üstteki kayıt olarak seçin.
4. **Tamam**'ı seçin.

    Yürütme istatistikleri, uygulama tablolarındaki yinelenen çağrılar hakkında bilgi verir:

    - **ERSolutionTable** **ERSolutionVersionTable** tablosundaki yapılandırma sürümü kaydı sayısı kadar çağrılır. Bu tür çağrıların sayısı performansı geliştirmek için zaman olarak azaltılabilir.
    - **ERVendorTable** **ERSolutionVersionTable** tablosunda keşfedilen her kayıt sürümü için iki kez çağrılır. Bu tür çağrıların sayısı da performansı geliştirmek için azaltılabilir.

    ![ER Model eşleme tasarımcı sayfasındaki yürütme istatistikleri.](./media/GER-JoinDS-Set1Run2.PNG)

5. Sayfayı kapatın.

### <a name="execute-er-format"></a>ER biçimi yürütme

1. Finance veya RCS'nin ikinci oturumuyla web tarayıcı sekmenizi değiştirin.
2. **Çalıştır**'ı seçin.
3. İletişim sayfasında, **BİRLEŞTİR veri kaynağını kullan** alanında **Evet**'i seçin.
4. **Tamam**'ı seçin.
5. Oluşturulan dosyaları gözden geçirin.

    ![JOIN veri kaynağı kullanılarak elektronik rapor parametreleriyle oluşturulan dosya.](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> ER biçimi yürütme izlemesini analiz etme

1. Finance veya RCS'nin ilk oturumunda **Tasarımcı**'yı seçin.
2. **Performans izleme**'yi seçin.
3. **Performans izleme** kılavuzunda, geçerli model eşleme bileşenini kullanan bir ER biçiminin en son yürütme izlemesini temsil eden en üstteki kaydı seçin.
4. **Tamam**'ı seçin.

    İstatistikler size aşağıdakiler hakkında bilgi verir:

    - Uygulama veritabanı, gerekli alanlara erişmek için **ERVendorTable**, **ERSolutionTable** ve **ERSolutionVersionTable** tablolarından kayıtlar almak üzere bir kez çağrıldı.

    ![ER Model eşleme tasarımcı sayfasındaki performans istatistikleri detayları.](./media/GER-JoinDS-Set2Run2.PNG)

    - **Ayrıntılar** veri kaynağında yapılandırılan birleştirmeler kullanılarak, yapılandırma sürümü sayısını hesaplamak üzere uygulama veritabanı bir kez çağrıldı.

    ![Uygulama veritabanı çağrılarını gösteren ER Model eşleme tasarımcı sayfası.](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>Sınırlamalar

Bu makaledeki örnekte görebileceğiniz gibi, **JOIN** veri kaynağı, birleştirilmesi gereken kayıtların ayrı veri kümelerini açıklayan birçok veri kaynağından oluşturulabilir. Bu veri kaynaklarını, yerleşik ER [FİLTRESİ](er-functions-list-filter.md) işlevini kullanarak yapılandırabilirsiniz. Veri kaynağını **BİRLEŞTİR** veri kaynağının dışında çağrılacak şekilde yapılandırdığınızda, şirket aralıklarını veri seçimi koşulunun parçası olarak kullanabilirsiniz. **BİRLEŞTİR** veri kaynağının başlangıç uygulaması bu türdeki veri kaynaklarını desteklemez. Örneğin, [FİLTRE](er-functions-list-filter.md) tabanlı bir veri kaynağını **BİRLEŞTİR** veri kaynağının yürütme kapsamı içinde çağırdığınızda, çağrılan veri kaynağı veri seçimi koşulunun bir parçası olarak şirket aralıklarını içeriyorsa, özel durum oluşur.

Microsoft Dynamics 365 Finance 10.0.12 sürümünde (2020 Ağustos) şirket aralıklarını, **JOIN** veri kaynağı yürütme kapsamında çağrılan [FILTER](er-functions-list-filter.md) tabanlı birleştirme veri kaynağında veri seçimi koşulunun bir parçası olarak kullanabilirsiniz. Uygulama [sorgu](../dev-ref/xpp-library-objects.md#query-object-model)oluşturucusunun sınırlamaları nedeniyle, şirket aralıkları **BİRLEŞTİR** veri kaynağının yalnızca ilk veri kaynağı için desteklenir.

### <a name="example"></a>Örnek

Örneğin, birden fazla şirketin yurt dışı ticari hareket listelerini ve bu hareketlerde başvurulan stok maddesinin ayrıntılarını almak için uygulama veritabanına tek bir çağrı yapmanız gerekir.

Bu durumda, aşağıdaki yapıları ER model eşlemenizde yapılandırırsınız:

- **Intrastat** tablosunu gösteren **Intrastat** kök veri kaynağı.
- **InventTable** tablosunu gösteren **Maddeler** kök veri kaynağı.
- Hareketlere erişilmesi gereken şirket listesini döndüren **Şirketler** kök veri kaynağı ( bu örnekte **DEMF** ve **GBSI**), hareketlerin erişilmesi gereken şirket kök veri kaynağı. Şirket kodu, **Companies.Code** alanından alınabilir.
- `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))` ifadesine sahip **X1** kök veri kaynağı. Veri seçimi koşulunun bir parçası olarak bu ifade şirket aralıklarının tanımını içerir `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.
- **X1** veri kaynağının iç içe geçmiş bir öğesi olarak **X2** veri kaynağı. `FILTER (Items, Items.ItemId = X1.ItemId)` ifadesini içerir.

Son olarak, **X1**'in ilk veri kaynağı ve **X2**'nin ikinci veri kaynağı olduğu bir **BİRLEŞTİR** veri kaynağı yapılandırabilirsiniz. **Sorgu**'yu, ER'yi bu veri kaynağını doğrudan bir SQL çağrısı olarak veritabanı düzeyinde çalıştırmaya zorlamak için **Yürüt** seçeneği olarak belirtebilirsiniz.

Yapılandırılan veri kaynağı ER yürütmesi [izlenirken](trace-execution-er-troubleshoot-perf.md) çalıştırıldığında, ER model eşleme tasarımcısında ER performans izlemesenin bir parçası olarak aşağıdaki ifade gösterilir.

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> Yapılandırılmş bir **BİRLEŞTİR** veri kaynağı çalıştırısanız bir hata oluşur; bu, yürütülen **BİRLEŞTİR** veri kaynağının ek veri kaynakları için şirket aralıkları olan veri seçimi koşullarını içerir.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Performans sorunlarını gidermek için ER biçimi yürütülmesini izle](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
