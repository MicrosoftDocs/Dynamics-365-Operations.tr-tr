---
title: Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?
description: Bu konu, bir çalışanın bakış açısından üretim katı yürütme arabiriminin nasıl kullanılacağını açıklar.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 38bc07d37b5c51f143846110c87cff9952d52b0e
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500802"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Üretim katı yürütme arabirimi dokunma etkileşimi için en iyi duruma getirilmiştir. Tasarımı, atölye ortamları için erişilebilirlik gereksinimlerini karşılayan görsel bir kontrast sağlar. İş kartı cihazı ile aynı işlevsel tüm yetenekleri sunar. Ancak, bir iş listesinden paralel olarak birden fazla işin başlatılmasına olanak tanır. (Bu yetenek *iş gruplama* olarak da bilinir.) Ek olarak, bir iş listesinden, çalışanlar Microsoft Dynamics 365 kılavuzunda oluşturulmuş bir Kılavuzu açabilir. Böylece, bir HoloLens üzerinde görsel yönergeler elde edebilirler.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Çalışan olarak üretim katı yürütme arabiriminde nasıl oturum açılır?

Çalışanlar cihazı kullanmaya başlamadan önce, bir gözetmen veya teknik personelin bunu hazırlaması ve Dynamics 365 Supply Chain Management'ta doğru sayfayı açması gerekir. Cihazı ayarlama hakkında daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini çalıştırmak için cihazı ayarlama](production-floor-execution-setup.md).

Cihaz hazırlandıktan sonra, üzerinde oturum açma sayfası görüntülenir. Bu sayfa, yerel iş hücresi işlerinin durumu hakkında bilgi gösterir. Bu bilgiler periyodik olarak güncelleştirilir. Sayfada, çalışanlar oturum açmak için kendi rozet kimliklerini kullanırlar. Çalışanların Supply Chain Management için bir kullanıcı hesabına sahip olmaları gerekmemesine rağmen, kullanıcıların oturum açarken kullanabileceği *saatine kayıtlı çalışan* hesabı olmalıdır.

![Üretim katı yürütme arabirimi oturum açma sayfası](media/pfei-sign-in-page.png "Üretim katı yürütme arabirimi oturum açma sayfası")

Bu konunun geri kalan bölümleri, çalışanların arabirimle nasıl etkileştiğini açıklamaktadır.

## <a name="all-jobs-tab"></a>Tüm işler sekmesi

**Tüm işler** sekmesi, durumu *başlatılmadı*, *durduruldu* veya *Başlatıldı* olan tüm üretim işlerini gösteren bir iş listesi sağlar. (Bu sekme adı özelleştirilebilir ve sisteminiz için farklı olabilir.)

![Tüm işler sekmesi](media/pfei-all-jobs-tab.png "Tüm işler sekmesi")

İş listesinde aşağıdaki sütunlar vardır. Sayılar, önceki görseldeki sayılara karşılık gelir.

1. **Seçim sütunu**: En soldaki sütun, çalışan tarafından seçilmiş olan işleri belirtmek için onay işareti kullanır. Çalışanlar, aynı anda listedeki birden fazla işi seçebilir. Listedeki tüm işleri seçmek için, sütun başlığındaki onay işaretini seçin. Tek bir iş seçildiğinde, o işle ilgili ayrıntılar sayfanın alt bölümünde gösterilir.
1. **İş durumu sütunu**: Bu sütun, her projenin durumunu belirtmek için semboller kullanır. Bu sütunda simge içermeyen işler *başlatılmadı* durumundadır. Yeşil üçgen, durumu *başlatıldı* olan işleri belirtir. İki sarı dikey çizgi, durumu *durdurulmuş* olan işleri gösterir.
1. **Yüksek öncelik sütunu**: Bu sütun, yüksek önceliğe sahip işleri göstermek için ünlem işaretleri kullanır.
1. **Sipariş**: Bu sütun bir projeyle ilgili üretim emri numarasını gösterir.
1. **Açıklama**: Bu sütunda bir projenin ait olduğu operasyonun açıklaması gösterilir.
1. **Gerekli**: Bu sütunda bir işin üretilmesi için planlanan miktar gösterilir.
1. **Başlatıldı**: Bu sütunda, bir proje için zaten başlatılmış olan miktar gösterilir.
1. **Tamamlandı**: Bu sütunda, bir proje için zaten tamamlanmış olan miktar gösterilir.
1. **Hurdaya çıkarıldı**: Bu sütunda, bir proje için zaten hurdaya çıkarılmış olan miktar gösterilir.
1. **Geri kalan**: Bu sütunda bir proje için tamamlanmak üzere kalan miktar gösterilir.

