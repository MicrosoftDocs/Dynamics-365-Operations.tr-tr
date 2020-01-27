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
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870253"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Apps'i katıştırma

[!include [banner](../includes/banner.md)]

Platform güncelleştirmesi 14,  hizmet geliştiricileri ve teknik olmayan kullanıcıların kod yazmadan mobil cihazlar, tabletler ve web için özel iş uygulamaları oluşturmasını sağlayan bir hizmet olan Microsoft Power Apps ile tümleştirmeyi destekler. Sizin tarafınızdan geliştirilen Power Apps, kuruluşunuz veya daha geniş bir ekosistem tarafından geliştirilmiş PowerApps ürün işlevselliğini artırmak amacıyla Finance and Operations uygulamalarına katıştırılabilir. Örneğin, başka bir sistemden alınan bilgileri Finance and Operations uygulamalarına eklemek için bir Power App oluşturabilirsiniz.

Katıştırılmış Power Apps hakkında daha fazla bilgi için [Power Apps'a  katıştırma](https://www.youtube.com/watch?v=x3qyA1bH-NY) kısa videosunu izleyin.

## <a name="adding-an-embedded-power-app-to-a-page"></a>Bir sayfaya katıştırılmış bir Power App ekleme

### <a name="overview"></a>Genel bakış

İstemciye bir Power App katıştırmadan önce istediğiniz görsellere ve/veya işleve sahip bir Power App bulmanız ya da oluşturmanız gerekir. Burada bir Power App oluşturma işlemini ayrıntılı şekilde açıklamayacağız. Power Apps'te yeniyseniz [Power Apps'a giriş](https://docs.microsoft.com/powerapps/getting-started) konusu iyi bir başlangıç noktası olabilir.

Belirli bir Power App'i eklemek için hazır duruma geldiğinizde, bir sayfada Power App'e ulaşmanın iki yolundan sizin senaryonuza en uygun olanını seçebilirsiniz. İlk yöntem standart Eylem Bölmesine eklenmiş olan Power Apps düğmesini kullanmaktır. Bu mekanizma kullanılarak eklenen Power Apps, Power Apps menü düğmesi içinde menü öğeleri olarak görünür. Seçildiğinde, bu menü öğelerinden her biri katıştırılmış Power App içeren bir yan bölme açar. Alternatif olarak, Power App'i doğrudan sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak göstermeyi tercih edebilirsiniz.

Katıştırılmış Power App'inizi yapılandırırken, Power App'e giriş olarak göndermek istediğiniz tek bir alan seçebilirsiniz. Bu, Power App'in gördüğünüz geçerli verileri temel alarak yanıt vermesini sağlar.

### <a name="details"></a>Ayrıntılı

Aşağıdaki yönergeler bir Power App'in web istemcisine nasıl katıştırılacağını gösterir.

1. Power App'i katıştırmak istediğiniz sayfaya gidin. Bu, Power App'e giriş olarak geçirilmesi gereken verileri içeren sayfanın aynısı olacaktır.
2. **Power App ekle** bölmesini açın:

    - **Seçenekler**'e tıklayın ve **Bu formu kişiselleştir**'i seçin. **Ekle** menüsünün altında **Power App**'i seçin. Son olarak, Power App'i eklemek istediğiniz bölgeyi seçin. Power App'i Power Apps menü düğmesinin altına katıştırmak istiyorsanız Eylem Bölmesi'ni seçin. Power App'i doğrudan sayfaya katıştırmak istiyorsanız uygun sekmeyi, hızlı sekmeyi, dikey pencereyi veya bölümü (bir çalışma alanındaysanız) seçin.
    - Power App'e Power Apps menü düğmesi kullanılarak erişilecekse bunun yerine standart Eylem Bölmesi'ndeki **Power Apps** menü düğmesine tıklayıp ardından **Power App Ekle**'yi seçebilirsiniz.

3. Katıştırılmış Power App'i yapılandırın:

    - **Ad** alanı, katıştırılmış Power App'i içerecek olan düğme veya sekme için gösterilecek metni belirtir. Çoğu kez, bu alanda Power App adını tekrarlamak isteyebilirsiniz.
    - **Uygulama kodu** katıştırmak istediğiniz Power App'in GUID değeridir. Bu değeri almak için [web.powerapps.com](https://web.powerapps.com) adresinde Power App'i bulun ve ardından **Ayrıntılar** altında **Uygulama kodu** alanını bulun.
    - **Power App için giriş verisi** için isteğe bağlı olarak Power App'e geçirmek istediğiniz verileri içeren alanı seçebilirsiniz. Power App'in Finance and Operations uygulamalarından gönderilen verilere nasıl erişebileceğine ilişkin ayrıntılar için bu konunun ilerleyen kısmındaki [Finance and Operations uygulamalarının verilerinden yararlanan bir Power App oluşturma](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) bölümüne bakın.
    - Katıştırdığınız Power App türüyle eşleşen **Uygulama boyutu**'nu seçin. Mobil cihazlar için oluşturulan Power Apps için **İnce**, tabletler için oluşturulan Power Apps için **Geniş** seçeneğini belirleyin. Bu, katıştırılmış Power App için yeterli miktarda alan ayrılmasını sağlar.
    - **Tüzel kişilikler** hızlı sekmesi, Power App'in hangi tüzel kişilikler tarafından kullanılabileceğini seçme olanağı tanır. Power App varsayılan olarak tüm tüzel kişiliklere gösterilir.

4. Yapılandırmanın doğru olduğunu onayladıktan sonra Power App'i sayfaya katıştırmak için **Ekle**'ye tıklayın. Katıştırılmış Power App'i görmek için tarayıcıyı yenilemeniz istenir.

## <a name="sharing-an-embedded-power-app"></a>Katıştırılmış bir Power App paylaşma

Bir sayfaya Power App'i katıştırdıktan sonra ve bunun sayfadan aktarılan her veri bağlamı ile düzgün çalıştığını onayladıktan sonra, bu katıştırılmış Power App'i sistemdeki diğer kullanıcılarla paylaşmak isteyebilirsiniz. Bunu üründeki kişiselleştirme özelliklerini kullanarak iki farklı yoldan yapabilirsiniz:

- Önerilen senaryo bu işlemi bir kişiselleştirmeyi tüm kullanıcılara veya bir kullanıcı alt kümesine sunabilecek olan sistem yöneticisi aracılığıyla gerçekleştirmektir.
- Alternatif olarak, sayfanızdaki kişiselleştirmeleri dışa aktarabilir, bir veya daha fazla kullanıcıya gönderebilir ve bu kullanıcıların değişiklikleri içe aktarmalarını isteyebilirsiniz. Kişiselleştirme araç çubuğundaki Yönet seçeneği kişiselleştirmeleri dışa ve içe aktarmanıza olanak tanır.

Üründeki kişiselleştirme özelliklerini ve onları nasıl kullanacağınıza dair daha fazla ayrıntı için bkz. [kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations uygulamalarının verilerinden yararlanan bir Power App oluşturma

Finance and Operations uygulamalarına katıştırılacak bir Power App oluşturmanın önemli bir bölümü Finance and Operations uygulamalarından alınan giriş verilerini kullanmaktır. Power App içinde, bu giriş verilerine Param("EntityId") değişkeni kullanılarak erişilebilir.

Örneğin, Power App'in OnStart işlevinde, Finance and Operations uygulamalarından alınan giriş verilerini bir değişkene şu şekilde ayarlayabilirsiniz:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Katıştırılmış bir Power App görüntüleme

Katıştırılmış bir Power App'i Finance and Operations uygulamalarındaki bir sayfada görüntülemek için katıştırılmış Power App'in bulunduğu sayfaya gitmeniz yeterlidir. Power Apps'a standart Eylem Bölmesindeki Power Apps düğmesi aracılığıyla erişilebileceğini veya sayfada doğrudan yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak görünebileceğini unutmayın. Bir kullanıcı bir sayfada Power App'i ilk yüklemeye çalıştığında, kullanıcının Power App'i kullanmak için gerekli izinlere sahip olmasını sağlamak üzere Power Apps'te oturum açması istenir.

## <a name="editing-an-embedded-power-app"></a>Katıştırılmış bir Power App'i düzenleme

Bir Power App sayfaya katıştırıldıktan sonra, bu Power App'in yapılandırmasında bazı değişiklikler yapmanız gerekebilir. Örneğin, katıştırılmış Power App ile ilişkilendirilen etikette değişiklik yapmak isteyebilirsiniz veya PowerApp'in yeni bir sürümü oluşturulduğunda en son Power App'i gösterecek şekilde Uygulama Kodunu güncelleştirmeniz gerekebilir.

Katıştırılmış bir Power App yapılandırmasını düzenlemek için aşağıdaki adımları izleyin:

1. **Power App düzenle** bölmesine gidin.

    - Katıştırılmış Power App'e Power Apps menü düğmesi aracılığıyla erişiliyorsa Power Apps menü düğmesine sağ tıklayın ve **Kişiselleştir**'i seçin. Yapılandırmak istediğiniz Power App'i **Power App Seç** açılır menüsünden seçin.
    - Katıştırılmış Power App doğrudan sayfa üzerinde görünüyorsa **Seçenekler**'i ve ardından **Bu formu kişiselleştir**'i seçin. **Seç** aracını kullanarak katıştırılmış Power App'e tıklayın.

2. Power Apps yapılandırmasında gerekli değişiklikleri yapın ve ardından **Kaydet**'e tıklayın.

## <a name="removing-an-embedded-power-app"></a>Katıştırılmış bir Power App'i kaldırma

Power App bir sayfaya katıştırıldıktan sonra gerekirse kaldırmak için iki yol vardır:

- Bu konunun önceki kısmında yer alan [Katıştırılmış bir Power App'i düzenleme](#editing-an-embedded-power-app) bölümündeki talimatları kullanarak **Power App Düzenle** bölmesine gidin. Bölmenin, kaldırmak istediğiniz katıştırılmış Power App ile ilgili bilgileri görüntülendiğini doğrulayın ve ardından **Sil** düğmesine tıklayın.
- Katıştırılmış bir Power App, kişiselleştirme verisi olarak kaydedildiğinden, sayfanın kişiselleştirmesini temizlemek bu sayfadaki katıştırılmış Power Apps'i de kaldırır. Sayfanın kişiselleştirmesini temizlemek kalıcı bir işlemdir ve geri alınamaz. Bir sayfadaki kişiselleştirmeleri kaldırmak için **Seçenekler**'i ve ardından **Bu form kişiselleştir**'i seçin. **Yönet** menüsü altından **Temizle** düğmesini seçin. Tarayıcınızı yenilendikten sonra, bu sayfadaki önceki tüm özelleştirmeler kaldırılır. Kişiselleştirme kullanarak sayfaları en iyi duruma getirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="appendix"></a>Ek

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Power App'in katıştırıldığı yer üzerindeki geliştirici denetimi

Varsayılan olarak kullanıcılar, Power Apps menü düğmesi altından veya doğrudan sayfaya bir sekme, hızlı sekme, dikey pencere veya çalışma alanına yeni bir bölüm olarak herhangi bir sayfaya Power Apps katıştırabilir. Ancak, gerekirse geliştiriciler aşağıdaki yöntemleri kullanarak bu özelliği yalnızca Power Apps'ın belirli sayfalara katıştırılmasına izin verecek şekilde yapılandırabilir:

- **isPowerAppPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, Power Apps menü düğmesi görüntülenmez ve kullanıcılar Power Apps'ı bu sayfadaki bir sekme dahil olmak üzere herhangi bir yere katıştıramaz.
- **isPowerAppTabPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, kullanıcılar Power Apps'ı doğrudan sayfa üzerine bir sekme, hızlı sekme veya panorama bölümü olarak ekleyemez. Sayfada katıştırmaya izin verilmiş olması durumunda, kullanıcılar Power Apps'ı Power Apps menü düğmesi aracılığıyla katıştırabilecektir.

Aşağıdaki örnek Power Apps'ın nereye katıştırılabileceğini yapılandırmak için gerekli olan iki yöntemi içeren yeni bir sınıfı göstermektedir.

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
