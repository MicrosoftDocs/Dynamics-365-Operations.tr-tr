---
title: Tercih edilen bakım görevlilerini ayarla
description: Bu konuda Varlık Yönetimi'nde tercih edilen bakım görevlisi ayarlama işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 851cf6df576db303d9fefdcd0e732a92a019189a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354120"
---
# <a name="set-up-preferred-maintenance-workers"></a>Tercih edilen bakım görevlilerini ayarla

[!include [banner](../../includes/banner.md)]

 

İş emri planlama sırasında hangi bakım görevlisinin veya görevli grubunun iş emrini tamamlamak üzere tahsis edileceğini belirten bir tercih yapabilirsiniz. Bu işlevin kullanımı isteğe bağlıdır, ancak çalışanın yeteneklerine ve yetkinliklerine dayalı olarak işin tamamlanması için en nitelikli bakım görevlisini seçmenize yardımcı olabilir. Yalnızca, planlama zamanında uygun olan bakım görevlileri planlanır. Tercih edilen bakım görevlisi ayarı planlama sırasında bir iş emriyle eşleşirse ancak bakım görevlisi diğer işlere tahsis edilmişse, iş emri uygun durumdaki başka bir bakım görevlisi için planlanır.

Tercih edilen bakım görevlilerini ayarlamak için önce bakım görevlileri ve görevli gruplarını ayarlamanız gerekir. Bakım görevlileri ve görevli gruplarını nasıl ayarlayacağınızla ilgili açıklama için bkz. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Tercih edilen bakım görevlilerini ayarlama

Tercih edilen bakım görevlisi veya görevli grubu aşağıdakilerden biri veya daha fazlasıyla ilgili olabilir:

- görevle  
- bakım işi türü çeşidiyle  
- bakım işi türüyle  
- bakım işi türü kategorisiyle  
- varlıkla  
- varlık türüyle  

Aynı kayıt için ne kadar çok seçim yaparsanız, kurulumunuz o kadar belirgin olacaktır.

1. **Varlık Yönetimi** > **Kurulum** > **Çalışanlar** > **Tercih edilen bakım görevlileri**'ne tıklayın.

2. Yeni bir kayıt oluşturmak için **Yeni**'ye tıklayın.

3. Bir "varsayılan" bakım görevlisi veya görevli grubu oluşturarak başlayın. Bu, yalnızca **Tercih edilen bakım görevlisi grubu** alanında veya **Tercih edilen bakım görevlisi** alanında seçim yapacağınız anlamına gelir. Aşağıdaki ekran görüntüsünde, **tercih edilen bakım görevlisi grubu** olarak "Talepler" in seçildiği bir ilk kayıt örneği görürsünüz.

    [!NOTE] Varsayılan kurulum, iş emri planlaması sırasında başka, daha özel kombinasyon iş emrinin içeriğiyle eşleşirse kullanılacaktır.

4. Yeni bir kayıt oluşturmak için adım 2'yi tekrarlayın. Tercih edilen çalışan veya çalışan grubunun ayrıntı düzeyine bağlı olarak gerekli seçimleri yapın. 

    *Örnek:* Aşağıdaki ekran görüntüsünde, altıncı kayıtta, tercih edilen çalışan olarak bakım görevlisi Shawn Richardson seçilidir. Planlanan saatte uygun olması durumunda, "CH-BP1-03-02" varlığı ve "tesis değerlendirmesi " bakım işi türünü içeren bir iş emri planlamasında otomatik olarak seçilecektir.

    [!NOTE] Genellikle, iş emri planlama sırasında tercih edilen bir bakım çalışanı seçildiğinde, Varlık Yönetimi olası bir eşleşmeyi denetlemek için tüm **Tercih edilen bakım görevlileri** kayıtlarına bakar ve her zaman en belirgin birleşimi denetler. Eşleşme bulunmazsa, **Tercih edilen bakım çalışanı grubu** alanında veya **Tercih edilen bakım çalışanı** alanında bulunan "varsayılan" kayıt kullanılır.

![Şekil 1.](media/02-work-order-scheduling.png)

Ayrıca, bakım talebi veya iş emri oluşturulurken seçilebilecek *sorumlu* bakım görevlileri de ayarlayabilirsiniz. **Tüm iş emirleri** ve **Tüm bakım istekleri** alanında gerekirse seçimi düzenleyebilirsiniz. Daha fazla bilgi için bkz. [Sorumlu bakım görevlileri](../setup-for-maintenance-requests/responsible-workers.md).

İş emri planlama sırasında, hangi çalışanların bir iş emriyle ilgili işleri tamamlaması gerektiğini belirlemek için farklı puanlar hesaplanır (bu puanlar,**Varlık yönetimi parametreleri** > **İş emri planlama** bağlantısında ayarlanır). İş emri planlama sırasında iki veya daha fazla tercih edilen bakım çalışanı veya sorumlu bakım çalışanı aynı puanı elde ederse, bir çalışan rasgele seçilir. Aksi takdirde, iş emrini tamamlamak için tahsis edilen daima en yüksek puanlı çalışan olur.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]