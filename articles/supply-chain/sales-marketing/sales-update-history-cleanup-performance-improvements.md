---
title: Satış geçmişi verilerini temizleme işlemini zamanlama
description: Bu makalede, periyodik Satış güncelleştirme geçmişi temizleme görevini düzenli aralıklarla çalışacak şekilde zamanlayarak sistem performansının artırılmasına nasıl yardımcı olacağınız açıklanmaktadır.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335518"
---
# <a name="schedule-sales-history-data-cleanup"></a>Satış geçmişi verilerini temizleme işlemini zamanlama

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, standart operasyonlarının bir parçası olarak, satış geçmişi güncelleştirme verilerini sürekli oluşturur ve depolar. Zamanla büyük miktarda eski satış geçmişi verisi sisteminizde birikebilir. Bu birikmiş veriler, satış siparişleriyle ilgili belgeler deftere nakledildiğinde performans sorunlarına ve işlevsel sorunlara neden olabilir. (Bu belgeler satış sipariş teyitlerini, satış sevk irsaliyelerini, satış malzeme çekme listelerini ve faturaları içerir). Bu nedenle, periyodik *Satış güncelleştirme geçmişi temizleme* görevini düzenli aralıklarla çalışacak şekilde ayarlamanız ve zamanlamanız gerekir. Bu görev artık gerekmeyen tüm satış geçmişi güncelleştirme verilerini kaldırır.

