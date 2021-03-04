---
title: Elektronik raporlama ile testi otomatikleştirme
description: Bu konu, işlevsellik testini otomatikleştirmek için Elektronik raporlama (ER) çerçevesinin temel özelliğini nasıl kullanabileceğinizi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0a2586afd56eef0f953454ad246ff3647a5b09d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681460"
---
# <a name="automate-testing-with-electronic-reporting"></a>Elektronik raporlama ile testi otomatikleştirme

[!include[banner](../includes/banner.md)]

Bu konu, işlevsellik testini otomatikleştirmek için Elektronik raporlama (ER) çerçevesini nasıl kullanabileceğinizi açıklar. Bu konudaki örnekte, satıcı ödeme işlemi testinin nasıl otomatikleştirildiği gösterilmektedir.

Uygulama, satıcı ödeme işlemi sırasında ödeme dosyaları ve ilgili belgeler oluşturmak için ER çerçevesini kullanır. ER çerçevesi, farklı ödeme tipleri ve farklı biçimlerdeki belgelerin oluşturulması için ödeme işlemeyi destekleyen bir veri modeli, model eşleme ve biçim bileşenlerini içerir. Bu bileşenler Microsoft Dynamics Lifecycle Services (LCS)'den yüklenebilir ve örneğe aktarılabilir.

Ayrıca, her bir Microsoft bileşenini özelleştirebilir ve kendi özel bileşeninizin temeli olarak kullanabilirsiniz. Özel bir sürüm oluşturarak, belirli gereksinimleri destekleyen değişiklikler yapabilirsiniz. Örneğin, müşteriye özel uygulama verilerine erişmek için ER veri modelini ve ER model eşleştirmesini ayarlayabilirsiniz veya bir ER. oluşturulan bir belgenin düzenini değiştirmek için bir ER biçimini değiştirebilirsiniz.

Satıcı ödemeleri oluşturan ve ayrıca kontrol raporlarını işleyen ödeme dosyalarını işlemek için örneğinizdeki özelleştirilmiş ER biçimlerini kullanabilirsiniz. Sürüm Oluşturma ER bileşenlerinde desteklenir. Bu nedenle, Microsoft, satıcı ödeme işlemesi için ER çözümlerinin güncelleştirilmiş sürümlerini sağlayabilir ve güncelleştirilmiş sürümü otomatik olarak yeniden temelleyerek özelleştirilmiş bileşeniniz ile birleştirebilirsiniz. Ancak, beklediğiniz gibi çalıştığından emin olmak için yeniden temel sürümü test etmeniz gerekir.

ER veri modelleri ve ER model eşleştirmeleri, farklı türlerdeki ödemeleri işlemek ve ülkeye/bölgeye özel ödeme belgeleri oluşturmak için kullanılan birçok ER biçiminde ortaktır. Bu nedenle, birden çok şirket için otomatik olarak gerçekleştirilmesi için kullanıcı kabulü ve tümleştirme testini otomatikleştirmek istenir, ancak her bir hedef şirketin ülke/bölge bağlamını dikkate alır, farklı veri kümeleri kullanır, vb. .

Bir yapılandırma sağlayıcısından aldığınız biçime göre bir biçimin özel sürümünün nasıl oluşturulduğu hakkında daha fazla bilgi için [ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.](./tasks/er-upgrade-format.md)'e bakın.

## <a name="key-concepts"></a>Kilit kavramlar

İşlevsel yetkili kullanıcılar, kaynak kodu yazmak zorunda kalmadan kullanıcı kabul ve tümleştirme testini yazabilir.

