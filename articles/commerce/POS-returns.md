---
title: POS'ta iade oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce Satış Noktasındaki (POS) peşin hareketler veya müşteri siparişleri için iadelerin nasıl başlatılacağı açıklanmıştır.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: 4a0d5efe043d72f936a15ec9a8ead9987fdb22b891a5a3ae94f95aa5ea7a6e67
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715542"
---
# <a name="create-returns-in-pos"></a>POS'ta iade oluşturma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında peşin hareketler veya müşteri siparişleri için iadelerin nasıl başlatılacağı açıklanmıştır.

> [!NOTE]
> Commerce sürüm 10.0.20 ve sonrasında, **POS'ta birleşik iade işleme deneyimi** olarak adlandırılan yeni bir özellik mevcuttur. Bu özellik, hareket türü (peşin hareket veya müşteri siparişi) ya da siparişin oluşturulduğu orijinal kanal dikkate alınmaksızın, POS'de daha tutarlı ve birleşik bir iade süreci sağlar. Tüm kuruluşların, POS'de iade işlemenin genel güvenilirliğini artırmaya yardımcı olmak için bu yeni özelliği açması önerilir.
>
> Özellik, etkinleştirildikten sonra kapatılamaz.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>İade hareketi işlemini kullanarak iadeleri işleme

İade hareketi işlemini POS [ekran düzeninize](pos-screen-layouts.md) eklemenizi öneririz. Commerce 10.0.20 sürümünden önceki sürümlerde, iade hareketi işlemi yalnızca peşin hareketlerin iadelerinin işlenmesini doğru şekilde destekler. Commerce sürümü 10.0.20 veya daha ileri bir sürümde **POS için birleşik iade işleme deneyimi** ni açtıktan sonra iade hareketi işlemi zaten faturalanmış olan "teslim alma" veya "eve teslimat" siparişleri gibi müşteri siparişlerinden kaynaklanan iadelerin işlenmesini de destekler.

Kullanıcılar; iade hareketi işlemini kullanarak, aşağıdaki dört arama ölçütünü girerek, bir peşin hareket veya müşteri siparişini arayabilir. Kullanıcılar bu ölçütleri aygıt klavyesi, ekran üzerindeki tuş takımı veya barkod tarayıcısı kullanarak girebilir.

- Makbuz kodu
- Sipariş numarası
- Kanal referans kodu (sipariş onay kodu olarak da bilinir)
- Fatura kimliği

Arama ölçütleriyle eşleşen bir hareket veya sipariş bulunursa, **İade edilebilir ürünler** sayfası görüntülenir. Burada, kullanıcılar iade edilen maddeleri belirtebilirler. Ayrıca, iade miktarları ve neden kodları da girebilirler.

POS, iade edilebilir ürünler listesindeki her bir sipariş satırı için, orijinal satınalma miktarıyla ilgili bilgileri ve daha önce işlenmiş olan tüm iadelerin miktarlarını gösterir. Bir sipariş satırı için kullanıcının girdiği iade miktarı, **İade edilebililir** alanının değerine eşit veya bundan küçük olmalıdır.

![İade edilebilir ürünler sayfası.](media/returnslist.png)

İade işleme sırasında, bir kullanıcının fiziksel ürünü varsa ve o ürünün bir barkodu varsa, kullanıcı iadeyi kaydetmek için barkodunu tarayabilir. Barkodlar her tarandığında, iade miktarı bir maddeye göre artar. Ancak, barkod etiketinin bir yerleşik miktarı varsa, bu miktar **Şimdi iade edilen** alanına girilir.

Ayrıca, kullanıcılar **İade edilebilir ürünler** sayfasında iade edilecek öğeleri el ile seçebilir ve sonra da sağdaki ayrıntılar bölmesini kullanarak **Şimdi iade edilen** alanını güncelleştirebilir.

Bir hareket için maksimum **Şimdi iade edilen** miktarı belirtildiyse, kullanıcı tüm satırlarda maksimum iade edilebilir miktarı ayarlamak için POS uygulama çubuğundaki **Tümünü seç** işlemini seçebilir.

**Şimdi iade edilen** miktarı olan her satır için, kullanıcının ayrıntılar panelini kullanarak bir iade neden kodu seçmesi gerekir. Peşin hareketlerinin iadesi için, iade neden kodları mağazanın işlevsellik profilinde bilgi kodları olarak yapılandırılabilir. Müşteri siparişlerinin iadesi için, iade neden kodları Dynamics 365 Commerce genel merkezindeki **İade neden kodları** sayfasında yapılandırılır.

