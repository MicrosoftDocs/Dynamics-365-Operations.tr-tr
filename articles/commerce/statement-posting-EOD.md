---
title: Ekstre deftere nakil işlevi geliştirmeleri
description: Bu konu ekstre deftere nakli özelliğinde yapılan geliştirmeleri tanımlar.
author: josaw1
manager: AnnBe
ms.date: 05/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 68abef8f28c04a4f6f88e638c8abf944d06a32c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416497"
---
# <a name="improvements-to-statement-posting-functionality"></a>Ekstre deftere nakil işlevi geliştirmeleri

[!include [banner](includes/banner.md)]

Bu konu ekstre deftere nakli özelliğinde yapılan ilk geliştirme kümesini açıklar. Bu iyileştirmeler Microsoft Dynamics 365 for Finance and Operations 7.3.2 içinde kullanılabilirdir.

## <a name="activation"></a>Etkinleştirme

Varsayılan olarak, Finance and Operations 7.3.2 dağıtımı sırasında program eski ekstre deftere nakil özelliğini kullanacak şekilde ayarlanır. Geliştirilmiş ekstre deftere nakil özelliğini etkinleştirmek için buna ilişkin yapılandırma anahtarını etkinleştirmeniz gerekir.

- **Sistem Yönetimi** \> **Kurulum** \> **Lisans yapılandırması**'na gidin ve daha sonra **Perakende ve Ticaret** düğümü altından **Ekstreler (eski)** onay kutusunun seçimini kaldırın ve **Ekstreler** onay kutusunu işaretleyin.

Yeni **Ekstreleri** yapılandırma anahtarı etkinleştirildiğinde, **Ekstreleri** adındaki yeni menü kullanılabilir olur. Bu menü öğesi ekstreleri el ile oluşturmanızı, hesaplamanızı ve deftere nakletmenizi sağlar. Toplu olarak deftere nakletme işlemi kullanıldığında hataya neden olan bir ekstre de bu menü öğesi ile kullanılabilir olacaktır. (**Ekstreleri (eski)** yapılandırma anahtarı etkinleştirildiğinde, menü öğesi adı **Açık ekstreler** olur.)

Commerce bu yapılandırma anahtarlarıyla ilgili aşağıdaki doğrulamaları içerir:

- İki yapılandırma anahtarı aynı anda açılamaz.
- Yaşam döngüsü süresince belirli bir ekstrede gerçekleştirilen tüm işlemler için aynı yapılandırma anahtarı kullanılmalıdır (Oluştur, Hesapla, Sil, Deftere naklet, vb.). Örneğin, **Ekstre (eski)** yapılandırma anahtarı açık olduğunda bir ekstreyi oluşturduktan ve hesapladıktan sonra aynı ekstreyi **Ekstre** yapılandırma anahtarını etkinleştirerek deftere nakledemezsiniz.

> [!NOTE]
> **Ekstre (eski)** yapılandırma anahtarını kullanmanızı zorunlu kılan nedenler yoksa gelişmiş ekstre deftere nakil özelliği için **Ekstre** yapılandırma anahtarını kullanmanızı öneririz. Microsoft yeni ve geliştirilmiş ekstre deftere nakil özelliğine yatırım yapmaya devam edecektir ve bundan yararlanmak için en kısa sürede buna geçmeniz önemlidir. Eski ekstre deftere nakli özelliği 8.0 sürümü itibarıyla kullanım dışı bırakılmıştır.

## <a name="setup"></a>Ayarlama

Ekstre deftere nakli özelliğinde yapılan geliştirmelerin bir parçası olarak, **Ticaret parametreleri** sayfasının **Deftere nakil** sekmesindeki **Ekstre** hızlı sekmesinde üç yeni parametre bulunmaktadır:

