---
title: Seçilen dosyalardan verileri toplu iş modunda el ile içeri aktarma
description: Bu konuda, seçilen dosyalardan verilerin toplu iş modunda el ile nasıl içeri aktarılacağı açıklanmaktadır.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075631"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Seçilen dosyalardan verileri toplu iş modunda el ile içeri aktarma

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

[Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesini seçilen gelen dosyalardaki verileri toplu iş modunda el ile içeri aktarmak üzere kullanmak için içeri aktarmayı destekleyen bir ER [biçimi](er-overview-components.md#format-component) yapılandırın. Ardından, bu biçimi veri kaynağı olarak kullanan **Hedef** türü [model eşlemesini](er-overview-components.md#model-mapping-component) çalıştırın. Verileri içeri aktarmak için, içeri aktarmak istediğiniz dosyaya gidin ve el ile seçin. 

Toplu iş modunda veri içeri aktarmayı destekleyen yeni ER özelliği, bu işlemin katılımsız olarak yapılandırılmasını sağlar. ER kullanıcı arabiriminden (UI) yeni bir toplu işlem planlayarak veri içeri aktarma işlemini gerçekleştirmek için ER yapılandırmalarını kullanabilirsiniz.

Bu konuda, el ile seçilen bir dosyadan toplu iş modunda veri içeri aktarma işleminin nasıl tamamlandığı açıklanmaktadır. Örneklerde iş verisi olarak satıcı hareketleri kullanılmaktadır. Bu örneklerin adımları **USMF** şirketinde tamamlanabilir. Kodlama gerekmez.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden biri:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- 1099 ödemeleri için ER biçimi ve model yapılandırmaları

### <a name="create-the-required-er-configurations"></a>Gerekli ER yapılandırmalarını oluşturma

Gerekli ER yapılandırmalarını oluşturmak ve diğer önkoşulları karşılamak için şu adımlardan birini izleyin:

- **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası olan **Bir Microsoft Excel dosyasından ER veri içe aktarma** görev kılavuzlarını oynatın. Bu görev kılavuzları, Microsoft Excel dosyalarından satıcı hareketlerini etkileşimli olarak içe aktarmak için ER yapılandırmalarını tasarlama ve kullanma sürecinde size yol gösterir. Daha fazla bilgi için bkz. [Excel biçiminde gelen belgeleri ayrıştırma](parse-incoming-documents-excel.md).
- [SharePoint'ten veri içeri aktarmayı yapılandırma](er-configure-data-import-sharepoint.md) bölümündeki örnekleri tamamlayın. Bu örnekler, satıcı hareketlerini bir SharePoint klasöründe depolanan Excel dosyalarından etkileşimli olarak içeri aktaran ER yapılandırmalarını tasarlama ve kullanma sürecinde size yol gösterir.

### <a name="download-the-required-er-configurations"></a>Gerekli ER yapılandırmalarını indirme

1. Aşağıdaki ER yapılandırmalarını indirin ve yerel olarak kaydedin.

    | İçerik açıklaması | Dosya |
    |---------------------|------|
    | **1099 Ödemeleri modeli** ER veri modeli yapılandırması | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Satıcıların hareketlerini içeri aktarmak için (Excel)** ER biçimi yapılandırması | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. İndirilen ER yapılandırmalarını aşağıdaki sırayla Dynamics 365 Finance örneğinize içeri aktarmak için [XML dosyasından yükle](er-defer-sequence-element.md#import-the-sample-er-configurations) seçeneğini kullanın:

    1. ER data model configuration
    2. ER format configuration

### <a name="download-the-required-excel-files"></a>Gerekli Excel dosyalarını indirme

- Aşağıdaki örnek veri kümesini indirin ve yerel olarak kaydedin.

    | İçerik açıklaması | Dosya |
    |---------------------|------|
    | Gelen **1099import-data.xlsx** içeri aktarma için örnek veriler içeren dosya | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Önkoşulları gözden geçirin

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, toplu iş modunda veri içeri aktarma için hazırlanan ER çözümünü gözden geçirin.
3. **Satıcıların hareketlerini içeri aktarmak için (Excel)** biçimi yapılandırmasını gözden geçirin.

    - Bu yapılandırmanın biçim bileşeni, gelen Excel dosyasını ayrıştırmak için tasarlanmıştır.
    - Bu yapılandırmanın model eşleme bileşeni, ayrıştırılan Excel dosyasındaki verileri kullanarak temel veri modelini doldurmak için kullanılır.

    ![ER kullanıcı arabiriminden toplu iş modunda veri içeri aktarmak için ER biçimi yapılandırması.](./media/er-configure-data-import-batch-configurations-1.png)

4. **1099 Ödemeleri modeli** veri modeli yapılandırmasını gözden geçirin.

    - Bu yapılandırmanın model bileşeni, çalışan ER bileşenleri arasında veri aktarmak için kullanılan veri modelinin yapısını temsil eder.
    - Bu yapılandırmanın model eşleme bileşeni, yürütülen biçim bileşeninden veri çekmek ve uygulama tablolarını güncelleştirmek için kullanılır.

    ![ER kullanıcı arabiriminden toplu iş modunda veri içeri aktarmak için ER veri modeli yapılandırması.](./media/er-configure-data-import-batch-configurations-2.png)

5. Excel'de **1099import-data.xlsx** dosyasını açın.

    ![Toplu iş modunda içeri aktarabileceğiniz verileri içeren örnek Excel dosyası.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Kullanıcı arabiriminden ER için toplu veri içeri aktarmayı etkinleştirme

1. **Sistem Yönetimi** \> **Çalışma alanları** \> **Özellik yönetimi** seçeneğine gidin.
2. **Özellik yönetimi** çalışma alanında, **El ile yüklenen belgelerin toplu iş modunda ER içeri aktarmasını çalıştır** özelliğini seçin ve ardından **Şimdi etkinleştir**'i seçin.

## <a name="import-data-from-manually-selected-excel-files"></a>El ile seçilen Excel dosyalarından verileri içeri aktarma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, **1099 Ödemeleri modeli** veri modeli yapılandırmasını seçin.
3. **Yapılandırma bileşenleri** Hızlı Sekmesinde, **1099 el ile hareket içeri aktarmak için** bağlantısını seçin.
4. **Modelden veri kaynağına eşleme** sayfasında, **1099 el ile yapılan hareketleri içeri aktarmak için** modeli eşlemesi önceden seçilidir. **Çalıştır**'ı seçin.
5. **Parametreler** sekmesinde **Göz at**'ı seçin. **1099import-data.xlsx** dosyasını bulup seçin ve **Tamam**'ı seçin.
6. **Fiş kodunu girin** alanına **V-00001** girin.
7. **Arka planda çalıştır** sekmesinde, **Toplu işleme** öğesini **Evet** olarak ayarlayın.

    **Görev açıklaması** alanının **"1099 el ile hareket içeri aktarmak için" model eşlemesini çalıştırma yapılandırması '1099 Ödemeler modeli'** olarak ayarlandı. Bu değer, seçili model eşlemesinin yürütülmesinin yeni bir toplu işlem olarak zamanlanacağını gösterir.

    ![Elektronik rapor parametreleri iletişim kutusunda toplu iş modunda veri içeri aktarma ayrıntılarını belirtme.](./media/er-configure-data-import-batch-execution-parameters.png)

8. **Tamam**'ı seçin. Yeni bir toplu işlemin zamanlandığını bildiren bir ileti.

    ![Modelden veri kaynağına eşleme sayfasında yeni bir zamanlanmış toplu işlemle ilgili ileti.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Toplu İşlem sayfasında veri içeri aktarma sonuçlarını gözden geçirme

1. **Ortak** \> **Sorgular** \> **Toplu işler** \> **Toplu işlerim**'e gidin.
2. **Toplu İşlem** sayfasında, zamanlanan toplu işlemi bulmak için toplu işlerin listesine filtre uygulayın ve seçin.
3. İş ayrıntılarını gözden geçirmek için **İş Kimliği** bağlantısını seçin.
4. **Toplu iş görevleri** hızlı sekmesinde, **Günlük**'ü seçin.

    ![Toplu İşlem sayfasındaki Günlük düğmesi.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Yürütme ayrıntılarını gözden geçirin.

    ![Toplu İşlem sayfasında zamanlanan toplu işlemin yürütme günlüğü.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Veri içeri aktarma parametrelerini değiştirme

Toplu işleminiz zamanlandıktan sonra henüz çalıştırılmamış olsa da, zamanlanmış veri içeri aktarma parametrelerini değiştirebilirsiniz.

1. **Ortak** \> **Sorgular** \> **Toplu işler** \> **Toplu işlerim**'e gidin.
2. **Toplu İşlem** sayfasında, zamanlanan toplu işlemi bulmak için toplu işlerin listesine filtre uygulayın ve seçin.
3. **Durumu değiştir**'i seçin.
4. **Yeni durum seç** iletişim kutusunda, **Tut**'u seçin ve sonra **Tamam**'ı seçin.
5. İş ayrıntılarına erişmek için **İş Kimliği** bağlantısını seçin.
6. **Toplu iş görevleri** hızlı sekmesinde, **Parametreler**'i seçin.
7. **Elektronik rapor parametreleri** iletişim kutusunda şu adımları izleyin:

    1. Veri içeri aktarma için alternatif dosyayı seçmek üzere **Göz at**'ı seçin.
    2. Satıcı hareketlerini içeri aktarma fiş numarasını değiştirmek için **Fiş kodunu girin**'i seçin.

        ![Elektronik rapor parametreleri iletişim kutusunda zamanlanmış toplu işlem için veri içeri aktarma parametrelerini değiştirme.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. **Tamam**'ı seçin.

8. Toplu işlemin hala seçili olduğundan emin olun ve sonra **Durumu değiştir**'i yeniden seçin.
9. **Yeni durum seç** iletişim kutusunda, **Bekliyor**'u seçin ve sonra **Tamam**'ı seçin.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>ER kaynak sayfasında veri içeri aktarma sonuçlarını gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama kaynağı**'na gidin.
2. Veri içeri aktarma sırasında otomatik olarak oluşturulan **Satıcıların hareketlerini (Excel) içeri aktarmak için** kaydını seçin.

    ![Elektronik raporlama kaynağı sayfasındaki Satıcıların hareketlerini içeri aktarma (Excel) yapılandırması için kayıt.](./media/er-configure-data-import-batch-files-source-1.png)

3. **Kaynakların dosya durumları**'nı seçin.
4. **Dosyalar** ve **İçeri aktarma biçimi için kaynak günlükleri** hızlı sekmelerinde içeri aktarma ayrıntılarını gözden geçirin.
5. **Dosyalar** Hızlı Sekmesinde kaydı seçin. İçe aktarılan dosyanın bu kayda iliştirilmiş olduğuna dikkat edin.

    ![Kaynaklar sayfasının Dosya durumlarındaki kayda iliştirilmiş içeri aktarılan dosya.](./media/er-configure-data-import-batch-files-source-2.png)

6. İçeri aktarılan dosyayı gözden geçirmek için **Ekler**'i seçin.

    ![Belge görünümü sayfasında içeri aktarılan dosya.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Bu ekleri tutmak için ER çerçevesi, ER parametrelerinin **Diğerleri** alanında geçerli şirket için [ayarlanan](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) bir belge türü kullanır.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>1099'lar için Satıcı kapatma sayfasındaki veri içeri aktarma sonuçlarını gözden geçirme

1. **Borç hesapları** \> **Periyodik görevler** \> **Vergi 1099** \> **1099 formlarına ilişkin satıcı kapatması**'na gidin.
2. **Başlangıç tarihi** alanına **12/31/2017** (31 Aralık 2017) girin.
3. **El ile 1099 hareketleri**'ni seçin.

    ![Vergi 1099 hareketleri sayfasında içeri aktarılan satıcı hareketleri.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
