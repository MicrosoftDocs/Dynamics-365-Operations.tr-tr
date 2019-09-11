---
title: Tercih edilen bakım görevlilerini ayarla
description: Bu konuda Varlık Yönetimi'nde tercih edilen bakım görevlisi ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887423"
---
# <a name="preferred-maintenance-workers"></a>Tercih edilen bakım görevlileri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

İş emri planlama sırasında hangi bakım görevlilerinin iş emirlerini tamamlamak üzere tahsis edileceğini belirten bir tercih yapabilirsiniz. Bu işlevin kullanımı isteğe bağlıdır, ancak çalışanın yeteneklerine ve yetkinliklerine dayalı olarak işin tamamlanması için en nitelikli bakım görevlisini seçmenize yardımcı olabilir. Bu nedenle, iş siparişi planlama sırasında, **Tercih edilen bakım görevlileri** kurulumu, bir iş emri için belirli bir bakım görevlisinin veya çalışan grubunun planlanıp planlanmayacağını belirlemek için kullanılır. Yalnızca, planlama zamanında uygun olan bakım görevlileri planlanır. Tercih edilen bakım görevlisi ayarı planlama sırasında bir iş emriyle eşleşirse ancak bakım görevlisi diğer işlere tahsis edilmişse, iş emri uygun durumdaki başka bir bakım görevlisi için planlanır.

Tercih edilen bakım görevlilerini ayarlamadan önce, ilk olarak seçilmek için uygun olması gereken bakım görevlilerini ve çalışan gruplarını ayarlamanız gerekir. Bakım görevlileri ve çalışan gruplarını nasıl ayarlayacağınızla ilgili açıklama için bkz. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Tercih edilen bakım görevlilerini ayarlama

Tercih edilen bakım görevlisi veya çalışan grubu belirli bir

- görevle  
- bakım işi türü çeşidiyle  
- bakım işi türüyle  
- bakım işi türü kategorisiyle  
- varlıkla  
- varlık türüyle  

veya bu seçimlerin bir bileşiyle ilgili olabilir. Aynı kayıt için ne kadar çok seçim yaparsanız, kurulumunuz o kadar belirgin olacaktır.

1. **Varlık Yönetimi** > **Kurulum** > **Çalışanlar** > **Tercih edilen bakım görevlileri**'ne tıklayın.

2. Yeni bir kayıt oluşturmak için **Yeni**'ye tıklayın.

3. Yukarıdaki madde işareti listesde gösterilen alanlarda seçim yapılmamış bir "varsayılan" bakım görevlisi veya çalışan grubu kurulumu oluşturarak başlayın. Bu, yalnızca **Tercih edilen bakım görevlisi grubu** alanında veya **Tercih edilen bakım görevlisi** alanında seçim yapacağınız anlamına gelir. Aşağıdaki şekilde, tercih edilen bakım görevlisi grubu olarak "Talepler" in seçildiği bir ilk kayıt örneği görürsünüz.

>[!NOTE]
>Varsayılan kurulum, iş emri planlaması sırasında başka, daha özel kombinasyon iş emrinin içeriğiyle eşleşirse kullanılacaktır.

4. Yeni bir kayıt oluşturmak için adım 2'yi tekrarlayın. Tercih edilen çalışan veya çalışan grubunun ayrıntı düzeyine bağlı olarak gerekli seçimleri yapın. *Örnek:* Aşağıdaki şekilde, altıncı kayıtta, tercih edilen çalışan olarak bakım görevlisi Shawn Richardson seçilidir. Planlanan saatte uygun olması durumunda, "CH-BP1-03-02" varlığı ve "tesis değerlendirmesi " bakım işi türünü içeren bir iş emri planlamasında otomatik olarak seçilecektir.

>[!NOTE]
>Genellikle, iş emri planlama sırasında tercih edilen bir bakım çalışanı seçildiğinde, Varlık Yönetimi olası bir eşleşmeyi denetlemek için tüm **Tercih edilen bakım görevlileri** kayıtlarına bakar ve her zaman en belirgin birleşimi denetler. Eşleşme bulunmazsa, **Tercih edilen bakım çalışanı grubu** alanında veya **Tercih edilen bakım çalışanı** alanında bulunan "varsayılan" kayıt kullanılır.


![Şekil 1](media/02-work-order-scheduling.png)

Ayrıca, bakım talebi veya iş emri oluşturulurken seçilebilecek sorumlu bakım çalışanları da ayarlayabilirsiniz. **Tüm iş emirleri** ve **Tüm bakım istekleri** alanında gerekirse seçimi düzenleyebilirsiniz. Daha fazla bilgi için [Sorumlu bakım çalışanları](../setup-for-maintenance-requests/responsible-workers.md) bölümüne başvurun.

İş emri planlama sırasında, hangi çalışanların bir iş emriyle ilgili işleri tamamlaması gerektiğini belirlemek için farklı puanlar hesaplanır (bu puanlar,**Varlık yönetimi parametreleri** > **İş emri planlama** bağlantısında ayarlanır). İş emri planlama sırasında iki veya daha fazla tercih edilen bakım çalışanı veya sorumlu bakım çalışanı aynı puanı elde ederse, bir çalışan rasgele seçilir. Aksi takdirde, iş emrini tamamlamak için tahsis edilen daima en yüksek puanlı çalışan olur.

