---
title: Geriye dönük maliyetlendirme
description: Bu konu, Yalın imalat için geriye dönük maliyetlendirme kavramını tanıtmaktadır.
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: be4dbadaeac747953af44236156453edc596fcd5
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018124"
---
# <a name="backflush-costing"></a>Geriye dönük maliyetlendirme

[!include [banner](../includes/banner.md)]

Bu konu, Yalın imalat için geriye dönük maliyetlendirme kavramını tanıtmaktadır. 

Yalın üretim için maliyetlendirme, üretim akışının geriye dönük maliyetlendirme olarak bilinen maliyet biriktirme yöntemini kullanmasına olanak sağlar. Geriye dönük maliyetlendirme yönteminde, doğrudan malzemeler üretim akışının süren iş işlemi (WIP) maliyet hesabında toplanır ve tüketilir. Standart maliyet stok model grubu kullanılır. Üretim akışından alınan ürünler, başlangıç maliyetlerinde WIP'den çıkartılır. Standart maliyet ve geriye dönük maliyetlendirme arasındaki fark, geriye dönük maliyetlendirme için farkların kanban veya tamamlanmış ürün başına hesaplanmamasıdır. Bunun yerine, farklar üretim akışı başına bir dönem üzerinden hesaplanır. Bu yöntem, malzeme tüketimini raporlamak için gerçekten yalın bir kavramı tanıtır. Adanmış çekilen malzeme miktarları bir kanban veya üretim siparişine raporlanmaz. Bunun yerine, tüm toplu işler veya birimler, üretim akışına hazırlanır. Toplu işler veya işleme birimleri boş olarak kaydedildikten sonra, tüketilmiş olarak bildirilirler. Gelişmiş tüketim, [üretim akışının yapılandırmasına](../production-control/lean-manufacturing-modeling-lean-organization.md) bağlı olarak kullanılabilir. Gelişmiş tüketimin kullanılabilmesi kuruluşların için önce kendilerine üretim akışının süren işi içerisinden malzeme kaybolmasına izin vermeleri gerekir. Periyodik geriye dönük maliyetlendirme, süren işin etkin değerini, dönemin sonunda belirler. Bu belirleme, kanban işleme birimlerini ve kanban iş durumunu temel alır. Maliyet grubu ve madde başına etkin değerler ve gerçek süren iş değerleri arasındaki farklılıklar hesaplanır ve farklar olarak gösterilir.

## <a name="configuring-backflush-costing"></a>Geriye dönük maliyetlendirme yapılandırması
Maliyetlendirmeyi etkinleştirmek için aşağıdaki kurulumu tamamlamanız gerekir:

-   **Üretim grubu ve üretim akışı için süren iş hesaplarını ayarlayın.** Üretim akışı için süren iş hesapları, üretim grubunda belirtilir. Geriye dönük maliyetlendirme üretim akışı, süren iş değerinde geriye dönük maliyetlendirme, her bir üretim akışında çalıştırılmadan önce ve sonraki farkları olarak hesaplar. Bu nedenle, her üretim akışı için bir süren iş hesabı oluşturmanız öneririz.
-   **Kaynak grubuna bir maliyet kategorisi atayın** Çalışma hücresinin çalışma zamanı kategorisine bir maliyet kategorisi atamanız gerekir. Etkinliğe göre farkları belirlemek için her iş hücresi için bir maliyet kategorisi oluşturmanız gerekir. Kurulum ve miktar için maliyet kategorileri, yalın imalat için maliyetlendirmede dikkate alınmaz. Kaynak grup başına süren iş hesapları, geriye dönük maliyetlendirmede yok sayılır. Taşeronlu faaliyetler için maliyet kategorisi gerekli değildir. Bunun yerine, etkin servise atanan maliyet grubu kullanılır.
-   **Maliyet grupları ata.** Bir üretim akışında maliyet dağıtım ayrıştırmayı etkinleştirmek için, maliyet gruplarını maliyet grubu türüne atamanız gerekir:
    -   **Doğrudan malzeme maliyeti grubu** - Doğrudan malzeme, maliyetlendirme için malzemenin kategorisini tanımlayan bir maliyet grubu gerektirmektedir. Bu maliyet grubu, maliyetin, süren işin ve farkların doğrudan malzemeye göre birleştirilmiş bir görüntüsünü sağlar.
    -   **Doğrudan üretim maliyet grubu** - Doğrudan üretim maliyet grubu, yönetimsel kaynakların üretim akışına doğrudan maliyet katkısını yakalar. Bu maliyet grubu, maliyetin, süren işin ve farkların doğrudan üretim maliyetine göre birleştirilmiş bir görüntüsünü sağlar.
    -   **Dolaylı maliyet grubu** - Dolaylı maliyet grubu, üretim akışına dolaylı maliyetin katkısını hesaplamak için gereklidir. Bu maliyet grubu, maliyetin, süren işin ve farkların dolaylı maliyete göre birleştirilmiş bir görüntüsünü sağlar.
    -   **Doğrudan taşeron maliyet grubu** - Hizmetler için maliyet grubu, atanmış maliyet ve süren işin birleştirilmiş bir görünümü sağlar ve alt sözleşmeli hizmetlerin maliyet farklarını belirler.
    -   **Mamul mal için maliyet grubu** - Mamul mallar, ürün kategorisini maliyetlendirme için tanımlayan bir maliyet grubu gerektirir. Bu maliyet grubu, maliyetin, süren işin ve farkların ürün kategorisine göre birleştirilmiş bir görüntüsünü sağlar. Ürünler için standart maliyet, ürün reçetesine (BOM) dayanan maliyet hesaplaması ve üretim akışı veya kanban kuralları ya da rota kullanarak hesaplanır.

### <a name="costing-sheet"></a>Maliyetlendirme tablosu

Maliyetlendirme tablosu, şirket için maliyet yapısını modeller ve maliyeti sınıflandırmak için maliyet grupları tarafından oluşturulur. Maliyetlendirme tablosu çeşitli biçimlere sahiptir. Buna göre tasarlanmış yapının maliyet bilgisini gösterir. Maliyetlendirme tablosunda, dolaylı maliyeti hesaplamak için kullanılan formülü de tanımlarsınız. Hesaplama formülü miktarlar, ağırlık, hacim veya değere dayalı olabilir.

-   **Bir maliyetlendirme sürümü tanımla** Maliyetlendirme sürümünde, şirket maliyetin nasıl saklanması gerektiğini tanımlar. Maliyetlendirme versiyonu, maliyetlendirme versiyonuna atanan maliyetlendirme tipine bağlı olan bir standart maliyet kayıtları veya planlanan maliyet kayıtları kümesi içerebilir. Yalın imalatın maliyetlendirmesi için kullanılan maliyetlendirme sürümü, standart maliyete dayalı olmalıdır.
-   **Piyasaye sürülen ürünler için bir stok model grubu atayın** Üretim akışıyla ilişkili olan tüm ürünler, **Standart maliyet** stok model grubunu kullanan bir stok model grubuna atanmalıdır. Standart maliyet, site ve etkinleştirme tarihine göre tutulur. Ana ürünler için stok model grubu, maliyet ürün çeşidi veya ana ürün için tutuluyorsa seçilebilir.
-   **Tanım olarak, alt sözleşmeli hizmetler stoksuz hizmetlerdir.** Alt sözleşmeli etkinliklerin stok model grubu yoktur. Alt sözleşmeli bir işi doğru maliyetlendirmek için hizmet etkinliğinin stok ilkesi **Stoklu ürün = Yanlış** olarak ayarlandığı bir stok model grubuna ait olduğundan emin olmanız gerekir.