- **Ekstre içeriğini sil işlevini devre dışı bırak** – Bu seçenek yalnızca eski ekstre deftere nakil özelliği için kullanılır. Kullanıcıların yarı deftere nakledilmiş durumdaki ekstreleri silmelerini önlemek için bu seçeneği **Hayır** olarak ayarlamanızı öneririz. Yarı deftere nakledilmiş durumdaki ekstrelerin içeriği silinirse, veriler bozulur. Bu seçeneği yalnızca özel durumlar için **Evet** olarak ayarlamanız gerekir.
- **Hesaplama sırasında stoğu rezerve et** – Stok rezervasyonu için **Stok deftere nakil** toplu işini kullanmanızı ve bu seçeneği **Hayır** olarak ayarlamanızı öneririz. Bu seçenek **Hayır** olarak ayarlandığında, gelişmiş ekstre deftere nakil özelliği hesaplama sırasında stok rezervasyon girişleri oluşturmaya çalışmaz (girişler daha önceden **Stok deftere nakil** toplu işlemi aracılığıyla ayarlanmadıysa). Bunun yerine, özellik stok rezervasyon girişlerini yalnızca deftere nakil sırasında oluşturur. Bu uygulama bir tasarım seçimiydi ve hesaplama işlemi ile deftere nakil işlemi arasındaki zaman aralığının tipik olarak kısa olması olgusunu temel almaktaydı. Bununla birlikte, stoğu hesaplama sırasında rezerve etmek istiyorsanız, bu seçeneği **Evet** olarak ayarlayabilirsiniz.

    Eski ekstre deftere nakli özelliği, bu seçeneğin ayarının ne olduğuna bakılmaksızın, stoğu daima ekstre hesaplama işlemi sırasında rezerve eder (rezervasyonun daha önce **Stok deftere nakil** toplu işlemi aracılığıyla yapılmamış olması durumunda).

- **Sayımın devre dışı bırakılması gerekli** – Bu seçenek **Evet** olarak ayarlandığında, sayılan tutar ile hareket tutarı arasındaki fark mağazaları için **Ekstre** hızlı sekmesinde belirtilen eşiğin dışında olsa bile ekstre deftere nakil işlemi devam eder.

Ek olarak, aşağıdaki parametreler **Ticaret parametleri** sayfasının **Deftere nakil** sekmesindeki **Toplu işleme** hızlı sekmesinde kullanıma sunulmuştur: 

- **Paralel ekstre deftere nakil maksimum sayısı** - Bu alan, çoklu ekstreleri deftere nakletmek için kullanılacak toplu iş görevlerini tanımlar. 
- **Ekstre başına sipariş işleme için maksimum iş parçacığı** - Bu alan, tek bir ekstre için satış siparişleri oluşturmak ve faturalamak üzere ekstre deftere nakli toplu işi tarafından kullanılan maksimum iş parçacığı sayısını gösterir. Ekstre deftere nakil işlemi tarafından kullanılacak toplam iş parçacığı sayısı, bu parametredeki değer **Paralel ekstre deftere nakil maksimum sayısı** parametresindeki değerle çarpılarak hesaplanır. Bu parametrenin değerinin çok yüksek bir değere ayarlanması, ekstre deftere nakil işleminin performansını olumsuz etkileyebilir.
- **Toplama dahil edilen maksimum hareket satırı** - Bu alan, yenisi oluşturulmadan önce tek bir toplam harekete dahil edilecek hareket satırlarının sayısını tanımlar. Toplu hareketler müşteri, iş tarihi veya mali boyutlar gibi farklı toplama ölçütleri temel alınarak oluşturulur. Tek bir hareketindeki satırların, farklı toplu hareketler arasında bölünemeyeceğini unutmayın. Bu, toplu hareketteki satırların sayısının, farklı ürünlerin sayısı gibi etkenlere bağlı olarak biraz daha yüksek veya düşük olma olasılığı bulunduğu anlamına gelir.
- **Mağaza hareketlerini doğrulamak için maksimum iş parçacığı sayısı** - Bu alan, hareketlerini doğrulamak için kullanılacak iş parçacıklarının sayısını tanımlar. Hareketlerinin doğrulanması, hareketler ekstrelerden çekilmeden önce gerçekleşmesi gereken bir adımdır. **Ticaret parametreleri** sayfasının **Deftere nakil** sekmesindeki **Hediye kartı** hızlı sekmesinde bir **Hediye kartı ürünü** tanımlamanız gerekir. Kuruluş hediye kartları kullanmasa bile tanımlanması gerekir.

