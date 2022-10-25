---
title: Makine durumu senaryosu
description: Bu makalede, ekipmanınızın kullanılabilirliğini izlemek için sensör verilerini kullanmanıza olanak tanıyan makine durumu senaryosu açıklanmaktadır.
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
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689652"
---
# <a name="the-machine-status-scenario"></a>Makine durumu senaryosu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

*Makine durumu* senaryosu, ekipmanınızın kullanılabilirliğini izlemek için sensör verilerini kullanmanıza olanak tanır. Bir makine kaynağındaki bir üretim işi çıktı ürettiğinde sinyal gönderen bir sensör ayarlarsanız ancak belirli bir aralıkta sensör sinyali alınmazsa süpervizörün panosunda bir bildirim gösterilir.

## <a name="scenario-dependencies"></a>Senaryo bağımlılıkları

*Makine durumu* senaryosu, aşağıdaki bağımlılıklara sahiptir:

- Bildirimin tetiklenmesi için eşlenmiş bir makinede üretim işi devam ediyor olmalıdır.
- *part-out* sinyalini temsil eden bir sinyalin IoT hub'ına gönderilmesi gerekir.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Makine durumu senaryosu için demo verileri hazırlama

*Makine durumu* senaryosunu test etmek için bir demo sistemi kullanmak istiyorsanız demo verilerinin yüklü olduğu bir sistem kullanın, *USMF* tüzel kişiliğini (şirket) seçin ve ek [demo verilerini](../../fin-ops-core/fin-ops/get-started/demo-data.md) bu bölümde açıklandığı gibi hazırlayın. Kendi sensörlerinizi ve verilerinizi kullanıyorsanız bu bölümü atlayabilirsiniz.

### <a name="set-up-a-sensor-simulator"></a>Sensör simülatörü ayarlama

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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Üretim katı yürütme arabirimini yapılandırma

Önceki bölümde *P0111* madde numarası için zamanlanan ve serbest bırakılan işi başlatmak için üretim katı yürütme arabirimini kullanacaksınız. Üretim katı yürütme arabirimini yapılandırmak için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Üretim yürütme \> Üretim katı yürütmesi**'ne gidin.
1. Arabirimi daha önce ayarlamadıysanız bir oturum açma sayfası görüntülenir. Kimlik bilgilerinizi girin.
1. Hoş geldiniz sayfasında, **Cihazı yapılandırın** sihirbazını açmak için **Yapılandır**'ı seçin.
1. **Cihazı yapılandırın - Adım 1 - Yapılandırma seçin** sayfasında, *Varsayılan* adlı yapılandırmayı seçin.
1. **Sonraki**'yi seçin.
1. **Cihazı yapılandırın - Adım 2 - Üretim katı alanını tanımlayın** sayfasında, **Kaynak** alanını *3118* olarak ayarlayın.
1. **Tamam**'ı seçin.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Üretim katı yürütme arabiriminde arama seçeneğini etkinleştirme

Daha önce serbest bırakılan bir üretim emrinin üretim işini bulmayı kolaylaştırmak için üretim katı yürütme arabiriminde arama seçeneğini etkinleştirmek üzere aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.
1. *Varsayılan* yapılandırmayı seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, **Aramayı dahil et** seçeneğini *Evet* olarak ayarlayın.
1. Sayfayı kapatın.

### <a name="start-the-first-job-in-the-batch-order"></a>Toplu iş emrindeki ilk işi başlatma

Kaynak *3118*'de zamanlanan işi başlatmak için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Üretim yürütme \> Üretim katı yürütmesi**'ne gidin.
1. **Rozet kimliği** alanına *123* girin. Ardından **Oturum aç**'ı seçin.
1. Devamsızlık nedeni sorulursa devamsızlık için kartlardan birini seçin ve ardından **Tamam**'ı seçin.
1. **Arama** alanına, daha önce not ettiğiniz toplu iş emri numarasını girin. Ardından **Return** tuşunu seçin.
1. Siparişi seçin ve ardından **İşi başlat**'ı seçin.
1. **İşi başlat** iletişim kutusunda **Başlat**'ı seçin.

## <a name="set-up-the-machine-status-scenario"></a>Makine durumu senaryosunu ayarlama

