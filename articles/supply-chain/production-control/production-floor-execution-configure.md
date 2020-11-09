---
title: Üretim katı yürütme arabirimini yapılandırma
description: Bu konu, üretim katı yürütme arabirimi için bir veya daha fazla konfigürasyon oluşturmayı açıklamaktadır. Üretim katı yürütme arabirimini açtığınızda, seçilen bir konfigürasyon ve tarayıcıya ve cihaza özel iş filtresini otomatik olarak yükler. Konfigürasyonda, belirli bir kullanım için geçerli olması gereken ilkeleri ayarlayabilirsiniz.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cf58a7d851577854d08bad70cff69794c3841a2d
ms.sourcegitcommit: 9dd2d38e76d4d93171315ec319e6ce7d51d4e6c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2020
ms.locfileid: "4012516"
---
# <a name="configure-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini yapılandırma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Atölye çalışanları işlerin başlatılması, işlere ilişkin geri bildirim bildirmek, dolaylı faaliyetleri kaydetmek ve devamsızlığı bildirmek gibi günlük çalışmalarını kaydetmek için üretim katı yürütme arabirimini kullanır. Bu kayıtlar, ilerlemeyi izlemenin ve üretim emirleriyle ilgili maliyetin temelini oluşturur ve çalışanların ödemesine yönelik temel hesaplama içindir.

Üretim katı yürütme arabirimini açtığınızda, seçilen bir konfigürasyon ve tarayıcıya ve cihaza özel iş filtresini otomatik olarak yükler. Konfigürasyonda, belirli bir kullanım için geçerli olması gereken ilkeleri ayarlayabilirsiniz. Burada bazı kullanım örnekleri verilmiştir:

- Şirket salonundaki bir cihazda, çalışanlar ofise geldiği sırada girişleri ve çıkarken çıkışları kaydedilir.
- Atölye katındaki bir cihazda, makine operatörleri işleri başlatıp bitirdikleri saati kaydeder. Ayrıca, molalar ve dolaylı faaliyetleri de kaydederler.

Bu konu, iş kartı aygıtını konfigüre etmek için çeşitli seçenekleri açıklamaktadır.

## <a name="turn-on-new-features-in-feature-management"></a>Özellik yönetiminde yeni özellikleri etkinleştir

Bu konuda açıklanan ayarlardan birkaçı sisteminizde kullanılabilmesi için etkin olmalıdır. Aşağıdaki özelliklerin herhangi birini veya tümünü gerekli şekilde etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanın.

### <a name="generate-license-plate"></a>Plaka oluştur

Bu özelliği kullanılabilir hale getirmek için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası
1. İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin

### <a name="print-label"></a>Etiket yazdır

Bu özelliği kullanılabilir hale getirmek için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):

1. İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası
1. İş Kartı Cihazından etiket yazdır

### <a name="allow-locking-the-touch-screen"></a>Dokunmatik ekranın kilitlenmesini sağla

Bu özelliği kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin:

- (Önizleme) Temizlenebilmeleri için iş kartı cihazını ve iş kartı terminalini kilitleme özelliği

## <a name="work-with-production-floor-execution-configurations"></a>Üretim katı yürütme arabirimi yapılandırmalarıyla çalışma

Cihaz konfigürasyonları oluşturmak ve sürdürmek için, **Üretim denetimi \> Kurulum \>Üretim yürütme \> Üretim katı yürütmesini yapılandır** 'a gidin. **Üretim katı yürütmesini konfigüre et** sayfası mevcut konfigürasyonların bir listesini gösterir. Bu sayfada aşağıdaki eylemleri gerçekleştirebilirsiniz:

- Görüntülemek ve düzenlemek için sol sütunda listelenmiş üretim katı yapılandırmasını seçin.
- Listeye yeni bir aygıt konfigürasyonu eklemek Için eylem bölmesinde **yeni** 'yi seçin. Yeni Yapılandırmayı tanımlamanıza yardımcı olacak bir adı **yapılandırma** alanına girin. Buraya girdiğiniz ad, tüm cihaz yapılandırmaları arasında benzersiz olmalıdır ve daha sonra düzenleyemeyeceksiniz.

Sonra, seçili cihaz konfigürasyonuyla ilgili çeşitli ayarları yapılandırın. Aşağıdaki alanlar kullanılabilir:

