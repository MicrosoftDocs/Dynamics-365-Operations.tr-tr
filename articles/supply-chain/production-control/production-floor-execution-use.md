---
title: Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?
description: Bu makale, bir çalışanın bakış açısından üretim katı yürütme arabiriminin nasıl kullanılacağını açıklar.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 876ee36c75a31ca89a9351d0ee1484e66076b6aa
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748726"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?

[!include [banner](../includes/banner.md)]

Üretim katı yürütme arabirimi dokunma etkileşimi için en iyi duruma getirilmiştir. Tasarımı, atölye ortamları için erişilebilirlik gereksinimlerini karşılayan görsel bir kontrast sağlar. İş kartı cihazı ile aynı işlevsel tüm yetenekleri sunar. Ancak, bir iş listesinden paralel olarak birden fazla işin başlatılmasına olanak tanır. (Bu yetenek *iş gruplama* olarak da bilinir.) Ek olarak, bir iş listesinden, çalışanlar Microsoft Dynamics 365 kılavuzunda oluşturulmuş bir Kılavuzu açabilir. Böylece, bir HoloLens üzerinde görsel yönergeler elde edebilirler.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Çalışan olarak üretim katı yürütme arabiriminde nasıl oturum açılır?

Çalışanlar cihazı kullanmaya başlamadan önce, bir gözetmen veya teknik personelin bunu hazırlaması ve Dynamics 365 Supply Chain Management'ta doğru sayfayı açması gerekir. Cihazı ayarlama hakkında daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini çalıştırmak için cihazı ayarlama](production-floor-execution-setup.md).

Cihaz hazırlandıktan sonra, üzerinde oturum açma sayfası görüntülenir. Bu sayfa, yerel iş hücresi işlerinin durumu hakkında bilgi gösterir. Bu bilgiler periyodik olarak güncelleştirilir. Sayfada, çalışanlar oturum açmak için kendi rozet kimliklerini kullanırlar. Çalışanların Supply Chain Management için bir kullanıcı hesabına sahip olmaları gerekmemesine rağmen, kullanıcıların oturum açarken kullanabileceği *saatine kayıtlı çalışan* hesabı olmalıdır.

![Üretim katı yürütme arabirimi oturum açma sayfası.](media/pfei-sign-in-page.png "Üretim katı yürütme arabirimi oturum açma sayfası")

Bu makalenin geri kalan bölümleri, çalışanların arabirimle nasıl etkileştiğini açıklamaktadır.

## <a name="all-jobs-tab"></a>Tüm işler sekmesi

**Tüm işler** sekmesi, durumu *başlatılmadı*, *durduruldu* veya *Başlatıldı* olan tüm üretim işlerini gösteren bir iş listesi sağlar. (Bu sekme adı özelleştirilebilir ve sisteminiz için farklı olabilir.)

![Tüm işler sekmesi.](media/pfei-all-jobs-tab.png "Tüm işler sekmesi")

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

![Etkin işler sekmesi.](media/pfei-active-jobs-tab.png "Etkin işler sekmesi")

Etkin işler aşağıdaki sütunlar vardır:

- **Seçim sütunu**: En soldaki sütun, çalışan tarafından seçilmiş olan işleri belirtmek için onay işareti kullanır. Çalışanlar, aynı anda listedeki birden fazla işi seçebilir. Listedeki tüm işleri seçmek için, sütun başlığındaki onay işaretini seçin. Tek bir iş seçildiğinde, o işle ilgili ayrıntılar sayfanın alt bölümünde gösterilir.
- **Sipariş**: Bu sütun bir projeyle ilgili üretim emri numarasını gösterir.
- **Açıklama**: Bu sütunda bir projenin ait olduğu operasyonun açıklaması gösterilir.
- **Gerekli**: Bu sütunda bir işin üretilmesi için planlanan miktar gösterilir.
- **Başlatıldı**: Bu sütunda, bir proje için zaten başlatılmış olan miktar gösterilir.
- **Tamamlandı**: Bu sütunda, bir proje için zaten tamamlanmış olan miktar gösterilir.
- **Hurdaya çıkarıldı**: Bu sütunda, bir proje için zaten hurdaya çıkarılmış olan miktar gösterilir.
- **Geri kalan**: Bu sütunda bir proje için tamamlanmak üzere kalan miktar gösterilir.

