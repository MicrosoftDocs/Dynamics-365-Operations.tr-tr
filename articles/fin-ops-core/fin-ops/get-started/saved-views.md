---
title: Kayıtlı görünümler
description: Bu konu, kaydedilmiş görünümler özelliklerinin nasıl kullanılacağını açıklar.
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: fe79558b9d2ac4ef1c83918b949d11983b2cc0d8
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260495"
---
# <a name="saved-views"></a>Kayıtlı görünümler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Giriş
Kişiselleştirme, kullanıcıların ve kuruluşların gereksinimlerine uygun Kullanıcı deneyimini en iyi duruma getirmesine izin verirken önemli bir rol oynar. Kişiselleştirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

Geleneksel kişiselleştirmeyle, kullanıcıların her form için yalnızca tek bir kişiselleştirmeler kümesi olabilir. Kaydedilmiş görünümler, birçok önemli yolla kişiselleştirmede genişletir:

-    Görünümler, kullanıcıların form başına birden çok adlandırılmış kişisel grup kümesine sahip olmasını ve bunlar arasında hızla geçiş yapabilmelerini sağlar. Bu, kullanıcının belirli bir iş görevi yerine getirmek üzere her bir görünüm için tasarlanmış birden çok iyileştirilmiş görünüm oluşturmasını sağlar. 

