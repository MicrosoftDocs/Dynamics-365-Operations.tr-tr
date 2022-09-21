---
title: Ürün kalitesi senaryosu
description: Bu makale, ürün kalitesi senaryosu hakkında bilgi sağlamaktadır. Bu senaryo, bir ürün grubunun kalitesini ölçmek için bir sensör kullanır ve bir ölçüm tanımlanmış bir eşiğin dışına düşerse bir uyarı oluşturur.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 8c4808ea3a0389c2a8699f0e11ea154705a6916d
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428430"
---
# <a name="the-product-quality-scenario"></a>Ürün kalitesi senaryosu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Ürün kalitesi* senaryosunda, üretim bölümündeki bir ürün partisinin kalitesini ölçmek için bir sensör ayarlanır. Bir ölçüm ürün için tanımlanmış bir eşiğin dışına düşerse süpervizörün kontrol panelinde bir bildirim gösterilir. Örneğin, bir sensör üretim hattından çıkan bir gıda ürününün nemini ölçüyor. Ölçüm, ürün için izin verilen minimum veya maksimum nem değerinin dışındaysa bir bildirim oluşturulur.

## <a name="scenario-dependencies"></a>Senaryo bağımlılıkları

*Ürün kalitesi* senaryosu, aşağıdaki bağımlılıklara sahiptir:

- Uyarının tetiklenebilmesi için bir üretim emrinin eşlenmiş bir makinede çalışması ve bu makinenin eşlenen toplu iş özniteliğe sahip bir ürün üretmesi gerekir.
- Toplu iş özniteliğini temsil eden bir sinyal IoT Hub'a gönderilmelidir ve benzersiz özellik adı eklenmelidir.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Ürün kalitesi senaryosu için demo verileri hazırlama

*Ürün kalitesi* senaryosunu test etmek için bir demo sistemi kullanmak istiyorsanız demo verilerinin yüklü olduğu bir sistem kullanın, *USMF* tüzel kişiliğini (şirket) seçin ve ek [demo verilerini](../../fin-ops-core/fin-ops/get-started/demo-data.md) bu bölümde açıklandığı gibi hazırlayın. Kendi sensörlerinizi ve verilerinizi kullanıyorsanız bu bölümü atlayabilirsiniz.

Bu bölümde, serbest bırakılan *P0111* (*Kompozit Kasa*) ürününü *ürün kalitesi* senaryosuyla kullanabilmeniz için demo verilerini ayarlayacaksınız. Bu senaryoda, sistem bir algılayıcı tarafından ölçülen bir toplu iş özniteliği değerinin, ürünle ilişkili bir toplu iş özniteliği için tanımlanan eşiğin dışında olup olmadığını izler.

### <a name="set-up-a-sensor-simulator"></a>Sensör simülatörü ayarlama

