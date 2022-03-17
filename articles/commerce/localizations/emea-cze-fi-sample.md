---
title: Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği
description: Bu konu, Microsoft Dynamics 365 Commerce'taki Çek Cumhuriyeti'ne yönelik mali tümleştirme örneğine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: cb9679bd02c5400fc015c6807407b01e9bf55343
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388248"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'taki Çek Cumhuriyeti'ne yönelik mali tümleştirme örneğine genel bakış sağlar.

Çek Cumhuriyeti'nde yazar kasalara yönelik yerel mali gereksinimlerin karşılanması amacıyla Çek Cumhuriyeti için Dynamics 365 Commerce işlevi, satış noktasının (POS) harici bir mali kayıt hizmetiyle örnek tümleştirmesini içerir. Bu örnek, [mali tümleştirme işlevini](fiscal-integration-for-retail-channel.md) genişletir. [EFSTA'nın](https://efsta.org/) [EFR (Elektronik Yazar Kasa)](https://efsta.org/sicherheitsloesungen/) çözümüne dayalıdır ve HTTPS protokolü üzerinden EFR hizmetiyle iletişim kurulmasını sağlar. EFR hizmeti, Elektronik Satış Kaydını (EET - Elektronická evidence tržeb), diğer bir deyişle, satış verilerinin vergi makamlarının mali web hizmetine çevrimiçi olarak iletilmesini sağlar.

EFR hizmeti, Commerce Hardware station'da veya Hardware station'dan bağlanılabilecek ayrı bir makinede barındırılmalıdır. Örnek, kaynak kodu biçiminde sağlanır ve Commerce yazılım geliştirme setinin (SDK) bir parçasıdır.

Microsoft, EFSTA'dan herhangi bir donanım, yazılım veya belge yayınlamaz. EFR çözümünü edinme ve çalıştırma hakkında bilgi için [EFSTA](https://efsta.org/kontakt/) ile iletişime geçin.

## <a name="scenarios"></a>Senaryolar

Aşağıdaki senaryolar, Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneğinde ele alınmıştır:

- Nakit hareketlerinin mali kayıt hizmetine kaydı.

    - Mali kayıt hizmetine ayrıntılı hareket verileri gönderin. Bu verilere, satış satırı bilgilerinin yanı sıra iskontolar, ödemeler ve vergiler ile ilgili bilgiler dahildir. Mali kayıt hizmeti, verileri daha sonra vergi makamlarının web hizmetine gönderir ve bu hizmetten hareketin mali tanımlama kodunu içeren bir onay alır.
    - Mali kayıt hizmetinden gelen yanıtı kaydedin. Bu yanıtta, mali tanımlama kodu ve hareketin güvenlik kodu gibi mali veriler yer alır.
    - Makbuzdaki kayıtlı bir hareketin mali verilerini yazdırın.

- Hediye kartı işlemlerinin ve müşteri havalelerinin mali kayıt hizmetine kaydı.

    - Hediye kartı verin veya hediye kartına para ekleyin.
    - Müşteri hesabı havalesi kaydedin.
    - Müşteri siparişi oluşturun ve sipariş için havale kaydedin.
    - Müşteri siparişini düzenleyin ve sipariş havalesini geçersiz kılın.
    - Müşteri siparişini iptal edin ve sipariş havalesini iade edin.

- Aşağıdaki seçenekler gibi hata işleme özellikleri.

    - Yeniden deneme mümkünse mali kaydı yeniden deneme (örneğin, mali kayıt hizmeti kullanılamıyorsa, hazır değilse veya yanıt vermiyorsa).
    - Mali kaydı erteleme.
    - Mali kaydı atlama veya hareketi kayıtlı olarak işaretleme ve hatanın nedenini ve ek bilgileri kaydetmek için bilgi kodlarını dahil etme.
    - Yeni bir satış hareketi açılmadan veya bir satış hareketi sonlandırılmadan önce mali kayıt hizmetinin kullanılabilir durumda olup olmadığını denetleme.

### <a name="gift-cards"></a>Hediye kartları

Mali kayıt hizmeti tümleştirme örneği, hediye kartlarıyla ilişkili aşağıdaki kuralları uygular.

- Bir satış hareketindeki *Hediye kartı ver* veya *Hediye kartına ekle* işlemleriyle ilgili satış satırları, hareketin mali kayıt hizmetine kaydedilmesinden sonra özel bir öznitelikle işaretlenir.
- Hediye kartıyla ödeme, hareketin mali kayıt hizmetine kaydedilmesinden sonra normal bir ödeme olarak kabul edilir ve özel bir öznitelikle işaretlenir.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Müşteri hesabı havaleleri ve müşteri siparişi havaleleri

Mali kayıt hizmeti tümleştirme örneği, müşteri hesabı havaleleri ve müşteri siparişi havaleleri ile ilişkili aşağıdaki kuralları uygular.

- Müşteri hesabı havalesi veya müşteri siparişi havalesi ile ilişkili bir hareket, mali kayıt hizmetinde tek satır hareketi olarak kaydedilir ve özel bir öznitelikle işaretlenir. Havale KDV grubu bu satırda belirtilir.
- Karma müşteri siparişi, diğer bir deyişle, hem müşteri tarafından mağazadan teslim alınabilecek ürünler hem de daha sonra çekilecek veya sevk edilecek ürünler içeren bir müşteri siparişi oluşturulduğunda, mali kayıt hizmetine kaydedilen hareket hem teslim alınan ürünlere yönelik satırlar hem de sipariş havalesine ilişkin bir satır içerir.
- Müşteri hesabından ödeme, hareketin mali kayıt hizmetine kaydedilmesinden sonra normal bir ödeme olarak kabul edilir ve özel bir öznitelikle işaretlenir.
- Bir müşteri siparişi teslim alma işlemine uygulanan müşteri siparişi havale tutarı, hareketin mali kayıt hizmetine kaydedilmesinden sonra normal bir ödeme olarak kabul edilir ve özel bir öznitelikle işaretlenir.

### <a name="offline-registration"></a>Çevrimdışı kayıt

Mali kayıt hizmeti, hareket verilerini vergi makamlarının mali web hizmetine iletemezse (örneğin, yanıt zaman aşımından dolayı) ve web hizmetinden onay (yani, hareketin mali tanımlama kodu) alamazsa hareket için yerel bir imza oluşturur ve yanıta bu imzayla birlikte özel bir hata kodu dahil eder. Mali kayıt hizmeti, ağ bağlantısı tekrar sağlanır sağlanmaz orijinal siparişteki hareketleri arka planda yeniden gönderir.

### <a name="limitations-of-the-sample"></a>Örneğin sınırlamaları

Mali kayıt hizmeti yalnızca satış vergisinin fiyata dahil edildiği senaryoları destekler. Bu nedenle, **Fiyatlara satış vergisi dahildir** seçeneği hem mağazalar hem de müşteriler için **Evet** olarak ayarlanmalıdır.

## <a name="set-up-commerce-for-the-czech-republic"></a>Çek Cumhuriyeti için Commerce'ı ayarlama

Bu bölümde, Çek Cumhuriyeti'ne özel veya Çek Cumhuriyeti için önerilen Commerce ayarları açıklanmaktadır. Daha fazla bilgi için bkz. [Commerce giriş sayfası](../index.md).

Çek Cumhuriyeti'ne özel işlevleri kullanmak için aşağıdaki ayarları belirtmeniz gerekir.

- Tüzel kişiliğin birincil adresinde, **Ülke/bölge** alanını **CZE** (Çek Cumhuriyeti) olarak ayarlayın.
- Çek Cumhuriyeti'nde bulunan her mağazanın POS işlevi profilinde, **ISO kodu** alanını **CZ** (Çek Cumhuriyeti) olarak ayarlayın.

Çek Cumhuriyeti için aşağıdaki ayarları da belirtmeniz gerekir. Kurulumu tamamladıktan sonra uygun dağıtım işlerini çalıştırmanız gerektiğini unutmayın.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Çek Cumhuriyeti gereksinimleri uyarınca KDV'yi ayarlama


Satış vergisi kodları, satış vergisi grupları ve madde satış vergisi grupları oluşturmanız gerekir. Ayrıca, ürün ve hizmetlerle ilgili satış vergisi bilgilerini de ayarlamanız gerekir. Satış vergisi özelliklerinin nasıl ayarlanacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Satış vergisine genel bakış](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Mağazaları ayarlama

**Tüm mağazalar** sayfasında, mağaza ayrıntılarını güncelleştirin. Özellikle aşağıdaki parametreleri ayarlayın.

- **Satış vergisi grubu** alanında, varsayılan müşteriye yapılacak satışlarda kullanılması gereken satış vergisi grubunu belirtin.
- **Fiyatlara satış vergisi dahildir** seçeneğini **Evet** olarak ayarlayın.
- **Ad** alanını şirket adı olarak ayarlayın. Bu değişiklik, şirket adının satış makbuzunda göründüğünden emin olmanıza yardımcı olur. Alternatif olarak, şirket adını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.
- **Vergi kimlik numarası (TIN)** alanını şirket kimlik numarası olarak ayarlayın. Bu değişiklik, şirket kimlik numarasının satış makbuzunda göründüğünden emin olmanıza yardımcı olur. Alternatif olarak, şirket kimlik numarasını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.

### <a name="set-up-functionality-profiles"></a>İşlev profillerini ayarlama

POS işlevi profillerini ayarlayın.

- **Makbuz numaralandırma** hızlı sekmesinde **Satış**, **Satış siparişi** ve **İade** makbuz hareket türleri için kayıt oluşturarak veya mevcut kayıtları güncelleştirerek makbuz numaralandırmasını ayarlayın.

### <a name="set-up-registration-numbers"></a>Kayıt numaralarını ayarlama

1. **Kuruluş yönetimi \> Genel adres defteri \> Kayıt türleri \> Kayıt türleri**'ne gidin. Yeni bir kayıt türü oluşturun. **Ülke/bölge** alanını **CZE** (Çek Cumhuriyeti) olarak belirleyin ve kuruluşla sınırlı hale getirin.
2. **Kuruluş yönetimi \> Genel adres defteri \> Kayıt türleri \> Kayıt kategorileri**'ne gidin. Yeni bir kayıt kategorisi oluşturun. Önceki adımdan kayıt türünü seçin ve **Kayıt kategorisi**'ni **İş Alanı Kodu** olarak ayarlayın.
3. **Kuruluş yönetimi \> Kuruluşlar \> İşletme birimleri** seçeneğine gidin. Çek Cumhuriyeti'nde bulunan her mağaza için mağazayla ilişkili birimi seçin. **Adres** hızlı sekmesinde, **Diğer seçenekler** açılır listesini genişletin ve **Gelişmiş**'i seçin. 
4. Açılan **Adresleri yönet** sayfasında aşağıdaki ayarı belirtmeniz gerekir.

    - **Adres** hızlı sekmesinde, **Ülke/bölge** alanını **CZE** olarak ayarlayın.
    - **Kayıt Kodu** hızlı sekmesinde yeni bir kayıt oluşturun. Daha önce oluşturulan kayıt türünü seçin ve kayıt numarasını ayarlayın.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Özel alanları, satış makbuzlarına yönelik makbuz biçimlerinde kullanılabilecek şekilde yapılandırma

POS makbuz biçimlerinde kullanılan dil metnini ve özel alanları yapılandırabilirsiniz. Makbuz kurulumunu oluşturan kullanıcının varsayılan şirketi, dil metni kurulumunun oluşturulduğu tüzel kişilikle aynı olmalıdır. Alternatif olarak, aynı dil metinleri hem kullanıcının varsayılan şirketinde hem de kurulumun oluşturulduğu mağazanın tüzel kişiliğinde oluşturulmalıdır.

**Dil metni** sayfasında, makbuz düzenlerine yönelik özel alanların etiketlerine aşağıdaki kayıtları ekleyin. Tabloda gösterilen **Dil Kodu**, **Metin Kodu** ve **Metin** değerlerinin yalnızca örnek olduğunu unutmayın. Bunları gereksinimlerinizi karşılayacak şekilde değiştirebilirsiniz. Ancak kullandığınız **Metin Kodu** değerleri benzersiz ve 900001'e eşit veya bundan daha büyük olmalıdır.

Aşağıdaki POS etiketlerini tablodaki **Dil metni**'nin **POS** bölümüne ekleyin:

| Dil kodu | Metin Kodu | Metin                   |
|-------------|---------|------------------------|
| tr-TR       | 900001  | ID provozovny/pokladny |
| tr-TR       | 900002  | BKP                    |
| tr-TR       | 900003  | PKP                    |
| tr-TR       | 900004  | FIK                    |
| tr-TR       | 900005  | Bilgi                   |
| tr-TR       | 900006  | Numara serisi        |

**Özel alanlar** sayfasında, makbuz düzenlerine yönelik özel alanlara aşağıdaki kayıtları ekleyin. **Açıklamalı alt yazı metni kodu** değerlerinin, **Dil metni** sayfasında belirttiğiniz **Metin Kodu** değerlerine karşılık gelmesi gerektiğini unutmayın:

| Ad                 | Tür    | Altyazı metni kodu |
|----------------------|---------|-----------------|
| TLT                  | Giriş | 900001          |
| SEC                  | Giriş | 900002          |
| SIGN                 | Giriş | 900003          |
| FISCAL               | Giriş | 900004          |
| INFO                 | Giriş | 900005          |
| CONTINUOUSNUMBER     | Giriş | 900006          |

> [!NOTE]
> Önceki tabloda listelendiği gibi, doğru özel alan adlarını belirtmeniz önemlidir. Yanlış bir özel alan adı, makbuzlardaki verilerin eksik olmasına neden olur.

### <a name="configure-receipt-formats"></a>Makbuz biçimlerini yapılandırma

Gerekli her makbuz biçimi için **Yazdırma davranışı** alanının değerini **Her zaman yazdır** olarak değiştirin.

Makbuz biçimi tasarımcısında, aşağıdaki özel alanları ilgili makbuz bölümlerine ekleyin. Alan adlarının önceki bölümde tanımladığınız dil metinlerine karşılık geldiğini unutmayın.

- **Üst bilgi:** Aşağıdaki alanları ekleyin.

    - **Mağaza adı** ve **Vergi Kimlik Numarası**: Bu alanlar makbuzlara şirket adını ve kimlik numarasını yazdırmak için kullanılır. Alternatif olarak, şirket adını ve kimlik numarasını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.
    - **Mağaza adresi**, **Tarih**, **Zaman 24Sa**, **Makbuz Numarası** ve **Kayıt numarası**.
    - **Sıra numarası**: Bu alan, mali kayıt hizmetindeki nakit hareketi sayısını tanımlar.

- **Satırlar:** Aşağıdaki alanları ekleyin.

    - **Madde adı**
    - **Miktar**
    - **Vergiyle birlikte toplam fiyat**

- **Alt bilgi:** Aşağıdaki alanları ekleyin.

    - Her ödeme yöntemine ait ödeme tutarlarının yazdırılması için ödeme alanları. Örneğin, **Ödeme adı** ve **Ödeme tutarı** alanlarını düzenin bir satırına ekleyin.
    - **ID provozovny/pokladny** : Bu alan, iş alanlarının ve yazar kasanın tanımlayıcılarını yazdırır.
    - **BKP** : Bu alan, mali kayıt hizmeti tarafından atanan, vergi mükellefine ait güvenlik kodunu yazdırır.
    - **FIK**: Bu alan, çevrimiçi kaydın başarılı olması durumunda, vergi makamlarının web hizmeti tarafından atanan hareketin mali tanımlama kodunu yazdırır.
    - **PKP**: Bu alan, çevrimdışı kayıt durumunda mali kayıt hizmeti tarafından oluşturulan vergi mükellefi imza kodunu yazdırır.
    - **Bilgi**: Bu alan, mali kayıt hizmetinden gelen ek bilgileri yazdırır.

Makbuz biçimleriyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Makbuz biçimlerini ayarlama ve tasarlama](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Çek Cumhuriyeti için mali tümleştirmeyi ayarlama

Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Örnek, Commerce Runtime'ın (CRT) uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Çek Cumhuriyeti için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-cze-fi-sample-sdk.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

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
    1. Mali belge sağlayıcısı yapılandırma dosyasını **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)) kısmından indirin.
    1. Mali bağlayıcı yapılandırma dosyasını **Configurations \> Connectors \> ConnectorEFRSample.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)) kısmından indirin.

    > [!WARNING]
    > [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Bu mali tümleştirme örneğinin yapılandırma dosyaları, LCS'deki bir geliştirici VM'sinde Retail SDK'nin aşağıdaki klasörlerinde bulunur:
    >
    > - **Mali belge sağlayıcısı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **Mali bağlayıcı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

1. **Retail ve Commerce \> Headquarters ayarı \> Parametreler \> Paylaşılan Commerce parametreleri**'ne gidin. **Genel** hızlı sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**'na gidin ve daha önce indirdiğiniz mali belge sağlayıcısı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**'a gidin ve daha önce indirdiğiniz mali bağlayıcı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı işlevi profilleri**'ne gidin. Yeni bir bağlayıcı işlev profili oluşturun. Daha önce yüklediğiniz belge sağlayıcıyı ve bağlayıcıyı seçin. [Veri eşleme ayarlarını](#default-data-mapping) gerektiği gibi güncelleştirin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**'ne gidin. Yeni bir bağlayıcı teknik profili oluşturun ve daha önce yüklediğiniz mali bağlayıcıyı seçin. [Bağlayıcı ayarlarını](#fiscal-connector-settings) gerektiği gibi güncelleştirin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**'na gidin. Daha önce oluşturduğunuz bağlayıcı işlev profili için yeni bir mali bağlayıcı grubu oluşturun.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemleri**'ne gidin. Yeni bir mali kayıt işlemi ve mali kayıt işlem adımı oluşturun, ardından daha önce oluşturduğunuz mali bağlayıcı grubunu seçin.
1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın. Kayıt işleminin etkinleştirilmesi gereken mağazaya bağlı bir işlev profili seçin. **Mali kayıt işlemi** hızlı sekmesinde, daha önce oluşturduğunuz mali kayıt işlemini seçin.
1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**'ne gidin. Mali yazıcının bağlanacağı Hardware station'a bağlı bir donanım profili seçin. **Mali çevre birimleri** hızlı sekmesinde, daha önce oluşturduğunuz bağlayıcı teknik profilini seçin.
1. Kanal veritabanına verileri aktarmak için dağıtım planını (**Retail ve Commerce \> Retail ve Commerce IT \> Dağıtım planı**) açın ve **1070** ile **1090** işlerini seçin.

#### <a name="default-data-mapping"></a>Varsayılan veri eşlemesi

Aşağıdaki varsayılan veri eşlemesi, mali tümleştirme örneğinin bir parçası olarak sağlanan mali belge sağlayıcısı yapılandırmasına dahil edilmiştir:

- **Katma değer vergisi (KDV) oranlarının eşlemesi** – Satış vergisi kodları için ayarlanan vergi yüzdesi değerlerinin, mali hizmete gönderilen isteklerdeki **TaxG** (vergi grubu) özniteliğinin değerleriyle eşlenmesi. Varsayılan eşleme şöyledir:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Her bir çiftteki ilk bileşen, EFR mali kayıt hizmeti tarafından desteklenen bir KDV vergi grubunu temsil eder. İkinci bileşen, karşılık gelen KDV oranını temsil eder. Çek Cumhuriyeti'nde EFR'nin desteklediği KDV vergi grupları hakkında daha fazla bilgi için [EFR referansına](https://public.efsta.net/efr/) bakın.

- **Varsayılan KDV grubu eşlemesi** – Önceden belirlenmiş KDV gruplarından biriyle eşleştirilemeyen tüm KDV tutarları varsayılan (temel) KDV grubuna atanır. Varsayılan eşleme şöyledir:

    ```
    A
    ```

- **Havale KDV grubu eşlemesi** – Müşteri havale tutarları ve müşteri siparişi havale tutarları, havale KDV grubuna atanır. Varsayılan eşleme şöyledir:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Mali bağlayıcı ayarları

Aşağıdaki ayarlar, mali tümleştirme örneğinin bir parçası olarak sağlanan mali bağlayıcı yapılandırmasına dahil edilmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Zaman aşımı** – Mali bağlayıcının mali kayıt hizmetinden yanıt gelmesini bekleyeceği süre (milisaniye cinsinden).

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Çek Cumhuriyeti için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-cze-fi-sample-sdk.md).
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

Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Örnek, CRT'nin uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Çek Cumhuriyeti için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-cze-fi-sample-sdk.md). Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve mali kayıt hizmetinden gelen yanıtları işlemektir.

#### <a name="request-handler"></a>İstek işleyicisi

Mali kayıt hizmeti için mali belgeler oluşturmak üzere kullanılan, belge sağlayıcısına yönelik tek bir **DocumentProviderEFRFiscalCZE** istek işleyicisi vardır.

Bu işleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler.

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali kayıt hizmetine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satış, müşteri hesabı havaleleri ve müşteri siparişi havaleleri.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Bu istek, mali kayıt hizmetinden gelen yanıtı döndürür. Bu yanıt, kaydedilmeye hazır olması için dize oluşturacak şekilde seri hale getirilir.

#### <a name="configuration"></a>Yapılandırma

Mali belge sağlayıcısına ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** kısmında bulunur. Dosyanın amacı, mali belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali kayıt hizmeti ile iletişim kurmaktır. Hardware station uzantısı, CRT uzantısının oluşturduğu belgeleri mali kayıt hizmetine göndermek için HTTP protokolünü kullanır. Ayrıca, mali kayıt hizmetinden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EFRHandler** istek işleyicisi, mali kayıt hizmetine giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler.

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
