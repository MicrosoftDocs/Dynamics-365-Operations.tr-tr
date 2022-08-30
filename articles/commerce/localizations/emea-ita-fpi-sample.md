---
title: İtalya için yazarkasa tümleştirme örneği
description: Bu makale, Microsoft Dynamics 365 Commerce'taki İtalya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-01
ms.openlocfilehash: dff555a58c31b4e3daedd56b617dd44c4a87e601
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336772"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>İtalya için yazarkasa tümleştirme örneği

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'taki İtalya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.

İtalya için Commerce işlevi, satış noktasının (POS) mali bir yazıcıyla örnek tümleştirmesini içerir. Örnek, [mali tümleştirme işlevini](fiscal-integration-for-retail-channel.md) Epson'un [Epson FP-90III Serisi](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) yazıcılarıyla çalışacak şekilde genişletir ve Fiscal ePOS-Print API'yı kullanarak EpsonFPMate web hizmeti aracılığıyla web sunucusu modunda mali bir yazıcıyla iletişimi sağlar. Örnek yalnızca Registratore Telematico (RT) modunu destekler. Örnek, kaynak kodu biçiminde sağlanır ve Commerce yazılım geliştirme setinin (SDK) bir parçasıdır.

Microsoft, Epson'dan herhangi bir donanım, yazılım veya belge yayınlamaz. Mali yazıcının nasıl edinileceği ve çalıştırılacağı hakkında bilgi için [Epson Italia S.p.A](https://www.epson.it) ile iletişime geçin.

## <a name="scenarios"></a>Senaryolar

Aşağıdaki senaryolar, İtalya için mali yazıcı tümleştirme örneğinde ele alınmıştır:

- Satış senaryoları:

    - Peşin satış ve iadeler için mali makbuz yazdırma.
    - Mali yazıcıdan gelen yanıtı kaydetme ve kanal veritabanında saklama.
    - Vergiler:

        - Mali yazıcının vergi kodlarıyla (departmanlar) eşleme.
        - Eşlenen vergi verilerini mali yazıcıya aktarma.
        - Mali makbuza vergileri yazdırma.

    - Ödemeler:

        - Mali yazıcının ödeme yöntemleriyle eşleme.
        - Mali makbuza ödemeleri yazdırma.
        - Para üstü bilgilerini yazdırma.

    - Satır iskontolarını yazdırma.
    - Hediye kartları:

        - Verilen/yeniden ücretlendirilen hediye kartı satırını, satışa yönelik mali makbuzdan hariç tutma.
        - Hediye kartının normal ödeme yöntemi olarak kullanıldığı bir ödemeyi yazdırma.

    - Müşteri sipariş işlemleri için mali makbuzları yazdırma:

        - Müşteri siparişi havaleleri için mali makbuz yazdırılmaz.
        - Bir karma müşteri siparişine ait teslim alım satırları için mali makbuz yazdırma.
        - Bir müşteri siparişine ait teslim işlemi için mali makbuz yazdırma.
        - İade siparişi için mali makbuz yazdırma.

    - Mali makbuza makbuz numarası için barkod yazdırma.
    - Mali makbuza bir satış hareketi için belirtilen [müşteri bilgilerini](emea-ita-customer-information.md) yazdırma. Bu bilgilere örnek olarak müşterinin şans oyunu kodu verilebilir. 

- Gün sonu bildirimleri (mali X ve mali Z raporları).
- Aşağıdaki seçenekler gibi hata işleme özellikleri:

    - Yeniden deneme mümkünse mali kaydı yeniden deneme (örneğin, mali yazıcı bağlı değilse, hazır değilse veya yanıt vermiyorsa, yazıcının kağıdı bittiyse ya da kağıt sıkışması yaşandıysa).
    - Mali kaydı erteleme.
    - Mali kaydı atlama veya hareketi kayıtlı olarak işaretleme ve hatanın nedenini ve ek bilgileri kaydetmek için bilgi kodlarını dahil etme.
    - Yeni bir satış hareketi açılmadan veya bir satış hareketi sonlandırılmadan önce mali yazıcının kullanılabilir durumda olup olmadığını denetleme.

