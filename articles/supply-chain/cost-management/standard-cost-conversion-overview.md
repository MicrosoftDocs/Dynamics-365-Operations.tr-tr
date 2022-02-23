---
title: Standart maliyet dönüştürme özeti
description: Bu makalede bir standart maliyet dönüştürme işleminin kurulması ve yürütülmesine yardımcı olacak sürecin genel görünümü verilmiştir. Listelenen adımlar bir standart maliyet dönüştürme işlemi için ön koşulları tamamlamanızdan sonra tamamlanacak şekilde açıklanmıştır.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9874d3b44a687a60ea1fd26889af3d1b644f86a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439378"
---
# <a name="standard-cost-conversion-overview"></a>Standart maliyet dönüştürme özeti

[!include [banner](../includes/banner.md)]

Bu makalede bir standart maliyet dönüştürme işleminin kurulması ve yürütülmesine yardımcı olacak sürecin genel görünümü verilmiştir. Listelenen adımlar bir standart maliyet dönüştürme işlemi için ön koşulları tamamlamanızdan sonra tamamlanacak şekilde açıklanmıştır. 

Seçili maddeler grubu için stok modelini bir fiili maliyetlendirme yaklaşımından standart maliyetlendirme yaklaşımına dönüştürmek için **Standart maliyet dönüştürme işlemleri** sayfasını kullanın. Dönüştürme süreci bir önkoşul stok kapanışı yapmayı, geçiş döneminde (geçiş başlangıç tarihi ve planlanan dönüştürme tarihi tarafından tanımlanır) birkaç adım gerçekleştirmeyi ve dönüştürmeyi ve ilgili stok kapanışını gerçekleştirmeyi içerir.

-   Geçiş döneminden önce stok kapanışı − Stok kapanışı bir önkoşul adımını temsil eder, çünkü bir maddenin eski değerleme yöntemi altındaki açık hareketlerini kapatır. Geçiş dönemi içinde, örneğin faturalar gibi eski tarihli hareketleri girebilir ve deftere nakledebilirsiniz, böylece önceki dönemi kapatabilirsiniz. Eski değerleme yönteminin tümüyle devre dışı kalması için stok kapatma tarihi geçiş başlangıç tarihinden bir gün önce olmalıdır.
-   Geçiş dönemindeki dönüştürme adımları − Yeni bir maliyetlendirme versiyonu için kullanıcı tanımlı bir tanımlayıcı içeren bir dönüştürme kaydı oluşturmak için **Standart maliyet dönüştürme işlemleri** sayfasını kullanın. Dönüştürülmesi gereken maddeleri belirler ve maddenin bekleyen standart maliyetlerini yeni maliyetlendirme versiyonuna girersiniz. Dönüştürme işlemini önleyebilecek sorunları belirlemek üzere seçilen maddelerde bir denetim gerçekleştirir ve ardından başka bir denetim gerçekleştirmeden önce sorunları çözersiniz. Maddeler kontrolleri başarıyla geçtikten sonra durumu (dönüştürme kaydının) **Hazır** olarak değiştirin. Planlanan dönüştürme tarihinde, dönüştürmeyi gerçekleştirin ve isteğe bağlı olarak bir stok kapanışı ekleyin. Bir geçiş dönemi içinde bir maddenin stok hareketleri eski stok modeline göre yayınlanır ve değerlendirilir. Ardından, dönüştürme işlemi başarıyla tamamlanır, stok hareketleri standart maliyete yeniden değerlendirilir.
-   Dönüştürmeden önce stok kapanışı − Stok kapanışı, dönüştürmeyi planlanan dönüştürme tarihinde gerçekleştirmenin bir parçası olarak dahil edilebilir veya dönüştürme öncesinde ayrı bir adım olarak gerçekleştirilebilir.