## <a name="active-jobs-tab"></a>Etkin işler sekmesi

**Etkin işler** sekmesi, oturum açan çalışanın önceden başlattığı tüm işlerin listesini gösterir. (Bu sekme adı özelleştirilebilir ve sisteminiz için farklı olabilir.)

![Etkin işler sekmesi](media/pfei-active-jobs-tab.png "Etkin işler sekmesi")

Etkin işler aşağıdaki sütunlar vardır:

- **Seçim sütunu**: En soldaki sütun, çalışan tarafından seçilmiş olan işleri belirtmek için onay işareti kullanır. Çalışanlar, aynı anda listedeki birden fazla işi seçebilir. Listedeki tüm işleri seçmek için, sütun başlığındaki onay işaretini seçin. Tek bir iş seçildiğinde, o işle ilgili ayrıntılar sayfanın alt bölümünde gösterilir.
- **Sipariş**: Bu sütun bir projeyle ilgili üretim emri numarasını gösterir.
- **Açıklama**: Bu sütunda bir projenin ait olduğu operasyonun açıklaması gösterilir.
- **Gerekli**: Bu sütunda bir işin üretilmesi için planlanan miktar gösterilir.
- **Başlatıldı**: Bu sütunda, bir proje için zaten başlatılmış olan miktar gösterilir.
- **Tamamlandı**: Bu sütunda, bir proje için zaten tamamlanmış olan miktar gösterilir.
- **Hurdaya çıkarıldı**: Bu sütunda, bir proje için zaten hurdaya çıkarılmış olan miktar gösterilir.
- **Geri kalan**: Bu sütunda bir proje için tamamlanmak üzere kalan miktar gösterilir.

## <a name="my-machine-tab"></a>Makinem sekmesi

**Makinem** sekmesi, çalışanların **Tüm işler** sekmesinde ayarlanan filtre dahilindeki makine kaynağına bağlı olan kıymeti seçmesine olanak tanır. Çalışan, en fazla dört seçili sayacın değerlerini ve en son bakım istekleri ve kaydedilmiş kesinti süreleri listelerini okuyarak seçili kıymetin durumunu ve sistem durumunu görüntüleyebilir. Çalışan aynı zamanda seçili kıymet için bakım isteyebilir ve makine kesinti süresini kaydedebilir ve düzenleyebilir. (Bu sekme adı özelleştirilebilir ve sisteminiz için farklı olabilir.)
 
![Makinem sekmesi](media/pfei-my-machine-tab.png "Makinem sekmesi")

**Makinem** sekmesi aşağıdaki sütunlara sahiptir. Sayılar, önceki görseldeki sayılara karşılık gelir.

1. **Makine kıymeti**: İzlemek istediğiniz makine kıymetini seçin. Eşleşen kıymetler listesinden seçim yapmak için bir ad yazmaya başlayın veya iş listesi filtresi dahilindeki kaynaklarla ilişkilendirilmiş tüm kıymetlerin listesinden seçim yapmak için büyüteç simgesini seçin.

    > [!NOTE]
    > Supply Chain Management kullanıcıları, **Tüm kıymetler** sayfasını kullanarak gerektiğinde her kıymete bir kaynak atayabilir (**Sabit kıymet** sekmesindeki **Kaynak** açılır listesini kullanarak). Daha fazla bilgi için bkz. [Kıymet oluşturma](../asset-management/objects/create-an-object.md).

