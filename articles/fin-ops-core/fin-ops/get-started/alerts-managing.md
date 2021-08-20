---
title: Uyarıların toplu işlenmesi
description: Bu konu toplu iş işleme uyarıları hakkında bilgi sağlar.
author: RichdiMSFT
ms.date: 09/10/2010
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: bc5366ea0e0a93cbd7806bb87608590f5304031a92751ff25a1531c2a3b135b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764444"
---
# <a name="batch-processing-of-alerts"></a>Uyarıların toplu işlenmesi

[!include [banner](../includes/banner.md)]

Uyarılar, toplu işleme işlevi ile işlenir. Uyarıları işlemeden ve göndermedne önce toplu işlemeyi ayarlamanız gerekir.

Toplu işleme işlevi iki olay türünü destekler:

- Değişiklik tabanlı olaylar tarafından tetiklenen olaylar. Bu olaylar, oluşturma/silme ve güncelleştirme olayları olarak da adlandırılır.
- Son tarihler tarafından tetiklenen olaylar.

Her olay türü için toplu işlemler oluşturabilirsiniz.

## <a name="batch-processing-for-change-based-events"></a>Değişiklik tabanlı olaylar için toplu işleme

Sistem, toplu işlemenin son çalıştırılmasından bu yana gerçekleşen tüm değişiklik tabanlı olayları okur. Değişiklik tabanlı olaylar, alanlardaki güncelleştirmeleri, kayıtların silinmesini ve kayıtların oluşturulmasını içerir. Bu olaylar, uyarı kurallarında ayarladığınız koşullarla karşılaştırılır. Olay, kuraldaki koşullarla eşleştiğinde toplu işlem bir uyarı oluşturur.

### <a name="frequency-for-change-based-events"></a>Değişiklik tabanlı olayların sıklığı

Değişiklik tabanlı olaylar için, sistemin olayı günlüğe kaydetmesinin ardından olayın işlenmesini tetikleyen bir toplu iş oluşturabilirsiniz. Toplu işi, daha sık tekrarlayacak şekilde ayarlarsanız değişiklikler meydana geldiğinde kullanıcılar uyarıları daha erken alır. Ancak daha yüksek toplu işleme sıklığı, sistem performansını olumsuz etkileyebilir.

Diğer taraftan, daha az tekrarlanan ve sistem yükü düşük olduğu zamanlara planladığınız bir toplu iş, sistem performansını artırmaya yardımcı olabilir. Ancak, toplu işleme için düşük bir sıklık, kullanıcıların zamanında uyarı taleplerini karşılamayabilir.

Bu nedenle, değişiklik tabanlı olaylar için toplu işleme sıklığını ayarlarken uyarıların zamanında verilmesi ile tüm sistemin performansı arasındaki dengeyi göz önünde bulundurun. Uyarı kuralları oluşturan kullanıcıların sayısı arttıkça bu konular daha önemli hale gelir. Sıklık, sistemin işlediği olay sayısını etkilemez. Ancak daha fazla kullanıcı kural oluşturursa işlem daha fazla denetim çalıştırır. Bu tür veri alışverişleri, sistem performansını etkileyebilir.

#### <a name="the-risks-of-low-batch-frequency"></a>Düşük toplu iş sıklığının riskleri

Değişiklik tabanlı olayların toplu işlemesi için düşük bir frekans ayarlarsanız uyarı kurallarındaki koşullarla ilgili veriler, işlenmeden önce değişebilir. Bu nedenle, uyarıları kaybedebilirsiniz.

Örneğin, olay **müşteri ilgili kişi bilgileri değişti** ve koşul **müşteri = BB** olduğunda tetiklenmesi için bir uyarı oluşturabilirsiniz. Başka bir ifadeyle, BB müşterisi için müşteri ilgili bilgileri değiştiğinde işlem, olayı günlüğe kaydeder. Bununla birlikte, toplu işleme sistemi, toplu işlemin veri girişinden daha az sıklıkta gerçekleşeceği şekilde ayarlanır. Müşteri adı, olay işlenmeden önce **BB**'den **AA**'ya değişirse veritabanındaki veri artık kuraldaki koşul (**müşteri = BB**) ile eşleşmez. Bu nedenle, olay son olarak işlendiğinde uyarı oluşturulmaz.