> [!NOTE]
> Ekstre deftere nakilleriyle ilgili olan ve mağazalar ile **Ticaret parametreleri** sayfasında tanımlanan tüm ayarların ve parametreler, geliştirilmiş ekstre deftere nakil özelliğine uygulanabilir.

## <a name="processing"></a>İşleniyor

**Ekstreleri toplu işle hesapla** ve **Ekstreleri toplu işle deftere naklet** menü öğeleri kullanılarak ekstreler toplu şekilde hesaplanabilir ve deftere nakledilebilir. Alternatif olarak, geliştirilmiş ekstre deftere nakil özelliğinin sağladığı **Ekstreler** menü öğesi kullanılarak ekstreler el ile hesaplanabilir ve deftere nakledilebilir.

Toplı ekstre hesaplama ve deftere nakletme adımları eski ekstre deftere nakil özelliğindeki adımlarla aynıdır. Bununla birlikte, ekstreleri arka uçta işleme temel işleminde önemli geliştirmeler yapılmıştır. Bu geliştirmeler işlemi daha esnek hale getirir ve durum ve hata bilgileri için daha fazla görünürlük sağlar. Bu nedenle, kullanıcılar hataların kök nedenine gidebilir ve veri bozulmasına neden olmadan ve verilerin düzeltilmesine gerek kalmadan deftere nakil işlemine devam edebilir.

Aşağıdaki bölümlerde ekstreler ve deftere nakledilen ekstreler için kullanıcı arabiriminde görünen deftere nakil özelliğindeki bazı önemli geliştirmeleri açıklamaktadır.

### <a name="status-details"></a>Durum ayrıntıları

Hesaplama ve deftere nakil işlemlerinde ekstre deftere nakil rutinine yeni bir durum modeli eklenmiştir.

Aşağıdaki tabloda hesaplama işlemi sırasındaki çeşitli durumlar ve bunların sırası açıklanmaktadır.

| Durum sırası | İl      | Tanım |
|-------------|------------|-------------|
| 1           | Başlatıldı    | Ekstre oluşturuldu ve hesaplanmaya hazır. |
| 2           | İşaretli     | Ekstre için kapsamda olan hareketler ekstre parametreleri temel alınarak tanımlanır ve bunlar ekstre kodu ile işaretlenir. |
| 3           | Hesaplandı | Ekstre satırları hesaplanır ve gösterilir. |

Aşağıdaki tabloda deftere nakil işlemi sırasındaki çeşitli durumlar ve bunların sırası açıklanmaktadır.

| Durum sırası | İl                   | Tanım |
|-------------|-------------------------|-------------|
| 1           | Denetlendi                 | Parametrelerle (örneğin değerlendirme masrafı) ve ekstre ve ekstre satırlarıyla (örneğin, sayılan tutar ile hareket tutarı arasındaki fark) ilgili birden fazla doğrulama yapıldı |
| 2           | Toplanan              | Adlandırılmış ve adlandırılmamış müşteriler için satış hareketleri yapılandırmaya göre toplanır. Toplanan her hareket sonunda bir satış siparişine dönüştürülür. |
| 3           | Müşteri siparişi oluşturuldu  | Toplanan hareket temel alınarak sistemde satış siparişleri oluşturulur. |
| 4           | Müşteri faturası oluşturuldu | Satış siparişleri faturalandı. |
| 5           | İskontolar deftere nakledildi        | Periyodik iskonto günlükleri yapılandırmaya göre deftere nakledilir. |
| 6           | Gelir/gider deftere nakledildi   | Gelir/gider hareketleri fiş olarak deftere nakledilir. |
| 7           | Fişler bağlandı         | Ödeme günlükleri oluşturulur ve ilgili faturaya bağlanır. |
| 8           | Ödemeler deftere nakledildi         | Ödeme günlükleri deftere nakledilir. |
| 9           | Hediye kartları deftere nakledildi       | Hediye kartı hareketleri fiş olarak deftere nakledilir. |
| 10          | Gönderildi                  | Ekstre deftere nakledildi olarak işaretlenir. |

