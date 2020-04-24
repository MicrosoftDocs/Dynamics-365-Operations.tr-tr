---
title: Ambar işinin ertelenmiş işlemesi
description: Bu konu, Dynamics 365 Supply Chain Management'ta ambar işi koyma işlemlerinin ertelenmiş işlenmesini sağlayan işlevselliği açıklar.
author: josaw1
manager: tfehr
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d274eae4ad3ba60eadb18ca8de22d4b2d10fe727
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205702"
---
# <a name="deferred-processing-of-warehouse-work"></a>Ambar işinin ertelenmiş işlemesi

[!include [banner](../includes/banner.md)]

Bu konu, Dynamics 365 Supply Chain Management'ta mevcut olan ambar işi için erteleme işlemlerinin ertelenmesini sağlayan işlevselliği açıklar.

Ertelenmiş işleme işlevselliği, ambar çalışanlarının arka planda işlenirken ambar işçilerinin başka işler yapmaya devam etmesini sağlar. Ertelenmiş işleme, birçok iş hattının işlenmesi gerektiğinde ve çalışan bu işin zaman uyumsuz olarak işlenmesine izin verebilirse yararlıdır. Ayrıca, sunucu işlem zamanında geçici veya planlanmamış artışlara sahip olabilir ve artan işlem süresi kullanıcının verimliliğini etkileyebilir.