Dönüştürme süreci başarıyla tamamlandıktan sonra, her bir madde için stok modeli, standart maliyete dayalı olur ve maddenin standart maliyetleri etkinleştirilir. İzleyen stok hareketleri maddenin standart maliyetiyle değerlenir. Buna ek olarak sistem maddenin fiziksel stok hareketlerini girişler için dönüştürür ve dönüştürme tarihi itibariyle standart maliyete çıkarır. Sistem ayrıca maddenin mali eldeki stokunu standart maliyete dönüştürür ve değer farkını bir stok yeniden değerlemesi olarak deftere nakleder. Dönüştürmeden sonra gerçekleşen herhangi bir hareket maddenin standart maliyetiyle değerlenir. Eski tarihli hareketleri dönüştürme tarihinden önce giremezsiniz çünkü dönüştürme tarihinden bir gün önce stok kapanışı gerçekleştirilmelidir. Dönüştürme yalnızca bir önceki gün stok kapanışı yapılmışsa gerçekleştirilebilir. Bu stok kapanışı iptal edilemez.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Bir standart maliyet dönüştürme kaydı ve ilgili maliyetlendirme sürümünü tanımlayın
Bir dönüştürme kaydı oluşturmak için **Standart maliyet dönüştürme işlemleri** sayfasını kullanın. Yalnızca mevcut dönüştürme kayıtları tamamlandığında yeni bir dönüştürme kaydı oluşturulabilirsiniz. Planlı geçiş döneminin süresi, geçiş başlangıç tarihi ve planlanan dönüştürme tarihi tarafından belirlenir. Planlı geçiş dönemi tek bir gün kadar kısa olabilir. Planlı bir geçiş dönemi, dönüştürme sürecinin tüm adımları tamamlaması için yeterli zamanı olmasına yardımcı olur. Kapatmaların dönüştürme süreci başlatılmadan önce tamamlanması için, geçiş başlangıç tarihinden bir gün önce bir stok kapanışı yapılmalıdır. Geçiş başlangıç tarihi ile stok kapanış tarihinin doğru sırada olduğundan emin olmak için, geçiş başlangıç tarihini, mevcut bir stok kapanışından bir gün sonraki bir tarihi yansıtacak şekilde değiştirebilir veya bir stok kapanışı yapabilirsiniz. Bir dönüştürme kaydı girerken, dönüştürülen maddelerin standart maliyetlerini içerecek yeni bir maliyetlendirme versiyonu için kullanıcı tanımlı bir tanımlayıcı da girersiniz. Maliyetlendirme sürümü, dönüştürme kaydını kaydettiğinizde otomatik olarak oluşturulur.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Dönüştürme kaydı için yeni maliyetlendirme sürümünü inceleyin ve değiştirin
Yeni maliyetlendirme sürümü, **Dönüştürme** maliyetlendirme tipinin gösterdiği gibi dönüştürme kaydı için ayrılır. Ayrılan maliyetlendirme sürümü, standart maliyetler için bir maliyetlendirme sürümüne benzerdir ve dönüştürme kaydıyla ilişkili maddelerin madde maliyet kayıtlarını içerir. Bir dönüştürme kaydı için ayrılan maliyetlendirme sürümü, incelemeniz ve gerektiği gibi düzenlemeniz gereken aşağıdaki ayarlara sahiptir.

-   **Maliyet Türü:** Bu alanın **Standart maliyet** konumuna ayarlanmalıdır.
-   **Sürüm:** Bu tanımlayıcı, maliyet versiyonu kimliği için dönüştürme kaydına girilen bilgileri yansıtır.
-   **Ad:** Varsayılan olarak ad boştur. İsteğe bağlı olarak bir ad girebilirsiniz.
-   **Blok:** Bu alan **Hayır** konumuna ayarlanmalıdır. Dönüştürme kaydının durumunu **Hazır** olarak değiştirene kadar maliyetlendirme versiyonuna maliyet kayıtları girebilirsiniz. **Hazır** durumu, seçilen öğelerin denetlendiğini ve maliyet kayıtlarında değişikliğe izin verilmemesi gerektiğini gösterir.
-   **Blok etkinleştirme:** Bu alan **Evet** konumuna ayarlanmalıdır. Ayrılan maliyetlendirme versiyonunda beklemede olan bir maliyet kaydını el ile etkinleştiremezsiniz. Etkinleştirme, dönüştürmeyi uyguladığınızda gerçekleşir.
-   **Başlangıç tarihi:** Başlangıç tarihi, dönüştürme kaydına girilen planlanan dönüştürme tarihini yansıtır.
-   **Site:** Herhangi bir site için maliyet kayıtlarının girilebilmesi için bu alanı boş bırakın.
-   **Fiyat türü alan grubuna izin ver:** Sadece maliyet fiyatı kayıtlarının girilebilmesi için bu alanı **Evet** konumuna ayarlayın.
-   **Geri dönüş ilkesi:** Bu alanı **Yok** konumuna ayarlayın. Diğer maliyetlendirme sürümlerinde etkinleştirilmiş maliyet bilgilerine gerek duyduğunuzda geri dönüş ilkesini **Etkin** olarak değiştirin. Örneğin üretilen maddelerin maliyetlerini hesaplamak için bileşenler, maliyet kategorileri ve dolaylı maliyetler hakkındaki maliyet bilgileri gerekebilir.
-   **Geri dönüş maliyetlendirme sürümü:** Bu alanı boş bırakın.