Önceki tablodaki her durum normalde bağımsızdır ve durumlar arasında hiyerarşik bir bağımlılık oluşturulur. Bu bağımlılık yukarıdan aşağıya doğru akar. Sistem bir durumu işlerken hatalarla karşılaşırsa, ekstre durumu önceki durumuna geri döndürülür. İşlemin bir sonraki yeniden denemesi başarısız olan durumdan sürdürülür ve ileri doğru devam eder. Bu yöntemin aşağıdaki faydaları vardır:

- Kullanıcı hatanın oluştuğu durumu tam olarak görebilir.
- Verilerin bozulması önlenmiş olur. Örneğin, eski ekstre deftere nakil özelliğinde, bazı satış siparişlerinin faturalandığı ancak diğerlerinin açık bırakıldığı örnekler vardı. Ayrıca, fatura deftere naklinde hata oluştuğundan, bazı ödeme günlüklerinin kapatılacak ilgili faturaya sahip olmadığı örnekler de görülüyordu.
- Kullanıcılar ekstrenin geçerli durumunu ekstrenin **Yürütme ayrıntıları** grubundaki **Durum ayrıntıları** düğmesini kullanarak görebilirler. Durum ayrıntıları sayfasında üç bölüm bulunur:

    - İlk bölüm ekstrenin geçerli durumunu ve bir hata oluşmuşsa hata kodu ile ayrıntılı hata iletisini gösterir.
    - İkinci bölüm hesaplama işleminin çeşitli durumlarını gösterir. Görsel ipuçları başarılı şekilde çalıştırılan durumlar, hata nedeniyle çalıştırılamayan durumları ve henüz çalıştırılmamış olan durumları gösterir.
    - Üçüncü bölüm deftere nakil işleminin çeşitli durumlarını gösterir. Görsel ipuçları başarılı şekilde çalıştırılan durumlar, hata nedeniyle çalıştırılamayan durumları ve henüz çalıştırılmamış olan durumları gösterir.

Ayrıca, ikinci ve üçüncü bölüm başlığı ilgili işlemin genel durumunu gösterir.

### <a name="event-logs"></a>Olay günlükleri

Bir ekstre çeşitli işlemlerden geçer (örneğin Oluştur, Hesapla, Temizle ve Deftere naklet) ve aynı işlemin birden fazla örneği ekstrenin yaşam döngüsü süresince çağrılabilir. Örneğin, bir ekstre oluşturulduktan veya hesaplandıktan sonra bir kullanıcı ekstre içeriğini temizleyip ekstreyi yeniden hesaplayabilir. Ekstrenin **Yürütme ayrıntıları** grubundaki **Olay günlükleri** düğmesi, bir ekstrede çağrılan çeşitli işlemlerin denetim kılavuzunu bu işlemlerin ne zaman çağrıldığı bilgisiyle birlikte verir.

### <a name="aggregated-transactions"></a>Toplanan hareketler

Deftere nakil işlemi sırasında satış hareketleri yapılandırmaya göre toplanır. Toplanan bu hareketler sistemde saklanır ve satış siparişleri oluşturmak için kullanılır. Toplanan her hareket sistemde karşılık gelen bir satış siparişi oluşturur. Toplanan hareketleri **Yürütme ayrıntıları** grubundaki **Toplanan hareketler** düğmesini kullanarak görebilirsiniz.

Toplanan hareketin **Satış siparişi ayrıntısı** sekmesi aşağıdaki bilgileri gösterir:

- **Kayıt kodu** - Toplanan hareketin kodu.
- **Ekstre numarası** – Toplanan hareketin ait olduğu ekstre.
- **Tarih** - Toplanan hareketin oluşturulduğu tarih.
- **Satış kodu** – Toplanan hareketten bir satış siparişi oluşturulduğunda, satış siparişinin kodu. Bu alan boşsa, ilgili satış siparişi oluşturulmamıştır.
- **Toplanan satır sayısı** – Toplanan hareket ve satış siparişi için toplam satır sayısı.
- **Durum** – Toplanan işlemin son durumu.
- **Fatura kodu** – Toplanan hareket için satış siparişi faturalandığında, satış faturası kodu. Bu alan boşsa, satış siparişi için fatura deftere nakledilmemiştir.