-    Belirli sayfa türleri için oluşturulan görünümler, kullanıcı tarafından eklenmiş filtreler ve sıralamalar da içerebilir, bunlar da kullanıcıların yaygın olarak filtrelenen veri kümelerine hızlıca dönmesine olanak sağlar. Daha fazla ayrıntı için [Hangi sayfalar görünümleri destekler](saved-views.md#what-pages-support-views) bölümüne göz atın. 

-    Görünümler, belirli güvenlik rollerindeki ve belirli tüzel kişiliklerdeki kullanıcılara yayımlanabilir. Bu nedenle, belirli bir tüzel kişilite belirtilen role ve erişime sahip herhangi bir kullanıcı, söz konusu kullanıcı bunu kişiselleştirmemesine rağmen o görünüme erişebilir ve bu görünümü kullanabilir. Bu yayımlama yeteneği, kuruluşların işletmeler için en iyi duruma getirilmiş şirket standart görünümlerini tanımlamasına olanak tanır. Daha fazla bilgi için bkz. [Kişiselleştirmeleri görünümler ile kuruluş düzeyinde yönetmek](saved-views.md#managing-personalizations-at-an-organizational-level-with-views)

-    Geleneksel kişiselleştirmenin aksine, bir kullanıcı açık kişiselleştirmeler gerçekleştirdiğinde veya bir listeye filtre uyguladığında görünümler otomatik olarak kaydedilmez. Açık kaydetmeler, bir görünümü, bu görünüm ile değişiklikler ilişkilendirilmeden önce oluşturmak için esneklik sağlamak ve görünüm tanımlarının uzun süreli kullanım için amaçlanmayan istem dışı olarak filtreler veya kişiselleştirmeler ile değiştirilmediğinden emin olmak üzere gereklidir.  

-    Görünümler, çalışma alanlarına kutucuk, liste veya bağlantı olarak eklenebilir. Bu nedenle, filtrelenmiş bir veri kümesi bir çalışma alanında görüntülenebilir ve kullanıcılar, o veri kümesiyle ilgili bir dizi kişiselleştirme kümesini kutucuk veya bağlantıyla ilişkilendirebilir.

## <a name="switching-between-views"></a>Görünümler arasında geçiş yapma
Görünümler bir ortam için etkinleştirildikten sonra, görünümleri destekleyen tüm sayfalar formun en üstüne, geçerli görünümün adını gösteren daraltılmış bir görünüm seçicisi denetimi içerir.  

Görünüm seçicisinde iki boyut varyasyonu vardır: 

-   **Büyük görünüm seçicileri**: Bir listeyi gösteren sayfalar, birkaç nedenden dolayı daha büyük görünüm seçicisine sahip olacaktır. En önemlisi, daha büyük görünüm seçicisi, kullanıcı tanımlı filtreleri içerebilen sayfaları belirtir. Filtreler görünümlerde yer aldığından, görünüm adları ekranda gösterilen verilerin en iyi açıklaması olacağı ve beklentilerin kullanıcıların Bu sayfa türlerinde daha sık geçiş yapma işlemi olacağı için büyük seçici boyutuna da izin verilir.  
 
-   **Küçük görünüm seçicileri**: Diğer tüm tam sayfa formları (çalışma alanları ve gösterge tablosu hariç), sayfa başlığının yanında görünen daha küçük bir görünüm seçicisine sahiptir. Bu sayfalardaki görünümler yalnızca kişiselleştirmeler içerir (kullanıcı tanımlı filtreler değil). Bu sayfalarda form başlığı veya kayıt başlığı genellikle formun üst kısmındaki en önemli bilgiler olur. Daha küçük boyut ayrıca, bu sayfalarda daha düşük olan görüntüleme geçişi sıklığını da yansıtır. 
 
Görünüm adını tıklatırsanız, görünüm seçicisi açılır ve bu sayfayla ilgili kullanılabilir görünümlerin listesini gösterir

-    **Standart görünüm**: **Standart** görünüm (daha önce **Klasik** görünüm olarak bilinirdi), açık kişiselleştirmelerin uygulanmadığı kullanıma hazır sayfa görünümüdür.
-    **Kişisel görünümler**: Asma kilitleri olmayan görünümler kişisel görünümlerinizi temsil eder. Bunlar, oluşturduğunuz veya bir yöneticinin size verdiği görünümlerdir.  
-    **Kilitli görünümler**: Bazı görünümlerde ( **Standart** görünüm ve rolünüze yayımlanmış görünümler gibi), görünüm seçicide görünümün yanında bir asma kilit simgesi bulunur. Bu simge, bu görünümleri düzenleyemeyeceğinizi belirtir. Ancak, sayfa kullanımını yansıtan örtülü kişiselleştirmeler otomatik olarak kaydedilir. Bu örtülü kişiselleştirmeler, bir ızgara sütununun genişliğine veya bir hızlı sekmenin genişletilmesine veya daraltılmasına yönelik bir değişiklik içerir. Ancak kişiselleştirme ayrıcalıklarınız varsa, **Farklı kaydet** eylemini kullanarak kilitli bir görünümü temel alan kişisel bir görünüm de yapabilirsiniz.
-    **Yeni görünümler**: Henüz açılmamış yayınlanmış görünümler, görünüm adının solundaki bir spark ile ayarlanır.  

Farklı bir görünüme geçmek için önce görünüm seçicisini açın ve sonra yüklemek istediğiniz görünümü seçin. 

## <a name="creating-and-modifying-views"></a>Görünüm oluşturma ve değiştirme
Geleneksel kişiselleştirmenin aksine, bir kullanıcı açık kişiselleştirmeler gerçekleştirdiğinde (veya bir listeye filtre uyguladığında) görünümler otomatik olarak kaydedilmez. Bu değişiklikleri bir görünüme kaydetmek için açık bir eylem gerekli. Bu, kullanıcıya bir görünümü, bu görünüm ile değişiklikler ilişkilendirilmeden önce oluşturmak için esneklik sağlamak ve görünüm tanımlarının istem dışı olarak filtreler veya kişiselleştirmeler ile değiştirilmediğinden emin olmak üzere gereklidir. Açık kişiselleştirmelerin (örneğin genişleyen veya daralan hızlı sekme veya bir sütunun genişliğinin değişmesi gibi), kilitli görünümler için bile otomatik olarak güncel görünüme kaydedildiğini unutmayın. 

Görünümün geçerli durumunun bilindiğinden emin olmak için, açık kişiselleştirme veya filtreleme gerçekleştirerek bir görünümde değişiklik yapmaya başladığınızda, geçerli görünüm adının yanında, kaydedilmemiş, değiştirilmiş bir sürümü aradığınızı belirten bir yıldız işareti görünür.

Bu değişiklikleri kaydetmek istiyorsanız, aşağıdaki adımları izleyin.
1.  Görünüm seçiciyi açmak için görünüm adını seçin.
2.  Varolan görünümü değiştirmek için:
     1. **Kaydet**'i seçin. Bu eylemin kilitli görünümler için etkinleştirilmeyeceğini unutmayın. 
3.  Yeni bir görünüm oluşturmak için:
     1.    **Farklı kaydet**'i seçin. 
     2.    Bir görünüm adı ve (isteğe bağlı olarak) bir açıklama girin.
     3.    **Kaydet**'i seçin.

## <a name="changing-the-default-view"></a>Varsayılan görünümü değiştirmek
Varsayılan görünüm, sayfaya ilk gittiğinizde sistemin açmaya çalışacağı görünümdür. Bunu en sık olarak kullanmayı beklediğiniz görünüme ayarlamalısınız.  

Bir sayfa için varsayılan görünümü değiştirmek için şu adımları izleyin: 
1.  Varsayılan olarak kullandığınız görünüme geçin. 
2.  Görünüm seçiciyi açmak için görünüm adını seçin. 
3.  **Daha fazla** ve **Varsayılan olarak sabitle**'yi seçin.  

Alternatif olarak, yeni bir görünüm oluştururken (**Farklı kaydet** eylemini kullanarak), görünümü kaydetmeden önce, **Varsayılan olarak sabitle** olarak ayarlayarak yeni görünümü varsayılan görünüm haline getirebilirsiniz.

Bazı durumlarda, bir sayfaya ilk gittiğinizde varsayılan görünümle ilişkilendirilmiş sorgunun yürütülmeyeceğini unutmayın. Örneğin, bir sayfaya bir kutucukta gezindiğinizde, kutucuktaki sorgu, varsayılan görünümle ilişkilendirilmiş sorgudan bağımsız olarak yürütülür. Ayrıca, Standart görünümle tanımlı bir sorguya sahip olan bir sayfaya giderseniz, orijinal sorgu varsayılan görünümün sorgusunun yerine yürütülür. Bu durumda, görünüm yüklenirken bir bilgi iletisi ile uyarı alırsınız. Sayfa yüklendikten sonra görünümlerin değiştirilmesi, görünüm sorgusunun beklendiği gibi yürütülmelerine olanak sağlar. Sürüm 10.0.10 Platform Update 34'ten başlayarak, bilgi iletisi varsayılan görünümün sorgusunu doğrudan yükleme olanağı sağlayan katıştırılmış bir eyleme sahip olacaktır.

## <a name="managing-personal-views"></a>Kişisel görünümleri yönetme 
**Görünümlerimi Yönet** iletişim kutusu, kişisel görünümleriniz ve görünüm seçicisindeki görünümlerin sırası üzerinde temel bakım olanakları sağlar. Bu sayfayı açmak için görünüm seçiciyi açılır menüsünü açmak üzere görünüm adını tıklatın, **Diğer**'i seçin ve sonra **Görünümlerimi Yönet**'i seçin.  

Bu sayfayla ilgili kullanılabilir görünümlerin listesi için aşağıdaki eylemler kümesi kullanılabilir.  
-    **Varsayılan görünümü değiştir**: **Varsayılan olarak sabitle** eylemini geçerli vurgulanmış görünümü bu sayfa için varsayılan görünüm yapmak üzere kullanın.  
-    **Görünümlerinizi yeniden sıralayın**: Görünümlerinizi belirli bir sırada yeniden düzenlemek için **Yukarı taşı** ve **Aşağı taşı** eylemlerini kullanın.  
-    **Görünümüyeniden adlandırın**: Vurgulanmış olan kişisel görünümün adını değiştirmek için **Yeniden Adlandır** eylemini kullanın. Bu eylem kilitli görünümler için kapatılmıştır. 
-    **Görünümü sil**: Geçerli olarak vurgulanmış görünümü sayfadan kalıcı olarak silmek için **Kaldır** eylemini kullanın. Bir görünümü kaldırdıktan sonra kurtarmanın bir yolu yoktur.  

Bu iletişim kutusunda yapılan tüm değişiklikler **Kaydet** düğmesini seçtikten sonra etkinleşir.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Organizasyon düzeyindeki kişiselleştirmeleri görünümleriyle yönetmek
Kaydedilmiş görünümlerin kuruluş düzeyinde kişiselleştirmenin yönetimini geliştirmeye nasıl yardımcı olduğunu anlamanıza yardımcı olması için bu bölümde kişiselleştirme yönetiminin, kaydedilen görünümler özelliği olmadan önce nasıl çalıştığı açıklanmaktadır.

Görünümler olmadan, yöneticiler bir sayfaya, bir kullanıcı grubuna veya kişiselleştirme sayfasını kullanan kullanıcılara sayfa için bir kişisel ayarlar uygular. Bu kullanıcılar kişiselleştirme haklarına sahip ise, kişiselleştirmeler o sayfaya uygulanır. Ancak, kullanıcıların sayfayı daha fazla kişiselleştirmesinin önleneceği ve böylece kuruluş, kullanıcıların tutarlı bir kullanıcı arabirimine sahip olmasını gerektirmediğinden emin olunmamıştır. Bu kullanıcıların kişiselleştirme hakları yoksa, bir yönetici tarafından kendilerine verilen kişiselleştirmeler yüklenmemiştir. Dahası, yeni kullanıcılar bir kuruluşta işe alındığında, yöneticiler kullanıcı için kişiselleştirmeler kümesini el ile yüklemek zorunda kalmaktadır. O roldeki kullanıcılar tarafından kullanılabilecek belirli bir kişisel belirleme kümesini belirtmek için otomatik bir mekanizma yoktur.

Kaydedilmiş görünümler özelliği, öncelikle görünümlerin kullanıcı gruplarına yayımlanabilmesi nedeniyle, kişiselleştirmelerin için kuruluş düzeyinde yönetimini önemli ölçüde kolaylaştırır. Bir görünüm yayımlandıktan sonra tanımlı güvenlik rollerinden birine sahip olan ve belirtilen tüzel kişiliklerde bulunan tüm kullanıcılar, kullanıcının kişiselleştirilme yapması mümkün olmamakla birlikte, görünüm gösterilebilir ve kullanılabilir. Her kullanıcının, sayfa kullanımı (örtülü kişiselleştirmeler) otomatik olarak uygulandığı yayımlanmış görünümün bir kopyası olmasına karşın, hiçbir kullanıcı yayımlanmış bir görünüme açık kişiselleştirme veya sorgu güncelleştirmeleri kaydedemez. Başka bir deyişle, yayınlanan görünümler kilitlenir. Ek olarak, yeni kullanıcılara görünümlerin yayımlandığı tüzel kişilikler içinde roller verilirse, rolleri ve tüzel kişilikler ile ilişkili görünümleri otomatik olarak görürler. Yönetici tarafından başka bir eyleme gerek yoktur. Benzer şekilde, kullanıcılar bir kuruluştaki rolleri değiştirdiklerinde veya farklı tüzel kişiliklere erişim verildiğinde, kendileri için daha önce yayınlanmış görünümlere artık erişemeyebilirler. Yine, yönetici tarafından başka bir eyleme gerek yoktur.

Yayımlanmış bir görünüme yapılan güncelleştirmeler, görünümü uygun güvenlik rollerine ve tüzel kişiliklere yeniden yayımlayarak kullanıcılara kolayca dağıtılabilir.

Bu yayımlama yeteneği, kuruluşların işletmeler için belirli güvenlik rollerindeki kullanıcıları hedeflemiş olarak en iyi duruma getirilmiş şirket standart görünümlerini tanımlamasına olanak tanır.  

## <a name="publishing-views"></a>Yayımlama görünümleri
Yayımlama işlemi sırasında, görünümler bir veya daha fazla tüzel kişilik için bir veya daha fazla güvenlik rolüne atanabilir. Bu nedenle, bir tüzel kişiliğe erişimi olan ve bu rollerden birine atanan tüm kullanıcılar, düzenleyemeseler bile görünümlere erişebilir ve bunları kullanabilirler. Sistem yöneticilerinin görünüm seçicisi açılır menüsünde bulunan **Yayımla** eylemine erişimi vardır. Bununla birlikte, kuruluştaki diğer güvenilen kullanıcılara da, yeni **Kaydedilmiş görünümler yöneticisi** rolü aracılığıyla görünüm yayımlamasına erişim izni verilebilir.

Bir görünümü yayımlamak için şu adımları izleyin: 
1.  Yayımlamak istediğiniz görünümün kişisel bir kopyasını oluşturun ve kaydedin. 
2.  Şu anda yüklü olan görünümle, görünüm adını, görünüm seçici açılır menüsünü açmak için seçin. 
3.  **Diğer** düğmesini ve ardından **Yayımla**'yı seçin. Yayınla iletişim kutusu açılır.  
4.  Görünüm için bir ad ve (isteğe bağlı olarak) bir açıklama girin. Girdiğiniz ad, görünümü alan kullanıcıların görünüm seçicileri içinde görebilmeleri için kullanılan addır. Bir sayfayla ilgili yayımlanmış görünümlerin adları benzersiz olmalıdır. Görünümlerin uygulandığı roller listesi veya tüzel kişilikler farklılık gösterse bile yinelenen adlara izin verilmez.
5.  Bu görünüm tarafından hedeflenen kullanıcılara karşılık gelen güvenlik rollerini ekleyin.
6. Bu görünümün kullanılabilir olması gereken tüzel kişilikleri ekleyin. 
7. [10.0.9/Platform update 33 veya sonrası] Görünümün, seçilen kullanıcılar için varsayılan görünüm olarak yayımlanıp yayımlanmayacağını belirleyin. Bir görünümün varsayılan olarak yapılması, bu görünümün, kullanıcıların hedef sayfayı bir sonraki açtıklarında görecekleri görünüm olduğu anlamına gelir. Bu, kullanıcıların varsayılan görünümünü değiştirecek; ancak, yayımlama gerçekleştirildikten sonra kullanıcılar varsayılan görünümlerini değiştirmeye devam edebilir.    
8.  **Yayımla**'yı seçin.

Bazı ortamlarda, kullanıcılar yayımlanan görünümü görebilmeleri için biraz zaman (bir saat kadar) sürebilir.

## <a name="modifying-a-published-view"></a>Yayınlanmış görünümü değiştirme
Bir görünümü yayımladıktan sonra, yayınlanmış bir görünümde değişiklik yapmak istediğinizi fark edebilirsiniz. Yayımlanmış bir görünümde canlı değişiklikler yapamazsınız, ancak bu görünümler tüm kullanıcılar için (yayımcılar dahil) düzenlemeye karşı kilitlenmiş olduğundan, güncelleştirme yapmak için bir görünümü yeniden yayımlayabilirsiniz.  

Yayınlanmış bir görünümde yapmak istediğiniz değişiklikler yalnızca yayımlama parametreleri (görünümün adı ve açıklaması veya görünümün yayımlandığı güvenlik rolü) içeriyorsa, aşağıdakileri yapın: 
1.  Güncelleştirmek istediğiniz parametreler için yayımlanmış görünüme geçin. 
2.  Görünüm seçici açılır menüsünden **Yayımla**'yı seçin. 
3.  Varolan görünümü güncelleştirmek istiyorsanız **Evet**'i seçin (farklı bir ad altında yayımlamak istiyorsanız **Hayır**'ı seçin).
4.  Görünüm için ad, açıklama ve/veya güvenlik rollerini güncelleştirin. 
5.  **Yayımla**'yı seçin. 
6.  [10.0.8/Platform update 32 veya öncesi] Yayımlanan görünümün adını güncelleştirdikten sonra, yayımlanmış görünümü eski adıyla da silmeniz gerekecektir (daha ayrıntılı bilgi için **Yayınlanmış görünümleri yönetme** bölümüne bakın). 
7. [10.0.9/Platform update 33 veya sonrası] Özgün olarak bu yayımlanmış görünümü varsayılan görünüm olarak seçtiyseniz, yeniden yayımlamadan sonra bu kullanıcılar için varsayılan görünüm olur.  

Yayınlanan görünümde yapılan değişiklikler görünümle ilişkili kişiselleştirmeler veya filtrelerle değişiklik yapmak içeriyorsa, şu adımları izleyin: 
1.  Değiştirmek istediğiniz yayımlanmış görünüme geçin. 
2.  Yayımlanmış görünümün yerel taslağını oluşturmak için yayımlanmış görünümün bir kopyasını kaydedin. 
3.  Yerel taslağı gerekli değişikliklerle değiştirin.
4.  Görünümü özgün adıyla yayımlayın. 

## <a name="managing-published-views"></a>Yayımlanmış görünümleri yönetme
Kişisel görünümleri yönetmek gibi, **Görünümlerimi yönet** iletişim kutusu, yayımlama ayrıcalıklarına sahip kullanıcılara, yayımlanmış görünümler içeren bir sayfa üzerinde temel bakım yeterlilikleri sağlar (kendi kişisel görünümlerine ek olarak). Bu sayfayı açmak için görünüm seçiciyi açılır menüsünü açmak üzere görünüm adını tıklatın, **Diğer**'i seçin ve sonra **Görünümlerimi Yönet**'i seçin.

Tüm kullanıcılar kişisel görünümlerini gösteren **Görünümlerim** sekmesini görürken, yayımlama ayrıcalığına sahip kullanıcılar, o sayfa için yayımlanan tüm görünümleri gösteren **Yayımlanmış** bir sekmesi de görür. Birçok kullanıcı yayımlama görünümü olabileceği için, görünümü gerçekten yayımlamış olan kullanıcı olup olmadığına bakılmaksızın, yayımlanmış görünümlerin tam listesini yönetmeniz önemlidir.

Sayfa için tüm yayımlanmış görünümlerin listesi için aşağıdaki eylem kümesi kullanılabilir. 

-    **Yayınla**: Yayımlama parametreleri (ad, açıklama, güvenlik rolleri) değiştirildikten sonra bir görünümü yeniden yayımlamak için **Yayımla** eylemini kullanın.
-    **Kaldır**: Yayınlanmış bir görünümü kalıcı olarak silmek için **Kaldır** eylemini kullanın. Bu eylem sistemdeki tüm kullanıcıların görünümünü kaldırır. Yayınlanan görünümlerin kaldırılması **Kaydet** düğmesi seçildikten sonra etkili olur.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kaydedilmiş görünümleri ortamımda nasıl etkinleştirebilirim? 
Not: **kaydedilmiş görünümler** özelliği, kişiselleştirme sisteminin Finance and Operations'da etkinleştirilmesini gerektirir. Tüm ortam için kişiselleştirme kapatılmışsa, aşağıdaki adımları izleseniz bile görünümler devre dışı bırakılır. 

**10.0.9/platform güncelleştirmesi 33 ve sonrası** **kaydedilmiş Görünümler** özelliği, herhangi bir ortamda doğrudan Özellik yönetiminde kullanılabilir. Diğer genel Önizleme özellikleri gibi, üretim için bu özelliğin etkinleştirilmesi, [Tamamlayıcı Kullanım Koşulları Sözleşmesine](https://go.microsoft.com/fwlink/?linkid=2105274) tabidir.  

**10.0.8/Platform güncellemesi 32 ve öncesi** **kaydedilen Görünümler** özelliği, aşağıdaki adımları izleyerek ek test ve tasarım değişiklikleri sağlamak amacıyla katman 1 (geliştirme/test) ve katman 2 (korumalı alan) ortamlarında etkinleştirilebilir.

1.  **Uçuşu etkinleştirin**: Aşağıdaki SQL beyanını yürütün: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. Statik deneme sürümü önbelleğini temizlemesi için **IIS'yi Sıfırla**'yın. 

3.  **Özelliği bulun**: **Özellik Yönetimi** çalışma alanına gidin. **Kaydedilmiş görünümler** listede görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.   

4.  **Özelliği etkinleştirin**: **Özellikler listesinde kaydedilmiş görünümler** özelliğini bulun ve Ayrıntılar bölmesindeki **Şimdi etkinleştir**'i seçin.

Sonraki tüm kullanıcı oturumları kaydedilmiş görünümleri etkin olarak başlayacaktır.


### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Görünümler etkinleştirildiğinde varolan kişiselleştirmeler ne olur? 
Görünümler etkinleştirildiğinde, bir Kullanıcı ve form için varolan tüm kişiselleştirmeler, varsayılan görünüm olarak otomatik olarak ayarlanan **Görünümlerim** denen yeni bir görünüme kaydedilir. Bu, formlarda görünüm Seçicisi denetiminin görünmesi dışında, görünümler etkinleştirilmeden önce ve sonra tutarlı bir kullanıcı deneyimi olmasını sağlamak içindir.  

### <a name="what-pages-support-views"></a>Hangi sayfalar görünümleri destekler? 
Görünümler, sayfaların tümünde değil ama pek çoğunda bulunabilir. Özellikle, görünümler şu anda panolar ve çalışma alanları dışındaki tüm tam ekran sayfalarda kullanılabilirdir. İletişim kutuları, açılan diyaloglar, aramalar ve gelişmiş önizlemeler içeren tam ekran olmayan sayfalar da şu anda görünümleri desteklememektedir. Çalışma alanları ve iletişim kutuları gibi ek sayfa türleri için görüntüleme desteği gelecekteki bir güncelleştirmeyle ilgili olarak değerlendirilebilir.   

### <a name="who-is-allowed-to-publish-views"></a>Görünüm yayımlamaya kimlerin izni vardır?
Yalnızca sistem yöneticileri ve **Kaydedilmiş görünümler yöneticisi** rolüne atanmış kullanıcıların görünümleri yayımlama hakları vardır. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Bu görünüme ilişkin filtreleri niçin kaydedemiyorum? 
Bir filtrenin görünüm ile kaydedilmeye neden görünmeyebileceği birkaç neden vardır: 

- Sayfa, görünüm tanımının bir parçası olarak filtre kaydetmeyi desteklemiyor olabilir. Yalnızca büyük görünüm seçicileri olan sayfaların, kişiselleştirmeler ve sorgu değişikliklerinin görünüm olarak kaydedilmesine izin vermesi gerektiğini unutmayın. Daha fazla bilgi için **Görünümleri değiştirme** bölümüne bakın. 

- Söz konusu sayfa, görünüm sorgusunu tamamen görmezden gelebileceği veya verileri kalıcı olmayan geçici bir tabloda çalışabileceği için görünümleri doğru şekilde desteklemeyebilir. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Sayfayı ziyaret ederken hangi verileri görüyorum? 
Küçük görüntüleme seçili sayfalar için (görünüme yalnızca kişiselleştirmeler kaydedilebilir), sayfayı her zaman ziyaret ettiğinizde aynı verileri görürsünüz. 

Büyük görünüm seçicileri olan sayfalar için (kişiselleştirmeler ve sorgular görünüme kaydedilebilir), öncelikle varsayılan görünümle ilişkilendirilmiş sorguyla bağlantılı verileri görürsünüz. Bunun iki temel istisnası vardır: Bir sayfaya bir kutucukta gezindiğinizde, döşemedeki sorgu, varsayılan görünümle ilişkilendirilmiş sorgudan bağımsız olarak yürütülür. Bu kutucuğu, görünümler etkinleştirildikten sonra oluşturduysanız, bir kutucuk seçilmesi sayfayı o döşemeyle ilişkili görünümle açar.   
     - Bir sayfaya giderseniz ve bu giriş noktası bir sorguya sahipse, özgün sorgu başlangıçta varsayılan görünümün sorgusunun yerine yürütülür. Bu durumda, görünüm yüklenirken bir bilgi iletisi ile uyarı alırsınız. Ayrıca, sayfa yüklendikten sonra bu görünüme geçerek, görünüm sorgusunun ne olursa olsun yürütülmesine izin vermek istiyorsanız da onay alabilirsiniz.  


