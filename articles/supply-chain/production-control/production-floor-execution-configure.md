---
title: Üretim katı yürütme arabirimini yapılandırma
description: Bu konu, üretim katı yürütme arabirimi için bir veya daha fazla konfigürasyon oluşturmayı açıklamaktadır. Üretim katı yürütme arabirimini açtığınızda, seçilen bir konfigürasyon ve tarayıcıya ve cihaza özel iş filtresini otomatik olarak yükler. Konfigürasyonda, belirli bir kullanım için geçerli olması gereken ilkeleri ayarlayabilirsiniz.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5a0ead85eaeb6b96b80716614990af8c8e5e70f7
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384759"
---
# <a name="configure-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini yapılandırma

[!include [banner](../includes/banner.md)]

Atölye çalışanları işlerin başlatılması, işlere ilişkin geri bildirim bildirmek, dolaylı faaliyetleri kaydetmek ve devamsızlığı bildirmek gibi günlük çalışmalarını kaydetmek için üretim katı yürütme arabirimini kullanır. Bu kayıtlar, ilerlemeyi izlemenin ve üretim emirleriyle ilgili maliyetin temelini oluşturur ve çalışanların ödemesine yönelik temel hesaplama içindir.

Üretim katı yürütme arabirimini açtığınızda, seçilen bir konfigürasyon ve tarayıcıya ve cihaza özel iş filtresini otomatik olarak yükler. Konfigürasyonda, belirli bir kullanım için geçerli olması gereken ilkeleri ayarlayabilirsiniz. Burada bazı kullanım örnekleri verilmiştir:

- Şirket salonundaki bir cihazda, çalışanlar ofise geldiği sırada girişleri ve çıkarken çıkışları kaydedilir.
- Atölye katındaki bir cihazda, makine operatörleri işleri başlatıp bitirdikleri saati kaydeder. Ayrıca, molalar ve dolaylı faaliyetleri de kaydederler.

Bu konu, tesisinizde kullanımda olan her cihaz için bir üretim katı yürütme arabirimi yapılandırmaya yönelik çeşitli seçenekleri açıklamaktadır.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Üretim katı yürütme arabirimini ve ilgili isteğe bağlı özellikleri açma

Üretim katı yürütme arabirimi ve bu konuda açıklanan isteğe bağlı ayarlardan birkaçı, bunları kullanabilmeniz için sisteminizden açılmalıdır. Aşağıdaki alt bölümlerde açıklanan özellikleri gerektiği gibi açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanın.

### <a name="the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimi

Bu konu, bu konuda açıklanan birincil özelliktir ve bu bölümde sözü edilen tüm diğer özellikler için bir önkoşuldur. Supply Chain Management 10.0.25 itibarıyla zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Üretim katı yürütme* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

### <a name="generate-license-plates"></a>Plaka oluşturma

