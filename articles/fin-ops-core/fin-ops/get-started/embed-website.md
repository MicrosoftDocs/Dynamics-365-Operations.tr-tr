---
title: Üçüncü taraf uygulamaları katıştırma
description: Bu konu, ürün işlevselliğini artırmak için üçüncü taraf uygulamaların istemciye nasıl katıştırılacağını açıklar.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f47fb6a2fdb586fbc9f25938c3b9c1cfc16ddc1af432b91621421bd829b23925
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737811"
---
# <a name="embed-third-party-apps"></a>Üçüncü taraf uygulamaları katıştırma

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Birçok müşteri, işlerini yürütmek için bir dizi uygulama kullanır. Bu uygulamalardan bazıları, Finance and Operations uygulamalarla birlikte çalışan üçüncü taraf web uygulamalardır. Daha kusursuz bir kullanıcı deneyimi sağlamak için, bu üçüncü taraf uygulamaları doğrudan Finance and Operations uygulamalarınıza katıştırmak için **(Önizleme) tam sayfa uygulamalar** özelliğini kullanabilirsiniz (üçüncü taraf uygulamaların katıştırmaya izin verdikleri varsayılır). Böylece, kullanıcılar sekmeler veya pencereler arasında geçiş yapmak zorunda kalmadan gereksinim duydukları web sitelerine ve uygulamalara erişebilirler.

Ürüne üçüncü taraf uygulamaları katıştırabilmeniz için, Özellik yönetiminde **(Önizleme) Tam sayfa uygulamalar** özelliğini açmanız gerekir. Ardından bir üçüncü taraf uygulamasını veya web sitesini katıştırmak için aşağıdaki yöntemlerden birini kullanabilirsiniz. Bu yöntemler, tuval uygulamalarını Microsoft Power Apps'ten Finance and Operations uygulamalarına katıştırmak için kullanılan yöntemlere benzer.

- Varolan bir sayfada uygulamayı veya web sitesini yeni bir sekme sayfası olarak katıştırma (pivot sekmesi, hızlı sekme, dikey pencere veya çalışma alanı bölümü).
- Panodan uygulama veya web sitesi için yeni bir tam sayfa deneyimi oluşturun.

## <a name="embed-a-website-on-an-existing-page"></a>Varolan bir sayfaya web sitesi katıştırma

Sistemdeki varolan bir sayfaya katıştırılmış bir uygulama eklemek istiyorsanız bu prosedürü kullanın.

1. Uygulamayı katıştırmak istediğiniz sayfayı açın.
2. **Bir uygulama ekle** bölmesini açın:

    1. **Kişiselleştirme** araç çubuğunu açmak için **Seçenekler**'i ve ardından **Kişiselleştir**'i seçin.
    2. **Diğer \> Bir uygulama ekle**'yi seçin.

3. Uygulamayı eklemek istediğiniz sayfa bölgesini seçin. Bu bölge, bir pivot sekmesi, hızlı sekme, dikey pencere veya çalışma alanı bölümü için *sekme konteyneri* olmalıdır.
4. **Web sitesi**'ni seçin.
5. Katıştırılmış uygulamayı yapılandırın:

    - **Ad** – Katıştırılmış uygulamayı içeren sekme için gösterilmesi gereken metni girin. Bu metnin genellikle uygulamanın adı olmasını istersiniz.
    - **URL** – Uygulamanın konumunu belirtin.

    > [!IMPORTANT]
    > - Güvenlik nedenleriyle, URL'de Köprü Metni Aktarım Protokolü Güvenli (HTTPS) kullanılmalıdır.
    > - Uygulama veya web sitesinin katıştırmaya izin verecek şekilde yapılandırılması gerekir.