### <a name="gift-cards"></a>Hediye kartları

Mali yazıcı tümleştirme örneği, hediye kartlarıyla ilişkili aşağıdaki kuralları uygular:

- *Hediye kartı ver* ve *Hediye kartına ekle* işlemleriyle ilgili satış satırları, mali makbuzdan hariç tutulur.
- Yalnızca hediye kartı satırlarından oluşan mali makbuzlar yazdırılmaz.
- Bir harekette verilen veya yeniden ücretlendirilen toplam hediye kartı tutarı, mali makbuzun ödeme satırlarından düşülür.
- Ödeme satırlarının hesaplanmış düzeltmeleri, ilgili mali harekete başvuru içerecek şekilde kanal veritabanına kaydedilir.
- Hediye kartı ile ödeme, normal bir ödeme olarak kabul edilir.

### <a name="customer-deposits-and-customer-order-deposits"></a>Müşteri havaleleri ve müşteri siparişi havaleleri

Mali yazıcı tümleştirme örneği, müşteri havaleleri ve müşteri siparişi havaleleri ile ilişkili aşağıdaki kuralları uygular:

- Hareketin müşteri havalesi olması durumunda mali makbuz yazdırılmaz.
- Bir harekette yalnızca müşteri siparişi havalesi veya müşteri siparişi havale iadesi varsa mali makbuz yazdırılmaz.
- Müşteri siparişi teslim alım işlemlerinde, daha önce ödenen havale tutarı mali makbuz üzerine yazdırılır.
- Karma müşteri siparişi oluşturulduğunda, müşteri siparişi havale tutarını ödeme satırlarından düşme.
- Ödeme satırlarının hesaplanmış düzeltmelerini, karma müşteri siparişine yönelik mali harekete başvuru içerecek şekilde kanal veritabanına kaydetme.

### <a name="limitations-of-the-sample"></a>Örneğin sınırlamaları

- Mali yazıcı yalnızca satış vergisinin fiyata dahil edildiği senaryoları destekler. Bu nedenle, **Fiyatlara satış vergisi dahildir** seçeneği hem mağazalar hem de müşteriler için **Evet** olarak ayarlanmalıdır.
- Günlük raporlar (mali X ve mali Z), mali yazıcının üretici yazılımına katıştırılmış biçim kullanılarak yazdırılır.
- Mali yazıcı, karma hareketleri desteklemez. POS işlev profillerinde **Satış ve iadeleri bir makbuzda birleştirmeyi engelle** seçeneği **Evet** olarak ayarlanmalıdır.
- Örnek yalnızca Registratore Telematico (RT) modunda çalışan mali yazıcılarla tümleştirmeyi destekler.

## <a name="set-up-fiscal-integration-for-italy"></a>İtalya için mali tümleştirmeyi ayarlama