*Satış güncelleştirme geçmişi temizleme* görevini kullanırsanız, görevin daha etkili çalışmasını sağlayan *Satış geçmişi temizleme işlemi performans iyileştirmeleri* özelliğini etkinleştirmenizi öneririz. (Yine de, bu özelliği etkinleştirmeden de görevi çalıştırabilirsiniz.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Satış geçmişi temizleme özelliklerini açma

*Satış güncelleştirme geçmişi temizleme* görevini bu makalede açıklanan tüm özelliklerle birlikte ayarlamak ve kullanmak için, aşağıdaki alt bölümlerde açıklandığı gibi, özellik yönetimindeki *Satış geçmişi temizleme işlemi performans iyileştirmeleri* ve *Yaşına göre satış güncelleştirme geçmişini temizle* özelliklerini etkinleştirmeniz gerekir.

### <a name="sales-history-cleanup-performance-improvements"></a>Satış geçmişi temizleme işlemi performans iyileştirmeleri

**Satış güncelleme geçmişi temizleme** periyodik toplu iş, yüksek satış güncelleştirmeleri hacmine sahip ortamlarda seyrek çalıştırılırsa uzun sürebilir. Bu durumlarda, *Satış Geçmişi Temizleme performans iyileştirmeleri* özelliği çalışma süresinin azaltılmasına ve güvenilirliği artırmanıza yardımcı olur.

Özellik, varolan temizleme işini aşağıdaki yollarla geliştirir:

- Temizlemeyi toplu işlemlere böler (özelleştirmeler aracılığıyla toplu iş boyutunu değiştirebilirsiniz).
- En fazla 2 saat boyunca çalışacak (özelleştirmelerin süresini değiştirebilirsiniz).
- Mümkün olduğunda, kilitlemeyi en aza indirmek ve temizleme sırasında işlem tablolarını birleştirmekten kaçınmak için veritabanı yeteneklerinden yararlanılacaktır.

Özellik etkinleştirildikten sonra, **Satış güncelleştirme geçmişi temizliği** toplu işlemi (**Satış ve pazarlama \> dönemi görevleri \> Temizleme \> Satış güncelleme geçmiş temizleme**), daha önce olduğu gibi çalışacak, ancak daha iyi performans ve en fazla 2 saat boyunca çalışacaktır. Bu, belirli bir bekletme süresi çerçevesi için tüm verileri temizlemek amacıyla birkaç kez çalıştırılması gerekebilecek anlamına gelir.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Model:** *Satış ve pazarlama*
- **Özellik adı:** *Satış geçmişi temizleme işlemi performans iyileştirmeleri*

### <a name="clean-up-sales-update-history-based-on-age"></a>Yaşına göre satış güncelleştirme geçmişini temizle

*Yaşına göre satış güncelleştirme geçmişini temizle* özelliği, periyodik *Satış güncelleştirme geçmişi temizleme* görevini çalıştırırken tutulacak kayıtların maksimum yaşını belirtmenizi sağlar. Eski kayıtlar silinecek. Bu özellik, geçerlilik süresi her zaman görevin çalıştırıldığı tarihe göre hesaplandığı için, görevi belirli aralıklarla çalışacak şekilde ayarladığınızda yararlıdır. Bu özelliği kullanmazsanız, yalnızca tutulacak en eski kayıtlar için belirli bir tarih ayarlayabilirsiniz.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Yaşına göre satış güncelleştirme geçmişini temizle* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Satış geçmişi temizleme periyodik görevini ayarlama ve zamanlama

*Satış geçmişi temizleme* periyodik görevini ayarlamak ve zamanlamak için aşağıdaki adımları izleyin.

1. Geçmişe ait satış siparişi deftere nakil verilerinin kaç gün tutulacağını belirlemek için iş gereksinimlerinizi analiz edin. Temizleme görevini genellikle her üç ayda bir ve en fazla altı ayda bir çalıştırmanızı öneririz.
1. **Satış ve pazarlama \> Periyodik görevler \> Temizleme \> Satış güncelleştirme geçmişi temizleme**'ye gidin.
1. **Satış güncelleştirme geçmişini temizle** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Temizle** – Temizlenecek kayıt türünü belirtmek için aşağıdaki değerlerden birini seçin:

        - **Yürütüldü** – Yalnızca tam olarak işlenmiş kayıtları silin. Bu kayıtlar üzerinde büyük olasılıkla daha fazla işlem yapmayacağınızdan bu seçenek en güvenli seçenektir.
        - **Yürütüldü ve hatalı** – Tam olarak işlenmiş kayıtları ve hatanın oluştuğu kayıtları silin. Bu seçenek en sık kullanılan seçenektir. Otomatik olarak temizlenmelerini sağlamak yerine hatalı kayıtları denetlemek ve düzeltmek isteyebilirsiniz. Ancak birçok şirket bu kayıtları, büyük olasılıkla artık ilgili olmadıklarından yaklaşık bir ay sonra temizlemeyi tercih eder.
        - **Tümü** – Yürütülen, hatalı ve bekleyen kayıtları silin. Bekleyen kayıtlar geçerlidir ancak henüz tam olarak işlenmemiştir. Çoğu durumda, bunların otomatik olarak silinmesini istemezsiniz. Ancak bazı durumlarda, belirli bir süre geçtikten sonra bunların otomatik olarak silinmesini seçebilirsiniz.

    - **Kayıtları yaşa göre sakla** – Kayıtları görevin çalıştırıldığı gündeki yaşına göre temizlemeyi mi yoksa sabit bir tarihten önce oluşturulan kayıtları silmeyi mi tercih ettiğinizi belirtin. Temizlemeyi yinelenen bir görev olarak zamanlıyorsanız, yaş her zaman görevin çalıştırıldığı tarihe göre hesaplandığı için bu seçeneği *Evet* olarak ayarlamalısınız.

        - **Maksimum yaş** alanını etkinleştirmek için bu seçeneği *Evet* olarak ayarlayın. Bu alan, görev her çalıştırıldığında tutulacak kayıtların maksimum yaşını belirtmek için kullanılır. **En eski oluşturulma tarihi** alanı yok sayılır.
        - **En eski oluşturulma tarihi** alanını etkinleştirmek için bu seçeneği *Hayır* olarak ayarlayın. Bu alan, görev çalıştırıldığında tutulacak kayıtların en eski oluşturulma tarihini belirtmek için kullanılır. **Maksimum yaş** alanı dikkate alınmaz.

    - **En eski oluşturulma tarihi** – Bu ayar yalnızca **Kayıtları yaşa göre sakla** seçeneği *Hayır* olarak ayarlandığında uygulanır. Görev çalıştırıldığında tutulacak kayıtların en eski oluşturulma tarihini belirtin. Bu tarihten önce oluşturulan kayıtlar silinir.
    - **Maksimum yaş** – Bu ayar yalnızca **Kayıtları yaşa göre sakla** seçeneği *Evet* olarak ayarlandığında uygulanır. Görev her çalıştırıldığında tutulacak kayıtların maksimum yaşını (gün olarak) belirtin. Eski kayıtlar silinecek.

1. **Arka planda çalıştır** hızlı sekmesinde görevin nasıl, ne zaman ve ne sıklıkta çalıştırılacağını belirtin. 1. adımda belirlediğiniz zamanlamayı uygulamak için bu ayarları kullanın. Alanlar, Supply Chain Management'ta bulunan diğer [toplu işler](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Ayarlarınızı uygulayıp iletişi kutusunu kapatmak için **Tamam**'ı seçin.
