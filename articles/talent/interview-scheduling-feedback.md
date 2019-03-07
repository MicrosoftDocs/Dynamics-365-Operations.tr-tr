---
title: Mülakat planlama ve geri bildirim
description: Bu konu, Attract içinde mülakat zamanlama ve geribildirim etkinlikleri hakkında bilgi sağlar.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2019
ms.locfileid: "374996"
---
# <a name="interview-scheduling-and-feedback"></a>Mülakat planlama ve geri bildirim

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Planlayıcı faaliyeti

Planlama etkinliği, isteğe bağlıdır ve iki bileşeni vardır: Aday uygunluk talebi ve Zamanlama. Aday erişilebilirliği bileşeni, adayın erişilebilirliğini istemek için e-posta kullanmanıza olanak sağlar. Zamanlama bileşeni, aday ve işe alma ekibiyle görüşmeler planlanma yeteneğini sağlar.

### <a name="candidate-availability-request"></a>Aday uygunluk talebi

Adayların uygunluğunu talep eden bir e-postayı göndermek için **Aday uygunluğu talep et** alanını seçin. Bu alan seçili değilse, bu adım iş için işe alım sürecinde gösterilmeyecektir.

Uygunluk talebini göndermek için **Talebi gönder**'i tıklatın, kullanılabilir tarihleri ve bir e-posta şablonu seçin ve e-postayı adaya gönderin.

