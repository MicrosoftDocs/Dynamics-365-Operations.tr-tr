---
title: İş akışı onay işlemlerindeki eylemler
description: Bu makalede, onay bir iş akışı onay sürecindeki her katılımcının gerçekleştirebileceği eylemler açıklanmaktadır.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 829ee16b8fd72a0808a657419524487d9c1b3123
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560487"
---
# <a name="actions-in-workflow-approval-processes"></a>İş akışı onay işlemlerindeki eylemler

[!include [banner](../includes/banner.md)]

Bu makalede, onay bir iş akışı onay sürecindeki her katılımcının gerçekleştirebileceği eylemler açıklanmaktadır.

Bir iş akışı çeşitli gruplarda kişiler içerebilir: Başlatıcı, görev alanlar, karar vericiler ve onaylayıcılar. Örneğin, aşağıdaki gider raporu iş akışında, Sam başlatandır, sıranın üyeleri görevin atananlarıdır, John karar vericidir ve Frank, Sue ve Ann de onaylayıcılardır.

[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)

Aşağıdaki bölümlerde her grubun gerçekleştirebileceği iş akışı eylemleri açıklanmıştır.

## <a name="actions-that-an-originator-can-perform"></a>Başlatanın yerine getirebileceği eylemler

Başlatan, işlenmek üzere bir belge göndererek bir iş akışı örneğini başlatır. Örneğin, Sam kendi gider raporu göndermek için **Gider raporu** sayfasında **Gönder** düğmesini tıklatmalıdır.

## <a name="actions-that-a-task-assignee-can-perform"></a>Görev alanın yerine getirebileceği eylemler

Bir görev birden fazla kişiye veya birkaç kişi tarafından izlenen bir iş öğesi sırasına atanabilir. Ancak bir görevi yalnızca bir kişi tamamlayabilir. Örneğin, Sam bir gider raporu gönderdi ve kendi girişlerini kuruluşunun Gider raporları bölümünün gözden geçirmesi için yönlendirdi.

Adventure Works gider raporları bölümünün üyeleri sırayı izler. Bu departman üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti. Şimdi aşağıdaki eylemlerden birini gerçekleştirebilir: Tamamlama, reddetme, temsilci seçme, değişiklik talep etme, yeniden atama veya yayımlama.

> [!NOTE]
> Gerçekleştirilebilecek eylemler, yazılım geliştiricisinin görevi nasıl tasarladığına bağlı olarak değişebilir.

### <a name="complete"></a>Tamamla

Bir kullanıcı bir görevi tamamladığında, işlenmek üzere gönderilen belge, iş akışında yer alan bir sonraki kullanıcıya (eğer mevcutsa) atanır. Başka işlem gerekmiyorsa, iş akışı süreci sona erer.

Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti. Julie her gözden geçirme işlemi tamamlandıktan sonra belgeyi John'a atanır.

### <a name="reject"></a>Reddet

Bir kullanıcı bir belgeyi reddettiğinde iş akışı süreci sona erer.

Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti. Eğer Julie gider raporunu reddederse, iş akışı işlemi sona erer.

Sam, daha sonra gider raporunu yeniden gönderebilir. Önce değişiklikler yapabilir veya ilk sürümü yeniden gönderebilir. Sam gider raporunu yeniden gönderirse, iş akışı işlemi el ile inceleme görevinden başlar.

### <a name="delegate"></a>Temsilci

Bir kullanıcı görevi devrederse, görev başka bir kullanıcıya atanır.

Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti. Julie, bu görevi onun yardımcısı olan Tim'e devreder.

Bunun üzerine Tim, Julie adına hareket eder. Bu nedenle, Tim kendi incelemesini tamamlandığında, sanki görevi bitiren Julie gibi, gider raporu John'a atanır.

### <a name="request-change"></a>Değişiklik iste

Bir kullanıcı gönderilen belgede değişiklik yapılmasını talep ederse, belge başlatana geri gönderilir.

Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti. Julie, gider raporunda bir kaç hata fark eder ve değişiklik talebinde bulunur. Gider raporu Sam'e geri gönderilir.

Sam, daha sonra gider raporunu yeniden gönderebilir. Önce talep edilen değişiklikleri yapabilir veya ilk sürümü yeniden gönderebilir. Sam gider raporu yeniden gönderirse, çalışma öğesini sırasının bir üyesi gider raporu ve girişleri yeniden gözden geçirmek zorundadır.

### <a name="reassign"></a>Yeniden Ata

Bir iş öğesi sırasının üyeleri o sırada bulunan belgeleri bir başka sıraya yeniden atayabilirler.

Örneğin, Adventure Works Gider Raporları departmanının bir üyesi olan Julie, sırayı izlemektedir. İş yükünü dengelemeye yardımcı olmak için, gider raporu ve ona dahil olan girişleri başka bir sıraya yeniden atayabilir.

### <a name="release"></a>Sürüm

