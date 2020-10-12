---
title: Power Apps uygulamasından tuval uygulamalarını ekleme
description: Bu konu ürün işlevselliğini artırmak için Microsoft Power Apps uygulamasından tuval uygulamalarının istemciye nasıl katıştırılacağını açıklar.
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
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
ms.openlocfilehash: e57e4567a80aa9f9ba5ac434b0d71204460e164f
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893119"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Apps uygulamasından tuval uygulamalarını ekleme

[!include [banner](../includes/banner.md)]

Microsoft Power Apps, geliştiricilerin ve teknik olmayan kullanıcıların mobil cihazlar, tabletler ve web için kod yazmak zorunda kalmadan özel iş uygulamaları oluşturmalarına olanak tanır. Finance and Operations uygulamaları Power Apps ile tümleştirmeyi destekler. Ürün işlevselliğini artırmak için, siz, kuruluşunuz veya daha geniş bir ekosistem tarafından geliştirilen tuval uygulamaları, Finance and Operations uygulamalarına katıştırılabilir. Örneğin, Power Apps'ten, başka bir sistemden alınan bilgilerle bir Finance and Operations uygulamasına destek olan bir tuval uygulaması oluşturabilirsiniz.

Katıştırılmış Power Apps hakkında daha fazla bilgi için [Power Apps'a katıştırma](https://www.youtube.com/watch?v=x3qyA1bH-NY) kısa videosunu izleyin.

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Power Apps'ten bir sayfaya katıştırılmış bir tuval uygulaması ekleme

### <a name="overview"></a>Genel bakış

İstemciye Power Apps'ten bir tuval uygulaması katıştırmadan önce, istediğiniz görsellere ve/veya işleve sahip bir uygulama bulmanız veya oluşturmanız gerekir. Bu konu, uygulama oluşturma işleminin ayrıntılı açıklamasını içermez. Power Apps uygulamasında yeni iseniz, [Power Apps belgelere](https://docs.microsoft.com/powerapps/) bakın.

Uygulamayı katıştırmaya hazır olduğunuzda, bir sayfadaki belirli bir tuval uygulamasına erişmek için iki yol vardır. Senaryonuza en çok uyan yaklaşımı seçebilirsiniz. İlk yaklaşım standart Eylem Bölmesi'ne eklenmiş olan **Power Apps** düğmesini kullanır. Bu yaklaşımı kullanarak eklediğiniz uygulamalar, **Power Apps** menü düğmesinde öğeler olarak görünür. Bu menü öğelerinden birini seçtiğinizde katıştırılmış uygulama içeren bir yan bölme görünür. Alternatif olarak, bir uygulamayı bir sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak doğrudan katıştırabilirsiniz.

Katıştırılmış tuval uygulamanızı yapılandırırken, uygulamaya bağlam olarak göndermek istediğiniz tek bir alan seçebilirsiniz. Bu adın uygulamanın görüntülemekte olduğunuz verilere dayanarak yanıt vermesini sağlar.

> [!NOTE]
> Modellenen uygulamaları katıştırmak için şu anda bu düzeneği kullanamazsınız.  

### <a name="details"></a>Ayrıntılı

Aşağıdaki yordam Power Apps'ten bir tuval uygulamasının Web istemcisine nasıl katıştırılacağını gösterir.

1. Tuval uygulamasını katıştırmak istediğiniz sayfaya gidin. Bu sayfa, uygulamaya giriş olarak geçirilmesi gereken verileri içeren sayfadır.
2. **Power Apps'ten bir uygulama ekle** bölmesini açın:

    - **Seçenekler**'e tıklayın ve **Bu sayfayı kişiselleştir**'i seçin. **Ekle** menüsünden **Power Apps**'i seçin. Son olarak, uygulamayı eklemek istediğiniz bölgeyi seçin. Uygulamayı Power Apps menü düğmesinin altına katıştırmak istiyorsanız Eylem Bölmesi'ni seçin. Uygulamayı sayfaya doğrudan katıştırmak istiyorsanız uygun sekmeyi, hızlı sekmeyi, dikey pencereyi veya bölümü (bir çalışma alanındaysanız) seçin.
    - Uygulamaya Power Apps menü düğmesiyle erişilecekse, alternatif olarak, standart Eylem Bölmesi'ndeki **Power Apps** menü düğmesine tıklayıp ardından **Uygulama ekle**'yi seçebilirsiniz.

3. Katıştırılmış uygulamayı yapılandırın:

    - **Ad** alanı, katıştırılmış uygulamayı içerecek olan düğme veya sekme için gösterilecek metni belirtir. Çoğu kez, bu alanda uygulamanın adını yinelemek isteyebilirsiniz.
    - **Uygulama kimliği** alanı, katıştırmak istediğiniz tuval uygulamasının genel benzersiz tanımlayıcısını (GUID) belirtir. Bu değeri almak için [web.powerapps.com](https://web.powerapps.com) adresinde uygulamayı bulun ve **Ayrıntılar** altından **Uygulama kodu** alanını bulun.
    - **Uygulama için giriş bilgisi** için, isteğe bağlı olarak uygulamaya geçirmek istediğiniz verileri içeren alanı seçebilirsiniz. Uygulamanın Finance and Operations uygulamalarından gönderilen verilere nasıl erişebileceğine ilişkin ayrıntılar için bu konunun ilerleyen kısmındaki [Finance and Operations uygulamalarının verilerinden yararlanan uygulamalar oluşturma](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) bölümüne bakın.
    - Katıştırdığınız uygulamanın türüyle eşleşen **Uygulama boyutu**'nu seçin. Mobil cihazlara yönelik oluşturulan uygulamalar için **İnce**'yi, tabletlere yönelik oluşturulan uygulamalar için **Geniş**'i seçin. Bu, katıştırılmış uygulama için yeterli alan ayrılmasını sağlar.
    - **Tüzel kişilikler** hızlı sekmesi, uygulamanın hangi tüzel kişilikler tarafından kullanılabileceğini seçme olanağı tanır. Varsayılan ayar, uygulamayı tüm tüzel kişiliklere erişebilir yapmaktır. Bu seçenek yalnızca [Kaydedilmiş görünümler](saved-views.md) özelliği devre dışı bırakılınca kullanılabilir. 

4. Yapılandırmanın doğru olduğunu onayladıktan sonra Power App'i sayfaya katıştırmak için **Ekle**'ye tıklayın. Katıştırılmış uygulamayı görmek için tarayıcıyı yenilemeniz istenir.

## <a name="sharing-an-embedded-app"></a>Katıştırılmış bir uygulamayı paylaşma

Bir sayfaya tuval uygulamasını katıştırdıktan sonra ve sayfadan aktarılan her veri bağlamı ile düzgün çalıştığını onayladıktan sonra sistemdeki diğer kullanıcılarla uygulamayı paylaşmak isteyebilirsiniz. Katıştırılmış bir tuval uygulamasını paylaştırmak için, aşağıdaki adımları izleyin.

1. Power Apps içinden uygulamaya erişebilmeleri için uygun kullanıcılarla [tuval uygulamasını paylaşın](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app). 

2. Bu kullanıcılar sayfayı görüntülerken, katıştırılmış uygulamanın görünmesini sağlamak amacıyla, hedeflenen kullanıcıların uygun kişiselleştirmelere sahip olduğundan emin olun. Aşağıdaki yaklaşımlardan herhangi birini kullanabilirsiniz:

    - Önerilen: Katıştırılmış uygulamayı içeren bir görünüm oluşturmak ve yayımlamak için [Kaydedilen görünümler](saved-views.md) özelliğini kullanın. Bu yaklaşım, yayımlanmış görünümle hedeflenen güvenlik rollerine sahip tüm kullanıcıların Finance and Operations uygulamalarındaki uygulamayı görebilmesini sağlar. 
    - Kaydedilmiş görünümler özelliği açık değilse, sistem yöneticisinin tüm kullanıcılara veya bir kullanıcı alt kümesine katıştırılmış uygulamayı içeren bir kişiselleştirmeyi göndermesini sağlayabilirsiniz. Alternatif olarak, sayfanızın kişiselleştirmelerini dışa aktarabilir ve bunları bir veya daha fazla kullanıcıya gönderebilirsiniz. Bu kullanıcıların her biri kişiselleştirmeleri içe aktarabilir. Kişiselleştirme araç çubuğunda, kişiselleştirmeleri dışa ve içe aktarmanıza olanak sağlayan eylemler vardır. 
    
> [!NOTE]
> Tuval uygulaması harici kullanıcılarla paylaşılıyorsa, bu kullanıcılar Finance and Operations uygulamaların içinde katıştırılmış uygulamayı kullanamaz. Ancak, bunlar doğrudan Power Apps içinden uygulamaya erişebilir. Harici kullanıcılar, Finance and Operations uygulamasının dağıtıldığı Microsoft 365 Azure Directory'ye ait olmayan konukları ve kullanıcıları içerir.

Üründeki kişiselleştirme özelliklerini ve onları nasıl kullanacağınıza dair daha fazla ayrıntı için bkz. [kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Finance and Operations uygulamalarından gönderilen verileri kullanan bir tuval uygulaması oluşturma

Bir Finance and Operations uygulamasına katıştırılacak bir tuval uygulaması oluşturduğunuzda, işlemin önemli bir bölümü Finance and Operations uygulamasındaki giriş verilerini kullanmaktır. Power Apps geliştirme deneyiminde, bir Finance and Operations uygulamasından geçirilen giriş verilerine **Param("EntityId")** değişkeni kullanarak erişilebilir.

Örneğin, uygulamanın OnStart işlevinde, Finance and Operations uygulamalarından alınan giriş verilerini bir değişkene şu şekilde ayarlayabilirsiniz:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Tuval uygulamasını görüntüleme

Katıştırılmış bir tuval uygulamasını Finance and Operations uygulamalarındaki bir sayfada görüntülemek için, katıştırılmış uygulamanın bulunduğu sayfaya gitmeniz yeterlidir. Uygulamalara, standart Eylem Bölmesi'ndeki **Power Apps** düğmesi kullanılarak erişilebildiğini unutmayın. Alternatif olarak, bir sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak doğrudan görüntülenebilirler. Kullanıcılar sayfaya ilk kez bir uygulama yüklemeye çalıştıklarında, oturum açmaları istenir. Bu adım, kullanıcıların uygulamayı kullanmak için uygun izinlere sahip olmasını gerektirir.

## <a name="editing-an-embedded-app"></a>Katıştırılmış bir uygulamayı düzenleme

Bir uygulama bir sayfaya katıştırıldıktan sonra, bu uygulamanın yapılandırmasında bazı değişiklikler yapmanız gerekebilir. Örneğin, katıştırılmış uygulama ile ilişkilendirilen etikette değişiklik yapmak isteyebilirsiniz veya uygulamanın yeni bir sürümü oluşturulduğunda Uygulama Kodunu en son uygulamayı gösterecek şekilde güncelleştirmeniz gerekebilir.

Katıştırılmış bir uygulama yapılandırmasını düzenlemek için şu adımları izleyin:

1. **Uygulamayı düzenle** bölmesine gidin.

    - Katıştırılmış uygulamaya Power Apps menü düğmesiyle erişiliyorsa Power Apps menü düğmesine sağ tıklayın ve **Kişiselleştir**'i seçin. Yapılandırmak istediğiniz uygulamayı **Uygulama seçin** açılır menüsünden seçin.
    - Katıştırılmış uygulama doğrudan sayfa üzerinde görünüyorsa **Seçenekler**'i ve ardından **Bu sayfayı kişiselleştir**'i seçin. **Seç** aracını kullanarak, katıştırılmış uygulamaya tıklayın.

2. Uygulama yapılandırmasında gerekli değişiklikleri yapın ve **Kaydet**'e tıklayın.

## <a name="removing-an-app"></a>Uygulamayı kaldırma

Uygulama bir sayfaya katıştırıldıktan sonra gerekirse kaldırmak için iki yol vardır:

- Bu konunun önceki kısmında yer alan [Katıştırılmış bir uygulamayı düzenleme](#editing-an-embedded-app) bölümündeki yönergeleri kullanarak **Uygulama düzenle** bölmesine gidin. Bölmenin kaldırmak istediğiniz katıştırılmış uygulama ile ilgili bilgileri görüntülendiğini doğrulayın ve ardından **Sil** düğmesine tıklayın.
- Katıştırılmış uygulama, kişiselleştirme verisi olarak kaydedildiğinden, sayfanın kişiselleştirmesini temizlemek bu sayfadaki tüm katıştırılmış uygulamaları da kaldırır. Sayfanın kişiselleştirmesini temizlemek kalıcı bir işlemdir ve geri alınamaz. Bir sayfadaki kişiselleştirmelerinizi kaldırmak için **Seçenekler**'i ve ardından **Bu sayfayı kişiselleştir**'i ve son olarak **Temizle** düğmesini seçin. Tarayıcınızı yenilendikten sonra, bu sayfadaki önceki tüm özelleştirmeler kaldırılır. Kişiselleştirme kullanarak sayfaları en iyi duruma getirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="appendix"></a>Ek

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Geliştirici tarafından] Uygulamanın katıştırıldığı yeri belirtme

Varsayılan olarak kullanıcılar, Power Apps menü düğmesi altından veya doğrudan sayfaya bir sekme, hızlı sekme, dikey pencere veya çalışma alanına yeni bir bölüm olarak herhangi bir sayfaya uygulamalar katıştırabilir. Ancak, gerekirse geliştiriciler aşağıdaki yöntemleri kullanarak bu özelliği yalnızca uygulamaların belirli sayfalara katıştırılmasına izin verecek şekilde yapılandırabilir:

- **isPowerAppPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, Power Apps menü düğmesi görüntülenmez ve kullanıcılar uygulamaları bu sayfadaki bir sekme dahil olmak üzere herhangi bir yere katıştıramaz.
- **isPowerAppTabPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, kullanıcılar uygulamaları doğrudan sayfa üzerine bir sekme, hızlı sekme veya panorama bölümü olarak ekleyemez. Sayfada katıştırmaya izin verilmiş olması durumunda, kullanıcılar uygulamaları Power Apps menü düğmesiyle katıştırabilecektir.

Aşağıdaki örnek uygulamaların nereye katıştırılabileceğini yapılandırmak için gerekli olan iki yöntemi içeren yeni bir sınıfı göstermektedir.

```powerapps
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
