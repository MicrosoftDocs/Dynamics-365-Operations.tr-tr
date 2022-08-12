---
title: Kayıtlı görünümler
description: Bu makale, kaydedilmiş görünümler özelliklerinin nasıl kullanılacağını açıklar.
author: jasongre
ms.date: 04/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 14369b02f1d7553be5c732f3bdf768825267998b
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2022
ms.locfileid: "9125165"
---
# <a name="saved-views"></a>Kayıtlı görünümler

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

## <a name="introduction"></a>Giriş

Kişiselleştirme, kullanıcıların ve kuruluşların gereksinimlerine uygun Kullanıcı deneyimini en iyi duruma getirmesine izin verirken önemli bir rol oynar. Kişiselleştirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

Geleneksel kişiselleştirme, kullanıcıların her form için sayfa başına yalnızca tek bir kişiselleştirme kümesi olmasına izin verir. **Kaydedilmiş görünümler** özelliği, birçok önemli yolla kişiselleştirmede genişletir:

- Görünümler, kullanıcıların form başına birden çok adlandırılmış kişisel grup kümesine sahip olmasını ve bunlar arasında hızla geçiş yapabilmelerini sağlar. Bu, kullanıcının belirli bir iş görevi yerine getirmek üzere her bir görünüm için tasarlanmış birden çok iyileştirilmiş görünüm oluşturmasını sağlar. 
- Belirli sayfa türleri için oluşturulan görünümler, kullanıcı tarafından eklenmiş filtreler ve sıralamalar da içerebilir, bunlar da kullanıcıların yaygın olarak filtrelenen veri kümelerine hızlıca dönmesine olanak sağlar. Daha fazla ayrıntı için [Hangi sayfalar görünümleri destekler](saved-views.md#what-pages-support-views) bölümüne göz atın. 
- Görünümler, belirli güvenlik rollerindeki ve belirli tüzel kişiliklerdeki kullanıcılara yayımlanabilir. Bu nedenle, belirli bir tüzel kişilite belirtilen role ve erişime sahip herhangi bir kullanıcı, söz konusu kullanıcı bunu kişiselleştirme iznine sahip olmaması durumunda bile o görünüme erişebilir ve bu görünümü kullanabilir. Bu yayımlama yeteneği, kuruluşların işletmeler için en iyi duruma getirilmiş şirket standart görünümlerini tanımlamasına olanak tanır. Daha fazla bilgi için bkz. [Kişiselleştirmeleri görünümler ile kuruluş düzeyinde yönetmek](saved-views.md#managing-personalizations-at-an-organizational-level-with-views)
- Geleneksel kişiselleştirmenin aksine, bir kullanıcı kişiselleştirmeler gerçekleştirdiğinde veya bir listeye filtre uyguladığında görünümler otomatik olarak kaydedilmez. Kullanıcılara, o görünümle ilişkilendirilmiş değişikliklerden önce veya sonra bir görünüm oluşturma esnekliği sağlamak için açık kaydetme gereklidir. Bu gereksinim ayrıca görünüm tanımlarının uzun vadeli kullanım amaçlı olmayan filtreler veya kişiselleştirmeler tarafından istenmeden değiştirilmesini de sağlar. Sistemin normal sayfa kullanımının bir parçası olarak (örneğin, sütun genişlikleri veya bölümlerin genişletilmiş veya daraltılmış durumu) otomatik olarak depoladığı kalemler her bir görünüm için kaydedilir.
- Görünümler, çalışma alanlarına kutucuk, liste veya bağlantı olarak eklenebilir. Bu nedenle, filtrelenmiş bir veri kümesi bir çalışma alanında görüntülenebilir ve kullanıcılar, o veri kümesiyle ilgili bir dizi kişiselleştirme kümesini kutucuk veya bağlantıyla ilişkilendirebilir.

## <a name="switching-between-views"></a>Görünümler arasında geçiş yapma

Görünümler bir ortam için kullanılabilir hale getirildikten sonra, görünümleri destekleyen herhangi bir sayfanın en üstüne, geçerli görünümün adını gösteren daraltılmış bir görünüm seçicisi denetimi içerir.

Görünüm seçicisinde iki boyut varyasyonu vardır: 

- **Büyük görünüm seçicileri**: Bir listeyi gösteren sayfalar, birkaç nedenden dolayı daha büyük görünüm seçicisine sahip olacaktır. En önemlisi, daha büyük görünüm seçicisi, kullanıcı tanımlı filtreleri ve sıralamaları içerebilen sayfaları belirtir. Filtreler ve sıralamalar görünümlerde yer aldığından, görünüm adları ekranda gösterilen verilerin en iyi açıklaması olacağı ve beklentilerin kullanıcıların Bu sayfa türlerinde daha sık geçiş yapma işlemi olacağı için büyük seçici boyutuna da izin verilir. Kılavuzdaki gruplandırma, büyük görünüm seçicileri bulunan bir sayfadaki görünümlere de kaydedilebilir. 
- **Küçük görünüm seçicileri**: Diğer tüm tam ekran sayfaları (çalışma alanları ve pano hariç), sayfa başlığının yanında görünen daha küçük bir görünüm seçicisine sahiptir. Bu sayfalardaki görünümler, kullanıcı tanımlı filtreleri değil, yalnızca kişiselleştirmeler içerir. Bu sayfalarda form başlığı veya kayıt başlığı genellikle sayfanın üst kısmındaki en önemli bilgiler olur. Daha küçük boyuttaki görünüm seçici ayrıca, bu sayfalarda beklenen daha düşük görüntüleme geçişi sıklığını da yansıtır. 
 
Görünüm adını seçerseniz görünüm seçicisi açılır ve bu sayfayla ilgili kullanılabilir görünümlerin listesini gösterir.

**Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde görünüm seçici, kullanılabilir görünümleri iki bölümde gösterir. İlk bölüm, mevcut tüzel kişiliğe özgü tüm görünümleri gösterir ve ikinci bölüm, tüm tüzel kişilikler tarafından kullanılabilen görünümleri gösterir. İlk bölüm, yalnızca sayfa için tüzel kişiliğe özel görünümler varsa görünür.

- **Standart görünüm**: **Standart** görünüm kişiselleştirme uygulanmamış olan sayfanın kutudan çıkış görünümden yer alır.
- **Kişisel görünümler**: Asma kilitleri olmayan görünümler kişisel görünümlerinizi temsil eder. Bunlar, oluşturduğunuz veya bir yöneticinin size verdiği görünümlerdir.
- **Kilitli görünümler**: Bazı görünümlerde ( **Standart** görünüm ve rolünüze yayımlanmış görünümler gibi), görünüm seçicide görünümün yanında bir asma kilit simgesi bulunur. Bu simge, bu görünümleri düzenleyemeyeceğinizi belirtir. Ancak, sayfa kullanımını yansıtan değişiklikler otomatik olarak kaydedilir. Bu değişiklikler kılavuz sütununun genişliğinde değişiklikler ve bir hızlı sekmenin genişletilmiş ya da daraltılmış durumunda yapılan değişiklikler içerir. Ancak kişiselleştirme ayrıcalıklarınız varsa, **Farklı kaydet** eylemini kullanarak kilitli bir görünümü temel alan kişisel bir görünüm de yapabilirsiniz.
- **Yeni görünümler**: Henüz açılmamış yayımlanmış görünümlerde, görünüm adının solunda bir alev sembolü bulunur.

Farklı bir görünüme geçmek için önce görünüm seçicisini açın ve sonra yüklemek istediğiniz görünümü seçin. 

## <a name="creating-and-modifying-views"></a>Görünüm oluşturma ve değiştirme

Geleneksel kişiselleştirmenin aksine, bir kullanıcı sayfayı kişiselleştirdiğinde veya bir kullanıcı bir listeye filtre uyguladığında veya listeyi sıraladığında, görünümler otomatik olarak kaydedilmez. Bu değişiklikleri bir görünüme kaydetmek için açık bir eylem gerekli. Bu gereklilik kullanıcılara, o görünümle ilişkilendirilmiş değişikliklerden önce veya sonra bir görünüm oluşturma esnekliği sağlar. Ayrıca, görünüm tanımlarının tek seferlik filtreler veya kişiselleştirmeler tarafından istem dışı olarak değiştirilmemesini de sağlar. Tipik sayfa kullanımı kalemlerinin (örneğin, sütun genişlikleri veya bölümlerin genişletilmiş veya daraltılmış durumu), kilitli görünümlerde bile otomatik olarak geçerli görünüme kaydedildiğini unutmayın.

Görünümün geçerli durumunun bilindiğinden emin olmak için bir görünümü kişiselleştirerek veya filtreleyerek değiştirmeye başladığınızda, geçerli görünüm adının yanında bir yıldız işareti (\*) görünür. Bu sembol, o görünümün kaydedilmemiş, değiştirilmiş olduğunu gösterir.

Bu değişiklikleri kaydetmek istiyorsanız, aşağıdaki adımları izleyin.

1. Görünüm seçiciyi açmak için görünüm adını seçin.
2. Varolan görünümü değiştirmek için **Kaydet**'i seçin. Bu eylemin kilitli görünümler için kullanılabilir olmadığını unutmayın. 
3. Yeni bir görünüm oluşturmak için:

    1. **Farklı kaydet**'i seçin. 
    2. **Görünümü farklı kaydet** bölmesinde, görünüm için bir ad ve isteğe bağlı olarak bir açıklama girin.
    3. Bu görünümün varsayılan görünümünüz olmasını istiyorsanız **Varsayılan olarak sabitle**'yi seçin. Varsayılan görünümler hakkında daha fazla bilgi için bir sonraki [Varsayılan görünümü değiştirme](#changing-the-default-view) bölümüne bakın. 
    4. **Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde bu görünümün tüm tüzel kişilikler için mi yoksa yalnızca tüzel kişiliklerin bir alt kümesi için mi kullanılabilir olmasını istediğinizi seçebilirsiniz.
    5. **Kaydet**'i seçin.

## <a name="changing-the-default-view"></a>Varsayılan görünümü değiştirmek

Varsayılan görünüm, sayfayı ilk açtığınızda sistemin açmaya çalışacağı görünümdür. Varsayılan görünümü en sık olarak kullanmayı beklediğiniz görünüme ayarlamalısınız. 

> [!NOTE]
> - Temel **Kayıtlı görünümler** özelliğinde, tüzel kişilikler için tek bir genel varsayılan görünüm vardır. Varsayılan görünümü değiştirirseniz, o anda içinde bulunduğunuz tüzel kişilik ne olursa olsun, o görünüm varsayılan olarak açılır.
> - **Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde her tüzel kişilik, sayfa başına kendi varsayılan görünümüne sahip olabilir.

Bir sayfa için varsayılan görünümü değiştirmek için şu adımları izleyin:

1. Varsayılan olarak kullandığınız görünüme geçin. 
2. Görünüm seçiciyi açmak için görünüm adını seçin. 
3. **Daha fazla** ve **Varsayılan olarak sabitle**'yi seçin.

Alternatif olarak, yeni bir görünüm oluştururken (**Farklı kaydet** eylemini kullanarak), görünümü kaydetmeden önce, **Varsayılan olarak sabitle** olarak ayarlayarak yeni görünümü varsayılan görünüm haline getirebilirsiniz.

> [!WARNING]
> Bazı durumlarda, bir sayfayı ilk kez açtığınızda varsayılan görünümle ilişkilendirilmiş sorgu çalışmaz. Örneğin, bir sayfayı bir kutucuk üzerinden açarsanız, kutucuktaki sorgu, varsayılan görünümle ilişkilendirilmiş sorgudan bağımsız olarak çalıştırılır. Ayrıca tanımlı bir sorguya sahip **standart** görünümlü bir sayfayı açarsanız varsayılan görünümün sorgusunun yerine özgün sorgu çalıştırılır. Bu durumda, görünüm yüklendiğinde bir bilgi iletisi alacaksınız. Sayfa yüklendikten sonra görünümler arasında geçiş yaptığınızda, görünüm sorgusu beklendiği gibi çalışamaz. Sürüm 10.0.10 ve sonrasında, aldığınız bilgi iletisi varsayılan görünümün sorgusunu doğrudan yükleme olanağı sağlayan katıştırılmış bir eyleme sahip olacaktır.

## <a name="managing-personal-views"></a>Kişisel görünümleri yönetme

**Görünümlerimi Yönet** iletişim kutusu, kişisel görünümleriniz ve görünüm seçicisindeki görünümlerin sırası üzerinde temel bakım olanakları sağlar. Bu sayfayı açmak için görünüm seçiciyi açılır menüsünü açmak üzere görünüm adını tıklatın, **Diğer**'i seçin ve sonra **Görünümlerimi Yönet**'i seçin.

**Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde **Görünümlerimi yönet** iletişim kutusunun **Görünümlerim** bölümü, sayfa için mevcut görünümleri bölümler halinde gösterir. Mevcut tüzel kişiliğe özel görünümler kendi bölümlerinde gösterilir. **Genel görünümler** bölümü her zaman gösterilir, böylece tüm tüzel kişiliklerde sayfa için mevcut olan görünümleri yönetebilirsiniz. 

Bu sayfayla ilgili kullanılabilir görünümlerin listesi için aşağıdaki eylemler kümesi kullanılabilir.

- **Varsayılan görünümü değiştir**: **Varsayılan olarak sabitle** eylemini geçerli seçilmiş görünümü bu sayfa için varsayılan görünüm yapmak üzere kullanın. **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde **Genel görünümler** bölümü, geçerli tüzel kişilik veya tüm tüzel kişilikler için bir görünümü varsayılan görünüm yapmanıza olanak tanır.
- **Görünümlerinizi yeniden sıralayın**: Görünümlerinizi belirli bir sırada yeniden düzenlemek için **Yukarı taşı** ve **Aşağı taşı** eylemlerini kullanın.
- **Görünümüyeniden adlandırın**: Seçilmiş olan kişisel görünümün adını değiştirmek için **Yeniden Adlandır** eylemini kullanın. Bu eylem kilitli görünümler için kapatılmıştır. 
- **Görünümü sil**: Geçerli olarak seçilmiş görünümü sayfadan kalıcı olarak silmek için **Sil** eylemini kullanın. Bir görünümü kaldırdıktan sonra kurtarmanın bir yolu yoktur.

Bu iletişim kutusunda yapılan tüm değişiklikler **Güncelleştir** düğmesini seçtikten sonra etkinleşir.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Organizasyon düzeyindeki kişiselleştirmeleri görünümleriyle yönetmek

Kaydedilmiş görünümlerin kuruluş düzeyinde kişiselleştirmenin yönetimini geliştirmeye nasıl yardımcı olduğunu anlamanıza yardımcı olması için bu bölümde kişiselleştirme yönetiminin, **Kaydedilmiş görünümler** özelliği olmadan önce nasıl çalıştığı açıklanmaktadır.

Görünümler olmadan, yöneticiler bir sayfaya, bir kullanıcı grubuna veya kişiselleştirme sayfasını kullanan kullanıcılara sayfa için bir kişisel ayarlar uygular. Bu kullanıcılar kişiselleştirme haklarına sahip ise, kişiselleştirmeler o sayfaya uygulanır. Ancak, kullanıcıların sayfayı daha fazla kişiselleştirmesinin önleneceği ve böylece kuruluş, kullanıcıların tutarlı bir kullanıcı arabirimine sahip olmasını gerektirmediğinden emin olunmamıştır. Bu kullanıcıların kişiselleştirme hakları yoksa, bir yönetici tarafından kendilerine verilen kişiselleştirmeler yüklenmemiştir. Dahası, yeni kullanıcılar bir kuruluşta işe alındığında, yöneticiler kullanıcı için kişiselleştirmeler kümesini el ile yüklemek zorunda kalmaktadır. O roldeki kullanıcılar tarafından kullanılabilecek belirli bir kişisel belirleme kümesini belirtmek için otomatik bir mekanizma yoktur.

**Kaydedilmiş görünümler** özelliği, öncelikle görünümlerin kullanıcı gruplarına yayımlanabilmesi nedeniyle, kişiselleştirmelerin için kuruluş düzeyinde yönetimini önemli ölçüde kolaylaştırır. Bir görünüm yayımlandıktan sonra tanımlı güvenlik rollerinden birine sahip olan ve belirtilen tüzel kişiliklerde bulunan tüm kullanıcılar, kullanıcının kişiselleştirilme erişimi olmasa bile, görünüm gösterilebilir ve kullanılabilir. Her kullanıcının, sayfa kullanımı öğeleri otomatik olarak uygulandığı yayımlanmış görünümün bir kopyası olmasına karşın, hiçbir kullanıcı yayımlanmış bir görünüme kişiselleştirme veya sorgu güncelleştirmeleri kaydedemez. Başka bir deyişle, yayınlanan görünümler kilitlenir. Ek olarak, yeni kullanıcılara görünümlerin yayımlandığı tüzel kişilikler içinde roller atanırsa, rolleri ve tüzel kişilikler ile ilişkili görünümleri otomatik olarak görürler. Yönetici tarafından başka bir eyleme gerek yoktur. Benzer şekilde, kullanıcılar bir kuruluştaki rolleri değiştirdiklerinde veya farklı tüzel kişiliklere erişim verildiğinde, kendileri için daha önce yayınlanmış görünümlere artık erişemeyebilirler. Yine, yönetici tarafından başka bir eyleme gerek yoktur.

Yayımlanmış bir görünüme yapılan güncelleştirmeler, görünümü uygun güvenlik rollerine ve tüzel kişiliklere yeniden yayımlayarak kullanıcılara kolayca dağıtılabilir.

Bu yayımlama yeteneği, kuruluşların işletmeler için belirli güvenlik rollerindeki kullanıcıları hedeflemiş olarak en iyi duruma getirilmiş şirket standart görünümlerini tanımlamasına olanak tanır.

## <a name="publishing-views"></a>Yayımlama görünümleri

Yayımlama işlemi sırasında, görünümler bir veya daha fazla tüzel kişilik için bir veya daha fazla güvenlik rolüne atanabilir. Bu nedenle, bir tüzel kişiliğe erişimi olan ve bu rollerden birine atanan tüm kullanıcılar, görünümlere erişebilir ve bunları kullanabilirler. Ancak kullanıcı, görünümleri düzenleyemez. Varsayılan olarak, sistem yöneticilerinin görünüm seçicisi açılır menüsünde bulunan **Yayımla** eylemine erişimi vardır. Bununla birlikte, kuruluştaki diğer güvenilen kullanıcılara da, yeni **Kaydedilmiş görünümler yöneticisi** rolü aracılığıyla görünüm yayımlamasına erişim izni verilebilir.

Bir görünümü yayımlamak için şu adımları izleyin:

1. Yayımlamak istediğiniz görünümün kişisel bir kopyasını oluşturun ve kaydedin. 
2. Şu anda yüklü olan görünümle, görünüm adını, görünüm seçici açılır menüsünü açmak için seçin. 
3. **Diğer** düğmesini ve ardından **Yayımla**'yı seçin. Yayınla iletişim kutusu açılır.
4. Görünümün adını girin. Girdiğiniz ad, görünümü alan kullanıcıların görünüm seçicileri içinde görebilmeleri için kullanılan addır. Bir sayfayla ilgili yayımlanmış görünümlerin adları benzersiz olmalıdır. Görünümlerin uygulandığı roller listesi veya tüzel kişilikler farklılık gösterse bile yinelenen adlara izin verilmez.
5. **10.0.17 ve sonraki güncelleştirmeler:** **(Önizleme) Kuruluş görünümleri için çeviri desteği** özelliği açıksa, **Ad** alanının yanındaki **Çeviriler** düğmesini seçerek görünüm adı için kuruluşunuzda gerekli olan dil kadar çeviri ekleyebilirsinzi. Ardından görünüm adı kullanıcılara geçerli dillerinde gösterilir. Çeviri tanımlanmayan dilleri çalıştıran kullanıcılara gösterilecek çeviriyi belirtmek için varsayılan dili de ayarlayabilirsiniz.
5. İsteğe bağlı: Görünüm için bir açıklama girin; böylece bu görünümü alan kullanıcılar amacını daha iyi anlayabilir. 
6. Görünümün, seçilen kullanıcılar için varsayılan görünüm olarak yayımlanıp yayımlanmayacağını belirleyin. Bir görünüm varsayılan olarak ayarlandığında, bu görünüm, kullanıcıların hedef sayfayı bir sonraki açtıklarında görecekleri görünüm olur. Hedeflenen her kullanıcının tek, genel varsayılan görünümü değiştirilir. Ancak, yayımlama gerçekleştirildikten sonra kullanıcılar varsayılan görünümlerini değiştirmeye devam edebilir.

    > [!NOTE]
    > Görünümü varsayılan görünüm olarak yayımladığınızda aşağıdaki davranışa dikkat edin:
    >
    > - Görünümü tüzel kişiliklerin bazılarına veya tümüne varsayılan görünüm olarak yayımladığınızda aşağıdaki davranış gerçekleşir:
    >
    >    - Yalnızca temel **Kayıtlı görünümler** özelliği etkinleştirilirse hedeflenen her kullanıcı için tek ve genel olan varsayılan görünüm değişir. 
    >    - **Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde ve görünümü tüzel kişiliklerin bir alt kümesine yayımladığınızda bu tüzel kişiliklerin varsayılan görünümü, hedeflenen tüm kullanıcılar için değişir.
    >
    > - Bir kullanıcının birden çok görünümün varsayılan görünüm olarak yayımlandığı rollere sahip olması durumunda, yayımlanan son görünüm kullanıcının varsayılan görünümü olarak kullanılacaktır. 

8. Bu görünüm tarafından hedeflenen kullanıcılara karşılık gelen güvenlik rollerini ekleyin. 
9. Görünümü, seçilen her güvenlik rolünün alt rollerine yayımlamak isteyip istenediğinizi belirleyin. İstiyorsanız uygun güvenlik rolleri için satırdaki **Alt rolleri dahil et** onay kutusunu seçin. Bu onay kutusu, alt rollere sahip olmayan roller için kullanılamaz.
10. Bu görünümün kullanılabilir olması gereken tüzel kişilikleri ekleyin. 

    > [!NOTE]
    > Belirli bir tüzel kişiliğe bir görünüm yayımlayıp bu görünümü varsayılan görünüm olarak yayımlamazsanız aşağıdaki davranışa dikkat edin:
    >
    > - Yalnızca temel **Kayıtlı görünümler** özelliği etkinleştirildiğinde kullanıcının sayfa için görünüm seçicisi başlangıçta yalnızca belirtilen tüzel kişilikler için görünümü gösterir. Ancak görünümün ilk kez yüklenmesinin ardından sayfanın görünüm seçicisi tüzel kişiliklerden bağımsız olarak her zaman yüklenen görünümü gösterir.
    > - **Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde görünüm seçici yalnızca belirtilen tüzel kişilikler için görünümü gösterir.

11. **Yayımla**'yı seçin.

Bazı ortamlarda, kullanıcılar yayımlanan görünümü görebilmeleri için biraz zaman (bir saat kadar) sürebilir.

## <a name="modifying-a-published-view"></a>Yayınlanmış görünümü değiştirme

Bir görünümü yayımladıktan sonra, değiştirmek isteyebilirsiniz. Yayımlanmış bir görünümde canlı değişiklikler yapamazsınız ancak bu görünümler tüm kullanıcılar için (yayımcılar dahil) düzenlemeye karşı kilitlenmiş olduğundan, güncelleştirme yapmak için bir görünümü yeniden yayımlayabilirsiniz.

Yayınlanmış bir görünümde yapmak istediğiniz değişiklikler yalnızca yayımlama parametreleri (görünümün adı ve açıklaması veya görünümün yayımlandığı güvenlik rolü) içeriyorsa, aşağıdakileri yapın:

1. Güncelleştirmek istediğiniz parametreler için yayımlanmış görünüme geçin. 
2. Görünüm seçici açılır menüsünden **Yeniden Yayımla**'yı seçin. Sürüm 10.0.12 veya öncesini kullanıyorsanız varolan görünümü güncelleştirmek için **Yayımla**'yı ve sonra **Evet**'i seçmelisiniz.
3. Görünüm için ad, açıklama, güvenlik rolleri ve tüzel kişilikleri güncelleştirin. 
4. **Yayımla**'yı seçin. Özgün olarak bu yayımlanan görünümü varsayılan görünüm olarak seçtiyseniz, yeniden yayımladıktan sonra kullanıcılar için varsayılan görünüm olur. 

Yayınlanan görünümde yapılan değişiklikler, görünümle ilişkili kişiselleştirmeler veya filtrelerde değişiklik içeriyorsa aşağıdaki adımları izleyin.

1. Değiştirmek istediğiniz yayımlanmış görünümü yükleyin. 
2. Yerel taslakta gerekli değişiklikleri yapın.
3. Görünüm seçici açılır menüsünden **Yeniden Yayımla**'yı seçin.
4. Görünümü, kaydedilmemiş değişiklikleriyle birlikte yayımlamak istediğinizi belirtmek için **Evet**'i seçin. 
5. Düzeltme gerektiren tüm yayımlama parametrelerini ayarlayın ve sonra **Yayımla**'yı seçin. 

## <a name="managing-published-views"></a>Yayımlanmış görünümleri yönetme

Kişisel görünümleri yönetmek gibi, **Görünümlerimi yönet** iletişim kutusu, yayımlama ayrıcalıklarına sahip kullanıcılara, yayımlanmış görünümler içeren bir sayfa üzerinde temel bakım yeterlilikleri sağlar (kendi kişisel görünümlerine ek olarak). Bu sayfayı açmak için görünüm seçiciyi açılır menüsünü açmak üzere görünüm adını tıklatın, **Diğer**'i seçin ve sonra **Görünümlerimi Yönet**'i seçin.

Tüm kullanıcılar kişisel görünümlerini gösteren **Görünümlerim** sekmesine sahip olsa da yayımlama ayrıcalığına sahip kullanıcılar, o sayfa için yayımlanan ve yayımlanmayan tüm görünümleri gösteren **Kuruluş görünümleri** sekmesini de görür. Birçok kullanıcı görünüm yayımlayabileceği için görünümü gerçekten yayımlamış olan kullanıcı olup olmadığınıza bakılmaksızın, yayımlanmış görünümlerin tam listesini yönetmeniz önemlidir.

Sayfa için tüm yayımlanmış görünümlerin listesi için aşağıdaki eylem kümesi kullanılabilir. 

- **Yeniden Yayımla**: Yayımlama parametreleri (ad, açıklama, güvenlik rolleri) değiştirildikten sonra bir görünümü yeniden yayımlamak için **Yeniden Yayımla** eylemini kullanın.
- **Yayımla**: Şu anda yayımdan kaldırılmış bir görünümü yayımlamak için **Yayımla** eylemini kullanın. 
- **Yayımdan Kaldır**: Bir görünümü devre dışı bırakmak için **Yayımdan Kaldır** eylemini kullanın. Görünüm sistemde kullanılabilir olmaya devam eder ancak kullanıcılar görünüm yeniden yayımlanana kadar görünüm seçicisinde göremez.
- **Kişisel olarak Kaydet** – yayınlanan görünümün kişisel taslak kopyasını oluşturmak için **kişisel olarak Kaydet** eylemini kullanın. Bu özellik, size yayınlanmamış veya henüz yayınlanmamış bir görünümün içeriğini anlamanıza yardımcı olabilir. Ayrıca, bir görünümü düzenleyip yeniden yayımlamak için de kullanabilirsiniz.
- **Sil**: Yayımlanmış bir görünümü kalıcı olarak silmek veya yayımdan kaldırmak için **Sil** eylemini kullanın. Bu eylem sistemdeki tüm kullanıcıların görünümünü de kaldırır. Yayımlanan görünümlerin kaldırılması **Kaydet** düğmesi seçildikten sonra etkili olur. Bir görünüm silindikten sonra kurtarılamaz. 

## <a name="managing-views-globally"></a>Görünümleri genel olarak yönetme

Bu makale belirtildiği gibi, bazı yönetim özellikleri her sayfada yer almakla birlikte, **sistem yöneticileri** ve **kaydedilmiş görünüm yöneticileri**, **Kişiselleştirme** sayfası aracılığıyla sistem için görünümleri daha bütüncül olarak yönetebilir. Özellikle, Bu sayfa aşağıdaki bölümlere ve yeteneklere sahiptir: 

- **Yayınlanan Görünümler** – Bu bölüm, organizasyonunuz için yayımlanmış tüm görünümleri listeler. Burada, görünümün hedeflediği güvenlik rollerini veya tüzel kişilikler ayarladıktan sonra bir görünümü yeniden yayımlayabilirsiniz. Dilerseniz görünümleri dışa aktarabiliri silebilir veya yayımdan kaldırabilirsiniz. Bir görünümün bir kişisel kopyasını oluşturmak için **Kişisel olarak kaydet** eylemini kullanabilirsiniz, böylece görünümü güncelleştirebilir veya içeriğinin daha iyi anlaşılmasını sağlayabilirsiniz. 
- **Yayımlanmamış görünümler**: Bu bölüm, sisteminizdeki yayımlanmayan tüm kuruluş görünümlerini listeler. Bu görünümler genellikle içe aktarma özelliği aracılığıyla sisteme gelir. Bu görünümleri yayımlayabilir, dışa aktarabilir veya silebilirsiniz. 10.0.12 sürümüne eklenen **hızlı yayımlama** eylemi, varolan güvenlik rolü ve yasal varlık yapılandırmaları kullanılarak tek bir eylemde bu bölümdeki çoklu görünümlerin yayımlanmasına olanak tanır. Görünümün bir kişisel kopyasını oluşturmak için **Kişisel olarak kaydet** eylemini kullanabilirsiniz, böylece görünümü güncelleştirebilir veya içeriğinim daha iyi anlaşılmasını sağlayabilirsiniz.
- **Kişisel görünümler** – Bu bölümde tüm görünümler sistemdeki kullanıcılar tarafından oluşturulur. Bir kişisel görünümü kuruluşa yayımlayabilir veya bu görünümlerden birini veya birkaçını diğer kullanıcılara kopyalayabilirsiniz. Bu görünümleri gerektiğinde dışa aktarabilir veya silebilirsiniz.
- **Kullanıcı ayarları**: Görüntülenecek kullanıcıyı seçin veya kullanıcının tüm sistem veya kullanıcının ziyaret ettiği belirli sayfalar için kişiselleştirme özelliğini kullanma olanağını ayarlayın. Kullanıcının kişiselleştirmelerini görüntüleyebilir ve sistemde etkileşime geçebilirsiniz. Ayrıca, o kullanıcının tüm kişiselleştirmelerini silebilir veya kullanıcının özellik açıklamalarını sıfırlayabilirsiniz. Özellik açıklamaları sıfırlanırsa yeni özellikler sunan ve kullanıcının daha önce kapattığı tüm açılan pencereler kullanıcının bu özelliklerle sonraki karşılaşmasında yeniden görünür.
- **Sistem ayarları**: Tüm kullanıcılar için kişiselleştirmeleri geçici olarak devre dışı bırakabilirsiniz. Bu durumda, tüm kullanıcılar için hiçbir kişiselleştirme uygulanmaz ve tüm sayfalar varsayılan durumlarına sıfırlanır. Kişiselleştirmeyi daha sonra yeniden etkinleştirirseniz, tüm kişiselleştirmeler yeniden uygulanır. Ayrıca sistemdeki tüm kullanıcılar için tüm kişiselleştirmeleri kalıcı olarak silebilirsiniz. Silinmiş kişiselleştirmeler kurtarılamaz. Bu nedenle, bu görevi uygulamadan önce, daha sonra içeri aktarmak isteyebileceğiniz kişiselleştirmeleri dışa aktardığınızdan emin olun.

**Kişiselleştirme** sayfasına erişimi olan kullanıcılar, Eylem bölmesindeki **Görünümleri içe aktar** düğmesini kullanarak kişisel veya kuruluş görünümlerini de içe aktarabilir. Kuruluş görünümlerinde, ek açık yayımlama olmadan görünümleri kullanıcılara sunmak için **Hemen yayımla**'yı seçebilirsiniz.

## <a name="known-issues"></a>Bilinen sorunlar

Kaydedilmiş görünümlerle ilgili bilinen sorunların listesi için bkz. [Kaydedilmiş görünümlerden tam olarak yararlanan formlar oluşturma](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kaydedilmiş görünümleri ortamımda nasıl etkinleştirebilirim?

> [!NOTE]
> **Kaydedilmiş görünümler** özelliği, finans ve operasyon uygulamalarında Kişiselleştirme sisteminin etkinleştirilmesini gerektirir. Tüm ortam için kişiselleştirme kapatılmışsa, aşağıdaki adımları izleseniz bile görünümler devre dışı bırakılır. 

**Kayıtlı görünümler** özelliğini herhangi bir ortamda Özellik yönetimi ile etkinleştirebilir veya devre dışı bırakabilirsiniz. Etkinleştirildiğinde kayıtlı görünümler sonraki tüm kullanıcı oturumlarında etkinleştirilir.

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

Küçük görüntüleme seçicilerine sahip sayfalar için (görünüme yalnızca kişiselleştirmeler kaydedilebilir), sayfayı her zaman ziyaret ettiğinizde aynı verileri görürsünüz. 

Büyük görünüm seçicileri olan sayfalar için (hem kişiselleştirmeler hem de sorgular görünüme kaydedilebilir), genellikle varsayılan görünümle ilişkilendirilmiş sorguyla bağlantılı verileri görürsünüz. İki ana özel durum vardır:

- Bir sayfaya bir kutucukta gezindiğinizde, döşemedeki sorgu, varsayılan görünümle ilişkilendirilmiş sorgudan bağımsız olarak yürütülür. Bu kutucuğu, görünümler etkinleştirildikten sonra oluşturduysanız, bir kutucuk seçilmesi sayfayı o döşemeyle ilişkili görünümle açar.
- Bir sayfaya giderseniz ve bu giriş noktası bir sorguya sahipse, özgün sorgu başlangıçta varsayılan görünümün sorgusunun yerine yürütülür. Bu durumda, görünüm yüklenirken bir bilgi iletisi ile uyarı alırsınız. Ayrıca, sayfa yüklendikten sonra bu görünüme geçerek, görünüm sorgusunun ne olursa olsun yürütülmesine izin vermek istiyorsanız da onay alabilirsiniz.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Belirli bir tüzel kişilik için yayımlanan bir görünüm neden tüm tüzel kişiliklerde görünüyor?

Belirli bir tüzel kişiliğe bir görünüm yayımlayıp bu görünümü varsayılan görünüm olarak yayımlamazsanız aşağıdaki davranış gerçekleşir:

- Yalnızca temel **Kayıtlı görünümler** özelliği etkinleştirildiğinde kullanıcının sayfa için görünüm seçicisi başlangıçta yalnızca belirtilen tüzel kişilikler için görünümü gösterir. Ancak görünümün ilk kez yüklenmesinin ardından sayfanın görünüm seçicisi tüzel kişiliklerden bağımsız olarak her zaman yüklenen görünümü gösterir. Bu davranış, kullanıcıların kendi kişisel kopyalarını yayımlanan görünüm yüklendikten sonra aldıkları için ve kişisel görünümlerin genel olması nedeniyle oluşur.
- **Sürüm 10.0.21 veya sonrası:** **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği etkinleştirildiğinde görünüm seçici yalnızca belirtilen tüzel kişilikler için görünümü gösterir. Bu davranış, özellik sayesinde görünümlerin (kişisel görünümler dahil) belirli tüzel kişiliklere bağlanması nedeniyle oluşur.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