[![Aday uygunluk talebi göndermek için Attract işe alan görünümü](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Aday, talebe yanıt vermek için bir e-posta alırsa, aday portalına giriş yapabilir, uygun oldukları tarihleri seçebilir ve **Gönder** üzerine tıklayabilirler.

### <a name="schedule"></a>Planlama
Mülakat döngüsünü hızlıca oluşturmak mülakatı yapanlara ve adaylara göndermek için mülakat planlayıcısı için birden fazla yapılandırma mevcuttur.

1. **Plan oluştur** üzerine tıklayın ve **Görüşmeciler ekle** kutusunda, mülakat döngüsünün katılımcısı olacak tüm görüşmecileri listeleyin.
[![Bir mülakat döngüsü zamanlamaya başlatmak için Attract işe alan görünümü](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Aday, mülakat talebi uygunluğuna yanıt verdiyse, **Mülakat tarihi** alanı seçimleriyle önceden doldurulmuş olacaktır. Gerekirse, farklı bir tarih seçebilirsiniz.
    
    **Bunu bir panel görüşmesi yap** alanını seçerseniz, soldaki görüşmeci grubu, mülakatı oluşturmak için tek bir panel döngüsüne taşınır. Bu nedenle, görüşmeler için belirli bir sıra tanımlamanız gerekir.
    
    Görüşme planının katılımcıların ihtiyaçlarını en iyi şekilde karşılayacak şekilde düzenlenmesi gerekir. Bu, dahili bir adaysa, uygunluklarını zamanlama önerisinin bir parçası olarak dahil edebilirsiniz.
    
    Bir çevrimiçi toplantı yapmak için **Skype toplantıları ekle** alanını seçin ve her bir görüşmeci bir **Skype for Business** bağlantısına sahip olacaktır.

2. Her bir görüşme etkinliği için bir görüşme süresi seçin ve sonra zamanlamayı başlatmak için **Tamam** üzerine tıklayın.

    **Öneriler** seçilirse, öneriler gösterilir ve görüşme kılavuzu önceden doldurulacaktır. Seçilen tüm görüşmecilerin geçerli takvim uygunluğunu görebileceksiniz. Dahili bir adaysa, adayın takvimini de görebileceksiniz.

3. Öneri mevcut değilse, **Görüşmeciler** sekmesinde, bir zaman aralığına tıklayın, görüşme başlığını, ayrıntılarını girin ve konum ayrıntılarını gerektiği gibi doldurun. Görüşme için **Skype for Business** bağlantısını dahil etmeyi de seçebilirsiniz.

4. Ek görüşmeciler dahil etmek için bir veya birden fazla görüşmeciyi seçmek için **Görüşme ekle** kılavuz sütununa tıklayın. Bir görüşmeyi döngüden çıkarmak için üç nokta (...) seçeneğini kullanabilirsiniz.
    
5. Görüşmeler farklı bir saat diliminde zamanlanmışsa, gerekli şehir/saat dilimini sağ üstteki açılır menü listesinden seçin. Görüşmeci uygunluk kılavuzu, yeni saat dilimini yansıtmak için güncelleştirilir. Bu saat dilimi seçimi şimdi **Görüşme özeti** görünümünde de görünecektir, bu da aday ve görüşmeciler ile paylaşılacaktır. 

6. İlgili görüşmecilere toplantı davetiyelerini göndermek için **Görüşmecilere gönder**'i tıklatın.

    Görüşme talepleri görüşmecilere gönderildikten sonra, doğrudan aldıkları e-posta daveti içinden yanıt verebilirler.

    >[!NOTE]
    > Tüm 1:1 görüşmeler için görüşmeci, görüşme talebine yanıt vermediyse (kabul veya ret) her 24 saatte bir hatırlatma görüşmecilere gönderilir.

    > Tüm panel görüşmeleri için görüşme talebini yanıtlamak üzere otomatik hiçbir anımsatıcı yoktur. Bir anımsatmayı el ile tetiklemek için görüşmeyi düzenleyin ve **Güncelleştir ve Gönder** seçeneğini kullanarak talebi görüşmecilere geri gönderin.

    Görüşmeci yanıtları Attract içinde yakalanır ve gösterilir. Bir görüşmeci daveti reddederse, değişiklik yapmanız için size bildirilir. Yanıtlarını **Planlayıcı** kılavuz görünümünde görmek için kabarcık simgesine tıklayın.

[![Attract bir işe alanın bir görüşmecinin yanıtını görmek için](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Görüşme planı hazırlandıktan ve aday ile paylaşılmaya hazır olduktan sonra **Adaya gönder** üzerine tıklayın. Görüşmeci adlarını ve sıralarını aday ile paylaşmayı veya gizlemeyi seçebilirsiniz.

8. Bir e-posta şablonu seçin ve görüşme özetini adaya gönderin. Aday, bu bilgiyi e-postada ve aday portalında görüntüleyebilirler.
    
>[!NOTE] 
> Bir adayın takvim uygunluğu yalnızca aday dahiliyse gösterilir. Benzer şekilde, yalnızca dahili adaylar görüşme planı önerilerini geliştirmek için kullanılabilir. Şu anda, adaylar (dahili veya harici), e-posta toplantı daveti almazlar, bunun yerine adaylar yalnızca görüşmenin özetini alırlar.

## <a name="feedback-activity"></a>Geri bildirim faaliyeti

Geribildirim etkinliği bir iş şablonunda isteğe bağlıdır. Bu faaliyet, görüşmeye katılanların bir başvuran için öneriler veya geribildirim yorumları girmesine olanak tanır. **İşe Alım Ekbinden katılımcı geri bildirimi al** alanını seçerseniz, işe alımcı, işe alım yöneticisi ve görüşmeciler otomatik olarak geribildirim etkinliğine eklenir. Kuruluşlar, görüşmeye katılanların kendilerine ait geri bildirim göndermeden önce diğer kişilerin geri bildirimlerini görüntülemesine izin verebilir. Kuruluşlar ayrıca görüşmecilerin geri bildirimlerini gönderdikten sonra düzenlemesine de izin verir. Görüşmecilerin, gerçekleştirmiş oldukları görüşmeler için geribildirimlerini, bir iş şablonunun yapılandırma ön ayarı için girmeleri hatırlatılır. İşe alım müdür veya bir işe alımcı da görüşmecinin geribildirim girmesini hatırlatabilir.

## <a name="interview-activity"></a>Görüşme faaliyeti

Görüşme etkinliği, üç bileşene sahip isteğe bağlı bir etkinliktir: Aday uygunluk talebi, Planlama ve Geribildirim. İş şablonunda görüşme etkinliğini, adayın uygun talebi, zamanlamasının tamamını istiyorsanız kullanın. ve geribildirim olarak, işlemin bir parçası olarak bunları işe alma sürecinin tekil parçası olarak kullanır.
