---
title: Ambar uygulaması aracılığıyla plaka teslim alma
description: Bu konu, fiziksel stoku almak için bir plaka teslim alma işlemi kullanmayı desteklemek üzere ambar uygulamasının nasıl ayarlanacağını açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0d6894c0adb5671818e976dbb5116ecb947025d2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439681"
---
# <a name="license-plate-receiving-via-the-warehouse-app"></a>Ambar uygulaması aracılığıyla plaka teslim alma

[!include [banner](../includes/banner.md)]

Bu konu, fiziksel stoku almak için bir plaka teslim alma işlemi kullanmayı destekleyecek şekilde ambar uygulamasının nasıl ayarlanacağını açıklamaktadır.

Bu işlevi, bir ön sevkiyat bildirimi (ÖSB) ile ilgili gelen stoğun girişini hızlı bir şekilde kaydetmek için kullanabilirsiniz. Ambar yönetim işlemleri transfer emri sevk etmek için kullanıldığında, sistem otomatik olarak bir ÖSB oluşturur. Satınalma siparişi işlemi için, ÖSB el ile kaydedilebilir veya bir gelen ÖSB veri varlığı işlemi kullanılarak otomatik olarak içe aktarılabilir.

ÖSB verileri, paletlerin (ana plakalar) kutular içerebildiği (iç içe geçmiş plakalar) *paketleme yapıları* aracılığıyla yüklere ve sevkiyatlara bağlıdır.

> [!NOTE]
> İç içe geçmiş plakalara sahip paketleme yapıları kullanıldığında, stok hareketlerinin sayısını azaltmak için sistem ana plakadaki fiziksel eldeki stoku kaydeder. Fiziksel eldeki stoğun hareketinin ana plakadan iç içe geçmiş plakalara taşınmasını tetiklemek için, paketleme yapısı verilerine göre, mobil cihazın *İçe içe geçmiş plakalara paketle* işi oluşturma işlemini temel alan bir menü öğesi sağlaması gerekir.

## <a name="warehousing-mobile-device-app-processing"></a>Ambarlama mobil cihaz uygulaması işlemi