Çıkış ürünleri için üretim akışına dayanan maliyet hesaplaması, hizmetler için standart maliyetin alt sözleşmeli etkinliklerle ilişkili olmasını gerektirir. Hizmetlere atanan maliyet grubu, alt sözleşmeli etkinliklerin maliyet farkını belirlemekte kullanılır.

## <a name="cost-calculation-for-lean-manufacturing"></a>Yalın üretim için maliyet hesaplaması
Üretim akışından dışarı tedarik edilen ürünler için ürün reçetesi hesaplaması ya bir rota sürümüne ya da üretim akışına dayalı olmalıdır. Ürün reçetesi hesaplaması, bir ürünün maliyetini ve ürünü üretmek için gerekli malzeme ve kaynakların ilişkili dökümünü hesaplar. Üretim akışı için süren iş hesabından çıkartma, bir ürünün madde ve maliyet grubuna göre dökümü kullanılarak yapılır.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Üretim akışına dayanan hesaplama

Dynamics 365 Supply Chain Management için Yalın imalat, yollardan bağımsızdır. Bir üretim akışından tedarik edilen ürünler için maliyet hesaplaması, üretim akışını temel alabilir. Hesaplamanın yapılabilmesinden önce, ürünü üretim akışından tedarik eden bir kanban kuralı oluşturulmalıdır. Ürün, üretim tarihinde aynı tesisteki birden fazla üretim akşından tedarik edilebiliyorsa, ürün reçetesi hesaplaması için üretim akışını seçebilirsiniz. **Varsayılan üretim akışı** sayfası üzerinde bir varsayılan üretimi akışını her bir madde için yapılandırabilirsiniz. Aynı ürün için aynı üretim akşında, aynı hesaplama tarihinde etkin birden fazla kanban kuralı mevcutsa, hesaplama, hesaplama için etkin ilk kanban kuralını seçer.

### <a name="calculation-that-is-based-on-the-route"></a>Rotayı temel alan hesaplama

Rotayı temel alan hesaplama, üretim akışını temel alan hesaplama kadar geçerlidir. Ancak, rotayı temel alan hesaplama, Yalın imalat işlevi için maliyetlendirmeyi kullanmaz. Rota, kaynak grupları için kaynak gereksinimlerini kullanmalıdır. Sistematik farkları önlemek için aynı iş hücrelerini veya en azından aynı maliyet kategorilerini kullanmalıdır. Kurulum ve miktar içi maliyet kategorilerinden yine kaçınmalısınız. Bunlar maliyeti, Yalın imalat maliyet geriye dönük hesaplamasına göre daha ayrıntılı bir dökümle hesaplamazlar. Maliyeti hesaplamak için hangi seçeneği (üretim akışı veya rotası) kullanmanız gerektiğini belirlemek için, maliyet dökümünün sonuçlarını göz önünde bulundurun. Gerçeğe daha çok yaklaşan ve genel olarak daha az fark üreten sürüm daha iyi bir seçenektir. Bir ürünün, tek bir üretim akışı ve tek bir kanban kuralı tarafından sağlandığı bir Yalın imalat ortamında, üretim akışına dayanan bir hesaplamanın daha doğru olması muhtemeldir. Yalın imalat ve üretim siparişleri tarafından aynı tesiste tedarik edilebilir veya aynı akış içerisinde birden fazla üretim akışı veya birden fazla kanban kuralına sahip bir ürün için bir hesaplama, üretim için değil de maliyet hesaplaması için özel olarak inşa edilmiş bir rota sürümüne dayanan bir hesaplama daha doğru olabilir. Üretim akışı hesaplaması, alt sözleşme içeren ürünleri hesaplarken kullanılmalıdır. Üretim emirleri ve Yalın imalat içerisinde alt sözleşme için maliyet modelleri, iki farklı yaklaşımı kullanır. Yalın üretim yeni bir maliyet grubu türü olan **Doğrudan alt sözleşme verme**'yi, alt sözleşmeli hizmetleri hesaplamak için kullanır.

