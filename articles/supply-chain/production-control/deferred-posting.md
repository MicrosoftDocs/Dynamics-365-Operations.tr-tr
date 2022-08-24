---
title: Günlüklere nakletmeden önce tamamlanan malları fiziksel olarak kullanılabilir şeklinde işaretleme
description: Üretilmiş bir madde tamamlandı olarak bildirildiğinde, daha fazla fiziksel işlem için kullanılabilir olarak kaydedilir ve bir veya daha fazla günlük deftere nakledilir. Bu makalede, bir ileti kuyruğundaki bir toplu iş tarafından işlenmelerini sağlayarak günlük deftere nakil işlemlerini nasıl erteleyebileceğiniz açıklanmaktadır.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7a8327552d9e6c38721fdac9ee1795e61f90f329
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266496"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Günlüklere nakletmeden önce tamamlanan malları fiziksel olarak kullanılabilir şeklinde işaretleme

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Bir çalışan üretilmiş bir maddeyi tamamlandı olarak raporladığında, sistem bunu daha fazla fiziksel işleme (örneğin, sevkiyat veya yerine koyma) için kullanılabilir olarak kaydeder. Bu işlem sırasında, bir veya daha fazla günlük deftere nakledilir (tamamlandı günlüğü, malzeme çekme listesi günlüğü ve rota kartı günlüğü olarak rapor). Maddelerinizin tüm deftere nakiller işlenmeden önce fiziksel olarak kullanılabilmesini sağlamak istiyorsanız, sistemi günlük deftere nakil işlemlerini erteleyecek şekilde ayarlayabilirsiniz. Ertelenen deftere nakiller daha sonra, sistem kaynaklarının izin verdiği ölçüde deftere nakilleri işleyecek bir toplu iş tarafından yönetilir.

Aşağıdaki şekil, deftere nakil ertelenmiş ve ertelenmemişken günlük deftere nakil işlemlerinin nasıl çağrılacağını gösterir.

![Günlük deftere nakli ertelenmiş ve ertelenmemişken tamamlandı olarak bildirme işlemi.](media/deferred-posting-flowchart.png "Günlük deftere nakli ertelenmiş ve ertelenmemişken tamamlandı olarak bildirme işlemi")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Sisteminiz için ertelenmiş günlük deftere nakil işlemi özelliğini açma

Ertelenmiş günlük deftere nakil işlemini kullanabilmeniz için sisteminizde bu özelliği etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve özelliği etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. **Özellik yönetimi** çalışma alanında bu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Üretim denetimi*
- **Özellik adı:** *(Önizleme) Günlüklere nakletmeden önce tamamlanan malları fiziksel olarak kullanılabilir şeklinde işaretle*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Tamamlandı bildirimi için günlük deftere nakil seçeneklerini ayarlama

Çalışanlar, aşağıdaki istemcilerden birini kullanarak maddeleri tamamlandı olarak bildirebilir:

- Web istemcisi
- Warehouse Management mobil uygulaması
- Üretim katı yürütme arabirimi

Web istemcisi, Warehouse Management mobil uygulaması ile aynı deftere nakil yöntemi yapılandırmasını kullanır. Ancak, üretim katı yürütme arabiriminin kullandığı deftere nakil yöntemi ayrı olarak yapılandırılmalıdır.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Web istemcisi ve Warehouse Management mobil uygulaması için günlük deftere nakil seçeneklerini ayarlama

Mobil uygulamada çalışanlar, **İş oluşturma işlemi** değerinin *Tamamlandı olarak bildir* veya *Tamamlandı olarak bildir ve yerine koy* olduğu bir mobil aygıt menü öğesini açarak öğeleri tamamlandı olarak bildirir. Web istemcisinde çalışanlar, maddeleri **Tüm üretim emirleri** listesi sayfasından veya **Üretim emri (Ayrıntılar)** sayfasından tamamlandı olarak raporlar. Şirket genelinde varsayılan bir yöntem yapılandırabilir ve aynı zamanda ambara özel geçersiz kılmaları gereksinim duyduğunuz şekilde ayarlayabilirsiniz.

Maddeleri web istemcisinden veya Warehouse Management mobil uygulamasından tamamlandı olarak bildirmek için, şirket genelindeki varsayılan deftere nakil yöntemini yapılandırmak üzere aşağıdaki yordamı kullanın.