1. **Ayarlar**: Seçili makine kıymeti için görüntülenecek sayaçları seçebileceğiniz bir iletişim kutusu açmak için dişli simgesini seçin. Bu sayaçların değerleri, **Kıymet yönetimi** sekmesinin en üstünde gösterilir. **Ayarlar** menüsü (aşağıdaki ekran görüntüsünde gösterilmektedir) en çok dört sayacı etkinleştirmenize olanak tanır. Etkinleştirmek istediğiniz her sayaç için, kutucuğun üst tarafındaki arama alanını kullanarak bir sayaç seçin. Arama alanı, **Kıymet yönetimi** sayfasının en üstünde seçilen kıymetle ilişkilendirilmiş tüm sayaçları listeler. Sayaç için **Toplam** değeri veya en son **Gerçek** değeri izlemek için her sayacı ayarlayın. Örneğin, makinenin kaç saattir çalıştığını takip eden bir sayaç ayarlarsanız bunu **Toplam** olarak ayarlamanız gerekir. En son güncelleştirilen sıcaklığı veya basıncı ölçmek üzere bir sayaç ayarlarsanız, bunu **Gerçek** olacak şekilde ayarlamalısınız. Ayarlarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.

    ![Makinem sekmesi](media/pfei-my-machine-tab-settings.png "Makinem sekmesi")

1. **Bakım iste**: Bakım isteği oluşturabileceğiniz bir iletişim kutusu açmak için bu düğmeyi seçin. Açıklama ve bir not girebilirsiniz. Talep, bir Supply Chain Management kullanıcısına gösterilir ve bu kullanıcı bakım isteğini bakım iş emrine dönüştürebilir.
1. **Kesinti süresini kaydet**: Makinenin kesinti süresini kaydedebileceğiniz bir iletişim kutusu açmak için bu düğmeyi seçin. Bir neden kodu seçebilir ve kesinti süresi için bir tarih/saat aralığı girebilirsiniz. Makinenin kesinti süresi kaydı, makine kıymetinin verimliliğini hesaplamak için kullanılır.
1. **Görüntüle veya düzenle**: Mevcut kesinti süresi kayıtlarını düzenleyebileceğiniz veya görüntüleyebileceğiniz bir iletişim kutusu açmak için bu düğmeyi seçin.


## <a name="starting-and-completing-production-jobs"></a>Üretim işlerini başlatma ve tamamlama

Çalışanlar, **tüm işler** sekmesinde iş seçip **işi Başlat** iletişim kutusunu açmak için **işi Başlat**'ı seçerek bir üretim işi başlatır.

![İş başlatma iletişim kutusu](media/pfei-start-job-dialog.png "İş başlatma iletişim kutusu")

Çalışanlar üretim miktarını doğrulamak ve işi başlatmak için **İşi Başlat** iletişim kutusunu kullanırlar. Çalışanlar **miktar** alanını seçip beliren sayısal klavyeyi kullanarak miktarı ayarlayabilir. Ardından çalışanlar, iş üzerinde çalışmaya başlamak için **Başlat**'ı seçer. **İşi Başlat** iletişim kutusu kapatılır ve iş **etkin işler** sekmesine eklenir.

Çalışanlar herhangi bir durumda olan bir işi başlatabilir. Bir çalışan, durumu *başlatılmadı* olan bir işi başlattığında, **işi Başlat** iletişim kutusundaki **miktar** alanı, ilk olarak tüm miktarı gösterir. Bir çalışan, durumu *Başlatıldı* veya *Durduruldu* olan bir işi başlattığında, **Miktar** alanı, ilk olarak kalan miktarı gösterir.

## <a name="reporting-good-quantities"></a>Sağlam miktarlar raporlaması

Bir çalışan bir işi tamamladığında veya kısmen tamamladığında, **etkin işler** sekmesinde bir iş seçip sonra **İlerlemeyi Raporla**'yı seçerek üretilen sağlam miktarları rapor edebilir. Sonra, **İlerlemeyi Raporla** iletişim kutusunda, çalışan sayısal klavyeyi kullanarak sağlam miktarı girer. Varsayılan olarak miktar boştur. Bir miktar girildikten sonra, çalışan, işin durumunu *devam ediyor*, *Durduruldu* veya *tamamlandı* olarak güncelleştirebilir.

