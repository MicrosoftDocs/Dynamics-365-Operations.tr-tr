---
title: Üçüncü taraf uygulamaları katıştırma
description: Bu makalede, ürün işlevselliğini artırmak için üçüncü taraf uygulamaların istemciye nasıl ekleneceği açıklanmaktadır.
author: jasongre
ms.date: 09/13/2021
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
ms.openlocfilehash: 3c07befc7150ff0a121fd3aaa0b5233df9f431e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868622"
---
# <a name="embed-third-party-apps"></a>Üçüncü taraf uygulamaları katıştırma

[!include [banner](../includes/banner.md)]

Birçok müşteri, işlerini yürütmek için bir dizi uygulama kullanır. Bu uygulamalardan bazıları, Finans ve Operasyon uygulamalarıyla birlikte çalışan üçüncü taraf web uygulamalarıdır. Daha kusursuz bir kullanıcı deneyimi sağlamak için, bu üçüncü taraf uygulamaları doğrudan Finans ve Operasyon uygulamalarınıza eklemek için **Tam sayfa uygulamalar** özelliğini kullanabilirsiniz (üçüncü taraf uygulamaların eklemeye izin verdikleri varsayılır). Böylece, kullanıcılar sekmeler veya pencereler arasında geçiş yapmak zorunda kalmadan gereksinim duydukları web sitelerine ve uygulamalara erişebilirler.

Ürüne üçüncü taraf uygulamaları katıştırabilmeniz için Özellik yönetiminde **Tam sayfa uygulamalar** özelliğini açmanız gerekir. Ardından bir üçüncü taraf uygulamasını veya web sitesini katıştırmak için aşağıdaki yöntemlerden birini kullanabilirsiniz. Bu yöntemler, tuval uygulamalarını Microsoft Power Apps'ten Finans ve Operasyon uygulamalarına eklemek için kullanılan yöntemlere benzer.

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
7. Uygulamanın beklendiği gibi göründüğünü onaylayın. Uygulama görüntülenmiyorsa bu makalenin ilerleyen bölümlerinde yer alan [Sorun giderme](#troubleshooting) bölümüne bakın.
8. Görünüm seçiciyi açın ve **Kaydet**'i (uygulama, geçerli görünümle ilişkilendirilmeliyse) veya **Farklı kaydet**'i (uygulamayı farklı bir görünüme kaydetmek için) seçin.

    Sayfanın görünüm seçicisi yoksa (örneğin, sayfa bir iletişim kutusu veya çalışma alanı ise) bu adımı atlayabilirsiniz.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Web sitesini panodan tam sayfa deneyimi olarak katıştırma

Eklemek istediğiniz uygulama mevcut bir sayfayla ilişkili değilse veya Finans ve Operasyon uygulaması içinde uygulama için tam sayfa bir deneyim istiyorsanız bu yordamı kullanın.

1. Panoyu açın.
2. Panoyu seçin ve basılı tutun (veya sağ tıklayın), **Kişiselleştir** seçeneğini belirleyin ve ardından **Sayfa ekle**'yi seçin.
3. **Sayfa ekle** bölmesinde, **Web sitesi**'ni seçin.
4. Katıştırılmış uygulamayı yapılandırın:

    - **Ad** – Panoda katıştırılmış uygulama için eklenen kutucukta gösterilmesi gereken metni girin. Bu metnin genellikle uygulamanın adı olmasını istersiniz.
    - **URL** – Uygulamanın konumunu belirtin.

    > [!IMPORTANT]
    > - Güvenlik nedenleriyle, URL'de HTTPS kullanması gerekir.
    > - Uygulama veya web sitesinin katıştırmaya izin verecek şekilde yapılandırılması gerekir.

5. Uygulamayı panoya yeni bir kutucuk olarak eklemek için **Kaydet**'i seçin.
6. Panoda yeni kutucuğu seçin ve uygulamanın beklendiği gibi göründüğünü onaylayın. Uygulama görüntülenmiyorsa bu makalenin ilerleyen bölümlerinde yer alan [Sorun Giderme](#troubleshooting) bölümüne bakın.

## <a name="sharing-embedded-apps"></a>Katıştırılmış uygulamaları paylaşma

Önceki bölümlerde açıklanan yöntemlerden birini kullanarak bir uygulamayı katıştırdıktan sonra, görünümü sistemdeki diğer kullanıcılarla paylaşmak isteyebilirsiniz. Katıştırılmış bir uygulamayı paylaştırmak için, aşağıdaki yöntemlerden birini kullanın:

- **Görünümü yayımlayın (Önerilen):** Katıştırılmış uygulama bir görünüme kaydedilmişse bunu paylaşmak için önerilen ve tercih edilen yol, hedeflenen tüzel kişiliklerde uygun güvenlik rollerine sahip kullanıcılara görünümü yayımlamaktır. Bu durumda, yalnızca istenen kullanıcılar bu sayfadaki katıştırılmış uygulamayı görüntüler. Görünümün nasıl yayımlanacağı hakkında daha fazla bilgi için bkz. [Görünümleri yayımlama](saved-views.md#publishing-views).

    Ayrıca,katıştırılmış bir uygulamayı panodan tam sayfa deneyimi olarak da yayımlayabilirsiniz. Panoda, uygulamayla ilişkilendirilmiş kutucuğu seçin ve tutun (veya sağ tıklayın), **Kişiselleştir**'i seçin ve ardından **Sayfayı yayımla**'yı seçin. *Yayımlama görünümleri* deneyimine benzer bir deneyim gösterilir ve yayımlamak için güvenlik rollerini seçebilirsiniz. 10.0.21 veya sonraki güncelleştirmede, **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği açıksa uygulamayı istediğiniz tüzel kişiliklere de yayımlayabilirsiniz.

- **Kişiselleştirmeyi kopyalayın:** Görünümleri desteklemeyen sayfalar (örneğin, iletişim kutuları veya çalışma alanları) veya tam sayfa uygulama deneyimi için, kişiselleştirmeyi uygun kullanıcılara kopyalayabilirsiniz. Daha fazla bilgi için bkz. [Kişiselleştirmeleri paylaşma](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Katıştırılmış uygulamaları görüntüleme

Katıştırılmış bir uygulamayı Finans ve Operasyon uygulamalarındaki bir sayfada görüntülemek için, eklenmiş uygulamanın bulunduğu sayfayı açın. Bazı sayfalarda katıştırılmış uygulamalara, standart Eylem Bölmesi'ndeki **Power Apps** düğmesi kullanılarak erişilebildiğini unutmayın. Alternatif olarak, bir sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak doğrudan görüntülenebilir.

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

Bu makalede kişiselleştirme yoluyla üçüncü taraf uygulama veya web siteleri ekleme yöntemine odaklanılmaktadır ancak geliştiriciler, bunları bir forma eklemek için Visual Studio geliştirme deneyimini de kullanabilir. Forma bir **WebsiteHostControl** denetimi eklemeniz yeterli olacaktır. Denetimdeki mevcut meta veri özellikleri, kişiselleştirme deneyimle aynı özelliklere sahiptir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