## <a name="material-consumption"></a>Malzeme tüketimi
Bir malzeme stoktan, süren işe tüketildiğinde, malzemenin maliyeti süren işe, bir maliyet grubu için geçerli standart maliyetinden eklenir. Bu işlem, aşağıdaki koşullarda gerçekleşir:

-   Kanban sorunları, stoku güncelleştiren kanban çekme satırları için deftere nakledilir.
-   Transfer işleri, stoku çekmede güncelleştiren ancak girişte güncelleştirmeyen için tamamlanır (Malzemenin stoktan süren işe nakli).

## <a name="receiving-products-from-the-production-flow"></a>Üretim akışından ürünleri almak
Ürünler, aşağıdaki durumlarda üretim akışından alınır:

-   **Stoku girişte güncelleştir** seçeneği **Evet** olarak ayarlanmış olan İşlem işleri tamamlanır.
-   Stoku girişte güncelleştiren ancak **Stoku çekmede güncelleştir** seçeneği **Hayır** (süren işten stoka aktarım) olarak ayarlanmış transfer işleri tamamlanır. Bu seçenek, ürün reçetesi ve rota yapılandırmasından bağımsız olarak herhangi bir ürünü bir üretim akışından almanıza olanak sağlar. İşlem yalnızca fiziksel akışları izler. Bu seçenek özellikle yan ürünleri, ortak ürünleri veya hurdaları bir üretim akışından alırken ve üretim akışı süren işin maliyet bakiyesini düzeltmek için uygundur.

Üretim akışından alınan ürünler, süren işten çıkartılır.

## <a name="products-in-wip"></a>Süren işteki ürünler
Yalın imalatın süren iş modeli, süren işin parçası olan malzemeyi, yarı bitmiş ürünleri ve bitmiş ürünleri yönetmeniz için kanban işleme birimi durumlarını kullanmanıza olanak sağlar.

-   **Atanan** - Kanban, süren iş içerisinde muhasebesi tutulan tüketilen malzemeye sahip olabilir.
-   **Alınan** - Kanban, **Girişte stoku güncelleştir** seçeneği **Hayır** olarak ayarlanmış son etkinliği gösteriyorsa, bir stoka kayıtlı olmayan bir ürünün veya yarı bitmiş ürünün tam işleme birimini temsil eder.

Süren işteki malzeme, stok eldeki genel bakışlarında görünür değildir. Bununla birlikte, kanban miktar genel bakışında görünürdür.

## <a name="consuming-products-in-wip"></a>Süren iş içerisinde ürünleri tüketmek
Süren iş içerisindeki ürünler, karşılık gelen kanban işleme birimleri boşaltıldığında tüketilir. Bir kanban boş sinyali, bir etkin maliyetlendirme hareketi üretmez, ancak bir sonraki geriye dönük maliyetlendirme çalıştırıldığında etkili olur. Boşaltılan kanban işleme birimleri, daha fazla elde olarak hesaba katılmaz ve bu nedenle dönem içerisinde tüketilmiş olarak hesaplanır.

### <a name="automatic-empty-registration"></a>Otomatik boş kayıt

Planlanan veya etkinlik kanbanları, kanban kuralında otomatik boş kayıt olarak ayarlanabilir:

-   **İşleme birimleri alındığında** - Planlanmış kanbanlar için varsayılan olarak, malzeme kanbanın son işi tamamlandığında tüketilmiş olarak bildirilir. Sabit miktar kanbanları için bu seçenek yalnızca tek bölmeli kanbanlar için önerilir çünkü kartı, bir kanban son hedefine vardığında talebin kaynağına döndürür.
-   **Kaynak gereksinimi kaydedildiğinde** - Bu seçenek, yalnızca etkinlik kanbanları için kullanılabilir ve onlar için varsayılan seçenektir. Süren iş ile bağlantılı olarak bu seçenek, süren işi temiz tutmak için kullanışlıdır çünkü süren iş içerisindeki bileşenler için kanbanlar otomatik olarak boşaltılır ve bu nedenle, üst kanban hazırlandığında süren işten tüketilir.