Ayrılmış maliyetlendirme versiyonunda bulunan madde maliyet bilgileri yalnızca **Standart maliyet dönüştürme işlemleri** sayfasında saklanabilir. Dönüştürme işlemi sırasında maliyetlendirme sürümü için maliyetleri hesaplamak üzere **Maliyetlendirme sürümü kurulumu** sayfasını veya **Maliyetlendirme sürümü bakımı** sayfasını kullanamazsınız. Ancak, bu sayfaları, ayrılmış maliyetlendirme sürümü dönüştürme işlemi başarıyla gerçekleştirildikten sonra saklamak için kullanabilirsiniz.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Standart maliyete dönüştürülecek maddeleri tanımlayın
Standart maliyete dönüştürülmesi gereken maddeleri tek tek tanımlamak için **Standart maliyet dönüştürme işlemleri** sayfasını kullanın. **Maddeleri standart maliyet dönüştürmesine ekle** sayfasını kullanarak birden çok madde ekleyebilirsiniz. Genel olarak, maliyetlerin doğru şekilde hesaplanması için tüm üretilen maddeleri tek bir dönüştürme kaydına dahil etmeniz gerekir.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Dönüştürülmekte olan her bir madde için beklemedeki standart maliyeti girin veya hesaplayın
Satın alınan maddeler ve transfer edilen maddeler için, ayrılmış maliyetlendirme versiyonundaki standart maliyetleri girmek üzere **Madde fiyatı** sayfasını kullanın. Maliyet kayıtları tesise özeldir ve bir maddenin beklemedeki maliyetleri her tesis için girilmelidir. Üretilen maddeler için beklemedeki maliyetleri hesaplamak üzere **Madde fiyatı** sayfasını kullanın. Tesis bir transfer tesisini temsil etmiyorsa, üretilen bir maddenin beklemedeki maliyetleri her üretim tesisi için girilmelidir. Bu durumda, bekleyen maliyetler el ile girilmelidir. Bazı maddeler renk, boyut veya konfigürasyon ürün boyutlarına sahip olabilir. **Standart maliyet dönüştürme işlemleri** sayfasında, **Çeşide göre maliyet fiyatını kullan** onay kutusu, ürün boyutlarının her bir kombinasyonu için standart maliyeti gösterir. Bu onay kutusunun işareti kaldırıldığında madde için yalnızca bir beklemedeki maliyet girmeniz gerekir.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Dönüştürülen maddelerle ilgili herhangi bir sorun olup olmadığını kontrol edin ve varsa sorunu giderin
Dönüştürülmekte olan maddelerle ilgili sorunları tanımlamak için **Standart maliyet dönüştürme kontrolleri** raporunu kullanın. Sorun olan hiçbir madde bulunmuyorsa, dönüştürme kaydındaki durumu **Kontrol edildi** olarak değişir. Maddede sorunlar varsa, bu sorunu gidermeniz ve **Kontrol edildi** durumuna gelene kadar raporu tekrar çalıştırmanız gerekir. Maddeyle ilgili sorunları zamanında gideremiyorsanız, isteğe bağlı olarak maddeyi dönüştürmeden silebilir ve maddeyi daha sonra dönüştürebilirsiniz.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Dönüştürme kaydının durumunu Hazır olarak değiştirin.
Dönüştürme kaydının durumu **Hazır** olarak değiştirildiğinde, standart maliyet dönüştürme çalıştırılmadan önce son bir kontrol yapılmasını sağlar. Durum yalnızca aşağıdaki koşullar karşılandığında **Hazır** olarak değişir:

-   Dönüştürme kaydındaki her maddenin durumu **Kontrol edildi** olmalıdır.
-   Stok kapanışı, geçiş başlangıç tarihinden bir gün önce yapılmış olmalıdır. Geçiş başlangıç tarihi ile stok kapanış tarihinin doğru sırada olduğundan emin olmak için, geçiş başlangıç tarihini, mevcut bir stok kapanışından bir gün sonraki bir tarihi yansıtacak şekilde değiştirebilir veya bir stok kapanışı yapabilirsiniz.

