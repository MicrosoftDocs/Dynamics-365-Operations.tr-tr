---
title: "Süreçlerdeki faaliyetler"
description: "Bu konu, işe alma işleminde kullanılabilecek faaliyetlerin çeşitli türleri hakkında bilgi sağlar."
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: tr-tr
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a>İşe alım süreçlerindeki faaliyetler

[!include[banner](../includes/banner.md)]

Faaliyetler beceri için Microsoft Dynamics 365 for Talent: Attract'te işe alma işleminin bir parçası olarak eklenebilir. Faaliyetler işlem şablonuna eklenebilir veya doğrudan işteki işe alma işlemine eklenebilir. Bir iş tanımlanınca, bir işlem şablonu seçilir ve şablona dahil edilen faaliyetler işe uygulanır. Bir şablon seçili değilse, varsayılan şablon kullanılır. Şablon uygulandıktan sonra işe alma işlemi iş üzerinde değiştirilebilir.

> [!NOTE] 
> İşlem şablonları, Kapsamlı işe alma eklentisinde kullanılabilir.

## <a name="prospect-activity"></a>Aday müşteri faaliyeti

Aday müşteri faaliyeti, aday müşterilerin bir işe eklenebilir olup olmadığını kontrol eder. Varsayılan olarak, müşteri adayları bir işe eklenebilir. Aday müşteri faaliyetini devre dışı bırakmak için **Müşteri adaylarını etkinleştir** seçeneğini **Kapalı** olarak ayarlayın. Aday müşteri faaliyeti açık olduğunda, işe alma müdürleri müşteri adaylarını ekleyebilir ve görüntüleyebilir, **Aday müşteri** sekmesi iş üzerinde gösterilir.

## <a name="application-activity"></a>Başvuru faaliyeti

İşe alma işlem şablonunda Başvuru faaliyeti gereklidir. Başvurularını gönderen veya Başvuru aşamasına eklenen adaylara e-posta göndermek için **Adaya posta gönder** seçeneğini **Açık** olarak ayarlayın.

## <a name="scheduler-activity"></a>Planlayıcı faaliyeti

Planlayıcı faaliyeti isteğe bağlıdır. Bu faaliyetin iki bileşeni vardır: Aday erişilebilirliği ve Zamanlama. Aday erişilebilirliği bileşeni, adayın erişilebilirliğini istemek için e-posta kullanmanıza olanak sağlar. Zamanlama bileşeni, aday ve işe alma ekibiyle görüşmeler planlanma yeteneğini sağlar. Planlayıcı faaliyetinde, aşağıdaki seçenekler yapılandırılabilir: **Aday erişilebilirliği iste**, **Çevrimiçi toplantı** ve **Adaya posta gönder**.

- Aday erişilebilirliğini talep etmek üzere e-posta göndermek için **Aday erişilebilirliği iste** seçeneğini **Açık** olarak ayarlayın. Seçeneği **Kapalı** olarak ayarlarsanız bu adım, işteki işe alma işleminde görüntülenmez.
- Canlı akış veya Skype Kurumsal kullanarak bir konferans çağrısında **Çevrimiçi toplantı** alanını **Skype Kurumsal** olarak ayarlayın. Doğru **Skype Toplantısına katıl** bağlantısı, daha sonra görüşme yapılanlara göndereilecek olan görüşme toplantısı isteğine eklenir.
- Adaylara planlamayı sonlandırmak üzere e-posta göndermek için **Adaya posta gönder** seçeneğini **Açık** olarak ayarlayın. Seçeneği **Kapalı** olarak ayarlarsanız, adaylar yalnızca Aday portalına giriş yaptığında görüşme planını alacak.

## <a name="feedback-activity"></a>Geri bildirim faaliyeti

Geri bildirim faaliyeti isteğe bağlıdır. Bu faaliyet, görüşmeye katılanların bir başvuran için öneriler girmesine olanak tanır. Ayrıca sahip oldukları geri bildirim yorumları da girebilir. **İşe Alım Ekbinden katılımcı geri bildirimi al** seçeneğini açarsanız işe alan, işe alma yöneticisi ve görüşmeciler Geri Bildirim faaliyetine otomatik olarak girer. Kuruluşlar, görüşmeye katılanların kendilerine ait geri bildirim göndermeden önce diğer kişilerin geri bildirimlerini görüntülemesine izin verebilir. Kuruluşlar ayrıca görüşmecilerin geri bildirimlerini gönderdikten sonra düzenlemesine de izin verir.

## <a name="interview-activity"></a>Görüşme faaliyeti

Görüşme faaliyeti isteğe bağlıdır. Bu faaliyetin üç bileşeni vardır: Aday erişilebilirliği, Zamanlama ve Geri Bildirim. Aday erişilebilirliği bileşeni, adayın erişilebilirliğini istemek için e-posta kullanmanıza olanak sağlar. Zamanlama bileşeni, aday ve işe alma ekibiyle görüşmeler planlanma yeteneğini sağlar. Planlayıcı faaliyetinde, aşağıdaki seçenekler yapılandırılabilir: **Aday erişilebilirliği iste**, **Çevrimiçi toplantı** ve **Adaya posta gönder**.

