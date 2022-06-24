---
title: Konum kapasitesine göre stok yenileme
description: Bu makale, Konum kapasitesine göre stok yenileme özelliği hakkında bilgi sağlar. Bu özellik, gün için gerekli olacak tüm stok yenileme işini etkinleştirir ve malzeme çekme konumunun stok dışında veya kapasitenin üzerine geçmediğinden emin olmak amacıyla bu stok yenileme çalışmasının kullanılabilirliğini yönetir.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 72cda7608d55414ee62bc7dcc1e02e28f6212aff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899251"
---
# <a name="replenishment-over-location-capacity"></a>Yerleşim kapasitesine göre stok yenileme

[!include [banner](../includes/banner.md)]

Bazı yüksek hacimli veya alan kısıtlamalı ambarlar, malzeme çekme konumuna sığmayacak bir gün içindeki kalem miktarını sevk etmelidir. *Konum kapasitesine göre stok yenileme* özelliği, gün için gerekli olacak tüm stok yenileme işini etkinleştirir ve malzeme çekme konumunun stok dışında veya kapasitenin üzerine geçmediğinden emin olmak amacıyla bu stok yenileme çalışmasının kullanılabilirliğini yönetir.

Özellik, bir konuma sığacak olandan daha fazla stok yenileme işinin oluşturulmasını sağlar ve konum dolduğunda, stok yenileme işinin tamamlanmasını engeller. Malzeme çekme konumundaki stok yapılandırılabilir bir eşiğin altına düşerse daha fazla stok yenileme işi kullanılabilir duruma getirilir.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Konum kapasitesine göre stok yenileme özelliğini açma

Bu özelliği kullanılabilir hale getirmek için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. Kuruluş genelinde iş durdurma (Supply Chain Management sürüm 10.0.21 itibariyle bu özellik zorunludur; bu nedenle varsayılan olarak açıktır ve yeniden kapatılamaz.)
1. Konum kapasitesine göre stok yenileme

## <a name="set-up-the-feature-for-the-example-scenario"></a>Örnek senaryo için özelliği ayarlama

Bu bölümde, bu özelliğin nasıl ayarlanacağı ve bu makalenin ilerleyen kısımlarında sağlanan örnek senaryo için örnek verilerin nasıl hazırlanacağı gösterilmektedir.

### <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak [örnek senaryo](#example-scenario) üzerinden çalışmak için standart [demo verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="location-profile"></a>Yerleşim profili

