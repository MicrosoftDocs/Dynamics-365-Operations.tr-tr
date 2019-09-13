---
title: Kayıtlı görünümler
description: Bu konu, kaydedilmiş görünümler özelliklerinin nasıl kullanılacağını açıklar.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 43f25796e6271f14acfc72f931398ab63338a307
ms.sourcegitcommit: b068b17ef708a0b349db8df1542e4244bb983d13
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870845"
---
# <a name="saved-views"></a>Kayıtlı görünümler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Giriş
Kişiselleştirme, kullanıcıların ve kuruluşların gereksinimlerine uygun Kullanıcı deneyimini Microsoft Dynamics 365 for Finance and Operations içinde en iyi duruma getirmesine izin verirken önemli bir rol oynar. Kişiselleştirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

Geleneksel kişiselleştirmeyle, kullanıcıların her form için yalnızca tek bir kişiselleştirmeler kümesi olabilir. Kaydedilmiş görünümler, birçok önemli yolla kişiselleştirmede genişletir:

-    Görünümler, kullanıcıların form başına birden çok adlandırılmış kişisel grup kümesine sahip olmasını ve bunlar arasında hızla geçiş yapabilmelerini sağlar. Bu, kullanıcının belirli bir iş görevi yerine getirmek üzere her bir görünüm için tasarlanmış birden çok iyileştirilmiş görünüm oluşturmasını sağlar. 

