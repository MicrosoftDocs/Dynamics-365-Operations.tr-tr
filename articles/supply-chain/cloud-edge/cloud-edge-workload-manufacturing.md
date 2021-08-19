---
title: Bulut ve uç ölçek birimleri için üretim yürütme iş yükleri
description: Bu konuda, üretim yürütme iş yüklerinin bulut ve edge ölçek birimleri ile nasıl çalıştığı açıklanmaktadır.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 958c7a8853e5ef0d7fb211225796d7808e4e7ae1afaf861cc6746157225c0dbb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721475"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için üretim yürütme iş yükleri

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Üretim yürütme iş yükü şu anda önizlemede sunulmaktadır.
> İş yükü ölçek birimleri kullanıldığında, genel önizlemedeki bazı iş işlevleri tam olarak desteklenmez.

Üretim yürütmede, ölçek birimleri aşağıdaki özellikleri sunar:

- Makine operatörleri ve üretim katı denetçileri operasyonel üretim planına erişebilirler.
- Makine operatörleri, gizli ve süreç üretim işleri çalıştırarak planı güncel tutabilir.
- Üretim katı denetçisi, çalışma planını ayarlayabilir.
- Çalışanlar, doğru çalışan maaşı hesaplamasını sağlamak için kenardan giriş ve çıkış zamanlarına erişebilirsiniz.

Bu konuda, üretim yürütme iş yüklerinin bulut ve edge ölçek birimleri ile nasıl çalıştığı açıklanmaktadır.

## <a name="the-manufacturing-lifecycle"></a>Üretim yaşam döngüsü

Aşağıdaki çizimin gösterdiği gibi, üretim yaşam döngüsü üç aşamaya ayrılmıştır: *Planlama*, *Çalıştırma* ve *Sonuçlandırma*.