Konum profilinde kapasiteye göre stok yenileme işlevini etkinleştirin.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Sol bölmede **PICK-06** seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Stok yenileme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Konum Kapasitesini Aş:** *Evet*

        Etkin olduğunda, yerleşimin maksimum kapasitesinin stok yenileme işi tarafından aşılmasına izin verilir. Ayrıca, **Stok yenileme** hızlı sekmesindeki diğer alanları da etkinleştirir.

    - **İş kullanılabilirlik eşiği türü:** *Miktar*

        Bu alan, ne kadar işin serbest bırakılacağını belirlemek için kullanılan yöntemi tanımlar. Miktar ya da yüzdeye göre serbest bırakabilirsiniz:

        - *Yüzde* - Stok sınırları veya hacimlere göre kapasite yüzdesi kullanmak için bu seçeneği işaretleyin. Bu seçeneğin belirlenmesi **Taşma yüzdesi** alanını etkinleştirir ve ilgili iki miktar alanı olan **Taşma miktarı** ve **Taşma birimi**'ni devre dışı bırakır.

            Malzeme çekme konumları hacim kullanıyorsa bu seçeneği kullanabilirsiniz.

            Bu seçenek işaretliyse **Taşma yüzdesi** alanını daha fazla stok yenileme işinin kullanılabilir hale gelmesini sağlayacak yüzdeye ayarlayın.

        - *Miktar* - Belirli bir miktar değeri kullanmak için bu seçeneği belirleyin. Bu seçeneğin belirlenmesi **Taşma yüzdesi** alanını devre dışı bırakır ve **Taşma miktarı** ile **Taşma birimi** alanlarını etkinleştirir.

            Stok yenilenen konumlarda hacim kullanmıyorsanız veya konuma daha fazla stok getirilmesini istediğiniz tutarlı miktarlar olduğunda bu seçeneği kullanın.

           Bu seçenek işaretliyse **Taşma miktarı** ve **Taşma birimi** alanlarını daha fazla stok yenileme işinin kullanılabilir hale gelmesini sağlayacak miktara ve birime ayarlayın.

    - **Taşma miktarı:** *0,65*

        Bu alan, konumun taştığı miktarı tanımlar.

        İş, konumdaki eldeki stok miktarı ve iş miktarı toplamı bu değerin altında olduğunda kullanılabilir olur. Bu değerin üzerindeki tüm stok yenileme işleri engellenir ve engellemenin el ile kaldırılması gerekir.

        Konum stok sınırlamaları, iş miktarı hesaplanırken dikkate alınır.

    - **Taşma birimi:** *PL*

        Bu alan taşma miktarıyla ilişkilendirilmiş birimi tanımlar.

        Bu durumda, konum 0,65 palet (PL) olarak ayarlandığında, daha fazla stok yenileme işi kullanılabilir duruma gelir.

    - **Taşma yüzdesi**

        Bu alan, konumun taştığı yüzdeyi tanımlar.

        İş, konumdaki eldeki stok miktarı ve iş miktarı toplamı bu yüzdenin altında olduğunda kullanılabilir olur. Bu değerin üzerindeki tüm stok yenileme işi miktarı yüzdesi engellenir ve engellemenin el ile kaldırılması gerekir.

        Konum stok sınırlamaları, iş miktarı yüzdesi hesaplanırken dikkate alınır. Konum stok sınırlarının tanımlanmaması durumunda, konum profili için birim kısıtlamaları tanımlandıysa iş miktarı yüzdesi birime göre hesaplanır.

> [!IMPORTANT]
> **USMF** tüzel kişiliği ve daha önce etkinleştirilen *Konum plakası konumlandırması* özelliği için demo verileri kullanıyorsanız, örnek senaryoda mobil adımları tamamlamak için **BULK-06** konum profilinin **Plaka konumlandırmayı etkinleştir** ayarını kapatmanız gerekir.

### <a name="wave-step-code"></a>Dalga adım kodu

