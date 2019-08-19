---
title: Regression Suite Automation Tool eğitimi kullanma
description: Bu konu, Regression Suite Automation Tool'un (RSAT) nasıl kullanılacağını gösterir. Çeşitli özellikleri tanımlar ve gelişmiş komut dosyası kullanan örnekler sağlar.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 02933c1649960a4fb58953798799422528d6731d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850839"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool eğitimi kullanma

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Bu sayfayı pdf formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın. 

Bu öğretici, Regression Suite Automation Tool (RSAT) gelişmiş özelliklerinden bazılarının arasında, bir demo ataması içerir ve strateji ve önemli öğrenme noktalarını açıklar.

## <a name="features-of-rsattask-recorder"></a>RSAT/Görev kaydedici özellikleri

### <a name="validate-a-field-value"></a>Bir alan değeri doğrula

Bu özellik hakkında daha fazla bilgi için, bkz [Doğrulama işlevi olan yeni bir görev kaydı oluşturma](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Kaydedilen değişken

Bu özellik hakkında daha fazla bilgi için, bkz [Kaydedilmiş bir değişken oluşturmak için varolan görev kaydını değiştirme](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Türetilmiş test olayı

1. Regression Suite Automation Tool'u (RSAT) açın ve [Regression Suite Automation Tool eğitimi ayarlama ve yükleme](./hol-set-up-regression-suite-automation-tool.md)'da oluşturduğunuz test olaylarını seçin.
2. **Yeni \> Türetilmiş test olayı oluştur**'u seçin.

    ![Yeni menüsünde türetilmiş test olayı komutu oluşturma](./media/use_rsa_tool_01.png)

3. Geçerli test paketindeki her seçili test olayı için bir türetilmiş test olayının oluşturulduğunu ve her türetilmiş test olayının kendi Excel parametre dosyası kopyasına sahip olduğunu bildiren bir ileti alırsınız. **Tamam**'ı seçin.

    > [!NOTE]
    > Türetilmiş bir test olayı çalıştırdığınızda, üst test olayının görev kaydını ve kendi Excel parametre dosyası kopyasını kullanır. Bu şekilde, birden fazla görev kaydını korumak zorunda kalmadan, aynı testi farklı parametrelerle çalıştırabilirsiniz. Türetilmiş test olayının master test olayı ile aynı test paketinin parçası olması gerekmez.

    ![İleti kutusu](./media/use_rsa_tool_02.png)

    İki ek türev test çalışması oluşturulur ve **Türetilmiş mi?** onay kutusu seçili değildir.

    ![Türetilmiş test olayları oluşturuldu](./media/use_rsa_tool_03.png)

    Azure DevOps'ta otomatik olarak bir türetilmiş test olayı oluşturulur Bu, **Yeni bir ürün oluştur** test olayının alt öğesidir ve özel bir anahtar sözcükle etiketlenir: **RSAT:DerivedTestSteps**. Bu test olayları Azure DevOps'ta otomatik olarak test planına eklenir.

    ![RSAT: DerivedTestSteps anahtar sözcüğü](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Herhangi bir nedenle, oluşturulan türetilmiş test çalışmaları doğru sırada değilse test paketindeki test olaylarını doğru sırayla çalıştırabilmek için Azure DevOps'a gidin ve test olaylarını yeniden sıralayın, böylece RSAT onları doğru sırada çalıştırabilir.

4. Yalnızca türetilmiş test olaylarını seçin ve sonra karşılık gelen Excel parametre dosyasını açmak için **Düzenle**'yi seçin.
5. Bu Excel parametre dosyalarını, ana dosyaları düzenlediğiniz şekilde düzenleyin. Başka bir deyişle, ürün kimliğinin otomatik olarak üretilmesine olanak verecek şekilde ayarlandığından emin olun. Ayrıca, kaydedilen değişkenin ilgili alanlara kopyalanmış olduğundan da emin olun.
6. Hem Excel parametre dosyalarının **Genel** sekmesinde, hem de **Şirket** alanının değerini **USSI**olarak güncelleyin, böylece türetilmiş test olayları ana test olaylarından farklı bir tüzel kişiliğe karşı çalışacaktır. Belirli bir kullanıcıya (veya belirli bir kullanıcıyla ilişkilendirilmiş role) göre test olaylarını çalıştırmak için, **Test Kullanıcısı** alanının değerini güncelleştirebilirsiniz.
7. **Çalıştır**'ı seçin ve ürünün hem USMF tüzel kişiliği hem de USSI tüzel kişiliği içinde oluşturulduğunu doğrulayın.

### <a name="validate-notifications"></a>Bildirim doğrulama

Bu özellik, bir eylemin meydana geldiğini doğrulamak için kullanılabilir. Örneğin, bir üretim emri oluşturulduğunda, tahmin edildiğinde ve sonra başlatıldığında, Microsoft Dynamics 365 for Finance and Operations üretim emrinin başlatıldığını size bildiren bir "Üretim-Başlangıcı" iletisi gösterir.

![Üretim – Başlangıç bildirimi](./media/use_rsa_tool_05.png)

Uygun kayıt için Excel parametre dosyasının **MessageValidation** sekmesine ileti metnini girerek bu iletiyi RSAT ile doğrulayabilirsiniz.

![Mesaj doğrulama sekmesi](./media/use_rsa_tool_06.png)

Test olayı çalıştırıldıktan sonra Excel parametre dosyasındaki ileti Finance and Operations'ta gösterilen iletiyle karşılaştırılır. İletiler eşleşmezse test olayı başarısız olur.

> [!NOTE]
> Excel parametre dosyasındaki **MessageValidation** sekmesine birden çok ileti girebilirsiniz. İletiler, bilgi iletileri yerine hata veya uyarı iletileri de olabilir.

### <a name="validate-values-by-using-operators"></a>Değerleri işleçleri kullanarak doğrulama

RSAT'ın önceki sürümlerinde, değerleri yalnızca beklenen değerle eşitlenmiş bir denetim değeri olarak doğrulayabilirsiniz. Yeni özellik, bir değişkenin eşit olmadığını, daha küçük olduğunu veya belirtilen bir değerden fazla olduğunu doğrulamanıza olanak tanır.

- Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    Excel parametre dosyasında yeni bir **Operatör** alanı görünür.

    > [!NOTE]
    > RSAT'ın daha eski bir sürümünü kullanıyorsanız yeni Excel parametre dosyaları oluşturmanız gerekir.

    ![Operatör alanı](./media/use_rsa_tool_07.png)

Aşağıdaki örnek, Eldeki stoğun 0'dan (sıfır) fazla olup olmadığı doğrulamak için bu özelliği nasıl kullanabileceğinizi gösterir.

1. **USMF** şirketinde demo verilerinde, aşağıdaki adımları içeren bir görev kaydı oluşturun:

    1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
    2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Ürün numarası** alanını **1000** değeriyle filtreleyin.
    3. **Eldeki stok**'u seçin.
    4. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin,  **Site** alanını **1** değeriyle filtreleyin.
    5. Listede, seçili satırı işaretleyin.
    6. **Toplam kullanılabilir** alanının değerinin **411.0000000000000000** olduğunu doğrulayın.

2. Görev kaydını LCS'deki BPM kitaplığına kaydedin ve Azure DevOps ile eşitleyin.
3. Test durumunu test planına ekleyin ve test çalışmasını RSAT'a yükleyin.
4. Excel parametre dosyasını açın. **InventOnhandItem** sekmesinde, **Operatör** alanı içeren bir **InventOnhandItem doğrula** bölümü göreceksiniz .

    ![Operatör alanı](./media/use_rsa_tool_08.png)

5. Eldeki stok miktarının her zaman 0'dan büyük olacağını doğrulamak için **Değer** alanını **411**'den **0**'a ve **Operatör** alanının değerini eşittir işaretini (**=**) büyüktür işareti (**\>**) olarak değiştirin.

    ![Değer ve Operatör alanlarının değerleri değişti](./media/use_rsa_tool_09.png)

6. Kaydedin ve Excel parametresi dosyasını kapatın.
7. Excel parametre dosyasında yaptığınız değişiklikleri Azure DevOps'a kaydetmek için **Yükle**'yi seçin.

Şimdi, stokta belirtilen maddenin **Toplam Kullanılabilir** alanının değeri 0 (sıfır)'dan büyükse eldeki gerçek stok değerine bakılmaksızın testler geçer.

### <a name="generator-logs"></a>Oluşturucu günlükleri

Bu özellik, çalıştırılan test olaylarının günlüklerini içeren bir klasör oluşturur.

- Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.

    ```
    <add key="LogGeneration" value="false" />
    ```

Test olaylarını çalıştırıldıktan sonra, günlük dosyalarını **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs** altında bulabilirsiniz.

![GeneratorLogs klasörü](./media/use_rsa_tool_10.png)

> [!NOTE]
> .config dosyasındaki değeri değiştirmeden önce varolan test olayları varsa, yeni test çalışmaları dosyaları üretene kadar bu test olayları için günlükler oluşturulmaz.
> 
> ![Yeni menüde yalnızca Metin Yürütmesi ve Parametre Dosyaları oluştur komutu](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Anlık görüntü

Bu özellik, görev kaydı sırasında gerçekleştirilen adımların ekran görüntülerini alır.

- Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

**C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, altında çalışan her test olayı için ayrı bir klasör oluşturulur.

![Test olayı için anlık görüntü klasörü](./media/use_rsa_tool_12.png)

Bu klasörlerin her biri için, test olayları çalıştırılırken gerçekleştirilen adımların anlık görüntülerini bulabilirsiniz.

![Anlık görüntü dosyaları](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>Atama

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

Aşağıdaki şekil, RSAT'da bu senaryoya yönelik iş süreçlerini gösterir.

![Demo senaryosu için iş süreçleri](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strateji – Önemli öğrenme

### <a name="data"></a>Veriler

- Temsili veri birimlerinizin (ürün/altın yapılandırma verilerinin bir kopyası ve geçirilen veriler) olduğundan emin olun.
- Görev kaydediciyle yeni veri oluşturduğunuzda, varolan adlarla çakışmayacak test adları oluşturun (örneğin, **RSATxxx**gibi bir önek kullanın).
- Katman olmayan 1 ortamlarda testleri yeniden çalıştırmak için Azure Point geri yüklemeyi kullanın.
- Benzersiz bir birleşim oluşturmak için yalnızca **RASGELE** ve **ŞiMDi** Excel işlevlerini kullanabilseniz de çalışma oldukça yüksektir. Aşağıda bir örnek verilmiştir.

    ```
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

### <a name="command-line"></a>Komut satırı

RSAT, bir **Komut İstemi** penceresinden çağrılabilir.

> [!NOTE]
> **TestRoot** ortam değişkeninin RSAT yükleme yolu olarak ayarlandığını doğrulayın. (Microsoft Windows'ta **Kontrol Paneli**'ni açın, **Sistem ve Güvenlik \> Sistem \> Gelişmiş sistem ayarları**'nı seçin ve sonra **Çevre Değişkenleri**'ni seçin.)

1. Bir **Komut İstemi** penceresini yönetici olarak açın.
2. Aracı yükleme dizininden çalıştırın.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Tüm komutları listeleyin.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShell örnekleri

#### <a name="run-a-test-case-in-a-loop"></a>Bir döngüde test olayı çalıştırma

Yeni bir müşteri oluşturan bir test koduna sahipsiniz. Kodlama yoluyla, bu test olayı, her yineleme çalıştırılmadan önce aşağıdaki verileri rasgele bir döngüde çalışabilir:

- Müşteri kodu
- Müşteri adı
- Müşteri adresi

Müşteri kimliği *ATCUS\<number\>*, biçiminde  \<number\> **000000001** ve **999999999** değerleri arasında olacaktır.

Aşağıdaki örnek, kullanılan ilk sayıyı tanımlamak için **başlangıç** parametresi olan bir parametreyi kullanır. Oluşturulması gereken müşteri sayısını tanımlamak için ikinci parametre olan **NR**öğesini kullanılır. Her yinelemede, Excel parametre dosyasındaki parametreler bir UpdateCustomer işlevi kullanılarak değiştirilir. Sonra, RSAT komut satırı bir RunTestCase işlevinde çağrılır.

Yönetici modunda Microsoft Windows PowerShell Integrated Scripting Environment (ISE) açın ve aşağıdaki kodu **Untitled1.ps1** adlı pencereye yapıştırın.

```
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
$excelFilename = "full path to excel file parameter file"
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

```
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