Bazen, bir iş maddesi kuyruğu üyesi görevi kabul eder, ancak daha sonra görevi tamamlayamayacağına karar verebilir. Bu durumda, görevi kabul eden kişi belgeyi iş maddesi kuyruğuna geri bırakabilir.

Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti. Eğer Julie, görevi tamamlayamayacağına karar verirse, belgeyi serbest bırakabilir. Böylece Adventure Works gider raporları bölümünün diğer üyelerinin görevi tamamlayabilmesi için gider raporu sıraya döndürülür.

## <a name="actions-that-a-decision-maker-can-perform"></a>Bir karar vericinin gerçekleştirebileceği eylemler

Genellikle, karar vericinin yanıtlaması gereken bir soru olduğundan, belge bir karar vericiye atanır. Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur. Karar verici bu seçeneklerden birini seçmezse, kararı başkasına devredebilir.

### <a name="choice-1-or-choice-2"></a>\[Seçenek 1\] veya \[Seçenek 2\]

Karar vericinin belgeyle ilgili bir soruyu yanıtlaması gerekir. Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur. Karar vericinin seçtiği cevap, belgeyi işlemek için kullanılacak iş akışı dalını belirler.

Örneğin, Sam'in gider raporu John'a atanır. Belgedeki bilginin Sam'in yöneticisini aramaya gerektirip gerektirmediğine karar vermesi gerekir. John çağrının gerekli olduğuna karar verirse, gider raporu Aretha'ya atanır, onun da bunun üzerine Sam'in yöneticisini araması gerekir. Eğer John, aramanın gerekli olmadığına karar verirse, gider raporu onay için Frank'e atanır.

### <a name="delegate"></a>Temsilci

B'r karar verici, karar vermeyi devrederse, belge kararı vermek zorunda olan başka bir kullanıcıya atanır.

Örneğin, Sam'in gider raporu John'a atanır. John, kararı onun asistanı olan Maria'ya devreder.

Bunun üzerine Maria, John adına hareket eder. Eğer Maria Sam'in yöneticisini aramaya gerek olduğuna karar verirse, gider raporu Aretha'ya atanır, onun da bunun üzerine Sam'in yöneticisini araması gerekir. Eğer Maria, aramanın gerekli olmadığına karar verirse, gider raporu onay için Frank'e atanır.

## <a name="actions-that-an-approver-can-perform"></a>Onaylayanın yerine getirebileceği eylemler

Bir belge, bir onaylayana atandığında, onaylayan şu eylemlerden birini gerçekleştirebilir: onaylama, reddetme, devretme veya değişiklik talep etme.

### <a name="approve"></a>Onayla

Onaylayan belgeyi onayladığında, belge iş akışında yer alan sonraki kullanıcıya (eğer mevcutsa) atanır. Başka işlem gerekmiyorsa, iş akışı süreci sona erer.

Örneğin, Sam için 6.000 ABD Doları için bir gider raporu gönderdi ve bu belge Frank'e atandı. Frank belgeyi onayladığında, belge onaylanmak üzere Sue'ya atanır. Sue gider raporunu onayladığında, iş akışı işlemi sona erer.

### <a name="reject"></a>Reddet

Onaylayan bir belgeyi reddettiğinde iş akışı süreci sona erer.

Örneğin, Sam 12.000 ABD Doları için bir gider raporu gönderdi ve bu belge Sue'ya atandı. Eğer Sue gider raporunu reddederse, iş akışı işlemi sona erer.

Sam, daha sonra gider raporunu yeniden gönderebilir. Önce değişiklikleri yapabilir veya gider raporunun ilk sürümünü yeniden gönderebilir. Eğer Sam gider raporunu yeniden gönderirse, iş akışı işlemi onay işleminden başlar.

### <a name="delegate"></a>Temsilci

Onaylayan bir belgeyi devrettiğinde, belge onay için başka bir kullanıcıya atanır.

Örneğin, Sam için 12.000 ABD Doları için bir gider raporu gönderdi ve bu belge Frank'e atandı. Mete gider raporu için temsilci olarak Ayla'yı atar.

Ann böylece Frank adına hareket eder. Bu sebeple, Ann belgeyi onayladığında, belge sanki Frank tarafından onaylanmış gibi, onaylanmak üzere Sue'ya atanır. Sue belgeyi onayladıktan sonra, onaylanmak üzere Ann'e gönderilir.

### <a name="request-change"></a>Değişiklik iste

Onaylayan bir belgede değişiklik yapılmasını talep ederse, belge başlatana geri gönderilir.

Örneğin, Sam 12.000 ABD Doları için bir gider raporu gönderdi ve bu belge Sue'ya atandı. Eğer Sue bir değişiklik isteğinde bulunursa, gider raporu Sam'e geri gönderilir.

Sam, daha sonra gider raporunu yeniden gönderebilir. Önce talep edilen değişiklikleri yapabilir veya gider raporunun ilk sürümünü yeniden gönderebilir. Sam gider raporunu yeniden gönderirse, onaylama işleminde ilk onaylayan Frank olduğu için belge onaylanmak üzere Frank'e gönderilir.