## <a name="my-jobs-tab"></a>İşlerim sekmesi

**İşlerim** sekmesi, çalışanları özel olarak kendilerine atanan tüm başlamamış ve bitmemiş işleri kolaylıkla görüntülemenizi sağlar. Bunlar, işlerin bazen başka türden kaynaklar (örneğin makineler) yerine belirli çalışanlara (insan kaynakları) atanan ya da her zaman çalışan şirketlerde yararlıdır.

Zamanlama sistemi, her bir üretim işini belirli bir kaynak kaydına otomatik olarak atar ve her kaynak kaydının bir türü vardır (makine veya insan gibi). Bir çalışanı üretim çalışanı olarak ayarladığınızda, çalışan hesabını benzersiz bir insan kaynakları kaydıyla ilişkilendirebilirsiniz.

**İşlerim** sekmesi, oturum açmış bir çalışan çalışanın insan kaynakları kaydına atanan tüm başlamamış ve tamamlanmamış işleri listeler. Oturum açmış çalışan o işlerle çalışmaya başlasa bile, bir makineye veya başka türde bir kaynağa atanan işleri hiçbir zaman listelemez.

Oturum açan çalışan tarafından başlatılan tüm işleri, her projenin atandığı kaynak türüne bakılmaksızın görüntülemek için **Etkin işler** sekmesini kullanın. Çalışan veya başlatma durumundan bağımsız olarak, yerel iş filtresinin konfigürasyonuyla eşleşen bitmemiş tüm işleri görüntülemek için, **Tüm işler** sekmesini kullanın.

![İşlerim sekmesi.](media/pfei-my-jobs-tab.png "İşlerim sekmesi")

## <a name="my-machine-tab"></a>Makinem sekmesi

**Makinem** sekmesi, çalışanların **Tüm işler** sekmesinde ayarlanan filtre dahilindeki makine kaynağına bağlı olan kıymeti seçmesine olanak tanır. Çalışan, en fazla dört seçili sayacın değerlerini ve en son bakım istekleri ve kaydedilmiş kesinti süreleri listelerini okuyarak seçili kıymetin durumunu ve sistem durumunu görüntüleyebilir. Çalışan aynı zamanda seçili kıymet için bakım isteyebilir ve makine kesinti süresini kaydedebilir ve düzenleyebilir. (Bu sekme adı özelleştirilebilir ve sisteminiz için farklı olabilir.)

![Makinem sekmesi.](media/pfei-my-machine-tab.png "Makinem sekmesi")

**Makinem** sekmesi aşağıdaki sütunlara sahiptir. Sayılar, önceki görseldeki sayılara karşılık gelir.

1. **Makine kıymeti**: İzlemek istediğiniz makine kıymetini seçin. Eşleşen kıymetler listesinden seçim yapmak için bir ad yazmaya başlayın veya iş listesi filtresi dahilindeki kaynaklarla ilişkilendirilmiş tüm kıymetlerin listesinden seçim yapmak için büyüteç simgesini seçin.

    > [!NOTE]
    > Supply Chain Management kullanıcıları, **Tüm kıymetler** sayfasını kullanarak gerektiğinde her kıymete bir kaynak atayabilir (**Sabit kıymet** sekmesindeki **Kaynak** açılır listesini kullanarak). Daha fazla bilgi için bkz. [Kıymet oluşturma](../asset-management/objects/create-an-object.md).

