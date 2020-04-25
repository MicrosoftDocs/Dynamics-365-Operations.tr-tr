---
title: İzin ve devamsızlık türlerini yapılandırma
description: Dynamics 365 Human Resources'ta çalışanların götürebileceği izin tiplerini ayarlayın.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198062"
---
# <a name="configure-leave-and-absence-types"></a>İzin ve devamsızlık türlerini yapılandırma

Dynamics 365 Human Resources'ta izin türleri, bir personelin bildirebileceği çeşitli türde devamsızlıkları tanımlayabilir. İzin tiplerini kuruluşunuzun gereksinimlerine göre uyarlayabilirsiniz. İzin türleri örnekleri:

- Ücretli süre kesintisi (PTO)
- Ücretsiz izin
- Ücretli izin
- Hastalık izni
- Tıbbi izin
- Aile izni
- Kısa süreli engellilik
- Matem izni

## <a name="add-a-leave-type"></a>İzin türü Ekle

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum** altında, **izin ve devamsızlık tipleri**'ni seçin.

3. **Yeni**'yi seçin.

4. **Tür** altındaki izin türü için ad girin, **iş akışı kimliğinden** bir iş akışı seçin ve **açıklama** altında bir açıklama girin.

5. **Genel** olarak, **kategori** açılan menüsünde **yok**, **zamanlanmış** veya **zamanlanmamış** seçeneğini belirleyin.

6. **Kazanç kodu** açılan menüsünden bir kazanç kodu seçin.

7. **Neden kodu gerekli** olduğunda, neden kodu olmasını istiyorsanız bunu seçin. Neden kodları olmasını istiyorsanız, bunları eklemeniz gerekebilir. **Neden kodları** altında, **Ekle**'yi seçin, bir neden kodu seçin ve sonra da yanındaki **etkin** onay kutusunu seçin.

8. **Seçili rollere erişimi kısıtlamak** altında, erişimi kısıtlamak istediğinizi seçin. Sonra, **bu izin türü için güvenlik rolleri** altında güvenlik rollerini seçin. Güvenlik rolleri, bu yordamda daha önce **iş akışı kodu** altında seçtiğiniz iş akışında tanımlanmıştır.

9. **Kaydet**'i seçin.

## <a name="configure-leave-type-rules"></a>İzin türü kurallarını yapılandırma

1. İzin türü için yuvarlama seçeneklerini ayarlayın. **Yok**, **yukarı**, **aşağı** ve **en yakın** seçenekleri vardır. Ayrıca, izin tipiyle ilgili Yuvarlama Duyarlığı da ayarlayabilirsiniz.

2. İzin türü için **tatil düzeltmesi** ayarlayın. Bu seçeneği belirlediğinizde, izin türü için sürenin nasıl tahakkuk ettirildiğini belirlemek için İnsan Kaynakları iş gününe denk düşen tatilleri kullanır. Örneğin, Noel günü Pazartesi gününe denk gelirse İnsan Kaynakları tahakkukları işlerken izin türünden bir günü çıkarır.

   Tatilleri çlışma zmaanı takviminde ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)
   
## <a name="configure-preview-features"></a>Önizleme özelliklerine yapılandırma

İzin ve devamsızlık için Önizleme özelliklerini etkinleştirdiyseniz, bu ayarları sizin için de konfigüre etmeniz gerekir.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Transfer edilecek devir bakiyeleri için izin türünü seçin. Ayrıca, devir için yeni bir izin türü oluşturabilirsiniz. 

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin ve devamsızlık planı oluşturma](hr-leave-and-absence-plans.md)
- [Çalışma süresi takvimleri oluşturma](hr-leave-and-absence-working-time-calendar.md)