### <a name="set-up-processing-for-change-based-alerts"></a>Değişiklik tabanlı uyarılar için işlemeyi ayarlama

1. **Sistem yönetimi** &gt; **Periyodik görevler** &gt; **Uyarılar** &gt; **Değişiklik tabanlı uyarılar**'a gidin.
2. **Değişiklik tabanlı uyarılar** iletişim kutusuna uygun bilgileri girin.

## <a name="batch-processing-for-due-date-events"></a>Vade tarihi olayları için toplu işleme

Sistem, vade tarihlerinin neden olduğu tüm olayları algılar ve bu olaylar, uyarı kurallarında ayarlanan koşullarla karşılaştırılır. Bir olay, kuraldaki koşullarla eşleştiğinde toplu işlem bir uyarı oluşturur.

### <a name="frequency-for-due-date-events"></a>Vade tarihi olaylarının sıklığı

Vade tarihi olayları için, sistem yükünü dengelemek üzere geceleri veya günün belirli zamanlarında çalışan toplu işler oluşturmak isteyebilirsiniz. Toplu işi günde en az bir kez çalışacak şekilde ayarlamanızı öneririz. Uyarıların mümkün olduğunca erken gönderilmesi gerekiyorsa toplu işlemeyi sistem tarihi değiştikten hemen sonra gerçekleşecek şekilde ayarlayın. Vade tarihi olayları için uyarıları, toplu iş uyarıları işledikten sonra oluşturmak isterseniz toplu işi aynı gün içerisinde tekrar çalıştırabilirsiniz.

Örneğin, belirli bir günde bir toplu iş çalıştırılmış olabilir. Daha sonra, aynı günde bir uyarıyı tetiklemesi gereken vade tarihi olan bir satınalma siparişi oluşturursunuz. Uyarıyı aynı gün almak için satınalma siparişi oluşturulduktan sonra toplu işi yeniden çalıştırmanız gerekir. Ancak, toplu işi aynı gün içerisinde çalıştırmazsanız bir sonraki günün toplu işi, önceki günlerde işlenmemiş vade tarihi olaylarını algılar.

> [!NOTE]
> Toplu işlem günde bir defadan fazla çalıştığında bile aynı vade tarihi olayları ve koşulları için yinelenmez. Uyarılar yalnızca son toplu iş çalıştıktan sonra sistemde oluşan değişiklikler nedeniyle vadesi geçmiş hale gelen tarihler için oluşturulur.

### <a name="batch-processing-window"></a>Toplu işleme penceresi

Bir şirketteki uyarı kurallarının işlenmesi birkaç nedenden dolayı durdurulabilir. Bu nedenler arasında tatiller, sistem hataları veya toplu işlerin bir süredir çalıştırılmasını engelleyen diğer sorunlar yer alır.

Toplu işin birkaç gün boyunca çalıştırılmaması nedeniyle vade tarihi uyarılarının geçersiz olmasını önlemek için bir toplu işleme penceresi oluşturabilirsiniz. Toplu işleme penceresi, bir toplu işin belirli bir gün sayısı boyunca çalışmasını önlemek için kullanılabilir.

Toplu işleme penceresi ayarlarsanız uyarı, vade tarihi ölçütünde tanımlanan zaman sınırını aşsa bile, uyarı kuralı işlendiğinde gönderilir. Bu zaman sınırı ile tanımlanan döneme ek olarak toplu işleme penceresi aşılmadığı sürece bir uyarı gönderilmeye devam eder. Ancak süre, zaman sınırı ile tanımlanan değere ek olarak toplu işleme zaman dilimini aştığında uyarı artık gönderilmez.

### <a name="set-up-processing-for-due-date-alerts"></a>Vade tarihi uyarıları için işlemeyi ayarlama

1. **Sistem yönetimi** &gt; **Periyodik görevler** &gt; **Uyarılar** &gt; **Vade tarihine yönelik uyarılar**'a gidin.
2. **Vade tarihine yönelik uyarılar** iletişim kutusuna uygun bilgileri girin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]