Toplanan hareketin **Hareket ayrıntıları** sekmesi toplanan harekete çekilmiş olan tüm hareketleri gösterir. Toplanan hareketteki toplanan satırlar hareketlerinden toplanan tüm kayıtları gösterir. Toplanan satırlar ayrıca madde, çeşit, miktar, fiyat, net tutar, birim ve ambar gibi ayrıntıları gösterir. Temel olarak, toplanan her satır bir satış siparişi satırına karşılık gelir.

**Toplanan hareketler** sayfasından, **Satış siparişini XML'e aktar** düğmesini kullanarak belirli bir toplanan hareket için XML indirebilirsiniz. XML dosyasını, satış siparişi oluşturma ve deftere nakletmeyle ilgili hata ayıklama sorunları için kullanabilirsiniz. XML dosyasını indirin, test ortamına yükleyin ve sorunu test ortamında ayıklayın. Toplanan hareketler için XML dosyası indirme işlevi deftere nakledilmiş olan ekstreler için kullanılamaz.

Toplanan hareket görünümü aşağıdaki faydaları sağlar:

- Kullanıcı satış siparişi oluşturma sırasında başarısız olan toplanan hareketleri ve faturalama sırasında başarısız olan satış siparişlerini görebilir.
- Kullanıcı hareketlerin nasıl toplandığını görebilir.
- Kullanıcı hareketlerinden satış siparişlerine ve satış faturalarına kadar eksiksiz bir denetim kılavuzuna sahip olur. Bu denetimi kılavuzu eski ekstre deftere nakil özelliğinde kullanılamaz.
- Toplanan XML dosyası satış siparişi oluşturma ve faturalama sırasındaki sorunların daha kolay tanımlanmasını sağlar.

### <a name="journal-vouchers"></a>Günlük fişleri

Ekstrenin **Yürütme ayrıntıları** grubundaki **Günlük fişleri** düğmesi bir ekstre için oluşturulan ve iskontolat, gelir/gider hesaplar, hediye kartları vb. ile ilgili olan tüm fiş hareketlerini gösterir.

Şu anda, program yalnızca deftere nakledilen ekstreler için bu verileri gösterir.

### <a name="payment-journals"></a>Ödeme günlükleri

Ekstrenin **Yürütme ayrıntıları** grubundaki **Ödeme günlükleri** düğmesi, bir ekstre için oluşturulan tüm çeşitli ödeme günlüklerini gösterir.

Şu anda, program yalnızca deftere nakledilen ekstreler için bu verileri gösterir.

## <a name="other-improvements"></a>Diğer geliştirmeler

Kullanıcının görebileceği diğer arka uç geliştirmeleri ekstre deftere nakil özelliğinde yapılmıştır. Burada bazı örnekler verilmiştir:

