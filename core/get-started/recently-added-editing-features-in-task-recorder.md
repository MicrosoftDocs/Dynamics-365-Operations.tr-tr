---
title: "Görev kaydedicisine en son eklenen düzenleme özellikleri"
description: "Görev kılavuzları oluşturmak için görev kaydedici kullanıyorsanız, bu konu içinde tanımlanan işlevi kullanarak dosyalarınızı daha verimli bir şekilde düzenleyebilirsiniz."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3be54879494948f75b192fcc22239b9064173220
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Görev kaydedicisine en son eklenen düzenleme özellikleri

[!include[banner](../includes/banner.md)]


Görev kılavuzları oluşturmak için görev kaydedici kullanıyorsanız, bu konu içinde tanımlanan işlevi kullanarak dosyalarınızı daha verimli bir şekilde düzenleyebilirsiniz.

Bu özellikler **Ayarlar &gt; Görev Kaydedici &gt; Kaydı düzenle** menüsünde bulunur.

-   Dosyanın tamamını tekrar kaydetmeden adımlar ekleyin.
-   Bir alt görevin altındaki adımları dosyanın tamamını yeniden kaydetmeden taşıyın.
-   Kayıt adı ve açıklaması alanlarını daraltın.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Dosyanın tamamını tekrar kaydetmeden adımlar ekleme
Artık görev kılavuzunda istediğiniz yere tüm dosyayı yeniden oynatmadan veya yeniden kaydetmeden bir adım ekleyebilirsiniz.

1.  Ardından yeni adımı eklemek istediğiniz adımı seçin. Adımın vurgulandığından emin olun.

Görev kaydedicinin bir adım eklemesi için doğru sayfanın açık olmasını sağlamanız gerekir. Doğru sayfa, yeni adımın gerçekleştiği sayfadır. Görev kaydedicide hangi sayfanın etkin olduğunu belirleyen bir mekanizma vardır ve doğru sayfanın açık olmaması durumunda işlevi devre dışı bırakır. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Doğru sayfadayken **Adım ekle** kullanılabilir olur.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. **Adım ekle**'ye tıklayın.

**Adım ekle**'ye tıkladığınızda, görev kaydedici kayıt moduna geçer. Kullanıcı arabiriminde yapılan eylem artık kaydedilir adımlar olarak yerine eklenir.

3. **Durdur**'a tıklayın.

İşlemi tekrarlayabilir, gerektiği kadar çok adım ekleyebilir veya alt görev taşıyabilirsiniz (alt görevler için aşağıya bakın).

4. Görev kılavuzu düzenlemeyi tamamladığınızd **Düzenleme bitti**'ye tıklayın ve görev kılavuzunu kaydetmek veya yayımlamak için seçeneklerden birini seçin.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Bir alt görevin altındaki adımları dosyanın tamamını yeniden kaydetmeden taşıyın.
Bir alt görevin altındaki adımları dosyanın tamamını yeniden oynatmadan veya yeniden kaydetmeden taşıyabilirsiniz. Mevcut bir adım bloğunu gruplandırmak isterseniz alt görev adımını veya son alt görev adımını da taşıyabilirsiniz.

1.  Taşımak istediğiniz adımı veya alt görev adımını seçin. Adımın vurgulandığından emin olun.
2.  Elipse tıklayın ve ardından **Adımı şundan sonraya taşı**'ya tıklayın.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Adımı veya alt görev adımını hangi adım veya alt görev adımından sonraya taşımak istediğinizi seçin. Görev kaydedici adımı taşır.

4. Son alt görev adımını taşımak için seçin, elipse tıklayın, **Adımı şundan sonraya taşı**'ya tıklayın ve ardından son alt görev adımının hangi adımdan sonra geleceğini seçin.

Görev kılavuzundaki ilk adımın bir alt görev içinde olmasını istiyorsanız, ikinci adım olarak bir alt görev oluşturun ve sonra ilk adım onun içine taşıyın. İstediğiniz kadar çok adım veya alt görev ekleyebilir ya da taşıyabilirsiniz.

5. Görev kılavuzu düzenlemeyi tamamladığınızd **Düzenleme bitti**'ye tıklayın ve görev kılavuzunu kaydetmek veya yayımlamak için seçeneklerden birini seçin.

## <a name="collapse-recording-name-and-description"></a>Kayıt adı ve açıklaması alanlarını daraltma
**Kayıt adı** ve **Kayıt açıklaması** alanlarını genişletebilir veya daraltabilirsiniz. Bu alanlar daraltıldığında, Görev kaydedicinin düzenleme bölmesinde daha fazla adım görünür hale gelir. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Ayrıca bkz.
--------

[Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Görev kaydedici hızlı başvuru](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)




