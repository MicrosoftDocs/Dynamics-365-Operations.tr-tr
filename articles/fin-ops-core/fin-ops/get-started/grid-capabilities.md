---
title: Kılavuz yetenekleri
description: Bu makalede, kılavuz denetiminin çeşitli güçlü özellikleri açıklanmaktadır. Bu özelliklere erişebilmek için yeni ızgara özelliğini etkinleştirmeniz gerekir.
author: jasongre
ms.date: 08/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 096f441d39dde0f322ed117ab35a6a4641a38a93
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405478"
---
# <a name="grid-capabilities"></a>Kılavuz yetenekleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Yeni ızgara denetimi, kullanıcı üretkenliğini artırmak, verilerinizin daha ilginç görünümlerini elde etmek ve verilerinize anlamlı bilgiler yüklemek için kullanılabileceğiniz çeşitli yararlı ve güçlü yetenekler sağlar. Bu makalede aşağıdaki yetenekler ele alınıyor: 

- Hesaplanmış değerleri gösterme 
- Sistemi önceden hazırlama
- Matematik ifadelerini değerlendirme 
- Tablo verilerini gruplandırma (**Kılavuzlarda gruplandırma** özelliği kullanılarak ayrı olarak etkinleştirilir)
- Sütunları dondurma (**Kılavuzlardaki sütunları dondurma** özelliği kullanılarak ayrı olarak etkinleştirilir)
- Otomatik olarak sütun genişliğine sığdır
- Uzatılabilir sütunlar

## <a name="showing-calculated-values"></a>Hesaplanmış değerleri gösterme
Finans ve operasyon uygulamalarında kullanıcılar bir kılavuzdaki her bir sayısal sütun için bir hesaplanmış değeri görüntüleyebilirler. Kılavuzun altındaki alt bilgi bölümü bu hesaplanmış değerleri gösterir.