- Toplam personel, terminal ve vardiya varlıklarını dikkate almaz. Daha az toplama parametresi olduğundan, daha az satış siparişi satırının işlenmesi gerekir.
- Hareket tablolarındaki kilitlenme durumları ek uzantı tablolarıyla ve işlemleri hareket tablolarında güncelleştirmek yerine ekleme işlemleri yapılarak azaltılmıştır.
- Çalışan toplu iş görevlerinin sayısı parametreye dönüştürülmüş ve sınırlandırılmıştır. Bu nedenle, bu sayı müşterinin ortamına göre özel olarak ayarlanabilir. Eski ekstre deftere nakil özelliğinde, aynı anda sınırsız sayıda toplu iş görevi oluşturuldu. Bunun sonucu yönetilemeyen yükler, genel gider ve toplu iş sunucusunda tıkanmalar oluyordu.
- Ekstreler, maksimum hareket sayısına sahip ekstrelere öncelik verilerek işlenmek üzere etkin şekilde sıraya alınır.
- **Ekstreleri toplu işle hesapla** ve **Ekstreleri toplu işle deftere naklet** gibi toplu iş işlemleri yalnızca toplu iş modunda çalışır. Eski ekstre deftere nakil özelliğinde kullanıcılar bu toplu işleri çok parçacıklı olan toplu işlemlerin aksine tek parçacıklı bir işlem olan etkileşimli modda çalıştırmayı seçebiliyordu.
- Eski ekstre deftere nakil özelliğinde, toplu işteki herhangi bir hata tüm toplu işin hatalı durumda olmasına neden oluyordu. Geliştirilen özellikte, diğer toplu iş görevlerinin başarıyla tamamlanmış olması durumunda toplu iş görevi hataları toplu işi hatalı duruma sokmaz. Hatalar nedeniyle deftere nakledilmeyen ekstreleri görebileceğiniz **Ekstreler** sayfasını kullanarak bir toplu iş yürütme çalışmasının deftere nakil durumunu değerlendirmeniz gerekir.
- Eski ekstre deftere nakil özelliğinde, ekstre hatası ilk gerçekleştiğinde tüm toplu işin başarısız olmasına neden oluyordu. Kalan ekstreler işlenmiyordu. Gelişmiş özellikte, bazı ekstreler başarısız olsa bile toplu işlem tüm ekstreleri işlemeye devam eder. Bir diğer avantaj ise kullanıcıların hatalı ekstre sayısını tam olarak görebilmesidir. Bu nedenle, kullanıcıların sürekli hataları düzeltme ve deftere nakil işlemini tüm ekstreler deftere nakledilene kadar çalıştırma döngüsüne takılması gerekmez.

## <a name="general-guidance-about-the-statement-posting-process"></a>Ekstre deftere nakil işlemine yönelik genel bir kılavuz

- Ekstre deftere nakil işlemini toplu işte çalıştırmanızı öneririz. Çünkü toplu iş çalıştırma çok parçacıklı işleme konusunda toplu iş altyapısının gücünden faydalanır. Çoklu iş parçacığı kullanımı, ekstre deftere nakillerinde normal olarak görülen çok büyük hacimli hareketlerin işlenmesi için gereklidir.
- Sorunsuz bir deftere nakil deneyimi yaşamanız için madde model grubundaki negatif fiziksel stoğu açmanızı öneririz. Bazı senaryolarda, negatif fiziksel stok olmadığında negatif ekstrelerin deftere nakledilmesi mümkün olmayabilir. Örneğin, teorik olarak, stokta yalnızca tek bir maddenin birimi varsa ve madde için bir satış hareketi ve iade hareketi gerçekleştiyse, hareketin negatif stok açık olmasa bile deftere nakledilebilmesi gerekir. Ancak, ekstre deftere nakil işlemi tek bir müşteri siparişindeki hem satış hem de iade hareketini çektiğinden, önce satış satırının ve ardından iade satırının deftere nakledileceğinin garantisi yoktur. Bu nedenle, hatalar oluşabilir. Bu senaryoda negatif stok açık olursa, hareket deftere nakli negatif olarak etkilenmez ve sistem stoğu doğru şekilde yansıtır.
- Ekstreleri hesaplarken ve deftere naklederken toplamı kullanmanızı öneririz. Bu nedenle, aşağıdaki ayarlar bazı toplam parametreleri için önerilir:

    - **Retail ve Commerce** \> **Genel merkez ayarı** \> **Parametreler** \> **Commerce parametreleri**'ne gidin. Ardından **Deftere nakil** sekmesinde, **Stok güncelleştirme** hızlı sekmesindeki **Ayrıntı düzeyi** alanında **Özet**'i seçin.
    - **Retail ve Commerce** \> **Genel merkez ayarı** \> **Parametreler** \> **Commerce parametreleri**'ne gidin. Ardından **Deftere nakil** sekmesinde **Toplam** hızlı sekmesinde **Fiş hareketleri** seçeneğini **Evet** olarak ayarlayın.