![İlerlemeyi raporla iletişim kutusu](media/pfei-report-progress-dialog.png "İlerlemeyi raporla iletişim kutusu")

## <a name="reporting-scrap"></a>Hurda raporlaması

Bir çalışan bir işi tamamladığında veya kısmen tamamladığında, **etkin işler** sekmesinde bir iş seçip sonra **Hurdayı Raporla**'yı seçerek hurdayı rapor edebilir. Sonra, **Hurdayı Raporla** iletişim kutusunda, çalışan sayısal klavyeyi kullanarak hurda miktarını girer. Çalışan ayrıca bir neden (*yok*, *makine*, *işleç* veya *malzeme*) seçer.

![Hurda raporla iletişim kutusu](media/pfei-report-scrap-dialog.png "Hurda raporla iletişim kutusu")

## <a name="completing-a-job-and-starting-a-new-job"></a>Bir iş tamamlama ve yeni bir proje başlatma

Çalışanlar **etkin işler** sekmesinde bir veya daha fazla geçerli işi seçerek ve ardından **İlerlemeyi raporla**'yı seçerek iş tamamlar. Daha sonra, üretilen miktarı (sağlam miktar) girip durumu *tamamlandı* olarak ayarlar. Birden fazla iş seçilmişse, bir çalışan bunlar arasında hareket etmek için **Önce** ve **Sonra** düğmelerini kullanır. Yeni bir iş başlatmak için, çalışan, **tüm işler** sekmesinde bunu seçer ve sonra **İşi başlat**'ı seçer.

Bir çalışan, önceki işler açıkken yeni bir iş de başlatabilir. Yine çalışan, **tüm işler** sekmesinde yeni işi seçer ve sonra **İşi başlat**'ı seçer. Ancak, bu durumda, **işi Başlat** iletişim kutusu, çalışana bir işte çalıştıkları ve dolayısıyla yeni işi başlatmadan önce o işi durdurması veya tamamlaması gerektiğini bildirir.

## <a name="working-on-multiple-jobs-in-parallel"></a>Paralel olarak çoklu işler üzerinde çalışma

Bir çalışan aynı anda çoklu işler üzerinde çalışabilir (paralel olarak). Bu durumda, çalışanın üzerinde çalıştığı işler koleksiyonuna *iş grubu* denir. Çalışan, gruba yeni işler ekleyebilir veya grupta bir veya daha fazla iş tamamlayabilir. Aşağıdaki iki senaryo, bir çalışanın paralel olarak işlerde nasıl çalışabileceğini göstermektedir.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Senaryo 1: Etkin işi olmayan bir çalışan, iki iş başlatmak ve bunlarda paralel olarak çalışmak istiyor

Çalışan, **tüm işler** sekmesinde iki işi seçer ve sonra **İşi başlat**'ı seçer. **İşi Başlat** iletişim kutusu her iki seçili işi de gösterir ve çalışan her bir işte başlaması için miktarı ayarlayabilir. Çalışan daha sonra iletişim kutusunu onaylar ve her iki işi de başlatabilir.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Senaryo 2: Sürmekte olan iki etkin işi olan bir çalışan, üçüncü bir iş başlatmak ve diğeri iki iş ile paralel çalışmak istiyor

Çalışan, **tüm işler** sekmesinde üçüncü işi seçer ve sonra **Grupla**'yı seçer. **Grupla** iletişim kutusunda, çalışan, başlangıç miktarını ayarlayabilir. Çalışan bu iletişim kutusunu, **Grupla** seçeneğini belirleyerek onaylar.

## <a name="working-on-indirect-activities"></a>Dolaylı faaliyetlerde çalışma

Dolaylı faaliyetler, doğrudan bir üretim emriyle ilişkili olmayan faaliyetlerdir. Dolaylı faaliyetler, [Zaman ve katılımcı için dolaylı faaliyetleri ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance) konusunda açıklandığı şekilde esnek bir şekilde tanımlanabilir.

