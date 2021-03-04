---
title: Perakende kanalları için stok kullanılabilirliğini hesaplama
description: Bu konu, mağaza ve çevrimiçi kanallarla ilgili eldeki stoğu göstermek için kullanılabilen seçenekleri açıklar.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: de4ee98198f441b8f42a8a55aa5ff1015f485234
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416413"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Perakende kanalları için stok kullanılabilirliğini hesaplama

[!include [banner](../includes/banner.md)]

Bu konuda, bir şirketin çevrimiçi ve mağaza kanallarındaki ürünler için tahmini eldeki stok kullanılabilirliğini görüntülemek amacıyla Microsoft Dynamics 365 Commerce'in nasıl kullanabileceği açıklanmaktadır.

## <a name="accuracy-of-calculation"></a>Hesaplama doğruluğu

Commerce, ölçeklenebilirlik ve performans sağlamak için birden çok sunucu ve veritabanı kullanır. Bu nedenle, satış noktası (POS) uygulaması, e-Ticaret stok kullanılabilirliği uygulama programlama arabirimleri (API'lar) ve Commerce Headquarters'daki eldeki stok sayfalarındaki tüm kullanılabilir stok değerlerininin gerçek zamanlı olarak yüzde 100 doğru olmayabileceğini anlamanız önemlidir. Çevrimiçi veya mağaza kanalında ürünler için oluşturulan hareketler henüz Commerce Headquarters sunucusu ve veritabanı ile eşitlenmediyse Commerce Headquarters'da bulunan eldeki stok sayfaları bu ürünler için doğru gerçek zamanlı bir stok değeri göstermeyebilir. Tersi durumda, şirketinizi kullanıcıların Commerce Headquarters veya diğer tümleşik uygulamalarda satış yapabilecek, alabilecek, iade edebilecek veya stoğu bir mağaza veya çevrimiçi ambar dışında ayarlayabilecek şekilde yapılandırdıysanız POS veya çevrimiçi kanal, tüm maddeler için doğru bir gerçek zamanlı eldeki değer göstermek için gerekli bilgilere sahip olmayabilir.

Bu konu, uygulamalar veya kanallar arasındaki veri gecikmesini sınırlamaya yardımcı olmak amacıyla sık çalıştırılabilecek veri eşitleme işlemlerini açıklamaktadır. Ancak, operasyon günü içinde sağlanan tüm eldeki kullanılabilirlik verilerinin tahmini değer olarak kabul edildiğini anlamanız çok önemlidir. Bu nedenle, raflardaki gerçek fiziksel envanterle uygulamanın sağladığı eldeki stok bilgilerini veya POS'ta gösterilen eldeki değerleri Commerce Headquarters'daki aynı ambar için bulduğunuz eldeki verilerle karşılaştırmaya çalışırsanız değerler farklılık gösterebilir. Operasyon günü boyunca bu fark beklenir ve sorun olduğu düşünülmemelidir. Verileri denetlemek ve stok kullanılabilirliği API'larında ve Commerce Headquarters'da sağlanan değerlerin deponuzda veya ambar rafınızda bulduğunuz gerçek fiziksel birimlerle aynı olduğundan emin olmak istiyorsanız bunu yapmak için en iyi zaman, kanal işlemlerinin gün için durdurulması ve tüm hareketlerin Commerce Headquarters ve kanal arasında doğru şekilde eşitlenmesi sonrasıdır.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>E-ticaret stok kullanılabilirliği istekleri için stok arama API'ları kullanma

Müşterileriniz bir e-Ticaret sitesinde alışveriş yaparken bir ürünün stok kullanılabilirliğini göstermek için aşağıdaki API'ları kullanabilirsiniz.

- **GetEstimatedAvailability**: E-Ticaret kanalı ambarındaki veya e-Ticaret kanalının karşılama grubunun yapılandırmasına bağlı tüm ambarlardaki maddeyle ilgili stok kullanılabilirliğini elde etmek için bu API'yı kullanın. Bu API, boylam ve enlem verilerine dayalı olarak belirli bir arama alanındaki veya yarıçaptaki ambarlar için de kullanılabilir.
- **GetEstimatedProductWarehouseAvailability**: Belirli bir ambardaki bir madde için stok isteğinde bulunmak üzere bu API'yı kullanın. Örneğin, API'yı sipariş çekme işlemleri içeren senaryolarda stok kullanılabilirliğini göstermek için kullanabilirsiniz.

> [!NOTE]
> Bu API'lar Dynamics 365 Retail sürüm 10.0.7 ve önceki sürümler için **GetProductAvailabilities** ve **GetAvailableInventoryNearby** API'larının yerini almaktadır.

İki API da Commerce sunucusundan veri alıp bir ürün veya ürün çeşidi ile bir ambarın belirli bir birleşimi için eldeki stoğa ilişkin bir tahmin sağlar. Commerce sunucusunda yer alan diğer API'lar ürün için genel eldeki miktarları almak üzere doğrudan Commerce Headquarters'a gidebildiği halde, olası performans sorunları ve bu sık isteklerin Commerce Headquarters sunucularınızda yapabileceği ilgili etki nedeniyle bunların bir e-Ticaret ortamında kullanılması önerilmez. Ayrıca eldeki stok Commerce sunucusu aracılığıyla hesaplanıyorsa hesaplamanın, henüz Commerce Headquarters ile eşitlenmemiş olan son e-ticaret hareketlerinde satılan stoğu içermesi daha olasıdır. Commerce Headquarters'ın bu hareketlerle ilgili bilgilere sahip olmasa da Commerce sunucusu ve kanal veritabanı verilere sahip olabilir. Bu nedenle, veriler hesaba katılır ve bir ürünün kullanılabilir stoğuna daha doğru tahmin sunmaya yardımcı olabilir.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>E-Ticaret ile hesaplanan stok kullanılabilirliği ile başlama

Daha önce belirtilen iki API'yı kullanmadan önce, Commerce Headquarters'daki **Özellik yönetimi** çalışma alanı ile **En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama** özelliğini etkinleştirmelisiniz.

API'ların bir maddenin stok kullanılabilirliğine ilişkin en iyi tahmini hesaplayabilmesi için, Commerce Headquarters'dan alınan stok kullanılabilirliğinin periyodik anlık görüntüsünün işlenmesi ve e-Ticaret Commerce Scale Unit'in kullandığı kanal veritabanına gönderilmesi gereklidir. Anlık görüntü, Commerce Headquarters'ın bir ürün veya ürün çeşidi ile bir ambarın belirli bir birleşimine ait stok kullanılabilirliği hakkında sahip olduğu bilgileri temsil eder. Bu stok girişlerinden veya sevkiyatlardan ya da Commerce Headquarters'da gerçekleştirilen ve e-Ticaret kanalının yalnızca işlemin eşitlenmesi nedeniyle bilgi sahibi olduğu diğer işlemlerden kaynaklanan stok ayarlarını veya hareketlerini içerebilir.

**Ürün kullanılabilirliği** işinin oluşturduğu veritabanı anlık görüntüsü yalnızca, anlık görüntünün çekildiği sırada Commerce Headquarters'da işlenmiş ve deftere nakledilmiş stok hareketlerini hesaplar. Stok, bir mağaza ambarındaki bir ürünle ilgili olarak POS uygulamasındaki peşin veya zaman uyumsuz müşteri sipariş satışı aracılığıyla satılmışsa Commerce Headquarters'ın satış için ilgili stok çıkış hareketi hakkındaki bilgilere hemen sahip olmaz. Yalnızca P işinin ilgili hareketi mağazanın kanal veritabanından Commerce Headquarters'a yüklemesinden sonra bu tür mağaza satışları için satılan stok hakkındaki bilgilere sahip olur ve ilgili satış siparişi ekstre deftere nakil işlemi veya akış deftere nakil işlemleri aracılığıyla oluşturulur. Commerce Headquarters'da sipariş oluşturma işlemi ilgili stok hareketlerini oluşturur. E-Ticaret kanalı siparişlerinde, Commerce Headquarters, yalnızca hareketler P işi aracılığıyla Commerce Headquarters'da gönderildikten ve sipariş eşitleme işlemi tamamlandıktan sonra stok hareketleri hakkında bilgiye sahip olur. Bu nedenle, dağıtılmış sunucular arasında gerçekleşen sabit satış işlemleri nedeniyle **Ürün kullanılabilirliği** işinde sunulan stok anlık görüntü değerinin yüzde 100 doğru olmayabileceğini anlamanız önemlidir.

Commerce Headquarters'da stok anlık görüntüsünü almak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Retail ve Commerce BT \> Ürünler ve stok \> Ürün kullanılabilirliği**'ne gidin.
1. **Ürün kullanılabilirliği** işini çalıştırmak için **Tamam**'ı seçin. Ayrıca bu işi bir toplu işte çalışacak şekilde zamanlayabilirsiniz.

**Ürün kullanılabilirliği** işinin çalışması bittikten sonra, yakalanan verilerin e-Ticaret kanalı veritabanlarına gönderilmesi gerekir, böylece son Commerce Headquarters stok anlık görüntüsü tahmini eldeki stok hesaplamasında dikkate alınabilir.

1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. **1130** (**Ürün kullanılabilirliği**) işini çalıştırarak **Ürün kullanılabilirliği** işinin Commerce Headquarters'da oluşturduğu anlık görüntü verilerini kanal veritabanlarınızla eşitleyin.

**GetEstimatedAvailability** veya **GetEstimatedProductWarehouseAvailability** API'sından stok kullanılabilirliği istendiğinde, ürün için olası en iyi tahmini tahmin elde etmek amacıyla bir hesaplama çalıştırılır. Hesaplama, kanal veritabanında bulunan ancak 1130 işinin sağladığı anlık görüntü verilerinde yer almayan tüm e-Ticaret müşteri siparişlerine başvurur. Bu mantık, son işlenen stok hareketi Commerce Headquarters'da izlenerek ve bu, kanal veritabanındaki hareketlerle karşılaştırarak gerçekleştirilir. Bu, kanal tarafı hesaplama mantığının temelini oluşturur, böylece e-Ticaret kanalı veritabanındaki müşteri siparişi satış hareketleri için oluşan ek stok hareketleri, API'nın sağladığı tahmin edilen tahmini stok değerinde dikkate alınabilir.

Kanal tarafı hesaplama mantığı, istenen ürün ve ambar için tahmini fiziksel kullanılabilir değeri ve toplam kullanılabilir değeri verir. Değerler, isterseniz e-Ticaret sitenizde gösterilebilir ya da e-Ticaret sitenizde diğer iş mantığını tetiklemek için kullanılabilir. Örneğin, API'nın gönderdiği eldeki gerçek miktar yerine "stokta yok" iletisi gösterebilirsiniz.

Tahmin edilen stok değeri için kanal tarafındaki e-Ticaret API'larının kullandığı hesaplama mantığı, stoğu yalnızca kanal veritabanında oluşturulmuş ancak Commerce Headquarters'da henüz eşitlenmemiş ve deftere nakledilmemiş müşteri siparişlerine göre değerlendirebilir. Ayrıca kanal veritabanınız mağazaya özel ambarlarla ilgili olarak peşin satışa ilişkin hareket verileri içeriyorsa peşin satışlar bu ambarlar için kanal tarafındaki e-Ticaret hesaplamasında dikkate alınmaz.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>POS kanalında stok arama işlemini yapılandırma

Retail sürüm 10.0.9 ve önceki sürümlerde, POS'taki **Stok arama** işlemi, mağazanın kanal yapılandırmasının parçası olarak karşılama grubu için yapılandırılan kullanıcının mevcut mağazası ve tüm diğer mağazalarda seçilen ürünün stok bilgilerini almak için Commerce Headquarters'a yapılan gerçek zamanlı bir servis çağrısı kullanıyordu. Commerce sürüm 10.0.10 ve üzerinde ise Commerce Headquarters'a yapılan gerçek zamanlı servis çağrılarını kapatabilirsiniz. Bunun yerine, mağaza için fiziksel olarak kullanılabilir olan eldeki stoğu ve karşılama grubunda tanımlanan diğer yerleşimleri belirlemek için Commerce sunucusunda kanal tarafı hesaplamasını kullanabilirsiniz. Bu kanal tarafından hesaplanan stok yapılandırması, Commerce Headquarters'dan stok aramaları almak için çevrimiçi olmanız gerekmediğinden, İnternet bağlantısının güvenilir olmadığı yerlerde de yararlıdır.

Kanal tarafı hesaplaması doğru yapılandırılıp yönetildiğinde Commerce kanalı veritabanında harekete dayalı veriler kullandığından ancak Commerce Headquarters henüz bununla ilgili bilgiye sahip olmayabileceğinden mevcut mağaza stoğuna ilişkin daha güvenilir bir tahmin sağlayabilir. Örneğin, POS'ta stok aramaları için var olan gerçek zamanlı servis aramasını kullanırsanız Commerce Headquarters henüz büyük olasılıkla bir ürün için gerçekleşen peşin bir satış hakkında bilgi sahibi olmayacaktır. Bu nedenle, Commerce Headquarters'ın bu ürün için verdiği eldeki stok değeri büyük olasılıkla mağazanın fiili eldeki stokunu bir birim kadar aşabilir. Ancak kanal tarafı hesaplaması kullanırsanız peşin satışı hesaplamaya katılarak gösterilen eldeki değerden düşülebilir. Hem kanal tarafı hesaplamasının hem de gerçek zamanlı servis çağrısının sağladığı değerler yalnızca eldeki stoğa ilişkin tahminler olduğu halde, kanal tarafı hesaplamasının sağladığı değer, geçerli mağaza için daha büyük olasılıkla doğrudur.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>POS kanalı tarafı ile hesaplanan stok kullanılabilirliği ile başlama

Kanal tarafı hesaplama mantığını kullanmak ve POS uygulamasından alınan stok aramaları için gerçek zamanlı servis çağrılarını kapatmak için öncelikle Commerce Headquarters'daki **Özellik yönetimi** çalışma alanı üzerinden **En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama** özelliğini etkinleştirmeniz gerekir. Özelliği etkinleştirmenin yanı sıra, **İşlevsellik profilinde** değişiklik yapmalısınız.

**İşlevsellik profilini** değiştirmek için aşağıdaki adımları izleyin:

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın.
1. Bir işlev profili seçin.
1. **İşlevler** hızlı sekmesindeki **Stok kullanılabilirliği hesaplaması** bölümünde **Gerçek zamanlı servis** olan **Stok kullanılabilirliği hesaplama modu** değerini **Kanal** olarak değiştirin. Varsayılan olarak, tüm işlev profilleri gerçek zamanlı servis çağrıları kullanır. Bu nedenle, kanal tarafı hesaplama mantığı kullanmak istiyorsanız bu alanın değerini değiştirmeniz gerekir. Seçilen işlev profiline bağlı her perakende mağazası bu değişiklikten etkilenir.

Daha sonra aşağıdaki adımları gerçekleştirerek, değişiklikleri dağıtım zamanlaması işlemi aracılığıyla kanala eşitlemeniz gerekir:

1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. **1070** (**Kanal yapılandırması**) işini çalıştırın.

Yapılandırma tamamlandıktan sonra, bir POS uygulamasındaki bir kullanıcı **Stok arama** işlemini (standart ve matris görünümleri) kullandığında, fiziksel stokla ilgili olarak sağlanan bilgiler artık gerçek zamanlı bir servis çağrısı kullanmaz. Bunun yerine, geçerli mağazanın fiziksel olarak kullanılabilir stoğu ve karşılama grubundaki tüm mağazalar hakkındaki veriler, Commerce Headquarters'dan kanal veritabanına teslim edilen son bilinen anlık görüntüye göre hesaplanır. Anlık görüntü değeri 1130 işindeki son eşitlenen anlık görüntüye dahil edilmeyen kanal veritabanındaki seçilen ürün için var olan ek satış veya iade hareketlerine göre mevcut fiziksel değeri ayarlamak için kanal tarafı hesaplamasıyla daha da daraltılır. Kanal veritabanında, karşılama grubundaki ambarlardan veya mağazalardan herhangi birine ait hareket verileri yoksa değerin yeniden hesaplanmasında hesaba katılabilecek ek hareketler içermez. Bu nedenle, bu ambarlar veya mağazalar için gösterilebilecek en iyi eldeki stok tahmininde, son bilinen Commerce Headquarters anlık görüntüsüne ait veriler yer alabilir.

POS'un **'Sipariş karşılama** ekranları da, bir sipariş karşılama satırı seçildiğinde ve bir kullanıcı seçili maddenin ilgili eldeki stoğu için **Ayrıntılar** panelini görüntülediğinde, maddeler için eldeki stoku göstermek üzere kanal tarafı hesaplamasını kullanır.

## <a name="optimize-your-inventory-data"></a>Stok verilerinizi en iyi duruma getirme

Stoğun mümkün olan en iyi tahminini elde etmek için, aşağıdaki Commerce toplu işleri kullanmanız ve bunları sıkça çalıştırmanız çok önemlidir:

- **P işi**: P işi **Dağıtım zamanlamaları** sayfasında bulunur ve sıkça çalıştırılmalıdır. Bu iş, e-Ticaret siparişleri, POS'un oluşturduğu zaman uyumsuz müşteri siparişleri ve POS'un kanal veritabanlarından oluşturduğu peşin siparişleri daha fazla işlenebilmeleri için Commerce Headquarters'a götürür. Kanaldaki bu veriler Commerce Headquarters ile eşitleninceye kadar, Commerce Headquarters'ın bu hareketlerden ortaya çıkan ambarlardaki ürünlerle ilgili stok düzeltmeleri hakkında hiçbir bilgisi yoktur.
- **Siparişleri eşitle**: Bu iş Commerce Headquarters'daki P işinin sunduğu ham hareket verilerini işler ve Commerce Headquarters'da e-Ticaret ve zaman uyumsuz müşteri sipariş hareketlerini satış siparişlerine dönüştürür. Bu iş işlene alınana ve satış siparişleri oluşturuluncaya kadar, hiçbir stok hareketi oluşturulmaz. Bu nedenle, Commerce Headquarters'daki eldeki stok, hareketleri dikkate almaz.
- **Toplu işteki hareket ekstrelerini hesapla**: Mağazada oluşturulan peşin hareketler için, akış deftere nakil işlemi, satışlarla ilgili stoğun verimli şekilde güncelleştirilmesini sağlar. Peşin siparişler için stok hareketlerinin en etkili şekilde işlenmesini sağlamak üzere sisteminizi, [akış deftere nakil işlemini](https://docs.microsoft.com/dynamics365/commerce/trickle-feed)kullanacak şekilde yapılandırdığınızdan emin olun.
- **Toplu işteki hareket ekstrelerini deftere naklet**: Bu iş, akışı deftere nakletme işlemi için de gereklidir. **Toplu işteki hareket ekstrelerini hesapla** işinden sonra gelir. Bu iş, hesaplanmış ekstreleri sistematik olarak deftere nakleder, böylece nakit satış siparişleri Commerce Headquarters'da oluşturulur ve Commerce Headquarters mağaza stoğunuzu daha doğru şekilde yansıtır.
- **Ürün kullanılabilirliği**: Bu iş, Commerce Headquarters'daki stoğun anlık görüntüsünü oluşturur.
- **1130 (Ürün kullanılabilirliği)**: Bu iş **Dağıtım zamanlamaları** sayfasında bulunur ve **Ürün kullanılabilirliği** işinden hemen sonra çalıştırılmalıdır. Bu iş, stok anlık görüntü verilerini Commerce Headquarters'dan kanal veritabanlarına aktarır.

Bu toplu işleri çok sık (birkaç dakika arayla) çalıştırmamanız önerilir. Sık yapılan çalıştırmalar Commerce Headquarters (HQ) üzerinde aşırı yük oluşturur ve performansı etkileyebilir. Genel olarak, ürün kullanılabilirliği ve 1130 işlerini saatlik olarak çalıştırmak ve P-işi, sipariş eşitleme ve akışla kademeli deftere nakil ile ilgili işleri aynı veya daha yüksek sıklıkla ayarlamak iyi bir yaklaşımdır.

> [!NOTE]
> Performans nedeniyle, kanal tarafı stok kullanılabilirliği hesaplamaları e-Ticaret API'sını veya yeni POS kanal tarafı stok mantığını kullanarak stok kullanılabilirliği isteği oluşturmak için kullanıldığında, hesaplamada, hesaplama mantığını yeniden çalıştırmayı gerekçelendirmek için yeterince zaman geçip geçmediğini belirlemek amacıyla bir önbellek kullanılır. Varsayılan önbellek 60 saniyeye ayarlanır. Örneğin, mağazanız için kanal tarafındaki hesaplamayı açtınız ve **Stok arama** sayfasında bulunan bir ürünle ilgili eldeki stoğu görüntülediniz. Daha sonra ürünün bir birimi satılıyorsa **Stok arama** sayfası, önbellek temizlenene kadar azalan stoğu göstermez. Kullanıcılar POS'taki hareketleri deftere naklettikten sonra, eldeki stoğun azaldığını doğrulamadan önce 60 saniye beklemelidir.

İş senaryonuz için daha küçük bir önbellek süresi gerekiyorsa yardım için ürün destek temsilcinize başvurun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]