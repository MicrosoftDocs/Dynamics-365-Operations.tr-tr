---
title: Satış noktasındaki (POS) müşteri siparişleri
description: Bu makalede, satış noktasındaki (POS) müşteri siparişleri hakkında bilgi sağlanmaktadır. Müşteri siparişleri, özel siparişler olarak da adlandırılır. Bu makale, ilgili parametreler ve hareket akışları hakkında bir tartışma içerir.
author: josaw1
ms.date: 08/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260594"
- intro-internal
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6051e0a18823b354dd9940aac70a086a0f317002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850394"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Satış noktasındaki (POS) müşteri siparişleri

[!include [banner](includes/banner.md)]

Bu makalede, satış noktası (POS) uygulamasında müşteri siparişlerinin nasıl oluşturulup yönetileceği ile ilgili bilgi sağlanmaktadır. Müşteri siparişleri, alışverişçilerin sonraki bir tarihte ürün çekmek, farklı bir konumdan ürünü çekmek veya maddelerin kendilerine gönderilmelerini sağlamak istedikleri satışları yakalamak için kullanılabilir. 

Çok kanallı ticaret dünyasında pek çok perakendeci, çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için müşteri siparişleri seçeneği veya özel siparişler sağlar. Burada bazı tipik senaryolar vardır:

- Bir müşteri, ürünler belirli bir tarihte belirli bir adrese teslim edilmesini istiyor.
- Bir müşteri, ürünleri, müşterinin satın aldığı mağazadan başka bir konumda bulunan bir mağazadan teslim almak istiyor.
- Bir mağaza konumundaki müşteri, ürünleri bugünden sipariş vermek ve bunları daha sonraki bir tarihte aynı mağaza konumundan çekmek istiyor.

Ayrıca, ürünler farklı bir zaman veya yerde teslim edilebileceğinden veya çekilebileceğinden perakendeciler müşteri siparişlerini, tükenen stokların neden olabileceği satış kayıplarını en aza indirmek için kullanabilir.

## <a name="set-up-customer-orders"></a>Müşteri siparişleri ayarlamak
POS'ta müşteri siparişi işlevini kullanmayı denemeden önce, Commerce yönetim merkezinde gerekli tüm yapılandırmaları tamamladığınızdan emin olun.

### <a name="configure-modes-of-delivery"></a>Teslimat şekillerini yapılandırma

