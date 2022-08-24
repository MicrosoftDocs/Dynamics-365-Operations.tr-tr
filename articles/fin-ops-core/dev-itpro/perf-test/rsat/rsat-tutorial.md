---
title: Regression suite automation tool öğreticisi
description: Bu makale, Regression Suite Automation Tool'un (RSAT) nasıl kullanılacağını gösterir. Çeşitli özellikleri tanımlar ve gelişmiş komut dosyası kullanan örnekler sunar.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277419"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool öğreticisi

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Bu sayfayı pdf formatında indirip kaydetmek için internet tarayıcısı araçlarını kullanın.

Bu öğretici, Regression Suite Automation Tool'un (RSAT) bazı gelişmiş özelliklerini ele alır, bir tanıtım ataması içerir ve strateji ve anahtar öğrenme noktalarını açıklar.

## <a name="notable-features-of-rsat-and-task-recorder"></a>RSAT ve görev kaydedicisinin önemli özellikleri

### <a name="validate-a-field-value"></a>Bir alan değeri doğrula

RSAT, beklenen değerleri doğrulamak için test olayınıza doğrulama adımları dahil etmenize imkan tanır. Bu özellik hakkında bilgi almak için [Beklenen değerlerin doğrulanması](rsat-validate-expected.md) makalesine bakın.

Aşağıdaki örnek, eldeki stoğun 0'dan (sıfır) fazla olup olmadığını doğrulamak için bu özelliği nasıl kullanabileceğinizi gösterir.

1. **USMF** şirketinin demo verilerinde aşağıdaki adımları içeren bir görev kaydı oluşturun:

    1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
    2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Madde numarası** alanında **1000** değeriyle filtreleme yapın.
    3. **Eldeki stok**'u seçin.
    4. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Tesis** alanında **1** değeriyle filtreleme yapın.
    5. Listede seçili satırı işaretleyin.
    6. **Toplam kullanılabilir** alan değerinin **411.0000000000000000** olduğunu doğrulayın.

2. Görev kaydını **geliştirici kaydı** olarak kaydedin ve Azure DevOps'ta test olayınıza iliştirin.
3. Test olayını test planına ekleyin ve RSAT'a yükleyin.
4. Excel parametre dosyasını açın ve **TestCaseSteps** sekmesine gidin.
5. Eldeki stoğun her zaman **0**'dan fazla olup olmayacağını doğrulamak için **Kullanılabilir Toplamı Doğrulama** adımına gidin ve değerini **411**'den **0**'a değiştirin. **İşleç** alanının değerini, eşittir işaretinden (**=**) büyüktür işaretine (**\>**) değiştirin.
6. Excel parametre dosyasını kaydedin ve kapatın.
7. Excel parametre dosyasında yaptığınız değişiklikleri Azure DevOps'a kaydetmek için **Karşıya Yükle**'yi seçin.

Bu durumda, stokta belirtilen maddenin **Toplam Kullanılabilir** alan değeri 0 (sıfır)'dan büyükse testler, eldeki gerçek stok değerine bakılmaksızın geçecektir.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Kaydedilen değişkenler ve test olaylarının zincirlenmesi

RSAT'ın en önemli özelliklerinden biri, test olaylarının zincirlenmesi; yani, bir testin diğer testlere değişken aktarma yeteneğidir. Daha fazla bilgi için [Test olaylarının zincirlenmesi için değişkenlerin kopyalanması](rsat-chain-test-cases.md) makalesine bakın.

### <a name="derived-test-case"></a>Türetilmiş test olayı

RSAT, bir görevin farklı veri yapılandırmalarıyla çalışmasını sağlayarak aynı görev kaydını birden fazla test olayı ile kullanmanıza imkan tanır. Daha fazla bilgi için [Türetilmiş test olayları](rsat-derived-test-cases.md) makalesine bakın.

### <a name="validate-notifications-and-messages"></a>Bildirim ve iletilerin doğrulanması

Bu özellik, bir eylemin meydana gelip gelmediğinin doğrulanması için kullanılabilir. Örneğin, bir üretim emri oluşturulduğunda, tahmin edildiğinde ve sonrasında başlatıldığında uygulama, size üretim emrinin başlatıldığını bildiren bir "Üretim-Başlangıç" iletisi gösterir.