Bir çalışan gelen lisans plakası numarasını taradığında, sistem lisans tabakası alma işlemini başlatır. Bu bilgileri temel alarak, lisans kalıbının içeriği (ÖSB'den gelen veriler), gelen yerleştirme konumuna fiziksel olarak kaydedilir. Takip eden akışlar iş süreci gereksinimlerinizi temel alır.

## <a name="work-policies"></a>İş ilkeleri

Olduğu gibi, (örneğin) *tamamlandı bildirimi* mobil cihaz menüsü menü öğesi işlemi ile, lisans levhası işlemi tanımlanan kurulumu temel alan birkaç iş akışını destekler.

### <a name="work-policies-with-work-creation"></a>İş oluşturma ile iş ilkeleri

İş oluşturan bir iş ilkesi kullanarak gelen maddeleri kaydettiğinizde, sistem her kayıt için yerine koyma çalışma kayıtları oluşturur ve kaydeder. *Lisans levhası teslim alma ve çalışma sürecini yerine koyma* işlemini kullanırsanız, kayıt ve yerine koyma işlemleri tek bir mobil aygıt menü öğesi kullanılarak tek bir işlem olarak gerçekleştirilir. *Lisans levhası alma* işlemini kullanırsanız, alma ve yerine koyma süreçleri, her biri kendi mobil aygıt menü öğesi olan iki farklı ambar operasyonu olarak işlenir.

### <a name="work-policies-without-work-creation"></a>İş oluşturma olmadan iş ilkeleri

Lisans levhası alma sürecini iş oluşturmadan kullanabilirsiniz. *Transfer alış irsaliyesi* ve/veya *satınalma siparişleri* iş emri türüne sahip iş ilkelerini tanımlarsanız ve *Lisans levhası alma (ve yerine koyma)* için Işlemi kullanıyorsanız , aşağıdaki iki ambar mobil uygulama işlemi iş oluşturmaz. Bunun yerine, yalnızca gelen teslim noktası içindeki lisans kalıbına gelen fiziksel stoku kaydetmeleri gerekir.

- *Plaka teslim alma*
- *Plaka alma ve yerine koyma*

> [!NOTE]
> - **Stok yerleşimleri** bölümünde iş ilkesi için en az bir konum tanımlamanız gerekir. Birden fazla iş ilkesi için aynı konumu belirtemezsiniz.
> - Ambar mobil cihaz menüsü öğelerinin **yazdırma etiketi** seçeneği, iş oluşturma olmadan bir lisans levhası etiketi yazdırmayacaktır.

Bu işlevselliğin sisteminizde kullanılabilmesini sağlamak için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *lisans levhası alma yenilikleri* özelliğini etkinleştirmelisiniz.

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Lisans levhalarını izlememeyen bir konumda sayım alma

**Kullanım lisansı levha izleme** açık değilse bile bir yerleşim profiline atanan ambar konumu kullanılabilir. Bu nedenle, stok aldığınızda, eldeki stoku iş oluşturma yapılmadan bir konuma doğrudan kaydedebilirsiniz.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Bir ambardaki her alan konumu için mobil cihaz menü öğeleri ekle

*Lisans tabakasını alma geliştirmeleri* özelliği, ambar mobil uygulamaya yerleşime özel lisans levhası alıcı (ve yerine koyma) menü öğeleri ekleyerek bir ambardaki herhangi bir konumu almanıza olanak tanır. Daha önce sistem, yalnızca her ambar için tanımlanan varsayılan konumda almayı destekler. Ancak, bu özellik açık olduğunda, lisans levhası (ve yerine koyma) için mobil cihaz menüsü öğeleri şimdi, her bir menü öğesi için özel bir "to" konumu seçmenizi sağlayan **varsayılan verileri kullan** seçeneğini sağlar. (Bu seçenek bazı menü öğesi türleri için zaten kullanılabilir.)

Bu işlevselliğin sisteminizde kullanılabilmesini sağlamak için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *lisans levhası alma yenilikleri* özelliğini etkinleştirmelisiniz.

## <a name="show-or-skip-the-receiving-summary-page"></a>Teslim alma özet sayfasını gösterme veya atlama

*Mobil cihazlarda teslim alma özet sayfası görüntülenip görüntülenmeyeceğni denetle* özelliğini, plaka teslim alma işleminin bir parçası olarak ek bir ayrıntılı Ambarlama uygulaması akışından yararlanmak üzere kullanabilirsiniz.

Bu özellik etkinleştirildiğinde, plaka teslim alma veya plaka teslim alma ve yerine koyma için mobil cihaz menüsü öğeleri bir **Teslim alma özeti sayfası görüntüle** ayarı sağlar. Bu ayar aşağıdaki seçeneklere sahiptir:

- **Ayrıntılı özet görüntüle** - Plaka teslim alma sırasında çalışanlar tam ÖSB bilgilerini gösteren ek bir sayfa görürler.
- **Özeti atla** – Çalışanlar tüm ÖSB bilgilerini göremez. Ambar çalışanları da bir değerlendirme kodu ayarlayamaz veya teslim alma işlemi sırasında özel durumlar ekleyemez.

Bu işlevselliği sisteminizde kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *mobil cihazlar özelliğinde alıcı özet sayfasının görüntülenip görüntülenmemesini* açmanız gerekir.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme

Bir ÖSB zaten varolan plaka kimliği içeriyorsa ve plaka kaydının oluştuğu ambar yerleşimden başka bir ambar yerleşimindeki eldeki fiziksel stok verilerine sahipse, plaka teslim alma işlemi kullanılamaz.

Transit ambarının plakaları izlemediği (ve bu nedenle her plaka için fiziksel eldeki stoğu izlemediği) transfer emri senaryoları için, transitteki plakaların fiziksel eldeki stoklarının güncelleştirilmesini önlemek için *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelle* özelliğini kullanabilirsiniz.

Bu işlevi sisteminizde kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *hedef ambar özelliğinden farklı olan transfer emrinin sevk edilmiş lisans levhalarını etkinleştirmeniz gerekir*.

Bu özellik kullanılabilir olduğunda işlevselliği yönetmek için, aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde **Plakalar** hızlı sekmesinde, **Transit ambarı plaka ilkesi** alanını aşağıdaki değerlerden birine ayarlayın:

    - **İzlenemeyen plakanın yeniden kullanılmasına izin ver** – Sistem, *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme* özelliğinin kullanılabilir olmadığı durumlardaki gibi çalışır. Bu değer, özelliği ilk etkinleştirdiğinizde varsayılan ayardır.
    - **İzlenmeyen plakanın yeniden kullanılmasını engelle** – Transfer emri alınana kadar hedef ambarda, yalnızca sevk edilen plakayla ilgili olan eldeki stok güncelleştirmelerine izin verilir.

## <a name="more-information"></a>Daha fazla bilgi

Mobil cihaz menü öğeleri hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).

*Tamamlandı bildirimi* üretim senaryosu hakkında daha fazla bilgi için [Ambar iş ilkelerine genel bakış](warehouse-work-policies.md)'a bakın.

Giriş yük yönetimi hakkında daha fazla bilgi için bkz. [Satınalma siparişleri için gelen yüklerin ambarda işlenmesi.](inbound-load-handling.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]