-    Belirli sayfa türleri için oluşturulan görünümler, kullanıcı tarafından eklenmiş filtreler ve sıralamalar da içerebilir, bunlar da kullanıcıların yaygın olarak filtrelenen veri kümelerine hızlıca dönmesine olanak sağlar. Daha fazla ayrıntı için [Hangi sayfalar görünümleri destekler](saved-views.md#what-pages-support-views) bölümüne göz atın. 

-    Görünümler güvenlik rollerine yayımlanabilir, bu da ilgili role sahip tüm kullanıcıların, kullanıcının kişiselleştirme yeteneğine bakmaksızın o görünüme erişebilir ve kullanılabilir olacağı anlamına gelir. Bu yayımlama yeteneği, kuruluşların işletmeler için en iyi duruma getirilmiş şirket standart görünümlerini tanımlamasına olanak tanır. [Kişiselleştirmeleri görünümler ile kuruluş düzeyinde yönetmek](saved-views.md#managing-personalizations-at-an-organizational-level-with-views)'e göz atın.

-    Geleneksel kişiselleştirmenin aksine, bir kullanıcı açık kişiselleştirmeler gerçekleştirdiğinde veya bir listeye filtre uyguladığında görünümler otomatik olarak kaydedilmez. Açık kaydetmeler, bir görünümü, bu görünüm ile değişiklikler ilişkilendirilmeden önce oluşturmak için esneklik sağlamak ve görünüm tanımlarının uzun süreli kullanım için amaçlanmayan istem dışı olarak filtreler veya kişiselleştirmeler ile değiştirilmediğinden emin olmak üzere gereklidir.  

## <a name="switching-between-views"></a>Görünümler arasında geçiş yapma
Görünümler bir ortam için etkinleştirildikten sonra, görünümleri destekleyen tüm sayfalar formun en üstüne, geçerli görünümün adını gösteren daraltılmış bir görünüm seçicisi denetimi içerir.  

Görünüm seçicisinde iki boyut varyasyonu vardır: 

-   **Büyük görünüm seçicileri**: Bir listeyi gösteren sayfalar, birkaç nedenden dolayı daha büyük görünüm seçicisine sahip olacaktır. En önemlisi, daha büyük görünüm seçicisi, kullanıcı tanımlı filtreleri içerebilen sayfaları belirtir. Filtreler görünümlerde yer aldığından, görünüm adları ekranda gösterilen verilerin en iyi açıklaması olacağı ve beklentilerin kullanıcıların Bu sayfa türlerinde daha sık geçiş yapma işlemi olacağı için büyük seçici boyutuna da izin verilir.  
 
-   **Küçük görünüm seçicileri**: Diğer tüm tam sayfa formları (çalışma alanları ve gösterge tablosu hariç), sayfa başlığının yanında görünen daha küçük bir görünüm seçicisine sahiptir. Bu sayfalardaki görünümler yalnızca kişiselleştirmeler içerir (kullanıcı tanımlı filtreler değil). Bu sayfalarda form başlığı veya kayıt başlığı genellikle formun üst kısmındaki en önemli bilgiler olur. Daha küçük boyut ayrıca, bu sayfalarda daha düşük olan görüntüleme geçişi sıklığını da yansıtır. 
 
Görünüm adını tıklatırsanız, görünüm seçicisi açılır ve bu sayfayla ilgili kullanılabilir görünümlerin listesini gösterir

-    **Klasik Görünüm**: klasik görünüm açık bir kişiselleştirmeler uygulanmamış olan sayfanın kutudan çıkış görünümden yer alır.  
-    **Kişisel görünümler**: Asma kilitleri olmayan görünümler kişisel görünümlerinizi temsil eder. Bunlar, oluşturduğunuz veya bir yöneticinin size verdiği görünümlerdir.  
-    **Kilitli Görünümler**: bazı görünümlerde (Classic görünümü ve rolünüzde yayınlanan tüm görünümler), görünüm seçicide sonra bu görünümleri düzenleyemeyeceğinizi belirten bazı görünümler için bir asma kilidi vardır. Ancak, örtülü kişiselleştirmeleri yansıtan otomatik olarak kaydedilir (örneğin, bir ızgara sütununun genişliğini değiştirmek veya bir hızlı sekmeyi genişletmek veya daraltmak). Ancak kişiselleştirme ayrıcalıklarınız varsa, **Kopyasını kaydet** eylemini kullanarak kilitli bir görünümü temel alan kişisel bir görünüm de yapabilirsiniz.
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
     1.    **Bir kopyasını kaydet**'i seçin. 
     2.    Bir görünüm adı ve (isteğe bağlı olarak) bir açıklama girin.
     3.    **Kaydet**'i seçin.

## <a name="changing-the-default-view"></a>Varsayılan görünümü değiştirmek
Varsayılan görünüm, sayfaya ilk gittiğinizde sistemin açmaya çalışacağı görünümdür. Bunu en sık olarak kullanmayı beklediğiniz görünüme ayarlamalısınız.  

Bir sayfa için varsayılan görünümü değiştirmek için şu adımları izleyin: 
1.  Varsayılan olarak kullandığınız görünüme geçin. 
2.  Görünüm seçiciyi açmak için görünüm adını seçin. 
3.  **Daha fazla** ve **Varsayılan olarak sabitle**'yi seçin.  

Alternatif olarak, yeni bir görünüm oluştururken (**Kopyasını kaydet** eylemini kullanarak), görünümü kaydetmeden önce, **Varsayılan olarak sabitle** olarak ayarlayarak yeni görünümü varsayılan görünüm haline getirebilirsiniz.  

Bazı durumlarda, bir sayfaya ilk gittiğinizde varsayılan görünümle ilişkilendirilmiş sorgunun yürütülmeyeceğini unutmayın. Örneğin, bir sayfaya bir kutucukta gezindiğinizde, döşemedeki sorgu, varsayılan görünümle ilişkilendirilmiş sorgudan bağımsız olarak yürütülür. Ayrıca, klasik görünümünde tanımlı bir sorguya sahip olan bir sayfaya giderseniz, özgün sorgu başlangıçta varsayılan görünümün sorgusunun yerine yürütülür. Bu durumda, görünüm yüklenirken bir bilgi iletisi ile uyarı alırsınız. Sayfa yüklendikten sonra görünümlerin değiştirilmesi, görünüm sorgusunun beklendiği gibi yürütülmelerine olanak sağlar.

## <a name="managing-personal-views"></a>Kişisel görünümleri yönetme 
**Görünümlerimi Yönet** iletişim kutusu, kişisel görünümleriniz ve görünüm seçicisindeki görünümlerin sırası üzerinde temel bakım olanakları sağlar. Bu sayfayı açmak için görünüm seçiciyi açılır menüsünü açmak üzere görünüm adını tıklatın, **Diğer**'i seçin ve sonra **Görünümlerimi Yönet**'i seçin.  

Bu sayfayla ilgili kullanılabilir görünümlerin listesi için aşağıdaki eylemler kümesi kullanılabilir.  
-    **Varsayılan görünümü değiştir**: **Varsayılan olarak sabitle** eylemini geçerli vurgulanmış görünümü bu sayfa için varsayılan görünüm yapmak üzere kullanın.  
-    **Görünümlerinizi yeniden sıralayın**: Görünümlerinizi belirli bir sırada yeniden düzenlemek için **Yukarı taşı** ve **Aşağı taşı** eylemlerini kullanın.  
-    **Görünümüyeniden adlandırın**: Vurgulanmış olan kişisel görünümün adını değiştirmek için **Yeniden Adlandır** eylemini kullanın. Bu eylem kilitli görünümler için kapatılmıştır. 
-    **Görünümü sil**: Geçerli olarak vurgulanmış görünümü sayfadan kalıcı olarak silmek için **Kaldır** eylemini kullanın. Bir görünümü kaldırdıktan sonra kurtarmanın bir yolu yoktur.  

Bu iletişim kutusunda yapılan tüm değişiklikler **Kaydet** düğmesini seçtikten sonra etkinleşir.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Organizasyon düzeyindeki kişiselleştirmeleri görünümleriyle yönetmek
Bir organizasyon düzeyinde kişiselleştirmeleri yönetmenin gelişmelerini anlamak için önce kişiselleştirme yönetiminin nasıl çalıştığı hakkında görünümlerden önce bakalım.  

Görünümler olmadan, yöneticiler bir sayfaya, bir kullanıcı grubuna veya kişiselleştirme sayfasını kullanan kullanıcılara sayfa için bir kişisel ayarlar uygular. Bu kullanıcılar kişiselleştirme haklarına sahip ise, kişiselleştirmeler o sayfaya uygulanır. Ancak, kullanıcıların sayfayı daha fazla kişiselleştirmesinin önleneceği ve böylece kuruluş, kullanıcıların tutarlı bir kullanıcı arabirimine sahip olmasını gerektirmediğinden emin olunmamıştır. Bu kullanıcıların kişiselleştirme hakları yoksa, bir yönetici tarafından kendilerine verilen kişiselleştirmeler yüklenmemiştir. Dahası, yeni kullanıcılar bir kuruluşta işe alındığında, yöneticiler kullanıcı için kişiselleştirmeler kümesini el ile yüklemek zorunda kalmaktadır. O roldeki kullanıcılar tarafından kullanılabilecek belirli bir kişisel belirleme kümesini belirtmek için otomatik bir mekanizma yoktur.

Kaydedilmiş görünümler özelliğiyle, öncelikle görünümlerin güvenlik rollerine yayımlanması nedeniyle, kişiselleştirmeler için organizasyon yönetimi önemli ölçüde daha kolaydır. Bir görünüm yayımlandıktan sonra, bu da ilgili role sahip tüm kullanıcıların, kullanıcının kişiselleştirme yeteneğine bakmaksızın o görünüme erişebilir ve kullanılabilir olacağı anlamına gelir. Her kullanıcının, sayfa kullanımı (örtük kişiselleştirmeler) otomatik olarak uygulandığı yayımlanmış görünümün bir kopyası varken, hiçbir kullanıcı sorguya açık kişiselleştirme veya güncelleştirme (yayınlanan görünümlerin kilitli olduğu anlamına gelir) kaydedemez. Ek olarak, yeni kullanıcılara görünümün yayımlandığı bir rol verilirse, yöneticiden herhangi bir eylemde bulunmadan ilişkili görünümleri otomatik olarak görürler. Benzer şekilde, bir kullanıcı kuruluştaki rolleri değiştirirse, eski rolleriyle ilişkilendirilmiş görünümlere artık bunlar için yönetici tarafından herhangi bir eylem yapılmadan erişilemez. Yayımlanmış bir görünüme yapılan güncelleştirmeler, görünümü uygun güvenlik rollerine yeniden yayımlayarak kullanıcılara kolayca dağıtılabilir.

Bu yayımlama yeteneği, kuruluşların işletmeler için belirli güvenlik rollerindeki kullanıcıları hedeflemiş olarak en iyi duruma getirilmiş şirket standart görünümlerini tanımlamasına olanak tanır.  

## <a name="publishing-views"></a>Yayımlama görünümleri
Yayımlama işlemi sırasında, görünümler bir veya daha fazla güvenlik rolüne atanabilir, başka bir deyişle, söz konusu role sahip olan tüm kullanıcılar o görünüme erişebilir ve kullanılabilir, ancak görünümü düzenleyemezler. Şu anda yalnızca sistem yöneticilerinin, görünüm Seçici açılır menüsünde **Yayımla** eylemi için hakları vardır, ancak diğer güvenilen kullanıcılara yayımlama hakları vermek için gelecekteki bir güncelleştirmede yeni bir güvenlik rolü kullanılabilir.  

Bir görünümü yayımlamak için şu adımları izleyin: 
1.  Yayımlamak istediğiniz görünümün kişisel bir kopyasını oluşturun ve kaydedin. 
2.  Şu anda yüklü olan görünümle, görünüm adını, görünüm seçici açılır menüsünü açmak için seçin. 
3.  **Diğer** düğmesini ve ardından **Yayımla**'yı seçin. Yayınla iletişim kutusu açılır.  
4.  Görünüm için bir ad ve (isteğe bağlı olarak) bir açıklama girin. Bu, görünümü alan kullanıcıların görünüm seçicileri içinde görebilmeleri için kullanılan addır. Uygulandığı roller listesi farklılık gösterdiğinden bile, sayfa için yayımlanmış görünümlere yinelenen adlara izin verilmediğini unutmayın.  
5.  Bu görünümü alacak kullanıcılara karşılık gelen güvenlik rollerini ekleyin.  
6.  **Yayımla**'yı seçin.

Bazı ortamlarda, kullanıcılar yayımlanan görünümü görebilmeleri için biraz zaman (bir saat kadar) sürebilir.

## <a name="modifying-a-published-view"></a>Yayınlanmış görünümü değiştirme
Bir görünümü yayımladıktan sonra, yayınlanmış bir görünümde değişiklik yapmak istediğinizi fark edebilirsiniz. Yayımlanmış bir görünümde canlı değişiklikler yapamazsınız, ancak bu görünümler tüm kullanıcılar için (yayımcılar dahil) düzenlemeye karşı kilitlenmiş olduğundan, güncelleştirme yapmak için bir görünümü yeniden yayımlayabilirsiniz.  

Yayınlanmış bir görünümde yapmak istediğiniz değişiklikler yalnızca yayımlama parametreleri (görünümün adı ve açıklaması veya görünümün yayımlandığı güvenlik rolü) içeriyorsa, aşağıdakileri yapın: 
1.  Güncelleştirmek istediğiniz parametreler için yayımlanmış görünüme geçin. 
2.  Görünüm seçici açılır menüsünden **Yayımla**'yı seçin. 
3.  Varolan görünümü güncelleştirmek istiyorsanız **Evet**'i seçin (farklı bir ad altında yayımlamak istiyorsanız **Hayır**'ı seçin).
4.  Görünüm için ad, açıklama ve/veya güvenlik rollerini güncelleştirin. 
5.  **Yayımla**'yı seçin. 
6.  Yayınlanan görünümün adını güncelleştirdikten sonra, yayımlanmış görünümü eski adıyla da silmeniz gerekecektir (daha ayrıntılı bilgi için **Yayınlanmış görünümleri yönetme** bölümüne bakın). 

Yayınlanan görünümde yapılan değişiklikler görünümle ilişkili kişiselleştirmeler veya filtrelerle değişiklik yapmak içeriyorsa, şu adımları izleyin: 
1.  Değiştirmek istediğiniz yayımlanmış görünüme geçin. 
2.  Yayımlanmış görünümün yerel taslağını oluşturmak için yayımlanmış görünümün bir kopyasını kaydedin. 
3.  Yerel taslağı gerekli değişikliklerle değiştirin.
4.  Görünümü özgün adıyla yayımlayın. 

## <a name="managing-published-views"></a>Yayımlanmış görünümleri yönetme
Kişisel görünümleri yönetmek gibi, **Görünümlerimi yönet** iletişim kutusu, yayımlama ayrıcalıklarına sahip kullanıcılara, yayımlanmış görünümler içeren bir sayfa üzerinde temel bakım yeterlilikleri sağlar (kendi kişisel görünümlerine ek olarak). Bu sayfayı açmak için görünüm seçiciyi açılır menüsünü açmak üzere görünüm adını tıklatın, **Diğer**'i seçin ve sonra **Görünümlerimi Yönet**'i seçin.

Tüm kullanıcılar kişisel görünümlerini gösteren **Görünümlerim** sekmesini görürken, yayımlama ayrıcalığına sahip kullanıcılar, o sayfa için yayımlanan tüm görünümleri gösteren **Yayımlanmış** bir sekmesi de görür. Birçok kullanıcı yayımlama görünümü olabileceği için, görünümü gerçekten yayımlamış olan kullanıcı olup olmadığına bakılmaksızın, yayımlanmış görünümlerin tam listesini yönetmeniz önemlidir.

Sayfa için tüm yayımlanmış görünümlerin listesi için aşağıdaki eylem kümesi kullanılabilir. 

-    **Yayınla**: Değiştirilmiş yayımlama parametreleriyle bir görünümü yeniden yayımlamak için **Yayımla** eylemini kullanın (ad, açıklama, güvenlik rolleri).  
-    **Kaldır**: Yayınlanmış bir görünümü kalıcı olarak silmek için **Kaldır** eylemini kullanın. Bu eylem sistemdeki tüm kullanıcıların görünümünü kaldırır.  
 
Bu iletişim kutusunda yapılan tüm değişiklikler **Kaydet** düğmesini seçtikten sonra etkinleşir.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kaydedilmiş görünümleri ortamımda nasıl etkinleştirebilirim? 
Özellik önizlemede olduğunda kaydedilmiş görünümleri etkinleştirmek için aşağıdaki adımları izleyin: 

1.  **Uçuşu etkinleştirin**: Aşağıdaki SQL beyanını yürütün: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. Statik deneme sürümü önbelleğini temizlemesi için **IIS'yi Sıfırla**'yın. 

3.  **Özelliği bulun**: **Özellik Yönetimi** çalışma alanına gidin. **Kaydedilmiş görünümler** listede görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.   

4.  **Özelliği etkinleştirin**: **Özellikler listesinde kaydedilmiş görünümler** özelliğini bulun ve Ayrıntılar bölmesindeki **Şimdi etkinleştir**'i seçin.

Sonraki tüm kullanıcı oturumları kaydedilmiş görünümleri etkin olarak başlayacaktır.  

Ortam için kişiselleştirme kapatılmışsa, yukarıdaki adımları izleseniz bile görünümler devre dışı bırakılır. Bunun nedeni, görünümler özelliğinin kişiselleştirme alt sisteminin üzerine kurulmuş olmasıdır.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Görünümler etkinleştirildiğinde varolan kişiselleştirmeler ne olur? 
Görünümler etkinleştirildiğinde, bir Kullanıcı ve form için varolan tüm kişiselleştirmeler, varsayılan görünüm olarak otomatik olarak ayarlanan **Görünümlerim** denen yeni bir görünüme kaydedilir. Bu, formlarda görünüm Seçicisi denetiminin görünmesi dışında, görünümler etkinleştirilmeden önce ve sonra tutarlı bir kullanıcı deneyimi olmasını sağlamak içindir.  

### <a name="what-pages-support-views"></a>Hangi sayfalar görünümleri destekler? 
Görünümler, Finance and Operations ilgili sayfaların tümünde değil, ama pek çoğunda bulunabilir. Özellikle, görünümler şu anda panolar ve çalışma alanları dışındaki tüm tam ekran sayfalarda kullanılabilirdir. İletişim kutuları, açılan diyaloglar, aramalar ve gelişmiş önizlemeler içeren tam ekran olmayan sayfalar da şu anda görünümleri desteklememektedir. Çalışma alanları ve iletişim kutuları gibi ek sayfa türleri için görüntüleme desteği gelecekteki bir güncelleştirmeyle ilgili olarak değerlendirilebilir.   

### <a name="who-is-allowed-to-publish-views"></a>Görünüm yayımlamaya kimlerin izni vardır?
Şu an sistem yöneticileri yalnızca görünümleri yayımlama hakları olan kullanıcılardır.  Gelecekteki bir güncelleştirmede müşterilere kimlerin yayımlayabileceği daha fazla esneklik sağlayan yeni bir güvenlik rolü planlanmıştır.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Bu görünüme ilişkin filtreleri niçin kaydedemiyorum? 
Bir filtrenin görünüm ile kaydedilmeye neden görünmeyebileceği birkaç neden vardır: 

- Sayfa, görünüm tanımının bir parçası olarak filtre kaydetmeyi desteklemiyor olabilir. Yalnızca büyük görünüm seçicileri olan sayfaların, kişiselleştirmeler ve sorgu değişikliklerinin görünüm olarak kaydedilmesine izin vermesi gerektiğini unutmayın. Daha fazla bilgi için "Görünümleri değiştirme" bölümüne bakın. 

- Görünüm varsayılan görünüm ise ve sayfanın gezinti yolu bir sorgu içeriyorsa, görünümün sorgusu başlangıçta uygulanmayabilir. Bunun için iki birincil senaryo vardır: 
     - Bir sayfaya bir kutucukta gezindiğinizde, döşemedeki sorgu, varsayılan görünümle ilişkilendirilmiş sorgudan bağımsız olarak yürütülür. 
     - Bir sayfaya giderseniz ve bu giriş noktası bir sorguya sahipse, özgün sorgu başlangıçta varsayılan görünümün sorgusunun yerine yürütülür. 
     
  Bu durumlar gerçekleştiğinde, görünüm yüklenirken bir ek bilgilendirici mesaj ile uyarılacaksınız. Ayrıca, sayfa yüklendikten sonra bu görünüme geçerek, görünüm sorgusunun ne olursa olsun yürütülmesine izin vermek istiyorsanız da onay alabilirsiniz.  

- Söz konusu sayfa, görünüm sorgusunu tamamen görmezden gelebileceği veya verileri kalıcı olmayan geçici bir tabloda çalışabileceği için görünümleri doğru şekilde desteklemeyebilir. 
