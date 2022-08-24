---
title: Avusturya için mali kayıt hizmeti tümleştirme örneği
description: Bu makale, Microsoft Dynamics 365 Commerce'taki Avusturya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7f4f1d796028330d2d655b1e13d3e36bbef95403
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287578"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Avusturya için mali kayıt hizmeti tümleştirme örneği

[!include[banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'taki Avusturya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.

Avusturya'da yazar kasalara yönelik yerel mali gereksinimlerin karşılanması amacıyla Avusturya için Dynamics 365 Retail işlevi, satış noktasının (POS) harici bir mali kayıt hizmetiyle örnek tümleştirmesini içerir. Bu örnek, [mali tümleştirme işlevini](fiscal-integration-for-retail-channel.md) genişletir. [EFSTA'nın](https://www.efsta.eu/at/) [EFR (Elektronik Yazar Kasa)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) çözümüne dayalıdır ve HTTPS protokolü üzerinden EFR hizmetiyle iletişim kurulmasını sağlar. EFR hizmeti, Retail Hardware station'da veya Hardware station'dan bağlanılabilecek ayrı bir makinede barındırılmalıdır. Örnek, kaynak kodu biçiminde sağlanır ve Commerce yazılım geliştirme setinin (SDK) bir parçasıdır.

Microsoft, EFSTA'dan herhangi bir donanım, yazılım veya belge yayınlamaz. EFR çözümünü edinme ve çalıştırma hakkında bilgi için [EFSTA](https://www.efsta.eu/at/kontakt) ile iletişime geçin.

## <a name="scenarios"></a>Senaryolar

Aşağıdaki senaryolar, Avusturya için mali kayıt hizmeti tümleştirme örneğinde ele alınmıştır:

- Nakit hareketlerinin mali kayıt hizmetine kaydı:

    - Mali kayıt hizmetine ayrıntılı hareket verileri gönderin. Bu verilere, satış satırı bilgilerinin yanı sıra iskontolar, ödemeler ve vergiler ile ilgili bilgiler dahildir.
    - Mali kayıt hizmetinden gelen yanıtı kaydedin. Bu yanıt, dijital bir imza ve kayıtlı hareketin bağlantısını içerir.
    - Vergileri kaydedin ve mali kayıt hizmetinin vergi kodlarıyla eşleyin.
    - Makbuzdaki kayıtlı bir hareketin QR kodunu yazdırın.

- Hediye kartı işlemlerinin ve müşteri havalelerinin mali kayıt hizmetine nakit olmayan hareketler olarak kaydı:

    - Hediye kartı verin veya hediye kartına para ekleyin.
    - Müşteri hesabı havalesi kaydedin.
    - Müşteri siparişi havalesi kaydedin.

- Satış dışı hareketlerin ve olayların mali kayıt hizmetine nakit olmayan hareketler olarak kaydı:

    - Vardiya açma ve Vardiya kapatma
    - Başlangıç tutarı, Kasa devri girişi ve Ödeme kaldırma
    - Fiyat geçersiz kılma
    - Vergi geçersiz kılma
    - Makbuzun kopyasını yazdır
    - Çekmeceyi aç
    - X raporunu yazdır
    - Z raporunu yazdır

- Avusturya'ya özel alanlar içeren gün sonu bildirimleri (X/Z raporları) yazdırma:

    - Müşterilere teslim edilen ürün veya hizmetlerin toplam sayısı
    - Vergi oranına göre satışların dökümü
    - Kasiyer/yazar kasa operatörüne göre ödemelerin dökümü
    - Günlük satışları düşüren fiyat iskontoları ve iadeler
    - Sıfır satış (hediyeler)

- Aşağıdaki seçenekler gibi hata işleme özellikleri:

    - Yeniden deneme mümkünse mali kaydı yeniden deneme (örneğin, mali kayıt hizmeti kullanılamıyorsa, hazır değilse veya yanıt vermiyorsa).
    - Mali kaydı erteleme.
    - Mali kaydı atlama veya hareketi kayıtlı olarak işaretleme ve hatanın nedenini ve ek bilgileri kaydetmek için bilgi kodlarını dahil etme.
    - Yeni bir satış hareketi açılmadan veya bir satış hareketi sonlandırılmadan önce mali kayıt hizmetinin kullanılabilir durumda olup olmadığını denetleme.

### <a name="gift-cards"></a>Hediye kartları

Mali kayıt hizmeti tümleştirme örneği, hediye kartlarıyla ilişkili aşağıdaki kuralları uygular:

- *Hediye kartı ver* ve *Hediye kartına ekle* işlemleriyle ilgili satış satırları, nakit hareketinden hariç tutulur. Bu satırları nakit hareketinin bir parçası olarak kaydetmek yerine, mali kayıt hizmetinde ayrı bir nakit olmayan hareket olarak kaydedin.
- Makbuz yalnızca hediye kartı satırlarından oluşuyorsa makbuza vergi grubu dökümü ve QR kodu yazdırılmaz.
- Bir harekette verilen veya yeniden ücretlendirilen toplam hediye kartı tutarı, nakit hareketi tutarından ayrı olarak makbuza yazdırılır.
- Ödeme satırlarının hesaplanmış düzeltmeleri, ilgili mali harekete başvuru içerecek şekilde kanal veritabanına kaydedilir.
- Hediye kartı ile ödeme, normal bir ödeme olarak kabul edilir.

### <a name="customer-deposits-and-customer-order-deposits"></a>Müşteri havaleleri ve müşteri siparişi havaleleri

Mali kayıt hizmeti tümleştirme örneği, müşteri havaleleri ve müşteri siparişi havaleleri ile ilişkili aşağıdaki kuralları uygular:

- Hareket bir müşteri havalesi ise nakit olmayan hareket olarak kaydetme.
- Bir harekette yalnızca müşteri siparişi havalesi veya müşteri siparişi havale iadesi varsa nakit olmayan hareket olarak kaydetme.
- Karma müşteri siparişi oluşturulduğunda, müşteri siparişi havale tutarını ödeme satırlarından düşme.
- Ödeme satırlarının hesaplanmış düzeltmelerini, karma müşteri siparişine yönelik mali harekete başvuru içerecek şekilde kanal veritabanına kaydetme.

### <a name="limitations-of-the-sample"></a>Örneğin sınırlamaları

Mali kayıt hizmeti yalnızca satış vergisinin fiyata dahil edildiği senaryoları destekler. Bu nedenle, **Fiyatlara satış vergisi dahildir** seçeneği hem mağazalar hem de müşteriler için **Evet** olarak ayarlanmalıdır.

## <a name="set-up-commerce-for-austria"></a>Avusturya için Commerce'ı ayarlama

Bu bölümde, Avusturya'ya özel veya Avusturya için önerilen Commerce ayarları açıklanmaktadır. Kurulumla ilgili daha fazla bilgi için [Commerce giriş sayfasına](../index.md) bakın.

Avusturya'ya özel işlevleri kullanmak için aşağıdaki ayarları belirtmeniz gerekir:

- Tüzel kişiliğin birincil adresinde, **Ülke/bölge** alanını **AUT** (Avusturya) olarak ayarlayın.
- Avusturya'da bulunan her mağazanın POS işlevi profilinde, **ISO kodu** alanını **AT** (Avusturya) olarak ayarlayın.

Avusturya için aşağıdaki ayarları da belirtmeniz gerekir. Kurulumu tamamladıktan sonra uygun dağıtım işlerini çalıştırmanız gerektiğini unutmayın.

### <a name="set-up-vat-per-austrian-requirements"></a>Avusturya gereksinimleri uyarınca KDV'yi ayarlama

Satış vergisi kodları, satış vergisi grupları ve madde satış vergisi grupları oluşturmanız gerekir. Ayrıca, ürün ve hizmetlerle ilgili satış vergisi bilgilerini de ayarlamanız gerekir. Satış vergisi özelliklerinin nasıl ayarlanacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Satış vergisine genel bakış](../../finance/general-ledger/indirect-taxes-overview.md).

Satış makbuzlarında, bir satış vergisi kodu için kısaltılmış bir kod (örneğin, "A" veya "B") yazdırabilirsiniz. Bu işlevi kullanılabilir hale getirmek için **Satış vergisi kodları** sayfasındaki **Kod yazdır** alanını ayarlayın.

### <a name="set-up-stores"></a>Mağazaları ayarlama

**Tüm mağazalar** sayfasında, mağaza ayrıntılarını güncelleştirin. Özellikle aşağıdaki parametreleri ayarlayın:

- **Satış vergisi grubu** alanında, varsayılan müşteriye yapılacak satışlarda kullanılması gereken satış vergisi grubunu belirtin.
- **Fiyatlara satış vergisi dahildir** seçeneğini **Evet** olarak ayarlayın.
- **Ad** alanını şirket adı olarak ayarlayın. Bu değişiklik, şirket adının satış makbuzunda göründüğünden emin olmanıza yardımcı olur. Alternatif olarak, şirket adını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.
- **Vergi kimlik numarası (TIN)** alanını şirket kimlik numarası olarak ayarlayın. Bu değişiklik, şirket kimlik numarasının satış makbuzunda göründüğünden emin olmanıza yardımcı olur. Alternatif olarak, şirket kimlik numarasını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.

### <a name="set-up-functionality-profiles"></a>İşlev profillerini ayarlama

POS işlevi profillerini ayarlama:

- **Makbuz numaralandırma** hızlı sekmesinde **Satış**, **Satış siparişi** ve **İade** makbuz hareket türleri için kayıt oluşturarak veya mevcut kayıtları güncelleştirerek makbuz numaralandırmasını ayarlayın.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Özel alanları, satış makbuzlarına yönelik makbuz biçimlerinde kullanılabilecek şekilde yapılandırma

POS makbuz biçimlerinde kullanılan dil metnini ve özel alanları yapılandırabilirsiniz. Makbuz kurulumunu oluşturan kullanıcının varsayılan şirketi, dil metni kurulumunun oluşturulduğu tüzel kişilikle aynı olmalıdır. Alternatif olarak, aynı dil metinleri hem kullanıcının varsayılan şirketinde hem de kurulumun oluşturulduğu mağazanın tüzel kişiliğinde oluşturulmalıdır.

**Dil metni** sayfasında, makbuz düzenlerine yönelik özel alanların etiketlerine aşağıdaki kayıtları ekleyin. Tabloda gösterilen **Dil Kodu**, **Metin Kodu** ve **Metin** değerlerinin yalnızca örnek olduğunu unutmayın. Bunları gereksinimlerinizi karşılayacak şekilde değiştirebilirsiniz. Ancak kullandığınız **Metin Kodu** değerleri benzersiz ve 900001'e eşit veya bundan daha büyük olmalıdır.

Aşağıdaki POS etiketlerini tablodaki **Dil metni**'nin **POS** bölümüne ekleyin:

| Dil kodu | Metin Kodu | Metin                      |
|-------------|---------|---------------------------|
| tr-TR       | 900001  | QR Kodu                   |
| tr-TR       | 900002  | Sürekli Numara         |
| tr-TR       | 900003  | Vergi Perakende Yazdırma Kodu     |
| tr-TR       | 900004  | Toplam (satış)             |
| tr-TR       | 900005  | Toplam Vergi (satış)         |
| tr-TR       | 900006  | Vergi Dahil Toplam (satış) |
| tr-TR       | 900007  | Vergi Tutarı (satış)        |
| tr-TR       | 900008  | Vergi Matrahı (satış)         |

**Özel alanlar** sayfasında, makbuz düzenlerine yönelik özel alanlara aşağıdaki kayıtları ekleyin. **Açıklamalı alt yazı metni kodu** değerlerinin, **Dil metni** sayfasında belirttiğiniz **Metin Kodu** değerlerine karşılık gelmesi gerektiğini unutmayın:

| Ad                 | Tür    | Altyazı metni kodu |
|----------------------|---------|-----------------|
| QRCODE               | Giriş | 900001          |
| CONTINUOUSNUMBER     | Giriş | 900002          |
| RETAILPRINTCODE      | Giriş | 900003          |
| SALESTOTAL           | Giriş | 900004          |
| SALESTOTALTAX        | Giriş | 900005          |
| SALESTOTALINCLUDETAX | Giriş | 900006          |
| SALESTAXAMOUNT       | Giriş | 900007          |
| SALESTAXBASIS        | Giriş | 900008          |

> [!NOTE]
> Önceki tabloda listelendiği gibi, doğru özel alan adlarını belirtmeniz önemlidir. Yanlış bir özel alan adı, makbuzlardaki verilerin eksik olmasına neden olur.

### <a name="configure-receipt-formats"></a>Makbuz biçimlerini yapılandırma

Gerekli her makbuz biçimi için **Yazdırma davranışı** alanının değerini **Her zaman yazdır** olarak değiştirin.

Makbuz biçimi tasarımcısında, aşağıdaki özel alanları ilgili makbuz bölümlerine ekleyin. Alan adlarının önceki bölümde tanımladığınız dil metinlerine karşılık geldiğini unutmayın.

- **Üst bilgi:** Aşağıdaki alanları ekleyin:

    - Makbuzlara şirket adını ve kimlik numarasını yazdırmak için kullanılan **Mağaza adı** ve **Vergi Kimlik Numarası** alanları. Alternatif olarak, şirket adını ve kimlik numarasını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.
    - **Mağaza adresi**, **Tarih**, **Zaman 24Sa**, **Makbuz Numarası** ve **Kayıt numarası** alanları.
    - Mali kayıt hizmetindeki nakit hareketi sayısını tanımlamak için **Sürekli Numara** alanları.

- **Satırlar:** Aşağıdaki alanları ekleyin:

    - **Madde adı**.
    - **Miktar**.
    - **Vergiyle birlikte toplam fiyat**.
    - Maddeye uygulanan satış vergisi koduna karşılık gelen kısaltılmış kodu yazdırmak için kullanılan **Vergi Perakende Yazdırma Kodu**.

- **Alt bilgi:** Aşağıdaki alanları ekleyin:

    - Her ödeme yöntemine ait ödeme tutarlarının yazdırılması için ödeme alanları. Örneğin, **Ödeme adı** ve **Ödeme tutarı** alanlarını düzenin bir satırına ekleyin.
    - **Toplam satış** alan grubu:

        - Makbuzun toplam nakit satışı tutarını yazdırmak için kullanılan **Toplam (satış)** alanı. Tutara vergi dahil değildir. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
        - Makbuzun toplam nakit satışı tutarını yazdırmak için kullanılan **Vergi Dahil Toplam (satış)** alanı. Tutara vergi dahildir. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
        - Makbuzun nakit satışlarına yönelik toplam vergi tutarını yazdırmak için kullanılan **Toplam Vergi (satış)** alanı. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.

    - **Vergi dökümü** alan grubu. Bu alan grubundaki tüm alanlar ayrı bir satırda yazdırılmalıdır.

        - Her satış vergisi kodu için satış vergisi özetinin yazdırılmasını sağlayan standart bir alan olan **Vergi Kodu** alanı. Alan yeni satıra eklenmelidir.
        - Satış vergisi koduna ilişkin geçerli vergi oranını yazdırmak için kullanılan standart bir alan olan **KDV Yüzdesi** alanı.
        - Satış vergisi kodu için makbuzun toplam nakit satış tutarını yazdırmak üzere kullanılan **Vergi Matrahı (satış)** alanı. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
        - Satış vergisi kodu için makbuzun toplam nakit satış vergi tutarını yazdırmak üzere kullanılan **Vergi Tutarı (satış)** alanı.
        - Satış vergisi koduna karşılık gelen kısaltılmış kodu yazdırmak için kullanılan **Vergi Perakende Yazdırma Kodu** alanı.

    - Kayıtlı nakit hareketine yönelik başvuruyu QR kodu biçiminde yazdırmak için kullanılan **QR Kodu** alanı.

        > [!NOTE]
        > **QR Kodu** değeri, yazar kasa yanıtından alınır. EFR yalnızca, EFR yapılandırmasındaki **Öznitelikler** alanında yer alan değerin EFSTA belgelerinde açıklanması halinde yanıtında QR kodu döndürür. EFR yapılandırmasındaki **Öznitelikler** alanında bulunan QR kodu biçiminin **BMP** olarak ayarlanması gerekir.

Makbuz biçimleriyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Makbuz biçimlerini ayarlama ve tasarlama](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Avusturya için mali tümleştirmeyi ayarlama

Avusturya için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Örnek, Commerce Runtime'ın (CRT) uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Avusturya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-aut-fi-sample-sdk.md). Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

[Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md) konusunda açıklandığı şekilde mali tümleştirme ayarlama adımlarını tamamlayın:

1. [Bir mali kayıt işlemi ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ayrıca, [bu mali kayıt hizmeti tümleştirme örneğine özgü](#set-up-the-registration-process) mali kayıt işlemi ayarlarını da not edin.
1. [Hata işleme ayarlarını belirleyin](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Ertelenen mali kaydın el ile yürütülmesini etkinleştirin](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanal bileşenlerini yapılandırın](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Mali kayıt işlemini ayarlama

Kayıt işlemini etkinleştirmek üzere Commerce Headquarters'ı ayarlamak için aşağıdaki adımları izleyin. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Mali belge sağlayıcısı ve mali bağlayıcı için yapılandırma dosyalarını indirin:

    1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunu açın.
    1. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin (örneğin, **[sürüm/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. **src \> FiscalIntegration \> Efr**'yi açın.
    1. **Configurations \> DocumentProviders**'ı açın ve şu mali belge sağlayıcısı yapılandırma dosyalarını indirin: **DocumentProviderFiscalEFRSampleAustria.xml** ve **DocumentProviderNonFiscalEFRSampleAustria.xml** (örneğin, [sürüm/9.33 dosyalarının konumu](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Mali bağlayıcı yapılandırma dosyasını **Configurations \> Connectors \> ConnectorEFRSample.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)) kısmından indirin.

    > [!WARNING]
    > [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Bu mali tümleştirme örneğinin yapılandırma dosyaları, LCS'deki bir geliştirici VM'sinde Retail SDK'nin aşağıdaki klasörlerinde bulunur:
    >
    > - **Mali belge sağlayıcısı yapılandırma dosyaları:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Mali bağlayıcı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

1. **Retail ve Commerce \> Headquarters ayarı \> Parametreler \> Paylaşılan Commerce parametreleri**'ne gidin. **Genel** hızlı sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**'na gidin ve daha önce indirdiğiniz mali belge sağlayıcısı yapılandırma dosyalarını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**'a gidin ve daha önce indirdiğiniz mali bağlayıcı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı işlevi profilleri**'ne gidin. Daha önce yüklediğiniz her bir mali belge sağlayıcısı için bir tane olmak üzere iki yeni bağlayıcı işlev profili oluşturun ve daha önce yüklediğiniz mali bağlayıcıyı seçin. [Veri eşleme ayarlarını](#default-data-mapping) gerektiği gibi güncelleştirin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**'ne gidin. Yeni bir bağlayıcı teknik profili oluşturun ve daha önce yüklediğiniz mali bağlayıcıyı seçin. [Bağlayıcı ayarlarını](#fiscal-connector-settings) gerektiği gibi güncelleştirin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**'na gidin. Daha önce oluşturduğunuz her bir bağlayıcı işlev profili için bir tane olmak üzere iki yeni mali bağlayıcı grubu oluşturun.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemleri**'ne gidin. Yeni bir mali kayıt işlemi ve iki mali kayıt işlem adımı oluşturun, ardından daha önce oluşturduğunuz mali bağlayıcı gruplarını seçin.
1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın. Kayıt işleminin etkinleştirilmesi gereken mağazaya bağlı bir işlev profili seçin. **Mali kayıt işlemi** hızlı sekmesinde, daha önce oluşturduğunuz mali kayıt işlemini seçin. Mali olmayan olayların POS'a kaydını etkinleştirmek için **İşlevler** hızlı sekmesinde, **POS** altında **Denetim** seçeneğini **Evet** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**'ne gidin. Mali yazıcının bağlanacağı Hardware station'a bağlı bir donanım profili seçin. **Mali çevre birimleri** hızlı sekmesinde, daha önce oluşturduğunuz bağlayıcı teknik profilini seçin.
1. Kanal veritabanına verileri aktarmak için dağıtım planını (**Retail ve Commerce \> Retail ve Commerce IT \> Dağıtım planı**) açın ve **1070** ile **1090** işlerini seçin.

#### <a name="default-data-mapping"></a>Varsayılan veri eşlemesi

Aşağıdaki varsayılan veri eşlemesi, mali tümleştirme örneğinin bir parçası olarak sağlanan mali belge sağlayıcısı yapılandırmasına dahil edilmiştir:

- **Katma değer vergisi (KDV) oranlarının eşlemesi** – Satış vergisi kodları için ayarlanan vergi yüzdesi değerlerinin, mali hizmete gönderilen isteklerdeki **TaxG** (vergi grubu) özniteliğinin değerleriyle eşlenmesi. Varsayılan eşleme şöyledir:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Her bir çiftteki ilk bileşen, EFR mali kayıt hizmeti tarafından desteklenen bir KDV vergi grubunu temsil eder. İkinci bileşen, karşılık gelen KDV oranını temsil eder. Avusturya'da EFR'nin desteklediği KDV vergi grupları hakkında daha fazla bilgi için [EFR referansına](https://public.efsta.net/efr/) bakın.

#### <a name="fiscal-connector-settings"></a>Mali bağlayıcı ayarları

Aşağıdaki ayarlar, mali tümleştirme örneğinin bir parçası olarak sağlanan mali bağlayıcı yapılandırmasına dahil edilmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Cihaz zaman aşımı** – Mali bağlayıcının mali kayıt hizmetinden yanıt gelmesini bekleyeceği süre (milisaniye cinsinden).
- **Mali kayıt bildirimlerini göster** – Bu bayrak, mali kayıt hizmetinin döndürdüğü bildirimlerin operatöre gösterilip gösterilmeyeceğini denetler.

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Avusturya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-aut-fi-sample-sdk.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

#### <a name="set-up-the-development-environment"></a>Geliştirme ortamını ayarlama

Örneği test etmek ve genişletmek üzere bir geliştirme ortamı ayarlamak için aşağıdaki adımları izleyin.

1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunu klonlayın veya indirin. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin. Daha fazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** kısmından EFR çözümünü açın ve derleyin.
1. CRT uzantılarını yükleyin:

    1. CRT uzantı yükleyicisini bulun:

        - **Commerce Scale Unit:** **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** klasöründe **ScaleUnit.EFR.Installer** yükleyicisini bulun.
        - **Modern POS'taki yerel CRT:** **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** klasöründe **ModernPOS.EFR.Installer** yükleyicisini bulun.

    1. CRT uzantısı yükleyicisini komut satırından başlatın:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Modern POS'taki yerel CRT:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Mali bağlayıcı uzantılarını yükleyin:

    Mali bağlayıcı uzantılarını [Donanım istasyonuna](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) veya [POS kaydına](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) yükleyebilirsiniz.

    1. Hardware station uzantılarını yükleyin:

        1. **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** klasöründe **HardwareStation.EFR.Installer** yükleyicisini bulun.
        1. Aşağıdaki komutu çalıştırarak uzantı yükleyicisini komut satırından başlatın.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. POS uzantılarını yükleyin:

        1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** adresindeki POS mali bağlayıcı örnek çözümünü açın ve derleyin.
        1. **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** klasöründe, **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** yükleyicisini bulun.
        1. Aşağıdaki komutu çalıştırarak uzantı yükleyicisini komut satırından başlatın.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Üretim ortamı

Mali tümleştirme örneği için Cloud Scale Unit'i ve self servis dağıtılabilir paketleri oluşturup yayınlamak için [Mali tümleştirme örneği için derleme işlem hattı ayarlama](fiscal-integration-sample-build-pipeline.md) konusundaki adımları izleyin. **EFR build-pipeline.yml** şablon YAML dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunun **Pipeline\\YAML_Files** klasöründe bulunabilir.

## <a name="design-of-extensions"></a>Uzantıların tasarımı

Avusturya için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Örnek, CRT'nin uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Avusturya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-aut-fi-sample-sdk.md). Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı 

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve mali kayıt hizmetinden gelen yanıtları işlemektir.

#### <a name="request-handler"></a>İstek işleyicisi

Belge sağlayıcıları için iki istek işleyicisi vardır:

- **DocumentProviderEFRFiscalAUT** – Bu işleyici, mali kayıt hizmeti için mali belgeler oluşturmak üzere kullanılır.
- **DocumentProviderEFRNonFiscalAUT** – Bu işleyici, mali kayıt hizmeti için mali olmayan belgeler oluşturmak üzere kullanılır.

Bu işleyiciler **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali kayıt hizmetine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetNonFiscalDocumentDocumentProviderRequest** – Bu istek, hangi mali olmayan belgelerin oluşturulması gerektiği bilgisini içerir. Mali kayıt hizmetine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satışlar, X raporu yazdırma, Z raporu yazdırma, müşteri hesabı havaleleri, müşteri siparişi havaleleri, denetim olayları ve satış dışı hareketler.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Bu istek, mali kayıt hizmetinden gelen yanıtı döndürür. Bu yanıt, kaydedilmeye hazır olması için dize oluşturacak şekilde seri hale getirilir.

#### <a name="configuration"></a>Yapılandırma

Mali belge sağlayıcısına ait yapılandırma dosyaları, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** klasöründe bulunur:

- **DocumentProviderFiscalEFRSampleAustria** – Mali belgeler için mali belge sağlayıcısına ait yapılandırma dosyası.
- **DocumentProviderNonFiscalEFRSampleAustria** – Mali olmayan belgeler için mali belge sağlayıcısına ait yapılandırma dosyası.

Bu dosyaların amacı, mali belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali kayıt hizmeti ile iletişim kurmaktır. Hardware station uzantısı, CRT uzantısının oluşturduğu belgeleri mali kayıt hizmetine göndermek için HTTP ve HTTPS protokollerini kullanır. Ayrıca, mali kayıt hizmetinden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EFRHandler** istek işleyicisi, mali kayıt hizmetine giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Mali bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri mali kayıt hizmetine gönderir ve hizmetten bir yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, mali kayıt hizmetinin sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, mali kayıt hizmetini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Mali bağlayıcıya ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** kısmında bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="pos-fiscal-connector-extension-design"></a>POS mali bağlayıcı uzantısı tasarımı

Bir POS mali bağlayıcı uzantısının amacı, POS'den mali kayıt hizmeti ile iletişim kurmaktır. İletişim için HTTPS protokolünü kullanır.

#### <a name="fiscal-connector-factory"></a>Mali bağlayıcı fabrikası

Mali bağlayıcı fabrikası, bağlayıcı adını mali bağlayıcı uygulamasıyla eşleştirir ve **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** dosyasında bulunur. Bağlayıcı adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

#### <a name="efr-fiscal-connector"></a>EFR mali bağlayıcı

EFR mali bağlayıcısı, **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** dosyasında bulunur. Aşağıdaki istekleri destekleyen **IFiscalConnector** arabirimini uygular:

- **FiscalRegisterSubmitDocumentClientRequest** – Bu istek, belgeleri mali kayıt hizmetine gönderir ve hizmetten bir yanıt döndürür.
- **FiscalRegisterIsReadyClientRequest** – Bu istek, mali kayıt hizmetinin sistem durumu denetimi için kullanılır.
- **FiscalRegisterInitializeClientRequest** – Bu istek, mali kayıt hizmetini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** klasöründe bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Zaman aşımı** – Bağlayıcının mali kayıt hizmetinden yanıt gelmesini bekleyeceği, milisaniye cinsinden süre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