Arka plan işleme SysOperation çerçevesi kullanılarak elde edilir. Daha fazla bilgi için bkz. [SysOperation Çerçevesine Genel Bakış](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>İş işleme ilkelerini yapılandırma

Ertelenmiş işlemeyi kullanmak için, bir iş işleme ilkesini yapılandırmalı ve kullanmalısınız.

İlkeler, **İş işleme ilkeleri** sayfasında yapılandırılır. Aşağıdaki tabloda, o sayfada kullanılabilecek alanlar açıklanmıştır.

| Alan                           | Tanım |
|---------------------------------|-------------|
| İş işleme ilkesi adı     | İş işleme ilkelerinin adı. |
| İş siparişi türü                 | İlkenin uygulandığı iş emri türü. |
| Operasyon                       | İlke kullanılarak işlenen işlem. |
| İş işleme yöntemi          | İş satırını işlemek için kullanılan yöntem. Yöntem **Anlık**olarak ayarlanmışsa biçim, hiçbir iş işleme ilkesi satırı işlemek için kullanılmadığında biçime benzer. Yöntem **Ertelenmiş**olarak ayarlanırsa toplu iş çerçevesi kullanan ertelenmiş işlem kullanılır. |
| Ertelenen işleme eşiği   | **0** (sıfır) değeri hiçbir eşik olmadığını gösterir. Bu durumda, ertelenmiş işlem kullanılabiliyorsa kullanılır. Belirli bir eşik hesaplaması eşiğin altındaysa, Anlık yöntem kullanılır. Aksi takdirde, Ertelenmiş yöntem kullanılabiliyorsa kullanılır. Satış ve transfer ile ilgili işler için eşik, iş için işlenen ilişkili kaynak yük hattı sayısı olarak hesaplanır. Stok yenileme çalışması için, eşik iş tarafından yenilenmekte olan iş satırlarının sayısı olarak hesaplanır. Örneğin, **5** eşiğini ayarlayarak, beşten az başlangıç kaynağı yükleme hattına sahip daha küçük işler ertelenmiş işlemeyi kullanmaz, ancak daha büyük işler onu kullanır. Yalnızca iş işleme yöntemi **Ertelenmiş**olarak ayarlanmışsa eşiğin etkisi vardır. |
| Ertelenen işleme toplu iş grubu |İşleme için kullanılan toplu iş grubu. |

Ertelenmiş yerine koyma işleme için şu iş emri türleri desteklenir: satış siparişi, transfer emri çıkışı ve stok yenileme.

## <a name="assigning-the-work-creation-policy"></a>İş oluşturma ilkesini atama

İş oluşturma ilkesi ambar yönetimi parametrelerinde atanabilir. Ayrıca bireysel ambarlar düzeyinde atanabilir. İlke bir ambara atanmışsa yalnızca o ambar için oluşturulan çalışmaya uygulanır. Ambar düzeyinde ilke atanmamışsa ambar yönetimi parametrelerinden gelen ilke uygulanır.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Ertelenmiş yerine koyma işleme görevlerini görüntüleme

Ertelenmiş yerine koyma işleme görevleri **Ertelenmiş yerine koyma işleme görevleri** sayfasında görüntüleyebilirsiniz.

Varsayılan olarak, **Tamamlanan** görevler gösterilir.

| Alan            | Tanım |
|------------------|-------------|
| Durum           | Görevin durumu. |
| Toplu iş durumu | İlgili toplu işin durumu. Toplu işlem işlenirse toplu iş geçmişi günlük ve toplu işlemdeki bilgileri içerir. |

Olası durumlarla ilgili açıklama aşağıda verilmiştir:

- **Bekleniyor** – İlgili toplu işlem toplu iş sunucusunda işlemeyi bekliyor.
- **Başarısız** – İşlem başarısız oldu. Görev **Ertelenmiş yerine koymayı işle** eylemi kullanılarak yeniden işlenir veya **Ertelenmiş yerine koymayı iptal et** eylemini kullanarak iptal edilebilir.
- **Tamamlandı** – İş tamamlandı.

## <a name="impact-on-closed-work-dates"></a>Kapalı iş tarihlerine etki

Ertelenmiş yerine koyma işleme kullanıldığında, kapalı çalışma tarihi oluşturulan tarih/saat ertelenmiş yerine koyma işleme görevleri olarak ayarlanır. Kapalı çalışma tarihi, yerine koyma işlemi tamamlandığında en iyi tahmin olduğundan kullanılır.

## <a name="reprocessing-a-failed-task"></a>Başarısız olan bir görevi yeniden işleme

Başarısız olan bir görevi sayfada seçerek ve sonra **Ertelenmiş yerine koymayı işleme**seçeneğini belirleyerek yeniden işleyebilirsiniz. Yeniden işleme, hemen işlenmek üzere ayarlanmış gibi, kullanıcının mobil cihazdan yerine koyma işlemini tamamladığı bir duruma karşılık gelir.

## <a name="canceling-failed-tasks"></a>Başarısız görevleri iptal etme

Yalnızca başarısız görevler iptal edilebilir. Bir görevi iptal ettiğinizde, yeni bir kullanıcıya atayabilirsiniz. Alternatif olarak, görev işi işleyen kullanıcıya atanmış olarak kalabilir. İptal işlemi, işin mobil cihazına son çekme adımı yeni tamamlanmış ve işin geri alınması gerektiği gibi geri getirildiği bir duruma karşılık gelir. Bununla birlikte, kullanıcı işin "farklı" olduğunu belirleyebilecektir, çünkü sadece bir yerine koyma aşamasına sahip olacaktır ve yer, işi ilk işleyen kullanıcının son konum olarak konumlandırıldığı yere karşılık gelecektir.

Bir görev iptal edildiğinde, iş artık geciktirilmiş yerine koyma işlemini engelleme nedeni tarafından engellenmeyecektir. Mobil cihaz kullanılarak yeniden işlenebilir.

Görev iptal edildiğinde görev kaydı silinir.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Ertelenmiş işleme ilkesini atlamak için mobil aygıt menüsünü yapılandırma

Ertelenmiş işleme ilkesinin kullanılabilmesi için mobil aygıt menü öğesini yapılandırabilirsiniz. İş daha sonra hiçbir ertelenmiş işleme politikasında kullanılmadığı gibi işlenir. Bu işlevsellik bir gözetmenin ertelenen yerine koyma kullanmadığı belirli bir menü öğesini kullanmasını sağlar. Yapılandırmak için **Ertelenmiş put işleme ilkesi işleme** alanını **Ayarları geçersiz kılma ve yerine koymayı eşzamanlı olarak işleme** olarak ayarlayın 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Ertelenmiş yerine koyma işleme uygulanmadığında kısıtlamalar

Burada ertelenmiş yerine koyma işleme ilkesi yapılandırılmış olsa bile uygulanmadığını birkaç senaryo vardır. Burada bazı örnekler verilmiştir:

- El ile iş tamamlama kullanılır.
- İş otomatik tamamlama kullanılarak tamamlanır.
- Denetim şablonları kullanılır.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Giden iş izleme çalışma alanından ertelenmiş işleme görevlerini izleme

**Giden iş izleme** çalışma alanının, ertelenmiş yerine koyma işleme görevlerini izlemenize yardımcı olan iki kutucuğu vardır:

- **Başarısız ertelenmiş yerine koyma işleme görevleri** -Bu kutucuk başarısız olan görevlerin sayısını gösterir. Başarısız görevler varsa ambar yöneticisi otomatik olarak yeniden işlenmediği için bunları yeniden işlemeli veya iptal etmelisiniz.
- **Bekleyen ertelenmiş yerine koyma işleme görevleri** – Bu kutucuk 10 dakikadan fazla **Bekleyen** durumundaki görevlerin sayısını gösterir. Kutucuk bir sayı gösteriyorsa toplu iş sırasında bir sorunun oluştuğunu gösteriyor olabilir. **Bekleyen** görevleri el ile işleyebilirsiniz. Bir görevin toplu işi daha sonra işlenecekse zaten işlendiğinden, yalnızca başarısız olur. Hiçbir etkisi olmayacak.

## <a name="deleting-completed-tasks"></a>Tamamlanan görevleri silme

İşlemi tamamladıktan sonra ertelenmiş işleme işlemlerini seçerek ve sayfadan silerek silebilirsiniz.
