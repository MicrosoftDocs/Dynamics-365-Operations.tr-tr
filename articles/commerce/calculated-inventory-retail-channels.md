---
title: Perakende kanalları için stok kullanılabilirliğini hesaplama
description: Bu konuda, bir şirketin çevrimiçi ve mağaza kanallarındaki ürünler için tahmini eldeki stok kullanılabilirliğini görüntülemek amacıyla Microsoft Dynamics 365 Commerce'in nasıl kullanabileceği açıklanmaktadır.
author: hhainesms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 2b6f9663ed08ab431ffc6ffe3154854250c1b092
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350486"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Perakende kanalları için stok kullanılabilirliğini hesaplama

[!include [banner](../includes/banner.md)]

Bu konuda, bir şirketin çevrimiçi ve mağaza kanallarındaki ürünler için tahmini eldeki stok kullanılabilirliğini görüntülemek amacıyla Microsoft Dynamics 365 Commerce'in nasıl kullanabileceği açıklanmaktadır.

## <a name="accuracy-of-inventory-availability"></a>Stok kullanılabilirliğinin doğruluğu

Commerce, ölçeklenebilirlik ve performans sağlamak için birden çok sunucu ve veritabanı kullanır. Bu nedenle, satış noktası (POS) uygulaması, e-ticaret stok kullanılabilirliği uygulama programlama arabirimleri (API'lar) ve Commerce genel merkezindeki eldeki stok sayfalarındaki tüm kullanılabilir stok değerlerinin gerçek zamanlı olarak yüzde 100 doğru olmayabileceğini anlamanız önemlidir. Çevrimiçi veya mağaza kanalında ürünler için oluşturulan hareketler henüz Commerce genel merkezi ile eşitlenmediyse Commerce genel merkezinde bulunan eldeki stok sayfaları bu ürünler için doğru gerçek zamanlı bir stok değeri göstermeyebilir. Tersi durumda, şirketinizi kullanıcıların Commerce genel merkezi veya diğer tümleşik uygulamalarda satış yapabilecek, alabilecek, iade edebilecek veya stoğu bir mağaza veya çevrimiçi ambar dışında ayarlayabilecek şekilde yapılandırdıysanız POS veya çevrimiçi kanal, tüm maddeler için doğru bir gerçek zamanlı değer göstermek için gerekli bilgilere sahip olmayabilir.

Operasyon günü içinde sağlanan tüm eldeki kullanılabilirlik verilerinin tahmini değer olarak kabul edildiğini anlamanız çok önemlidir. Bu nedenle, raflardaki gerçek fiziksel envanterle uygulamanın sağladığı eldeki stok bilgilerini veya POS'ta gösterilen eldeki değerleri Commerce genel merkezindeki aynı ambar için bulduğunuz eldeki verilerle karşılaştırmaya çalışırsanız değerler farklılık gösterebilir. Operasyon günü boyunca bu fark beklenir ve sorun olduğu düşünülmemelidir. Verileri denetlemek ve POS, API'ler ve genel merkezde sağlanan değerlerin deponuzda veya ambar rafınızda bulduğunuz gerçek fiziksel birimlerle aynı olduğundan emin olmak istiyorsanız bunu yapmak için en iyi zaman, kanal işlemlerinin gün için durdurulması ve tüm hareketlerin Commerce genel merkezi ve kanallar arasında doğru şekilde eşitlenmesi sonrasıdır.

## <a name="channel-side-inventory-calculation"></a>Kanal tarafında stok hesaplaması

Kanal tarafında stok hesaplaması, Commerce genel merkezindeki son bilinen kanal stok verilerini temel olarak alan ve daha sonra o temele dahil olmayan ve kanal tarafında gerçekleşen ek stok değişikliklerini hesaba katarak eldeki stoğun gerçek zamanlı tahminini elde eden bir mekanizmadır. 

Şu anda kanal tarafında stok hesaplama mantığında aşağıdaki stok değişiklikleri dikkate alınır:

- Mağazada, peşin siparişle satılan stok
- Mağazada veya çevrimiçi kanallarda müşteri üzerinden satılan stok
- Mağazaya iade edilen stok
- Mağaza ambarından karşılanan stok (çekme, paketleme, sevk etme)

Bir önkoşul olarak kanal tarafında stok hesaplamasını kullanmak için, **Ürün kullanılabilirlik** işi tarafından oluşturulan, genel merkezden alınan stok verilerinin periyodik anlık görüntüsünün kanal veritabanlarına gönderilmesi gerekir. Anlık görüntü, genel merkezin bir ürün veya ürün çeşidi ile bir ambarın belirli bir birleşimine ait stok kullanılabilirliği hakkında sahip olduğu bilgileri temsil eder. Yalnızca anlık görüntü çekildiği sırada genel merkezde işlenmiş ve deftere nakledilmiş stok hareketlerini içerir ve dağıtılmış sunucular arasında gerçekleşen sürekli satış işlemleri nedeniyle gerçek zamanlı olarak yüzde 100 doğru olmayabilir.

- Stok, bir mağazadaki bir ürünle ilgili olarak POS uygulamasındaki peşin veya zaman uyumsuz müşteri sipariş satışı aracılığıyla satılmışsa genel merkezin satış için ilgili stok çıkış hareketi hakkındaki bilgilere hemen sahip olmaz. Genel merkez yalnızca P işinin ilgili hareketi mağazanın kanal veritabanından genel merkeze yüklemesinden sonra bu tür mağaza satışları için satılan stok hakkındaki bilgilere sahip olur ve ilgili satış siparişleri ekstre deftere nakil işlemi veya akış deftere nakil işlemleri aracılığıyla oluşturulur. Genel merkezde sipariş oluşturma işlemi ilgili stok hareketlerini oluşturur. 
- E-ticaret kanalı siparişlerinde, genel merkez, yalnızca hareketler P işi aracılığıyla genel merkezde gönderildikten ve sipariş eşitleme işlemi tamamlandıktan sonra stok hareketleri hakkında bilgiye sahip olur.

Commerce genel merkezde stok anlık görüntüsünü almak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Retail ve Commerce BT \> Ürünler ve stok \> Ürün kullanılabilirliği**'ne gidin.
1. **Ürün kullanılabilirliği** işini çalıştırmak için **Tamam**'ı seçin. Ayrıca bu işi bir toplu işte çalışacak şekilde de zamanlayabilirsiniz.

**Ürün kullanılabilirliği** işinin çalışması bittikten sonra, yakalanan verilerin kanal veritabanlarına gönderilmesi gerekir, böylece son genel merkez stok anlık görüntüsü kanal tarafındaki tahmini eldeki stok hesaplamasında dikkate alınabilir.

Anlık görüntü verilerini genel merkezden kanal veritabanlarınıza eşitlemek için aşağıdaki adımları izleyin.

1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. **1130** (**Ürün kullanılabilirliği**) işini çalıştırarak **Ürün kullanılabilirliği** işinin genel merkezde oluşturduğu anlık görüntü verilerini kanal veritabanlarınızla eşitleyin.

## <a name="inventory-availability-apis-for-e-commerce"></a>E-ticaret için stok kullanılabilirliği API'leri

Commerce, bir ürünün stok kullanılabilirliğini sorgulamak üzere e-ticaret senaryoları için aşağıdaki API'leri sağlar:

- **GetEstimatedAvailability** - Çevrimiçi kanalın karşılama grubuyla bağlantılı çevrimiçi kanal ambarındaki veya ambarlardaki bir ürün veya ürün çeşidinin envanterini sorgulamak için bu API'yi kullanın.
- **GetEstimatedProductWarehouseAvailability**: Belirli bir ambardaki bir madde veya madde çeşidinin stoğunu sorgulamak üzere bu API'yi kullanın.

> [!NOTE]
> Bu API'ler Commerce sürüm 10.0.7 ve önceki sürümler için **GetProductAvailabilities** ve **GetAvailableInventoryNearby** API'lerinin yerini almaktadır.

Her iki API de dahili olarak kanal tarafı hesaplama mantığını kullanır ve istenen ürün ve ambar için tahmini **fiziksel kullanılabilir** miktar, **toplam kullanılabilir** miktar, **ölçü birimi (UoM)** ve **stok düzeyi** değerlerini döndürür. Döndürülen değerler, isterseniz e-ticaret sitenizde gösterilebilir ya da e-ticaret sitenizde diğer iş mantığını tetiklemek için kullanılabilir. Örneğin, "stok dışı" stok düzeyi olan ürünlerin satın alınmasını engelleyebilirsiniz.

Commerce'de yer alan diğer API'ler ürün için genel eldeki miktarları almak üzere doğrudan genel merkeze gidebildiği halde, olası performans sorunları ve bu sık isteklerin genel merkez sunucularınızda yapabileceği ilgili etki nedeniyle bunların bir e-ticaret ortamında kullanılması önerilmez. Ek olarak, kanal tarafı hesaplamada yukarıda sözü edilen iki API, henüz genel merkez tarafından bilinmeyen kanallarda oluşturulan hareketleri hesaba katarak, ürünün kullanılabilirliğiyle ilgili daha doğru bir tahmin sağlayabilir.

Bu iki API'yi kullanmak için, genel merkezdeki **Özellik yönetimi** çalışma alanı ile **En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama** özelliğini etkinleştirmelisiniz. Çevrimiçi ve mağaza kanallarınız aynı satış siparişi karşılama ambarlarını kullanıyorsa ayrıca **Gelişmiş e-Ticaret kanal tarafında stok hesaplama mantığı** özelliğini etkinleştirmeniz gerekir.Böylece, iki API'nin mağaza kanalında oluşturulan deftere nakledilmemiş hareketleri (nakit-ve-hareket, müşteri siparişleri, iadeler) hesaba katarak kanal tarafındaki hesaplama mantığını hesaba katar. Bu özellikleri etkinleştirdikten sonra **1070** (**Kanal yapılandırma**) işini çalıştırmanız gerekir.

API çıktısında ürün miktarının nasıl döndürüleceğini tanımlamak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Genel merkez ayarı \> Parametreler \> Commerce parametreleri**'ne gidin.
1. **Stok** sekmesini seçin ve ardından **e-Ticaret için stok kullanılabilirliği API'leri** hızlı sekmesinde **API çıktısında miktar** ayarının değerini yapılandırın.
1. En güncel ayarları kanallara eşitlemek için **1070** (**Kanal yapılandırması**) işini çalıştırın.

**API çıktısında miktar** ayarı, üç seçenek sağlar:

- **İade stok miktarı** - İstenen ürünün fiziksel kullanılabilir ve toplam kullanılabilir miktarı API çıktısında verilir.
- **Stok tamponu hariç iade stoğu miktarı** -API çıktısında iade edilen miktar, stok tampon değeri çıkarılarak düzeltilir. Stok tamponu hakkında daha fazla bilgi için bkz. [Stok tamponlarını ve stok düzeylerini yapılandırma](inventory-buffers-levels.md).
- **İade edilmemiş stok miktarı** - API çıktısında yalnızca stok düzeyi döndürülür. Stok düzeyleri hakkında daha fazla bilgi için bkz. [Stok tamponlarını ve stok düzeylerini yapılandırma](inventory-buffers-levels.md).

`QuantityUnitTypeValue` API parametresini, API'lerin miktarı hangi birim türünde döndürmelerini istediğinizi belirtmek için kullanabilirsiniz. Bu parametre, **stok birimi** (varsayılan), **satınalma birimi** ve **satış birimi** seçeneklerini destekler. İade edilen miktar, genel merkezdeki ilgili ölçü biriminin (UOM) tanımlanan duyarlığına yuvarlanır.

**GetEstimatedAvailability** API, farklı sorgu senaryolarını desteklemek için aşağıdaki giriş parametrelerini sunar:

- `DefaultWarehouseOnly` - Çevrimiçi kanalın varsayılan ambarında bulunan bir ürünün envanterini sorgulamak için bu parametreyi kullanın. 
- `FilterByChannelFulfillmentGroup` ve `SearchArea` - `longitude`, `latitude` ve `radius` temel alınarak belirli bir arama alanındaki tüm malzeme çekme konumlarından bir ürünün envanterini sorgulamak için bu iki parametreyi kullanın. 
- `FilterByChannelFulfillmentGroup` ve `DeliveryModeTypeFilterValue` - Bir çevrimiçi kanalın karşılama grubuna bağlı ve belirli teslimat şekillerini destekleyecek şekilde yapılandırılmış belirli ambarlardan bir ürünün envanterini sorgulamak için bu iki parametreyi kullanın. `DeliveryModeTypeFilterValue` parametresi **tüm** (varsayılan), **sevkiyat** ve **malzeme çekme** seçeneklerini destekler. Örneğin, bir çevrimiçi siparişin çoklu sevkiyat ambarlarında karşılanabileceği bir senaryoda, bir ürünün stok kullanılabilirliğini tüm bu sevk ambarlarında sorgulamak için bu iki parametreyi kullanabilirsiniz. Bu durumda API, sevkiyat ambarlarından her biri için ürünün eldeki miktarını ve stok düzeyinin yanı sıra sorgu kapsamındaki tüm sevk ambarlardan elde edilen miktar ve toplam stok düzeyini döndürür.
 
Commerce satın alma kutusu, mağaza seçici, istek listesi, sepet ve sepet simge modülleri, e-ticaret sitesinde stok düzeyi iletileri görüntülemek için yukarıda belirtilen API'leri ve parametreleri kullanır. Commerce site oluşturucu, emtia ve satın alma davranışlarını denetlemek için çeşitli stok ayarları sağlar. Daha fazla bilgi için, [Envanter ayarları uygula](inventory-settings.md) konusuna bakın.

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Kanal tarafı hesaplama ile POS stok araması

Commerce sürüm 10.0.9 ve önceki sürümlerde, POS'taki **Stok arama** işlemi, mağazanın kanal yapılandırmasının parçası olarak karşılama grubu için yapılandırılan kullanıcının mevcut mağazası ve tüm diğer mağazalarda seçilen ürünün stok bilgilerini almak için Commerce genel merkeze yapılan gerçek zamanlı bir servis çağrısı kullanıyordu. Commerce sürüm 10.0.10 ve sonraki sürümlerde, genel merkeze gerçek zamanlı servis çağrılarını kapatabilir ve bunun yerine, mağaza için fiziksel olarak kullanılabilen eldeki stoğu ve karşılama grubunda tanımlanan diğer konumları belirlemek için Commerce sunucusunda kanal tarafı hesaplamasını kullanabilirsiniz. Bu kanal tarafından hesaplanan stok yapılandırması, genel merkezden stok aramaları almak için çevrimiçi olmanız gerekmediğinden, İnternet bağlantısının güvenilir olmadığı yerlerde de yararlıdır.

Kanal tarafı hesaplaması doğru yapılandırılıp yönetildiğinde Commerce kanalı veritabanında harekete dayalı veriler kullandığından ancak genel merkez henüz bununla ilgili bilgiye sahip olmayabileceğinden mevcut mağaza stoğuna ilişkin daha güvenilir bir tahmin sağlayabilir. Örneğin, POS'ta stok aramaları için var olan gerçek zamanlı servis aramasını kullanırsanız genel merkez henüz büyük olasılıkla bir ürün için gerçekleşen peşin bir satış hakkında bilgi sahibi olmayacaktır. Bu nedenle, genel merkezin bu ürün için verdiği eldeki stok değeri büyük olasılıkla mağazanın fiili eldeki stokunu bir birim kadar aşabilir. Ancak kanal tarafı hesaplaması kullanırsanız peşin satışı hesaplamaya katılarak gösterilen eldeki değerden düşülebilir. Hem kanal tarafı hesaplamasının hem de gerçek zamanlı servis çağrısının sağladığı değerler yalnızca eldeki stoğa ilişkin tahminler olduğu halde, kanal tarafı hesaplamasının sağladığı değer, geçerli mağaza için daha büyük olasılıkla doğrudur.

Kanal tarafı hesaplama mantığını kullanmak ve gerçek zamanlı servis çağrılarını kapatmak üzere Commerce Headquarters'da POS **Stok araması** işlemini yapılandırmak için öncelikle Commerce Headquarters'taki **Özellik yönetimi** çalışma alanı üzerinden **En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama** özelliğini etkinleştirmeniz ve ardından bu adımları izlemeniz gerekir.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın.
1. Bir işlev profili seçin.
1. **İşlevler** hızlı sekmesindeki **Stok kullanılabilirliği hesaplaması** bölümünde **Gerçek zamanlı servis** olan **Stok kullanılabilirliği hesaplama modu** değerini **Kanal** olarak değiştirin. Varsayılan olarak, tüm işlev profilleri gerçek zamanlı servis çağrıları kullanır. Kanal tarafı hesaplama mantığı kullanmak istiyorsanız bu alanın değerini değiştirmeniz gerekir. Seçilen işlev profiline bağlı her perakende mağazası bu değişiklikten etkilenir.

Daha sonra aşağıdaki adımları gerçekleştirerek, değişiklikleri genel merkezde dağıtım zamanlaması işlemi aracılığıyla kanallara eşitlemeniz gerekir.

1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. **1070** (**Kanal yapılandırması**) işini çalıştırın.

Yapılandırma tamamlandıktan sonra, bir POS uygulamasındaki bir kullanıcı **Stok arama** işlemini (standart ve matris görünümleri) kullandığında, fiziksel stokla ilgili olarak sağlanan bilgiler artık gerçek zamanlı bir servis çağrısı kullanmaz. Bunun yerine, geçerli mağazanın fiziksel olarak kullanılabilir stoğu ve karşılama grubundaki tüm mağazalar hakkındaki veriler, Commerce Headquarters'dan kanal veritabanına teslim edilen son bilinen anlık görüntüye göre hesaplanır. Anlık görüntü değeri 1130 işindeki son eşitlenen anlık görüntüye dahil edilmeyen kanal veritabanındaki seçilen ürün için var olan ek satış veya iade hareketlerine göre mevcut fiziksel değeri ayarlamak için kanal tarafı hesaplamasıyla daha da daraltılır. Kanal veritabanında, karşılama grubundaki ambarlardan veya mağazalardan herhangi birine ait hareket verileri yoksa değerin yeniden hesaplanmasında hesaba katılabilecek ek hareketler içermez. Bu nedenle, bu ambarlar veya mağazalar için gösterilebilecek en iyi eldeki stok tahmininde, son bilinen Commerce Headquarters anlık görüntüsüne ait veriler yer alabilir.

POS'un **'Sipariş karşılama** ekranları da, bir sipariş karşılama satırı seçildiğinde ve bir kullanıcı seçili maddenin ilgili eldeki stoğu için **Ayrıntılar** panelini görüntülediğinde, maddeler için eldeki stoku göstermek üzere kanal tarafı hesaplamasını kullanır.

## <a name="optimize-your-inventory-data"></a>Stok verilerinizi en iyi duruma getirme

Stoğun mümkün olan en iyi tahminini elde etmek için, aşağıdaki Commerce toplu işleri kullanmanız ve bunları sıkça çalıştırmanız çok önemlidir:

- **P işi**: P işi **Dağıtım zamanlamaları** sayfasında bulunur ve sıkça çalıştırılmalıdır. Bu iş, e-Ticaret siparişleri, POS'un oluşturduğu zaman uyumsuz müşteri siparişleri ve POS'un kanal veritabanlarından oluşturduğu peşin siparişleri daha fazla işlenebilmeleri için Commerce Headquarters'a götürür. Kanaldaki bu veriler Commerce Headquarters ile eşitleninceye kadar, Commerce Headquarters'ın bu hareketlerden ortaya çıkan ambarlardaki ürünlerle ilgili stok düzeltmeleri hakkında hiçbir bilgisi yoktur.
- **Siparişleri eşitle**: Bu iş Commerce Headquarters'daki P işinin sunduğu ham hareket verilerini işler ve Commerce Headquarters'da e-Ticaret ve zaman uyumsuz müşteri sipariş hareketlerini satış siparişlerine dönüştürür. Bu iş işlene alınana ve satış siparişleri oluşturuluncaya kadar, hiçbir stok hareketi oluşturulmaz. Bu nedenle, Commerce Headquarters'daki eldeki stok, hareketleri dikkate almaz.
- **Toplu işteki hareket ekstrelerini hesapla**: Mağazada oluşturulan peşin hareketler için, akış deftere nakil işlemi, satışlarla ilgili stoğun verimli şekilde güncelleştirilmesini sağlar. Peşin siparişler için stok hareketlerinin en etkili şekilde işlenmesini sağlamak üzere sisteminizi, [akış deftere nakil işlemini](./trickle-feed.md)kullanacak şekilde yapılandırdığınızdan emin olun.
- **Toplu işteki hareket ekstrelerini deftere naklet**: Bu iş, akışı deftere nakletme işlemi için de gereklidir. **Toplu işteki hareket ekstrelerini hesapla** işinden sonra gelir. Bu iş, hesaplanmış ekstreleri sistematik olarak deftere nakleder, böylece nakit satış siparişleri Commerce Headquarters'da oluşturulur ve Commerce Headquarters mağaza stoğunuzu daha doğru şekilde yansıtır.
- **Ürün kullanılabilirliği**: Bu iş, Commerce Headquarters'daki stoğun anlık görüntüsünü oluşturur.
- **1130 (Ürün kullanılabilirliği)**: Bu iş **Dağıtım zamanlamaları** sayfasında bulunur ve **Ürün kullanılabilirliği** işinden hemen sonra çalıştırılmalıdır. Bu iş, stok anlık görüntü verilerini Commerce Headquarters'dan kanal veritabanlarına aktarır.

> [!NOTE]
> - **Ürün kullanılabilirliği** ve **1130** işlerini saatlik olarak çalıştırmak ve P-işi, sipariş eşitleme ve akışla kademeli deftere nakil ile ilgili işleri aynı veya daha yüksek sıklıkla ayarlamak iyi bir yaklaşımdır.
> - Performans nedeniyle, kanal tarafı stok kullanılabilirliği hesaplamaları e-Ticaret API'sını veya POS kanal tarafı stok mantığını kullanarak stok kullanılabilirliği isteği oluşturmak için kullanıldığında, hesaplamada, hesaplama mantığını yeniden çalıştırmayı gerekçelendirmek için yeterince zaman geçip geçmediğini belirlemek amacıyla bir önbellek kullanılır. Varsayılan önbellek 60 saniyeye ayarlanır. Örneğin, mağazanız için kanal tarafındaki hesaplamayı açtınız ve **Stok arama** sayfasında bulunan bir ürünle ilgili eldeki stoğu görüntülediniz. Daha sonra ürünün bir birimi satılıyorsa **Stok arama** sayfası, önbellek temizlenene kadar azalan stoğu göstermez. Kullanıcılar POS'taki hareketleri deftere naklettikten sonra, eldeki stoğun azaldığını doğrulamadan önce 60 saniye beklemelidir.

İş senaryonuz için daha küçük bir önbellek süresi gerekiyorsa yardım için ürün destek temsilcinize başvurun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