1. **Ayarlar**: Seçili makine kıymeti için görüntülenecek sayaçları seçebileceğiniz bir iletişim kutusu açmak için dişli simgesini seçin. Bu sayaçların değerleri, **Kıymet yönetimi** sekmesinin en üstünde gösterilir. **Ayarlar** menüsü (aşağıdaki ekran görüntüsünde gösterilmektedir) en çok dört sayacı etkinleştirmenize olanak tanır. Etkinleştirmek istediğiniz her sayaç için, kutucuğun üst tarafındaki arama alanını kullanarak bir sayaç seçin. Arama alanı, **Kıymet yönetimi** sayfasının en üstünde seçilen kıymetle ilişkilendirilmiş tüm sayaçları listeler. Sayaç için **Toplam** değeri veya en son **Gerçek** değeri izlemek için her sayacı ayarlayın. Örneğin, makinenin kaç saattir çalıştığını takip eden bir sayaç ayarlarsanız bunu **Toplam** olarak ayarlamanız gerekir. En son güncelleştirilen sıcaklığı veya basıncı ölçmek üzere bir sayaç ayarlarsanız, bunu **Gerçek** olacak şekilde ayarlamalısınız. Ayarlarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.

    ![Makinem sekmesi ayarları.](media/pfei-my-machine-tab-settings.png "Makinem sekmesi ayarları")

1. **Bakım iste**: Bakım isteği oluşturabileceğiniz bir iletişim kutusu açmak için bu düğmeyi seçin. Açıklama ve bir not girebilirsiniz. Talep, bir Supply Chain Management kullanıcısına gösterilir ve bu kullanıcı bakım isteğini bakım iş emrine dönüştürebilir.
1. **Kesinti süresini kaydet**: Makinenin kesinti süresini kaydedebileceğiniz bir iletişim kutusu açmak için bu düğmeyi seçin. Bir neden kodu seçebilir ve kesinti süresi için bir tarih/saat aralığı girebilirsiniz. Makinenin kesinti süresi kaydı, makine kıymetinin verimliliğini hesaplamak için kullanılır.
1. **Görüntüle veya düzenle**: Mevcut kesinti süresi kayıtlarını düzenleyebileceğiniz veya görüntüleyebileceğiniz bir iletişim kutusu açmak için bu düğmeyi seçin.

## <a name="starting-and-completing-production-jobs"></a>Üretim işlerini başlatma ve tamamlama

Çalışanlar, **tüm işler** sekmesinde iş seçip **işi Başlat** iletişim kutusunu açmak için **işi Başlat**'ı seçerek bir üretim işi başlatır.

![İş başlatma iletişim kutusu.](media/pfei-start-job-dialog.png "İş başlatma iletişim kutusu")

Çalışanlar üretim miktarını doğrulamak ve işi başlatmak için **İşi Başlat** iletişim kutusunu kullanırlar. Çalışanlar **miktar** alanını seçip beliren sayısal klavyeyi kullanarak miktarı ayarlayabilir. Ardından çalışanlar, iş üzerinde çalışmaya başlamak için **Başlat**'ı seçer. **İşi Başlat** iletişim kutusu kapatılır ve iş **etkin işler** sekmesine eklenir.

Çalışanlar herhangi bir durumda olan bir işi başlatabilir. Bir çalışan, durumu *başlatılmadı* olan bir işi başlattığında, **işi Başlat** iletişim kutusundaki **miktar** alanı, ilk olarak tüm miktarı gösterir. Bir çalışan, durumu *Başlatıldı* veya *Durduruldu* olan bir işi başlattığında, **Miktar** alanı, ilk olarak kalan miktarı gösterir.

## <a name="reporting-good-quantities"></a>Sağlam miktarlar raporlaması

Bir çalışan bir işi tamamladığında veya kısmen tamamladığında, **etkin işler** sekmesinde bir iş seçip sonra **İlerlemeyi Raporla**'yı seçerek üretilen sağlam miktarları rapor edebilir. Sonra, **İlerlemeyi Raporla** iletişim kutusunda, çalışan sayısal klavyeyi kullanarak sağlam miktarı girer. Varsayılan olarak miktar boştur. Bir miktar girildikten sonra, çalışan, işin durumunu *devam ediyor*, *Durduruldu* veya *tamamlandı* olarak güncelleştirebilir.