![Üretim – Başlangıç bildirimi.](./media/use_rsa_tool_05.png)

Bu iletiyi, ileti metnini uygun kaydın Excel parametre dosyasındaki **İletiDoğrulama** sekmesine girerek doğrulayabilirsiniz.

![İleti Doğrulama sekmesi.](./media/use_rsa_tool_06.png)

Test olayı çalıştırıldıktan sonra Excel parametre dosyasındaki ileti, gösterilen iletiyle karşılaştırılır. İletiler eşleşmezse test olayı başarısız olacaktır.

> [!NOTE]
> Excel parametre dosyasındaki **İletiDoğrulama** sekmesine birden çok ileti girebilirsiniz. İletiler, bilgi iletileri yerine hata veya uyarı iletileri de olabilir.

### <a name="snapshot"></a>Anlık görüntü

Bu özellik, görev kaydı sırasında gerçekleştirilen adımların ekran görüntülerini alır. Denetim veya hata ayıklama amacıyla faydalıdır.

- Bu özelliği, kullanıcı arabirimi ile RSAT'i çalıştırırken kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini **yanlış**'tan **doğru**'ya değiştirin.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Bu özelliği RSAT CLI tarafından çalıştırılırken kullanmak için (örneğin Azure DevOps) RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini **yanlış**'tan **doğru**'ya değiştirin.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

RSAT, test olaylarını çalıştırırken adımların anlık görüntülerini (görüntüler) oluşturur ve bunları çalışma dizinindeki test olaylarının yürütme klasörüne kaydeder. Kayıttan yürütme klasöründe **StepSnapshots** adında ayrı bir alt klasör oluşturulur. Bu klasör, çalıştırılan test olaylarının anlık görüntülerini içerir.

## <a name="assignment"></a>Atama

### <a name="scenario"></a>Senaryo

1. Ürün tasarımcısı, yeni bir serbest bırakılan ürün oluşturur.
2. Üretim yöneticisi, stok düzeyini iki parçaya getirmek için bir üretim emri başlatır.
3. Imalat, üretim emrini başlatır ve sonlandırır ve eldeki miktarın iki parçadan oluştuğunu doğrular.
4. Satış ekibi, dört parçadan oluşan yeni ürün siparişini alır. Satış ekibi, bu şekilde net gereksinimleri dinamik plan aracılığıyla güncelleştirmiş olur. Kullanılabilir ek kapasite bulunmaması nedeniyle varsayılan sipariş politikası "yapmak yerine satın al" şeklinde ayarlanmıştır. Bu nedenle, planlı bir satınalma siparişi oluşturulur.
5. Alıcı, bir satıcı ekler, planlı satınalma siparişini kesinleştirir ve sonrasında satınalma siparişini onaylar.
6. Satın alınan mallar mağazaya ulaştığında mağaza operatörü, ilgili satınalma siparişini arar ve malları teslim alır. Sipariş bu noktada tamamlanmış olduğundan mallar, satış siparişine göre çekilebilir ve paketlenebilir.
7. Finans birimi, satınalma faturası ve satış faturasını deftere nakleder.

Aşağıdaki çizim, bu senaryoya ilişkin akışı göstermektedir.

![Gösteri senaryosu için akış.](./media/use_rsa_tool_14.png)

Aşağıdaki çizim, bu senaryo için LCS İş Süreci Modelleyicisi'nde bulunan iş süreçleri hiyerarşisini göstermektedir.

