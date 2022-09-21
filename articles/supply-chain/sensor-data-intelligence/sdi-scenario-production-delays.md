---
title: Üretim gecikmeleri senaryosu
description: Bu makalede, üretim iş çıkarma yeteneği belirli bir eşik değerin altına düşerse bir bildirim oluşturan üretim gecikmeleri senaryosu açıklanmaktadır.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 073762581d84646ba12b570e57327b7cab8efd3b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428417"
---
# <a name="the-production-delays-scenario"></a>Üretim gecikmeleri senaryosu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Üretim iş çıkarma yeteneği belirli bir eşik değerinin altına düşerse *üretim gecikmeleri* senaryosu bir bildirim oluşturur. Bu senaryoda, üretilen her madde için Microsoft Azure IoT Hub'a bir *part-out* sinyali gönderilir. Dynamics 365 Supply Chain Management içinde, sipariş gecikmesi üretim emrinin çalışmak üzere zamanlandığı zaman miktarına, üretilmesi gereken maddelerin sayısına, işin çalıştığı sürenin miktarına ve teslim alınan *part-out* sinyallerin sayısına bağlı olarak hesaplanır. İş için *part-out* sinyallerinin sayısı beklenen eşik değerinin altına düşerse bir gecikme bildirimi oluşturulur.

## <a name="scenario-dependencies"></a>Senaryo bağımlılıkları

*Üretim gecikmeleri* senaryosu, aşağıdaki bağımlılıklara sahiptir:

- Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.
- Eşlenmiş bir makinenin *part-out* sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir ve benzersiz bir ad eklenmelidir.
- Değerin milisaniye (MS) olarak ifade edildiği bir UNIX zaman damgası özelliği, Azure IoT Hub iletisinde bulunmalıdır.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Ürün gecikmeleri senaryosu için demo verileri hazırlama

*Üretim gecikmeleri* senaryosunu test etmek için bir demo sistemi kullanmak istiyorsanız demo verilerinin yüklü olduğu bir sistem kullanın, *USMF* tüzel kişiliğini (şirket) seçin ve ek [demo verilerini](../../fin-ops-core/fin-ops/get-started/demo-data.md) bu bölümde açıklandığı gibi hazırlayın. Kendi sensörlerinizi ve verilerinizi kullanıyorsanız bu bölümü atlayabilirsiniz.

### <a name="set-up-sensor-simulator"></a>Sensör simülatörünü ayarlama

Fiziksel bir sensör kullanmadan bu senaryoyu denemek istiyorsanız gerekli sinyalleri üretmek için bir simülatör ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Test için simülasyonu yapılmış bir sensör ayarlama](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>P0111 ürünü için kaynak 3118'in kullanıldığını doğrulama

Bir üretim emri zamanlanır ve serbest bırakılır. Bu nedenle, bir üretim işi kaynak *3118*'e (*Köpük kesme makinesi*) serbest bırakılır. Demo verilerinizdeki *P0111* ürünü için kaynak *3118*'in kullanıldığını doğrulamak için aşağıdaki adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Madde numarası** alanının *P0111* olarak ayarlandığı ürünü bulup seçin.
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

## <a name="set-up-the-production-delays-scenario"></a>Üretim gecikmeleri senaryosunu ayarlama

Supply Chain Management'ta *üretim gecikmeleri* senaryosunu ayarlamak için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Senaryoları**'a gidin.
1. **Üretim gecikmeleri** senaryosu kutusunda, bu senaryonun kurulum sihirbazını açmak için **Yapılandır**'ı seçin.
1. **Sensörler** sayfasında, ızgaraya sensör eklemek için **Yeni**'yi seçin. Ardından bunun için aşağıdaki alanları ayarlayın:

    - **Sensör Kimliği**: Kullandığınız sensörün kimliğini girin. (Raspberry PI Azure IoT Online Simulator kullanıyorsanız ve bunu [Test için sanal algılayıcı ayarlama](sdi-set-up-simulated-sensor.md) bölümünde açıklandığı gibi ayarladıysanız *ProductionDelay* girin.)
    - **Sensör açıklaması**: Sensörle ilgili açıklama girin.

1. Şimdi eklemek istediğiniz diğer tüm sütunlar için önceki adımı yineleyin. İstediğiniz zaman geri dönüp daha fazla sensör ekleyebilirsiniz.
1. **Sonraki**'yi seçin.
1. **İşletme kaydı eşleme** sayfasında, **Sensörler** bölümünde, yeni eklediğiniz sensörlerden birinin kaydını seçin.
1. **İşletme kaydı eşlemesi** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **İş kaydı**'nı, izlemek için seçilen sensörü kullandığınız kaynağa ayarlayın. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız *3118, Köpük kesme makinesi* olarak ayarlayın.)
1. **Sonraki**'yi seçin.
1. **Üretim gecikmesi sapma eşiği** sayfasında, bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız şu adımları izleyin:

    1. Sütun için arama filtreleri içeren bir açılır iletişim kutusu açmak için **Madde ilişkisi** sütun başlığını seçin. Arama kutusuna *P0111* yazın ve ardından **Uygula**'yı seçin.
    2. **İşlem** alanının *Kırp/Kes* olarak ayarlandığı satırı seçin. **Gecikme için bildirim eşiği (%** ) alanını, bildirimin gönderilmesi gereken eşiğe (yüzde olarak) ayarlayın.

1. **Sonraki**'yi seçin.
1. **Sensörleri etkinleştirin** sayfasında, ızgarada, eklediğiniz sensörü seçin ve ardından **Etkinleştir**'i seçin. Izgaradaki her etkinleştirilen sensör için **Etkin** sütununda bir onay işareti görünür.
1. **Bitir**'i seçin.

## <a name="work-with-the-production-delays-scenario"></a>Üretim gecikmeleri senaryosuyla çalışma

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Kaynak durumu sayfasında üretim gecikmesi verilerini görüntüleme

**Kaynak durumu** sayfasında, süpervizörler her makine kaynağıyla eşlenen sensörlerden alınan sinyallerin zaman çizelgesini izleyebilir. Zaman çizelgesini yapılandırmak için şu adımları izleyin.

1. **Üretim denetimi \> Üretim yürütme \> Kaynak durumu**'na gidin.
1. **Yapılandır** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Kaynak**: İzlemek istediğiniz kaynakları seçin. (Demo verileriyle çalışıyorsanız *3118*'i seçin.)
    - **Zaman serisi 1**: Adı için aşağıdaki biçime sahip kaydı (metrik anahtarı) seçin: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Görünen ad**: *Parça çıkış sinyali* girin.