Müşteri siparişlerini kullanmak için, mağaza kanalının kullanabileceği teslimat şekillerini yapılandırmalısınız. Bir mağazadan sipariş satırları müşteriye sevk edildiğinde kullanılabilecek en az bir teslimat şeklini tanımlamalısınız. Ayrıca sipariş satırları bir mağazadan çekildiğinde kullanılabilecek en az bir teslimatın alma şeklini tanımlamalısınız. Teslimat şekilleri Commerce yönetim merkezinde **Teslimat şekilleri** sayfasında tanımlanır. Commerce kanalları için teslimat şeklinin yapılandırılmasına ilişkin daha fazla bilgi için bkz. [Teslimat şekillerini tanımlama](./configure-call-center-delivery.md#define-delivery-modes).

![Teslimat şekilleri sayfası.](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Karşılama gruplarını ayarlama

Bazı mağazalar veya depo konumları müşteri siparişlerini karşılamayabilir. Bir kuruluş, karşılama gruplarını yapılandırarak, POS'ta müşteri siparişleri oluşturan kullanıcılara gösterilecek mağaza ve depoları konumu seçeneklerini belirtebilir. Karşılama grupları, **Karşılama grupları** sayfasında yapılandırılır. Kuruluşlar, gereksinim duydukları sayıda karşılama grubu oluşturabilir. Bir karşılama grubu tanımlandıktan sonra, **Mağazalar** sayfasının Eylem Bölmesindeki **Kurulum** sekmesinden **Karşılama grubu ataması**'nı seçerek grubu bir mağazaya bağlayın.

Commerce 10.0.12 ve sonraki sürümlerde kuruluşlar, karşılama gruplarında tanımlanan depo veya depo ve mağaza birleşimlerinin sevkiyat, malzeme çekme veya sevkiyat ve malzeme çekme için kullanılıp kullanılmayacağını tanımlayabilir. Bu, sevk edilecek maddeler için müşteri siparişi oluştururken işletmenin hangi ambarların seçilebileceğini ve maddelerin teslim alınması için bir müşteri siparişi oluştururken hangi mağazaların seçilebileceğini belirlemesi için ek esneklik sağlar. Bu yapılandırma seçenekleri kullanmak için **Karşılama grubundan etkinleştirilen "Sevkiyat" veya "Çekme" olarak konumun belirtilebilmesi"** özelliğini etkinleştirmelisiniz. Bir karşılama grubuna bağlı depo bir mağaza değilse, yalnızca sevkiyat konumu olarak yapılandırılabilir. Malzeme çekme için siparişler POS'ta yapılandırıldığında kullanılamaz.

![Karşılama grupları sayfası.](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanal ayarlarını yapılandırma

POS'ta müşteri siparişleri ile çalışırken, mağaza kanalının bazı ayarlarına dikkat etmeniz gerekir. Bu ayarlar, Commerce yönetim merkezindeki **Mağazalar** sayfasında bulunur.

- **Ambar**: Bu alan, bu mağazaya bağlı nakit ve müşteri malzeme çekme emirleri için stok küçültmekte kullanılacak ambarı gösterir. En iyi yöntem olarak, mağazalar boyunca çakışan iş mantığı sorunlarını önlemek için, her bir mağaza kanalının benzersiz ambarların kullanımını öneririz.
- **Sevkiyat Ambarı**: Bu alan, seçilen mağazadan gönderilecek müşteri siparişleri için stok küçültmekte kullanılacak ambarı gösterir. Ortamınızda, **Karşılama grubunda yerleşimleri "Sevkiyat" veya "Malzeme çekme" etkin olarak belirtme özelliği** etkinleştirilmişse , POS kullanıcıları, sevkiyatın yapılacağı bir mağaza seçmek yerine, POS'tan sevk etmek için belirli bir ambar seçebilirler. Bu nedenle, bu özellik etkinleştirildiğinde, siparişin oluşturulduğu sırada Kullanıcı siparişi sevk etmek için belirli bir ambarı seçeneği için sevkiyat ambarı artık kullanılmaz.
- **Karşılama grubu ataması**: POS'ta müşteri siparişleri oluşturulurken malzeme çekme konumları veya sevkiyat kaynakları için seçenekleri göstermek üzere referans gösterilen karşılama gruplarını bağlamak için bu düğmeyi seçin (Eylem Bölmesi'ndeki **Kurulum** sekmesinde).
- **Hedef esaslı vergi kullan**: Bu seçenek, sevkiyat adresinin, müşterinin adresine sevk edilen sipariş satırlarına uygulanacak vergi grubunu belirlemek için teslimat adresinin kullanılıp kullanılmayacağını gösterir.
- **Müşteri tabanlı vergi kullan**: Bu seçenek, müşterinin teslimat adresi için tanımlanan vergi grubunun evine sevkiyat için POS'ta oluşturulan müşteri siparişlerinin vergilendirilmesi için kullanılıp kullanılmayacağını gösterir.

![Mağazalar sayfasında mağaza kanalı kurulumu.](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Müşteri sipariş parametrelerini ayarlama

POS'ta müşteri siparişlerini oluşturmayı denemeden önce, Commerce yönetim merkezinde uygun parametreleri yapılandırmalısınız. Bu parametreler, **Commerce parametreleri** sayfasının **Müşteri siparişleri** sekmesinde bulunabilir.

- **Varsayılan sipariş türü**: POS'ta oluşturulan müşteri siparişlerine varsayılan olarak atanan sipariş türünü belirtebilirsiniz. Bu müşteri siparişleri satış siparişleri veya teklif siparişleri olabilir. Varsayılan sipariş türüne bakılmaksızın, kullanıcılar POS'tan satış siparişleri ve müşteri siparişleri oluşturmaya devam edebilir.
- **Varsayılan depozito yüzdesi**: Siparişin onaylanabilmesi için müşterinin depozito olarak ödemesi gereken sipariş toplamının yüzdesini belirtin. Ayrıcalıklarına bağlı olarak mağaza görevlilerinin, işlem hareket ekran düzeni için yapılandırılmışsa, POS'ta **Havale geçersiz kılma** işlemini kullanarak tutarı geçersiz kılabilir.
- **Teslimat alma şekli**: POS'ta malzeme çekme için yapılandırılmış satış siparişi satırlarına uygulanması gereken teslimat şeklini belirtin.
- **Carryout teslimat alınma şekli**: Bazı satırların teslim alma, bazı satırların sevkiyat ve bazılarının da anında müşteri tarafından alınma olacak şekilde karma bir sepet oluşturulduğunda teslim alınan sipariş satırları olarak kabul edilen satış siparişi satırlarına uygulanması gereken teslimat şeklini belirtin.
- **İptal ücreti yüzdesi**: Müşteri siparişi iptal edildiğinde, bir ücret uygulanacaksa bu tutarı belirtin.
- **İptal masrafı kodu**: POS ile iptal edilen müşteri siparişleri için iptal gideri uygulandığında kullanılması gereken Alacak hesapları gider kodunu belirtin. Masraf kodu, iptal masrafı için mali deftere nakil mantığını tanımlar.
- **Sevkiyat masrafı kodu**: **Gelişmiş otomatik masrafları kullan** seçeneği **Evet** olarak ayarlanmışsa, bu parametre ayarının hiçbir etkisi olmaz. Bu seçenek **Hayır** olarak ayarlanmışsa, kullanıcılardan POS'ta müşteri siparişleri oluştururken, sevkiyat masraflarını el ile girmeleri istenir. Kullanıcılar bir sevkiyat masrafı girdiğinde siparişlere uygulanacak Alacak hesapları gider kodunu eşlemek için bu parametreyi kullanın. Masraf kodu, sevkiyat masrafı için mali deftere nakil mantığını tanımlar.
- **Gelişmiş otomatik masrafları kullan**: POS'ta müşteri siparişleri oluşturulurken sistem tarafından hesaplanan otomatik masrafları kullanmak için bu seçeneği **Evet** olarak ayarlayın. Otomatik masraflar, sevkiyat ücretlerini ve diğer sipariş veya maddeye özel masrafları hesaplamak için kullanılabilir. Gelişmiş otomatik masrafları özelliğini ayarlama ve kullanma hakkında bilgi için bkz. [Çok yönlü kanal gelişmiş otomatik masrafları](./omni-auto-charges.md).

![Commerce parametreleri sayfasındaki müşteri siparişleri sekmesi.](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>POS'ta hareket ekran düzenlerini güncelleştirme

POS [ekran düzeninin](./pos-screen-layouts.md), müşteri siparişlerinin oluşturulmasını ve yönetilmesini destekleyecek şekilde yapılandırıldığından ve gerekli tüm POS işlemlerinin yapılandırıldığından emin olun. Müşteri siparişi oluşturma ve yönetimini doğru şekilde desteklemek için önerilen POS işlemlerinden bazıları şunlardır:
- **Tüm ürünleri sevk et**: Bu işlem, hareket sepetindeki tüm satırların bir hedefe sevk edileceğini belirtmek için kullanılır.
- **Seçili ürünleri sevk et**: Bu işlem, hareket sepetindeki seçili satırların bir hedefe sevk edileceğini belirtmek için kullanılır.
- **Tüm ürünleri çek**: Bu işlem, hareket sepetindeki tüm satırların seçili bir mağaza konumundan çekileceğini belirtmek için kullanılır.
- **Seçili ürünleri çek**: Bu işlem, hareket sepetindeki seçili satırların seçili bir mağaza konumundan çekileceğini belirtmek için kullanılır.
- **Tüm ürünleri teslim al**: Bu işlem, hareket sepetindeki tüm satırların teslim alınacağını için belirtmek kullanılır. POS'ta bu işlem kullanılırsa, müşteri siparişi öde ve al hareketine dönüştürülür.
- **Seçili ürünleri teslim al**: Bu işlem, hareket sepetindeki seçili satırların, satınalma sırasında müşteri tarafından satın alınacağını belirtmek için kullanılır. Bu işlemden yalnızca [karma sipariş](./hybrid-customer-orders.md) senaryosunda yararlanılır.
- **Siparişi geri çağır**: Bu işlem, müşteri siparişlerini aramak ve getirmek için kullanılır, böylece POS kullanıcıları gerektiğinde karşılama ile ilgili işlemlerini düzenleyebilir, iptal edebilir veya gerçekleştirebilir.
- **Teslimat şeklini değiştir**: Bu işlem, önceden sevkiyat için yapılandırılmış olan satırlar için teslimat şeklini, kullanıcıların "tüm ürünleri sevk et" veya "seçilen ürünleri sevk et" akışının aşamalarının üzerinden yeniden geçmelerine gerek kalmadan teslim etme modunu hızla değiştirmek için kullanılabilir.
- **Havale geçersiz kılma**: Bu işlem, müşterinin seçili müşteri siparişi için ödeyeceği depozito tutarını değiştirmek için kullanılabilir.

![POS hareket ekranındaki işlemler.](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>POS'ta müşteri siparişleriyle çalışma

> [!NOTE]
> Gelir kabulü işlevi şu anda Ticaret kanallarında (e-ticaret, POS, çağrı merkezi) kullanım için desteklenmiyor. Gelir kabulü ile konfigüre edilen maddeler, Ticaret kanallarında oluşturulan siparişlere eklenemez. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Müşteriye sevk edilecek ürünler için bir müşteri siparişi oluşturma

1. POS hareket ekranında harekete bir müşteri ekleyin.
2. Sepete ürünler ekle.
3. Ürünleri müşteri hesabındaki bir adrese sevk etmek için **Seçileni sevk et** veya **Tümünü sevk et** seçeneğini belirleyin.
4. Müşteri siparişinin oluşturulacağı seçeneği belirleyin.
5. "Sevk çıkış yeri" konumunu doğrulayın veya değiştirin, sevkiyat adresini onaylayın veya değiştirin ve bir sevkiyat yöntemi seçin.
6. Müşterinin istediği sipariş sevkiyat tarihini girin.
7. Vadesi gelen hesaplanmış tutarların ödemesini yapmak için ödeme işlevlerini kullanın veya vadesi gelen miktarları değiştirmek için **Havale geçersiz kılma** işlemini kullanın ve sonra ödemeyi uygulayın.
8. Tam sipariş toplamı ödenmediyse, faturalandığı sırada siparişle ilgili vadesi dolan bakiye için yakalanacak bir kredi kartı girin.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Müşterinin çekeceği ürünler için bir müşteri siparişi oluşturma

1. POS hareket ekranında harekete bir müşteri ekleyin.
2. Sepete ürünler ekle.
3. Siparişe ait malzeme çekme yapılandırmasını başlatmak için **Seçileni çek** veya **Tümünü çek** seçeneğini belirleyin.
4. Müşterinin seçili ürünleri çekeceği mağaza konumu seçin.
5. Maddenin çekilmesi için bir tarih seçin.
6. Vadesi gelen hesaplanmış tutarların ödemesini yapmak için ödeme işlevlerini kullanın veya vadesi gelen miktarları değiştirmek için **Havale geçersiz kılma** işlemini kullanın ve sonra ödemeyi uygulayın.
7. Tam sipariş toplamı ödenmediyse, müşterinin ödemeyi daha sonra (malzeme çekme sırasında) sağlayıp sağlamayacağını veya kredi kartı bilgilerinin güvenli şekilde saklanarak ve malzeme çekme sırasında kullanılıp çekim yapılıp yapılmayacağını seçin.

### <a name="edit-an-existing-customer-order"></a>Geçerli bir müşteri siparişini düzenle

Çevrimiçi veya mağaza kanalında oluşturulan perakende siparişleri gerektiğinde, POS aracılığıyla geri çekilebilir ve düzenlenebilir.

> [!IMPORTANT]
> Tüm perakende siparişler POS uygulaması aracılığıyla düzenlenemez. Çağrı merkezi kanalında oluşturulan siparişler, bu kanalda [Sipariş tamamlamayı etkinleştir](./set-up-order-processing-options.md#enable-order-completion) ayarı açıksa, POS üzerinden düzenlenemez. Doğru ödeme işleminin yapıldığından emin olmak için, bir çağrı merkezi kanalında oluşturulan ve Sipariş tamamlamayı etkinleştirme işlevini kullanan siparişlerin Commerce Headquarters'da çağrı merkezi uygulaması aracılığıyla düzenlenmesi gerekir.

> [!NOTE]
> Commerce genel merkezinde çağrı merkezi dışı bir kullanıcı tarafından oluşturulan POS'ta sipariş ve teklifleri düzenlememenizi öneririz. Bu siparişler ve teklifler, Commerce fiyatlandırma altyapısını kullanmaz. Bu nedenle, POS'ta düzenlendiklerinde Commerce fiyatlandırma altyapısı bunları yeniden fiyatlandırır.


Sürüm 10.0.17 ve sonrasında, kullanıcılar,sipariş kısmen karşılanabilse bile POS uygulaması üzerinden uygun siparişleri düzenleyebilir. Ancak, tamamen faturalanmış siparişler POS üzerinden düzenlenemez. Bu özelliği etkinleştirmek için **Özellik yönetimi** çalışma alanında **Satış Noktası'nda kısmen karşılanmış siparişleri düzenle** özelliğini açın. Bu özellik etkin değilse veya sürüm 10.0.16 veya öncesini kullanıyorsanız kullanıcılar yalnızca sipariş tam olarak açıksa POS'ta müşteri siparişlerini düzenleyebilirler. Ayrıca, özellik etkinleştirildiğinde, hangi mağazaların kısmi olarak karşılanan siparişleri düzenleyebileceğini sınırlayabilirsiniz. Belirli mağazalar için bu özelliği devre dışı bırakma seçeneği, **Genel** hızlı sekmesi altındaki **İşlevsellik profili** aracılığıyla konfigüre edilebilir.


1. **Siparişi geri çağır** seçeneğini belirleyin.
2. Siparişi bulmak için filtre girmek üzere **Ara**'yı kullanın ve sonra **Uygula** seçeneğini belirleyin.
3. Sonuç listesinden siparişi seçin ve sonra **Düzenle**'yi seçin. **Düzenle** düğmesi kullanılamıyorsa, sipariş düzenlenmenin mümkün olmadığı bir durumdadır.
4. Hareket sepetinden, müşteri siparişinde gerekli tüm değişiklikleri yapın. Bazı değişiklikler düzenleme sırasında yasaklanmış olabilir.
5. Ödeme işlemini seçerek düzenleme işlemini tamamlayın.
6. Herhangi bir değişiklik yapmadan düzenleme işleminden çıkmak için, **Hareketi hükümsüz kıl** işlemini kullanabilirsiniz.

#### <a name="pricing-impact-when-orders-are-edited"></a>Siparişler düzenlendiğinde fiyatlandırma etkisi

Siparişler POS'ta veya bir Commerce e-ticaret sitesinde verildiğinde müşteriler bir tutar taahhüt eder. Bu tutar bir fiyat içerir ve ayrıca bir iskonto da içerebilir. Sipariş veren ve ardından bu siparişi değiştirmek için (örneğin, başka bir öğe eklemek için) çağrı merkeziyle iletişime geçen müşteri, iskonto uygulanması konusunda belirli beklentilere sahiptir. Mevcut sipariş satırlarındaki promosyonların süresi dolsa bile müşteri, başlangıçta bu satırlara uygulanan iskontoların etkin kalmasını bekler. Ancak sipariş başlangıçta verildiğinde etkin iskonto yoksa ancak bu tarihten sonra bir iskonto yürürlüğe girdiyse müşteri, yeni iskontonun değiştirilen siparişe uygulanmasını bekler. Aksi takdirde müşteri, mevcut siparişi iptal edebilir ve ardından yeni iskontonun uygulandığı yeni bir sipariş oluşturabilir. Bu senaryoda, müşterilerin taahhüt ettiği fiyatların ve iskontoların korunması gerektiği gösterilmektedir. Aynı zamanda POS ve çağrı merkezi kullanıcıları, satış siparişi satırlarının fiyatlarını ve iskontolarını gerektiği gibi yeniden hesaplama esnekliğine sahip olmalıdır.

POS'ta siparişler geri çekilip düzenlendiğinde mevcut sipariş satırlarının fiyatları ve iskontoları "kilitli" olarak kabul edilir. Diğer bir deyişle, bazı sipariş satırları iptal edilmiş veya değiştirilmiş olsa da ya da yeni sipariş satırları eklense bile bunlar değişmez. Mevcut satış satırlarının fiyatlarını ve iskontolarını değiştirmek için POS kullanıcısı, **Yeniden Hesapla** seçeneğini belirlemelidir. Ardından fiyat kilidi, mevcut sipariş satırlarından kaldırılır. Ancak Commerce 10.0.21 sürümünden önce çağrı merkezinde bu özellik kullanılamıyordu. Bunun yerine, sipariş satırlarındaki tüm değişiklikler fiyatların ve iskontoların yeniden hesaplanmasına neden oluyordu.

Commerce 10.0.21 sürümünde, **Özellik yönetimi** çalışma alanında **Ticari siparişler için istenmeyen fiyat hesaplamasını engelle** adlı yeni bir özellik kullanılabilir. Bu özellik, varsayılan olarak açıktır. Açıldığında tüm e-ticaret siparişleri için yeni bir **Fiyat kilitli** özelliği kullanılabilir. Herhangi bir kanaldan verilen siparişler için sipariş yakalama tamamlandıktan sonra bu özellik tüm sipariş satırları için otomatik olarak etkinleştirilir (yani, onay kutusu seçilidir). Daha sonra Commerce fiyatlandırma altyapısı bu sipariş satırlarını tüm fiyat ve iskonto hesaplamalarından hariç tutar. Bu nedenle, sipariş düzenlendiğinde sipariş satırları varsayılan olarak fiyatlandırma ve iskonto hesaplamasından hariç tutulur. Ancak çağrı merkezi kullanıcıları, sipariş satırları için özelliği devre dışı bırakabilir (yani onay kutusunun işaretini kaldırabilir) ve ardından mevcut sipariş satırlarını fiyatlandırma hesaplamalarına dahil etmek için **Yeniden Hesapla** seçeneğini belirleyebilir.

Mevcut bir sipariş satırına el ile iskonto uygularken bile çağrı merkezi kullanıcılarının, iskontoyu uygulamadan önce satış satırının **Fiyat kilitli** özelliğini devre dışı bırakması gerekir.

Çağrı merkezi kullanıcıları ayrıca **Satış siparişi** sayfasının Eylem Bölmesi'ndeki **Satış** sekmesinde **Hesapla** grubundaki **Fiyat kilidini kaldır** seçeneğini belirleyerek de toplu olarak sipariş satırları için **Fiyat kilitli** özelliğini devre dışı bırakabilir. Bu durumda fiyat kilidi, düzenlenebilir olmayan satırlar (diğer bir deyişle, **Kısmen faturalandı** veya **Faturalandı** durumuna sahip satırlar) haricinde tüm sipariş satırlarından kaldırılır. Ardından, siparişteki değişiklikler tamamlanıp gönderildikten sonra fiyat kilidi tüm sipariş satırlarına yeniden uygulanır.

> [!IMPORTANT]
> **Ticari siparişler için istenmeyen fiyat hesaplamasını engelle** özelliği açıldığında, fiyatlandırma iş akışlarında ticari sözleşme değerlendirmesi kurulumu yok sayılır. Diğer bir deyişle, ticari sözleşme değerlendirmesi iletişim kutusunda **Fiyat kilitli** bölümü gösterilmez. Bu davranış, ticari sözleşme değerlendirmesi kurulumunun ve fiyat kilidi özelliğinin benzer bir amaca sahip olması nedeniyle gerçekleşir: istenmeyen fiyat değişikliklerini önlemek. Ancak ticari sözleşme değerlendirmesi için kullanıcı deneyimi, kullanıcıların yeniden fiyatlandırma amacıyla bir veya daha fazla sipariş satırı seçmesinin gerektiği büyük siparişlerde iyi ölçeklenmez.

> [!NOTE]
> **Fiyat kilitli** özelliği yalnızca **Çağrı merkezi** modülü kullanıldığında bir veya daha fazla seçili satır için devre dışı bırakılabilir. POS'un davranışı değişmeden kalır. Diğer bir deyişle, POS kullanıcısı seçili sipariş satırları için fiyatların kilidini açamaz. Ancak mevcut tüm sipariş satırlarından fiyat kilidini kaldırmak için **Yeniden Hesapla** seçeneğini belirleyebilir.

### <a name="cancel-a-customer-order"></a>Müşteri siparişini iptal etme

1. **Siparişi geri çağır** seçeneğini belirleyin.
2. Siparişi bulmak için filtre girmek üzere **Ara**'yı kullanın ve sonra **Uygula** seçeneğini belirleyin.
3. Sonuç listesinden siparişi seçin ve sonra **İptal**'i seçin. **İptal** düğmesi kullanılamıyorsa sipariş, iptal edilmesinin artık mümkün olmadığı bir durumdadır.
4. İptal masraflarının yapılandırılması durumunda, bunları onaylayın. Gerektiğinde iptal masraflarını onaylamadan önce, ayarlayabilirsiniz. 
5. Hareket sepetinden, bir ödeme işlemi seçerek iptal işlemini tamamlayın. Ödenen depozitolar iptal masrafını aşarsa, iade ödemelerinin yapılması gerekebilir.
6. Herhangi bir değişiklik yapmadan iptal işleminden çıkmak için, **Hareketi hükümsüz kıl** işlemini kullanabilirsiniz.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>POS'tan müşteri sipariş sevkiyatını veya malzeme çekmeyi sonlandırma

Bir sipariş oluşturulduktan sonra, maddeler müşteri tarafından bir mağaza konumundan çekilir veya siparişin yapılandırmasına bağlı olarak sevk edilir. Bu işlem hakkında daha fazla bilgi edinmek için [mağaza sipariş karşılama](./order-fulfillment-overview.md) belgelerine bakın.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Müşteri siparişleri için zaman uyumsuz işlem akışı

Müşteri siparişleri POS'ta zaman uyumlu ya da zaman uyumsuz modda oluşturulabilir. POS'ta müşteri siparişleri oluştururken performans sorunları veya kullanıcı gecikmeleri fark ederseniz, zaman uyumsuz sipariş oluşturmayı etkinleştirmeyi düşünebilirsiniz.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Müşteri siparişlerinin zaman uyumsuz modunda oluşturulmasını etkinleştirin

1. Commerce yönetim merkezinde, **İşlev profilleri** sayfasında, yapılandırmak istediğiniz mağazaya karşılık gelen işlevsellik profilini seçin.
2. **Genel** hızlı sekmesi üzerinde, **Müşteri siparişlerini zaman uyumsuz modda oluştur** seçeneğini **Evet** olarak ayarlayın.

**Müşteri siparişlerini zaman uyumsuz** moda oluştur seçeneği **Evet** olarak ayarlanmışsa, müşteri siparişleri her defasında zaman uyumsuz modda oluşturulur, Retail Transaction ServicePerakende İşlem Hizmeti (RTS) etkin olsa bile. Bu seçeneği **Hayır** olarak ayarlarsanız, müşteri siparişleri her defasında zaman uyumlu modda RTS kullanarak oluşturulur. Müşteri siparişleri zaman uyumsuz modda oluşturulduğunda, Commerce Pull (P) işlerinden Commerce Headquarters'da perakende satış hareketleri olarak çekilir ve oluşturulur. **Siparişleri eşitle** elle veya toplu bir iş aracılığıyla çalıştırıldığında perakende hareketlerine ait karşılık gelen satış siparişleri oluşturulur.

## <a name="additional-resources"></a>Ek kaynaklar

[Karma müşteri siparişleri](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
