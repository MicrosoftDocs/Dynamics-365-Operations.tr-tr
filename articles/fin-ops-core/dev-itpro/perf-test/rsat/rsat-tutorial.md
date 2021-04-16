---
title: Regression Suite Automation Tool eğitimi
description: Bu konu, Regression Suite Automation Tool'un (RSAT) nasıl kullanılacağını gösterir. Çeşitli özellikleri tanımlar ve gelişmiş komut dosyası kullanan örnekler sağlar.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 5a9f19168093f24a7f152b2b5b23b3728ca80222
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745177"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool eğitimi

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Bu sayfayı pdf formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın.

Bu öğretici, Regression Suite Automation Tool (RSAT) gelişmiş özelliklerinden bazılarının arasında, bir demo ataması içerir ve strateji ve önemli öğrenme noktalarını açıklar.

## <a name="notable-features-of-rsat-and-task-recorder"></a>RSAT ve Görev kaydedicinin önemli özellikleri

### <a name="validate-a-field-value"></a>Bir alan değeri doğrula

RSAT, beklenen değerleri doğrulamak için test olayınıza doğrulama adımları dahil etmenize olanak sağlar. Bu özellik hakkında bilgi için [Beklenen değerleri doğrulama](rsat-validate-expected.md) makalesine bakın.

Aşağıdaki örnek, Eldeki stoğun 0'dan (sıfır) fazla olup olmadığı doğrulamak için bu özelliği nasıl kullanabileceğinizi gösterir.

1. **USMF** şirketinde demo verilerinde, aşağıdaki adımları içeren bir görev kaydı oluşturun:

    1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
    2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Ürün numarası** alanını **1000** değeriyle filtreleyin.
    3. **Eldeki stok**'u seçin.
    4. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin,  **Site** alanını **1** değeriyle filtreleyin.
    5. Listede, seçili satırı işaretleyin.
    6. **Toplam kullanılabilir** alanının değerinin **411.0000000000000000** olduğunu doğrulayın.

2. Görev kaydını **geliştirici kaydı** olarak kaydedin ve Azure DevOps'ta test olayınıza ekleyin.
3. Test durumunu test planına ekleyin ve test çalışmasını RSAT'a yükleyin.
4. Excel parametre dosyasını açın ve **TestCaseSteps** sekmesine gidin.
5. Eldeki stokun her zaman **0**'dan fazla olup olmayacağını doğrulamak için **Kullanılabilir Toplamı Doğrulama** adımına gidin ve değerini **411** yerine **0** olarak değiştirin. **İşleç** alanının değerini, eşittir işareti (**=**) değerinden büyüktür işaretine (**\>**) değiştirin.
6. Kaydedin ve Excel parametresi dosyasını kapatın.
7. Excel parametre dosyasında yaptığınız değişiklikleri Azure DevOps'a kaydetmek için **Yükle**'yi seçin.

Şimdi, stokta belirtilen maddenin **Toplam Kullanılabilir** alanının değeri 0 (sıfır)'dan büyükse eldeki gerçek stok değerine bakılmaksızın testler geçer.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Kaydedilen değişkenler ve test olayları zinciri

RSAT'ın en önemli özelliklerinden biri test olaylarının zincirlenmesidir. Bir başka deyişle, bir testin diğer testlere değişken geçirme yeteneğidir. Daha fazla bilgi için [Test olaylarını zincirlemek için değişkenleri kopyalama](rsat-chain-test-cases.md) makalesine bakın.

### <a name="derived-test-case"></a>Türetilmiş test olayı

RSAT, bir görevin farklı veri yapılandırmalarıyla çalışacak şekilde etkinleştirerek, aynı görev kaydını birden fazla test olayı ile kullanmanıza olanak sağlar. Daha fazla bilgi için [Türetilmiş test olayları](rsat-derived-test-cases.md) makalesine bakın.

### <a name="validate-notifications-and-messages"></a>Bildirimleri ve iletileri doğrulama

Bu özellik, bir eylemin meydana geldiğini doğrulamak için kullanılabilir. Örneğin, bir üretim emri oluşturulduğunda, tahmin edildiğinde ve ardından başlatıldığında, uygulama üretim emrinin başlatıldığını size bildiren bir "Üretim-Başlangıcı" iletisi gösterir.

![Üretim – Başlangıç bildirimi](./media/use_rsa_tool_05.png)

Uygun kayıt için Excel parametre dosyasının **MessageValidation** sekmesine ileti metnini girerek bu iletiyi RSAT ile doğrulayabilirsiniz.

![Mesaj doğrulama sekmesi](./media/use_rsa_tool_06.png)

