---
title: Power Apps'i katıştırma
description: Bu konu ürün işlevselliğini artırmak için Power Apps'ın istemciye nasıl katıştırılacağını açıklar.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017740"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Apps'i katıştırma

[!include [banner](../includes/banner.md)]

Finance and Operations, hizmet geliştiricileri ve teknik olmayan kullanıcıların kod yazmadan mobil cihazlar, tabletler ve web için özel iş uygulamaları oluşturmasını sağlayan bir hizmet olan Microsoft Power Apps ile tümleştirmeyi destekler. Ürün işlevselliğini artırmak için, siz, kuruluşunuz veya daha geniş bir ekosistem tarafından geliştirilen Power Apps, Finance and Operations uygulamalarına katıştırılabilir. Örneğin, Power Apps'ten, başka bir sistemden alınan bilgilerle bir Finance and Operations uygulamasına destek olan bir uygulama oluşturabilirsiniz.

Katıştırılmış Power Apps hakkında daha fazla bilgi için [Power Apps'a katıştırma](https://www.youtube.com/watch?v=x3qyA1bH-NY) kısa videosunu izleyin.

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Power Apps'ten bir sayfaya katıştırılmış bir uygulama ekleme

### <a name="overview"></a>Genel Bakış

İstemciye Power Apps'ten bir uygulama katıştırmadan önce, istediğiniz görsellere ve/veya işleve sahip bir uygulama bulmanız veya oluşturmanız gerekir. Burada uygulamalar oluşturma sürecini ayrıntılı şekilde açıklamayacağız. Power Apps'te yeniyseniz [Power Apps'a giriş](https://docs.microsoft.com/powerapps/getting-started) konusu iyi bir başlangıç noktası olabilir.

Belirli bir uygulamayı eklemek için hazır olduğunuzda, bir sayfada uygulamaya ulaşmanın iki yolundan sizin senaryonuza en uygun olanını seçebilirsiniz. İlk yöntem standart Eylem Bölmesine eklenmiş olan Power Apps düğmesini kullanmaktır. Bu mekanizma kullanılarak eklenen uygulamalar Power Apps menü düğmesi içinde menü öğeleri olarak görünür. Seçildiğinde, bu menü öğelerinden her biri katıştırılmış uygulama içeren bir yan bölme açar. Alternatif olarak, bir uygulamayı bir sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak doğrudan katıştırmayı tercih edebilirsiniz.

Katıştırılmış uygulamanızı yapılandırırken, uygulamaya bağlam olarak göndermek istediğiniz tek bir alan seçebilirsiniz. Bu, uygulamanın görüntülemekte olduğunuz verileri temel alarak yanıt vermesini sağlar.

### <a name="details"></a>Ayrıntılı

Aşağıdaki yönergeler Power Apps'ten bir uygulamanın web istemcisine nasıl katıştırılacağını gösterir.

1. Uygulamayı katıştırmak istediğiniz sayfaya gidin. Bu, uygulamaya bağlam olarak geçirilmesi gereken verileri içeren sayfanın aynısı olacaktır.
2. **Power Apps'ten bir uygulama ekle** bölmesini açın:

    - **Seçenekler**'e tıklayın ve **Bu sayfayı kişiselleştir**'i seçin. **Ekle** menüsünden **Power Apps**'i seçin. Son olarak, uygulamayı eklemek istediğiniz bölgeyi seçin. Uygulamayı Power Apps menü düğmesinin altına katıştırmak istiyorsanız Eylem Bölmesi'ni seçin. Uygulamayı sayfaya doğrudan katıştırmak istiyorsanız uygun sekmeyi, hızlı sekmeyi, dikey pencereyi veya bölümü (bir çalışma alanındaysanız) seçin.
    - Uygulamaya Power Apps menü düğmesiyle erişilecekse, alternatif olarak, standart Eylem Bölmesi'ndeki **Power Apps** menü düğmesine tıklayıp ardından **Uygulama ekle**'yi seçebilirsiniz.

3. Katıştırılmış uygulamayı yapılandırın:

    - **Ad** alanı, katıştırılmış uygulamayı içerecek olan düğme veya sekme için gösterilecek metni belirtir. Çoğu kez, bu alanda uygulamanın adını yinelemek isteyebilirsiniz.
    - **Uygulama kodu**, katıştırmak istediğiniz uygulamanın GUID değeridir. Bu değeri almak için [web.powerapps.com](https://web.powerapps.com) adresinde uygulamayı bulun ve **Ayrıntılar** altından **Uygulama kodu** alanını bulun.
    - **Uygulama için giriş bilgisi** için, isteğe bağlı olarak uygulamaya geçirmek istediğiniz verileri içeren alanı seçebilirsiniz. Uygulamanın Finance and Operations uygulamalarından gönderilen verilere nasıl erişebileceğine ilişkin ayrıntılar için bu konunun ilerleyen kısmındaki [Finance and Operations uygulamalarının verilerinden yararlanan uygulamalar oluşturma](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) bölümüne bakın.
    - Katıştırdığınız uygulamanın türüyle eşleşen **Uygulama boyutu**'nu seçin. Mobil cihazlara yönelik oluşturulan uygulamalar için **İnce**'yi, tabletlere yönelik oluşturulan uygulamalar için **Geniş**'i seçin. Bu, katıştırılmış uygulama için yeterli alan ayrılmasını sağlar.
    - **Tüzel kişilikler** hızlı sekmesi, uygulamanın hangi tüzel kişilikler tarafından kullanılabileceğini seçme olanağı tanır. Varsayılan ayar, uygulamayı tüm tüzel kişiliklere erişebilir yapmaktır. Bu seçenek yalnızca [Kaydedilmiş görünümler](saved-views.md) özelliği devre dışı bırakılınca kullanılabilir. 

4. Yapılandırmanın doğru olduğunu onayladıktan sonra Power App'i sayfaya katıştırmak için **Ekle**'ye tıklayın. Katıştırılmış uygulamayı görmek için tarayıcıyı yenilemeniz istenir.

## <a name="sharing-an-embedded-app"></a>Katıştırılmış bir uygulamayı paylaşma

Bir sayfaya uygulamayı katıştırdıktan sonra ve bunun sayfadan aktarılan her veri bağlamı ile düzgün çalıştığını onayladıktan sonra sistemdeki diğer kullanıcılarla paylaşmak isteyebilirsiniz. Bunu üründeki kişiselleştirme özelliklerini kullanarak iki farklı yoldan yapabilirsiniz:

- Önerilen senaryo bu işlemi bir kişiselleştirmeyi tüm kullanıcılara veya bir kullanıcı alt kümesine sunabilecek olan sistem yöneticisi aracılığıyla gerçekleştirmektir.
- Alternatif olarak, sayfanızdaki kişiselleştirmeleri dışa aktarabilir, bir veya daha fazla kullanıcıya gönderebilir ve bu kullanıcıların değişiklikleri içe aktarmalarını isteyebilirsiniz. Kişiselleştirme araç çubuğunda, kişiselleştirmeleri dışa ve içe aktarmanıza olanak sağlayan eylemler vardır.

Üründeki kişiselleştirme özelliklerini ve onları nasıl kullanacağınıza dair daha fazla ayrıntı için bkz. [kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations uygulamalarından gönderilen verileri kullanan bir uygulama oluşturma

Power Apps'ten bir Finance and Operations uygulamasında katıştırılacak bir uygulama oluşturmanın önemli bir bölümü, o uygulamadaki giriş verilerinden yararlanmaktır. Power Apps geliştirme deneyiminden, bir Finance and Operations uygulamasından geçirilen giriş verilerine Param("EntityId") değişkeni kullanarak erişilebilir.

Örneğin, uygulamanın OnStart işlevinde, Finance and Operations uygulamalarından alınan giriş verilerini bir değişkene şu şekilde ayarlayabilirsiniz:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Uygulamayı görüntüleme

Katıştırılmış bir uygulamayı Finance and Operations uygulamalarındaki bir sayfada görüntülemek için, katıştırılmış uygulamanın bulunduğu sayfaya gitmeniz yeterlidir. Uygulamalara standart Eylem Bölmesindeki Power Apps düğmesiyle erişilebileceğini veya sayfada doğrudan yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak görünebileceğini unutmayın. Bir kullanıcı bir sayfada bir uygulamayı ilk kez yüklemeye çalıştığında, kullanıcının uygulamayı kullanmak için gerekli izinlere sahip olmasını sağlamak üzere oturum açması istenir.

## <a name="editing-an-embedded-app"></a>Katıştırılmış bir uygulamayı düzenleme

Bir uygulama bir sayfaya katıştırıldıktan sonra, bu uygulamanın yapılandırmasında bazı değişiklikler yapmanız gerekebilir. Örneğin, katıştırılmış uygulama ile ilişkilendirilen etikette değişiklik yapmak isteyebilirsiniz veya uygulamanın yeni bir sürümü oluşturulduğunda Uygulama Kodunu en son uygulamayı gösterecek şekilde güncelleştirmeniz gerekebilir.

Katıştırılmış bir uygulama yapılandırmasını düzenlemek için şu adımları izleyin:

1. **Uygulamayı düzenle** bölmesine gidin.

    - Katıştırılmış uygulamaya Power Apps menü düğmesiyle erişiliyorsa Power Apps menü düğmesine sağ tıklayın ve **Kişiselleştir**'i seçin. Yapılandırmak istediğiniz uygulamayı **Uygulama seçin** açılır menüsünden seçin.
    - Katıştırılmış uygulama doğrudan sayfa üzerinde görünüyorsa **Seçenekler**'i ve ardından **Bu sayfayı kişiselleştir**'i seçin. **Seç** aracını kullanarak, katıştırılmış uygulamaya tıklayın.

2. Uygulama yapılandırmasında gerekli değişiklikleri yapın ve **Kaydet**'e tıklayın.

## <a name="removing-an-app"></a>Uygulamayı kaldırma

Uygulama bir sayfaya katıştırıldıktan sonra gerekirse kaldırmak için iki yol vardır:

- Bu konunun önceki kısmında yer alan [Katıştırılmış bir uygulamayı düzenleme](#editing-an-embedded-power-app) bölümündeki yönergeleri kullanarak **Uygulama düzenle** bölmesine gidin. Bölmenin kaldırmak istediğiniz katıştırılmış uygulama ile ilgili bilgileri görüntülendiğini doğrulayın ve ardından **Sil** düğmesine tıklayın.
- Katıştırılmış uygulama, kişiselleştirme verisi olarak kaydedildiğinden, sayfanın kişiselleştirmesini temizlemek bu sayfadaki tüm katıştırılmış uygulamaları da kaldırır. Sayfanın kişiselleştirmesini temizlemek kalıcı bir işlemdir ve geri alınamaz. Bir sayfadaki kişiselleştirmelerinizi kaldırmak için **Seçenekler**'i ve ardından **Bu sayfayı kişiselleştir**'i ve son olarak **Temizle** düğmesini seçin. Tarayıcınızı yenilendikten sonra, bu sayfadaki önceki tüm özelleştirmeler kaldırılır. Kişiselleştirme kullanarak sayfaları en iyi duruma getirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="appendix"></a>Ek

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Uygulamanın katıştırıldığı yer üzerindeki geliştirici denetimi

Varsayılan olarak kullanıcılar, Power Apps menü düğmesi altından veya doğrudan sayfaya bir sekme, hızlı sekme, dikey pencere veya çalışma alanına yeni bir bölüm olarak herhangi bir sayfaya uygulamalar katıştırabilir. Ancak, gerekirse geliştiriciler aşağıdaki yöntemleri kullanarak bu özelliği yalnızca uygulamaların belirli sayfalara katıştırılmasına izin verecek şekilde yapılandırabilir:

- **isPowerAppPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, Power Apps menü düğmesi görüntülenmez ve kullanıcılar uygulamaları bu sayfadaki bir sekme dahil olmak üzere herhangi bir yere katıştıramaz.
- **isPowerAppTabPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, kullanıcılar uygulamaları doğrudan sayfa üzerine bir sekme, hızlı sekme veya panorama bölümü olarak ekleyemez. Sayfada katıştırmaya izin verilmiş olması durumunda, kullanıcılar uygulamaları Power Apps menü düğmesiyle katıştırabilecektir.

Aşağıdaki örnek uygulamaların nereye katıştırılabileceğini yapılandırmak için gerekli olan iki yöntemi içeren yeni bir sınıfı göstermektedir.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
