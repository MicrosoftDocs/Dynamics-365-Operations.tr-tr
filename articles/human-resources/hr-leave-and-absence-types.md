---
title: İzin ve devamsızlık türlerini yapılandırma
description: Dynamics 365 Human Resources'ta çalışanların götürebileceği izin tiplerini ayarlayın.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 098f614da80a1e7e3e31b30cea707ecfbd5b0a70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056624"
---
# <a name="configure-leave-and-absence-types"></a>İzin ve devamsızlık türlerini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

9. **Takvim rengi** altında, izin ve devamsızlık takvimlerinde bu izin türü için görüntülenecek rengi seçin. 

10. **Askıya alma ilişkileri** altında , bu tür iznin başka bir izin türünü askıya al veya başka bir izin türü tarafından askıya alınması seçeneklerinden birini belirleyin. Askıya alma türü için devamsızlık yetkisi isteği gönderildiğinde, askıya alma türü için bir yeniden gönderme askıya alma işlemi otomatik olarak oluşturulur. 

10. **Kaydet**'i seçin.

## <a name="configure-leave-type-rules"></a>İzin türü kurallarını yapılandırma

1. İzin türü için yuvarlama seçeneklerini ayarlayın. **Yok**, **yukarı**, **aşağı** ve **en yakın** seçenekleri vardır. Ayrıca, izin tipiyle ilgili Yuvarlama Duyarlığı da ayarlayabilirsiniz.

2. İzin türü için **tatil düzeltmesi** ayarlayın. Bu seçeneği belirlediğinizde, izin türü için sürenin nasıl tahakkuk ettirildiğini belirlemek için İnsan Kaynakları iş gününe denk düşen tatilleri kullanır. Örneğin, Noel günü Pazartesi gününe denk gelirse İnsan Kaynakları tahakkukları işlerken izin türünden bir günü çıkarır.

   Tatilleri çlışma zmaanı takviminde ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)
   
 3. İzin türü için **ileriye doğru izin türü** ayarlayın. Bu seçeneği belirlediğinizde, tüm ileri düzey bakiyeleri belirtilen izin türüne aktarılır. İleriye yönelik izin türü de, bırak ve devamsızlık planına dahil edilmesi gerekir. 
 
 4. İzin türü için **süre sonu kurallarını** tanımlayın. Bu seçeneği konfigüre ettiğinizde, gün veya ay birimini seçebilir ve bitiş tarihi için süreyi ayarlayabilirsiniz. Ayrıca, sona erme kuralının geçerlilik tarihini ayarlayabilirsiniz. Geçerlilik tarihi, izin süresinin dolmasını işleyen toplu işlemin ne zaman çalıştırılmaya başlayacağını veya kuralın ne zaman geçerli olacağını belirlemek için kullanılır. Toplu işlem işlenecek şekilde ayarlandıktan sonra sona erme süresi her zaman izin planı başlangıç tarihinde gerçekleşir. Örneğin, plan başlangıç tarihi 1/1/2020 olabilir ancak kural 6/1/2020'ye kadar oluşturulmamıştır. Geçerlilik tarihi 6/1/2020 olarak ayarlandığında kural bir sonraki yıl sınırı olan 1/1/2021 tarihinde işlenir. Bitiş tarihinde varolan tüm izin bakiyeleri izin dışında bırakılacak ve bırakma bakiyesine yansıtılır. 
 
## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin ve devamsızlık planı oluşturma](hr-leave-and-absence-plans.md)
- [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)
- [İzni askıya alma](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