![İlerlemeyi raporla iletişim kutusu.](media/pfei-report-progress-dialog.png "İlerlemeyi raporla iletişim kutusu")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Ortak ürün ve yan ürünleri olan toplu iş emirleriyle ilgili iyi miktarlar raporlama

Çalışanlar, toplu iş emirleriyle ilgili ilerlemeyi bildirmek için üretim tabanı yürütme arabirimini kullanabilir. Bu raporlama, ortak ürünlerde ve yan ürünlerde raporlamayı içerir.

Bazı üreticiler, özellikle işlem endüstrileri, üretim süreçlerini yönetmek için toplu iş emirleri kullanır. Toplu iş emirleri formüllerden oluşturulur ve bu formüller, çıkış olarak ortak ürünlere ve ürünlere sahip olacak şekilde tanımlanabilir. Bu toplu iş emirleriyle ilgili geribildirim raporlanırsa, çıktı tutarının formül maddesine ve ayrıca ortak ürünlerde ve ürünlere göre kaydedilmiş olması gerekir.

Bir çalışan bir toplu iş emrindeki bir işi tamamladığında veya kısmen tamamladığında, sipariş için çıktı olarak tanımlanan her ürün için sağlam veya ıskarta miktarları rapor edebilir. Toplu iş emri için çıktı olarak tanımlanan ürünler *Formül*, *Ortak ürün* veya *Yan ürün* türünde olabilir.

Ürünlere doğru miktarları bildirmek için, çalışan **Etkin işler** sekmesinde bir iş seçer ve sonra **Rapor ilerlemesini** seçer.

Sonra, **Rapor ilerleme durumu** iletişim kutusunda, çalışan raporlamak üzere toplu iş siparişi için çıktı olarak tanımlanan ürünler arasından seçim yapabilir. Çalışan, listedeki bir veya daha fazla ürün seçebilir ve **Rapor ilerlemesini** seçebilir. Her ürün için, miktar varsayılan olarak boştur ve çalışan miktarı girmek için sayısal klavyeyi kullanabilir. Çalışan, seçili ürünler arasında hareket etmek için **Önceki** ve **Sonraki** düğmelerini kullanabilir. Her ürün için bir miktar girildikten sonra, çalışan, işin durumunu *devam ediyor*, *Durduruldu* veya *tamamlandı* olarak güncelleştirebilir.

![Ortak ürünler ve yan ürünler bildirme](media/report-co-by-products.png "Ortak ürünler ve yan ürünler bildirme")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Planlama maddeleri için toplu iş emirleri üzerinde raporlama

Bir çalışan bir planlama maddesi için toplu iş emrindeki bir işi tamamladığında, bu maddeler *Formül* türünde bir madde içermediği için, yalnızca ortak ürün ve ürünlere ait miktarları raporlarsınız.

### <a name="reporting-co-product-variation"></a>Ortak ürün çeşitlemesi ile raporlama

**Ortak ürün çeşitleri** seçeneğinin *Evet* olarak ayarlandığı bir formül sürümünden toplu iş emri oluşturulursa, çalışan, toplu iş emirleriyle ilgili tanımın bir parçası olmayan ortak ürünlerde rapor verebilir. Bu işlev, üretim sürecinde beklenmeyen ürün çıktısının oluşabileceği senaryolarda kullanılır.

Bu durumda, çalışan, rapor ilerlemesi iletişim kutusunda **Ortak ürünler çeşitlerini** seçerek ortak ürün ve rapor edilecek miktarı belirtebilir. Çalışan, ortak ürün olarak tanımlanan tüm serbest bırakılan ürünler arasından seçim yapabilir.

### <a name="reporting-catch-weight-items"></a>Fiili ağırlık maddeleri raporlama