[![Kılavuzlarda hesaplanmış değerleri gösterme.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

10.0.29'dan önceki sürümlerde toplam, desteklenen tek hesaplanmış değerdir. Ancak 10.0.29 sürümden sonra kullanıcılar, **Genişletilmiş kılavuz toplam yetenekleri** özelliğini etkinleştirdikten sonra, aşağıdaki dört hesaplanmış değer arasından seçim yapabilirler:

- Minimum
- Maksimum
- Toplam
- Ortalama

Tek bir sütun, yalnızca bir hesaplanmış değer türü gösterebilir. Ancak kılavuzdaki her sütun, farklı bir hesaplanmış değer türü gösterecek şekilde yapılandırılabilir.

### <a name="showing-the-grid-footer"></a>Kılavuz alt bilgisini gösterme
Finans ve operasyon uygulamalarda her sekmeli kılavuzun altında altbilgi alanı vardır. Altbilgi, kılavuzda görülen verilerle ilgili değerli bilgileri gösterebilir. Aşağıda bu bilgilerin örnekleri verilmiştir:

- Tablodaki seçili satır sayısı (birden fazla kayıt seçtiğinizde)
- Yapılandırılan sayısal sütunların en altındaki hesaplanmış değerler (örneğin, genel toplamlar)
- Veri kümesindeki satır sayısı 

Bu altbilgi varsayılan olarak gizlidir ancak açabilirsiniz. Bir kılavuzun alt bilgisini göstermek için, kılavuz başlığında **Kılavuz seçenekleri** düğmesini seçin ve **Alt bilgiyi göster** seçeneğini belirleyin. Belirli bir ızgara için alt bilgiyi açtıktan sonra, kullanıcı alt bilgiyi gizlemeyi seçene kadar bu ayar hatırlanır. Alt bilgiyi gizlemek için **Kılavuz seçenekleri** menüsünde **Alt bilgiyi gizle**'yi seçin.

### <a name="specifying-columns-with-calculated-values"></a>Hesaplanmış değerleri olan sütunları belirtme
Şu anda hiçbir sütun varsayılan olarak hesaplanmış değerleri göstermez. Bunun yerine kurulum, kılavuzlardaki sütunların genişliklerini ayarlamaya benzer şekilde bir kerelik etkinlik olarak değerlendirilir. Bir sütunun hesaplanmış bir değerini görmek istediğinizi belirttikten sonra, sayfayı bir sonraki ziyaretinizde bu ayar hatırlanır.

Bir sütunu hesaplanmış değeri gösterecek şekilde yapılandırmanın iki yolu vardır:

- Hesaplanmış değerini görüntülemek istediğiniz sütunu seçin ve basılı tutun (veya sağ tıklayın). **Genişletilmiş kılavuz toplam yetenekleri** özelliği etkinse, **Sütun toplamlarını görüntüle**'yi seçin ve sonra istediğiniz hesaplanmış değeri seçin. Bu özellik etkinleştirilmemişse, **Bu sütunun toplamını al**'ı seçin. Bu eylem üç olayın oluşmasına neden olur:

    1. Kılavuz altbilgisi görünür hale gelir. 
    2. Sütunun hesaplanmış değerini görüntüleme tercihiniz kaydedilir. 
    3. Bu sütun ve hesaplanmış değerlerini göstermek üzere daha önce yapılandırdığınız diğer sütunlar için istenen hesaplama başlatılır. Hesaplanmış değerleri göstermek için gerekli olan zaman, veri kümesinin boyutuna bağlıdır.

- Altbilgi görünür olduktan sonra, hesaplanmış bir değerini görüntülemek istediğiniz sütunun en altındaki altbilgi alanında, **Toplamı göster** (veya **Genişletilmiş kılavuz toplam yetenekleri** özelliği etkinse, **Hesaplanan değeri seç**) seçeneğini belirleyin. Yapılandırılmış sütun yoksa, bu düğme tüm sayısal sütunlardaki altbilgide görünür.

    Hesaplanmış bir değeri göstermek için en az bir sütun yapılandırıldıktan sonra, **Toplamı göster** (veya **Hesaplanan değeri seç**) düğmesi yalnızca üzerine gelindiği veya odaklanıldığı zaman ortaya çıkacaktır. Düğmeyi seçme eylemi, yalnızca sütundaki bir hesaplanmış değeri görmek için tercihlerinizi kaydeder; böylece, daha sonra sayfaya yapılan ziyaretler sırasında söz konusu tercih uygulanır. Altbilgide, bu durum sütunda görünen bir çizgiyle belirtilir. (Veri kümesi yeterince küçükse hesaplanan değerin hemen görüneceğini unutmayın.)

Bir hata yaptıysanız ve artık belirli bir sütundaki hesaplanmış değeri görüntülemek istemiyorsanız, sütunu seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Toplamı gizle** (veya **Genişletilmiş kılavuz toplam yetenekleri** özelliği etkinse **Sütun toplamlarını görüntüle \> Hiçbiri**) seçeneğini belirleyin. Alternatif olarak, o sütundaki altbilgide **Toplamı gizle** (veya **Hesaplanan değeri gizle**) seçeneğini belirleyin. Bu tercih, sayfaya ileride yapılacak ziyaretler için de kaydedilecektir. 

### <a name="calculating-aggregate-values"></a>Toplam değerleri hesaplama
Altbilginin görünür olduğu ve sütunların önceden hesaplanan değerleri gösterecek şekilde yapılandırıldığı bir sayfaya gittiğinizde, bu değerler altbilgide gösterilmeyebilir. Bu davranış sayfadaki veri kümesinin boyutuna bağlıdır. Veri kümesi yeterince küçükse, hesaplanmış değerler veri kümesindeki satır sayısıyla birlikte otomatik olarak gösterilecektir. Yapılandırdığınız sütunların altındaki alt bilgide tireler varsa, veri kümesi sistemin hesaplanmış değerleri hemen gösteremeyeceği kadar büyüktür. Bu durumda, değerleri hesaplamak için açık bir eylem gereklidir. Değerleri hesaplamak için altbilgide **Hesapla** düğmesini seçin. Alternatif olarak, toplamını görmek istediğiniz sütunu seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Bu sütunun toplamını al** seçeneğini (veya **Genişletilmiş kılavuz toplam yetenekleri** özelliği etkinse **Sütun toplamlarını görüntüle**'yi ve sonra istenen hesaplanmış değeri) seçin.

Hesaplamanın tamamlanması çok uzun sürüyorsa, **İptal**'i seçerek işlemi istediğiniz iptal edebilirsiniz. Bazı durumlarda veri kümesi, toplam değerlerini hesaplayamayacak kadar büyük olur (kuruluşunuz tarafından uygulanan bir sınır). Bu durumda, bunun yerine verilerinize daha fazla filtre uygulamanız istenir.

> [!NOTE]
> Sistem yöneticileri, **İstemci performans seçenekleri** sayfasındaki her bir **Kılavuz parametresi için en fazla yerel kayıt sayısı** parametresini ayarlayarak, toplamları hesaplamak için kullanılabilen kayıt sayısı sınırını değiştirebilir. Varsayılan değer 25.000 kayıttır. Yöneticiler bu değeri ayarlarken dikkatli olmalıdır çünkü büyük bir değer kullanıcının makinesindeki kullanılabilir belleği tüketebilir. Değerin 50.000 kaydı aşmamanızı öneririz.

Siz veri kümesinde satır güncelleştirme, silme veya oluşturma işlemleri yaptıkça hesaplanmış değerler otomatik olarak güncelleştirilir.

## <a name="typing-ahead-of-the-system"></a>Sistemi önceden hazırlama
Birçok iş senaryosunda, sisteme verileri hızlı şekilde girebilme çok önemlidir. Yeni kılavuz denetimi tanıtılmadan önce, kullanıcılar yalnızca geçerli satırdaki verileri değiştirebiliyordu. Bu nedenle, bir satırda değişiklikler yaptıktan sonra kullanıcılar, sistem geçerli satırdaki değişiklikleri başarılı bir şekilde doğrulayana ve yeni bir satırın oluşturulmasıyla ilişkili tüm mantığı çalıştırana (satır oluşturulması durumunda) kadar başka bir satıra geçiş yapamayabilir veya yeni bir satır oluşturamayabilir. Kullanıcıların bu işlemlerin tamamlanmasını beklediği süreyi azaltmaya ve kullanıcı üretkenliğini artırmaya yardımcı olmak için, yeni kılavuz bu işlemleri zaman uyumsuz olacak şekilde ayarlar. Kullanıcılar önceki satır doğrulamaları ve satır oluşturma mantığı beklenirken değişiklik yapmak için yeni satırlar oluşturabilir veya diğer satırlara geçebilir. 

[![Sistemden önce yazma.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Bu yeni davranışı desteklemek için, satır seçim sütunu düzenleme modundayken, satır durumu için yeni bir sütun kılavuzun en sağına eklenir. Bu sütun aşağıdaki durumlardan birini gösterir:

- **Boş** – Herhangi bir durum görüntüsü satırın sistem tarafından başarıyla kaydedildiğini göstermez.
- **İşlem beklemede** – Bu durum, satırdaki değişikliklerin sunucu tarafından henüz kaydedilmediğini, ancak işlenmesi gereken değişiklikler sırasında olduğunu gösterir. Kılavuzun dışında bir eylem gerçekleştirmeden önce, bekleyen tüm değişikliklerin işlenmesi için beklemeniz gerekir. Ek olarak, bu satırlardaki metinler, satırların kaydedilmemiş durumunu gösterecek şekilde italik yapılır. 
- **Geçersiz durum** – Bu durum, satırın işlenmesi sırasında bazı uyarı veya iletinin tetiklenmesini ve sistemin bu satırdaki değişiklikleri kaydetmesini engellemiş olabileceğini gösterir. Eski kılavuzda, kaydetme işlemi başarısızsa sorunu hemen düzeltmek için satıra geri dönmeniz gerekiyordu. Ancak, yeni kılavuzda bir doğrulama sorunuyla karşılaşıldığı size bildirilir, ancak satırdaki sorunları ne zaman düzeltmek istediğinize karar verebilirsiniz. Sorunu düzeltmeye hazır olduğunuzda, odağı yeniden el ile satıra taşıyabilirsiniz. Alternatif olarak, **Bu sorunu düzelt** eylemini seçebilirsiniz. Bu eylem, odağı hemen sorunun bulunduğu satıra geri taşır ve kılavuzun içinde veya dışında düzenlemeler yapmanıza olanak sağlar. Bu doğrulama uyarısı giderilene kadar sonraki bekleyen satırların işlenmesinin durdurulduğunu unutmayın. 
- **Duraklatıldı** – Bu durum, bir satırın doğrulanması kullanıcı girişi gerektiren bir açılan iletişim kutusunu tetiklediği için işlemin sunucu tarafından duraklatıldığını belirtir. Kullanıcı başka bir satıra veri giriyor olabileceğinden açılır iletişim kutusu o kullanıcıya hemen sunulmayacaktır. Bunun yerine, kullanıcı işlemeyi sürdürmeyi seçtiğinde gösterilecektir. Bu durum, kullanıcıyı durumla ilgili bilgilendiren bir bildirimle birlikte gösterilir. Bildirim, açılır iletişim kutusunu tetikleyecek bir **İşlemeyi sürdür** eylemi içerir.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Sistemden önce veri girerken farklılıklar
Sistemin işlediği yerden önce veri girdiğinizde, veri giriş deneyiminde birkaç değişiklik bekleyebilirsiniz:

- Arama açılan listeleri olmadığını, aynı satırdaki farklı bir sütuna geçtiğinizde alan değerlerinin doğrulanmadığını ve sütunların başlangıçta varsayılan değerleri göstermediğini göreceksiniz. Bu davranış, sistemden önce oluşturma veya güncelleştirme yapmanız sırasında oluşur. Ancak sistem, şu anda düzenlemekte olduğunuz yere yetiştiğinde standart deneyim devam ettirilecektir. Genellikle varsayılan bir değer alan bir alanda değişiklik yaptıysanız, yaptığınız değişiklikler sunucu satırı işlemeye başladığında varsayılan alan değerini geçersiz kılar.
- **Aşağı ok** tuşunu kullanarak yeni bir satır oluşturursanız, kılavuzdaki tüm sütunlar düzenlenebilir olarak görünür. Varsayılan olarak, odak yeni satırdaki ilk sütuna kayar. Bu sütun, eski kılavuzda ilk odağı alan sütunla veya **Yeni** düğmesini seçtikten sonra odağı alan sütunla aynı olmayabilir. Kuruluşunuz sistemi özelleştirebilir ve **Aşağı ok** tuşu seçildiğinde ilk odağı alan sütunu değiştirebilir. Daha fazla bilgi için [Aşağı ok tuşu kullanılarak yeni satırlar oluşturulurken ilk odağı alan sütunu belirtme](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key) bölümüne bakın. Ne olursa olsun, her bir kılavuzu veri girişi için en iyi duruma getirmek amacıyla kişiselleştirmeyi kullanabilirsiniz. Özellikle, alanları yeniden sıralayabilirsiniz böylece ilk sütun, içine veri girmek için başlatmak istediğiniz sütun olur. Ayrıca, sekme duraklarını azaltmak ve bu görünümde veri girişi için gerekli olmayan alanları gizlemek amacıyla, veri girişi için genel olarak alanları yeniden sıralamak isteyebilirsiniz.

### <a name="pasting-from-excel"></a>Excel'den yapıştırma
Kullanıcılar her zaman finans ve operasyon uygulamalarındaki kılavuzlardan Microsoft Excel'e **Excel'e aktar** mekanizmasını kullanarak veri aktarabiliyordu. Ancak, sistemden önce veri girebilme özelliği, yeni kılavuzun Excel'den tablo kopyalanmasına ve onları finans ve operasyon uygulamalarında doğrudan ızgaralara yapıştırmasına olanak tanır. Yapıştırma işleminin başlatıldığı kılavuz hücresi kopyalanan tablonun nereye yapıştırılacağını belirler. Şu iki durum dışında, kılavuzun içeriği üzerine kopyalanan tablonun içeriği yazılır:

- Kopyalanan tablodaki sütun sayısı, yapıştırma konumundan başlayarak kılavuzda kalan sütun sayısını aşarsa, kullanıcıya ek sütunların yok sayıldığı bildirilir. 
- Kopyalanan tablodaki satır sayısı, yapıştırma konumundan başlayarak kılavuzdaki satır sayısını aşarsa, yapıştırılan içerik için varolan hücrelerin üzerine yazılır ve kopyalanan tablodaki tüm ek satırlar kılavuzun en altına yeni satırlar olarak eklenir. 

## <a name="evaluating-math-expressions"></a>Matematik ifadelerini değerlendirme
Verimlilik rampa olarak, kullanıcılar bir kılavuzdaki sayısal hücrelere matematiksel formüller girebilecek. Bu kullanıcılar, sistem dışındaki bir uygulamada hesaplama yapmaları gerekmez. Örneğin **= 15\*4** girerseniz ve alanın dışına gitmek için **sekme** tuşuna basarsanız, sistem ifadeyi değerlendirir ve alan için **60** değerini kaydeder.

[![Matematik ifadelerini değerlendirme.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Sistemin bir değeri ifade olarak tanımasını sağlamak için, değeri bir eşittir işaretiyle (**=**) başlatın. Desteklenen işleçler ve söz dizimi hakkında daha fazla bilgi edinmek için bkz. [Desteklenen matematik simgeleri](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Sürüm 10.0.29 itibariyle, sayısal denetimlerde matematiksel ifadeleri değerlendirme özelliği artık kılavuzun dışında da kullanılabilir.

## <a name="grouping-tabular-data"></a>Sekmeli verileri gruplandırma
İş kullanıcılarının sıklıkla anlık olarak veri analizi yapmaları gerekir. Bu analiz Microsoft Excel'e veri aktararak ve özet tabloları kullanarak yapılabilse de yeni kılavuz denetim özelliğine bağlı olan **Kılavuzlarda gruplandırma** özelliği sayesinde kullanıcılar, tablosal verilerini finans ve operasyon uygulamalarında ilginç yollarla organize edebilirler. Bu özellik **Hesaplanmış değerler** özelliğini genişlettiği için, **Gruplandırma** da grup düzeyinde hesaplanmış değerler (örneğin, alt toplamlar) sunarak verilere dair anlamlı bilgiler edinmenize olanak sağlar.

[![Kılavuzdaki verileri gruplandırma.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Bu özelliği kullanmak için, gruplandırmada kullanmak istediğiniz sütuna sağ tıklayın ve **Bu sütuna göre gruplandır**'ı seçin. Bu eylem, verileri, seçilen sütuna göre sıralar, kılavuzun başına yeni bir **Gruplandırma ölçütü** sütunu ve her grubun başına "üst bilgi satırları" ekler. Bu üst bilgi satırları her grup hakkında aşağıdaki bilgileri sağlar:

- Grubun veri değeri 
- Sütun adı (bu bilgi özellikle birden çok gruplandırma düzeyine sahip olduğunuzda yararlıdır)
- Bu gruptaki veri satırlarının sayısı
- Yapılandırılmış herhangi bir sütun (örneğin, sütun bir toplamı gösterecek şekilde yapılandırılmışsa alt toplamlar) için hesaplanan değerler

[Kaydedilmiş görünümler](saved-views.md) etkinken, sorguların görünümlere kaydedilmesine izin veren sayfalardaki görünümün bir parçası olarak gruplandırmayı kaydedebilirsiniz. Örneğin, büyük görünüm seçicileri olanlar. Daha fazla bilgi için [Görünümler arasında değiştirme](saved-views.md#switching-between-views) bölümüne bakın. 

### <a name="multiple-levels-of-grouping"></a>Birden çok gruplandırma düzeyi
Verileri tek bir sütuna göre gruplandırdıktan sonra, istediğiniz sütunda **Bu sütuna göre gruplandır**'ı seçerek verileri farklı bir sütuna göre gruplandırabilirsiniz. Bu işlem, iç içe geçmiş 5 gruplandırma düzeyine sahip oluncaya kadar tekrarlanabilir. Bu, desteklenen derinlik üst sınırıdır. Bu aşamada, ek sütunlara göre gruplandırma yapamazsınız.

Dilediğiniz zaman, bir sütuna sağ tıklayıp **Grubu Çöz**'ü seçerek söz konusu sütundaki gruplandırmayı kaldırabilirsiniz. Ayrıca, **Izgara seçenekleri**'ni ve ardından **Tümünün grubunu çöz**'ü seçerek tüm sütunlardaki gruplandırmayı kaldırabilirsiniz.

### <a name="sorting-grouped-data"></a>Gruplanmış verileri sıralama
Verileri bir veya daha fazla sütuna göre gruplandırma yaptıktan sonra, ilgili sütun başlığı üzerinden herhangi bir gruplandırma sütununun sıralama yönünü değiştirebilirsiniz. 

Gruplandırılmamış bir sütunda sıralama yaparsanız, gruplandırma değişmeden kalır. Veriler, seçilen sütuna göre her bir grubun içinde sıralanır.

### <a name="expanding-and-collapsing-groups"></a>Grupları genişletme ve daraltma
Verilerin ilk gruplandırmasında tüm gruplar genişletilmiş olacaktır. Tek grupları daraltarak verilerin özetlenmiş görünümlerini oluşturabilir veya verilerde gezinmeye yardımcı olması için grup genişletme ve daraltma özelliklerini kullanabilirsiniz. Bir grubu genişletmek veya daraltmak için, ilgili grup üst bilgisi satırında çift ayraç (>) düğmesini seçin. Bireysel grupların genişletme/daraltma durumunun kişiselleştirme bölümünde **kaydedilmeyeceğini** unutmayın.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Grup düzeyinde satır seçme ve seçimi kaldırma
Kılavuzdaki ilk sütunun en üstündeki onay kutusunu seçerek kılavuzdaki tüm satırları seçmeniz (veya seçimini kaldırmanız) için, ilgili grup üst bilgi satırındaki onay kutusunu seçerek bir gruptaki tüm satırları hızlıca seçebilir (veya seçimini kaldırırsınız). Grup üst bilgi satırındaki onay kutusu, tüm satırlar seçili, hiçbir satır seçilmemiş veya yalnızca bazıları seçili olsa bile, bu gruptaki satırların geçerli seçim durumunu her zaman yansıtır.

### <a name="hiding-column-names"></a>Sütun adlarını gizleme
Veriler gruplandırılırken, varsayılan davranış sütun adını grup başlık satırında göstermektir. **Izgara seçenekleri** > **Grup sütun adını gizle** seçeneğini belirleyerek grup üst bilgisi satırlarında sütun adını gizlemeyi seçebilirsiniz.

### <a name="grouping-on-date-and-time-columns"></a>Tarih ve saat sütunlarında gruplandırma
Tarih veya Tarih Saat alanlarında gruplandırma yaptığınızda, yıla, aya veya güne göre gruplama seçeneğine sahip olursunuz. İlgili başlık satırı içindeki "değer" grubu, o alandaki biçimle eşleşir. Ayrıca, Tarih Saat ve Saat alanları için saat, dakika veya saniyeye göre gruplayabilirsiniz.

> [!IMPORTANT]
> Kullanıcılar şu anda bir tarih veya saat sütunundaki bir segmentte gruplandırma yaptıktan sonra gruplandırma sütunu ekleyemez.

## <a name="freezing-columns"></a>Sütunları dondurma
Izgaradaki bazı sütunlar, bağlam açısından görünümün dışında kalmalarını istemeyeceğiniz kadar önemli olabilir. Bunun yerine, bu sütunlardaki değerlerin her zaman görünür olmasını isteyebilirsiniz. **Kılavuzdaki sütunları dondurma** özelliği kullanıcılara bu esnekliği sağlar. 

[![Kılavuzdaki sütunları dondurma.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Bir sütunu dondurmak için sütunun üst bilgisine sağ tıklayın ve **Sütunu dondur**'u seçin. Bu adımı ilk kez tamamladığınızda, seçili sütun ilk sütun olur ve artık görünümden kaymaz. Dondurulan sonraki sütunlar son dondurulmuş sütunun sağına eklenir. Dondurulmuş sütunları gereken şekilde yeniden sıralamak için standart taşıma işlevini kullanabilirsiniz. Ancak, dondurulmuş sütunlar, dondurulmamış sütunlar kümesi arasında görünecek şekilde taşınamaz. Benzer şekilde, dondurulmamış sütunlar, dondurulmuş sütunlar kümesi arasında görünecek şekilde taşınamaz.

Bir sütunu çözmek için donmuş sütunun üst bilgisine sağ tıklayın ve **Sütunu çöz**'ü seçin. 

Yeni ızgaradaki satır seçimi ve satır durumu sütunlarının, her zaman ilk iki sütun olarak dondurulduğunu unutmayın. Bu nedenle, bu sütunlar bir ızgaraya dahil edildiğinde, kılavuzdaki yatay kaydırma konumundan bağımsız olarak her zaman kullanıcılar tarafından görülecektir. Bu iki sütun yeniden sıralanamaz.

## <a name="autofit-column-width"></a>Otomatik olarak sütun genişliğine sığdır
Excel'de olduğu gibi kullanıcılar, bir sütunu sütun içinde o anda gösterilen içeriğe göre otomatik olarak yeniden boyutlandırılmaya zorlayabilir. Yalnızca sütunda boyutlandırma tutamaçlarına iki kez dokunmanız (veya çift tıklatmanız) yeterlidir. Alternatif olarak, odağı sütun başlığına yerleştirip **A** tuşunu (otomatik sığdırma için) seçebilirsiniz.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Yeni kılavuz denetimini ortamımda nasıl etkinleştirebilirim? 

**Yeni kılavuz denetimi** özelliği, herhangi bir ortamda doğrudan Özellik yönetiminde kullanılabilir. Özellik yönetiminde özelliği etkinleştirdikten sonra, sonraki tüm kullanıcı oturumları yeni ızgara denetimini kullanır. 

Bu özellik 10.0.21 sürümünde varsayılan olarak etkinleştirilmeye başlanmıştır. 2022 Ekim'de zorunlu hale gelmesi hedeflenmiştir.

## <a name="developer-topics"></a>Geliştirici konuları

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Geliştirici] Ayrı sayfalar için yeni ızgarayı kullanmayı devre dışı bırakma 
Kuruluşunuz yeni kılavuzla ilgili bazı sorunlar içeren bir sayfayı saptadığı zaman, tek bir formun, sistemin geri kalanında yeni kılavuz denetimiyle yararlanmaya devam ederken, eski kılavuz denetimini kullanmasına izin veren bir API kullanılabilir. Ayrı bir sayfayı yeni kılavuzdan geri çevirmek için forma ait `run()` yöntemine aşağıdaki `super()` çağrı gönderisini ekleyin.

```this.forceLegacyGrid();```

Bu API, eski kılavuz denetiminin kaldırılmasına izin vermek için kullanım dışı kalacaktır. Ancak, kullanım dışı bırakma duyurusu yapıldıktan sonra en az 12 ay kullanılabilir durumda kalacaktır. Herhangi bir sorun bu API'nin kullanılmasını gerektiriyorsa, bunları Microsoft'a bildirin.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Daha önce ızgarayı devre dışı bıraktıktan sonra bir sayfayı yeni ızgarayı kullanmaya zorlama
Yeni ızgaranın tek bir sayfada kullanılmamasını seçtiyseniz ilgili sorunlar çözüldükten sonra yeni ızgarayı yeniden etkileştirmek isteyebilirsiniz. Bunu yapmak üzere `forceLegacyGrid()` için çağrıyı kaldırmanız gerekir. Değişiklik, aşağıdakilerden biri gerçekleşene kadar etkili olmaz:

- **Ortam yeniden dağıtımı**: Ortam güncelleştirilip yeniden dağıtıldığında yeni ızgaranın devre dışı bırakıldığı sayfaları depolayan tablo (FormControlReactGridState) otomatik olarak temizlenir.
- **Tabloyu el ile temizleme**: Geliştirme senaryoları için FormControlReactGridState tablosunu temizlemek üzere SQL kullanmanız ve ardından AOS'u yeniden başlatmanız gerekir. Bu eylem birleşimi, yeni ızgaranın kullanım dışı bırakıldığı sayfaların önbelleğe alınmasını sıfırlar.

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Geliştirici] Sistemden önce kılavuzları tek tek Yazma'dan çıkarma özelliği
Kılavuzun *Sistemden önce yazma* özelliği ile iyi çalışmayan bazı senaryolar ortaya çıkmıştır. (Örneğin, bir satır doğrulandığında tetiklenen bazı kodlar veri kaynağı araştırmasının tetiklenmesine neden oluyor ve araştırma daha sonra varolan satırlardaki kaydedilmemiş düzenlemeleri bozabiliyor.) Kuruluşunuz böyle bir senaryo keşfederse, geliştiricinin zaman uyumsuz satır doğrulamasından tek bir kılavuzu seçmesine ve eski davranışa geri dönmesine olanak sağlayan bir API kullanılabilir.

Bir kılavuzda zaman uyumsuz satır doğrulaması devre dışı bırakıldığında, geçerli satırda doğrulama sorunları varken kullanıcılar yeni bir satır oluşturamaz veya kılavuzda varolan farklı bir satıra geçemez. Bu eylemin bir yan etkisi olarak, tablolar Excel'den finans ve operasyon kılavuzlarına yapıştırılamaz.

Tek bir kılavuzu zaman uyumsuz satır doğrulamasının dışında tutmak için formun `run()` yönteminde `super()` sonrasında aşağıdaki çağrıyı ekleyin.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Bu çağrı yalnızca istisnai durumlarda çağrılmalıdır ve tüm kılavuzlar için standart olmamalıdır.
> - Form yüklendikten sonra çalışma zamanında bu API'ye geçiş yapmanızı önermiyoruz.

### <a name="developer-size-to-available-width-columns"></a>[Geliştirici] Boyutlandırılabilir sütunlar
Bir geliştirici yeni kılavuzun içindeki sütunlar için **WidthMode** özelliğini **SizeToAvailable** olarak ayarladığında, bu sütunlar, özelliğin **SizeToContent** olarak ayarlanmış olması durumunda, ilk başta sahip olacakları aynı genişliğe sahip olurlar. Ancak, kılavuzun içinde kullanılabilen ek bir genişliği kullanmak için genişler. Özellik birden çok sütun için **SizeToAvailable** olarak ayarlandıysa, tüm bu sütunlar kılavuzun içinde kullanılabilir olan ek bir genişliği paylaşır. Ancak, bir kullanıcı bu sütunlardan birini el ile yeniden boyutlandırırsa, sütun statik hale gelir. Bu genişlikte kalacak ve artık fazladan kullanılabilir kılavuz genişliği kaplamayacak şekilde genişlemeyecek.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Geliştirici] Aşağı ok tuşu kullanılarak yeni satırlar oluşturulurken ilk odağı alan sütunu belirtme
[Sistemden önce veri girerken farklılıklar](#differences-when-entering-data-ahead-of-the-system) konusunda ele alındığı gibi, "Sistemden önce yazma" özelliği etkinse ve bir kullanıcı **Aşağı ok** tuşunu kullanarak yeni bir satır oluşturursa varsayılan davranış, odağı yeni satırdaki ilk sütuna almaktır. Bu deneyim eski kılavuzdaki deneyimden veya **Yeni** düğmesi seçildiğindeki deneyimden farklılık gösterebilir.

Kullanıcılar ve kuruluşlar veri girişi için en iyi duruma getirilmiş, kaydedilmiş görünümler oluşturabilir. (Örneğin, ilk sütunun veri girmeye başlamak istediğiniz ilk sütun olması için sütunları yeniden sıralayabilirsiniz.) Ek olarak, sürüm 10.0.29 itibariyle kuruluşlar, **selectedControlOnCreate()** yöntemini kullanarak bu davranışı ayarlayabilir. Bu yöntem, **Aşağı ok** tuşu kullanılarak yeni bir satır oluşturulurken geliştiricilerin ilk odağı alacak sütunu belirtmesine olanak tanır. Giriş olarak bu API, ilk odağı alması gereken sütuna karşılık gelen denetim kimliğini alır.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Geliştirici] React olmayan genişletilebilir kontrollerle kılavuzları işleme
Bir kılavuz yüklenirken sistem, React olmayan bir genişletilebilir denetimle karşılaşırsa, bunun yerine eski kılavuzu işlemeye zorlayacaktır. Bir kullanıcı bu durumla ilk kez karşılaştığında, sayfanın yenilenmesi gerektiğini belirten bir ileti gösterilecektir. Daha sonra bu sayfa, bir sonraki sistem güncelleştirmesine kadar kullanıcılara daha fazla bildirim vermeden eski kılavuzu otomatik olarak yükler. 

Bu durumu kalıcı olarak çözmek için, genişletilebilir denetim yazarları, kılavuzda kullanılmak üzere denetimin bir React sürümünü oluşturabilir.  Denetime ilişkin X++ sınıfı, geliştirildikten sonra, bu denetim için yüklenecek React paket konumunu belirtmek için **FormReactControlAttribute** özniteliğiyle donatılabilir. Örnek olarak `SegmentedEntryControl` sınıfına bakın.  

## <a name="known-issues"></a>Bilinen sorunlar
Bu bölüm, yeni ızgara denetimiyle ilgili bilinen sorunların listesini içerir.

### <a name="open-issues"></a>Açık sorunlar
- **Yeni kılavuz denetimi** özelliğini etkinleştirdikten sonra, bazı sayfalar varolan kılavuz denetimini kullanmaya devam eder. Bu, aşağıdaki durumlarda ortaya çıkar:
 
    - [Çözüldü] Çoklu sütunlar halinde işlenen sayfada bir kart listesi vardır.
        - Bu tür bir kart listesi 10.0.30 sürümünden başlayarak **Yeni kılavuz denetimi** tarafından desteklenir. forceLegacyGrid() öğesinin bu amaçla tüm kullanımları kaldırılabilir. 
    - [Çözüldü] Sayfada gruplanmış bir kart listesi vardır.
        - Gruplanmış kart listeleri 10.0.30 sürümünden başlayarak **Yeni kılavuz denetimi** tarafından desteklenir. forceLegacyGrid() öğesinin bu amaçla tüm kullanımları kaldırılabilir. 
    - [Çözüldü] React olmayan genişletilebilir bir denetimi olan kılavuz sütunu.
        - Genişletilebilir denetimler, ilgili denetimin kılavuza yerleştirildiğinde yüklenecek olan bir React sürümünü sağlayabilir ve kılavuzda kullanıldığı zaman bu denetimi yükleyecek şekilde denetim tanımını ayarlayabilir. Daha ayrıntılı bilgi için ilgili geliştirici bölümüne bakın. 

    Bir kullanıcı bu durumlardan biriyle karşılaştığında, sayfayı yenileme hakkında bir ileti görüntülenecektir. Bu ileti görüntülendikten sonra, bir sonraki ürün sürümü güncelleştirilinceye kadar, sayfa tüm kullanıcılar için varolan kılavuzla çalışmaya devam eder. Yeni kılavuzun kullanılabilmesi amacıyla gelecekteki bir güncelleştirme için bu senaryoların daha iyi işlenmesi dikkate alınacaktır.

- [BB 4582758] Yakınlaştırmayı 100'den başka bir yüzdeye değiştirdiğinizde kayıtlar bulanıklaşır

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