Test olayı çalıştırıldıktan sonra Excel parametre dosyasındaki ileti gösterilen iletiyle karşılaştırılır. İletiler eşleşmezse test olayı başarısız olur.

> [!NOTE]
> Excel parametre dosyasındaki **MessageValidation** sekmesine birden çok ileti girebilirsiniz. İletiler, bilgi iletileri yerine hata veya uyarı iletileri de olabilir.

### <a name="snapshot"></a>Anlık görüntü

Bu özellik, görev kaydı sırasında gerçekleştirilen adımların ekran görüntülerini alır. Denetleme veya hata ayıklama amacıyla yararlıdır.

- Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Test olayını çalıştırdığınızda RSAT, çalışma dizinindeki test olaylarının oynatma klasöründeki adımlarının anlık görüntülerini (görüntüler) oluşturur. RSAT'ın eski bir sürümünü kullanıyorsanız, görüntüler **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** konumuna kaydedilir, çalıştırılan her test olayı için ayrı bir klasör oluşturulur.

## <a name="assignment"></a>Assignment

### <a name="scenario"></a>Senaryo

1. Ürün tasarımcısı, yeni bir serbest bırakılan ürün oluşturur.
2. Üretim yöneticisi, stok düzeyini iki parçaya getirmek için bir üretim emri başlatır.
3. Üretim, üretim emrini başlatır ve sonlandırır ve eldeki miktarın iki parçadan oluştuğunu doğrular.
4. Satış ekibi, yeni ürünün dört parçadan oluşan siparişini alır. Bu nedenle, satış ekibi net gereksinimleri dinamik plan aracılığıyla güncelleştirir. Kullanılabilir ek kapasite bulunmadığından, varsayılan sipariş ilkesi "yapmak yerine satın al" olarak ayarlanmıştır. Bu nedenle, planlı bir satınalma siparişi oluşturulur.
5. Alıcı bir satıcı ekler, planlı satınalma siparişi sağlar ve sonra satınalma siparişini onaylar.
6. Satın alınan mallar mağazaya ulaştığında, mağaza operatörü ilgili satınalma siparişini arar ve malları alır. Sipariş şimdi tamamlanmış olduğundan, mallar çekilebilir ve satış siparişine göre paketlenebilir.
7. Vade farkı, satınalma faturası ve satış faturasını deftere nakleder.

Aşağıdaki resim bu senaryo için akış işlemini gösterir.

![Gösteri senaryosu için akış](./media/use_rsa_tool_14.png)

Aşağıdaki şekil, LCS İş Süreci Modelleyicisinde bu senaryoya ilişkin iş süreçleri hiyerarşisini gösterir.