Fiziksel bir sensör kullanmadan bu senaryoyu denemek istiyorsanız gerekli sinyalleri üretmek için bir simülatör ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Test için simülasyonu yapılmış bir sensör ayarlama](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Toplu iş özniteliğini ve kaynağını P0111 ürünüyle ilişkilendirme

Bir toplu iş özniteliğini *P0111* (*Kompozit Kasa*) ürünüyle ilişkilendirmek ve bunun için kaynak *3118*'in (*Köpük kesme makinesi*) kullanıldığını doğrulamak için aşağıdaki adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Madde numarası** alanının *P0111* olarak ayarlandığı ürünü bulup seçin.
1. Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Toplu öznitelikler** grubunda, **Ürüne özel**'i seçin.
1. **Ürüne özel** sayfasında, ürüne özgü toplu iş özniteliği oluşturmak için **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki alanları ayarlayın:

    - **Öznitelik kodu**: İzleyeceğiniz özniteliklerin kapsamını seçin (*Tablo*, *Grup* veya *Tümü*). Bu senaryoda, her zaman tek bir özniteliği izleyeceğiniz için *Tablo*'yu seçin.
    - **Öznitelik ilişkisi**: Değerini izlemek için *ürün kalitesi* senaryosunu kullanacağınız özniteliği seçin. Bu örnekte, standart demo verilerine dahil edilen bir öznitelik olan *Konsantrasyon*'u seçin.

1. **Değerler** hızlı sekmesinde, **Minimum** ve **Maksimum** alanlarında, özniteliğin kalite denetimini geçmek için raporlaması gereken kabul edilebilir değerler aralığını tanımlayın. Sensör bu aralığın dışında bir değer bildirirse sistem bunu kalite ihlali olarak tanımlayacaktır. Bu hızlı sekmedeki diğer alanlar *ürün kalitesi* senaryosuyla ilgili değildir. Şu anda gördüğünüz varsayılan değerler demo verilerinden gelir. Bu nedenle, bunları oldukları gibi bırakın ve *P0111* ürününün **Serbest bırakılan ürün ayrıntıları** sayfasına dönmek için **Ürüne özel** sayfasını kapatın.
1. Eylem Bölmesinde, **Mühendis** sekmesindeki **Görünüm** gurubunda **Rota**'yı seçin.
1. **Rota** sayfasında, sayfanın altındaki **Genel Bakış** sekmesinde, **Oper'in bulunduğu satırı seçin. No.** alanı *30* olarak ayarlanır.
1. Sayfanın altındaki **Kaynak gereksinimleri** sekmesinde, kaynak *3118*'in (*Köpük kesme makinesi*) işlemle ilişkili olduğundan emin olun.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>P0111 ürünü için üretim emri oluşturma ve serbest bırakma

*P0111* ürünü için bir üretim emri oluşturmak ve serbest bırakmak üzere aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Üretim emirleri \> Tüm üretim emirleri**'ne gidin.
1. **Tüm üretim emirleri** sayfasında, Eylem Bölmesinde, **Yeni toplu iş emri**'ni seçin.
1. **Toplu iş oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *P0111*
    - **Miktar:** *10*

1. Emri oluşturmak ve **Tüm üretim emirleri** sayfasına dönmek için **Oluştur**'u seçin.
1. **Madde numarası** alanının *P0111* olarak ayarlandığı üretim emirlerini aramak için **Filtre** alanını kullanın. Ardından, yeni oluşturduğunuz üretim emrini bulun ve seçin.
1. Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Tahmin**'i seçin.
1. **Tahmin** iletişim kutusunda, tahmini başlatmak için **Tamam** 'ı seçin.
1. Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Serbest Bırak**'ı seçin.
1. **Serbest bırakma** iletişim kutusunda, yeni oluşturduğunuz toplu iş emrinin numarasını not edin.
1. Emri serbest bırakmak için **Tamam**'ı seçin.

### <a name="configure-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini yapılandırma

Henüz yapmadıysanız üretim katı yürütme arabirimini kaynak *3118*'e (*Köpük kesme makinesi*) atanan işleri gösterecek şekilde yapılandırın. Talimatlar için aşağıdaki bölümlere bakın:

- [Üretim katı yürütme arabirimini yapılandırma](sdi-scenario-equipment-downtime.md#config-pfe)
- [Üretim katı yürütme arabiriminde arama seçeneğini etkinleştirme](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Toplu iş emrindeki ilk işi başlatma

Toplu iş emrindeki ilk işi başlatmak için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Üretim yürütme \> Üretim katı yürütmesi**'ne gidin.
1. **Rozet kimliği** alanına *123* girin. Ardından **Oturum aç**'ı seçin.
1. Devamsızlık nedeni sorulursa devamsızlık için kartlardan birini seçin ve ardından **Tamam**'ı seçin.
1. **Arama** alanına, daha önce not ettiğiniz toplu iş emri numarasını girin. Ardından **Return** tuşunu seçin.
1. Siparişi seçin ve ardından **İşi başlat**'ı seçin.
1. **İşi başlat** iletişim kutusunda **Başlat**'ı seçin.

## <a name="set-up-the-product-quality-scenario"></a>Ürün kalitesi senaryosunu ayarlama

Supply Chain Management'ta *ürün kalitesi* senaryosunu ayarlamak için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Senaryoları**'a gidin.
1. **Ürün kalitesi** senaryosu kutusunda, bu senaryonun kurulum sihirbazını açmak için **Yapılandır**'ı seçin.
1. **Sensörler** sayfasında, ızgaraya sensör eklemek için **Yeni**'yi seçin. Ardından bunun için aşağıdaki alanları ayarlayın:

    - **Sensör Kimliği**: Kullandığınız sensörün kimliğini girin. (Raspberry PI Azure IoT Online Simulator'ı kullanıyorsanız ve bunu [test için sanal sensör ayarlama](sdi-set-up-simulated-sensor.md) bölümünde açıklandığı gibi ayarladıysanız *Kalite* girin.)
    - **Sensör açıklaması**: Sensörle ilgili açıklama girin.

1. Şimdi eklemek istediğiniz diğer tüm sütunlar için önceki adımı yineleyin. İstediğiniz zaman geri dönüp daha fazla sensör ekleyebilirsiniz.
1. **Sonraki**'yi seçin.
1. **İşletme kaydı eşleme** sayfasında, **Sensörler** bölümünde, yeni eklediğiniz sensörlerden birinin kaydını seçin.
1. **İşletme kaydı eşlemesi** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **İşletme kaydı türü** alanı otomatik olarak *Kaynaklar(WrkCtrTable)* olarak ayarlanmalıdır. **İşletme kaydı** alanını, izlemek için seçilen sensörü kullandığınız kaynağa ayarlayın. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız *3118, Köpük kesme makinesi* olarak ayarlayın.)
1. Önceki adımda eklediğiniz satır için bir iş kaydı türü seçtikten hemen sonra, kılavuza otomatik olarak ikinci bir satır eklenir. Bu satırda, **İşletme kaydı türü** alanı *Toplu iş öznitelikleri(PdsBatchAttrib)* olarak ayarlanmalıdır. **İşletme kaydı** alanını, izlemek için seçilen sensörü kullandığınız toplu iş özniteliğine ayarlayın. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız bunu *Konsantrasyon, Konsantrasyon Yüzdesi* olarak ayarlayın.)
1. **Sonraki**'yi seçin.
1. **Sensörleri etkinleştirin** sayfasında, ızgarada, eklediğiniz sensörü seçin ve ardından **Etkinleştir**'i seçin. Izgaradaki her etkinleştirilen sensör için **Etkin** sütununda bir onay işareti görünür.
1. **Bitir**'i seçin.

## <a name="work-with-the-product-quality-scenario"></a>Ürün kalitesi senaryosuyla çalışma

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Kaynak durumu sayfasında ürün kalitesi verilerini görüntüleme

**Kaynak durumu** sayfasında, süpervizörler her makine kaynağıyla eşlenen sensörlerden alınan ürün kalitesi sinyalinin zaman çizelgesini izleyebilir. Zaman çizelgesini yapılandırmak için şu adımları izleyin.

1. **Üretim denetimi \> Üretim yürütme \> Kaynak durumu**'na gidin.
1. **Yapılandır** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Kaynak**: İzlemek istediğiniz kaynakları seçin. (Demo verileriyle çalışıyorsanız *3118*'i seçin.)
    - **Zaman serisi 1**: Adı için aşağıdaki biçime sahip kaydı (ölçüm anahtarı) seçin: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Görünen ad**: *Toplu iş öznitelik değerlerini* girin.

Aşağıdaki çizimde, değer kabul edilebilir değerler aralığında olduğunda **Kaynak durumu** sayfasındaki ürün kalitesi verilerine bir örnek gösterilmektedir.

![Değer aralık içinde olduğunda Kaynak durumu sayfasındaki ürün kalitesi verileri.](media/sdi-product-quality-in-range.png "Değer aralık içinde olduğunda Kaynak durumu sayfasındaki ürün kalitesi verileri")

Aşağıdaki çizimde, aralık dışı bir değer algılandığında ürün kalitesi verilerine bir örnek gösterilmektedir.

![Aralık dışı bir değer algılandığında Kaynak durumu sayfasındaki ürün kalitesi verileri.](media/sdi-product-quality-out-of-range.png "Aralık dışı bir değer algılandığında Kaynak durumu sayfasındaki ürün kalitesi verileri")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Ürün kalitesi verilerini Bildirimler sayfasında görüntüleme

Süpervizörler, **Bildirimler** sayfasında, sensör toplu iş özniteliği için tanımlanan eşiğin dışında kalan bir toplu iş özniteliği değerini ölçtüğünde oluşturulan bildirimi görüntüleyebilir. Her bildirim, kesintiden etkilenen üretim işine genel bir bakış sağlar ve etkilenen işi başka bir kaynağa yeniden atama seçeneği sunar.

**Bildirim** sayfasını açmak için **Üretim denetimi \> Sorgular ve raporlar \> Sensör Veri Yönetim Bilgileri \> Bildirimler**'e gidin.

Aşağıdaki şekilde bir ürün kalitesi bildirimi örneği gösterilmiştir.

![Ürün kalitesi bildirimi örneği.](media/sdi-product-quality-notification.png "Ürün kalitesi bildirimi örneği")