Bu özellikler, üretim katı yürütme arabiriminin plaka işlevlerini kullanılabilir hale getirir. Bu özelliği kullanmak istiyorsanız [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. *İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası*<br>(Supply Chain Management sürüm 10.0.21 itibarıyla, bu özellik varsayılan olarak açıktır. Supply Chain Management sürüm 10.0.25 itibarıyla, bu özellik zorunludur.)
1. *İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin*<br>(Supply Chain Management sürüm 10.0.25 itibarıyla, bu özellik zorunludur.)

### <a name="print-labels"></a>Etiket yazdır

Bu özellikler, üretim katı yürütme arabiriminin etiket yazdırma işlevlerini kullanılabilir hale getirir. Bu özelliği kullanmak istiyorsanız [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. *İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası*<br>(Supply Chain Management sürüm 10.0.21 itibarıyla, bu özellik varsayılan olarak açıktır. Supply Chain Management sürüm 10.0.25 itibarıyla, bu özellik zorunludur.)
1. *İş Kartı Cihazından etiket yazdır*<br>(Supply Chain Management sürüm 10.0.25 itibarıyla, bu özellik zorunludur.)

### <a name="allow-locking-the-touch-screen"></a>Dokunmatik ekranın kilitlenmesini sağla

Bu özellik, çalışanların dokunmatik ekranı kilitlemesine ve temizlemesine olanak sağlar.

Supply Chain Management sürüm 10.0.21 itibariyle, bu özellik varsayılan olarak açıktır. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Temizlenebilmeleri için iş kartı cihazını ve iş kartı terminalini kilitleme özelliği* özelliğini bularak bu işlevi açabilir veya kapatabilir.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimi için varlık yönetim işlevi

Bu özellik, üretim tabanı yürütme arabirimine bir kıymet yönetimi sekmesi ekler. Çalışanlar bu sekmeyi, iş listesinin seçili filtresinde bulunan makine kaynağına bağlı bir kıymeti seçmek için kullanabilir. Çalışan, seçili makine kıymeti için en fazla dört seçili sayaçtaki sayaç değerlerinden kıymetin durumunu ve sistem durumunu görebilir. Bu özelliği kullanmak için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özelliği açın:

- *Üretim katı yürütme arabirimi için varlık yönetim işlevi*<br>(Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır.)

### <a name="enable-job-search"></a>İş aramasını etkinleştir

Bu özellik, iş listesine bir arama alanı eklemeyi mümkün kılar. Çalışanlar iş kimliği girerek belirli bir iş bulabilir veya sipariş kimliği girerek belirli bir sipariş için tüm işleri bulabilirler. Çalışanlar kimliği tuş takımı kullanarak veya barkod tarayarak girebilir. Kullanmak için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özellikleri açın:

- *Üretim katı yürütme arabiriminde iş arama*<br>(Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Ortak ürünlerde ve yan ürünlerde raporlamayı etkinleştir

Bu özellik, çalışanların toplu iş emirleriyle ilgili ilerlemeyi bildirmek için üretim tabanı yürütme arabirimini kullanmasına olanak tanır. Bu raporlama, ortak ürünlerde ve yan ürünlerde raporlamayı içerir. Bu işlevi kullanmak getirmek için, [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin:

- *Üretim katı yürütme arabiriminden ortak ve yan ürünler raporu*

### <a name="enable-the-display-of-full-serial-batch-and-license-plate-numbers"></a>Tam seri, toplu iş ve plaka numarası gösterilmesini etkinleştir

Bu özellik, üretim katı yürütme arabiriminde seri numara, toplu iş ve plaka numarası listelerini görüntülemek için iyileştirilmiş bir deneyim sağlar. Ekran, sınırlı sayıda karakter bulunan bir kart görünümünden tam değerleri göstermek için yeterli alan sağlayan bir liste görünümüne dönüşür. Liste ayrıca belirli numaraları arama olanağı da sağlar.

Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır. Yöneticiler, [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Üretim katı yürütme arabiriminde tam seri, toplu iş ve plaka numarası gösterilmesini etkinleştir* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

### <a name="enable-registering-of-material-consumption"></a>Malzeme tüketimini kaydetmeyi etkinleştirme

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Bu özellik, çalışanların malzeme tüketimini, toplu iş numaralarını ve seri numaralarını kaydetmek için üretim katı yürütme arabirimini kullanmalarını sağlar. Özellikle proses endüstrilerindekiler olmak üzere bazı üreticilerin, her bir toplu iş veya üretim emri için tüketilen malzeme miktarını açıkça kaydetmesi gerekir. Örneğin, çalışanlar çalışırken tüketilen malzeme miktarını tartmak için bir ölçek kullanabilir. Tam malzeme izlenebilirliğini sağlamak için bu kuruluşların her ürünü üretirken hangi parti numaralarının tüketildiğini de kaydetmeleri gerekir.

Bu özelliğin iki versiyonu vardır. Yalnızca gelişmiş ambar işlemlerini (WMS) kullanmak üzere *etkinleştirilmemiş* maddeleri destekler. Diğeri, WMS'yi kullanacak şekilde *etkinleştirilen* öğeleri destekler. Bu işlevi kullanmak için, WMS'de etkinleştirilen öğelere sahip olup olmadığınıza bağlı olarak, [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özelliklerden birini veya her ikisini etkinleştirin (bu sırada):

- *(Önizleme) Üretim katı yürütme arabiriminde malzeme tüketimini kaydetme (WMS dışı)*
- *(Önizleme) Üretim katı yürütme arabiriminde (WMS özellikli) malzeme tüketimini kaydet*

> [!IMPORTANT]
> WMS olmayan özelliğini tek başına kullanabilirsiniz. Ancak, WMS kullanırsanız, her iki özelliği de etkinleştirmeniz gerekir.

### <a name="enable-reporting-on-catch-weight-items"></a>Fiili ağırlık maddelerinde raporlamayı etkinleştirme

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Çalışanlar, fiili ağırlık maddeleri için toplu iş emirleriyle ilgili ilerlemeyi bildirmek için üretim tabanı yürütme arabirimini kullanabilir. Toplu iş emirleri formüllerden oluşturulur ve bu formüller, formül maddeleri, ortak ürünler ve ürünler olarak fiili ağırlığa sahip olacak şekilde tanımlanabilir. Bir formül, fiili ağırlık olarak tanımlanan malzemeler için formül satırlarına sahip olacak şekilde de tanımlanabilir. Fiili ağırlık maddeleri stoğu izlemek için iki ölçü birimi kullanır: fiili ağırlık miktarı ve stok miktarı. Örneğin, yiyecek endüstrisinde kutulanmış et, fiili ağırlık miktarının kutu sayısını izlemek için kullanıldığı ve kutuların ağırlığını izlemek için stok miktarının kullanıldığı bir fiili ağırlık maddesi olarak tanımlanabilir.

Bu işlevi kullanmak getirmek için, [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin:

- *(Önizleme) Üretim katı yürütme arabiriminden elde edilen fiili ağırlık öğeleriyle ilgili rapor*

## <a name="work-with-production-floor-execution-configurations"></a>Üretim katı yürütme arabirimi yapılandırmalarıyla çalışma

Üretim katı yürütme yapılandırmaları oluşturmak ve sürdürmek için, **Üretim denetimi \> Kurulum \>Üretim yürütme \> Üretim katı yürütmesini yapılandır**'a gidin. **Üretim katı yürütmesini konfigüre et** sayfası mevcut konfigürasyonların bir listesini gösterir. Bu sayfada aşağıdaki eylemleri gerçekleştirebilirsiniz:

- Görüntülemek ve düzenlemek için sol sütunda listelenmiş üretim katı yapılandırmasını seçin.
- Listeye yeni bir yapılandırma eklemek için Eylem Bölmesinde **Yeni**'yi seçin. Yeni Yapılandırmayı tanımlamanıza yardımcı olacak bir adı **yapılandırma** alanına girin. Buraya girdiğiniz ad, tüm yapılandırmalar arasında benzersiz olmalıdır ve daha sonra düzenleyemeyeceksiniz.

Sonra, seçili yapılandırmayla ilgili çeşitli ayarları yapılandırın. Aşağıdaki alanlar kullanılabilir:

- **Yalnızca giriş ve çıkış saati** - Yalnızca giriş ve çıkış işlevselliği sağlayan basitleştirilmiş bir arabirim oluşturmak için bu seçeneği *Evet* olarak ayarlayın. Bu, bu sayfadaki diğer seçeneklerin çoğunu devre dışı bırakır. Bu seçeneği etkinleştirmeden önce **Sekme seçimi** hızlı sekmesindeki tüm satırları kaldırmanız gerekir.
- **Aramayı etkinleştir** - İş listesine bir arama alanı eklemek için bu seçeneği *Evet* olarak ayarlayın. Çalışanlar iş kimliği girerek belirli bir iş bulabilir veya sipariş kimliği girerek belirli bir sipariş için tüm işleri bulabilirler. Çalışanlar kimliği tuş takımı kullanarak veya barkod tarayarak girebilir.
- **Çıkış saatindeki rapor miktarı:** çalışanların çıkış yaparken sürmekte olan işler hakkında geribildirim raporlamalarını istemek için bunu *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar uyarılmayacaktır.
- **Çalışanı kilitle**: Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar kayıt yapıldıktan hemen sonra (yeni bir iş gibi) oturumları kapatılır. Arabirim daha sonra oturum açma sayfasına geri dönecektir. Bu seçenek *Evet* olarak ayarlandığında, çalışanlar üretim katı yürütme arabiriminde oturum açmış durumda kalır. Ancak, bir çalışan, üretim katı yürütme arabirimi aynı sistem kullanıcı hesabı altında çalışmaya devam ederken başka bir çalışanın oturum açmasını sağlayacak şekilde el ile oturumunu kapatabilir. Bu hesap türleri hakkında daha fazla bilgi için, [atanan kullanıcılar](config-job-card-device.md#assigned-users)'a bakın.
- **Kaydın gerçek zamanını kullan**: Her yeni kaydın bir çalışan tarafından gönderildiği tam zamana eşit olması için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlandığında, bunun yerine oturum açma zamanı kullanılır. Genellikle, **çalışanı kilitle** ve/veya **Tek çalışan** seçeneklerini çalışanların daha uzun süreler boyunca oturum açmış durumda kaldığı durumlarda *Evet* olarak işaretlediyseniz bu seçeneği *Evet* olarak ayarlamak isteyeceksiniz.
- **Tek çalışan**: Bu yapılandırmanın etkin olduğu her üretim katı yürütme arabirimini yalnızca bir çalışan kullanıyorsa, bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Evet* olarak ayarlandığında **çalışanı kilitle** seçeneği otomatik olarak *Evet*'e ayarlanır. Ek olarak, bu ayar işçi için bir rozet kimliği (veya benzer kimlik) kullanarak oturum açabilme gereksinimi (ve yeteneğini) kaldırır. Bunun yerine çalışan  Microsoft Dynamics 365 Supply Chain Management'ta *zaman kayıtlı çalışana* (*çalışanlar* tablosundan) bağlı bir sistem kullanıcısı hesabı kullanarak oturum açar ve üretim katı yürütme arabiriminde aynı anda o çalışan olarak oturum açmış olur.
- **Dokunmatik ekranı kilitlemeye izin ver**: Çalışanların üretim katı yürütme arabirimi dokunmatik ekran seçeneklerini kilitlemesine izin vererek ekranı temizlemelerini sağlamak için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Evet* olarak ayarlandığında, oturum açma sayfasına **Temizlemek için ekranı kilitle** düğmesi eklenir. Bir çalışan bu düğmeyi seçtiğinde, dokunmatik ekran, istenmeyen giriş yapılmasını önlemek için geçici olarak kilitlenir. Ayrıca, geri sayım süreölçeri de görüntülenir. Çalışan daha sonra cihazı ve ekranı güvenle temizleyebilir. Geri sayım tamamlandığında, dokunmatik ekran otomatik olarak yeniden kilidi açar.
- **Ekran kilitleme süresi**: **Dokunmatik ekranı kilitlemeye izin ver** seçeneği *Evet* olarak ayarlandığında, bu seçeneği kullanın ve dokunmatik ekranın temizleme amacıyla kilitlenmesi gereken saniye sayısını belirtin. Süre 5 ile 120 saniye arasında olmalıdır.
- **Lisans plakası oluştur**: Bir çalışanın bir üretm katı yürütme arabirimini her kullandığında tamamlandı bildirimi oluşturmak için bu seçeneği *Evet* olarak ayarlayın. Lisans levhası numarası, **Ambar yönetimi parametreleri** sayfasında ayarlanmış bir numara serisinden oluşturulur. Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar tamamlandı bildirimine göre, varolan bir lisans levhası belirtmelidir.
- **Etiket yazdır**: Bir çalışan bir çalışma tamamlandı bildirimi yapmak için üretim katı yürütme arabirimini kullandığında bir lisans plakası yazdırmak için bu seçeneği *Evet* olarak ayarlayın. Etiketin konfigürasyonu belge yönlendirmesinde, [Lisans plak etiketlerinin belge yönlendirme](../warehousing/document-routing-layout-for-license-plates.md) düzeninde açıklandığı gibi ayarlanır.
- **Sekme seçimi**: Geçerli yapılandırma etkin olduğunda, üretim katı yürütme arabirimi tarafından hangi sekmelerin görüntüleneceğini seçmek için bu bölümdeki ayarları kullanın. İstediğiniz kadar sekme tasarlayabilir ve gerekirse bunları gerektiği gibi ekleyip düzenleyebilirsiniz. Sekmelerin nasıl tasarlanacağı ve buradaki ayarlarla nasıl çalışılacağı hakkında ayrıntılı bilgi için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>İş konfigürasyonlarını temizle

Atölye gözetmeni, üretim katıyürütme arabirimini ayarladığında, bir konfigürasyon ve bir iş filtresi seçer. Bu seçimler, Supply Chain Management'ta bir referans tablosunda depolanır ve tarayıcı, bu tabloda doğru satırı bulmak için yerel bir çerezde depolanan bir kimliği kullanır. Tablo ayrıca, bir çalışanın her cihazda en son oturum açtığı tarih ve saati de günlüğe kaydeder.

Son 60 gün içinde herhangi bir faaliyet kaydetmemiş olan cihazlar için, bir toplu iş, referanslar tablosundaki girişleri belirli aralıklarla temizler. Bu adımları izleyerek, istediğiniz zaman girişleri el ile de temizleyebilirsiniz.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.
1. Eylem bölmesinde, **İstemci yapılandırmalarını temizle**'yi seçin.
1. **İstemci yapılandırmasını Temizle** iletişim kutusunda **gün sayısı** alanını, dikkate alınacak etkin olmama gün sayısına (bugünün tarihinden önce) ayarlayın. Bu süre içinde etkin olmayan cihazlar için tüm yapılandırmaları ve oturum açma kayıtlarını kaldırırsınız.
1. **Gün sayısı** ayarını temel alarak ilgili konfigürasyonları temizlemek için **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
