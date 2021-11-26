---
title: Manuel stok hareketinin ertelenmiş işlemesi
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta manuel stok hareketinin ertelenmiş işlemesinin nasıl kullanılacağını açıklamaktadır.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f5c9ba7079895feeb0c171f2021479587aa13cc9
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777678"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Manuel stok hareketinin ertelenmiş işlemesi

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta manuel stok hareketinin ertelenmiş işlemesinin nasıl kullanılacağını açıklamaktadır.

Ertelenmiş işleme, yerleştirme işlemi arka planda işlenirken ambar işçilerinin başka işler yapmaya devam etmesini sağlar. Ertelenmiş işleme sunucu işlem zamanında geçici veya planlanmamış artışlara olduğunda ve artan işlem süresi çalışan verimliliğini etkilediğinde faydalıdır. Bu özelliğin desteklediği iş türleri kümesine *Stok hareketi* iş türü de eklenmiştir.

Arka planda işleme, [İşlem ambarı uygulama olayları özelliği](warehouse-app-events.md) kullanılarak sağlanır.

## <a name="turn-on-this-feature-for-your-system"></a>Sisteminiz için bu özelliği etkinleştirme

Bu özellikleri kullanılabilir hale getirmek için, [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin. Bu özellikleri şu sırada etkinleştirmeniz gerekir:

1. Kuruluş genelinde iş durdurma (Supply Chain Management sürüm 10.0.21 itibariyle bu özellik zorunludur; bu nedenle varsayılan olarak açıktır ve yeniden kapatılamaz.)
1. Ambar uygulaması olaylarını işle
1. Ertelenen yerine koyma işlemleri
1. El ile stok hareketi işlemini ertelenmiş olarak işleme

## <a name="configure-the-work-processing-policies"></a>İş işleme ilkelerini yapılandırma

Ertelenmiş işlemeyi kullanmak için, bir iş işleme ilkesini kurmalı ve kullanmalısınız. Ertelenmiş işleme için [Ambar çalışması özelliğinin ertelenmiş işlemesi](deferred-put.md) şu iş türlerini destekler: *Satış siparişi*, *Transfer emri çıkışı* ve *Stok yenileme*. *Manuel stok hareketinin ertelenmiş işlemesi* özellikleri yeni bir iş türü ekler: *Stok hareketi*.

İş işleme ilkesi ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> İş \> İş işleme ilkeleri**'ne gidin.
1. Listeden mevcut bir ilkeyi seçin veya Eylem Bölmesi'nde **Yeni**'yi seçerek yeni bir ilke oluşturun. İlkelerin başlıklarında aşağıdaki alanlar yer alır:

    - **İş işleme ilkesi adı** – İş işleme ilkesinin adı.
    - **Açıklama** – İş işleme ilkesinin açıklaması.

1. **İşlem kuralları** hızlı sekmesinde, ilkenin uygulanacağı kurallar koleksiyonunu ayarlayın. Kuralları istediğiniz gibi eklemek veya kaldırmak için araç çubuğundaki düğmeleri kullanın. Her kural için aşağıdaki alanları ayarlayın:

    - **İş emri türü** – İlkenin uygulanacağı iş türünü seçin.
    - **İşlem** – İlkenin işlemek için kullanacağı işlemi seçin. **İş emri türü** alanında *Stok hareketi*'ni seçtiyseniz, çekme işlemleri ve yerleştirme işlemleri tek bir olay olarak işlendiğinden, bu alanı ayarlamanız gerekmez.
    - **İş işleme yöntemi** – İş satırını işlemek için kullanılan yöntemi seçin. *Anlık* seçeneğini belirlediyseniz davranış, satırı işlemek için herhangi bir iş işleme ilkesi seçilmediğinde gösterilen davranışa benzer. *Ertelenmiş*'i seçerseniz, sistem toplu iş çerçevesini kullanan ertelenmiş işlemeyi uygular.
    - **Ertelenmiş işlem eşiği** – Bu alanı *0* (sıfır) olarak ayarlarsanız eşik olmaz. Bu durumda, *Ertelenmiş* işlem yöntemi kullanılabiliyorsa kullanılır. Belirli bir eşik hesaplaması eşiğin altındaysa, *Anlık* yöntem kullanılır. Aksi takdirde, *Ertelenmiş* yöntem kullanılabiliyorsa kullanılır. Satış ve transfer ile ilgili işler için eşik, iş için işlenen ilişkili kaynak yük hattı sayısı olarak hesaplanır. Stok yenileme çalışması için, eşik iş tarafından yenilenmekte olan iş satırlarının sayısı olarak hesaplanır. Örneğin, *5* eşiğini ayarlayarak, beşten az başlangıç kaynağı yükleme hattına sahip daha küçük işler ertelenmiş işlemeyi kullanmaz, ancak daha büyük işler onu kullanır. Yalnızca **iş işleme yöntemi** *Ertelenmiş* olarak ayarlanmışsa eşiğin etkisi vardır.
    - **Ertelenmiş toplu iş grubu işlemi** – İşlenmek için kullanılan toplu iş grubunu belirtin. **İş emri türü** alanında *Stok hareketi*'ni seçtiyseniz, toplu iş grubu **İşlem ambarı uygulama olayları** iletişim kutusunda seçildiğinden, bu alanı ayarlamanız gerekmez.

## <a name="assign-the-work-creation-policy"></a>İş oluşturma ilkesini atama

İş oluşturma ilkesi atama hakkında ayrıntılar için bkz [Ambar işinin ertelenmiş işlemesi](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Ambar uygulaması olaylarını işlemek için bir toplu iş ayarlayın

*Manuel stok hareketi işleminin ertelenmiş işlemesi* işlemini kullanmak için zamanlanmış bir toplu iş ayarlayın.

1. **Ambar yönetimi \> Periyodik görevler \> Ambar uygulaması olaylarını işle**'ye gidin.
1. **Ambar uygulama olaylarını işle** iletişim kutusunda **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** seçeneğini *Evet* olarak ayarlayın.
1. **Tekrar**'ı seçin ve işletmenizin gereksinimlerini karşılayan bir çalışma zamanlaması ayarlayın.
1. Tüm iletişim kutularında **Tamam**'ı seçin.

## <a name="inquire-about-the-warehouse-app-events"></a>Ambar uygulaması olayları hakkında sorgulama

Ambar uygulamasının oluşturduğu olay kuyruğunu ve olay iletilerini **Ambar yönetimi \> Sorgular ve raporlar \> Mobil cihaz günlükleri \> Ambar uygulaması olayları**'na giderek görüntüleyebilirsiniz.

*Stok hareketi* olay iletileri, ilk oluşturuldukları *Kuyruğa alındı* durumuna sahip olur. Bu durum, **Ambar uygulaması olaylarını işle** toplu işinin olay iletilerini çekeceği ve bunları işleyeceği anlamına gelir. Durum *Tamamlandı* olarak güncelleştirildiğinde, ilgili tüm olaylar kuyruktan silinir.

Tüm *Stok hareketi* olayları, olay türü ve ambar başına tek bir koleksiyon altında toplanır.

Toplu iş, **Ambar uygulaması olaylarını işle** iletişim kutusunda ayarlanan tekrara göre ambar uygulama olaylarını işler. Bu nedenle, bir ileti işlenene kadar **Tanımlayıcı** alanına bakarak ambar kodunu bulabilirsiniz.

İletinin ayrıntıları, hareket ayrıntılarını içerir (örneğin, "gönderilen" ve "alıcı" konumlar).

Daha fazla bilgi için bkz. [Ambar uygulaması olayı işleme](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Ertelenmiş işleme ilkesini atlamak için mobil aygıt menüsünü yapılandırma

Mobil cihaz menüsünü ertelenmiş işlem ilkesini atlayacak şekilde yapılandırma ile ilgili ayrıntılar için bkz [Ambar işinin ertelenmiş işlemesi](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Kapalı iş tarihlerine etki

Kapatılan çalışma tarihlerinde oluşan etki hakkında ayrıntılı bilgi için bkz. [Ambar işinin ertelenmiş işlemesi](deferred-put.md).

## <a name="additional-resources"></a>Ek kaynaklar

- [Ambar işi için ertelenmiş işleme](deferred-put.md)
- [Ambar uygulaması olayı işleme](warehouse-app-events.md)
- [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