6. Uygulamayı sayfaya katıştırmak için **Kaydet**'i seçin. Uygulama, gruba son sekme veya bölüm olarak eklenir.
7. Uygulamanın beklendiği gibi göründüğünü onaylayın. Uygulama görüntülenmiyorsa, bu konunun ilerleyen bölümlerinde yer alan [Sorun giderme](#troubleshooting) bölümüne bakın.
8. Görünüm seçiciyi açın ve **Kaydet**'i (uygulama, geçerli görünümle ilişkilendirilmeliyse) veya **Farklı kaydet**'i (uygulamayı farklı bir görünüme kaydetmek için) seçin.

    Sayfanın görünüm seçicisi yoksa (örneğin, sayfa bir iletişim kutusu veya çalışma alanı ise) bu adımı atlayabilirsiniz.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Web sitesini panodan tam sayfa deneyimi olarak katıştırma

Katıştırmak istediğiniz uygulama varolan bir sayfayla ilişkili değilse veya Finance and Operations uygulaması içinde uygulama için tam sayfa bir deneyim istiyorsanız bu prosedürü kullanın.

1. Panoyu açın.
2. Sayfayı seçin ve basılı tutun (veya sağ tıklayın), **Kişiselleştir**'i seçin ve ardından **Sayfa ekle**'yi seçin.
3. **Sayfa ekle** bölmesinde, **Web sitesi**'ni seçin.
4. Katıştırılmış uygulamayı yapılandırın:

    - **Ad** – Panoda katıştırılmış uygulama için eklenen kutucukta gösterilmesi gereken metni girin. Bu metnin genellikle uygulamanın adı olmasını istersiniz.
    - **URL** – Uygulamanın konumunu belirtin.

    > [!IMPORTANT]
    > - Güvenlik nedenleriyle, URL'de HTTPS kullanması gerekir.
    > - Uygulama veya web sitesinin katıştırmaya izin verecek şekilde yapılandırılması gerekir.

5. Uygulamayı panoya yeni bir kutucuk olarak eklemek için **Kaydet**'i seçin.
6. Panoda yeni kutucuğu seçin ve uygulamanın beklendiği gibi göründüğünü onaylayın. Uygulama görüntülenmiyorsa, bu konunun ilerleyen bölümlerinde yer alan [Sorun giderme](#troubleshooting) bölümüne bakın.

## <a name="sharing-embedded-apps"></a>Katıştırılmış uygulamaları paylaşma

Önceki bölümlerde açıklanan yöntemlerden birini kullanarak bir uygulamayı katıştırdıktan sonra, görünümü sistemdeki diğer kullanıcılarla paylaşmak isteyebilirsiniz. Katıştırılmış bir uygulamayı paylaştırmak için, aşağıdaki yöntemlerden birini kullanın:

- **Görünümü yayımlayın (Önerilen):** Katıştırılmış uygulama bir görünüme kaydedilmişse, bunu paylaşmak için önerilen ve tercih edilen yol, uygun güvenlik rollerine sahip kullanıcılara görünümü yayımlamaktır. Ardından, yayımlanmış görünümle hedeflenen güvenlik rollerine sahip tüm kullanıcılar Finance and Operations uygulamalarında uygulamayı görebilir. Görünümün nasıl yayımlanacağı hakkında daha fazla bilgi için bkz. [Görünümleri yayımlama](saved-views.md#publishing-views).

    Ayrıca,katıştırılmış bir uygulamayı panodan tam sayfa deneyimi olarak da yayımlayabilirsiniz. Panoda, uygulamayla ilişkilendirilmiş kutucuğu seçin ve tutun (veya sağ tıklayın), **Kişiselleştir**'i seçin ve ardından **Sayfayı yayımla**'yı seçin. Şuanda yalnızca güvenlik rollerine yayımlayabilirsiniz. Ancak, tüzel kişiliklere yayımlama imkanı da özellik genel kullanıma sunulmadan önce eklenecektir.

- **Kişiselleştirmeyi kopyalayın:** Görünümleri desteklemeyen sayfalar (örneğin, iletişim kutuları veya çalışma alanları) veya tam sayfa uygulama deneyimi için, kişiselleştirmeyi uygun kullanıcılara kopyalayabilirsiniz. Daha fazla bilgi için bkz. [Kişiselleştirmeleri paylaşma](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Katıştırılmış uygulamaları görüntüleme

Katıştırılmış bir uygulamayı Finance and Operations uygulamalarındaki bir sayfada görüntülemek için, katıştırılmış uygulamanın bulunduğu sayfayı açın. Bazı sayfalarda katıştırılmış uygulamalara, standart Eylem Bölmesi'ndeki **Power Apps** düğmesi kullanılarak erişilebildiğini unutmayın. Alternatif olarak, bir sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak doğrudan görüntülenebilir.

## <a name="editing-or-removing-embedded-apps"></a>Katıştırılmış uygulamaları düzenleme veya kaldırma

Bir uygulama sayfaya katıştırıldığında, yapılandırmasını düzenlemeniz gerekebilir (örneğin, bölüm etiketini veya URL'yi değiştirmeniz gerekebilir). Alternatif olarak, uygulamayı sayfadan kaldırmanız da gerekebilir. Katıştırılmış bir uygulamanın yapılandırmasını düzenlemek veya uygulamayı tamamen kaldırmak için aşağıdaki prosedürlerden birini kullanın.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Varolan sayfalara katıştırılmış uygulamalar

1. Uygulamanın katıştırıldığı sayfayı açın.
2. **Kişiselleştirme** araç çubuğunu açmak için **Seçenekler**'i ve ardından **Kişiselleştir**'i seçin.
3. **Seçim** aracını seçin ve ardından katıştırılmış uygulamayı seçin.
4. Uygulamayı düzenlemek için yapılandırmada gerekli değişiklikleri yapın ve **Kaydet**'i seçin.

    Alternatif olarak, uygulamayı kaldırmak için **Sil**'i seçin.

5. Görünümü yeniden kaydedin veya tekrar yayımlayın. Sayfayı kaydetmeden sayfadan ayrılırsanız, **Web sitesini düzenle** bölmesinde gerçekleştirdiğiniz eylemlerden hiçbiri korunmayacaktır.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Panodan katıştırılmış uygulamalar

1. Panoyu açın.
2. Uygulamayla ilişkilendirilmiş kutucuğu seçin ve tutun (veya sağ tıklayın) ve ardından **Kişiselleştir**'i seçin.
3. Uygulamayı düzenlemek için **Sayfayı düzenle**'yi seçin. **Web sitesini düzenle** bölmesinde, uygulama yapılandırmasında gerekli değişiklikleri yapın ve **Kaydet**'i seçin.

    Alternatif olarak, uygulamayı kaldırmak için **Sayfayı kaldır**'ı seçin.

## <a name="appendix"></a>Ek

### <a name="troubleshooting"></a>Sorun Giderme

Web sitesi, Finance ve Operation uygulamasına katıştırıldığında doğru görüntülenmiyorsa veya URL bağlantısının reddedildiğini bildiren bir hata iletisi alırsanız, web sitesi büyük olasılıkla iFrame'e katıştırılmayı engelleyecek şekilde yapılandırılmıştır. Web sitesinin katıştırılabilir olup olmadığını belirlemek için aşağıdaki adımları izleyin.

1. Kullandığınız tarayıcı için geliştirici araçlarını açın.
2. **Ağ** sekmesinde, katıştırılmış siteden gelen yanıtı bulun ve seçin.
3. **Üstbilgiler** sekmesinde, **Yanıt Üstbilgileri**'nin altında, **x-kare-seçenekleri**'ni arayın. **x-kare seçenekleri** yanıt üstbilgilerinde yer alıyor ve **DENY** veya **SAMEORIGIN** değerine sahipse web sitesi katıştırılamaz. Güvenle katıştırmak için uygulamanın sahibiyle çalışmanız gerekir.

### <a name="developer-modeling-a-website-on-a-form"></a>[Geliştirici] Form üzerinde websitesi modelleme

Bu konu, kişiselleştirme yoluyla üçüncü taraf uygulama veya web sitelerini katıştırmaya odaklanıyor olsa da geliştiriciler Visual Studio geliştirme deneyimini kullanarak bunları bir forma katıştırabilir. Forma bir **WebsiteHostControl** denetimi eklemeniz yeterli olacaktır. Denetimdeki mevcut meta veri özellikleri, kişiselleştirme deneyimle aynı özelliklere sahiptir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