İade miktarı ve neden kodu iade edilecek her madde için ayarlandıktan sonra lullanıcı, işleme devam etmek için POS uygulama çubuğundaki **İade** işlemini seçebilir. Bir önceki sayfada seçilmiş olan iade edilebilir maddelerin alışveriş sepetine eklendiği POS hareket sayfası görüntülenir. Maddeler için **Şimdi iade edilen** miktarları, harekette negatif miktar satırları olarak görünür ve toplam para iadesi hesaplanır.

Kullanıcılar, bir döviz kuru siparişi oluşturuyorsa iade hareketine satır ekleyebilirler. Ayrıca, eklenen bir pozitif miktarlı satış satırı için **Ürün iade** işlemini kullanarak, bir iade hareketine başka dinamik iade maddeleri de ekleyebilirler.

> [!NOTE]
> POS'taki **Ürün iadesi** işlemi orijinal hareketlerle ilişkili herhangi bir doğrulama sağlamaz ve tüm ürünlerin iadesine izin verir. Bu nedenle, yalnızca yetkili kullanıcıların bu işlemi gerçekleştirmesine izin verilmesini veya bu işlem kullanılırsa bir yönetici geçersiz kılma işleminin gerekli kılınması önerilir.

Ödeme sırasında ödenmesi gereken bir para iadesi olduğunda, kuruluşlar, müşteri para iadesi için kullanılabilecek ödeme yöntemlerini sınırlayan iade [ödeme ilkelerini](refund_policy_returns.md) yapılandırabilir. Orijinal hareket kredi kartı kullanılarak ödenmişse, ödeme işlemcisine ve sistem yapılandırmasına bağlı olarak, kullanıcılar [orijinal karta para iadesi verme](dev-itpro/linked-refunds.md) seçeneğine sahip olabilirler. Bu durumda para iadesi, müşterinin kredi kartını tekrar okutması gerekmeden işlenebilir. Orijinal ödeme belirteci para iadesini gerçekleştirmek için kullanılır.

## <a name="other-return-options-in-pos"></a>POS'daki diğer iade seçenekleri

**POS'da birleşik iade işleme deneyimi** özelliği açık olduğunda kullanıcılar, peşin hareket veya müşteri siparişi için iade başlatmak amacıyla POS'ta **Günlüğü göster** işlemini de kullanabilirler. Böylece, günlükte bir hareket seçip POS uygulama çubuğunda **İade** işlemini seçebilirler. Bu işlem yalnızca siparişte iade edilebilir satırlar varsa kullanılabilir. **İade hareketi** işlemi ile aynı kullanıcı deneyimini başlatır.

Ayrıca, kullanıcılar müşteri siparişlerini arayıp geri çekmek için POS'taki **Siparişi geri çek** işlemini de kullanabilirler. (Bu işlem, peşin hareketler için kullanılamaz). Bu durumda, bir müşteri siparişi seçildikten sonra, POS uygulama çubuğundaki **İade** işlemi müşteri siparişinin iadesini başlatmak için kullanılabilir. Bu işlem yalnızca siparişte iade edilebilir satırlar varsa kullanılabilir. **İade hareketi** veya **Günlüğü göster** işlemi ile aynı kullanıcı deneyimini başlatır.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>İade siparişleri, Commerce genel merkezine satış siparişleri olarak nakledilir 

**POS'taki birleşik iade işleme deneyimi** özelliği açık olduğunda, POS'ta oluşturulan tüm iadeler, eksi satırları olan satış siparişleri olarak Commerce genel merkezine yazılır. Commerce 10.0.20 sürümünden önceki sürümlerde, kullanıcılar iade siparişlerinin negatif satırlara sahip satış siparişleri olarak mı yoksa iade mal yetki onayı (RMA) işlemi aracılığıyla oluşturulmuş iade emirleri olarak mı deftere nakledilmeleri gerektiğini seçebilir. 

**POS'ta birleşik iade işleme deneyimi** özelliğinde, POS'ta iade oluşturmak için RMA işlemini kullanma seçeneği kullanım dışı bırakıldı. Bu özellik etkinleştirildikten sonra, tüm iadeler negatif satırlar içeren satış siparişleri olarak oluşturulacak.

## <a name="offline-return-processing-improvements"></a>Çevrimdışı iade işleme geliştirmeleri

POS'ta bir iade işlenirken çoğu durumda, sistem Commerce genel merkezine iade için uygun olan geçerli miktarları doğrulayan gerçek zamanlı servis (RTS) çağrısı yapmaya çalışır. Bu doğrulama, bir müşterinin birden fazla konumda aynı maddeyi iade etmeye çalıştığı sahtekarlık senaryolarının engellenmesine yardımcı olur.