1. **Üretim denetimi \> Kurulum \> Üretim denetimi parametreleri** öğesine gidin.
1. **Günlükler** sekmesinde, **Tamamlandı olarak bildirme günlüğü** bölümünde, **Deftere nakil yöntemi** alanını aşağıdaki değerlerden birine ayarlayın:

    - *Anında* – Bir madde tamamlandı olarak bildirildiğinde sistem, tamamlanan maddeyi fiziksel olarak kullanılabilir olarak işaretlemeden önce ilgili tüm günlük deftere nakil işlemlerini tam olarak işler.
    - *Ertelenmiş* – Bir madde tamamlandı olarak bildirildiğinde sistem, tamamlanan maddeyi fiziksel olarak kullanılabilir olarak işaretler ve günlük deftere nakil işlemlerini bir ileti kuyruğuna ekler. Sistem, tamamlanmış bir maddeyi fiziksel olarak kullanılabilir olarak işaretlemeden önce, deftere nakillerin tam olarak işlenmesini beklemez.

**Üretim denetim parametreleri** sayfasında yapılandırılan varsayılan deftere nakil yöntemi için ambara özgü geçersiz kılmaları yapılandırmak üzere aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Kurulum \> Stok dökümü \> Ambarlar**'a gidin.
1. Ayarlamak istediğiniz ambarı seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Ambar** hızlı sekmesinde, **Üretim emirleri** bölümünde, **Deftere nakil yöntemi** alanını aşağıdaki değerlerden birine ayarlayın:

    - *Devral* – Seçili ambar, ayarı **Üretim denetim parametreleri** sayfasından devralır.
    - *Anında* – Bir madde tamamlandı olarak bildirildiğinde sistem, tamamlanan maddeyi fiziksel olarak kullanılabilir olarak işaretlemeden önce ilgili tüm günlük deftere nakil işlemlerini tam olarak işler.
    - *Ertelenmiş* – Bir madde tamamlandı olarak bildirildiğinde sistem, tamamlanan maddeyi fiziksel olarak kullanılabilir olarak işaretler ve günlük deftere nakil işlemlerini bir ileti kuyruğuna ekler. Sistem, tamamlanmış bir maddeyi fiziksel olarak kullanılabilir olarak işaretlemeden önce, deftere nakillerin tam olarak işlenmesini beklemez.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimi için günlük deftere nakil seçeneklerini ayarlama

Maddeler üretim katı yürütme arabiriminden tamamlandı olarak bildirildiğinde kullanılan deftere nakil yöntemini yapılandırmak için aşağıdaki yordamı kullanın.

1. **Üretim denetimi \> Kurulum \> Üretim yürütme \> Üretim emri varsayılanları** öğesine gidin.
1. **Tamamlandı olarak bildir** sekmesinde, **Tamamlandı olarak bildirme günlüğü** bölümünde, **Deftere nakil yöntemi** alanını aşağıdaki değerlerden birine ayarlayın:

    - *Anında* – Bir madde tamamlandı olarak bildirildiğinde sistem, tamamlanan maddeyi fiziksel olarak kullanılabilir olarak işaretlemeden önce ilgili tüm günlük deftere nakil işlemlerini tam olarak işler.
    - *Ertelenmiş* – Bir madde tamamlandı olarak bildirildiğinde sistem, tamamlanan maddeyi fiziksel olarak kullanılabilir olarak işaretler ve günlük deftere nakil işlemlerini bir ileti kuyruğuna ekler. Sistem, tamamlanmış bir maddeyi fiziksel olarak kullanılabilir olarak işaretlemeden önce, deftere nakillerin tam olarak işlenmesini beklemez.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>İleti işlemcisi toplu işini ertelenen deftere nakilleri işleyecek şekilde zamanlama

İleti işlemcisi toplu işi, kuyruğa alındıktan sonra günlük deftere nakillerinin işlenmesinden sorumludur. Günlük deftere nakillerinizin işlendiğinden emin olmak için, bu işi düzenli aralıklarla çalışacak şekilde yapılandırmalısınız. Gerekli toplu işi ayarlamak için aşağıdaki yordamı kullanın.

1. **Sistem yönetimi \>İleti işlemcisi \> İleti işlemcisi**'ne gidin.
1. **Parametreler** hızlı sekmesinde, **İleti kuyruğu** alanını *Üretim* olarak ayarlayın.
1. **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** öğesini *Evet* olarak ayarlayın. Sonra tekrarlayan bir zamanlama ayarlayın ve diğer ayarları gerektiği gibi yapılandırın. Ayarlar, Microsoft Dynamics 365 Supply Chain Management'taki diğer [arka plan işi](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) türleri için çalıştıkları gibi çalışır.

## <a name="track-the-progress-of-your-deferred-postings"></a>Ertelenen deftere nakillerinizin ilerlemesini izleme

Ertelenmiş günlük deftere nakilleri, *ileti işlemcisi* tarafından işlenene kadar *ileti işlemcisi iletileri* olarak sıraya alınır. İleti işlemcisi, planlanan toplu iş olarak çalışacak şekilde ayarlanmalıdır. İleti işlemcisi tarafından işlenen veya işlenecek ertelenmiş deftere nakil iletilerini görüntülemek için, **Üretim denetimi \> Üretim emirleri \> Ertelenmiş üretim emri deftere nakli**'ne gidin.