## <a name="7-back-up-the-database-before-conversion"></a>7. Dönüştürme öncesi veritabanını yedekleyin
Yedekleme, dönüştürme işlemi sırasında hatalar meydana gelmesi durumunda veritabanını geri yüklemenizi sağlar.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Dönüştürme kaydının durumu Hazır olunca dönüştürme işlemini gerçekleştirin
Dönüştürme işlemi planlanan geçiş başlangıç tarihinden bir gün önce stok kapanışı yapılmasını gerektirir. Bu şart, eski tarihli hareketlerin geçiş dönemine girilememesine yardımcı olur. Henüz bir stok kapanışı yapılmamışsa, dönüştürme işleminin bir parçası olarak bunu yapmak isteyip istemediğiniz sorulur. Dönüştürme süreci aynı anda sadece bir maddeyi işler. Maddenin düşük düzeyli koduna bağlı olarak, bir ürün yapısındaki en düşük maddeden başlar. Bir madde başarıyla dönüştürüldüğünde, dönüştürme kaydındaki durumu **Dönüştürüldü** olarak değiştirilir. Dönüştürme süreci yarıda kesilirse, başarıyla dönüştürülmemiş olan maddeler **Kontrol edildi** durumunda kalmaya devam eder. Dönüştürme sürecinin başarıyla tamamlanması şu etkilere sahiptir:

-   Dönüştürme kaydının durumu **Hazır** konumundan **Tamamlandı** konumuna ve seçilen her bir maddenin durumu **Kontrol edildi** konumundan **dönüştürüldü** konumuna değiştirilir.
-   Dönüştürülen maddeler için madde modeli grubu, standart maliyet stok modeli içeren yeni bir grubu yansıtacak şekilde değişir.
-   Dönüştürülen maddeler için standart maliyetler, ayrılmış maliyetlendirme versiyonu içinde etkinleştirilir.
-   Maliyetlendirme versiyonunun maliyetlendirme tipi **Dönüştürme** konumundan **Standart maliyet** konumuna değiştirilir ve maliyetlendirme sürümü artık standart maliyetler için diğer maliyetlendirme sürümleri gibi işlev görür.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Dönüştürülen maddeler için stok değerlerinin doğrulamasını ve mutabakatını yapın
**Fark analiz bildirimi** raporu, yeniden değerleme farkını analiz etmenize olanak tanırken, **Stok değeri** raporu belirli bir tarihteki stok değerini görüntülemenize izin verir.

-   Yeniden değerleme farklarını analiz edin. Dönüştürülen maddeler için stok yeniden değerleme farklarını görüntülemek üzere **Fark analiz bildirimi** raporunu kullanın. Ayrıca stokla birlikte dönüştürülen maddeler için stok yeniden değerleme hareketlerini görüntülemek üzere **Standart maliyet hareketleri** sayfasını da kullanabilirsiniz.
-   Geçiş başlangıç tarihinden önce stok değerini analiz edin. Dönüştürülen maddeler için stok değerlerini görüntülemek üzere **Stok değeri** raporunu kullanın. Raporun bitiş tarihi için, geçiş başlangıç tarihinden önceki günün tarihini kullanın.
-   Dönüştürme tarihinden önce stok değerini analiz edin. Dönüştürülen maddeler için stok değerlerini görüntülemek üzere **Stok değeri** raporunu kullanın. Raporun bitiş tarihi için, dönüştürme tarihinden önceki günün tarihini kullanın.
-   Dönüştürme tarihindeki stok değerini analiz edin. Dönüştürme tarihi itibariyle stok değerlerini görüntülemek için **Stok değeri** raporunu kullanın. Raporun hem Başlangıç tarihi hem Bitiş tarihi dönüştürme tarihiyle eşleşmelidir. Rapor seçim ölçütleri dönüştürülen maddeleri yansıtmalıdır.
-   Eski tarihli stok hareketlerini analiz edin. Dönüştürmeden sonra girilen eski tarihli stok hareketlerini görüntülemek için **Stok değeri** raporunu kullanın. Rapor için "Başlangıç tarihi ve bitiş tarihi, bunlar başlangıç tarihine ve dönüştürme tarihine (eksi bir gün) karşılık gelmelidir. Rapor seçim ölçütleri dönüştürülen maddeleri yansıtmalıdır. Bu rapor, geçiş dönemi içinde standart maliyette yapılan stok hareketlerini gösterir.


<a name="additional-resources"></a>Ek kaynaklar
--------

[Standart maliyet dönüştürme için önkoşullar](prerequisites-standard-cost-conversion.md)