- Oluşturulan belgeleri ana kopyalara karşılaştırmak için ER temel özelliğini kullanın. Daha fazla bilgi için [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md)'ya bakın.
- Test olaylarını kaydetmek ve temel değerlendirmeyi dahil etmek için görev kaydediciyi kullanın. Daha fazla bilgi için bkz. [Görev kaydedici kaynakları](../user-interface/task-recorder.md).
- Gerekli test senaryoları için grup test durumları. Daha fazla bilgi için bkz. [Kullanıcı kabul testleri oluşturma ve otomatikleştirme](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Kullanıcı kabul testleri için kitaplıklar oluşturmak amacıyla LCS'de İş süreci Modelleyicisi'ni (BPM) kullanın.
    - Microsoft Azure DevOps Services (Azure DevOps) içinde bir test planı ve test paketleri oluşturmak için BPM test kitaplıklarını kullanın.

İşlevsel yetkili kullanıcılar kullanıcı kabul ve bütünleştirme testlerini çalıştırabilir.

- İstenen test paketinin test çalışmalarını çalıştırmak için Regression Suite Automation Tool (RSAT)'u kullanın.
- Testin sonuçlarını Azure DevOps'a rapor edin ve bu sonuçları araştırmak için bu hizmeti kullanın.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki görevleri tamamlayabilmek için önce aşağıdaki ön koşulları tamamlamanız gerekir:

- Test otomasyonunu destekleyen bir topoloji dağıtın. **Sistem Yöneticisi** rolü Için bu topolojinin örneğine erişiminizin olması gerekir. Bu topoloji, bu örnekte kullanılacak demo verilerini içermelidir. Daha fazla bilgi için bkz. [Sürekli oluşturma ve test otomasyonunu destekleyen bir ortam dağıtma ve kullanma](../perf-test/continuous-build-test-automation.md).
- Kullanıcı kabul ve tümleştirme testlerini otomatik olarak çalıştırmak için RSAT'ı kullandığınız topolojiye yüklemeli ve uygun şekilde yapılandırmalısınız. RSAT'ı yükleme ve Finance and Operations uygulamaları ve Azure DevOps ile birlikte çalışacak şekilde yapılandırma hakkında daha fazla bilgi için bkz. [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Aracı kullanma ile ilgili ön koşullara dikkat edin. Aşağıdaki çizim, RSAT ayarları örneğini gösterir. Mavi dikdörtgen, Azure DevOps'a erişimi belirleyen parametreleri barındırır. Yeşil dikdörtgen, örneğe erişimi belirten parametreleri barındırır.

    ![RSAT ayarları](media/GER-Configure.png "RSAT Ayarları iletişim kutusunun ekran görüntüsü")

- Daha fazla raporlama ve inceleme için test olaylarının günlüklerini toplayabilmek amacıyla, paketlerdeki test yürütmelerini, doğru yürütme sırasının sağlanmasına yardımcı olmak için organize etmek amacıyla, topolojiden dağıtılmış Azure DevOps'a erişiminiz olmalıdır.
- Bu konudaki örneği tamamlamak için [RSAT testleri için ER kullanımı](https://go.microsoft.com/fwlink/?linkid=874684)'nı indirmenizi öneririz. Bu zip dosyası aşağıdaki görev kılavuzlarını içerir:

    | İçerik                                           | Dosya adı ve yer |
    |---------------------------------------------------|------------------------|
    | Test için veri hazırlamak üzere örnek görev kaydı | \\Recording.xml hazırlama |
    | Satıcı ödemesini işlemek için örnek görev kaydı   | \\Recording.xml işleme |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Borç hesapları modülünü, satıcı ödemelerini işleyecek şekilde hazırlayın

1. Örneğinizde oturum açın.
2. LCS deposundan aşağıdaki ER yapılandırmalarını indirme. Yönergeler için [ER Lifecycle Services'tan bir yapılandırmayı içe aktarma](./tasks/er-import-configuration-lifecycle-services.md)'a bakın.

    - **Ödeme modelil** ER modeli yapılandırması
    - **Ödeme modeli eşleme 1611** ER modeli eşleme yapılandırması
    - **BACS (İNG)** ER formatı yapılandırması

    ![Elektronik raporlama yapılandırmaları](media/GER-Configurations.png "Elektronik raporlamada Yapılandırmalar sayfasının ekran görüntüsü")

3. **GBSI** Büyük Britanya'da ülke/bölge bağlamı bulunan demo veri şirketini seçin.
4. Borç hesapları parametrelerini yapılandırın:

    1. **Borç hesapları \> Ödeme kurulumu \> Ödeme yöntemleri**'ne gidin.
    2. Ödeme yöntemleri için **Elektronik**'i seçin.
    3. Seçili ödeme yöntemini, satıcı ödeme işlemesi için daha önce yüklediğiniz **BACS (İNG.)** ER biçimini kullanacak şekilde yapılandırın:

        1. **Dosya formatları** Hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.
        2. **Biçim yapılandırmasını dışa aktarma** alanında, **BACS (İNG)**'yi seçin.

    ![Ödeme yöntemleri sayfası](media/GER-APParameters.png "Ödeme yöntemleri sayfasının ekran görüntüsü")

    > [!NOTE]
    > Bu ER biçiminin, özelleştirmeleri desteklemek üzere oluşturulan türetilmiş sürümü varsa **Elektronik** ödeme yönteminde bu yapılandırmayı seçebilirsiniz.

5. Örnek bir satıcı ödemesi oluşturun:

    1. **Borç hesapları \> Ödemeler \> Ödeme günlüğü**'ne gidin.
    2. Ödeme günlüğünü deftere nakletmediğinizden emin olun.

        ![Ödeme günlüğü sayfası](media/GER-APJournal.png "Ödeme günlüğü sayfasının ekran görüntüsü")

    3. **Satırlar**'ı seçin ve aşağıdaki bilgiye sahip satırı seçin.

        | Alan               | Örnek değer   |
        |---------------------|-----------------|
        | Satıcı adı         | GB\_SI\_000001  |
        | Borç               | 1,000.00        |
        | Para Birimi            | GBP             |
        | Mahsup hesabı türü | Banka            |
        | Mahsup hesabı      | GBSI OPER       |
        | Ödeme yöntemi   | Elektronik      |

    ![Satıcı ödemeleri sayfası](media/GER-APJournalLines.png "Satıcı ödemeleri sayfasının ekran görüntüsü")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Satıcı ödeme işlemini test etmek için ER çerçevesini hazırlayın

### <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma

1. **Organizasyon yönetimi \> Elektronik raporlama \> Elektronik raporlama parametreleri**'ne gidin.
2. **Ekler** sekmesinde, **Temel** alanında **Dosya**'yı Belge yönetimi (DM) çerçevesinin, temel özelliklerle ilgili belgeleri DM ekleri olarak tutmak için kullandığı belge türü olarak seçin.

    ![Elektronik raporlama parametreleri sayfası](media/GER-ERParameters.png "Elektronik raporlama parametreleri sayfasının ekran görüntüsü")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Satıcı ödemesiyle ilgili belgelerin temel kopyalarını oluştur

1. **Borç hesapları \> Ödemeler \> Ödeme günlüğü**'ne gidin.
2. **Satırlar**'ı seçin.
3. **Ödemeleri oluştur**'u seçin.
4. Ödeme yöntemleri için **Elektronik**'i seçin.
5. **GBSI OPER** banka hesabını seçin.
6. **Kontrol raporu yazdır** seçeneğini **Evet** olarak ayarlayın.
7. Oluşturulan çıktıyı bir ZIP dosyası olarak indirin.
8. İndirilen dosyayı açın.
9. İndirilen dosyadan aşağıdaki dosyaları ayıklayın:

    - **Dosya** metin biçiminde ödeme dosyası
    - **ERVendOutPaymControlReport** kontrol rapor dosyası XLSX biçiminde

    ![Ayıklanan dosyalar](media/GER-APJournalProcessed.png "Windows gezgininde ayıklanan dosya adlarının ekran görüntüsü")

### <a name="turn-on-the-er-baseline-feature"></a>ER temel özelliğini açın

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. Eylem Bölmesindeki **Yapılandırmalar** sekmesinde, **Kullanıcı parametreleri**'ni seçin.
3. **Hata ayıklama modu** seçeneğini **Evet** olarak ayarlayın.

**Hata ayıklama modu** parametresini etkinleştirerek, ER çerçevesini, giden belgeleri oluşturan herhangi bir ER formatının yürütülmesinden sonra aşağıdaki işlemleri yapmaya zorlarsınız:

1. Bir temelin yürütülen ER formatının herhangi bir bileşeni için yapılandırılmış olup olmadığını belirleyin.
2. Yapılandırılan her temelin geçerli koşullarda (oturum açmış şirketin şirket kodu, oluşturulan çıkışın dosya adı ve dosya adı uzantısı vb.) uygulanabilir olup olmadığını belirleyin.
3. Geçerli her temel için, aşağıdaki eylemleri gerçekleştirin:

    1. ER biçiminin yürütülmesi sırasında oluşturulan çıktıyı ilgili temelle karşılaştırın.
    2. Karşılaştırma sonuçlarını ER yapılandırmaları hata ayıklama günlüğünde saklayın.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Satıcı ödeme işlemi için ER temellerini yapılandırın

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. **Temelleri** seçin.
3. **Yeni**'yi seçin.
4. **Referans** alanında, **BACS (İNG)** formatını seçin.
5. **Ekler**'i seçin.
6. Satıcı ödeme dosyası için yeni bir temel ekleyin:

    1. **Yeni**'yi seçin.
    2. **Tür** alanında temel yapıları depolamak için ER parametrelerinde yapılandırdığıız **Dosya** DM belge türünü seçin.
    3. Yerel olarak kaydedilmiş **Dosya** ödeme dosyasını metin biçiminde seçmek için gözatın.
    4. **Açıklama** alanına **Ödeme TXT dosyası** girin.

7. Satıcı ödemesine kontrol raporu için yeni bir temel ekleyin:

    1. **Yeni**'yi seçin.
    2. **Tür** alanında temel yapıları depolamak için ER parametrelerinde yapılandırdığıız **Dosya** DM belge türünü seçin.
    3. Yerel olarak kaydedilmiş **ERVendOutPaymControlReport** kontrol raporu dosyasını XLSX formatında kaydetmek için gözatın.
    4. **Açıklama** alanına **Ödeme XLSX dosyası kontrol raporu** girin.

    ![Satıcı ödeme dosyası ve kontrol raporu için temeller](media/GER-BaselineAttachments.png "Seçilen Ödeme XLSX dosyası kontrol raporu ile Yapılandırma sayfasının ekran görüntüsü")

8. Sayfayı kapatın.
9. **Temeller** hızlı sekmesinde ödeme dosyasına bir temel yapılandırmak için **Yeni**'yi seçin:

    1. Yeni satırı **Ödeme dosyası için temel ayarları** olarak adlandırın.
    2. **Dosya bileşeni adı** alanında bu temeli BACS (İNG) metin formatı biçiminde ödeme dosyası oluşturan ER biçiminli bir çıktıya uygulamak için **dosya**'yı seçin.
    3. **Şirketler** alanında **BACS (UK)** ER biçimi GBSI şirketinde çalıştırıldığında bu temeli uygulamak için **GBSI**'yı seçin.
    4. **Dosya adı maskesi** alanında bu temeli sadece **.txt** dosya adı uzantılı **dosya** biçim bileşeni çıktılarına uygulamak için **\*.TXT** girin.
    5. **Temel** alanında, **Ödeme TXT dosyası**'nı bu temel, ortaya çıkan sonucu karşılaştırması için seçin.

10. Kontrol raporu için temel yapılandırmak amacıyla **Yeni**'yi seçin:

    1. Yeni satırı **Kontrol raporu için temel ayarları** olarak adlandırın.
    2. **Dosya bileşeni adı** alanında bu temeli kontrol raporu oluşturan ER biçiminli bir çıktıya uygulamak için **ERVendOutPaymControlReport**'yı seçin.
    3. **Şirketler** alanında **BACS (UK)** ER biçimi GBSI şirketinde çalıştırıldığında bu temeli uygulamak için **GBSI**'yı seçin.
    4. **Dosya adı maskesi** alanında bu temeli sadece **.xslx** dosya adı uzantılı **ERVendOutPaymControlReport** biçim bileşeni çıktılarına uygulamak için **\*.XLSX** girin.
    5. **Temel** alanında, **Ödeme XLSX konrol raporu**'nu bu temel, ortaya çıkan sonucu karşılaştırması için seçin.

    ![Yapılandırma sayfasında Temeller hızlı sekmesi](media/GER-BaselineRules.png "Yapılandırma sayfasında Temeller hızlı sekmesinin ekran görüntüsü")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Satıcı ödeme işlemini doğrulayacak testleri kaydedin

İşlevsel bir yetkili kullanıcı olarak satıcı ödeme işlemini test etmek için kendi adımlarınızı kaydedebilirsiniz. Öceneden yüklediğiniz (ve gerektiği yerde düzenlediğiniz) **Hazırla\\Kayıt.xml** görev kaydının yürütülmesini öneririz. Bu kayıt tüm test verilerinin doğru duruma ayarlanmasında kullanılır. Test birçok kez yapıldığından ve her testin aynı durumda olan verileri kullanması gerektiğinden bu adım gereklidir.

### <a name="reset-user-settings"></a>Kullanıcı ayarlarını sıfırlayın

1. Varsayılan panoyu açın.
2. **Ayarlar** düğmesini (çark simgesi) seçin.
3. **Kıllanıcı seçenekleri**'ni seçin.
4. **Kullanım verileri**'ni seçin.
5. **Sıfırla**'yı seçin.
6. Kullanım verilerini sıfırlamak istediğinizi onaylamak için **Evet**'i seçin.
7. Sayfayı kapatın.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Test için veri hazırlamak adına adımları kaydedin

1. **Ayarlar** düğmesini (çark simgesi) seçin.
2. **Görev kaydedici**'yi seçin.
3. **Kayıt yürüt**'ü seçin.
4. **Bu bilgisayardan aç**'ı seçin.
5. **Gözat**'ı seçin ve , yerel olarak kaydet **Hazırla\\Kayıt.xml** dosyasını seçin.
6. **Başlat**'ı seçin.
7. Kayıttaki tüm adımlar yürütülünceye kadar **Sonraki beklemedeki adımı yürüt**'ü seçmeye devam edin.

Bu görev kaydı performansı aşağıdaki eylemleri gerçekleştirir:

1. İşlenmiş ödeme satırının durumunu **Yok** olarak ayarlayın.

    ![Görev kaydetme adım 3-4](media/GER-Recording1Review1.png "Görev kaydetme adım 3-4'ün ekran görüntüsü")

2. **Hata ayıklama modu** ER kullanıcı parametrelerini açın.

    ![Görev kaydetme adım 9-10](media/GER-Recording1Review2.png "Görev kaydetme adım 9-10'un ekran görüntüsü")

3. Oluşturulan dosyaların temellerinin karşılaştırılmasını içeren ER hata ayıklama günlüğünü temizleyin.

    ![Görev kaydetme adım 13-15](media/GER-Recording1Review3.png "Görev kaydetme adım 13-15'in ekran görüntüsü")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Satıcı ödeme işlemini test edecek adımları kaydedin

Öceneden yüklediğiniz (ve gerektiği yerde düzenlediğiniz) **İşle\\Kayıt.xml** görev kaydının yürütülmesini öneririz. Bu kayıt, satıcı ödemelerini işlemek ve oluşturulan belgelerin ilgili temellerinin karşılaştırmasının sonuçlarını doğrulamak için kullanılır.

1. **Ayarlar** düğmesini (çark simgesi) seçin.
2. **Görev kaydedici**'yi seçin.
3. **Kayıt yürüt**'ü seçin.
4. **Bu bilgisayardan aç**'ı seçin.
5. **Gözat**'ı seçin ve , yerel olarak kaydedildi **İşle\\Kayıt.xml** dosyasını seçin.
6. **Başlat**'ı seçin.
7. Kayıttaki tüm adımlar yürütülünceye kadar **Sonraki beklemedeki adımı yürüt**'ü seçmeye devam edin.

Bu görev kaydı performansı aşağıdaki eylemleri gerçekleştirir:

1. Satıcı ödeme işlemini başlat
2. Doğru çalışma zamanı parametrelerini seçin ve kontrol raporu oluşturmayı açın.

    ![Görev kaydetme adım 3-8](media/GER-Recording2Review1.png "Görev kaydetme adım 3-8'in ekran görüntüsü")

3. Oluşturulan çıktıların karşılık gelen temellerle karşılaştırılmasının sonuçlarını kaydetmek için ER hata ayıklama günlüğüne erişin.

    ER hata ayıklama günlüğünde, karşılaştırmanın sonuçları **Oluşturulan metin** alanında görünür. **Biçim bileşeni** ve **Günlük girişine neden olan format biçimi yolu** oluşturulan çıktının temelleriyle karşılaştırıldığı dosya bileşenine referansta bulunur.

    ![Elektronik raporlama çalıştırma günlüklerindeki girişler sayfası](media/GER-ERDebugLog.png "Elektronik raporlama çalıştırma günlüklerdeki girişler sayfasının ekran görüntüsü")

4. Geçerli çıktının satır temelleriyle karşılaştırılması, görev kaydedicisini **Doğrula** seçeneği kullanılarak ve **Geçerli Değer** seçilerek kaydedilir.

    ![Geçerli değerle karşılaştırmak için Doğrula seçeneğini kullanma](media/GER-TRRecordValidation.png "Geçerli değerle karşılaştırmak için Doğrula seçeneğini kullanmanın ekran görüntüsü")

    Aşağıdaki resim, kaydedilen doğrulama adımlarının görev kaydında nasıl göründüğünü gösterir.

    ![Görev kaydetme adım 13-15](media/GER-Recording2Review2.png "Görev kaydetme adım 13-15'in ekran görüntüsü")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Kaydedilmiş testleri Azure DevOps'a ekle

1. Azure DevOps ortamını açın.
2. [Aracı yapılandırdığınızda ](#prerequisites) RSAT parametrelerinde tanımladığınız projeyi seçin.
3. [Aracı yapılandırdığınızda ](#prerequisites) RSAT parametrelerinde tanımladığınız test planını seçin.
4. Seçilen test planı için yeni bir test olayını seçin:

    1. Test olayını **Satıcının elektronik ödeme işlemini test etmek için verileri hazırla** olarak adlandırın.
    2. **Kayıt.xml** dosyasını daha önce yüklediğiniz **Hazırla** dosyasına iliştirin.

5. Seçilen test planı için yeni bir test olayını seçin:

    1. Test olayını **ER formatı BACS (İNG) kullanarak satıcı ödemelerini test etme** olarak adlandırın.
    2. **Kayıt.xml** dosyasını daha önce yüklediğiniz **İşle** dosyasına iliştirin.

    ![Seçilen test planı için yeni test olayları](media/GER-RSAT-DevOps-Tests-Passed.png "Seçilen test planı için yeni test olaylarının ekran görüntüsü")

> [!NOTE]
> Eklenen testlerin yürütme sırasının doğru olup olmadığına dikkat edin.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Kaydedilmiş testleri çalıştırmak için RSAT'yi hazırlayın

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Testleri Azure DevOps'dan yükleyin

1. Geçerli topolojide yerel RSAT uygulamasını açın.
2. Azure DevOps'da mevcut olan testleri RSAT'a yüklemek için **Yükle** seçeneğini seçin.

    ![RSAT'a yüklenen testler](media/GER-RSAT-RSAT-Tests-Loaded.png "RSAT'a yüklenen testlerin ekran görüntüsü")

### <a name="create-automation-and-parameters-files"></a>Otomasyon ve parametre dosyaları oluşturun

1. RSAT'da, Azure DevOps'dan yüklediğiniz testleri seçin.
2. RSAT otomasyonu ve parametre dosyaları yaratmak için **Yeni**'yi seçin.

    ![RSAT otomasyonu ve RSAT'ta oluşturulmuş parametreler dosyaları](media/GER-RSAT-RSAT-Tests-Initiated.png "RSAT otomasyonu ve RSAT'ta oluşturulmuş parametreler dosyalarının ekran görüntüsü")

### <a name="modify-the-parameters-files"></a>Parametre dosyalarını değiştirin

1. RSAT'ta **Satıcının elektronik ödeme işlemini test etmek için verileri hazırla** test olayını seçin.
2. **Düzenle** öğesini seçin.
3. Açılan Microsoft Excel çalışma sayfasında **Genel** çalışma sayfasında şirket kodunu **GBSI** olarak değiştirin, çünkü bu şirket test çalışması olarak kullanılacaktır.
4. RSAT'ta **ER formatı BACS (İNG) kullanarak satıcı ödemelerini test etme** test olayını seçin.
5. **Düzenle** öğesini seçin.
6. Açılan Excel çalışma kitabında, **Genel** çalışma sayfasında şirket kodunu **GBSI** olarak değiştirin.
7. **Erformatmappingrunlogtable** çalışma sayfası üzerinde, çalışma sayfasında, A:3 ve C:3 hücrelerinin, ER hata ayıklama günlüğü tablosundaki alanların, çıktının temeliyle karşılaştırmasının sonuçlarını doğrulamak için kullanılan alanların metnini içerdiğini unutmayın. Bu metinler, test yürütmesi sırasında oluşturulan ER hata ayıklama günlükleri kayıtlarını değerlendirmek için kullanılacaktır.

    ![ERFormatMappingRunLogTable çalışma sayfası](media/GER-RSAT-RSAT-ExcelParameters.png "ERFormatMappingRunLogTable çalışma sayfasının ekran görüntüsü")

## <a name="run-the-tests-and-analyze-the-results"></a>Testleri çalıştırın ve sonuçları analiz edin

### <a name="run-the-tests-in-rsat"></a>RSAT içindeki testleri çalıştırma

1. RSAT'da, yüklenen testleri seçin.
2. **Çalıştır**'ı seçin.

Test çalışmalarının bir web tarayıcısı kullanarak uygulamada otomatik olarak çalıştırılmalarına dikkat edin.

### <a name="analyze-the-results-of-test-execution"></a>Test yürütmesi sonuçlarını analiz et

Test yürütmesinin sonuçları RSAT'da depolanır. Her iki testin da geçtiğine emin olun.

![RSAT'ta geçen testler](media/GER-RSAT-RSAT-Tests-Passed.png "RSAT'ta geçen testlerin ekran görüntüsü")

Daha fazla analiz yapabilmeniz için Azure DevOps test yürütmesi sonuçlarının da gönderilip gönderilmediğine dikkat edin.

![Azure DevOps'taki test çalışmasının sonuçları](media/GER-RSAT-DevOps-Tests-Added.png "Azure DevOps'taki test çalışmasının sonuçlarının ekran görüntüsü")

### <a name="simulate-a-situation-where-tests-fail"></a>Testlerin başarısız olduğu bir durum benzetimi

Oluşturulan çıktılardan en az biri ilgili temelle eşleşmediğinde bu test paketinin başarısız olması gerekir. Bu durumu başarmak için, ilgili temelden farklı içeriğe sahip bir ödeme dosyası oluşturacak **BACS (İNG)** biçiminin türetilmiş sürümünü kullanabilirsiniz. Bu durumun benzetimini yapmak için aynı **BACS (İNG)** biçimini kullanabilir, ancak işlenmiş ödeme satırındaki ödeme tutarını değiştirebilirsiniz.

1. Uygulamayı açın ve **Borç hesapları \> Ödemeler \> Ödeme günlüğü**'ne gidin.
2. **Satırlar**'ı seçin.
3. Ödeme satırını seçin ve **Ödeme durumu \> Hiçbiri**'ni seçin.
4. **Borç** alanında, değeri **1,000.00** 'den **2,000.00**'e değiştirin.
5. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.

### <a name="run-the-tests-in-rsat"></a>RSAT içindeki testleri çalıştırma

1. RSAT'da, yüklenen testleri seçin.
2. **Çalıştır**'ı seçin.

Test çalışmalarının bir web tarayıcısı kullanarak uygulamada otomatik olarak çalıştırılmalarına dikkat edin.

### <a name="analyze-the-results-of-test-execution"></a>Test yürütmesi sonuçlarını analiz et

Test yürütmesinin sonuçları RSAT'da depolanır. İkinci testin ikinci yürütme esnasında başarısız olup olmadığına dikkat edin.

![RSAT'taki başarısız test sonuçları](media/GER-RSAT-RSAT-Tests-Failed.png "RSAT'taki başarısız test sonuçlarının ekran görüntüsü")

Daha fazla analiz yapabilmeniz için Azure DevOps test yürütmesi sonuçlarının da gönderilip gönderilmediğine dikkat edin.

![Azure DevOps'taki başarısız test sonuçları](media/GER-RSAT-DevOps-Tests-Failed.png "Azure DevOps'taki başarısız test sonuçlarının ekran görüntüsü")

Her testin durumuna erişebilirsiniz. Ayrıca yürütme günlüğüne erişerek herhangi bir hatanın nedenini çözümleyebilirsiniz. Aşağıdaki resimde, yürütme günlüğünde oluşturulan ödeme dosyası ve onun temeli arasındaki içerikteki fark nedeniyle hatanın oluştuğu gösterilir.

![Azure DevOps'taki hataları analiz etmek için yürütme günlüğü](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Azure DevOps'taki hataları analiz etmek için yürütme günlüğünün ekran görüntüsü")

Bu nedenle, gördüğünüz gibi, herhangi bir ER biçiminin çalışması, test platformu gibi RSAT ve ER temel özelliğini kullanan görev kaydedici tabanlı test çalışmaları kullanılarak otomatik olarak değerlendirilebilir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Görev kaydedici kaynakları](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Kullanıcı kabul testleri oluşturma ve otomatikleştirme](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Sürekli oluşturma ve test otomasyonunu destekleyen bir ortam dağıtma ve kullanma](../perf-test/continuous-build-test-automation.md)
- [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md)
- [ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.](tasks/er-upgrade-format.md)
- [ER Lifecycle Services'tan bir yapılandırmayı içe aktarma](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]