### <a name="message-grid-columns-and-filters"></a>İleti ızgarası sütunları ve filtreleri

Aradığınız belirli bir iletiyi bulmak için **Ertelenen üretim emri deftere nakli** sayfasının en üstünde yer alan alanları kullanabilirsiniz.

Aşağıdaki filtreler kullanılabilir:

- **İleti türü** – Kılavuzda gösterilen iletilerin türünü belirtir.
- **İleti durumu** – Kılavuzda gösterilen iletilerin durumunu belirtir. Aşağıdaki durumlar mevcuttur:

    - *Sıraya alındı* – İleti, ileti işlemcisi tarafından işlenmeye hazır.
    - *İşlendi* – İleti, ileti işlemcisi tarafından başarıyla işlendi.
    - *İptal edildi* – İleti son girişim sırasında işlenemedi ve kullanıcı tarafından iptal edildi.
    - *Başarısız* - İleti, son girişim sırasında işlenemedi. Sistem, başarısız olan iletileri üç kere yeniden dener. Daha sonra vazgeçer ve iletiyi *Başarısız* durumunda bırakır. İletiyi, bu üç denemeden sonra iptal edemeyeceğinizi veya düzenleyemeyeceğinizi unutmayın.

- **İleti içeriği** – Filtre, ileti içeriğinde tam metin araması yapar. (İleti içeriği kılavuzda görüntülenmez.) Filtre, birçok özel simgeyi (tire gibi) boşluk karakteri olarak işler ve tüm boşluk karakterlerini Boole VEYA işleçleri olarak değerlendirir. Örneğin, *USMF-123456*'ya eşit olan belirli bir `journalid` değeri arıyorsanız sistem, "USMF" veya "123456" içeren tüm iletileri bulur. Bu durumda, sonuçların listesi uzun olacaktır. Bu nedenle, sadece *123456* girilmesi daha iyi olacaktır çünkü bu şekilde daha belirgin sonuçlar alırsınız.

Ayrıca, sütun başlıklarından herhangi birini seçip açılan iletişim kutusuna ölçüt girerek listeyi sıralayabilir ve filtre uygulayabilirsiniz.

### <a name="view-the-message-log-message-content-and-details"></a>İleti günlüğünü, ileti içeriğini ve ayrıntıları görüntüleme

Bir iletiyle ilgili ayrıntılı bilgileri, iletiyi ızgarada seçip ardından her işleme olayının gösterildiği ileti ızgarası altında **Günlük** veya **Ham içerik** sekmesini seçerek bulabilirsiniz.

**Günlük** sekmesindeki araç çubuğunda aşağıdaki düğmeler bulunur:

- **Günlük** – İşlem sonuçlarını göstermek için bu düğmeyi seçin. Bu düğme özellikle, iletilerin **İşlem sonucu** değeri *Başarısız* olduğunda ve işleme hatasının nedenlerini öğrenmek istediğinizde yararlıdır.
- **Ürün demeti** – Birden fazla ileti işleme operasyonları, aynı toplu işlemin parçası olarak çalıştırılabilir. Ayrıntılı verileri görüntülemek için bu düğmeyi seçin. Örneğin, bazı iletiler için belirli bir işleme sırası gerektiren bağımlılıklar bulunup bulunmadığını görebilirsiniz.

### <a name="manually-process-or-cancel-a-message"></a>İletiyi manuel olarak işleme veya iptal etme

Mevcut durumuna bağlı olarak bir iletiyi gerekirse manuel olarak işleyebilir veya iptal edebilirsiniz. Izgarada iletiyi seçin ve sonra Eylem Bölmesi'nde **İşle** veya **İptal Et**'i seçin.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Başarısız işleme sonuçları için uyarı vermek üzere iş olayları ayarlama

Başarısız işleme sonuçları hakkında size uyarı veren [iş olaylarını](../../fin-ops-core/dev-itpro/business-events/home-page.md) ayarlayabilirsiniz. **Sistem yönetimi \> Kurulum \> İş olayları \> İş olayları kataloğu**'na gidin ve *İleti işlemcisi iletisi işlendi* adlı iş olayını etkinleştirin.

Etkinleştirme sürecinin bir parçası olarak, olayın tek bir tüzel kişiliğe özel mi, yoksa tüm tüzel kişilikler için mi geçerli olduğunu belirtmeniz istenir. Ayrıca bir **Uç nokta adı** değeri de girmeniz istenir. İlk olarak bu değer tanımlanmalıdır.

> [!NOTE]
> **Bir İş Olayı gerçekleştiğinde** alanı *Microsoft Power Automate* olarak ayarlandığında (örneğin *HTTPS* yerine), **Uç nokta adı** değeri, *Microsoft Power Automate* kurulumuna bağlı olarak Supply Chain Management'ta otomatik olarak oluşturulur.