- Aday erişilebilirliğini talep etmek üzere e-posta göndermek için **Aday erişilebilirliği iste** seçeneğini **Açık** olarak ayarlayın. Seçeneği **Kapalı** olarak ayarlarsanız bu adım, işteki işe alma işleminde görüntülenmez.
- Canlı akış veya Skype Kurumsal kullanarak bir konferans çağrısında **Çevrimiçi toplantı** alanını **Skype Kurumsal** olarak ayarlayın. Doğru **Skype Toplantısına katıl** bağlantısı, daha sonra görüşme toplantısı isteğine eklenir.
- Adaylara planlamayı sonlandırmak üzere e-posta göndermek için **Adaya posta gönder** seçeneğini **Açık** olarak ayarlayın. Seçeneği **Kapalı** olarak ayarlarsanız, adaylar yalnızca Aday portalına giriş yaptığında görüşme planını alacak.

Geri Bildirim bileşeni, kişilerin bir başvuran için öneriler girmesini sağlar. Ayrıca sahip oldukları geri bildirim yorumları da girebilir. **İşe Alım Ekbinden katılımcı geri bildirimi al** seçeneğini açarsanız işe alan, işe alma yöneticisi ve görüşmeciler Geri Bildirim bileşenine otomatik olarak girer. Kuruluşlar, görüşmeye katılanların kendilerine ait geri bildirim göndermeden önce diğer kişilerin geri bildirimlerini görüntülemesine izin verebilir. Kuruluşlar ayrıca görüşmecilerin geri bildirimlerini gönderdikten sonra düzenlemesine de izin verir.

## <a name="powerapps-activity"></a>PowerApps faaliyeti

PowerApps faaliyeti, Microsoft PowerApps uygulamasını işe alma işlemine gömmenizi sağlar. Uygulama tüm başvuranlar, yalnızca dahili başvuranlar, yalnızca harici başvuranlar veya hiçbir başvuran için gerekli şeklinde ayarlanabilir. Uygulama gerekli olarak işaretlenirse, aşama ileriye taşınmadan önce tamamlanmış olması gerekir. Uygulamayı gerekli olarak işaretli değilse, faaliyet isteğe bağlı bir adımdır ve uygulama tamamlanmasa bile aşama ilerleyebilir.

PowerApps faaliyetini işe alma sürecini kaydetmek için bir PowerApps kimliği girmeniz gerekir. PowerApps kimliği bulmak için [PowerApps](https://web.powerapps.com) adresine gidin, **Uygulamalar**'ı, ardından **Ayrıntılar**'ı seçin.

**Bu faaliyet için katılımcı eklenmesine izin ver** seçeneğini belirlerseniz PowerApps kullanan bir uygulama için ek katılımcılar eklenebilir. Örneğin, bir kuruluş teknik görevler için bir görüşme sorusu kitaplığı olan PowerApps uygulaması oluşturdu. Kuruluş şimdi yeni bir yazılım geliştirici işe alıyor ve yazılım geliştirici rolü için işe alma işlemine PowerApps faaliyeti ekledi. **Bu faaliyet için katılımcı eklenmesine izin ve** seçeneği işaretliyse, yazılım geliştirici rolüne başvuranı görüntüleyen bir işveren veya işe alma yöneticisi PowerApps faaliyetine kişiler ekleyebilir. Bu kişiler, görüşme soruları olan uygulamayı daha sonra görebilir.

> [!NOTE]
> PowerApps faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

## <a name="youtube-activity"></a>YouTube faaliyeti

YouTube faaliyeti, işe alma işleminin parça olarak YouTube videosu paylaşmanıza olanak sağlar. İşe alma işlemine YouTube faaliyetini kaydetmek için YouTube videosu URL'sini belirtmeniz gerekir. PowerApps faaliyeti söz konusu olduğunda, katılımcıların faaliyete eklenmesini sağlayabilirsiniz. **Yalnızca adaya göster** seçeneğini belirlerseniz video yalnızca aday deneyimi parçası olarak gösterilir. Attract'taki işe alma işleminde gösterilmez.

> [!NOTE]
> YouTube faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

## <a name="web-content-activity"></a>Web içeriği faaliyeti

Web içeriği faaliyeti, işe alma işlemine çevrimiçi içerik gömmenize olanak tanır. İşe alma işlemine Web içeriği faaliyetini kaydetmek için içeriğin URL'sini belirtmeniz gerekir. PowerApps ve YouTube faaliyeti söz konusu olduğunda, katılımcıların faaliyete eklenmesini sağlayabilirsiniz. **Yalnızca adaya göster** seçeneğini belirlerseniz içerik yalnızca aday deneyimi parçası olarak gösterilir. Attract'taki işe alma işleminde gösterilmez. Gösterilen içerik boyutunu seçebilirsiniz.

> [!NOTE]
> Web içeriği faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

## <a name="microsoft-forms-activity"></a>Microsoft Forms faaliyeti

Microsoft Forms faaliyeti, Microsoft Forms formunu işe alma işlemine gömmenizi sağlar. Microsoft Forms testler, anketler ve oylamalar oluşturmanıza olanak tanır. İşe alma işlemine Microsoft Forms faaliyetini kaydetmek için formun URL'sini belirtmeniz gerekir. PowerApps, YouTube ve Web içeriği faaliyeti söz konusu olduğunda, katılımcıların faaliyete eklenmesini sağlayabilirsiniz. **Yalnızca adaya göster** seçeneğini belirlerseniz form yalnızca aday deneyimi parçası olarak gösterilir. Attract'taki işe alma işleminde gösterilmez.

Microsoft Forms'da yazarlar, kurum dışındaki kullanıcıların anket veya testine yanıt verebilmesi için ayarlarını değiştirebilir. Bu durumda, kullanıcılar yanıtlarını anonim olarak gönderir. Anket veya testinizi kimin yaptığını görmek isterseniz yanıtlayanların adlarını anket veya testin bir parçası olarak girmesini isteyebilirsiniz.

> [!NOTE]
> Microsoft Forms faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