Çalışanlar, fiili ağırlık maddeleri için oluşturulan toplu iş emirleriyle ilgili ilerlemeyi bildirmek için bu üretim tabanı yürütme arabirimini kullanabilir. Toplu iş emirleri formüllerden oluşturulur ve bu formüller, formül maddeleri, ortak ürünler ve ürünler olarak fiili ağırlığa sahip olacak şekilde tanımlanabilir. Bir formül, fiili ağırlık olarak tanımlanan malzemeler için formül satırlarına sahip olacak şekilde de tanımlanabilir. Fiili ağırlık maddeleri stoğu izlemek için iki ölçü birimi kullanır: fiili ağırlık miktarı ve stok miktarı. Örneğin, yiyecek endüstrisinde kutulanmış et, fiili ağırlık miktarının kutu sayısını izlemek için kullanıldığı ve kutuların ağırlığını izlemek için stok miktarının kullanıldığı bir fiili ağırlık maddesi olarak tanımlanabilir.

## <a name="reporting-scrap"></a>Hurda raporlaması

Bir çalışan bir işi tamamladığında veya kısmen tamamladığında, **etkin işler** sekmesinde bir iş seçip sonra **Hurdayı Raporla**'yı seçerek hurdayı rapor edebilir. Sonra, **Hurdayı Raporla** iletişim kutusunda, çalışan sayısal klavyeyi kullanarak hurda miktarını girer. Çalışan ayrıca bir neden (*yok*, *makine*, *işleç* veya *malzeme*) seçer.

![Hurda raporla iletişim kutusu.](media/pfei-report-scrap-dialog.png "Hurda raporla iletişim kutusu")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Malzeme tüketimini ayarlama ve malzeme ayırmaları yapma

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Çalışanlar her üretim işi için malzeme tüketimini ayarlayabilir. Bu işlevsellik, bir üretim işi tarafından tüketilen gerçek malzeme miktarının planlanan miktardan daha fazla veya daha az olduğu senaryolarda kullanılır. Bu nedenle, stok düzeylerini güncel tutmak için ayarlanmalıdır.

Çalışanlar ayrıca malzemelerin toplu iş ve seri numaraları üzerinde rezervasyon yapabilir. Bu işlevsellik, bir çalışanın malzeme izlenebilirlik gereksinimlerini karşılamak için hangi malzeme toplu iş veya seri numaralarının tüketildiğini el ile belirtmesi gereken senaryolarda kullanılır.

Çalışanlar **Malzemeyi ayarla**'yı seçerek ayarlanacak miktarı belirtebilir. Bu düğme, aşağıdaki senaryolarda kullanılabilir:

- **Hurda raporla** iletişim kutusunda
- **İlerlemeyi raporla** iletişim kutusunda
- Sağdaki araç çubuğunda

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Hurdayı raporla ve İlerlemeyi raporla iletişim kutularından malzeme tüketimini ayarlama

Bir çalışan **İlerlemeyi raporla** veya **Hurdayı raporla** iletişim kutusuna raporlanacak miktarı girdikten sonra **Malzemeyi ayarla** düğmesi kullanılabilir duruma gelir. Kullanıcı bu düğmeyi seçtiğinde, **Malzemeyi ayarla** iletişim kutusu görüntülenir. Bu iletişim kutusu, proje için iyi veya hurdaya çıkarılan miktar bildirildiğinde tüketilmesi planlanan maddeleri listeler.

İletişim kutusundaki listede aşağıdaki bilgiler gösterilir:

- **Ürün numarası** – Ana ürün ve ürün varyantı.
- **Ürün adı**: Ürünün adı.
- **Teklif** – Proje için belirtilen miktar için ilerleme veya hurda bildirildiğinde tüketilecek tahmini malzeme miktarı.
- **Tüketim** – Proje için belirtilen miktar için ilerleme veya hurda bildirildiğinde tüketilecek gerçek malzeme miktarı.
- **Ayrılan** – Stokta fiziksel olarak ayrılan malzeme miktarı.
- **Birim** – Ürün reçetesi birimi.

İletişim kutusunun sağ tarafında aşağıdaki bilgiler gösterilir:

- **Ürün numarası** – Ana ürün ve ürün varyantı.
- **Tahmini** – Tüketecek tahmini miktar.
- **Başlatıldı** – Üretim işinde başlatılan miktar.
- **Kalan miktar** – Tahmini miktarın, tüketilmek üzere kalan miktarı.
- **Serbest bırakılan miktar** – Tüketilen miktar.

Aşağıdaki işlemler gerçekleştirilebilir:

- Çalışan, **Tüketimi ayarla**'yı seçerek malzeme için ayarlanacak miktarı belirtebilir. Miktar onaylandıktan sonra, **Tüketim** sütunundaki miktar ayarlanan miktarla güncelleştirilir.
- Çalışan **Malzemeyi ayarla**'yı seçtiğinde, bir üretim malzeme çekme listesi günlüğü oluşturulur. Bu günlük, **Malzemeyi ayarla** listesiyle aynı maddeleri ve miktarları içerir.
- Çalışan **Malzemeyi ayarla** iletişim kutusundaki bir miktarı ayarladığında, ilgili günlük satırındaki **Teklif** alanı aynı miktarla güncelleştirilir. Çalışan **Malzemeyi ayarla** iletişim kutusunda **İptal**'i seçerse, malzeme çekme listesi silinir.
- Çalışan **Tamam**'ı seçerse malzeme çekme listesi silinmez. **Hurdayı raporla** veya **İlerlemeyi raporla** iletişim kutusunda bildirildiğinde deftere nakledilir.
- Çalışan **İlerlemeyi raporla** veya **Hurda raporla** iletişim kutusunda **İptal**'i seçerse, malzeme çekme listesi silinir.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Birincil veya ikincil araç çubuğundan malzeme ayarlama

**Malzemeyi ayarla** düğmesi, birincil veya ikincil araç çubuğunda görünecek şekilde yapılandırılabilir. (Daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).) Çalışan, devam etmekte olan bir üretim işi için **Malzemeyi ayarla**'yı seçebilir. Bu durumda, çalışanın istenen ayarlamaları yapabileceği **Malzemeyi ayarla** iletişim kutusu görüntülenir. İletişim kutusu açıldığında, üretim emri için ayarlanan miktarlar için satırlar içeren bir üretim malzeme çekme listesi oluşturulur. Çalışan **Şimdi deftere naklet**'i seçerse, ayarlama onaylanır ve malzeme çekme listesi deftere nakledilir. Çalışan **İptal**'i seçerse, malzeme çekme listesi silinir ve ayarlama yapılmaz.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Fiili ağırlık maddeleri için malzeme tüketimini ayarla

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Çalışanlar, fiili ağırlık maddeleri için malzeme tüketimini ayarlayabilir. Bu işlevsellik, bir üretim işi tarafından tüketilen gerçek fiili ağırlık malzeme miktarının planlanan miktardan daha fazla veya daha az olduğu senaryolarda kullanılır. Bu nedenle, stok düzeylerini güncel tutmak için ayarlanmalıdır. Bir çalışan fiili ağırlık maddesinin tüketimini ayarladığında, hem fiili ağırlık miktarını hem de stok miktarını ayarlayabilirler. Örneğin, bir üretim işi kutu başına 2 kilogram tahmini ağırlığı olan beş kutu tüketmek üzere planlanacaksa, çalışan hem kullanılacak sayıda kutuyu hem de kutuların ağırlığını ayarlayabilir. Sistem, kutuların belirtilen ağırlığının, serbest bırakılan üründe tanımlanan minimum ve maksimum eşik içinde olduğunu doğrular.

### <a name="reserve-materials"></a>Yedek malzemeler

**Malzemeyi ayarla** iletişim kutusunda, bir çalışan **Malzemeyi ayır**'ı seçerek malzeme rezervasyonları yapabilir ve ayarlayabilir. Görüntülenen **Malzemeyi ayır** iletişim kutusu, her depolama ve izleme boyutu için madde için fiziksel olarak kullanılabilir stoku gösterir.

