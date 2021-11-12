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
ms.openlocfilehash: fa5a618527ce5a20b59902e7397000bf0796cbbb
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647201"
---
# <a name="configure-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini yapılandırma

[!include [banner](../includes/banner.md)]

Atölye çalışanları işlerin başlatılması, işlere ilişkin geri bildirim bildirmek, dolaylı faaliyetleri kaydetmek ve devamsızlığı bildirmek gibi günlük çalışmalarını kaydetmek için üretim katı yürütme arabirimini kullanır. Bu kayıtlar, ilerlemeyi izlemenin ve üretim emirleriyle ilgili maliyetin temelini oluşturur ve çalışanların ödemesine yönelik temel hesaplama içindir.

Üretim katı yürütme arabirimini açtığınızda, seçilen bir konfigürasyon ve tarayıcıya ve cihaza özel iş filtresini otomatik olarak yükler. Konfigürasyonda, belirli bir kullanım için geçerli olması gereken ilkeleri ayarlayabilirsiniz. Burada bazı kullanım örnekleri verilmiştir:

- Şirket salonundaki bir cihazda, çalışanlar ofise geldiği sırada girişleri ve çıkarken çıkışları kaydedilir.
- Atölye katındaki bir cihazda, makine operatörleri işleri başlatıp bitirdikleri saati kaydeder. Ayrıca, molalar ve dolaylı faaliyetleri de kaydederler.

Bu konu, iş kartı aygıtını konfigüre etmek için çeşitli seçenekleri açıklamaktadır.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Üretim katı yürütme arabirimini ve ilgili isteğe bağlı özellikleri açma

Üretim katı yürütme arabirimi ve bu konuda açıklanan isteğe bağlı ayarlardan birkaçı, bunları kullanabilmeniz için sisteminizden açılmalıdır. Aşağıdaki alt bölümlerde açıklanan özellikleri gerektiği gibi açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanın.

### <a name="the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimi

Bu konu, bu başlıkta açıklanan birincil özelliktir. Üretim katı yürütme arabirimini sisteminize ekler. Etkinleştirmek için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özellikleri açın:

- Üretim katı yürütmesi

### <a name="generate-license-plates"></a>Plaka oluşturma

