---
title: Almanya için mali kayıt hizmeti tümleştirme örneği
description: Bu konu, Microsoft Dynamics 365 Commerce'taki Almanya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 16079ba5ca830625c4f18df9fe6b5b307217183d
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614056"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Almanya için mali kayıt hizmeti tümleştirme örneği

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'taki Almanya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.

Almanya'da yazar kasalara yönelik yerel mali gereksinimlerin karşılanması amacıyla Almanya için Microsoft Dynamics 365 Commerce işlevi, satış noktasının (POS) harici bir mali kayıt hizmetiyle örnek tümleştirmesini içerir. Bu örnek, [mali tümleştirme işlevini](fiscal-integration-for-retail-channel.md) genişletir. [EFSTA'nın](https://www.efsta.eu/de/) [EFR (Elektronik Yazar Kasa)](https://www.efsta.eu/de/fiskalloesungen/deutschland) çözümüne dayalıdır ve HTTPS protokolü üzerinden EFR hizmetiyle iletişim kurulmasını sağlar. EFR hizmeti, Retail Hardware station'da veya Hardware station'dan bağlanılabilecek ayrı bir bilgisayarda barındırılmalıdır. Örnek, kaynak kodu biçiminde sağlanır ve Commerce yazılım geliştirme setinin (SDK) bir parçasıdır.

Microsoft, EFSTA'dan herhangi bir donanım, yazılım veya belge yayınlamaz. EFR çözümünü edinme ve çalıştırma hakkında bilgi için [EFSTA](https://www.efsta.eu/de/kontakt/kontakt) ile iletişime geçin.

## <a name="scenarios"></a>Senaryolar

Aşağıdaki senaryolar, Almanya için mali kayıt hizmeti tümleştirme örneğinde ele alınmıştır:

### <a name="sales-operations"></a>Satış işlemleri

- **Peşin satış ve iadelerin mali kayıt hizmetine kaydı:**

    Satış işlemlerinin kaydı aşağıdaki adımları içerir:

    1. Hareket başlangıcının kaydı

        Her hareketin başlangıcı, EFR hizmetine bağlı bir teknik güvenlik öğesine (TSE) kaydedilir. Kayıt sonucunda TSE, bir hareket kodu (TID) atar.

    2. Hareket bitişinin kaydı

        POS'ta tamamlanan bir hareket, hareket başlangıcının kaydı sırasında atanan TID ile aynı TID kullanılarak kaydedilir. Şu anda, mali kayıt hizmetine ayrıntılı hareket verileri gönderilmektedir. Bu verilere, satış satırı bilgilerinin yanı sıra iskontolar, ödemeler ve vergiler ile ilgili bilgiler dahildir.

    3. Mali kayıt hizmetinden gelen yanıtı kaydetme

        Güvenlik verileri, yanıtın bir parçası olarak TSE'den alınır ve kanal veritabanındaki hareket içine kaydedilir. Güvenlik verileri aşağıdaki bilgilerden oluşur:

        - TID
        - Hareketin başlangıç tarihi ve saati
        - Hareketin bitiş tarihi ve saati
        - İmza sayacı
        - Çek değeri
        - TSE'nin seri numarası

- **Müşteri siparişlerinin mali kayıt hizmetine kaydı:** Kayıt işlemi, peşin satış ve iade işlemleriyle aynıdır.
- **Hediye kartı ve havale içeren işlemlerin kaydı:** Kayıt işlemi, peşin satış ve iade işlemleriyle aynıdır.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Kullanıcıları mali kayıt hataları hakkında bildirme

Mali kayıt hizmeti, mali kayıt sırasında oluşan hatalar hakkında kullanıcıları iki yöntemle bilgilendirebilir:

- Makbuzlardaki **Bilgi mesajı** alanına karşılık gelen yanıttaki ek bilgileri yazdırma.
- Mali hizmetten alınan bildirimleri POS'ta kullanıcı iletileri olarak gösterme.

    > [!NOTE]
    > Bu bildirim mekanizması, **Bağlayıcı teknik profilleri** sayfasındaki **Mali kayıt bildirimlerini göster** parametresinin açık olmasını gerektirir .

#### <a name="printing-receipts"></a>Makbuzları yazdırma

Makbuz yazdırma, Almanya'da zorunludur. Tüm makbuzlar en azından aşağıdaki bilgileri içermelidir:

- Şirketin adı ve adresi
- Fiyatları ve miktarları dahil olmak üzere mallar hakkında bilgiler
- Alınan ödemeler hakkında bilgiler
- Vergi oranı başına toplam tutarlar dahil olmak üzere vergiler hakkında bilgiler
- Güvenlik verileri:

    - TID
    - Hareketin başlangıç tarihi ve saati
    - Hareketin bitiş tarihi ve saati
    - İmza sayacı
    - Çek değeri
    - TSE'nin seri numarası

- Bilgi iletisi

> [!NOTE]
> Makbuzların üzerine QR kodu da yazdırılabilir. QR kodu isteğe bağlı olsa da önemle önerilir. Mali kayıt hizmetinden gelen yanıtın bir parçası olarak QR kodunun nasıl alınacağı hakkında daha fazla bilgi için [EFSTA belgeleri](https://public.efsta.net/efr/) web sitesindeki "EFR Kılavuzu \[DE\]"belgesine bakın.
>
> Makbuzdaki **Bilgi mesajı** alanı, mali kayıt hizmetinden gelen bir bildirimi gösterir. Örneğin bir imza cihazı bozulduğunda, makbuz üzerine özel metin yazdırılabilir.

#### <a name="voided-suspended-and-recalled-transactions"></a>Hükümsüz kılınmış, askıya alınmış ve geri çekilmiş hareketler

- Hükümsüz kılınmış bir hareket, mali kayıt hizmetindeki bir hareketi sonlandırma isteği olarak kaydedilir.
- Askıya alınmış bir hareket, mali kayıt hizmetindeki bir hareketi sonlandırma isteği olarak kaydedilir.
- Askıya alınmış bir hareketin geri çekilmesi, mali kayıt hizmetindeki yeni bir hareketin başlangıcı olarak kaydedilir.

### <a name="non-sales-transactions-and-shift-closing"></a>Satış dışı hareketler ve vardiya kapanışı

Aşağıdaki satış dışı hareketler, **NFS** etiketi kullanılarak mali kayıt hizmetinde mali olmayan işlemler olarak kaydedilir:

- Başlangıç tutarını beyan et
- Kasa devri girişi
- Ödeme kaldırma
- Kasaya para nakli
- Bankaya para nakli
- Gelir hesapları
- Gider hesapları

**Vardiyayı kapat** işlemi, **NFS** etiketi kullanılarak mali kayıt hizmetinde mali olmayan bir işlem olarak da kaydedilir.

### <a name="data-export-and-audit"></a>Veri dışa aktarma ve denetleme

Hareketlerin bütünlüğünü, gerçekliğini ve eksiksizliğini sağlamak ve kaydedilen verilerin değiştirilmesini önlemeye yardımcı olmak için tüm hareketler bir TSE tarafından imzalanmalıdır.

> [!WARNING]
> Yalnızca onaylı bir TSE kullanılabilir. EFR çözümünde desteklenen TSE türleri ve modelleri hakkında bilgi için [EFSTA belgeleri](https://public.efsta.net/efr/) web sitesinde yayınlanan "EFR Kılavuzu \[DE\]" belgesine bakın. TSE'nin nasıl seçileceği ve edinileceği hakkında daha fazla bilgi için [EFSTA](https://www.efsta.eu/at/kontakt) ile iletişime geçin.

Almanya'daki yönetmelikler, DSFinV-K dışa aktarımının desteklenmesini gerektirir. DSFinV-K dışa aktarımı EFR çözümünde tetiklenebilir. DSFinV-K dışa aktarımı hakkında daha fazla bilgi için [EFSTA belgeleri](https://public.efsta.net/efr/) web sitesinde yayınlanan "EFR Kılavuzu \[DE\]" belgesine bakın.

### <a name="limitations-of-the-sample"></a>Örneğin sınırlamaları

Mali kayıt hizmeti yalnızca satış vergisinin fiyatlara dahil edildiği senaryoları destekler. Bu nedenle, **Fiyatlara satış vergisi dahildir** seçeneği hem mağazalar hem de müşteriler için **Evet** olarak ayarlanmalıdır.

Mali hizmet, aynı hareket satırına birden fazla satış vergisi kodunun uygulandığı durumları desteklemez.

Mali tümleştirme çerçevesi, satış tekliflerini desteklemez. Bu nedenle, bu işlemler mali hizmete kayıtlı değildir.

## <a name="set-up-commerce-for-germany"></a>Almanya için Commerce'ı ayarlama

Bu bölümde, Almanya'ya özel veya Almanya için önerilen Commerce ayarları açıklanmaktadır. Daha fazla kurulum bilgisi için bkz. [Commerce giriş sayfası](../index.md).

Almanya'ya özel işlevleri kullanmak için aşağıdaki ayarları belirtmeniz gerekir.

- Tüzel kişiliğin birincil adresinde, **Ülke/bölge** alanını **DEU** (Almanya) olarak ayarlayın.
- Almanya'da bulunan her mağazanın POS işlevi profilinde, **ISO kodu** alanını **DE** (Almanya) olarak ayarlayın.

Almanya için aşağıdaki ayarları da belirtmeniz gerekir. Kurulumu tamamladıktan sonra uygun dağıtım işlerini çalıştırdığınızdan emin olun.

### <a name="set-up-vat-per-german-requirements"></a>Almanya gereksinimleri uyarınca KDV'yi ayarlama

Satış vergisi kodları, satış vergisi grupları ve madde satış vergisi grupları oluşturmanız gerekir. Ayrıca, ürün ve hizmetlerle ilgili satış vergisi bilgilerini de ayarlamanız gerekir. Satış vergisi özelliklerinin nasıl ayarlanacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Satış vergisine genel bakış](../../finance/general-ledger/indirect-taxes-overview.md).

Satış makbuzlarında, bir satış vergisi kodu için kısaltılmış bir kod (örneğin, "A" veya "B") yazdırabilirsiniz. Bu işlevi kullanılabilir hale getirmek için **Satış vergisi kodları** sayfasındaki **Yazdırma kodları** alanını ayarlayın.

### <a name="set-up-stores"></a>Mağazaları ayarlama

**Tüm mağazalar** sayfasında, mağaza ayrıntılarını güncelleştirin. Özellikle aşağıdaki parametreleri ayarlayın:

- **Satış vergisi grubu** alanında, varsayılan müşteriye yapılacak satışlarda kullanılması gereken satış vergisi grubunu belirtin.
- **Fiyatlara satış vergisi dahildir** seçeneğini **Evet** olarak ayarlayın.
- **Ad** alanını şirket adı olarak ayarlayın. Bu değişiklik, şirket adının satış makbuzunda göründüğünden emin olmanıza yardımcı olur. Alternatif olarak, şirket adını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.
- **Vergi kimlik numarası (TIN)** alanını şirket kimlik numarası olarak ayarlayın. Bu değişiklik, şirket kimlik numarasının satış makbuzunda göründüğünden emin olmanıza yardımcı olur. Alternatif olarak, şirket kimlik numarasını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.

### <a name="set-up-functionality-profiles"></a>İşlev profillerini ayarlama

POS işlevi profillerini ayarlayın. **Makbuz numaralandırma** hızlı sekmesinde **Satış**, **Satış siparişi** ve **İade** makbuz hareket türleri için kayıt oluşturarak veya mevcut kayıtları güncelleştirerek makbuz numaralandırmasını ayarlayın.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Özel alanları, satış makbuzlarına yönelik makbuz biçimlerinde kullanılabilecek şekilde yapılandırma

POS makbuz biçimlerinde kullanılan dil metnini ve özel alanları yapılandırabilirsiniz. Makbuz kurulumunu oluşturan kullanıcının varsayılan şirketi, dil metni kurulumunun oluşturulduğu tüzel kişilikle aynı olmalıdır. Alternatif olarak, aynı dil metinleri hem kullanıcının varsayılan şirketinde hem de kurulumun oluşturulduğu mağazanın tüzel kişiliğinde oluşturulmalıdır.

**Dil metni** sayfasında, makbuz düzenlerine yönelik özel alanların etiketlerine aşağıdaki kayıtları ekleyin. Tabloda gösterilen **Dil Kodu**, **Metin Kodu** ve **Metin** değerlerinin yalnızca örnek olduğunu unutmayın. Bunları gereksinimlerinizi karşılayacak şekilde değiştirebilirsiniz. Ancak kullandığınız **Metin Kodu** değerleri benzersiz ve 900001'e eşit veya bundan daha büyük olmalıdır.

Aşağıdaki POS etiketlerini tablodaki **Dil metni** sayfasının **POS** bölümüne ekleyin.

| Dil kodu | Metin Kodu | Metin                                  |
|-------------|---------|---------------------------------------|
| tr-TR       | 900001  | QR kodu                               |
| tr-TR       | 900002  | Hareket Kodu                        |
| tr-TR       | 900003  | Vergi Perakende Yazdırma Kodu                 |
| tr-TR       | 900004  | Vergi Tutarı (satış)                    |
| tr-TR       | 900005  | Vergi Matrahı (satış)                     |
| tr-TR       | 900006  | Hareket başlangıç tarihi saati           |
| tr-TR       | 900007  | Hareket bitiş tarihi saati             |
| tr-TR       | 900008  | Güvenlik öğesinin seri numarası |
| tr-TR       | 900009  | İmza sayacı                     |
| tr-TR       | 900010  | Çek değeri                           |
| tr-TR       | 900011  | Bilgi iletisi                          |

**Özel alanlar** sayfasında, makbuz düzenlerine yönelik özel alanlara aşağıdaki kayıtları ekleyin. **Açıklamalı alt yazı metni kodu** değerlerinin, **Dil metni** sayfasında belirttiğiniz **Metin Kodu** değerlerine karşılık gelmesi gerektiğini unutmayın.

| Ad                            | Tür    | Altyazı metni kodu |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Giriş | 900001          |
| TRANSACTIONID\_DE               | Giriş | 900002          |
| RETAILPRINTCODE\_DE             | Giriş | 900003          |
| SALESTAXAMOUNT\_DE              | Giriş | 900004          |
| SALESTAXBASIS\_DE               | Giriş | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Giriş | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Giriş | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Giriş | 900008          |
| SIGNCOUNTER\_DE                 | Giriş | 900009          |
| SIGN\_DE                        | Giriş | 900010          |
| INFOMESSAGE\_DE                 | Giriş | 900011          |

> [!NOTE]
> Önceki tabloda listelendiği gibi, doğru özel alan adlarını belirtmeniz önemlidir. Yanlış bir özel alan adı, makbuzlardaki verilerin eksik olmasına neden olur.

### <a name="configure-receipt-formats"></a>Makbuz biçimlerini yapılandırma

Gerekli her makbuz biçimi için **Yazdırma davranışı** alanının değerini **Her zaman yazdır** olarak değiştirin.

Makbuz biçimi tasarımcısında, aşağıdaki özel alanları ilgili makbuz bölümlerine ekleyin. Alan adlarının önceki bölümde tanımladığınız dil metinlerine karşılık geldiğini unutmayın.

- **Üst bilgi:** Aşağıdaki alanları ekleyin:

    - Makbuzlara şirket adını ve kimlik numarasını yazdırmak için kullanılan **Mağaza adı** ve **Vergi Kimlik Numarası** alanları. Alternatif olarak, şirket adını ve kimlik numarasını satış makbuzu düzenine serbest biçimli metin olarak da ekleyebilirsiniz.
    - **Mağaza adresi**, **Tarih**, **Zaman 24Sa**, **Makbuz Numarası** ve **Kayıt numarası** alanları.

- **Satırlar:** Aşağıdaki alanları ekleyin:

    - **Madde adı** alanı
    - **Miktar** alanı
    - **Vergiyle birlikte toplam fiyat** alanı
    - Maddeye uygulanan satış vergisi koduna karşılık gelen kısaltılmış kodu yazdırmak için kullanılan **Vergi Perakende Yazdırma Kodu** alanı

- **Alt bilgi:** Aşağıdaki alanları ekleyin:

    - Her ödeme yöntemine ait ödeme tutarlarının yazdırılması için ödeme alanları. Örneğin, **Ödeme adı** ve **Ödeme tutarı** alanlarını düzenin bir satırına ekleyin.
    - **Vergi dökümü** alan grubundaki alanlar. Bu alan grubundaki tüm alanlar ayrı bir satırda yazdırılmalıdır.

        - Her satış vergisi kodu için satış vergisi özetinin yazdırılmasını sağlayan standart bir alan olan **Vergi Kodu** alanı. Alan yeni satıra eklenmelidir.
        - Satış vergisi koduna ilişkin geçerli vergi oranını yazdırmak için kullanılan standart bir alan olan **KDV Yüzdesi** alanı.
        - Satış vergisi kodu için makbuzun toplam nakit satış tutarını yazdırmak üzere kullanılan **Vergi Matrahı (satış)** alanı. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
        - Satış vergisi kodu için makbuzun toplam nakit satış vergi tutarını yazdırmak üzere kullanılan **Vergi Tutarı (satış)** alanı.
        - Satış vergisi koduna karşılık gelen kısaltılmış kodu yazdırmak için kullanılan **Vergi Perakende Yazdırma Kodu** alanı.

    - Mali kayıt hizmeti tarafından döndürülen güvenli hareket verilerini içeren alanlar:

        - Mali kayıt hizmetindeki nakit hareketi sayısını tanımlayan **Hareket Kodu** alanı
        - **Hareketin başlangıç tarihi** alanı
        - **Hareketin bitiş tarihi** alanı
        - **Güvenlik öğesinin seri numarası** alanı
        - **İmza sayacı** alanı
        - **Çek değeri** alanı
        - Kayıtlı nakit hareketine yönelik başvuruyu QR kodu biçiminde yazdırmak için kullanılan **QR Kodu** alanı

        > [!NOTE]
        > **QR Kodu** değeri, yazar kasa yanıtından alınır. EFR yalnızca, EFR yapılandırmasındaki **Öznitelikler** alanında yer alan değerin EFSTA belgelerinde açıklanması halinde yanıtında QR kodu döndürür. EFR yapılandırmasındaki **Öznitelikler** alanında bulunan QR kodu biçiminin **BMP** olarak ayarlanması gerekir.

    - Mali kayıt hizmetinden gelen bildirim iletilerinin makbuzlarda gösterilebilmesi için **Bilgi mesajı** alanı. Örneğin bir imza cihazı bozulduğunda, makbuz üzerine özel metin yazdırılabilir.

Makbuz biçimleriyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Makbuz biçimlerini ayarlama ve tasarlama](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Almanya için mali tümleştirmeyi ayarlama

Almanya için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Örnek, Commerce Runtime'ın (CRT) uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Almanya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-deu-fi-sample-sdk.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

[Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md) konusunda açıklandığı şekilde mali tümleştirme ayarlama adımlarını tamamlayın:

1. [Bir mali kayıt işlemi ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ayrıca, [bu mali kayıt hizmeti tümleştirme örneğine özgü](#set-up-the-registration-process) mali kayıt işlemi ayarlarını da not edin.
1. [Hata işleme ayarlarını belirleyin](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Mali tümleştirme çerçevesinin hata işleme özellikleri, yerel mali yönetmeliklerle tam olarak uyumlu olmayabilir.
    >
    > - İlk mali kayıt denemesi başarısız olsa bile tüm hareketlerin doğru şekilde kaydedilmesi gerektiğinden, **Mali kayıt işlemi** sayfasındaki **Hatada devam et** seçeneğini kapalı tutmanızı öneririz.
    > - **Mali kayıt işlemi** sayfasındaki **Atla** veya **Kaydedildi olarak işaretle** seçeneğini etkinleştirmeden önce, mali kayıt işlemindeki bu değişiklikleri vergi danışmanınızla veya yerel vergi dairenizle görüşmeniz gerekir.

1. [Ertelenen mali kaydın el ile yürütülmesini etkinleştirin](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanal bileşenlerini yapılandırın](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Mali kayıt işlemini ayarlama

Kayıt işlemini etkinleştirmek üzere Commerce Headquarters'ı ayarlamak için aşağıdaki adımları izleyin. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Mali belge sağlayıcısı ve mali bağlayıcı için yapılandırma dosyalarını indirin:

    1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunu açın.
    1. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin (örneğin, **[sürüm/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. **src \> FiscalIntegration \> Efr**'yi açın.
    1. Mali belge sağlayıcısı yapılandırma dosyasını **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)) kısmından indirin.
    1. Mali bağlayıcı yapılandırma dosyasını **Configurations \> Connectors \> ConnectorEFRSample.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)) kısmından indirin.

    > [!WARNING]
    > [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Bu mali tümleştirme örneğinin yapılandırma dosyaları, LCS'deki bir geliştirici VM'sinde Retail SDK'nin aşağıdaki klasörlerinde bulunur:
    >
    > - **Mali belge sağlayıcısı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
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

- **Ödeme türü eşlemesi** – Ödeme yöntemlerinin, mali hizmete gönderilen isteklerdeki **PayG** (ödeme grubu) özniteliğinin değerleriyle eşlenmesi. Varsayılan eşleme şöyledir:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Her bir çiftin ilk bileşeni, mağaza için ayarlanan bir ödeme yöntemini gösterir. İkinci bileşen, EFR mali kayıt hizmeti tarafından desteklenen ilgili ödeme grubunu temsil eder. Almanya'da EFR'nin desteklediği ödeme grupları hakkında daha fazla bilgi için [EFR referansına](https://public.efsta.net/efr/) bakın.

    Ödeme yöntemlerinin örnek eşlemesi, standart tanıtım verilerinde yapılandırılan ödeme yöntemlerine karşılık gelir.

    | Ödeme yöntemi | Ödeme yöntemi adı |
    |----------------|---------------------|
    | 1              | Nakit                |
    | 2              | Denetle               |
    | 3              | Kart                |
    | 4              | Müşteri hesabı    |
    | 5              | Diğer               |
    | 6              | Para Birimi            |
    | 7              | Fiş             |
    | 8              | Hediye kartı           |
    | 9              | Ödeme Kaldırma/Kaydırma |
    | 10             | Bağlılık Programı Kartları       |
    | 11             | Yerel olmayan çekler    |

    Bu nedenle, örnek eşlemeyi uygulamanızda yapılandırılan ödeme yöntemlerine göre değiştirmeniz gerekir.

- **Müşteri verilerini dahil et** – Bu parametre açıksa mali hizmete gönderilen istekler, müşterinin bir harekete eklendiği durumlarda ad ve adres gibi müşteri bilgilerini içerecektir.
- **Katma değer vergisi (KDV) oranlarının eşlemesi** – Satış vergisi kodları için ayarlanan vergi yüzdesi değerlerinin, mali hizmete gönderilen isteklerdeki **TaxG** (vergi grubu) özniteliğinin değerleriyle eşlenmesi. Varsayılan eşleme şöyledir:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Her bir çiftteki ilk bileşen, EFR mali kayıt hizmeti tarafından desteklenen bir KDV vergi grubunu temsil eder. İkinci bileşen, karşılık gelen KDV oranını temsil eder. Almanya'da EFR'nin desteklediği KDV vergi grupları hakkında daha fazla bilgi için [EFR referansına](https://public.efsta.net/efr/) bakın.

- **Hediye kartları ve havaleler için vergi grubu** – Hediye kartları veya havalelerle ilgili işlemler temel alınarak mali hizmete gönderilen isteklerdeki **TaxG** özniteliğinin değeri. Varsayılan eşleme şöyledir:

    ```
    G
    ```

- **KDV muafiyeti için vergi grubu** – Vergi yükümlülüklerinden muaf tutulan işlemler temel alınarak mali hizmete gönderilen isteklerdeki **TaxG** özniteliğinin değeri. Varsayılan eşleme şöyledir:

    ```
    F
    ```

> [!NOTE]
> Varsayılan veri eşlemesindeki vergi ayarları, EFR hizmetinde bulunan sistem ve vergi gruplarındaki eşleşen vergi ayarlarından sorumludur. Vergi grupları yalnızca, **Satış vergisi kodları** sayfasında **Yazdırma kodu** alanı ayarlandıysa makbuzlara yazdırılabilir.

#### <a name="fiscal-connector-settings"></a>Mali bağlayıcı ayarları

Aşağıdaki ayarlar, mali tümleştirme örneğinin bir parçası olarak sağlanan mali bağlayıcı yapılandırmasına dahil edilmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Zaman aşımı** – Mali bağlayıcının mali kayıt hizmetinden yanıt gelmesini bekleyeceği süre (milisaniye cinsinden).
- **Mali kayıt bildirimlerini göster** – Bu bayrak, mali kayıt hizmetinin döndürdüğü bildirimlerin operatöre gösterilip gösterilmeyeceğini denetler.

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Almanya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-deu-fi-sample-sdk.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

#### <a name="set-up-the-development-environment"></a>Geliştirme ortamını ayarlama

Örneği test etmek ve genişletmek üzere bir geliştirme ortamı ayarlamak için aşağıdaki adımları izleyin.

1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunu klonlayın veya indirin. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin. Daha fazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** kısmından EFR çözümünü açın ve derleyin.
1. Commerce Runtime uzantılarını yükleyin:

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

Almanya için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Örnek, CRT'nin uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Almanya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-deu-fi-sample-sdk.md). Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

### <a name="crt-extension-design"></a>CRT uzantısı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve mali kayıt hizmetinden gelen yanıtları işlemektir.

#### <a name="request-handler"></a>İstek işleyicisi

Belge sağlayıcısı olan **DocumentProviderEFRFiscalDEU** için bir istek işleyicisi mevcuttur. Bu işleyici, mali kayıt hizmeti için mali belgeler oluşturmak üzere kullanılır. **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali kayıt hizmetine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Bu istek, yanıtı genişletilmiş verilerle birlikte döndürür.

#### <a name="configuration"></a>Yapılandırma

Mali belge sağlayıcısına ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** kısmında bulunur. Dosyanın amacı, mali belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali kayıt hizmeti ile iletişim kurmaktır.

Hardware station uzantısı, **HardwareStation.Extension.EFRSample** öğesidir. CRT uzantısının oluşturduğu belgeleri mali kayıt hizmetine göndermek için HTTP protokolünü kullanır. Ayrıca, mali kayıt hizmetinden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EFRHandler** istek işleyicisi, mali kayıt hizmetine giden isteklerin işlenmesi için giriş noktasıdır. Bu işleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

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