İtalya için mali yazıcı tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Commerce SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\EpsonFP90IIISample** klasöründe bulunur. [Örnek](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), Commerce Runtime'ın (CRT) uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan oluşur. Commerce SDK'yı kullanma hakkında dah afazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md) ve [Bağımsız paketleme SDK'sı için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md).

> [!NOTE]
> İtalya için mali yazıcı hizmeti tümleştirme örneği, Commerce SDK 10.0.29 sürümü itibarıyla Commerce SDK'da bulunur. Commerce 10.0.28 veya öncesi sürümlerde, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [İtalya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-ita-fpi-sample-sdk.md).

[Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md) konusunda açıklandığı şekilde mali tümleştirme ayarlama adımlarını tamamlayın.

1. [Bir mali kayıt işlemi ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ayrıca, [bu mali yazıcı tümleştirme örneğine özgü](#set-up-the-registration-process) mali kayıt işlemi ayarlarını da not edin.
1. [İskontolar için mali metinleri ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Hata işleme ayarlarını belirleyin](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [POS'tan X/Z raporlarını ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Ertelenen mali kaydın el ile yürütülmesini etkinleştirin](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [POS'ta müşteri bilgilerinin yönetimine yönelik işlevi ayarlayın](emea-ita-customer-information.md#setup).
1. [Kanal bileşenlerini yapılandırın](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Mali kayıt işlemini ayarlama

Kayıt işlemini etkinleştirmek üzere Commerce Headquarters'ı ayarlamak için aşağıdaki adımları izleyin. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Mali belge sağlayıcısı ve mali bağlayıcı için yapılandırma dosyalarını indirin:

    1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunu açın.
    1. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin.
    1. **src \> FiscalIntegration \> EpsonFP90IIISample** öğesini açın.
    1. Mali belge sağlayıcısı yapılandırma dosyasını **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** kısmından indirin.
    1. Mali bağlayıcı yapılandırma dosyasını **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** kısmından indirin.

    > [!NOTE]
    > Commerce 10.0.28 veya öncesi sürümlerde, LCS'de bir geliştirici sanal makinesinde Retail SDK'nin önceki sürümünü kullanmalısınız. Bu mali tümleştirme örneğinin yapılandırma dosyaları, LCS'deki bir geliştirici VM'sinde Retail SDK'nin aşağıdaki klasörlerinde bulunur:
    >
    > - **Mali belge sağlayıcısı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Mali bağlayıcı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml

1. **Retail ve Commerce \> Headquarters ayarı \> Parametreler \> Paylaşılan Commerce parametreleri**'ne gidin. **Genel** hızlı sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**'na gidin ve daha önce indirdiğiniz mali belge sağlayıcısı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**'a gidin ve daha önce indirdiğiniz mali bağlayıcı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı işlevi profilleri**'ne gidin. Yeni bir bağlayıcı işlev profili oluşturun. Daha önce yüklediğiniz belge sağlayıcıyı ve bağlayıcıyı seçin. [Veri eşleme ayarlarını](#default-data-mapping) gerektiği gibi güncelleştirin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**'ne gidin. Yeni bir bağlayıcı teknik profili oluşturun ve daha önce yüklediğiniz mali bağlayıcıyı seçin. [Bağlayıcı ayarlarını](#fiscal-connector-settings) gerektiği gibi güncelleştirin.
6. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**'na gidin. Daha önce oluşturduğunuz bağlayıcı işlev profili için yeni bir mali bağlayıcı grubu oluşturun.
7. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemleri**'ne gidin. Yeni bir mali kayıt işlemi ve mali kayıt işlem adımı oluşturun, ardından daha önce oluşturduğunuz mali bağlayıcı grubunu seçin.
8. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın. Kayıt işleminin etkinleştirilmesi gereken mağazaya bağlı bir işlev profili seçin. **Mali kayıt işlemi** hızlı sekmesinde, daha önce oluşturduğunuz mali kayıt işlemini seçin.
9. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**'ne gidin. Mali yazıcının bağlanacağı Hardware station'a bağlı bir donanım profili seçin. **Mali çevre birimleri** hızlı sekmesinde, daha önce oluşturduğunuz bağlayıcı teknik profilini seçin.
10. Kanal veritabanına verileri aktarmak için dağıtım planını (**Retail ve Commerce \> Retail ve Commerce IT \> Dağıtım planı**) açın ve **1070** ile **1090** işlerini seçin.

#### <a name="default-data-mapping"></a>Varsayılan veri eşlemesi

Aşağıdaki varsayılan veri eşlemesi, mali tümleştirme örneğinin bir parçası olarak sağlanan mali belge sağlayıcısı yapılandırmasına dahil edilmiştir:

- **Ödeme türü eşlemesi** – Mağaza için yapılandırılan ödeme yöntemlerinin, mali yazıcının desteklediği ödeme türleriyle eşlenmesi. Aşağıdaki örnekte, varsayılan eşleme gösterilmektedir.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Bu eşlemedeki özniteliklerin açıklaması aşağıda verilmiştir:

    - **StorePaymentMethod**, **Retail ve Commerce \> Kanal kurulumu \> Ödeme yöntemleri \> Ödeme yöntemleri**'nde mağaza için ayarlanmış bir ödeme yöntemidir.
    - **PrinterPaymentType** ve **PrinterPaymentIndex**, Epson mali yazıcı belgelerinde tanımlanan ödeme türüne ve dizine karşılık gelir.
    - **DepositPaymentMethod**, müşteri siparişi teslim alım tutarının müşteri siparişi havalesiyle kapatılan bölümü için yazıcının ödeme türünü ve dizinini belirtmek üzere kullanılır.

    Aşağıdaki tabloda, ödeme yöntemlerinin örnek eşlemesinin, standart tanıtım verilerinde yapılandırılan ödeme yöntemlerine nasıl karşılık geldiği gösterilmektedir.

    | Ödeme yöntemi | Ödeme yöntemi adı |
    |----------------|---------------------|
    | 1              | Nakit                |
    | 3              | Kart                |
    | 4              | Müşteri hesabı    |
    | 6              | Para Birimi            |
    | 8              | Hediye kartı           |

    Örnek eşlemeyi uygulamanızda yapılandırılan ödeme yöntemlerine göre değiştirmeniz gerekir.

- **Makbuz numarası için barkod türü** – Mali makbuzda makbuz numarasını göstermek için kullanılan barkod türü. Varsayılan eşleme **CODE128**'dir.
- **Makbuz başlığına mali verileri yazdır** – Bu parametre açıksa mağaza bilgileri mali makbuza yazdırılır. Bu bilgilere mağazanın adı, adresi ve vergi kimlik numarasının yanı sıra kasiyerin adı da dahildir.
- **Mali yazıcı departmanı eşlemesi** – Mali yazıcı departmanlarının, katma değer vergisi (KDV) oranları, KDV muafiyeti türleri ve ürün türleriyle eşlenmesi. Aşağıdaki örnekte, varsayılan eşleme gösterilmektedir.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Bu eşlemedeki özniteliklerin açıklaması aşağıda verilmiştir:

    - **VATRate**, satış vergisi kodu olarak yapılandırılmış desteklenen bir KDV oranıdır. Eşlemedeki değerin iki ondalık basamağı vardır ancak ondalık ayırıcısı yoktur. Örneğin, **2200** yüzde 22'yi, **1000** ise yüzde 10'u temsil eder.
    - **VATExemptNature** yalnızca KDV oranının 0 (sıfır) olduğu durumlarda (verginin olmadığı durumlar dahil) uygulanabilir. Şu anda **VATExemptNature** yalnızca hediye kartlarında desteklenir ve eşlemedeki değer, XML yapılandırma dosyasındaki **VATExemptNatureForGiftCard** özelliğine karşılık gelmelidir.
    - **ProductType**, ürün türüdür. **0** değeri ürünleri, **1** değeri ise hizmetleri temsil eder.
    - **DepartmentNumber**, yazıcıda yapılandırılan ve önceki üç özniteliğe karşılık gelen departman numarasıdır.

    Örnek eşlemeyi, uygulamanızda yapılandırılan KDV oranlarına ve mali yazıcınızda yapılandırılan ilgili departmanlara göre değiştirmeniz gerekir.

- **Hediye kartı için KDV muafiyeti türü** – Bir hediye kartı verildiğinde veya yeniden doldurulduğunda uygulanması gereken KDV muafiyeti türü. Değer, mali yazıcı departmanı eşlemesindeki bir girişe karşılık gelmelidir. Varsayılan eşleme **NS**'dir.
- **Ücretsiz ürünleri etkinleştir** – Bu parametre açıksa yüzde 100 iskontolu ürünler için özel *omaggio* iskonto ayarlama türü etkinleştirilir.
- **İade kaynağı bilgi kodu** – Orijinal satış makbuzu sağlanmadığında bir iade hareketinin kaynağını yakalamak için kullanılan bilgi kodu. Bu parametre, orijinal satış hareketi mevcut değilse bir iade hareketinin kaynağı hakkında doğru bir ileti oluşturmak için **Orijinal satış tarihi için bilgi kodu** ve **İade kaynağı eşlemesi** parametreleri ile birlikte kullanılır. 

    Bu bilgi kodu, kullanıcının mağazalarınızdaki olası kaynaklardan birini seçmesini veya girmesini sağlayacak şekilde yapılandırılmalıdır. Örneğin, bir alt kod listesi (such as **Siteden iade** veya **Kiosktan iade**) olarak yapılandırılabilir. **İade kaynağı eşlemesi** parametresi daha sonra bilgi kodu değerini bir mali yazıcı komutuna çevirmek için kullanılır.

    **İade kaynağı bilgi kodu** için seçilen bilgi kodu, her satış hareketi başına bir kez tetiklenen zorunlu bir bilgi kodu olarak yapılandırılmalıdır. **Ürün iadesi** işlemi çalıştırıldığında tetiklenmesi için, POS işlevi profilinde **Ürün iadesi** bilgi kodu olarak atanmalıdır.

    Bu eşleme için varsayılan değer belirtilmemiştir. Uygulamanızda yapılandırılan bir bilgi kodu seçmeniz gerekir.

- **Orijinal satış tarihi için bilgi kodu** – Orijinal satış makbuzu sağlanmadığında bir iade hareketinin orijinal satış tarihini yakalamak için kullanılan bilgi kodu. Bu parametre, orijinal satış hareketi mevcut değilse bir iade hareketinin kaynağı hakkında doğru bir ileti oluşturmak için **İade kaynağı bilgi kodu** ve **İade kaynağı eşlemesi** parametreleri ile birlikte kullanılır.

    Bilgi kodu, **Giriş türü** alanı **Tarih** olarak ayarlanacak şekilde yapılandırılmalıdır. Satış hareketi başına bir kez tetiklenen zorunlu bilgi kodu olarak yapılandırılmalıdır. Ayrıca iki bilgi kodunun arka arkaya tetiklenmesi amacıyla, **İade kaynağı bilgi kodu** parametresine yönelik olarak seçilen bilgi kodu için **Bağlantılı bilgi kodu** olarak da atanmalıdır.

    Bu eşleme için varsayılan değer belirtilmemiştir. Uygulamanızda yapılandırılan bir bilgi kodu seçmeniz gerekir.

- **İade kaynağı eşlemesi** – Orijinal satış makbuzu sağlanmadığında bir iade hareketinin kaynağını yazdırmak için kullanılan iade kaynağı eşlemesi. Bu parametre, orijinal satış hareketi mevcut değilse bir iade hareketinin kaynağı hakkında doğru bir ileti oluşturmak için **İade kaynağı bilgi kodu** ve **Orijinal satış tarihi için bilgi kodu** parametreleri ile birlikte kullanılır. Aşağıdaki örnekte, varsayılan eşleme gösterilmektedir.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Bu eşlemedeki özniteliklerin açıklaması aşağıda verilmiştir:

    - **ReturnOrigin**, mağazalarınızdaki olası iade kaynaklarından biridir. Değer, **İade kaynağı bilgi kodu** parametresinin bir değerine karşılık gelmelidir.
    - **PrinterReturnOrigin**, mali yazıcının kabul ettiği iade kaynaklarından biridir (**POS**, **VR** veya **ND**).
    - **PrinterReturnOriginWithoutFiscalData**, mali yazıcının kabul ettiği bir iade kaynağıdır ve mali yazıcı üzerinden kaydedilmemesi nedeniyle bağlantılı mali verilere sahip olmayan bir orijinal satış hareketiyle bağlantılı bir iade hareketine karşılık gelir. Bu durumda orijinal satış tarihi, orijinal satış hareketinin tarihi olarak tanımlanır.

Aşağıdaki varsayılan veri eşlemeleri artık kullanılmamaktadır ve yalnızca geriye dönük uyumluluk amacıyla tutulur:

- Katma değer vergisi (KDV) kodlarının eşlemesi
- Havale ödeme türü

#### <a name="fiscal-connector-settings"></a>Mali bağlayıcı ayarları

Aşağıdaki ayarlar, mali tümleştirme örneğinin bir parçası olarak sağlanan mali bağlayıcı yapılandırmasına dahil edilmiştir:

- **Uç noktası adresi** – Yazıcının URL'si.
- **Tarih ve saat eşitleme** – Yazıcının tarih ve saatinin bağlı Hardware station ile eşitlenip eşitlenmeyeceğini belirten bir değer.

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

> [!NOTE]
> - İtalya için mali yazıcı hizmeti tümleştirme örneği, Commerce SDK 10.0.29 sürümü itibarıyla Commerce SDK'da bulunur. Commerce 10.0.28 veya öncesi sürümlerde, LCS'de bir geliştirici sanal makinesinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [İtalya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-ita-fpi-sample-sdk.md).
> - Commerce bileşenlerine hizmet veya kalite güncelleştirmeleri uyguladığınızda, ortamınızda dağıtılan Commerce kurulumları otomatik olarak güncelleştirilmez. Gerekli örnekleri el ile güncelleştirmeniz gerekir.

#### <a name="set-up-the-development-environment"></a>Geliştirme ortamını ayarlama

Örneği test etmek ve genişletmek üzere bir geliştirme ortamı ayarlamak için aşağıdaki adımları izleyin.

1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunu klonlayın veya indirin. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin. Daha fazla bilgi için bkz. [GitHub ve NuGet'ten Commerce SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** kısmından mali yazıcı tümleştirme çözümünü açın ve derleyin.
1. CRT uzantılarını yükleyin:

    1. CRT uzantı yükleyicisini bulun:

        - **Commerce Scale Unit:** **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** klasöründe **ScaleUnit.EpsonFP90III.Installer** yükleyicisini bulun.
        - **Modern POS'taki yerel CRT:** **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** klasöründe **ModernPOS.EpsonFP90III.Installer** yükleyicisini bulun.

    1. CRT uzantısı yükleyicisini komut satırından başlatın:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Modern POS'taki yerel CRT:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Hardware station uzantılarını yükleyin:

    1. **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** klasöründe **HardwareStation.EpsonFP90III.Installer** yükleyicisini bulun.
    1. Uzantı yükleyicisini komut satırından başlatın:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Üretim ortamı

Mali tümleştirme örneği için Cloud Scale Unit'i ve self servis dağıtılabilir paketleri oluşturup yayınlamak için [Mali tümleştirme örneği için derleme işlem hattı ayarlama](fiscal-integration-sample-build-pipeline.md) konusundaki adımları izleyin. **EpsonFP90III build-pipeline.yml** şablon YAML dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunun **Pipeline\\YAML_Files** klasöründe bulunabilir.

## <a name="design-of-extensions"></a>Uzantıların tasarımı

İtalya için mali yazıcı tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Commerce SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\EpsonFP90IIISample** klasöründe bulunur. [Örnek](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), CRT'nin uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan oluşur. Commerce SDK'yı kullanma hakkında dah afazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md) ve [Bağımsız paketleme SDK'sı için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md).

> [!NOTE]
> İtalya için mali yazıcı hizmeti tümleştirme örneği, Commerce SDK 10.0.29 sürümü itibarıyla Commerce SDK'da bulunur. Commerce 10.0.28 veya öncesi sürümlerde, LCS'de bir geliştirici sanal makinesinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [İtalya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-ita-fpi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, yazıcıya özgü belgeler oluşturmak ve mali yazıcıdan gelen yanıtları işlemektir.

#### <a name="request-handler"></a>İstek işleyicisi

**DocumentProviderEpsonFP90III** istek işleyicisi, mali yazıcıdan belge oluşturma isteğinin giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali yazıcıya kaydedilmesi gereken, yazıcıya özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satış, X raporu yazdırma ve Z raporu yazdırma.

#### <a name="configuration"></a>Yapılandırma

Mali belge sağlayıcısına ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** kısmında bulunur. Dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali yazıcı ile iletişim kurmaktır. Bu uzantı, CRT uzantısının oluşturduğu belgeleri mali yazıcıya göndermek için HTTP protokolünü kullanır. Ayrıca, mali yazıcıdan alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EpsonFP90IIISample** istek işleyicisi, mali çevre birimi cihazına giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri yazıcılara gönderir ve mali yazıcıdan yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, cihazın sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, yazıcıyı başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Mali bağlayıcıya ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** kısmında bulunur. Dosyanın amacı, bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