Özet olarak, kanban işleme birimleri atanabilir (= işlem içerisinde), alınabilir (= tam) veya boşaltılabilir. Kısmi boşaltma yoktur. Bu nedenle, tüketimin doğru kaydını etkinleştirebilmek için bir kanbanın üretim miktarlarını, dönem başına tüketimden az olacakları şekilde sınırlamak önemlidir. Toplu olarak atölyeye götürülüp günlük veya haftalık talebi karşılayan ürünler, süren işe tüketilmemelidir. Bunun yerine, bu ürünler stokta tutulmalıdır.

## <a name="backflush-costing"></a>Geriye dönük maliyetlendirme
Süren işi dönemsel olarak değerlemek ve malzeme, işçilik ve dolaylı maliyetlerin farkını hesaplayacak dönem sonu durumu oluşturmak için geriye dönük maliyetlendirme çalıştırmalısınız. Hesaplanan farkları, fark hesabına nakledilir. Geriye dönük maliyetlendirme işleminde, tüzel varlığın tüm üretim akışları aynı toplu iş işleminde kullanılır. Geriye dönük maliyetlendirme toplu iş içerisinde çalıştırıldığında, işleme üretim akışı tarafından çok iş parçacıklı olabilir. Geriye dönük dönemi, bir bitiş tarihi tarafından tanımlanır. Bir geriye dönük maliyetlendirme hesaplaması çalıştırıldığında, yeni bir hareketi bu tarihe nakledemezsiniz. Gün gerçekten bitmeden önce geçerli tarih için geriye dönük maliyetlendirmeyi asla çalıştırmamalısınız. Geriye dönük maliyetlendirme aşağıdaki adımları izler.

1.  Dönemin son tarihi itibariyle üretim akışındaki kullanılmamış miktarları belirleyin. Geriye dönük maliyetlendirme çalıştırıldığında, maliyetlendirme çalıştırılmasındaki tarihte kullanılmamış miktarları **Kullanılmamış miktarlar** iletişim kutusunda görebilirsiniz.
2.  Üretim akışının dönemdeki net gerçekleşen kullanımını hesaplayın.
3.  Süren işi gerçekleşen kaynak tüketimi ve ürünlerinden temizleyin.
4.  Dönem için üretim farklarını, standart maliyete hesaplar. **Dönem için kullanılan bileşenler için:**
    -   Üretim akışının dönemde tükettiği net gerçekleşen malzeme miktarını mali olarak güncelleştirin. Sistem tekil stok hareketlerini, üretim akışı için fiziksel olarak güncelleştirilen harekteleri mali olarak güncelleştirmek için, ilk giren ilk çıkar (FİFO) sırasında işler, dönem için net gerçekleşen miktarlara erişilene kadar.
    -   Hareketler, tüketilen miktarları tam olarak eşleştirmek için mali olarak ayrılır.
    -   Üretim akışı süren iş içerisindeki kullanılmayan miktarlar, fiziksel olarak güncelleştirilmiş durumda kalır.

    **Dönemin üretimi tamamlanan miktarları için:**
    -   Dönem için tamamlanan miktarların stok hareketlerini mali olarak güncelleştirin.

    **Dönüştürme maliyeti için:**
    -   Dönem için kaydedilen, uygulanan dönüştürme maliyet hareketleri (rota hareketleri), mali olarak güncelleştirilir.
    -   Tüm doğrudan üretim maliyetleri mali olarak güncelleştirilmiştir. Bu dönemde tamamlanan tüm kanban işlem işleri, toplanır.
    -   Dönem içerisinde tüketilen tüm dolaylı maliyetler, hesaplanır ve süren işten çıkartılır. Kalan dolaylı maliyet, fark olarak deftere nakledilir.

5.  Üretim farklarını standart maliyete göre hesapla. Fark, maliyet grubu başına hesaplanır.