[![Tek bir ortam kullanıldığında üretim yürütme aşamaları](media/mes-phases.png "Tek bir ortam kullanıldığında üretim yürütme aşamaları."](media/mes-phases-large.png)

_Planlama_ aşaması; ürün tanımı, planlama, sipariş oluşturma ve zamanlama ile serbest bırakma bilgilerini içerir. Serbest bırakma adımı; _Planlama_ aşamasından _Yürütme_ aşamasına geçişin nasıl yapılacağını gösterir. Bir üretim emri serbest bırakıldığında, üretim emri işleri üretim katında görünür ve yürütülmeye hazırdır.

Bir üretim işi tamamlandı olarak işaretlendiğinde, _Yürütme_ aşamasından _Sonlandırma_ aşamasına kadar hareket eder. _Sonlandırma_ aşamasında, *Yürütme* aşamasındaki kayıtlar hesaplandıkları, onaylandıkları ve transfer edildikleri bir onay iş akışından geçer. Bu noktada, üretim emri tamamlanır. Bu nedenle, çalışanların ödemeleri için temel üretilir.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Yürütme aşamasını ayrı bir iş yüküne bölme

Aşağıdaki çizimin gösterdiği gibi, ölçek birimleri kullanıldığında, _Yürütme_ aşaması ayrı bir iş yükü olarak bölünür.

[![Ölçek birimleri kullanıldığında üretim yürütme aşamaları](media/mes-phases-workloads.png "Ölçek birimleri kullanıldığında üretim yürütme aşamaları."](media/mes-phases-workloads-large.png)

Model şimdi tek örnekli bir yüklemeden hub ve ölçek birimlerine dayalı bir modele geçer. _Planlama_ ve _Sonlandırma_ aşamaları, hub'da arka ofis işlemleri olarak çalışır ve üretim yürütme iş yükü ölçek birimleri üzerinde çalışır. Veriler, hub ve ölçek birimleri arasında zaman uyumsuz olarak aktarılır.

Bir üretim emri hub üzerinde serbest bırakıldığında, üretim işlerini işlemek için gereken tüm veriler ölçek birimine aktarılır. Bu veriler üretim emirlerini, üretim rotalarını, ürün reçetelerini ve ürünleri içerir. Bir üretim emriyle (dolaylı faaliyetler, devamsızlık kodları ve üretim parametreleri gibi) ilgili olmayan veriler de hub'dan ölçek birimine transfer edilir. Kural olarak, hub'dan kaynaklanan ve ölçek birimine aktarılan veriler yalnızca hub'da oluşturulabilir veya güncelleştirilebilir. Örneğin, ölçek biriminde yeni bir devamsızlık kodu veya dolaylı faaliyet oluşturulamaz,&mdash;bunlar yalnızca kayıt için kullanılabilir. Yürütme sırasında ölçek biriminde yapılan kayıtlar, zaman ve katılımcı onayı, stok ve mali güncelleştirmelerin işlendiği hub'a aktarılır.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>İş yükleri üzerinde çalıştırılabilecek üretim yürütme görevleri

Aşağıdaki üretim yürütme görevleri, şu anda iş yükleri üzerinde ölçek birimleri kullanıldığında çalışabilir:

- Giriş, oturum açma, çıkış ve devamsızlık
- İşi başlat
- Paket işleri
- Rapor ilerlemesi
- Iskarta bildir
- Dolaylı faaliyet
- Mola
- Tamamlanıp kaldırıldı olarak bildirme (aynı zamanda ölçeklendirme birimi üzerinde ambar yürütme iş yükünü de çalıştırmanızı gerektirir, aynı zamanda bkz. [Ölçek biriminde tamamlandı ve kaldırıldı olarak bildirme](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Hub'da üretim yürütme iş yükleri ile çalışma

Genellikle, üretim yürütme iş yüklerini çalıştırmak için gereken süreçler, gerektiğinde hub'ı ve tüm ölçek birimlerini eşit tutmak için otomatik olarak çalışır. Ancak sorununuz varsa, iş yüklerinden alınan ham kayıtların işlenmesini el ile tetikleyebilir ve/veya kayıt işleme günlüğünü kontrol edebilirsiniz.

### <a name="manually-process-raw-registrations"></a>Ham kayıtları el ile işleme

İş yüklerinden alınan tüm kayıtları işlemek için Supply Chain Management'ta bir toplu işlem otomatik olarak çalışır. İş yükü üzerinde tamamlanmış bir proje için bir kayıt işlenirken, bu iş gerekli üretim günlüklerini ve günlük defteri girişlerini oluşturur.

İş genellikle otomatik olarak çalışmasına rağmen, hub'da oturum açıp **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Ham kayıtları işleme**'ye giderek istediğiniz zaman el ile çalıştırabilirsiniz.

### <a name="check-the-raw-registration-processing-log"></a>Ham kayıt işlem günlüğünü denetleme

Kayıt işleme günlüğünü gözden geçirmek için hub'da oturum açın ve **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Ham kayıt işleme günlüğü**'ne gidin. **Ham kayıt işleme günlüğü** sayfası, işlenen ham kayıtların bir listesini ve her kaydın durumunu gösterir.

![Ham kayıt işlem günlüğü sayfası.](media/mes-processing-log.png "Ham kayıt işlem günlüğü sayfası")

Listede herhangi bir kayıt seçip Eylem bölmesinden aşağıdaki düğmelerden birini seçerek çalışabilirsiniz:

- **İşle**: Seçilen kaydı el ile işleyin. Bu eylem, _Ham kayıtları işle_ işi çalıştırılmamışsa veya başarısız olduğunda yararlı olabilir.
- **İptal et**: Seçili kaydı iptal edin.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Bir ölçek biriminde üretim yürütme iş yükleri ile çalışma

Genellikle, üretim yürütme iş yüklerini çalıştırmak için gereken süreçler, gerektiğinde hub'ı ve tüm ölçek birimlerini eşit tutmak için otomatik olarak çalışır. Ancak sorun yaşıyorsanız bir ölçek biriminde işlenmiş olan siparişlerin geçmişini denetleyebilir veya _Üretim hub'ından ölçek birimi ileti işleyici_ işini el ile çalıştırabilirsiniz.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Bir ölçek biriminde işlenmiş olan üretim işlerinin geçmişini görüntüleme

Bir ölçek biriminde işlenmiş olan üretim işlerinin geçmişini gözden geçirmek için ölçek birimi makinesinde oturum açın ve **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Üretim işleri işlem geçmişi**'ne gidin. **Üretim işleri işleme geçmişi** sayfası, ölçek birimindeki üretim emirlerinin işlem geçmişini gösterir. Listeden herhangi bir üretim emri seçip Eylem bölmesinden aşağıdaki düğmelerden birini seçerek çalışabilirsiniz:

- **İşle**: Seçilen üretim emrini el ile işleyin.
- **İptal et**: Seçilen üretim emrini iptal edin.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Üretim hub'ından ölçek birimine ileti işleyici işi

_Üretim hub'ından ölçek birimine ileti işleyicisi_ işi, hub'dan ölçek birimine giden verileri işler. Üretim yürütme iş yükü dağıtıldığında bu iş otomatik olarak başlatılır. Bununla birlikte, **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Üretim hub'ından ölçek birimine ileti işleyici**'ye giderek istediğiniz zaman el ile çalıştırabilirsiniz.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Ölçek biriminde tamamlandı ve kaldırıldı olarak bildirme

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

Geçerli sürümde, tamamlandı ve kaldırıldı olarak bildirme işlemleri (tamamlanmış ürünler, ortak ürünler ve yan ürünler için), [ambar yürütme iş yükü ](cloud-edge-workload-warehousing.md) (üretim yürütme iş yükü değil) tarafından desteklenir. Bu nedenle, bu işlevi bir ölçek birimine bağlıyken kullanmak için aşağıdakileri yapmalısınız:

- Hem ambar yürütme iş yükünü hem de üretim yürütme iş yükünü ölçeklendirme biriminize yükleyin.
- Tamamlandı olarak bildirmek ve kaldırma çalışmasını işlemek için Warehouse Management mobil uygulamasını kullanın. Üretim katı yürütme arabirimi, şu anda bu işlemleri desteklememektedir.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