Malzeme ambar yönetimi işlemleri (WMS) için etkinleştirilmişse liste malzemenin üretim giriş konumu için yalnızca fiziksel olarak kullanılabilir stoku gösterir. Üretim giriş konumu, üretim işinin planlandığı kaynakta tanımlanır. Madde numarası toplu iş veya seri numarası kontrollüyse, fiziksel olarak kullanılabilir toplu iş ve seri numaralarının tam listesi gösterilir. Rezerve edilecek miktarı belirtmek için, çalışan **Malzemeyi ayır**'ı seçebilir. Varolan bir ayırmayı kaldırmak için, çalışan **Ayırmayı kaldır**'ı seçebilir.

Üretim giriş konumunu ayarlama hakkında daha fazla bilgi için şu blog yazısına bakın: [Üretim giriş konumunu ayarlama](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Çalışan **İlerlemeyi raporla** veya **Hurda raporla** iletişim kutusunda **İptal**'i seçtiğinde, çalışanın **Malzemeyi ayır** iletişim kutusunda yaptığı ayırmalar kalır.
>
> Fiili ağırlık maddeleri için rezervasyonlar ayarlanamaz.

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

Dolaylı faaliyetler, doğrudan bir üretim emriyle ilişkili olmayan faaliyetlerdir. Dolaylı faaliyetler, [Zaman ve katılımcı için dolaylı faaliyetleri ayarlama](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance) konusunda açıklandığı şekilde esnek bir şekilde tanımlanabilir.

Örneğin Contoso'da bir kat çalışanı olan Shannon, şirket toplantısına katılmak istiyor ve toplantılar dolaylı bir faaliyet olarak kabul edilir. Aşağıdaki iki senaryodan biri geçerlidir:

- **Shannon bir veya daha fazla etkin iş üzerinde çalışıyor.** Shannon **Etkinlik**'i seçer, etkinliği (toplantıyı) tanımlar ve seçimini onaylar. Sürmekte olan işleri olduğunu bildiren bir ileti görüntülenir. İletide, Shannon, toplantıya geçmeden önce üzerinde çalıştığı işleri tamamlamayı veya durdurmayı seçebilir.
- **Shannon'ın hiçbir etkin işi yok.** Shannon **Etkinlik**'i seçer, etkinliği (toplantıyı) tanımlar ve seçimini onaylar. Şimdi toplantıda olduğu kaydedildi.

Her iki durumda da Shannon seçimini onayladıktan sonra, oturum açma sayfasına veya dolaylı faaliyetinden dönmüş olduğunu onaylamasını bekleyen bir sayfaya gider. Beliren sayfa, üretim tabanı yürütme arabiriminin konfigürasyonuna bağlıdır. (Daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini yapılandırma](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Molaları kaydetme

Çalışanlar mola kaydedebilir. Molalar, [Kayıt temel alınarak ödeme](pay-based-on-registrations.md) konusunda açıklandığı gibi esnek şekilde tanımlanabilir.

Bir çalışan **Mola**'yı seçip ardından mola türünü temsil eden kartı (öğle yemeği gibi) seçerek bir molayı kaydeder. Çalışan seçimi onayladıktan sonra, cihazda oturum açma sayfası veya çalışanın moladan döndüğünü onaylayacağı bir sayfa gösterilir. Beliren sayfa, üretim tabanı yürütme arabiriminin konfigürasyonuna bağlıdır. (Daha fazla bilgi için bkz. [Üretim katı yürütme arabirimini yapılandırma](production-floor-execution-configure.md).)

## <a name="view-the-my-day-dialog"></a>"Günüm" iletişim kutusunu görüntüleme

**Günüm** iletişim kutusu, çalışanların kayıtlarının ve bakiyelerinin genel bir özetini sağlar. İletişim kutusu aşağıdaki üç bölüme ayrılmıştır:

- Ana bölümde, seçilen bir tarihte geçerli çalışanın yaptığı kayıtlar listelenir. Geçerli gün için kayıtları göstererek açılır ve alt görünümün diğer günlerle aynı olmasını sağlayan bir tarih seçici sağlar.
- **Son hesaplanan günlük bakiye** bölümünde, çalışanın ücretli süre, ücretli fazla mesai, devamsızlık ve ücretli devamsızlık hakkındaki geçerli bakiyeleri gösterilir. Bu değerler, onay işlemi sırasında hesaplanan kayıtlara dayanır.
- **Bakiyeler** bölümü, seçilen kayıt kategorileri (tatil, standart zaman ve fazla mesai gibi) için tanımlanmış bir dönemdeki bakiyelerin genel görünümünü sağlar. Bu bakiyeler, **Zaman ve katılımcı** modülünde istatistiksel bakiyelerin nasıl ayarlanacağını temel alan bir yöntemdir. Bunu ayarlama hakkında daha fazla bilgi için bkz. [Üretim katı yürütme arabiriminde tatil bakiyelerini gösterme](production-floor-execution-payroll-stats.md).

Yöneticiler, [Üretim kat yürütme arabiriminde tasarımda](production-floor-execution-tabs.md) açıklandığı gibi her ilgili sekme için, **Günüm** düğmesini bir araç çubuğuna yerleştirerek bu özelliği arabirime ekleyebilir.

## <a name="working-in-teams"></a>Ekipte çalışma

Aynı üretim işine birden fazla işçi atandığında, bir ekip oluşturabilirler. Ekip, bir çalışanı pilot olarak aday gösterebilir. Kalan işçiler ardından otomatik olarak bu pilotun asistanı olurlar. Ortaya çıkan ekip için, yalnızca pilot iş durumunu kaydetmelidir. Zaman kayıtları tüm ekip üyeleri için geçerlidir.

### <a name="prerequisites"></a>Önkoşullar

Takımları kullanmak için, yöneticinin, üretim tabanı yürütme arabiriminin **Tüm işler** sekmesindeki birincil araç çubuğu için **Yardımcı** eylemini etkinleştirmesi gerekir. Talimatlar için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Pilot ve asistan bulunan yeni bir takım oluştur

Çalışan, **Tüm işler** sekmesinde **Yardımcı**'yı seçerek yardımcı olarak kayıt yapabilir. Sonra da görüntülenen **Yardımcı yapılacak bir çalışanı seç** iletişim kutusunda çalışan, bir iş üzerinde etkin şekilde çalışan çalışanların listesinden bir pilot seçebilir. Çalışan, seçimini teyit ettikten sonra, seçilen çalışan için yeni ekibin lideri olan bir yardımcı olurlar.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Varolan bir takıma yeni bir pilot atama

Bir takım yeni bir pilot seçmek istediğinde, geçerli lider ekipte yeni bir çalışan olarak başka bir çalışanı aday vermelidir. Yeni bir pilot için aday eklemek amacıyla, geçerli pilot **Tüm işler** sekmesindeki **Yardımcı**'yı seçer. Daha sonra pilot, görüntülenen **Pilot değiştir** iletişim kutusundan zaten ekipte olan çalışanlar arasından yeni bir pilot seçebilir. Geçerli pilot onların seçimini onayladıktan sonra takımdan tamamen çıkarılır. Ancak, takıma gereksinim duydukları sürece yeniden katılabilir.

### <a name="assistant-clocks-out"></a>Yardımcı görev çıkışı

Yardımcı olarak çalışan bir çalışan görev çıkışı yaptığında takımdan ayrılırlar. **Kalıcı takımlar** ve **Göreve girişte yeniden başla** seçenekleri *Evet* olarak ayarlanmışsa, görev çıkışı yapan bir çalışan sonraki görev girişinde otomatik olarak ekibe yeniden katılır. Bu seçenekleri , **Zaman ve katılımcı parametreleri** sayfasının **Genel** sekmesinde bulabilirsiniz.

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