Supply Chain Management'ta *makine durumu* senaryosunu ayarlamak için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Senaryoları**'a gidin.
1. **Makine durumu** senaryosu kutusunda, bu senaryonun kurulum sihirbazını açmak için **Yapılandır**'ı seçin.
1. **Sensörler** sayfasında, ızgaraya sensör eklemek için **Yeni**'yi seçin. Ardından bunun için aşağıdaki alanları ayarlayın:

    - **Sensör Kimliği**: Kullandığınız sensörün kimliğini girin. (Raspberry PI Azure IoT Online Simulator'ı kullanıyorsanız ve bunu [Test için sanal sensör ayarlama](sdi-set-up-simulated-sensor.md) bölümünde açıklandığı gibi ayarladıysanız *MachineStatus* girin.)
    - **Sensör açıklaması**: Sensörle ilgili açıklama girin.

1. Şimdi eklemek istediğiniz diğer tüm sütunlar için önceki adımı yineleyin. İstediğiniz zaman geri dönüp daha fazla sensör ekleyebilirsiniz.
1. **Sonraki**'yi seçin.
1. **İşletme kaydı eşleme** sayfasında, **Sensörler** bölümünde, yeni eklediğiniz sensörlerden birinin kaydını seçin.
1. **İşletme kaydı eşlemesi** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **İşletme kaydı** alanını, izlemek için seçilen sensörü kullandığınız kaynağa ayarlayın. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız alanı *3118, Köpük kesme makinesi* olarak ayarlayın.)
1. **Sonraki**'yi seçin.
1. **Makine durumu eşiği** sayfasında, sistemin son *part-out* sinyalinden ne kadar süre sonra makine durumu bildirimi göndermesi gerektiğini tanımlayın. Eşiği tanımlamanın iki yolu vardır:

    - **Varsayılan eşik (dakika)**: Varsayılan eşiği tanımlamak için bu alanı ayarlayın. Değer daha sonra **Makinenin yanıt vermediğini belirleme eşiği (dakika)** alanının iki dakika veya daha kısa bir süreye ayarlandığı tüm kaynaklara uygulanır. Minimum değer *2* (dakika) şeklindedir.
    - **Makinenin yanıt vermediğini belirleme eşiği (dakika)**: Kılavuzdaki varsayılan eşiği kullanmak istemediğiniz her kaynak için bu alana bir geçersiz kılma değeri girin. İki dakika veya daha kısa bir eşik kullanacak şekilde ayarlanan kaynaklar, bunun yerine **Varsayılan eşik (dakika)** ayarını kullanır.

    > [!NOTE]
    > Genelde, makine durumunu izlemek için bir *part-out* sinyali kullanırsınız. Bu nedenle, her makine kaynağının eşiğinin, makinenin her parçayı üretmek için gereksinim duyduğundan daha uzun olduğunu doğrulamanız gerekir.

1. **Sonraki**'yi seçin.
1. **Sensörleri etkinleştirin** sayfasında, ızgarada, eklediğiniz sensörü seçin ve ardından **Etkinleştir**'i seçin. Izgaradaki her etkinleştirilen sensör için **Etkin** sütununda bir onay işareti görünür.
1. **Bitir**'i seçin.

## <a name="work-with-the-machine-status-scenario"></a>Makine durumu senaryosuyla çalışma

Sensörlerinizi taktıktan ve senaryoyu yapılandırdıktan sonra, makine durumu olaylarını Supply Chain Management'ta görüntüleyebilirsiniz. Bu bölümde, bu bilgilerin nerede ve nasıl görüntüleneceği açıklanmaktadır.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Kaynak durumu sayfasında makine durumu verilerini görüntüleme

**Kaynak durumu** sayfasında, süpervizörler her makine kaynağıyla eşlenen sensörlerden alınan *part-out* sinyalinin zaman çizelgesini izleyebilir. Zaman çizelgesini yapılandırmak için şu adımları izleyin.

1. **Üretim denetimi \> Üretim yürütme \> Kaynak durumu**'na gidin.
1. **Yapılandır** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Kaynak**: İzlemek istediğiniz kaynakları seçin. (Demo verileriyle çalışıyorsanız *3118*'i seçin.)
    - **Zaman serisi 1**: Adı için aşağıdaki biçime sahip kaydı (metrik anahtarı) seçin: *MachineReportingStatus&lt;Sensor&gt;*
    - **Görünen ad**: *Parça çıkış sinyali* girin.

Aşağıdaki çizimde, standart çalışma sırasında **Kaynak durumu** sayfasındaki makine durumu verilerinin bir örneği gösterilmektedir.

![Standart çalışma sırasında Kaynak durumu sayfasındaki makine durumu verileri.](media/sdi-resource-status-downtime-up.png "Standart işlem sırasında Kaynak durumu sayfasındaki makine durumu verileri")

Aşağıdaki çizimde, kapalı kalma süresi algılandığında makine durumu verilerine bir örnek gösterilmektedir.

![Kapalı kalma süresi algılandığında Kaynak durumu sayfasındaki makine durumu verileri.](media/sdi-resource-status-downtime-down.png "Kesinti algılandığında Kaynak durumu sayfasındaki makine durumu verileri")

### <a name="view-machine-status-on-the-notifications-page"></a>Bildirimler sayfasında makine durumunu görüntüleme

Süpervizörler, **Bildirimler** sayfasında, sensörün en son *part-out* sinyali vermesinden bu yana çok fazla zaman geçtiğinde oluşturulan bildirimleri görüntüleyebilir. Her bildirim, kesintiden etkilenen üretim işine genel bir bakış sağlar ve etkilenen işi başka bir kaynağa yeniden atama seçeneği sunar.

**Bildirim** sayfasını açmak için **Üretim denetimi \> Sorgular ve raporlar \> Sensör Veri Yönetim Bilgileri \> Bildirimler**'e gidin.

Aşağıdaki şekilde, bir makine durumu bildirimi örneği gösterilmiştir.

![Makine durumu bildirimi örneği.](media/sdi-resource-status-downtime-notification.png "Makine durumu bildirimi örneği")