![Gösteri senaryosuna ilişkin iş süreçleri.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strateji – Anahtar öğrenme

### <a name="data"></a>Veri

- Temsili veri hacimlerinizin (ürün/altın yapılandırma verilerinin bir kopyası ile birlikte taşınan veriler) olduğundan emin olun.
- Görev kaydediciyle yeni veri oluştururken var olan adlarla çakışmayan test adları oluşturun (örneğin, **RSATxxx** gibi bir ön ek kullanın).
- 1. katman olmayan ortamlarda testleri yeniden çalıştırmak için Azure'un belirli bir noktaya geri yükleme işlemini kullanın.
- Benzersiz bir bileşim oluşturmak için **RASTGELE** ve **ŞiMDi** Excel işlevlerini kullanabiliyor olsanız bile bu oldukça zahmetli bir işlemdir. Aşağıda bir örnek verilmiştir.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Görev kaydedici

- Kayda başlamadan önce senaryoları tanımlayın. İyi yönetilen bir projede önceden tanımlanmış test senaryoları bulunur. Bir test olayı oluşturmak için test senaryolarının sonucunun ne kadar tahmin edilebilir olduğunu göz önünde bulundurun.
- Farklı roller tarafından gerçekleştirilmesi veya bir sonraki adımdan önce bekleme süresi veya dış olay olması halinde kayıtları bölün.
- Listelerdeki değerleri seçmekten kaçının. Bunun yerine, **FIFO**, **AudioRM** ve **SiteWH** gibi metin biçimlerini kullanın. Liste içerisinden seçim yaptığınızda listedeki değerin kendisi değil, konumu kaydedilir. Bu listeye öğe eklenmesi halinde değerin konumu değişebilir. Bu nedenle, kaydınız farklı bir parametre kullanacaktır ve bu durumda senaryonun geri kalanı etkilenebilir.
- Çok kullanıcılı davranışı düşünün. Örneğin, yeni oluşturulan satış siparişinizin her zaman otomatik olarak seçili olacağını varsaymayın. Bunun yerine, doğru siparişi bulmak için her zaman filtreyi kullanın.
- Zincirleme test olaylarında kullanılabilmesi amacıyla yeni oluşturulan ürünün adını kaydetmek için Görev kaydedicisindeki Kopyala işlevini kullanın.
- Adımların doğru çalıştığını doğrulayacak denetim noktalarını belirlemek için Görev kaydedicisindeki Doğrulama işlevini kullanın.

### <a name="rsat"></a>RSAT

- Testi başka bir şirkette çalıştırmak için Excel parametre dosyasının **Genel** sekmesinde şirketi değiştirebilirsiniz. Yeni seçilen şirkette ayarların ve verilerin kullanılabilir olduğundan emin olun.
- Test kullanıcısını Excel parametre dosyasının **Genel** sekmesinden değiştirebilirsiniz. Test olayını çalıştıracak kullanıcının e-posta kimliğini belirtin. Bu şekilde test olayı, belirtilen kullanıcının güvenlik izinleri kullanılarak çalıştırılabilir.
- Test başlatılmadan önce beklemek için Excel parametre dosyasının **Genel** sekmesinde bir duraklatma tanımlayabilirsiniz. Bu duraklatma, toplu bir işte (örneğin, bir sonraki adımın gerçekleştirilebilmesi için bir iş akışının çalıştırılması gerektiğinde) kullanılabilir.

## <a name="advanced-scripting"></a>Gelişmiş kodlama

### <a name="cli"></a>CLI

RSAT, **Komut İstemi** ya da **PowerShell** penceresinden çağrılabilir.

> [!NOTE]
> **TestRoot** ortam değişkeninin RSAT yükleme yolu şeklinde ayarlandığını doğrulayın. (Microsoft Windows'ta **Kontrol Paneli**'ni açın, **Sistem ve Güvenlik \> Sistem \> Gelişmiş sistem ayarları**'nı seçin ve sonra **Çevre Değişkenleri**'ni seçin.)

1. Yönetici olarak **Komut İstemi** ya da **PowerShell** penceresi açın.
2. RSAT yükleme dizinine gidin.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Tüm komutları listeleyin.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Kullanılabilir parametrelerle birlikte belirli bir komuta ilişkin tüm komutları listeler veya yardım içeriğini gösterir.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: İsteğe bağlı parametreler

`command`: Burada ``[command]``, önceki listedeki konumlardan biridir.

#### <a name="about"></a>hakkında

Yüklü RSAT'ın sürümünü gösterir.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Ekranı temizler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>indir

Belirtilen test olayına ilişkin ekleri (Kayıt, Yürütme ve Parametre dosyalarını), Azure DevOps'tan çıktı dizinine indirir. Kullanılabilir tüm test olaylarını görmek için ``list`` komutunu kullanabilir ve ilk sütundaki herhangi bir değeri **test_case_id** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde indirme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.

##### <a name="download-required-parameters"></a>download: gerekli parametreler

+ `test_case_id`: Test olayı kimliğini gösterir.

##### <a name="download-optional-parameters"></a>download: isteğe bağlı parametreler

+ `output_dir`: Çıktı çalışma dizinini gösterir. Dizin mevcut olmalıdır. Bu parametrenin belirtilmemesi halinde ayarlardaki çalışma dizini kullanılır.

##### <a name="download-examples"></a>download: örnekler

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Belirtilen test paketindeki tüm test olaylarına ilişkin ekleri (Kayıt, Yürütme ve Parametre dosyalarını), Azure DevOps'tan çıktı dizinine indirir. Kullanılabilir tüm test paketlerini görmek için ``listtestsuitenames`` komutunu kullanabilir ve herhangi bir değeri **test_suite_name** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde indirme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/byid`: Bu anahtar, istenen test paketinin test paketi adı yerine Azure DevOps kimliği ile tanımlandığını gösterir.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: gerekli parametreler

+ `test_suite_name`: Test paketi adını gösterir. Bu parametre, /byid anahtarı **belirtilmemişse** gereklidir. Bu ad, Azure DevOps test paketi adıdır.
+ `test_suite_id`: Test paketi kimliğini gösterir. Bu parametre, /byid anahtarı **belirtilmişse** gereklidir. Bu kimlik, test paketi Azure DevOps kimliğidir.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: isteğe bağlı parametreler

+ `output_dir`: Çıktı çalışma dizinini gösterir. Dizin mevcut olmalıdır. Bu parametrenin belirtilmemesi halinde ayarlardaki çalışma dizini kullanılır.

##### <a name="downloadsuite-examples"></a>downloadsuite: örnekler

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>düzenle

Excel programında parametre dosyasını açmanıza ve bu dosyayı düzenlemenize imkan tanır.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>düzenleme: gerekli parametreler

+ `excel_file`: Mevcut bir Excel dosyasının tam yolunu içermelidir.

##### <a name="edit-examples"></a>düzenleme: örnekler

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>oluştur

Çıkış dizininde belirtilen test olayı için test yürütmesi ve parametre dosyalarını oluşturur. Kullanılabilir tüm test olaylarını görmek için ``list`` komutunu kullanabilirsiniz. **test_case_id** parametresi olarak ilk sütundan herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde oluşturma işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/dllonly`: Yalnızca Test Yürütmesi dosyalarını oluşturun. Excel parametre dosyasını yeniden oluşturmayın.
+ `/keepcustomexcel`: Mevcut parametre dosyasını yükseltin. Yürütme dosyalarını da yeniden oluşturur.

##### <a name="generate-required-parameters"></a>generate: gerekli parametreler

+ `test_case_id`: Test olayı kimliğini gösterir.

##### <a name="generate-optional-parameters"></a>generate: isteğe bağlı parametreler

+ `output_dir`: Çıktı çalışma dizinini gösterir. Dizin mevcut olmalıdır. Bu parametrenin belirtilmemesi halinde ayarlardaki çalışma dizini kullanılır.

##### <a name="generate-examples"></a>generate: örnekler

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Sağlanan test olayının türevi olan yeni bir test olayı (alt test olayı) oluşturur. Yeni test olayı da belirtilen test paketine eklenir. Kullanılabilir tüm test olaylarını görmek için ``list`` komutunu kullanabilir ve ilk sütundaki herhangi bir değeri **test_case_id** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde oluşturma işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.

##### <a name="generatederived-required-parameters"></a>generatederived: gerekli parametreler

+ `parent_test_case_id`: Üst öğe test olayı kimliğini temsil eder.
+ `test_plan_id`: Test planı kimliğini temsil eder.
+ `test_suite_id`: Test paketi kimliğini temsil eder.

##### <a name="generatederived-examples"></a>generatederived: örnekler

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Belirtilen test olayına ilişkin yalnızca Test Yürütmesi dosyaları oluşturur. Excel parametre dosyası oluşturmaz. Dosyalar, belirtilen çıktı dizininde oluşturulur. Kullanılabilir tüm test olaylarını görmek için ``list`` komutunu kullanabilir ve ilk sütundaki herhangi bir değeri **test_case_id** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde oluşturma işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: gerekli parametreler

+ `test_case_id`: Test olayı kimliğini gösterir.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: isteğe bağlı parametreler

+ `output_dir`: Çıktı çalışma dizinini gösterir. Dizin mevcut olmalıdır. Bu parametrenin belirtilmemesi halinde ayarlardaki çalışma dizini kullanılır.

##### <a name="generatetestonly-examples"></a>generatetestonly: örnekler

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>testpaketioluştur

Belirtilen test paketindeki tüm test olayları için test otomasyon dosyaları oluşturur. Kullanılabilir tüm test paketlerini görmek için ``listtestsuitenames`` komutunu kullanabilir ve herhangi bir değeri **test_suite_name** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde oluşturma işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/dllonly`: Yalnızca Test Yürütmesi dosyalarını oluşturun. Excel parametre dosyasını yeniden oluşturmayın.
+ `/keepcustomexcel`: Mevcut parametre dosyasını yükseltin. Yürütme dosyalarını da yeniden oluşturur.
+ `/byid`: Bu anahtar, istenen test paketinin test paketi adı yerine Azure DevOps kimliği ile tanımlandığını gösterir.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: gerekli parametreler

+ `test_suite_name`: Test paketi adını gösterir. Bu parametre, /byid anahtarı **belirtilmemişse** gereklidir. Bu ad, Azure DevOps test paketi adıdır.
+ `test_suite_id`: Test paketi kimliğini gösterir. Bu parametre, /byid anahtarı **belirtilmişse** gereklidir. Bu kimlik, test paketi Azure DevOps kimliğidir.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: isteğe bağlı parametreler

+ `output_dir`: Çıktı çalışma dizinini gösterir. Dizin mevcut olmalıdır. Bu parametrenin belirtilmemesi halinde ayarlardaki çalışma dizini kullanılır.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: örnekler

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>yardım

[?](#section) ile aynıdır komut.

#### <a name="list"></a>liste

Geçerli test planındaki tüm kullanılabilir test olaylarını listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Kullanılabilir tüm test planlarını listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Belirtilen test paketiyle ilgili test olaylarını listeler. Kullanılabilir tüm test paketlerini görmek için ``listtestsuitenames`` komutunu kullanabilir ve listeden herhangi bir değeri **suite_name** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: gerekli parametreler

+ `test_suite_name`: İstenen paketin adı.

##### <a name="listtestsuite-examples"></a>listtestsuite: örnekler

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Belirtilen test paketiyle ilgili test olaylarını listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: gerekli parametreler

+ `test_suite_id`: İstenen paketin kimliği.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: örnekler

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Geçerli test planındaki kullanılabilir tüm test olaylarını listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>kayıttan yürütme

Belirtilen Excel parametre dosyasıyla ilişkilendirilmiş test olayını kayıttan yürütür. Bu komut, mevcut yerel otomasyon dosyalarını kullanır; dosyaları Azure DevOps'tan indirmez. Bu komut, POS ticari test olayları için desteklenmez.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde kayıttan yürütme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/comments[="comment"]`: Özette **Açıklamalar** alanına ve Azure DevOps test olayı çalıştırmalarındaki test sonuç sayfalarına eklenecek özel bir bilgi dizesi sağlayın.

##### <a name="playback-required-parameters"></a>playback: gerekli parametreler

+ `excel_parameter_file`: Excel parametre dosyasının tam yolu. Dosya mevcut olmalıdır.

##### <a name="playback-examples"></a>playback: örnekler

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Aynı anda birden fazla test olayını kayıttan yürütür. Test olayları, kimlikleri ile tanımlanır. Bu komut, dosyaları Azure DevOps'tan indirir. Kullanılabilir tüm test olaylarını görmek için ``list`` komutunu kullanabilir ve ilk sütundaki değerlerden herhangi birini **test_case_id** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde kayıttan yürütme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/comments[="comment"]`: Özette **Açıklamalar** alanına ve Azure DevOps test olayı çalıştırmalarındaki test sonuç sayfalarına eklenecek özel bir bilgi dizesi sağlayın.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: gerekli parametreler

+ `test_case_id1`: Mevcut bir test olayının kimliği.
+ `test_case_id2`: Mevcut bir test olayının kimliği.
+ `test_case_idN`: Mevcut bir test olayının kimliği.

##### <a name="playbackbyid-examples"></a>playbackbyid: örnekler

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Aynı anda birden fazla test olayını kayıttan yürütür. Test olayları, Excel parametre dosyaları tarafından tanımlanır. Bu komut, mevcut yerel otomasyon dosyalarını kullanır; dosyaları Azure DevOps'tan indirmez.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde kayıttan yürütme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/comments[="comment"]`: Özette **Açıklamalar** alanına ve Azure DevOps test olayı çalıştırmalarındaki test sonuç sayfalarına eklenecek özel bir bilgi dizesi sağlayın.

##### <a name="playbackmany-required-parameters"></a>playbackmany: gerekli parametreler

+ `excel_parameter_file1`: Excel parametre dosyasının tam yolu. Dosya mevcut olmalıdır.
+ `excel_parameter_file2`: Excel parametre dosyasının tam yolu. Dosya mevcut olmalıdır.
+ `excel_parameter_fileN`: Excel parametre dosyasının tam yolu. Dosya mevcut olmalıdır.

##### <a name="playbackmany-examples"></a>playbackmany: örnekler

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Belirtilen bir veya birden çok test paketindeki tüm test olaylarını kayıttan yürütür. /local anahtarının belirtilmesi halinde kayıttan yürütme için yerel ekler kullanılır. Aksi taktirde ekler, Azure DevOps'tan indirilir. Kullanılabilir tüm test paketlerini görmek için ``listtestsuitenames`` komutunu kullanabilir ve ilk sütundan herhangi bir değeri **suite_name** parametresi olarak kullanabilirsiniz.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: isteğe bağlı anahtarlar

+ `/updatedriver`: Bu anahtarın belirtilmiş olması halinde kayıttan yürütme işlemi çalıştırılmadan önce İnternet tarayıcısının WebDriver'ı gerektiği şekilde güncelleştirilir.
+ `/local`: Bu anahtar, dosyaların Azure DevOps'tan indirilmesi yerine kayıttan yürütme için yerel eklerin kullanılması gerektiğini belirtir.
+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde kayıttan yürütme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/comments[="comment"]`: Özette **Açıklamalar** alanına ve Azure DevOps test olayı çalıştırmalarındaki test sonuç sayfalarına eklenecek özel bir bilgi dizesi sağlayın.
+ `/byid`: Bu anahtar, istenen test paketinin test paketi adı yerine Azure DevOps kimliği ile tanımlandığını gösterir.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: gerekli parametreler

+ `test_suite_name1`: Test paketi adını gösterir. Bu parametre, /byid anahtarı **belirtilmemişse** gereklidir. Bu ad, Azure DevOps test paketi adıdır.
+ `test_suite_nameN`: Test paketi adını gösterir. Bu parametre, /byid anahtarı **belirtilmemişse** gereklidir. Bu ad, Azure DevOps test paketi adıdır.
+ `test_suite_id1`: Test paketi kimliğini gösterir. Bu parametre, /byid anahtarı **belirtilmişse** gereklidir. Bu kimlik, test paketi Azure DevOps kimliğidir.
+ `test_suite_idN`: Test paketi kimliğini gösterir. Bu parametre, /byid anahtarı **belirtilmişse** gereklidir. Bu kimlik, test paketi Azure DevOps kimliğidir.

##### <a name="playbacksuite-examples"></a>playbacksuite: örnekler

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Belirtilen Azure DevOps test paketindeki tüm test olaylarını çalıştırır.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: isteğe bağlı anahtarlar

+ `/retry[=seconds]`: Bu anahtarın belirtilmiş ve test olaylarının diğer RSAT örnekleri tarafından durdurulmuş olması halinde kayıttan yürütme işlemi, belirtilen saniye boyunca bekler ve sonra bir kez daha dener. Varsayılan \[saniye\] değeri, 120 saniyedir. Bu anahtarın olmaması durumunda test olayları durdurulduğunda işlem hemen iptal edilir.
+ `/comments[="comment"]`: Özette **Açıklamalar** alanına ve Azure DevOps test olayı çalıştırmalarındaki test sonuç sayfalarına eklenecek özel bir bilgi dizesi sağlayın.
+ `/byid`: Bu anahtar, istenen test paketinin test paketi adı yerine Azure DevOps kimliği ile tanımlandığını gösterir.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: gerekli parametreler

+ `test_suite_id`: Test paketi kimliğini Azure DevOps'taki şekliyle gösterir.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: örnekler

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>çık

Uygulamayı kapatır. Bu komut, uygulamalar yalnızca etkileşimli modda çalışırken faydalıdır.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: örnekler

`quit`

#### <a name="upload"></a>upload

Belirtilen bir test paketi veya test olayına ait ek dosyaları (Kayıt, Yürütme ve Parametre dosyaları), Azure DevOps'a karşıya yükler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: gerekli parametreler

+ `test_suite_name`: Belirtilen test paketine ait tüm dosyalar karşıya yüklenir.
+ `test_case_id1`: Karşıya yüklenmesi gereken ilk test olayı kimliğini gösterir. Bu parametreyi yalnızca test paketi adı verilmediyse kullanın.
+ `test_case_idN`: Karşıya yüklenmesi gereken son test olayı kimliğini gösterir. Bu parametreyi yalnızca test paketi adı verilmediyse kullanın.

##### <a name="upload-examples"></a>upload: örnekler

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Belirtilen bir veya birden fazla test olayına ilişkin yalnızca Kayıt dosyasını Azure DevOps'a karşıya yükler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: gerekli parametreler

+ `test_case_id1`: Azure DevOps'a karşıya yüklenmesi gereken kayda ilişkin ilk test olayı kimliğini gösterir.
+ `test_case_idN`: Azure DevOps'a karşıya yüklenmesi gereken kayda ilişkin son test olayı kimliğini gösterir.

##### <a name="uploadrecording-examples"></a>uploadrecording: örnekler

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>kullanım

Bu uygulamanın üç kullanım modunu görüntüler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Uygulamayı etkileşimli olarak çalıştırma:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Uygulamayı bir komut belirterek çalıştırma:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Uygulamayı bir ayarlar dosyası ile çalıştırma:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Windows PowerShell örnekleri

#### <a name="run-a-test-case-in-a-loop"></a>Test olayının döngüde çalıştırılması

Yeni bir müşteri oluşturan bir test koduna sahipsiniz. Bu test olayı, kodlama yoluyla her bir tekrarlama çalıştırılmadan önce aşağıdaki verileri rastgele seçerek bir döngü içerisinde çalışabilir.

- Müşteri kimliği
- Müşteri adı
- Müşteri adresi

Müşteri kimliği, *ATCUS\<number\>* biçiminde olacak olup  \<number\>, **000000001** ve **999999999** arasında bir değer alacaktır.

Aşağıdaki örnekte kullanılan ilk sayının tanımlanması için tek parametre olarak, **başlangıç** kullanılmıştır. Oluşturulması gereken müşteri sayısının tanımlanması için ikinci parametre olan **NR** kullanılır. Excel parametre dosyasındaki parametreler, her tekrarlamada bir UpdateCustomer işlevi kullanılarak değiştirilir. Sonrasında RSAT komut satırı, bir RunTestCase işlevinde çağrılır.

Microsoft Windows PowerShell Integrated Scripting Environment'ı (ISE) yönetici modunda açın ve aşağıdaki kodu **Untitled1.ps1** adlı pencereye yapıştırın.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365'teki verilere bağlı bir komut dosyası çalıştırın

Aşağıdaki örnekte bir satınalma siparişinin sipariş durumununun bulunması için Open Data Protocol (OData) çağrısı kullanılmıştır. Örneğin, durum **faturalandırılmamış** şeklindeyse faturayı deftere nakleden bir RSAT test olayı çağrısı yapabilirsiniz.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
