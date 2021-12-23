---
title: Kılavuz çerçevesini işleme
description: Bu konu, X++ ile ambar mobil işlemlerimizi yöneten geliştiriciler için işlem kılavuzu çerçevesi hakkında bilgi sağlar.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902058"
---
# <a name="process-guide-framework"></a>Kılavuz çerçevesini işleme

[!include [banner](../includes/banner.md)]

Bu konu, X++ ile ambar mobil işlemlerini yöneten geliştiriciler için işlem kılavuzu çerçevesi hakkında bilgi sağlar. Ambar mobil işlemler, küçük adımlara bölünmekte olan işlemlerin sonucu olarak genişletilebilir. Her adımın iş mantığı ve kullanıcı arabirimi oluşturmasına yönelik adımlar, genişletilebilirlik sağlayan bağımsız sınıflara ayıklandı.

## <a name="overview-of-the-existing-design"></a>Varolan tasarıma genel bakış

Ambar mobil yürütme akışları, tek bir özel hizmet bitiş noktası aracılığıyla kullanıma sunulmuştur. İstek, mobil uygulamada sunulan kullanıcı arabiriminin meta verilerini ve kullanıcının girdiği değerleri içeren bir XML dizesi formunda, mobil uygulamadan ulaşır.

İstek alındığında, ilk adım bu XML'i seri durumdan çıkarmaktır. **WHSMobileAppServiceXMLTranslator** sınıfı, XML'yi hem denetim bilgilerini hem de oturum bilgilerini içeren bir kapsayıcıya dönüştürür.

Bundan sonra, kapsayıcıdaki bilgiler kullanıcının hangi ambar işlemini üzerinde çalıştığını veya başlatmak (**WHSWorkExecuteMode** sıralaması tarafından temsil edilir) ve buna uygun şekilde, **WHSWorkExecuteDisplay** sınıfının türetilmiş bir sınıfını oluşturmak için kullanılır. **displayform()** yöntemi çağrılır ve bu aşağıdakileri yapar:

-   Kullanıcıdan verileri işler (**WHSRFControlData** sınıfına temsilci atanmıştır, ancak bazı işlemler **processControl()** yöntemini geçersiz kılarak belirli mantık uygular).

-   İş mantığını yürütür.

-   Adımı artırır.

-   Yeni kullanıcı arabirimini temsil eden kapsayıcıyı oluşturur (normal olarak **oluştur...()** yönteminde).

Konteyner daha sonra XML'yi yeniden dizerek çeviriciyi geri döndürülür ve bunu mobil cihaza bir yanıt olarak gönderir.

Aşağıdaki sıra diyagramında, yürütme akışının genel bakışı verilmektedir. Diyagramın şematik genel bakışdan daha fazla olduğuna ve gerçek kodun 1:1 temsili olmadığını unutmayın.

