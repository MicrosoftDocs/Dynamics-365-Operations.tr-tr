---
title: "Görev Kaydedicisi düzenleme özellikleri en son eklenen"
description: "Görev kılavuzları oluşturmak için Görev Kaydedici kullanıyorsanız, daha fazla verimli bir şekilde bu wiki içinde tanımlanan işlevselliği kullanarak dosyalarınızı düzenleyebilirsiniz."
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
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Görev Kaydedicisi düzenleme özellikleri en son eklenen

Görev kılavuzları oluşturmak için Görev Kaydedici kullanıyorsanız, daha fazla verimli bir şekilde bu wiki içinde tanımlanan işlevselliği kullanarak dosyalarınızı düzenleyebilirsiniz.

Bu özellikler kullanılabilir **ayarları &gt;Görev Kaydedici &gt;düzenleme kayıt** menüsü.

-   Dosyanın tamamını yeniden kaydetmeden adımlar ekle.
-   Bir alt görevin altındaki adımları dosyanın tamamını yeniden kaydetmeden taşıyın.
-   Kayıt adı ve Açıklama alanlarını daraltın.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Dosyanın tamamını rerecording olmadan adımlar Ekle
Artık bir adım herhangi bir görev Kılavuzu'nda kayıttan yürütme veya dosyanın tamamını yeniden kayıt ekleyebilir.

1.  Eklenecek yeni adım sonra istediğiniz adıma seçin. Adım vurgulandığından emin olun.

Bir adımı eklemek, görev Kaydedicisi'ni açmak doğru sayfa olması gerekir. Doğru sayfa yeni adım oluştuğu sayfasıdır. Görev Kaydedicisi ne etkin sayfa, doğru sayfa açık değilse işlevlerini devre dışı bırakır belirler ve bir mekanizma vardır. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Doğru sayfa üzerinde olduğunda **Insert step** kullanılabilir.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. ' I **INSERT adım**.

Tıklattığınızda **Insert step**, Görev Kaydedici kayıt moduna geçer. Kullanıcı arabiriminde yapılan eylem şimdi kaydedilir ve yerinde adımlar eklenir.

3. ' I **Stop**.

(Aşağıdaki alt görevler için bakın) gerektiği gibi alt görevler olabildiğince çok sayıda adım eklenmesini veya işlemi yineleyebilirsiniz.

4. Tamamladığınızda, görev kılavuzu düzenleme'yi tıklatın **düzenleme yapılan**ve görev rehberi yayımlamak veya kaydetmek için seçeneklerden birini seçin.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Dosyanın tamamını rerecording olmadan adımları altında bir alt görevi taşı
Kayıttan yürütme veya dosyanın tamamını yeniden kayıt adımları altında bir alt görev taşıyabilirsiniz. Varolan bir engelleme adımları gruplamak istiyorsanız son alt görev adım veya alt görev adım taşıyabilirsiniz.

1.  Adım ya da taşımak istediğiniz alt görev adım seçin. Adım'da vurgulandığından emin olun.
2.  Üç noktayı tıklatın, sonra'ı **taşıma adım sonra**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Adım veya alt görev veya adım adım sonra taşımak istediğiniz alt görev adım seçin. Görev Kaydedici adım taşır.

4. Son alt görev adım taşımak, nesneyi seçin, üç noktayı tıklatın, tıklatın **taşıma adım sonra**ve sonra son alt görev adım olmasını istediğiniz adıma seçin.

İlk adımda görev kılavuzu içinde bir alt görev olmasını istiyorsanız, bir alt görev adımı ikinci adım olarak oluşturun ve sonra ilk adım içine taşıyın. Ekleyebilir veya kadar adımları veya gerektiği gibi alt görevleri taşıyın.

5. Tamamladığınızda, görev kılavuzu düzenleme'yi tıklatın **düzenleme yapılan**ve görev rehberi yayımlamak veya kaydetmek için seçeneklerden birini seçin.

## <a name="collapse-recording-name-and-description"></a>Daralt kayıt adı ve açıklaması
Genişletip daraltabileceğiniz **kayıt adı** ve **açıklama kaydı** alanlar. Bu alanlar daraltıldığında, daha fazla adım görev Kaydedicisi düzenleme bölmesi görünür hale gelir. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Ayrıca bkz.
--------

[Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Görev Kaydedici Hýzlý Baþvuru](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