> [!NOTE]
> Burada açıklandığı gibi bir dalga adımı kodu ayarlamak için öncelikle *Kuruluş genelinde dalga adımı kodu* adlı özelliği açmak üzere [özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanmanız gerekebilir.

1. **Ambar Yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin.
1. **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:

    - **Dalga adımı kodu:** *Stok yenileme*
    - **Dalga adımı açıklaması:** *Stok yenileme*
    - **Dalga adımı türü:** *Stok yenileme*

1. **Kaydet**'i seçin.

### <a name="replenishment-template"></a>Stok yenileme şablonu

Stok yenileme şablonları, bir konumda stokun ne zaman ve nasıl yenileneceğini denetleyen kural kümesidir.

1. **Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel Bakış** bölümünde, **Stok yenileme şablonu** alanının *Talep stok yenilemesi* olarak ayarlandığı satırı seçin.
1. Aşağıdaki değerleri ayarlayın:

    - **Dalga adımı kodu:** *Stok yenileme*
    - **Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver:** *Evet*

1. **Kaydet**'i seçin.

### <a name="wave-template"></a>Dalga şablonu

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Sol bölmede, **Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.
1. Listeden **61 Sevkiyat** şablonunu seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde **Stok yenileme işi serbest bırakmayı otomatik hale getir** seçeneğini *Evet* olarak ayarlayın.

    Talep tabanlı stok yenileme işi oluşturmak ve bunu otomatik olarak serbest bırakmak için bu seçeneği *Evet* olarak ayarlayın. Stok yenileme dalga yöntemini dalga şablonuna eklemeniz **Dalga talebi** türünde stok yenileme şablonu oluşturmanız gerekir. **Stok yenileme şablonları** sayfasında bir stok yenileme şablonu ayarlayın. Stok yenileme şablonu ayarlamak için bu stok yenileme yöntemini dalga şablonuna eklemeniz gerekir.

1. **Yöntemler** hızlı sekmesinde, **Seçili yöntemler** sütununda, aşağıdaki satırı bulun:

    - **Yöntem adı:** *stok yenileme*
    - **Ad:** *Stok yenileme*

1. Bu satır için **Dalga adımı kodu** alanını *Stok yenileme* olarak ayarlayın.
1. **Kaydet**'i seçin.

## <a name="example-scenario"></a>Örnek senaryo

Daha önce açıklanan örnek verilerin tümünü kullanılabilir hale getirip ayarladıktan sonra, bu senaryoda, *Konum kapasitesine göre stok yenileme* özelliğini deneyebilirsiniz. Bu senaryoda gösterilen değerler, standart demo verileriyle çalıştığınızı, **USMF** tüzel kişiliğini seçmiş olduğunuzu ve bu makalenin önceki bölümlerinde açıklanan örnek kayıtları hazırladığınızı varsayar. Bu senaryo aynı zamanda özelliğin bir üretim ayarında nasıl kullanılabileceğini gösteren bir örnek işlevi de görür.

### <a name="create-replenishment-work"></a>Stok yenileme işi oluştur

#### <a name="create-sales-order-1"></a>Satış siparişi oluşturma 1

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, yeni satış siparişi oluşturma iletişim kutusunu açmak için **Yeni**'yi seçin.
1. İletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Müşteri hesabı:** *US-007*
    - **Ambar:** *61*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde yeni, boş bir satır bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *T0100*
    - **Miktar:** *40*

1. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.
1. Sayfayı kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bilgi iletileri alırsınız. Ayrıca bir stok yenileme dalgası da oluşturulur.

    "İş kimliği XXXX, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir uyarı iletisi alırsınız.

#### <a name="create-sales-order-2"></a>Satış siparişi oluşturma 2

1. **Tüm satış siparişleri** sayfasında, Eylem Bölmesinde, yeni satış siparişi oluşturma iletişim kutusunu açmak için **Yeni**'yi seçin.
1. İletişim kutusunda aşağıdaki değeri ayarlayın.

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *61*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde yeni, boş bir satır bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *T0100*
    - **Miktar:** *60*

1. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.
1. Sayfayı kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bilgi iletileri alırsınız. Ayrıca bir stok yenileme dalgası da oluşturulur.

    "İş kimliği XXXX, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir uyarı iletisi alırsınız.

#### <a name="create-sales-order-3"></a>Satış siparişi oluşturma 3

1. **Tüm satış siparişleri** sayfasında, Eylem Bölmesinde, yeni satış siparişi oluşturma iletişim kutusunu açmak için **Yeni**'yi seçin.
1. İletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Müşteri hesabı:** *US-004*
    - **Ambar:** *61*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde yeni, boş bir satır bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *T0100*
    - **Miktar:** *30*

1. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.
1. Sayfayı kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bilgi iletileri alırsınız. Ayrıca bir stok yenileme dalgası da oluşturulur.

    "İş kimliği XXXX, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir uyarı iletisi alırsınız.

#### <a name="view-work-details"></a>İş ayrıntılarını görüntüleme

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. **Genel Bakış** bölümünde, ambar *61* için **Ambar** sütununa filtre uygulayın.
1. Üç talepli satış siparişi için yedi iş kodu oluşturulduğunu görürsünüz.

    - Yedi iş kodunun üçünde, **İş emri türü** için *Stok yenileme* değerine ve dördü ise **İş emri türü** için *Satış siparişleri* değerine sahiptir.
    - **İş emri türü** için *Stok yenileme* değerine sahip olan üç iş kodu, **Satırlar** bölümünde aynı *Malzeme çekme* ve *Yerine koyma* konumlarına sahiptir:

        - **Malzeme çekme:** *02A01R5S1B*
        - **Yerine koyma:** *06A01R2S1B*

    - Satış siparişi 1 için iki iş kodu oluşturuldu.

1. Satış siparişinin iş kodlarını not edin.

Eldeki miktarlarınıza bağlı olarak, oluşturulan iş miktarları biraz farklı olabilir. Ancak, oluşturulan iş başlıklarının tümü bu senaryo örneği ile eşleşmelidir.

#### <a name="on-hand-inventory-license-plate-id"></a>Eldeki stok plakası kodu

Bu senaryonun devamında, malzeme çekme ve stok yenileme senaryolarını tamamlamak için plakalevhasını tanımlamanız gereken Ambar Yönetimi mobil uygulamasını (veya bir emülatör) kullanacaksınız.

Daha sonra gereksinim duyacağınız plaka kodlarını bulmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Sorgular ve raporlar \>> Eldeki stok** öğesine gidin.
1. Filtre bölmesini açmak için **Filtreleri göster** düğmesini seçin.
1. Senaryo için plakaları almak üzere aşağıdaki filtre ölçütlerini girin. *Şununla başlar* filtresini kullanın.

    - **Madde numarası:** *T0100*
    - **Ambar:** *61*

1. **Uygula**'yı seçin.
1. Eylem Bölmesinde **Boyutlar** öğesini seçin.
1. **Boyutlar görünümü** iletişim kutusunda **Depolama Boyutları** bölümünde, tüm değerleri seçin.
1. **Hareketler** bölümünde, **Kalem numarası** ve **Miktar \<\> 0**'ı seçin.
1. Bitirdiğinizde iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Eldeki stok** kılavuzu her bir konumdaki *T0100* kalemi için plaka numaralarını gösterir. Daha sonra bu bilgilere gereksinim duyacağınız için her konumdaki plakayı not edin.
1. Sayfayı kapatın.

### <a name="process-steps"></a>İşlem adımları

İlk iki iş kodu için ambar konumu stok yenileme işlemi gerçekleştirin. Üçüncü stok yenileme işi üzerindeki çalışma, malzeme çekme konumundaki stok düzeyi eşiğin altında oluncaya kadar engellenir.

#### <a name="replenishment"></a>Stok yenileme

1. Ambar *61*'de bir kullanıcı olarak Ambar Yönetimi mobil uygulamasına oturum açın. (Kullanıcı kimliği olarak *61*, parola olarak *1* girin.)
1. **Stok \> Stok yenileme**'ye gidin.

    İlk stok yenileme işlemini tamamlamanız istenir. Kalem numarası, miktar ve malzeme çekme konumu gösterilir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.
1. **Tamam** düğmesini (onay işareti sembolü) seçin.

    Sistem, çekilen kalemin yeni plakaso için bir hedef plaka numarası oluşturur.

1. Değeri onaylamak için **Tamam**'ı seçin.

    Kullanıcıya hedef plakayı stok yenileme konumuna koymasını bildiren yerine koyma işi gösterilir. *Yerine koyma* konumu **06A01R2S1B** olmalıdır.

1. Yerine koyma ayrıntılarını onaylayın ve **Tamam**'ı seçin.

    "İş Tamamlandı" iletisi alırsınız ve sonraki stok yenileme malzeme çekme görevinin ayrıntıları gösterilir: kalem numarası, miktar ve malzeme çekilecek konum. Malzeme çekme konumu ilk stok yenileme konumuyla aynı olacaktır. Bu nedenle, plaka ilk stok yenileme işi görevi için kullanılan plakayla aynı koda sahip olacaktır.

1. İkinci iş göreviyle ilgili stok yenileme işini tamamlamak için önceki adımları yineleyin. Miktar ve hedef plaka, ilk iş göreviyle ilgili miktar ve hedef plakadan farklı olacaktır.

İkinci stok yenileme işi tamamlandıktan sonra, "İş Tamamlandı" iletisi alırsınız. Mobil cihaz da bazı stok yenileme işleri kalsa bile, kullanılabilir iş olmadığını bildirir. Bu davranış, stok yenileme işinin kullanılabilirlik durumunun *Bekletiliyor* olması nedeniyle oluşur ve bu nedenle **Engellendi** olarak işaretlenir.

İşin atandığı malzeme çekme konumunun konum profilinin **Taşma miktarı** değeri *0,65 PL* olduğu için *Bekletiliyor* durumu tetiklenmiştir. Önceki iki stok yenileme işi görevi, konumu *T0100* kalemi için neredeyse taşma sınırına kadar doldurmuştur. (Kalemin birim dönüştürmesi *1 PL = 100 beher* şeklindedir.) Bu nedenle, kalan stok yenileme işi, konumun taşma sınırını aşmasına neden olur.

Konumdan yeterince stok çekilene kadar mobil cihaz menü öğesindeki iş serbest bırakma eşiğinin altına getirmek için bu stok yenileme işi engellenmiş olarak kalır.

#### <a name="sales-order-pick"></a>Satış siparişi çekme

Kalan stok yenileme görevinin tamamlanabilmesi için önce, malzeme çekme konumunda stokun kalan stok yenileme işini engellemeyecek bir düzeyde olması gerekir. Başka bir deyişle,konumdaki eldeki stok miktarının ve stok yenileme miktarının toplamı, **Taşma miktarı** değerini aşamaz. Bu toplam, taşma miktarından az olduğunda, kalan stok yenileme işinin engeli kaldırılır.

1. Ambar *61*'de bir kullanıcı olarak Ambar Yönetimi mobil uygulamasına oturum açın. (Kullanıcı kimliği olarak *61*, parola olarak *1* girin.)
1. **Giden \> Satış çekme**'ye gidin.
1. Satış siparişi 1'in ilk iş kodunu girin.

    Daha önce **İş ayrıntıları** sayfasında not ettiğiniz satış siparişleri iş kodlarına bakın. Buraya gireceğiniz iş kodu, iki ayrı konumdan 10 beher miktarında malzeme çekme işi oluşturur.

1. **Tamam**'ı seçin.

    **Satış siparişleri: Malzeme çekme** görevi sayfası, ilk konum için kalem numarası, miktar ve malzeme çekilecek konumu gösterir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.
1. **Tamam** düğmesini (onay işareti sembolü) seçin.

    **Satış siparişleri: Malzeme çekme** görevi sayfası, sonraki konum için kalem numarası, miktar ve malzeme çekilecek konumu gösterir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.
1. **Tamam** düğmesini (onay işareti sembolü) seçin.

    **Satış siparişleri: Yerine koyma** sayfasında, tamamlanan her iki işi giden hazırlama konumuna yerine koymanız istenir.

1. **Tamam**'ı seçin.

    Bir "İş Tamamlandı" iletisi alırsınız.

1. Satış siparişi 1'in ikinci iş kodunu girin.

    Bu iş kodu için yalnızca bir malzeme çekme görevi vardır.

1. **Tamam**'ı seçin.

    **Satış siparişleri: Malzeme çekme** görevi sayfası, kalem numarası, miktar ve malzeme çekilecek konumu gösterir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.

    Belirttiğiniz plaka, stok yenileme işi görevlerinden alınan sistem tarafından oluşturulan plakalardan biridir. Doğru plaka kodunu aldığınızdan emin olmak için kalem, konum ve miktar açısından **Eldeki stok listesi** sayfasındaki stoku kontrol edin.

1. **Tamam** düğmesini (onay işareti sembolü) seçin.
1. Giden hazırlama konumunda yerine koyma görevi yönergelerini onaylayın.
1. **Tamam**'ı seçin.

    Bir "İş Tamamlandı" iletisi alırsınız.

Bağlantılı olduğu stok yenileme görevi tamamlanmadığı için satış siparişi 2, malzeme çekmeye karşı engellenmiştir. Şu anda malzeme çekme konumunda hala 30 beher miktarı bulunmaktadır ve satış siparişi 2 için stok yenileme miktarı 60 beherdir. Eldeki stok ve stok yenileme stoku toplamı (90 beher), 0,65 PL (veya 65 beher) olan taşma miktarını aşıyor. Stok yenileme işinin tamamlanabilmesi için önce satış siparişi 3'ün çekilmesi gerekir.

1. Satış siparişi 3'ün iş kodunu girin.

    Bu iş kodu için yalnızca bir malzeme çekme görevi vardır.

1. **Tamam**'ı seçin.

    **Satış siparişleri: Malzeme çekme** görevi sayfası, kalem numarası, miktar ve malzeme çekilecek konumu gösterir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.

    Belirttiğiniz plaka, stok yenileme işi görevlerinden alınan sistem tarafından oluşturulan plakalardan biridir. Doğru plaka kodunu aldığınızdan emin olmak için kalem, konum ve miktar açısından **Eldeki stok listesi** sayfasındaki stoku kontrol edin.

1. **Tamam** düğmesini (onay işareti sembolü) seçin.
1. Giden hazırlama konumunda yerine koyma görevi yönergelerini onaylayın.
1. **Tamam**'ı seçin.

    Bir "İş Tamamlandı" iletisi alırsınız.

Malzeme çekme konumundaki eldeki stok miktarı ve stok yenileme miktarının toplamı eşiğin altında olduğunda, kalan stok yenileme işini işleyebilirsiniz.

**İş ayrıntıları** sayfasına geri dönün ve konumda stok yenilemeyi kabul edecek kadar yeterli alan olmadığından nihai stok yenileme kısmının (satış siparişi 2 için) stok yenileme işi kullanılabilirliğinin *Açık* olduğuna dikkat edin.

Şimdi mobil cihaz üzerinden bu stok yenileme işini işleyebilirsiniz.

1. **Stok \> Stok yenileme**'ye gidin.

    Kalan stok yenileme işlemini tamamlamanız istenir. Kalem numarası, miktar ve malzeme çekme konumu gösterilir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.
1. **Tamam** düğmesini (onay işareti sembolü) seçin.

    Sistem, çekilen kalemin yeni plakaso için bir hedef plaka numarası oluşturur.

1. Değeri onaylamak için **Tamam**'ı seçin.

    Kullanıcıya hedef plakayı stok yenileme konumuna koymasını bildiren yerine koyma işi gösterilir. *Yerine koyma* konumu **06A01R2S1B** olmalıdır.

1. Yerine koyma ayrıntılarını onaylayın ve **Tamam**'ı seçin.

    "İş Tamamlandı" ve "Kullanılabilir İş Yok" iletilerini alırsınız.

Şimdi satış siparişi 2'yi çekebilirsiniz. Satış siparişiyle bağlantılı stok yenileme işi tamamlandığında, engeli kaldırılmıştır.

1. Satış siparişi 2'nin iş kodunu girin.

    Bu iş kodu için yalnızca bir malzeme çekme görevi vardır.

1. **Tamam**'ı seçin.

    **Satış siparişleri: Malzeme çekme** görevi sayfası, kalem numarası, miktar ve malzeme çekilecek konumu gösterir.

1. **LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.

    Belirttiğiniz plaka, stok yenileme işi görevinden alınan sistem tarafından oluşturulan bir plakadır. Doğru plaka kodunu aldığınızdan emin olmak için kalem, konum ve miktar açısından **Eldeki stok listesi** sayfasındaki stoku kontrol edin.

1. **Tamam** düğmesini (onay işareti sembolü) seçin.
1. Giden hazırlama konumunda yerine koyma görevi yönergelerini onaylayın.
1. **Tamam**'ı seçin.

    Bir "İş Tamamlandı" iletisi alırsınız.

## <a name="notes-and-tips"></a>Notlar ve ipuçları

- Bu işlev, tüm stok yenileme türleriyle çalışır: dalga talebi, minimum/maksimum, yükleme talebi ve eğri yerleştirme.
- Dilerseniz **İş ayrıntıları** sayfasından, her iş başlığı için stok yenileme işi kullanılabilirliğini el ile geçersiz kılabilirsiniz.
- Sistem stok yenileme işi kullanılabilirliğini ayarladığında, herhangi bir iş tamamlanmadan önce o konumda olan tüm stoku dikkate alır
- Satış siparişi işinin her parçası belirli bir stok yenileme işine bağlıdır. Karşılık gelen satış işi kullanılabilirlik işlevi yoktur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]