Örneğin Contoso'da bir kat çalışanı olan Shannon, şirket toplantısına katılmak istiyor ve toplantılar dolaylı bir faaliyet olarak kabul edilir. Aşağıdaki iki senaryodan biri geçerlidir:

- **Shannon bir veya daha fazla etkin iş üzerinde çalışıyor.** Shannon **Etkinlik**'i seçer, etkinliği (toplantıyı) tanımlar ve seçimini onaylar. Sürmekte olan işleri olduğunu bildiren bir ileti görüntülenir. İletide, Shannon, toplantıya geçmeden önce üzerinde çalıştığı işleri tamamlamayı veya durdurmayı seçebilir.
- **Shannon'ın hiçbir etkin işi yok.** Shannon **Etkinlik**'i seçer, etkinliği (toplantıyı) tanımlar ve seçimini onaylar. Şimdi toplantıda olduğu kaydedildi.

Her iki durumda da Shannon seçimini onayladıktan sonra, oturum açma sayfasına veya dolaylı faaliyetinden dönmüş olduğunu onaylamasını bekleyen bir sayfaya gider. Beliren sayfa, üretim tabanı yürütme arabiriminin konfigürasyonuna bağlıdır. (Daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini yapılandırma](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Molaları kaydetme

Çalışanlar mola kaydedebilir. Molalar, [Kayıt temel alınarak ödeme](pay-based-on-registrations.md) konusunda açıklandığı gibi esnek şekilde tanımlanabilir.

Bir çalışan **Mola**'yı seçip ardından mola türünü temsil eden kartı (öğle yemeği gibi) seçerek bir molayı kaydeder. Çalışan seçimi onayladıktan sonra, cihazda oturum açma sayfası veya çalışanın moladan döndüğünü onaylayacağı bir sayfa gösterilir. Beliren sayfa, üretim tabanı yürütme arabiriminin konfigürasyonuna bağlıdır. (Daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini yapılandırma](production-floor-execution-configure.md).)

## <a name="opening-instructions"></a>Açılış yönergeleri

Çalışanlar, **yönergeler** i seçerek işe iliştirilen bir belgeyi açabilirler. **Yönergeler** düğmesi, yalnızca belge ana verilerdeki işle ilişkilendirildiğinde kullanılabilir. Örneğin, Supply Chain Management **Serbest bırakılan ürünler** sayfasındaki bir ürüne iliştirilmiş bir belge, çalışanların atölye yürütme arabiriminde açmasını sağlayacak şekilde kullanılabilir.

## <a name="opening-mixed-reality-guides-for-hololens"></a>HoloLens için karma gerçeklik kılavuzlarını açma

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) Karma Gerçeklik kullanan Uygulamalı Öğrenim sunarak çalışanlara yardımcı olabilir. Çalışanlarınıza gereksinim duydukları araçlar ve parçalara yönelik kılavuzluk sağlayan adım adım yönergelerle standartlaştırılmış süreçler belirleyebilir ve bu araçların gerçek çalışma durumlarında nasıl kullanılacağını çalışanlarınıza gösterebilirsiniz. İşleme genel bakış.

1. Bir çalışan atölye yürütme arabiriminde bir iş listesi açtığında, arabirim gösterilen işler için ilgili kılavuzları bulur.
1. Çalışan, kılavuz listesini görmek için **kılavuzları** seçer.
1. Çalışan, listede ilgili bir Kılavuzu seçer.
1. Atölye yürütme arabirimi, seçilen kılavuzun QR kodunu gösterir.
1. Çalışan, HoloLens takar ve Kılavuzu başlatmak için QR koduna bakar.
1. Çalışan, görevi öğrenmek için kılavuzu inceler.

HoloLens için Kılavuzlar oluşturma, atama ve kullanma hakkında daha fazla bilgi için bkz. [Üretimde çalışanlar için karma gerçeklik kılavuzları sağlama](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]