![İşlemin şematik genel bakışı.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Yeniden tasarımın nedeni

Yukarıdaki tasarım, mobil akışlarda kullanılan işlemleri oluşturmak için çok basit bir çerçeve sunar. Ancak yukarıda da görüldüğü üzere, **displayform()** yöntemleri birden çok sorumluluğu üstlenir. Bunları diğer yöntemlere ve sınıflara devredebilir ancak somut sınıf sorumlulukları yokluğunda, sınıflar arasında tutarsız bir şekilde yapılır. Ayrıca, desteklenen senaryoların sayısı organik şekilde büyürken, bu sınıflardan bazıları karmaşık hale gelebilir. Konuları daha da ilginçleştirecek şekilde, bu sınıfların/yöntemlerin bazıları geçersiz kılınır ve çoklu modlarda yeniden kullanılır. Sonuç yüksek siklomatik karmaşıklık bakımından son derece uzun yöntemlerdir. Bunlar, geçmişte bakım sorunlarına neden olmuştur. Bu yöntemlerde hataları düzeltmek riskli ve gerileme eğilimlidir.
Örneğin, **WhsWorkExecuteDisplay** sınıfındaki **processWorkLine()** yöntemine birden çok işlem referans verir (temel olarak, iş yürütmenin gerçekleştirildiği yerler).

Bunları genişletilebilir yapmak için seçeneklerden biri **displayForm** yöntemlerini daha küçük yöntemlere bölmek ve genişletilebilirlik noktaları tanıtmak olacaktır. Ancak, senaryo matrisi nedeniyle, ortakların uzantıları yazması ve gerilemeleri karşı doğrulaması zor olacaktır. Yalnızca yukarıda belirtilen yapısal sorumluluk dağılımının eksikliğinden dolayı değil, aynı zamanda kod, kalite uzantıları oluşturma ile ilgili güçlükleri zaman içinde öngörülemeyen yollarla büyürdü.

Sonuç olarak, yeniden tasarım, bağımsız sorumlulukları olan açıkça tanımlanmış sınıflara sahip bir hedef içeren sürdürülebilir bir seçenektir. Bir sınıfın bir sorumluluğu, bir değişiklik nedeni ve bir genişletme nedeni olmalıdır.

## <a name="design-overview"></a>Tasarıma genel bakış

Yeniden tasarlanan çerçevede, temel strateji iki ilke etrafında döner: yürütme akışını iyi tanımlanmış sorumluluklara sahip ayrı bileşenlere böler ve her bir bileşenden iyi tanımlanmış genişletme noktalarına sahiptirler.

Yeni çerçevenin adı "ProcessGuide"dır. Bunun nedeni, bu sınıfların amacının bir kullanıcıyı bir iş işleminde rehberlik etmektir (kullanıcının, verilerle veya görevleri gerçekleştirme sırasında daha fazla esnekliğe sahip olduğu form tabanlı zengin istemciye kıyasla).

> [!NOTE]
> Göze çarpan bir ayrıntı, "WHS" ön ekinin kasıtlı olarak dahil edilmemesidir. Mobil işlemler başlangıçta depolama için kullanılsa da, daha sonra çeşitli üretim ve stok yönetimi işlemlerini desteklemek için sınırları aştılar. Sonuç olarak, ambar referansı çerçeve adında dışlandı.

Bileşenleri tanımlamak için ilk adım Üretim Başlatma işlemine bakmaktır (**WhsWorkExecuteDisplayProdStart** sınıfı). Sürecim şematiği aşağıdaki gibidir.

![Şematik işlem görüntüsü.](media/production-start-process-schematic.png)

Denetim akışına bakıldığında, aşağıdakiler gerekli bileşenlerdir:

-   Tüm iş sürecini birleştiren bir denetleyici.
-   İşlemdeki bir adımın yürütülmesinden sorumlu adım.
-   Bir adımdaki verileri işlemek için veri işlemcisi.
-   Bir adım için kullanıcı arabirimi oluşturmaktan sorumlu sayfa oluşturucu.
-   Adım geçişinden sorumlu bir gezinti aracısı.
-   İş sürecini yürütmekten sorumlu sınıf.

Yukarıdaki işlem akışı diyagramında, adım 1'de başlar ve önceki adımdan verileri işlemeye başlar ve sonra bir UI oluşturarak sonlandırırsanız, veriler bir sonraki adımda işlenmeye devam eder. Bu, birbirini izleyen adımlar arasında sıkı bir bağlantı oluşturur; sonuç olarak, yeni yüksek düzey şematik aşağıdaki gibi görünür:

![Üst düzey şematik işlemin resmi.](media/high-level-schematic.png)

Yeniden tasarlanan işlemdeki anahtar bileşenler şunlardır:

-   **ProcessGuideController** - Bu sınıf, iş sürecinin genel yürütmesini düzenler. Hem işlem yürütmesini oluşturan, hem de iptal için temizleme mantığının yanı sıra işlemden çıkılırken, adım ve gezinti aracısının örneğini oluşturan fabrikaları tanımlar.

-   **ProcessGuideStep** - Bu sınıf, iş sürecindeki bir tek adımı temsil eder. Bu sınıf, sayfa oluşturucu, eylemler ve veri işlemcileri sunan fabrikalar tanımını içerir ve bunları doğru sırada çağırmaktan sorumludur.

-   **ProcessGuideNavigationAgent** - Bu sınıf, adımlar arasındaki gezinmeden sorumludur. Bir adım tamamlandığında, sonraki adımı tanımlamaktan ve önceki adımın bir sonrakine iletişim kurması gerekebileceği parametreleri geçirmekten gezinti aracısı sorumludur.

-   **ProcessGuidePageBuilder** - Bu sınıf, kullanıcı arabiriminin örneğini oluşturmaktan sorumludur.

-   **ProcessGuideAction** - Bu sınıf, kullanıcıya düğme olarak gösterilen bir eylemi temsil eder.

-   **ProcessGuideDataProcessor** - Bu sınıf, kullanıcının alana girdiği verileri işlemekten sorumludur.

## <a name="execution-flow"></a>Yürütme akışı

Yürütme akışının başlangıç noktası değişmeden kalır. Bu nedenle, istek yine aynı son noktalar üzerinden ulaşır ve ardından XML'den kapsayıcıya seri numarasını kaldırma işlemi gerçekleşir. Bu konteyner daha sonra **getNextFormState()** öğesine geçirilir.

Dikkat edilecek üç önemli sınıf vardır:

-  **ProcessGuideSessionState** – Bu, yürütülmekte olan oturum durumu bilgilerini; modunu, geçişi, denetleyiciyi ve yürütülen adımı vb. içerir.

-  **ProcessGuidePage** – Bu, kullanıcı arabirimi meta verilerinin kesin türü belirlenmiş bir gösterimini içerir.

-  **ProcessGuideRequest** – Bu, yukarıdaki iki öğeyi üye olarak içerir ve mobil aygıttan alınan isteğin kesin türü bir gösterimidir.

Bu sınıflar, konteyner bilgileri (hem durum, hem de kullanıcı tarafından girilen denetim verileri) kullanılarak oluşturulur. Bu, değerlere erişmek ve değiştirmek için tür güvenli bir yol sağlar. İşlem sırasında kapsayıcının yinelenen erişimine kıyasla, hem okunabilirlik hem de performans açısından yarar sağlanır.

Oturum durumu bilgileri doğru **ProcessGuideController** sınıfının örneğini oluşturmak için kullanılır. Bir kez ayarlandıktan sonra, **ProcessGuideController** sınıfındaki **createResponse()** yöntemi çağrılır. Bu yöntem, işlem kılavuzu mantığına giriş noktasıdır ve yürütmeden sonra yanıtla birlikte gelir (**ProcessGuideResponse** sınıfında gösterilen). Yanıt daha sonra kapsayıcıya geri dönüştürülür ve daha sonra XML'ye dizileştirir ve yanıtı mobil aygıta geri gönderir.

Daha sonra, denetleyicinin yürütülmesi için sonraki adımı bulması gerekir. Yeni bir işlemin başlangıcıysa, denetleyici işlemdeki ilk adımı almak için **initialStep()** öğesini çağırır. Bundan sonra, **ProcessGuideStep** içindeki **yürüt()** yöntemini çağırır. Bu yöntem daha sonra bir **ProcessGuidePageBuilder** sınıfı örneği oluşturur ve kullanıcıya sunulacak kullanıcı arabiriminin sanal temsili olan bir **ProcessGuidePage** nesnesiyle geri dönecek **buildPage()** öğesini çağırır. Bu adım, sonucu yeniden denetleyiciye gönderir ve o durumda geçerli oturum durumunu kaydeder ve sonucu **ProcessGuideResponse** sınıfı biçiminde **getNextFormState()** öğesine geri döndürür. Bundan sonra, yanıt kapsayıcıya geri dönüştürülür ve sonra XML'ye yeniden dizileştirir ve böylece mobil aygıta yanıtı geri gönderir.

Aşağıdaki sıralı diyagram, bu denetim akışını açıklar. Bunun, tasarımın açıklaması için basitleştirilmiştir en yaygın denetim akışı olduğuna dikkat edin.

![Denetim akışı basitleştirildi.](media/control-flow.png)

Kullanıcı, bir düğmeyi (veya genellikle varsayılan eylemi tetikleyen) tıklatarak mobil cihazda bir eylem yaptığında istek **ProcessGuideController** sınıfındaki **createResponse()** yöntemine aynı rota üzerinden ulaşır. Ancak bu sefer, denetleyici, kullanıcının hangi adımı içinde olduğunu belirten oturum durumu bilgisini bilir. Buna göre, uygun **ProcessGuideStep** sınıfını başlatır ve yürütme yöntemini çağırır. **ProcessGuideStep**, kullanıcı tarafından çağrılan eylem adını okur ve uygun **ProcessGuideAction** sınıfını başlatır ve **yürütme()** öğesini çağırır.

**ProcessGuideAction** sınıfı, belirli bir eylemi yürütmekten sorumludur, ancak iki dikkate değer özel durumu vardır.

Birincisi, **ProcessGuideOKAction** sınıfıdır. Bu eylem, kullanıcının işlemde onaylamak ve ileri gitmek istediğini gösterir. Bu yönteme göre, bu yöntem aslında ProcessGuideStep sınıfına geri çağrı yapar ve bu adım **ProcessGuideDataProcessor** içinde **processData()** öğesini çağırır anlamına gelir. Bu, kullanıcının girdiği verileri işler ve sonra da adımın durumunu güncelleştirir ve sonucu denetleyiciye geri gönderir. İşlemcinin sonucuna bağlı olarak, adım, uygun kullanıcı arabirimini oluşturmak için sayfa oluşturucuyu çağırır veya adımın durumunu tamamlandı olarak ayarlar. Bu, aşağıdaki sıralı diyagramının üst yarısında yansıtılır.

Diğer özel durum, **ProcessGuideCancelResetProcessAction** ve **ProcessGuideCancelExitProcessAction** sınıflarında uygulanan iptal eylemleridir. Bu eylemler, işlemi iptal etme ve işlemin başlangıcına geri dönme veya işlemden tamamen çıkma amacını gösterir. Bu eylemler, **Tamam** eylemine benzer şekilde, bir adımda geri çağrı yapar ve bu da **ProcessGuideController**'a niyeti bildirir. Denetleyici daha sonra, durum değişkenlerinin gerekli temizlemesini yapar ve denetimi işlemdeki ilk adıma taşır veya işlemi tamamen sonlandırır.

Adım tamamlandıktan sonra, adımın durumu **Tamamlandı** olarak ayarlandıysa, denetleyici, bir sonraki adımın adını döndüren bir **ProcessGuideNavigationAgent** öğesini başlatır. Denetleyici bu adımı başlatır ve **yürütme()** yöntemini çağırır, döngü devam eder. En yaygın olarak, yeni adım kullanıcıya sunulacak bir sonraki ekran için kullanıcı arabirimi oluşturmak üzere ilgili **ProcessGuidePageBuilder** öğesini çağırır ve sonra geri gönderilir. Bu akış, aşağıdaki sıralı diyagramının alt yarısında yansıtılır.

![sıralı diyagram.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>ProcessGuide çerçevesi kullanarak yeni işlem oluşturma

Denetim akışını açıklamanın en iyi yolu, uygulamada var olan bir örnek (Üretim Başlangıcı işlemi) kullanmaktır.

## <a name="overview-of-the-production-start-process"></a>Üretim başlangıç işlemine genel bakış

Süreç akışını anlayarak başlayalım. İlk adımda, kullanıcıdan üretim emri kodu istenir.

![Üretim kodu isteği.](media/production-id-prompt.png)

Kullanıcı üretim emri kodunu girdiğinde, sipariş numarası doğrulanır. Çalışan doğrulamalardan bazıları, siparişin kullanıcının oturum açmış olduğu ambar konumunda olup olmadığına ve siparişin durumuna bağlıdır. Doğrulama başarısız olursa, kullanıcıya bir hata iletisi gösterilir. Doğrulama başarılı olursa, kullanıcıya üretim emri ve maddenin ayrıntıları gösterilir.

Kullanıcı işlemin başına geri dönmek için iptal edebilir veya onaylamak için **Tamam**'ı tıklayabilir. İkinci durumda, üretim emri **Başlatıldı** durumuna ayarlanır, ilgili günlükler nakledilir, denetim ilk adıma geri taşınır ve kullanıcıya "Tamamlanan Çalışma" iletisi gösterilir.


## <a name="creating-the-controller"></a>Denetleyici oluşturma

İş sürecini oluşturmanın ilk adımı, bir denetleyicinin varsayılan davranışlarını uygulayan **ProcessGuideController** denetleyicisi soyut sınıfından genişleyen, denetleyici sınıfını oluşturmaktır. Yeni sınıf adı **ProdProcessGuideProductionStartController**'dır ve **StartProdOrder** öğesinin **WHSWorkExecuteMode** değeri ile donatılmıştır. **WHSWorkExecuteDisplay** sınıflarında kullanılan aynı **SysExtension** tabanlı örnekleme kullanılır. Bu, mod için bir menü öğesi çalıştırdığında denetleyicinin örneğini oluşturmaya yardımcı olur.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Sınıfın adlandırma deseni şöyledir: **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Bu, denetleyici sınıfları için kullanılan ve diğer sınıflara genişletecek bir desendir.


## <a name="building-the-first-step"></a>İlk adımı oluşturma

Sonra, ilk adımı tanımlamak için **ProcessGuideStep**'ten genişleyen, **ProdProcessGuidePromptProductionIdStep** sınıfını oluşturursunuz.

Daha sonra sınıfı örneklerle destekleme görevi bir adım fabrikasına atanır, bu da **ProcessGuideController** temel sınıfı tarafından çağrılır. Varsayılan fabrika uygulaması, adımın adına göre başlatır. Bu nedenle, denetleyicideki ilk adım olarak **ProdProcessGuidePromptProductionIdStep** kimliği adımını başlatmak için, iki şey yapmanız gerekir:

-   **ProdProcessGuidePromptProductionIdStep** sınıfını bir **ProcessGuideStepName** özniteliğiyle donatın.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Denetleyici sınıfında, adım adını döndürmek için **initialStepName()** soyut yöntemini uygulayın.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> **ProcessGuideStepName** özniteliğindeki değerin, yukarıda gösterilen sınıf adıyla tam olarak eşleşmesi gerekmez. Ancak bunu uygulamak, sınıf kullanırken, çapraz referanslar etrafında birlik ve tür güvenilirlik sağlar. Bu adlandırma kuralını kullanmanız önerilir.
>
> **ProcessGuideStepName** tabanlı adım örneği **ProcessGuideStepDefaultFactory** sınıfında uygulanır. Nadiren de olsa adımı başlatmak için farklı bir strateji istiyorsanız, aşağıdakileri yapmanız gerekir:
> -   **ProcessGuidStepAbstractFactory**'den devralan yeni bir fabrika sınıfı oluşturun.
> -   İsteğe bağlı olarak, fabrikada gereken parametreleri içeren **ProcessGuideIStepCreationParameters** arabirimini uygulayan yeni bir parametre sınıfı oluşturun.
> -   Denetleyici sınıfınıza, yukarıdaki fabrika ve parametreleri döndürmek için **stepFactory()** ve **stepCreationParameters()** yöntemlerini geçersiz kılın.

Sonraki adım, **ProdProcessGuidePromptProductionIdStep** sınıfının işlevini uygulamaktır. Kullanıcı arabirimini oluşturmak, kullanıcı tarafından girilen verileri işlemek ve adımın ne zaman tamamlandığını belirlemek için mantık uygulamanız gerekir.

### <a name="building-the-user-interface-for-the-first-step"></a>İlk adım için kullanıcı arabirimi oluşturma

Kullanıcı arabirimi, **ProcessGuidePageBuilder** soyut sınıfından miras alınan bir sınıf kullanılarak oluşturulur. Bu adım için, ne yaptığını belirtmek için sınıfı adlandırın: **ProdProcessGuidePromptProductionIdPageBuilder**.

Sınıfın örnek oluşturma mekanizması, adımın denetleyiciden nasıl örneklendiği ile benzerdir. 

-   **ProdProcessGuidePromptProductionIdPageBuilder** sınıfını bir **ProcessGuidePageBuilderName** özniteliğiyle donatın.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   **ProdProcessGuidePromptProductionIdStep** sınıfında, bu adı döndürmek için **pageBuilderName()** soyut yöntemini uygulayın.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Adım fabrikasına benzer şekilde, sayfa oluşturucu fabrikası için uygulanan bir soyut fabrika modeli de vardır. Bu nedenle, nadiren de olsa sayfa oluşturucuyu başlatmak için farklı bir strateji istiyorsanız, aşağıdakileri yapmanız gerekir:
> - **ProcessGuidePageBuilderAbstractFactory**'den devralan yeni bir fabrika sınıfı oluşturun.
> - İsteğe bağlı olarak, fabrikada gereken parametreleri içeren **ProcessGuideIPageBuilderCreationParameters** arabirimini uygulayan yeni bir parametre sınıfı oluşturun.
> - Adım sınıfınıza, yukarıdaki fabrika ve parametreleri döndürmek için **pageBuilderFactory()** ve **pageBuilderCreationParameters()** yöntemlerini geçersiz kılın.

Kullanıcı arabirimini uygulamak için üretim emri kodunu girmek için bir metin kutusuna sahip bir sayfaya ve ayrıca bir **Tamam** düğmesine ve **İptal** düğmesine girmek ihtiyacınız vardır. **İptal** düğmesi işlemden çıkmalı.

Bunu uygulamak için, **ProdProcessGuidePromptProductionIdPageBuilder** sınıfındaki iki yöntemi geçersiz kılmanız gerekir:

-   Metin kutusunu eklemek için **addDataControls()** yöntemini kullanın.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   **Tamam** ve **İptal** düğmelerini eklemek için **addActionControls()** yöntemini kullanın.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Bu, ardından düğmeler gelen veri denetimlerini ekler. Ancak, veri denetimleri ve düğmeleriyle bir ekran oluşturmak istiyorsanız, esneklik için bunun yerine **addControls()** yöntemini geçersiz kılabilirsiniz.

Örneğin, kullanıcı hatalı bir üretim emri kodu girerse, doğrulama hataları söz konusu olduğunda sayfanın nasıl yeniden oluşturulacağı ele alınacak ek bir senaryodur. **ProcessGuidePageBuilder** temel sınıfı, kullanıcı arabirimini yeniden oluşturan, taranan değeri bırakan varsayılan davranışı uygular ve hata iletisi hata denetimini ekler. Kullanmak istediğiniz varsayılan davranış olduğu için, hataları işlemek için herhangi bir kod eklemeniz gerekmez.

> [!TIP]
> Hata durumları için özel UI davranışı uygulamak istiyorsanız, **rebuildFromRequestPage()**, **isErrorState()** ve **reuseRequestPageOnError()** yöntemlerinden birini veya birkaçını geçersiz kılabilirsiniz.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Kullanıcı tarafından girilen verileri ilk adımda işleme

Verilerin işlenmesi, **ProcessGuideDataProcessorDefault** sınıfında gerçekleştirilir ve bu da eski **WhsRfControlData** sınıfını çağırır. Bu varsayılan davranışta herhangi bir değişikliğe gerek yoktur ve **WhsRfControlData**'nın **ProdId** alanını doğrulama mantığı zaten vardır; bu nedenle bunu işleme mantığı yazmanız gerekmez. Doğrulama mantığı için gerekli uzantılar olması durumunda, **WhsControl** tabanlı genişletme mekanizmasını kullanmayı düşünün.

### <a name="determine-if-the-first-step-is-complete"></a>İlk adımın tamamlanıp tamamlanmadığına karar verin

Doğrulama başarılı olduğunda, adımın tamamlandı olarak işaretlenmesi zaman alabilir. Bu temel sınıfta yapılır, ancak adımın tamamlanması için koşulu uygulamanız gerekir. Aşağıdaki geçersiz kılınmış yöntem bunu yapar.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>İkinci adım: Sipariş ayrıntılarını görüntüleyin ve onaylayın

İşlemin ikinci adımında kullanıcıya sipariş ile ilgili ayrıntıların bulunduğu bir ekran gösterilir. Kullanıcı, üretim emrinin başlangıcını onaylamak için **Tamam** düğmesini tıklatabilir veya işlemin başlangıcına geri dönmek için **İptal**'i tıklatabilir. Bu örnek için, adıma **ProdProcessGuideConfirmProductionOrderStep** adını ve sayfa oluşturucu sınıfına **ProdProcessGuideConfirmProductionOrderPageBuilder** adını verin.

ProdProcessGuideConfirmProductionOrderStep sınıfı aşağıdakine benzer.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Kullanıcı buraya değer girmediği için, **isComplete()** yöntemini geçersiz kılmalısınız. Kullanıcı **Tamam**'ı tıklattığında adım tamamlanmıştır.

Sayfa oluşturucu sınıfı, üç etiket eklemek için **addDataControls()** yöntemini geçersiz kılar. İlk etiket, üretim emri kodunu gösterir; ikincisi madde bilgileri (madde kodu, boyutlar veya açıklama gibi) içerir ve üçüncüsü miktarı ve ölçü birimini içerir.

Daha sonra **addActionControls()** 2 düğme (**Tamam** düğmesi ve işlemi iptal edip başlangıca geri dönmek için **İptal** düğmesi) eklemek için geçersiz kılınır.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Uygulama Gezgini'ni kullanarak bu konudaki X++ yöntemleri için aynı kaynak kodunu bulabilirsiniz. Sınıf adına filtre uygulayın, sonra sınıf adını sağ tıklatıp **Kodu görüntüle**'yi seçin.

### <a name="step-3-start-the-production-order"></a>Adım 3: Üretim emrini başlatın

Üçüncü adım, üretim emrinin başlatılması için iş mantığının yürütüldüğü yerdir. Bu adım, önceki adımlardan biraz farklıdır (bu adımda bir kullanıcı arabirimi yoktur). Bu adım, kullanıcı önceki adımda **Tamam**'ı tıklattığında yürütülür.

**ProcessGuideStepWithoutPrompt** soyut sınıfı, bu tür adımlar için varsayılan davranışı uygular. Bu nedenle, geçerli adım **ProcessGuideStepWithoutPrompt** sınıfını genişletmeli ve **doExecute()** yöntemini geçersiz kılmalıdır.

Aşağıdaki kod örneğinde, sınıf ve **doExecute()** yöntemi uygulaması gösterilmektedir. Yöntem, hem sipariş kodunu hem de kullanıcı kimliğini oturum durumundan alır ve bu üretim emrini başlatmak için gereken yöntemi çağırır.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Bir özel durum söz konusuysa, çerçeve özel durum işleme mantığı, işlemin önceki adıma döndürülmesine olanak sağlar.

> [!NOTE]
> **addProcessCompletionMessage()** çağrısı, Gezinti parametrelerine "Tamamlanan çalışma" iletisini ekler. Sonraki adım (bir kullanıcı arabirimi olduğu varsayılır) bu iletiyi görüntüler. Temel sınıflar bu mantığı işler ve bu davranışa ulaşmak için işlem sınıflarına eklenmesi gereken belirli bir kod yoktur.


### <a name="building-the-navigation-through-the-steps"></a>Adımlar boyunca gezinmeyi oluşturma

**ProcessGuideController** temel sınıfı, kaynak ve hedef adımların basit bir haritası olan önceden tanımlanmış gezinti rotasını temel alan **ProcessGuideNavigationAgentDefault** sınıfını başlatır. Üretim başlangıç senaryosu için, koşullu dallanma olmadığından, bu uygulama yeterli olacaktır. Bu nedenle, gezinti rotasını tanımlamak için yalnızca **initializeNavigationRoute()** yöntemini geçersiz kılmanız gerekir.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Koşullu dallanmaya (kullanıcı eylemlerine veya başka herhangi bir koşula göre) sahip olacak işlemler vardır. Bu tür işlemlerle aşağıdakileri yapmanız gerekir:

-   **ProcessGuideNavigationAgent** sınıfından devralınan belirli gezinti aracılarını uygulayın.

-   Geçerli adıma, oturum durumuna, kullanıcı eylemine veya diğer mantığa dayalı doğru gezinti aracısını başlatmak için mantık içeren **ProcessGuideNavigationAgentAbstractFactory** sınıfından devralınan özel gezinti aracısı fabrikası uygulayın.

-   İsteğe bağlı olarak, uygun parametreleri geçirmek için denetleyici sınıfındaki **navigationAgentCreationParameters()** öğesini geçersiz kılın.

-   Yukarıda oluşturulan gezinti aracısı fabrikasını başlatmak için denetleyicideki **navigationAgentFactory()** öğesini geçersiz kılın.

### <a name="action-classes"></a>Eylem sınıfları

Eylem sınıfları, kullanıcı eylemlerini temsil ettiğinden, bu örnek eylemlerin nasıl oluşturulduğunu göstermek için **Tamam** eylemini kullanır.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Sınıfın, 2 soyut yöntem uygulamalıdır:

-   Bu eyleme bağlı bir düğme denetiminde görüntülenecek etiketi döndüren **etiket()**.

-   Eylemi gerçekleştiren **doExecute()**. Daha önce bahsedildiği gibi, **Tamam** düğmesi yalnızca adım için geri çağrı yapar. Ancak, diğer eylemler burada daha karmaşık mantığa sahip olabilir.

Eylemler, **ProcessGuideActionName** özniteliğine dayalı **SysExtension** çerçevesi kullanılarak örneklendirilir. Sayfa oluşturucuları örneklendirmesine benzer şekilde adım sınıfı varsayılan eylem fabrikasını uygular ve bunu geçersiz kılmak mümkündür. Sayfa oluşturucu, aşağıdakine benzer bir düğme denetimi ekler.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Böyle bir durumda, geçirilen ad için bir eylem sınıfı oluşturmak ve düğmeye bu eylemi uygulamak için adım sorar.

### <a name="summary"></a>Özet

Bu konuda açıklanan her şeyi özetlemek için, süreç için gereken kodun kapsamlı bir özeti aşağıda verilmiştir:

1.  **ProdProcessGuideProductionStartController**

    1.  İlk adımın adını sağlamak için **initialStepName()** öğesini geçersiz kılın.
    2.  Gezinti haritasını oluşturmak için **initializeNavigationRoute()** öğesini geçersiz kılın.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Adımın tamamlandı olarak kabul edileceğini belirtmek için **isComplete()** öğesini geçersiz kılın.
    2.  Kullanılacak sayfa oluşturucusunu belirtmek için **pageBuilderName()** öğesini geçersiz kılın.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  **Prod ID** metin kutusunu eklemek için **addDataControls()** öğesini geçersiz kılın.
    2.  **Tamam** ve **İptal** düğmelerini eklemek için **addActionControls()** yöntemini geçersiz kılın.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Kullanılacak sayfa oluşturucusunu belirtmek için **pageBuilderName()** öğesini geçersiz kılın.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Sipariş, madde ve miktar bilgileri etiketlerini eklemek için **addDataControls()** öğesini geçersiz kılın.

    2.  **Tamam** ve **İptal** düğmelerini eklemek için **addActionControls()** yöntemini geçersiz kılın.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Madde bilgi etiketlerini oluşturmak için kullanılan **generateItemInfoForProdId()** yöntemi bu konunun dışında bırakılmıştır. Bu yöntem, madde kodu, açıklama ve boyutları almak için birkaç tabloyu sorgular. **generateItemInfoForProdId()** öğesinin daha iyi anlaşılmasını istiyorsanız, kaynak koda bakın.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Üretim başlatma işlemini gerçekleştirmek ve işlem tamamlama iletisini eklemek için **doExecute()** öğesini geçersiz kılın.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Ortak desenlerin çok fazla olduğunu unutmayın (hata durumunda UI'nın yeniden oluşturulması, işlem tamalama iletisini belirleme, **Tamam** ve **İptal** davranışı), çerçeveye taşınmıştır. Bu sayede uygulama geliştiricisinin hatalara açık olan ve işlemler genelinde tutarsız davranış riski taşıyan standart kod yazmasına gerek kalmaz. Senaryonun ortak yoldan sapması gerektiğinde, uygulama geliştiricisine uygun yöntemleri geçersiz kılma seçeneği sağlamıştır, ancak bunlar hem açık hem de izleme olan bilerek yapılan bir sapmadır.


### <a name="extending-a-business-process"></a>İş sürecini genişletme

Buraya kadar, bu konuda **ProcessGuide** çerçevesi kullanılarak yeni bir işlemin nasıl oluşturulacağını vurgulandı. Bu son bölümde, bu iş sürecinin nasıl uzatılabilecek hakkında örnekler bulacaksınız.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Akışta bir adım ekleyin (ProcessGuideNavigationAgentDefault kullanarak)

Genişletilme yeri:

-   İşlem için **ProcessGuideController** sınıfının alt öğesi.

Nasıl genişletileceği:

-   Denetleyici sınıfında **initializeNavigationRoute()** yöntemini genişletin ve **ProcessGuideNavigationRoute** sınıfında **addFollowingStep()** öğesini çağırın.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Akışta bir adım ekleyin (özel gezinme aracısını kullanarak)

Genişletilme yeri:

-   **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**'ın alt öğesi.

Nasıl genişletileceği:

-   İstenen adım adını döndüren **ProcessGuideNavigationAgent** öğesinin yeni bir alt sınıfını oluşturun.

-   Yukarıda oluşturulan gezinti aracısını koşullu olarak döndüren **ProcessGuideNavigationAgentFactory**'den türetilen yeni bir sınıf oluşturun.

-   Yukarıda oluşturulan fabrikayı döndürmek için denetleyicideki **navigationAgentFactory()** yöntemini genişletin.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Varolan bir adımın kullanıcı arabirimine yeni bir denetim ekleme 

Genişletilme yeri:

-   Adım için **ProdProcessGuidePageBuilder**'ın alt öğesi.

Nasıl genişletileceği:

-   **addDataControls()** yöntemini genişletin ve ek denetimi ekleyin.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Kullanıcı arabiriminin varolan bir adımda tam olarak tamamlanması

Genişletilme yeri:

-   **ProdProcessGuideStep**'in alt öğesi.

Nasıl genişletileceği:

-   **ProdProcessGuidePageBuilder** sınıfının yeni bir alt sınıfını oluşturun ve istenen kullanıcı arabirimini uygulayın.

-   Yukarıda oluşturulan sınıfa yönelik **ProcessGuidePageBuilderNameAttribute** öğesini döndürmek için adım sınıfında **pageBuildeName()** yöntemini genişletin.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Bir adım tamamlandığında mantığı değiştirin

Genişletilme yeri:

-   **ProdProcessGuideStep**'in alt öğesi.

Nasıl genişletileceği:

-   Ek mantık oluşturmak için **isComplete()** yöntemini genişletin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]