![Demo senaryosu için iş süreçleri](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strateji – Önemli öğrenme

### <a name="data"></a>Veriler

- Temsili veri birimlerinizin (ürün/altın yapılandırma verilerinin bir kopyası ve geçirilen veriler) olduğundan emin olun.
- Görev kaydediciyle yeni veri oluşturduğunuzda, var olan adlarla çakışmayacak test adları oluşturun (örneğin, **RSATxxx** gibi bir önek kullanın).
- Katman olmayan 1 ortamlarda testleri yeniden çalıştırmak için Azure Point geri yüklemeyi kullanın.
- Benzersiz bir birleşim oluşturmak için yalnızca **RASGELE** ve **ŞiMDi** Excel işlevlerini kullanabilseniz de çalışma oldukça yüksektir. Aşağıda bir örnek verilmiştir.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Görev kaydedici

- Kayıt başlamadan önce senaryoları tanımlayın. İyi yönetilen bir projede önceden tanımlanmış test senaryoları vardır. Bir test olayı oluşturmak için, test senaryolarının sonucunun ne kadar tahmin edilebilir olduğunu düşünün.
- Kayıtları, farklı roller tarafından gerçekleştirildikleri takdirde veya bir sonraki adımdan önce bekleme süresi veya dış olay varsa bölün.
- Listelerdeki değerleri seçmeyi önleyin. Bunun yerine **FIFO**, **AudioRM**, ve **SiteWH** gibi değerleri kullanın. Bir listeyi seçtiğinizde, listedeki değerin konumu değil, değeri kaydedilir. Bu listeye öğe eklenirse değerin konumu değiştirilebilir. Bu nedenle, kaydınız farklı bir parametre kullanacak ve bu durumda senaryonun geri kalanı etkilenebilir.
- Çok kullanıcılı davranış hakkında düşünün. Örneğin, yeni oluşturulan satış siparişiniz her zaman otomatik olarak seçilebilir olarak kabul edilmez. Bunun yerine, doğru sıralamayı bulmak için her zaman filtreyi kullanın.
- Zincirleme test durumlarında kullanılabilmesi için yeni oluşturulan ürünün adını kaydetmek üzere Görev kaydedicisindeki Kopyala işlevini kullanın.
- Adımların doğru çalışmasını doğrulayan denetim noktalarını ayarlamak için Görev kaydedicisinin içindeki Doğrulama işlevini kullanın.

### <a name="rsat"></a>RSAT

- Testi başka bir şirkette çalıştırmak için, şirketi Excel parametre dosyasının **Genel** sekmesinde değiştirebilirsiniz. Ayarların ve verilerin yeni seçilen şirkette kullanılabilir olduğundan emin olun.
- Test kullanıcısını Excel parametre dosyasının **Genel** sekmesinden değiştirebilirsiniz. Test çalışmasını çalışacak kullanıcının e-posta kimliğini belirtin. Bu şekilde, test olayı, belirtilen kullanıcının güvenlik izinleri kullanılarak çalıştırılabilir.
- Test başlatılmadan önce beklemek için Excel parametre dosyasının **Genel** sekmesine bir duraklama tanımlayabilirsiniz. Bu duraklatma, bir toplu işlemde kullanılabilir (örneğin, bir sonraki adımın gerçekleştirilebilmesi için bir iş akışının çalıştırılması gerektiğinde).

## <a name="advanced-scripting"></a>Gelişmiş kodlama

### <a name="cli"></a>CLI

RSAT, bir **Komut İstemi** ya da **PowerShell** penceresinden çağrılabilir.

> [!NOTE]
> **TestRoot** ortam değişkeninin RSAT yükleme yolu olarak ayarlandığını doğrulayın. (Microsoft Windows'ta **Kontrol Paneli**'ni açın, **Sistem ve Güvenlik \> Sistem \> Gelişmiş sistem ayarları**'nı seçin ve sonra **Çevre Değişkenleri**'ni seçin.)

1. Bir **Komut İstemi** ya da **PowerShell** penceresini yönetici olarak açın.
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
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Kullanılabilen tüm komutlar ve parametreleriyle ilgili yardım gösterir.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: İsteğe bağlı parametreler

`command`: ``[command]`` öğesinin aşağıda belirtilen komutlardan biri olması durumu.

#### <a name="about"></a>hakkında

Geçerli sürümü gösterir.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Ekranı temizler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>indir

Belirtilen test çalışmasının eklerini çıkış dizinine yükler.
Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz. İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>download: gerekli parametreler

+ `test_case_id`: Test olayı kodunu temsil eder.
+ `output_dir`: Çıktı dizinini temsil eder. Dizin mevcut olmalıdır.

##### <a name="download-examples"></a>download: örnekler

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>düzenle

Excel programında parametreleri dosya açmanıza ve düzenlemenize olanak tanır.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: gerekli parametreler

+ `excel_file`: Mevcut bir Excel dosyasının tam yolunu içermelidir.

##### <a name="edit-examples"></a>edit: örnekler

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>oluştur

Çıkış dizininde belirtilen test çalışması için test yürütmesi ve parametre dosyaları oluşturur. Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz. İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>generate: gerekli parametreler

+ `test_case_id`: Test olayı kodunu temsil eder.
+ `output_dir`: Çıktı dizinini temsil eder. Dizin mevcut olmalıdır.

##### <a name="generate-examples"></a>generate: örnekler

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

Sağlanan test çalışmasının türevi olan yeni bir test durumu oluşturur. Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz. İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: gerekli parametreler

+ `parent_test_case_id`: Üst öğe test olayı kodunu temsil eder.
+ `test_plan_id`: Test planı kodunu temsil eder.
+ `test_suite_id`: Test paketi kodunu temsil eder.

##### <a name="generatederived-examples"></a>generatederived: örnekler

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Çıkış dizininde belirtilen test çalışması için yalnızca test yürütmesi dosyası oluşturur. Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz. İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: gerekli parametreler

+ `test_case_id`: Test olayı kodunu temsil eder.
+ `output_dir`: Çıktı dizinini temsil eder. Dizin mevcut olmalıdır.

##### <a name="generatetestonly-examples"></a>generatetestonly: örnekler

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

Belirtilen paket için çıkış dizininde tüm test çalışmalarını oluşturur. Tüm kullanılabilir test süitlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz. Sütundaki **test_suite_name** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: gerekli parametreler

+ `test_suite_name`: Test paketi adını temsil eder.
+ `output_dir`: Çıktı dizinini temsil eder. Dizin mevcut olmalıdır.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: örnekler

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>yardım

Benzer mi [?](#section) command.

#### <a name="list"></a>liste

Tüm kullanılabilir test çalışmalarını listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Tüm kullanılabilir test planlarını listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Belirtilen test paketiyle ilgili test çalışmalarını listeler. Tüm kullanılabilir test paketlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz. İlk sütundaki **suite_name** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: gerekli parametreler

+ `suite_name`: İstenen paketin adı.

##### <a name="listtestsuite-examples"></a>listtestsuite: örnekler

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Tüm kullanılabilir test paketlerini listeler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>yürütme

Excel dosyası kullanarak bir test durumunu yürütür.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: gerekli parametreler

+ `excel_file`: Excel dosyasının tam yolu. Dosya var olmalıdır.

##### <a name="playback-examples"></a>playback: örnekler

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Aynı anda birden fazla test çalışmasını kayıttan yürütür. Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz. İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: gerekli parametreler

+ `test_case_id1`: Mevcut test olayının kodu.
+ `test_case_id2`: Mevcut test olayının kodu.
+ `test_case_idN`: Mevcut test olayının kodu.

##### <a name="playbackbyid-examples"></a>playbackbyid: örnekler

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Excel dosyalarını kullanarak birçok test çalışmasını aynı anda kayıttan çalar.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: gerekli parametreler

+ `excel_file1`: Excel dosyasının tam yolu. Dosya var olmalıdır.
+ `excel_file2`: Excel dosyasının tam yolu. Dosya var olmalıdır.
+ `excel_fileN`: Excel dosyasının tam yolu. Dosya var olmalıdır.

##### <a name="playbackmany-examples"></a>playbackmany: örnekler

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Belirtilen test paketinden tüm test çalışmalarını kayıttan yürütür.
Tüm kullanılabilir test paketlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz. İlk sütundaki **suite_name** parametre olarak herhangi bir değeri kullanın.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: gerekli parametreler

+ `suite_name`: İstenen paketin adı.

##### <a name="playbacksuite-examples"></a>playbacksuite: örnekler

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>çıkış

Uygulamayı kapatır.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>yükle

Belirtilen test paketine veya test çalışmalarına ait olan tüm dosyaları karşıya yükler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload: gerekli parametreler

+ `suite_name`: Belirtilen test paketine ait olan tüm dosyaları karşıya yükler.
+ `testcase_id`: Belirtilen test olaylarına ait olan tüm dosyaları karşıya yükler.

##### <a name="upload-examples"></a>upload: örnekler

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Belirtilen test çalışmalarına ait olan yalnızca kayıt dosyasını karşıya yükler.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: gerekli parametreler

+ `testcase_id`: Belirtilen test olaylarına ait olan kayıt dosyasını karşıya yükler.

##### <a name="uploadrecording-examples"></a>uploadrecording: örnekler

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>kullanım

Bu uygulamayı başlatmak için iki yol gösterir: bir tane varsayılan ayar dosyası kullanıldığında, diğeri ayar dosyası sağlar.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell örnekleri

#### <a name="run-a-test-case-in-a-loop"></a>Bir döngüde test olayı çalıştırma

Yeni bir müşteri oluşturan bir test koduna sahipsiniz. Kodlama yoluyla, bu test olayı, her yineleme çalıştırılmadan önce aşağıdaki verileri rasgele bir döngüde çalışabilir:

- Müşteri kodu
- Müşteri adı
- Müşteri adresi

Müşteri kimliği *ATCUS\<number\>* biçiminde, \<number\> **000000001** ve **999999999** değerleri arasında olacaktır.

Aşağıdaki örnek, kullanılan ilk sayıyı tanımlamak için **başlangıç** parametresi olan bir parametreyi kullanır. Oluşturulması gereken müşteri sayısını tanımlamak için ikinci parametre olan **NR** öğesini kullanılır. Her yinelemede, Excel parametre dosyasındaki parametreler bir UpdateCustomer işlevi kullanılarak değiştirilir. Sonra, RSAT komut satırı bir RunTestCase işlevinde çağrılır.

Yönetici modunda Microsoft Windows PowerShell Integrated Scripting Environment (ISE) açın ve aşağıdaki kodu **Untitled1.ps1** adlı pencereye yapıştırın.

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365'teki verilere bağlı olan bir komut dosyası çalıştırın

Aşağıdaki örnek bir satınalma siparişinin sipariş durumunu bulmak için bir Open Data Protocol (OData) çağrısı kullanır. Durum **faturalanmamışsa**, örneğin, faturayı deftere nakleden bir RSAT test olayı çağrısı yapabilirsiniz.

```xpp
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