Bu özellikler, üretim katı yürütme arabiriminin plaka işlevlerini kullanılabilir hale getirir. Bu özelliği kullanmak istiyorsanız [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası
1. İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin

### <a name="print-labels"></a>Etiket yazdır

Bu özellikler, üretim katı yürütme arabiriminin etiket yazdırma işlevlerini kullanılabilir hale getirir. Bu özelliği kullanmak istiyorsanız [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası
1. İş Kartı Cihazından etiket yazdır

### <a name="allow-locking-the-touch-screen"></a>Dokunmatik ekranın kilitlenmesini sağla

Bu özellik, çalışanların dokunmatik ekranı hijyenik hale getirmesini sağlayan üretim katı yürütme arabirimine bir düğme ekler. Kullanmak için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özellikleri açın:

- Temizlenebilmeleri için iş kartı cihazını ve iş kartı terminalini kilitleme özelliği

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimi için varlık yönetim işlevi

Bu özellik, üretim tabanı yürütme arabirimine bir kıymet yönetimi sekmesi ekler. Çalışanlar bu sekmeyi, iş listesinin seçili filtresinde bulunan makine kaynağına bağlı bir kıymeti seçmek için kullanabilir. Çalışan, seçili makine kıymeti için en fazla dört seçili sayaçtaki sayaç değerlerinden kıymetin durumunu ve sistem durumunu görebilir. Bu özelliği kullanmak için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özelliği açın:

- Üretim katı yürütme arabirimi için varlık yönetim işlevi

### <a name="enable-job-search"></a>İş aramasını etkinleştir

Bu özellik, iş listesine bir arama alanı eklemeyi mümkün kılar. Çalışanlar iş kimliği girerek belirli bir iş bulabilir veya sipariş kimliği girerek belirli bir sipariş için tüm işleri bulabilirler. Çalışanlar kimliği tuş takımı kullanarak veya barkod tarayarak girebilir. Kullanmak için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) bulunan şu özellikleri açın:

- Üretim katı yürütme arabiriminde iş arama

### <a name="enable-reporting-on-co-products-and-by-products"></a>Ortak ürünlerde ve yan ürünlerde raporlamayı etkinleştir

Bu özellik, çalışanların toplu iş emirleriyle ilgili ilerlemeyi bildirmek için üretim tabanı yürütme arabirimini kullanmasına olanak tanır. Bu raporlama, ortak ürünlerde ve yan ürünlerde raporlamayı içerir. Bu özelliği kullanmak getirmek için, [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin:

- Üretim katı yürütme arabiriminden ortak ve yan ürünler raporu

## <a name="work-with-production-floor-execution-configurations"></a>Üretim katı yürütme arabirimi yapılandırmalarıyla çalışma

Cihaz konfigürasyonları oluşturmak ve sürdürmek için, **Üretim denetimi \> Kurulum \>Üretim yürütme \> Üretim katı yürütmesini yapılandır**'a gidin. **Üretim katı yürütmesini konfigüre et** sayfası mevcut konfigürasyonların bir listesini gösterir. Bu sayfada aşağıdaki eylemleri gerçekleştirebilirsiniz:

- Görüntülemek ve düzenlemek için sol sütunda listelenmiş üretim katı yapılandırmasını seçin.
- Listeye yeni bir aygıt konfigürasyonu eklemek Için eylem bölmesinde **yeni** 'yi seçin. Yeni Yapılandırmayı tanımlamanıza yardımcı olacak bir adı **yapılandırma** alanına girin. Buraya girdiğiniz ad, tüm cihaz yapılandırmaları arasında benzersiz olmalıdır ve daha sonra düzenleyemeyeceksiniz.

Sonra, seçili cihaz konfigürasyonuyla ilgili çeşitli ayarları yapılandırın. Aşağıdaki alanlar kullanılabilir:

- **Yalnızca giriş ve çıkış saati** - Yalnızca giriş ve çıkış işlevselliği sağlayan basitleştirilmiş bir arabirim oluşturmak için bu seçeneği *Evet* olarak ayarlayın. Bu, bu sayfadaki diğer seçeneklerin çoğunu devre dışı bırakır. Bu seçeneği etkinleştirmeden önce **Sekme seçimi** hızlı sekmesindeki tüm satırları kaldırmanız gerekir.
- **Aramayı etkinleştir** - İş listesine bir arama alanı eklemek için bu seçeneği *Evet* olarak ayarlayın. Çalışanlar iş kimliği girerek belirli bir iş bulabilir veya sipariş kimliği girerek belirli bir sipariş için tüm işleri bulabilirler. Çalışanlar kimliği tuş takımı kullanarak veya barkod tarayarak girebilir.
- **Çıkış saatindeki rapor miktarı:** çalışanların çıkış yaparken sürmekte olan işler hakkında geribildirim raporlamalarını istemek için bunu *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar uyarılmayacaktır.
- **Çalışanı kilitle**: Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar kayıt yapıldıktan hemen sonra (yeni bir iş gibi) oturumları kapatılır. Cihaz daha sonra oturum açma sayfasına geri dönecektir. Bu seçenek *Evet* olarak ayarlandığında, çalışanlar iş kartı cihazında oturum açmış durumda kalır. Ancak, bir çalışan, iş kartı cihazı aynı sistem kullanıcı hesabı altında çalışmaya devam ederken başka bir çalışanın oturum açmasını sağlayacak şekilde el ile oturumunu kapatabilir. Bu hesap türleri hakkında daha fazla bilgi için, [atanan kullanıcılar](config-job-card-device.md#assigned-users)'a bakın.
- **Kaydın gerçek zamanını kullan**: Her yeni kaydın bir çalışan tarafından gönderildiği tam zamana eşit olması için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlandığında, bunun yerine oturum açma zamanı kullanılır. Genellikle, **çalışanı kilitle** ve/veya **Tek çalışan** seçeneklerini çalışanların daha uzun süreler boyunca oturum açmış durumda kaldığı durumlarda *Evet* olarak işaretlediyseniz bu seçeneği *Evet* olarak ayarlamak isteyeceksiniz.
- **Tek çalışan**: Bu yapılandırmanın etkin olduğu her iş kartı aygıtını yalnızca bir alt kullanıyorsa, bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Evet* olarak ayarlandığında **çalışanı kilitle** seçeneği otomatik olarak *Evet*'e ayarlanır. Ek olarak, bu ayar işçi için bir rozet kimliği (veya benzer kimlik) kullanarak oturum açabilme gereksinimi (ve yeteneğini) kaldırır. Bunun yerine çalışan, bir *saatine kayıtlı çalışana* bağlı sistem kullanıcı hesabı kullanarak (*çalışanlar* tablosundan) Microsoft Dynamics 365 Supply Chain Management'ta oturum açar ve iş kartı cihazında aynı anda o çalışanla oturum açar.
- **Dokunmatik ekranı kilitlemeye izin ver**: Çalışanların iş kartı cihazı dokunmatik ekran seçeneklerini bu şekilde kilitlemesine izin vererek ekranı temizlemelerini sağlamak için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Evet* olarak ayarlandığında, cihaz oturum açma sayfasına **Temizlemek için ekranı kilitle** düğmesi eklenir. Bir çalışan bu düğmeyi seçtiğinde, dokunmatik ekran, istenmeyen giriş yapılmasını önlemek için geçici olarak kilitlenir. Ayrıca, geri sayım süreölçeri de görüntülenir. Çalışan daha sonra cihazı ve ekranı güvenle temizleyebilir. Geri sayım tamamlandığında, dokunmatik ekran otomatik olarak yeniden kilidi açar.
- **Ekran kilitleme süresi**: **Dokunmatik ekranı kilitlemeye izin ver** seçeneği *Evet* olarak ayarlandığında, bu seçeneği kullanın ve dokunmatik ekranın temizleme amacıyla kilitlenmesi gereken saniye sayısını belirtin. Süre 5 ile 120 saniye arasında olmalıdır.
- **Lisans levhasını oluştur**: Bir çalışanın bir iş kartı cihazını her kullandığında tamamlandı bildirimi oluşturmak için bu seçeneği *Evet* olarak ayarlayın. Lisans levhası numarası, **Ambar yönetimi parametreleri** sayfasında ayarlanmış bir numara serisinden oluşturulur. Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar tamamlandı bildirimine göre, varolan bir lisans levhası belirtmelidir.
- **Etiket Yazdır**: Bir çalışan bir çalışma tamamlandı bildirimi yapmak için iş kartı aygıtını kullandığında, bu seçeneği *Evet* olarak ayarlayın. Etiketin konfigürasyonu belge yönlendirmesinde, [Lisans plak etiketlerinin belge yönlendirme](../warehousing/document-routing-layout-for-license-plates.md) düzeninde açıklandığı gibi ayarlanır.
- **Sekme seçimi**: Geçerli yapılandırma etkin olduğunda, üretim katı yürütme arabirimi tarafından hangi sekmelerin görüntüleneceğini seçmek için bu bölümdeki ayarları kullanın. İstediğiniz kadar sekme tasarlayabilir ve gerekirse bunları gerektiği gibi ekleyip düzenleyebilirsiniz. Sekmelerin nasıl tasarlanacağı ve buradaki ayarlarla nasıl çalışılacağı hakkında ayrıntılı bilgi için bkz. [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>İş konfigürasyonlarını temizle

Atölye gözetmeni, üretim katıyürütme arabirimini ayarladığında, bir konfigürasyon ve bir iş filtresi seçer. Bu seçimler, Supply Chain Management'ta bir referans tablosunda depolanır ve tarayıcı, bu tabloda doğru satırı bulmak için yerel bir çerezde depolanan bir kimliği kullanır. Tablo ayrıca, bir çalışanın her cihazda en son oturum açtığı tarih ve saati de günlüğe kaydeder.

Son 60 gün içinde herhangi bir faaliyet kaydetmemiş olan cihazlar için, bir toplu iş, referanslar tablosundaki girişleri belirli aralıklarla temizler. Bu adımları izleyerek, istediğiniz zaman girişleri el ile de temizleyebilirsiniz.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.
1. Eylem bölmesinde, **İstemci yapılandırmalarını temizle**'yi seçin.
1. **İstemci yapılandırmasını Temizle** iletişim kutusunda **gün sayısı** alanını, dikkate alınacak etkin olmama gün sayısına (bugünün tarihinden önce) ayarlayın. Bu süre içinde etkin olmayan cihazlar için tüm yapılandırmaları ve oturum açma kayıtlarını kaldırırsınız.
1. **Gün sayısı** ayarını temel alarak ilgili konfigürasyonları temizlemek için **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