- **Çıkış saatindeki rapor miktarı:** çalışanların çıkış yaparken sürmekte olan işler hakkında geribildirim raporlamalarını istemek için bunu *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar uyarılmayacaktır.
- **Çalışanı kilitle** : Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar kayıt yapıldıktan hemen sonra (yeni bir iş gibi) oturumları kapatılır. Cihaz daha sonra oturum açma sayfasına geri dönecektir. Bu seçenek *Evet* olarak ayarlandığında, çalışanlar iş kartı cihazında oturum açmış durumda kalır. Ancak, bir çalışan, iş kartı cihazı aynı sistem kullanıcı hesabı altında çalışmaya devam ederken başka bir çalışanın oturum açmasını sağlayacak şekilde el ile oturumunu kapatabilir. Bu hesap türleri hakkında daha fazla bilgi için, [atanan kullanıcılar](config-job-card-device.md#assigned-users)'a bakın.
- **Kaydın gerçek zamanını kullan** : Her yeni kaydın bir çalışan tarafından gönderildiği tam zamana eşit olması için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlandığında, bunun yerine oturum açma zamanı kullanılır. Genellikle, **çalışanı kilitle** ve/veya **Tek çalışan** seçeneklerini çalışanların daha uzun süreler boyunca oturum açmış durumda kaldığı durumlarda *Evet* olarak işaretlediyseniz bu seçeneği *Evet* olarak ayarlamak isteyeceksiniz.
- **Tek çalışan** : Bu yapılandırmanın etkin olduğu her iş kartı aygıtını yalnızca bir alt kullanıyorsa, bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Evet* olarak ayarlandığında **çalışanı kilitle** seçeneği otomatik olarak *Evet* 'e ayarlanır. Ek olarak, bu ayar işçi için bir rozet kimliği (veya benzer kimlik) kullanarak oturum açabilme gereksinimi (ve yeteneğini) kaldırır. Bunun yerine çalışan, bir *saatine kayıtlı çalışana* bağlı sistem kullanıcı hesabı kullanarak ( *çalışanlar* tablosundan) Microsoft Dynamics 365 Supply Chain Management'ta oturum açar ve iş kartı cihazında aynı anda o çalışanla oturum açar.
- **Dokunmatik ekranı kilitlemeye izin ver** : Çalışanların iş kartı cihazı dokunmatik ekran seçeneklerini bu şekilde kilitlemesine izin vererek ekranı temizlemelerini sağlamak için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Evet* olarak ayarlandığında, cihaz oturum açma sayfasına **Temizlemek için ekranı kilitle** düğmesi eklenir. Bir çalışan bu düğmeyi seçtiğinde, dokunmatik ekran, istenmeyen giriş yapılmasını önlemek için geçici olarak kilitlenir. Ayrıca, geri sayım süreölçeri de görüntülenir. Çalışan daha sonra cihazı ve ekranı güvenle temizleyebilir. Geri sayım tamamlandığında, dokunmatik ekran otomatik olarak yeniden kilidi açar.
- **Ekran kilitleme süresi** : **Dokunmatik ekranı kilitlemeye izin ver** seçeneği *Evet* olarak ayarlandığında, bu seçeneği kullanın ve dokunmatik ekranın temizleme amacıyla kilitlenmesi gereken saniye sayısını belirtin. Süre 5 ile 120 saniye arasında olmalıdır.
- **Lisans levhasını oluştur** : Bir çalışanın bir iş kartı cihazını her kullandığında tamamlandı bildirimi oluşturmak için bu seçeneği *Evet* olarak ayarlayın. Lisans levhası numarası, **Ambar yönetimi parametreleri** sayfasında ayarlanmış bir numara serisinden oluşturulur. Bu seçenek *Hayır* olarak ayarlandığında , çalışanlar tamamlandı bildirimine göre, varolan bir lisans levhası belirtmelidir.
- **Etiket Yazdır** : Bir çalışan bir çalışma tamamlandı bildirimi yapmak için iş kartı aygıtını kullandığında, bu seçeneği *Evet* olarak ayarlayın. Etiketin konfigürasyonu belge yönlendirmesinde, [Lisans plak etiketlerinin belge yönlendirme](../warehousing/document-routing-layout-for-license-plates.md) düzeninde açıklandığı gibi ayarlanır.

## <a name="clean-up-job-configurations"></a>İş konfigürasyonlarını temizle

Atölye gözetmeni, üretim katıyürütme arabirimini ayarladığında, bir konfigürasyon ve bir iş filtresi seçer. Bu seçimler, Supply Chain Management'ta bir referans tablosunda depolanır ve tarayıcı, bu tabloda doğru satırı bulmak için yerel bir çerezde depolanan bir kimliği kullanır. Tablo ayrıca, bir çalışanın her cihazda en son oturum açtığı tarih ve saati de günlüğe kaydeder.

Son 60 gün içinde herhangi bir faaliyet kaydetmemiş olan cihazlar için, bir toplu iş, referanslar tablosundaki girişleri belirli aralıklarla temizler. Bu adımları izleyerek, istediğiniz zaman girişleri el ile de temizleyebilirsiniz.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et** 'e gidin.
1. Eylem bölmesinde, **İstemci yapılandırmalarını temizle** 'yi seçin.
1. **İstemci yapılandırmasını Temizle** iletişim kutusunda **gün sayısı** alanını, dikkate alınacak etkin olmama gün sayısına (bugünün tarihinden önce) ayarlayın. Bu süre içinde etkin olmayan cihazlar için tüm yapılandırmaları ve oturum açma kayıtlarını kaldırırsınız.
1. **Gün sayısı** ayarını temel alarak ilgili konfigürasyonları temizlemek için **Tamam** 'ı seçin.
