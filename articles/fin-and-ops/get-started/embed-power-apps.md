---
title: "PowerApps katıştırma"
description: "Bu konu ürün işlevselliğini artırmak için PowerApps'ın Finance and Operations istemcisine nasıl katıştırılacağını açıklar."
author: jasongre
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 0fd0b1e5f94e39455b3c0799c89eea5a59444ad7
ms.contentlocale: tr-tr
ms.lasthandoff: 03/23/2018

---

# <a name="embed-powerapps"></a>PowerApps katıştırma

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

Platform güncelleştirmesi 14'te, Microsoft Dynamics 365 for Finance and Operations hizmet geliştiricileri ve teknik olmayan kullanıcıların kod yazmadan mobil cihazlar, tabletler ve web için özel iş uygulamaları oluşturmasını sağlayan bir hizmet olan Microsoft PowerApps ile tümleştirmeyi destekler. Size, kuruluşunuz veya daha geniş bir ekosistem tarafından geliştirilmiş PowerApps ürün işlevselliğini artırmak amacıyla Finance and Operations istemcisine katıştırılabilir. Örneğin, başka bir sistemden alınan bilgileri Finance and Operations'a eklemek için bir PowerApp oluşturabilirsiniz.  

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Bir sayfaya katıştırılmış bir PowerApp ekleme
### <a name="overview"></a>Özet
Finance and Operations istemcisine bir PowerApp katıştırmadan önce istediğiniz görsellere ve/veya işleve sahip bir PowerApp bulmanız veya oluşturmanız gerekir. Burada bir PowerApp oluşturma işlemini ayrıntılı şekilde açıklamayacağız. PowerApps'te yeniyseniz [PowerApps'a giriş](https://docs.microsoft.com/en-us/powerapps/getting-started) konusu iyi bir başlangıç noktası olabilir.

Belirli bir PowerApp'ı eklemek için hazır duruma geldiğinizde, bir sayfada PowerApp'a ulaşmanın iki yolundan sizin senaryonuza en uygun olan bir tanesini seçebilirsiniz. İlk yöntem standart Eylem Bölmesine eklenmiş olan PowerApps düğmesini kullanmaktır. Bu mekanizma kullanılarak eklenen PowerApps PowerApps menü düğmesi içinde menü öğeleri olarak görünür. Seçildiğinde, bu menü öğelerinden her biri katıştırılmış PowerApp içeren bir yan bölme açar. Alternatif olarak, PowerApp'ı doğrudan sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak göstermeyi tercih edebilirsiniz. 

Finance and Operations'da katıştırılmış PowerApp'ınızı yapılandırırken, PowerApp'a giriş olarak göndermek istediğiniz tek bir alan seçebilirsiniz. Bu, PowerApp'ın Finance and Operations'da gördüğünüz geçerli verileri temel alarak yanıt vermesini sağlar.  

### <a name="details"></a>Ayrıntılı
Aşağıdaki yönergeler bir PowerApp'ın Finance and Operations web istemcisine nasıl katıştırılacağını gösterir.  

1. PowerApp'ı katıştırmak istediğiniz sayfaya gidin. Bu, PowerApp'a giriş olarak geçirilmesi gereken verileri içeren sayfanın aynısı olacaktır.  
2. **PowerApp ekle** bölmesini açın:
   - **Seçenekler**'e tıklayın ve **Bu formu kişiselleştir**'i seçin. **Ekle** menüsünden **PowerApp**'ı seçin. Son olarak, PowerApp'ı eklemek istediğiniz bölgeyi seçin. PowerApp'ı PowerApps menü düğmesinin altına katıştırmak istiyorsanız, Eylem Bölmesi'ni seçin. PowerApp'ı doğrudan sayfaya katıştırmak istiyorsanız uygun sekmeyi, hızlı sekmeyi, dikey pencereyi veya bölümü (bir çalışma alanındaysanız) seçin.   
   - PowerApp'a PowerApps menü düğmesi kullanılarak erişilecekse, bunun yerine standart Eylem Bölmesindeki **PowerApps** menü düğmesine tıklayıp **PowerApp Ekle**'yi seçebilirsiniz.  
3. Katıştırılmış PowerApp'ı yapılandırın:
   - **Ad** alanı, katıştırılmış PowerApp'ı içerecek olan düğme veya sekme için gösterilecek metni belirtir. Çoğu kez, bu alanda PowerApp adını tekrarlamak isteyebilirsiniz.  
   - **Uygulama kodu** katıştırmak istediğiniz PowerApp'ın GUID değeridir. Bu değeri almak için [web.powerapps.com](https://web.powerapps.com) adresinde PowerApp'ı bulun ve **Ayrıntılar** altından **Uygulama kodu** alanını bulun.  
   - **PowerApp için giriş verisi** için, isteğe bağlı olarak giriş olarak PowerApp'a geçirmek için istediğiniz verileri içeren alanı seçebilirsiniz. PowerApp'ın Finance and Operations'dan gönderilen verilere nasıl erişebileceğine ilişkin ayrıntılar için bu konunun ilerleyen kısmındaki [Finance and Operations verilerinden yararlanan bir PowerApp oluşturma](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) bölümüne bakın.  
   - Katıştırdığınız PowerApp türüyle eşleşen **Uygulama boyutunu** seçin. Mobil cihazlar için oluşturulan PowerApps için **İnce**, tabletler için oluşturulan PowerApps için **Geniş** seçeneğini belirleyin. Bu katıştırılmış PowerApp için yeterli miktarda alan ayrılmasını sağlar.
   - **Tüzel kişilikler** hızlı sekmesi, PowerApp'ın hangi tüzel kişilikler tarafından kullanılabileceğini seçme olanağı tanır. PowerApp varsayılan olarak tüm tüzel kişiliklere gösterilir.  
4. Yapılandırmanın doğru olduğunu onayladıktan sonra PowerApp'ı sayfaya katıştırmak için **Ekle**'ye tıklayın. Katıştırılmış PowerApp'ı görmek için tarayıcıyı yenilemeniz istenir. 

## <a name="sharing-an-embedded-powerapp"></a>Katıştırılmış bir PowerApp paylaşma
Bir sayfaya PowerApp'ı katıştırdıktan sonra ve bunun sayfadan aktarılan her veri bağlamı ile düzgün çalıştığını onayladıktan sonra, bu katıştırılmış PowerApp'ı sistemdeki diğer kullanıcılarla paylaşmak isteyebilirsiniz. Bunu üründeki kişiselleştirme özelliklerini kullanarak iki farklı yoldan yapabilirsiniz:

- Önerilen senaryo bu işlemi bir kişiselleştirmeyi tüm kullanıcılara veya bir kullanıcı alt kümesine sunabilecek olan sistem yöneticisi aracılığıyla gerçekleştirmektir. 

- Alternatif olarak, sayfanızdaki kişiselleştirmeleri dışa aktarabilir, bir veya daha fazla kullanıcıya gönderebilir ve bu kullanıcıların değişiklikleri içe aktarmalarını isteyebilirsiniz. Kişiselleştirme araç çubuğundaki Yönet seçeneği kişiselleştirmeleri dışa ve içe aktarmanıza olanak tanır.

Üründeki kişiselleştirme özelliklerini ve onları nasıl kullanacağınıza dair daha fazla ayrıntı için bkz. [kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Finance and Operations verilerinden yararlanan bir PowerApp oluşturma
Finance and Operations'a katıştırılacak bir PowerApp oluşturmanın önemli bir bölümü Finance and Operations'dan alınan giriş verilerini kullanmaktır. PowerApp içinde, bu giriş verilerine Param("EntityId") değişkeni kullanılarak erişilebilir.  

Örneğin, PowerApp'ın OnStart işlevinde, Finance and Operations'dan alınan giriş verilerini bir değişkene şu şekilde ayarlayabilirsiniz:

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>Katıştırılmış bir PowerApp görüntüleme
Katıştırılmış bir PowerApp'ı Finance and Operations'daki bir sayfada görüntülemek için katıştırılmış PowerApp'ın bulunduğu sayfaya gitmeniz yeterlidir. PowerApps'a standart Eylem Bölmesindeki PowerApps düğmesi aracılığıyla erişilebileceğini veya sayfada doğrudan yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak görünebileceğini unutmayın. Bir kullanıcı bir sayfada PowerApp'ı ilk yüklemeye çalıştığında, kullanıcının PowerApp'ı kullanmak için gerekli izinlere sahip olmasını sağlamak için PowerApps'te oturum açması istenir.   

## <a name="editing-an-embedded-powerapp"></a>Katıştırılmış bir PowerApp'ı düzenleme
Bir PowerApp sayfaya katıştırıldıktan sonra, bu PowerApp'ın yapılandırmasında için bazı değişiklikler yapmanız gerekebilir. Örneğin, katıştırılmış PowerApp ile ilişkilendirilen etikette değişiklik yapmak isteyebilirsiniz veya PowerApp'ın yeni bir sürümü oluşturulduğunda en son PowerApp'ı gösterecek şekilde Uygulama Kodunu güncelleştirmeniz gerekebilir. 

Katıştırılmış bir PowerApp yapılandırmasını düzenlemek için şu adımları izleyin:
1. **PowerApp düzenle** bölmesine gidin. 
   - Katıştırılmış PowerApp'a PowerApps menü düğmesi aracılığıyla erişiliyorsa, PowerApps menü düğmesine sağ tıklayın ve **Kişiselleştir**'i seçin. Yapılandırmak istediğiniz PowerApp'ı **PowerApp Seç** açılır menüsünden seçin.  
   - Katıştırılmış PowerApp doğrudan sayfa üzerinde görünüyorsa, **Seçenekler**'i ve ardından **Bu formu kişiselleştir**'i seçin. **Seç** aracını kullanarak, katıştırılmış PowerApp'a tıklayın.  
2. PowerApps yapılandırmasında gerekli değişiklikleri yapın ve ardından **Kaydet**'e tıklayın.  

## <a name="removing-an-embedded-powerapp"></a>Katıştırılmış bir PowerApp'ı kaldırma
PowerApp bir sayfaya katıştırıldıktan sonra gerekirse kaldırmak için iki yol vardır: 

- Bu konunun önceki kısmında yer alan [Katıştırılmış bir PowerApp'ı düzenleme](#editing-an-embedded-powerapp) bölümündeki talimatları kullanarak **PowerApp Düzenle** bölmesine gidin. Bölmenin kaldırmak istediğiniz katıştırılmış PowerApp ile ilgili bilgileri görüntülendiğini doğrulayın ve ardından **Sil** düğmesine tıklayın. 

- Katıştırılmış bir PowerApp kişiselleştirme verisi olarak kaydedildiğinden, sayfanın kişiselleştirmesini temizlemek bu sayfadaki katıştırılmış PowerApps'ı da kaldırır. Sayfanın kişiselleştirmesini temizlemek kalıcı bir işlemdir ve geri alınamaz. Bir sayfadaki kişiselleştirmeleri kaldırmak için **Seçenekler**'i ve ardından **Bu form kişiselleştir**'i seçin. **Yönet** menüsü altından **Temizle** düğmesini seçin. Tarayıcınızı yenilendikten sonra, bu sayfadaki önceki tüm özelleştirmeler kaldırılır. Kişiselleştirme kullanarak sayfaları en iyi duruma getirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).  

## <a name="appendix"></a>Ek 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>PowerApp'ın katıştırıldığı yer üzerindeki geliştirici denetimi
Varsayılan olarak kullanıcılar, PowerApps menü düğmesi altından veya doğrudan sayfaya bir sekme, hızlı sekme, dikey pencere veya çalışma alanına yeni bir bölüm olarak herhangi bir sayfaya PowerApps katıştırabilir. Ancak, gerekirse geliştiriciler aşağıdaki yöntemleri kullanarak bu özelliği yalnızca PowerApps'ın belirli sayfalara katıştırılmasına izin verecek şekilde yapılandırabilir: 

- **isPowerAppPersonalizationEnabled** - Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, PowerApps menü düğmesi görüntülenmez ve kullanıcılar PowerApps'ı bu sayfadaki bir sekme dahil olmak üzere herhangi bir yere katıştıramaz.. 

- **isPowerAppTabPersonalizationEnabled** - Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, kullanıcılar PowerApps'ı doğrudan sayfa üzerine bir sekme, hızlı sekme veya panorama bölümü olarak ekleyemez. Sayfada katıştırmaya izin verilmiş olması durumunda, kullanıcılar PowerApps'ı PowerApps menü düğmesi aracılığıyla katıştırabilecektir.  

Aşağıdaki örnek PowerApps'ın nereye katıştırılabileceğini yapılandırmak için gerekli olan iki yöntemi içeren yeni bir sınıfı göstermektedir.  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