Ağ veya bağlantı sorunları nedeniyle RTS çağrısının yapılmadığı durumları işlemek için, Commerce genel merkezinden bir mağazanın kanal veritabanına iade miktarı verilerini düzenli olarak eşitlemek amacıyla bir işlem yer alması yerinde yer alan bir işlemdir. Bu kanal tarafı iade izleme, POS'ta gösterilen **İade edilebilir** miktarların çevrimdışı olması durumunda bile bu miktarların doğru olmasını garanti altına almanıza yardımcı olur. Ayrıca, sahte iadeleri önlemeye yardımcı olmak için POS'un kanal tarafındaki bilgileri doğrulamaya devam etmesini de sağlar.

Bir çevrimdışı iade sürecini uygun şekilde kullanmak için, kuruluşlar Commerce genel merkezinde **İade miktarlarını güncelleştir** toplu işini sık çalışacak şekilde plan yapmalıdır. Bu işin, Commerce kanallarından Commerce genel merkezine yeni hareketler çeken P işiyle aynı frekansta çalıştırılması önerilmektedir.

**İade miktarlarını güncelleştir** işi, Commerce genel merkezinde bulunan tüm satış siparişleri için geçerli iadelerin mevcut miktarını hesaplar. İşin hesapladığı verilerin kanal veritabanlarına gönderilmesi gerekir; böylece mağaza kanalları güncelleştirilebilir. **İade miktarları** (1200) dağıtma işi bu amaç için kullanılır. İade edilebilir miktarla ilgili veriler Commerce genel merkezinden eşitlendiğinden, POS'ta bir iade işlenirse, ancak RTS çağrısı yapılamıyorsa POS, belirli bir satış satırı için **İade edilebilir** miktarları doğrulamak üzere kanal tarafı iade bilgilerini kullanabilir.

RTS çağrıları yapılamadığında ve POS iade doğrulaması için kanal tarafı verilerini kullanıyorsa, bir uyarı iletisi kullanıcıya "çevrimdışı" bir dönüş oluşturduklarını bildirir. Bu nedenle, POS'ta gösterilen **İade edilebilir** miktar, **İade miktarlarını güncelleştir** işinin ne zaman işlendiğine ve kanala eşitlendiğine bağlı olarak eski ve artık doğru olmayabilir.

Örneğin, bir müşteri bir sipariş satırı için başka bir kanaldaki bir iadeyi işlemiştir ancak bu veriler henüz **İade miktarlarını güncelleştir** işiyle ilgili olarak kanal veritabanlarıyla eşitlenmemiştir. Müşteri, daha sonra farklı bir mağazaya gider ve aynı maddeyi tekrar iade etmeye çalışır. Bu durumda, mağaza gerçek zamanlı iade verilerini almak üzere Commerce genel merkezine RTS çağrısı yapamazsa POS, maddenin yeniden iade edilmesine izin verir. Ancak, kullanıcı iadeyi doğrulamak için kullanılan bilgilerin güncel olmadığıyla ilgili uyarılır. Kullanıcının aldığı ileti yalnızca bir uyarı iletisidir. Kullanıcının, iadeyi işlemeye devam etmesini engellemez.

Kanal tarafı bilgileri herhangi bir nedenle güncel değilse ve çevrimdışı iade, gerçek **İade edilebilir** miktarı aşan bir miktarla iade edilirse Commerce genel merkezinde hareketi oluşturmak üzere bir ekstre deftere nakil işi yürütüldüğünde bir hata verilebilir.

> [!NOTE]
> **POS'ta birleşik işlem deneyimi** özelliği açıldığında, serileştirilmiş ürün iadelerinin doğrulanmasını destekleyen yeni isteğe bağlı özellikler kullanılabilir duruma gelir. Daha fazla bilgi için bkz. [Satış noktasında (POS) seri numarası denetimli ürünleri iade etme](POS-serial-returns.md).

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Kısmi miktarlı iadeler için doğru vergi hesaplamasını etkinleştirme

Bu özellik, bir sipariş birden çok fatura kullanılarak iade edildiğinde, vergilerin sonunda uygulanan vergi tutarına eşit olmasını sağlar.
1.  **Özellik yönetimi** çalışma alanına gidin ve **Kısmi miktarlı iadeler için uygun vergi hesaplamasını etkinleştir**'i arayın.
2.  **Kısmi miktarlı iadelerle ilgili doğru vergi hesaplamasını etkinleştir**'ı seçin ve ardından **Etkinleştir**'e tıklayın.


## <a name="additional-resources"></a>Ek kaynaklar

[Satış noktasında (POS) seri numarası denetimli ürünleri iade etme](POS-serial-returns.md)

[Önceden onaylanmış ve doğrulanmış hareketlerin bağlı iadesi](dev-itpro/linked-refunds.md)

[Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme](refund_policy_returns.md)

[POS kullanıcı arabirimi görsel yapılandırmaları](pos-screen-layouts.md)
