---
title: Satış Noktası'ndaki (POS) müşteri siparişleri
description: Bu konuda, Satış Noktası'ndaki (POS) müşteri siparişleri hakkında bilgi verilir. Müşteri siparişleri, özel siparişler olarak da adlandırılır. Bu konu, ilgili parametreler ve hareket akışları hakkında bir tartışma içerir.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 30e4dc0a45f7de5f0a7178b1e88f7c3d61a7395e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763713"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Satış Noktası'ndaki (POS) müşteri siparişleri

[!include [banner](includes/banner.md)]

Bu konuda, Satış Noktası'ndaki (POS) müşteri siparişlerinin nasıl oluşturulup yönetileceği ile ilgili bilgi verilir. Müşteri siparişleri, alışverişçilerin sonraki bir tarihte ürün çekmek, farklı bir konumdan ürünü çekmek veya maddelerin kendilerine gönderilmelerini sağlamak istedikleri satışları yakalamak için kullanılabilir. 

Çok kanallı ticaret dünyasında pek çok perakendeci, çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için müşteri siparişleri seçeneği veya özel siparişler sağlar. Burada bazı tipik senaryolar vardır:

- Bir müşteri, ürünler belirli bir tarihte belirli bir adrese teslim edilmesini istiyor.
- Bir müşteri, ürünleri, müşterinin satın aldığı mağazadan başka bir konumda bulunan bir mağazadan teslim almak istiyor.
- Bir mağaza konumundaki müşteri, ürünleri bugünden sipariş vermek ve bunları daha sonraki bir tarihte aynı mağaza konumundan çekmek istiyor.

Ayrıca, ürünler farklı bir zaman veya yerde teslim edilebileceğinden veya çekilebileceğinden perakendeciler müşteri siparişlerini, tükenen stokların neden olabileceği satış kayıplarını en aza indirmek için kullanabilir.

## <a name="set-up-customer-orders"></a>Müşteri siparişleri ayarlamak
POS'ta müşteri siparişi işlevini kullanmayı denemeden önce, Commerce yönetim merkezinde gerekli tüm yapılandırmaları tamamladığınızdan emin olun.

### <a name="configure-modes-of-delivery"></a>Teslimat şekillerini yapılandırma

Müşteri siparişlerini kullanmak için, mağaza kanalının kullanabileceği teslimat şekillerini yapılandırmalısınız. Bir mağazadan sipariş satırları müşteriye sevk edildiğinde kullanılabilecek en az bir teslimat şeklini tanımlamalısınız. Ayrıca sipariş satırları bir mağazadan çekildiğinde kullanılabilecek en az bir teslimatın alma şeklini tanımlamalısınız. Teslimat şekilleri Commerce yönetim merkezinde **Teslimat şekilleri** sayfasında tanımlanır. Commerce kanalları için teslimat şeklinin yapılandırılmasına ilişkin daha fazla bilgi için bkz. [Teslimat şekillerini tanımlama](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Teslimat şekilleri sayfası](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Karşılama gruplarını ayarlama

Bazı mağazalar veya depo konumları müşteri siparişlerini karşılamayabilir. Bir kuruluş, karşılama gruplarını yapılandırarak, POS'ta müşteri siparişleri oluşturan kullanıcılara gösterilecek mağaza ve depoları konumu seçeneklerini belirtebilir. Karşılama grupları, **Karşılama grupları** sayfasında yapılandırılır. Kuruluşlar, gereksinim duydukları sayıda karşılama grubu oluşturabilir. Bir karşılama grubu tanımlandıktan sonra, **Mağazalar** sayfasının Eylem Bölmesi'ndeki **Kurulum** sekmesinde bulunan bir düğme kullanılarak bir mağazaya bağlanır.

Commerce 10.0.12 ve sonraki sürümlerde kuruluşlar, karşılama gruplarında tanımlanan depo veya depo/mağaza birleşimlerinin sevkiyat, malzeme çekme veya sevkiyat ve malzeme çekme için kullanılıp kullanılmayacağını tanımlayabilir. Bu nedenle mağaza, konumdan veya sevkiyatla alınacak sipariş oluşturan kullanıcılarına gösterilecek depo ve mağaza seçeneklerini sunan ek esnekliği sağlar. Bu yapılandırma seçeneklerinden yararlanabilmek için, **Karşılama grubundan etkinleştirilen "Sevkiyat" veya "Çekme" olarak konumun belirtilebilmesi"** özelliğini etkinleştirmelisiniz. Bir karşılama grubuna bağlanan depo bir mağaza değilse, yalnızca sevkiyat konumu olarak yapılandırılabilir. Malzeme çekme için siparişler POS'ta yapılandırıldığında kullanılamaz.

![Karşılama grupları sayfası](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanal ayarlarını yapılandırma

POS'ta müşteri siparişleri ile çalışırken, mağaza kanalının bazı ayarlarına dikkat etmeniz gerekir. Bu ayarlar, Commerce yönetim merkezindeki **Mağazalar** sayfasında bulunur.

- **Ambar**: Bu alan, mağazadan sevkiyat için yapılandırılmış siparişleri karşılamak için kullanılacak ambarı gösterir.
- **Karşılama grubu ataması**: POS'ta müşteri siparişleri oluşturulurken malzeme çekme konumları veya sevkiyat kaynakları için seçenekleri göstermek üzere referans gösterilen karşılama gruplarını bağlamak için bu düğmeyi seçin (Eylem Bölmesi'ndeki **Kurulum** sekmesinde).
- **Hedef esaslı vergi kullan**: Bu seçenek, sevkiyat adresinin, müşterinin adresine sevk edilen sipariş satırlarına uygulanacak vergi grubunu belirlemek için teslimat adresinin kullanılıp kullanılmayacağını gösterir.
- **Müşteri tabanlı vergi kullan**: Bu seçenek, müşterinin teslimat adresi için tanımlanan vergi grubunun evine sevkiyat için POS'ta oluşturulan müşteri siparişlerinin vergilendirilmesi için kullanılıp kullanılmayacağını gösterir.

![Mağazalar sayfasında mağaza kanalı kurulumu](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Müşteri sipariş parametrelerini ayarlama

POS'ta müşteri siparişlerini oluşturmayı denemeden önce, Commerce yönetim merkezinde uygun parametreleri yapılandırmalısınız. Bu parametreler, **Commerce parametreleri** sayfasının **Müşteri siparişleri** sekmesinde bulunabilir.

- **Varsayılan sipariş türü**: POS'ta oluşturulan müşteri siparişlerine varsayılan olarak atanan sipariş türünü belirtebilirsiniz. Bu müşteri siparişleri satış siparişleri veya teklif siparişleri olabilir. Varsayılan sipariş türüne bakılmaksızın, kullanıcılar POS'tan satış siparişleri ve müşteri siparişleri oluşturmaya devam edebilir.
- **Varsayılan depozito yüzdesi**: Siparişin onaylanabilmesi için müşterinin depozito olarak ödemesi gereken sipariş toplamının yüzdesini belirtin. Ayrıcalıklarına bağlı olarak mağaza görevlilerinin, işlem hareket ekran düzeni için yapılandırılmışsa, POS'ta **Havale geçersiz kılma** işlemini kullanarak tutarı geçersiz kılabilir.
- **Teslimat alma şekli**: POS'ta malzeme çekme için yapılandırılmış satış siparişi satırlarına uygulanması gereken teslimat şeklini belirtin.
- **Carryout teslimat alınma şekli**: Bazı satırların teslim alma, bazı satırların sevkiyat ve bazılarının da anında müşteri tarafından alınma olacak şekilde karma bir sepet oluşturulduğunda teslim alınan sipariş satırları olarak kabul edilen satış siparişi satırlarına uygulanması gereken teslimat şeklini belirtin.
- **İptal ücreti yüzdesi**: Müşteri siparişi iptal edildiğinde, bir ücret uygulanacaksa bu tutarı belirtin.
- **İptal masrafı kodu**: POS ile iptal edilen müşteri siparişleri için iptal gideri uygulandığında kullanılması gereken Alacak hesapları gider kodunu belirtin. Masraf kodu, iptal masrafı için mali deftere nakil mantığını tanımlar.
- **Sevkiyat masrafı kodu**: **Gelişmiş otomatik masrafları kullan** seçeneği **Evet** olarak ayarlanmışsa, bu parametre ayarının hiçbir etkisi olmaz. Bu seçenek **Hayır** olarak ayarlanmışsa, kullanıcılardan POS'ta müşteri siparişleri oluştururken, sevkiyat masraflarını el ile girmeleri istenir. Kullanıcılar bir sevkiyat masrafı girdiğinde siparişlere uygulanacak Alacak hesapları gider kodunu eşlemek için bu parametreyi kullanın. Masraf kodu, sevkiyat masrafı için mali deftere nakil mantığını tanımlar.
- **Gelişmiş otomatik masrafları kullan**: POS'ta müşteri siparişleri oluşturulurken sistem tarafından hesaplanan otomatik masrafları kullanmak için bu seçeneği **Evet** olarak ayarlayın. Otomatik masraflar, sevkiyat ücretlerini ve diğer sipariş veya maddeye özel masrafları hesaplamak için kullanılabilir. Gelişmiş otomatik masrafları özelliğini ayarlama ve kullanma hakkında bilgi için bkz. [Çok yönlü kanal gelişmiş otomatik masrafları](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Commerce parametreleri sayfasındaki müşteri siparişleri sekmesi](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>POS'ta hareket ekran düzenlerini güncelleştirme

POS [ekran düzeninin](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts), müşteri siparişlerinin oluşturulmasını ve yönetilmesini destekleyecek şekilde yapılandırıldığından ve gerekli tüm POS işlemlerinin yapılandırıldığından emin olun. Müşteri siparişi oluşturma ve yönetimini doğru şekilde desteklemek için önerilen POS işlemlerinden bazıları şunlardır:
- **Tüm ürünleri sevk et**: Bu işlem, hareket sepetindeki tüm satırların bir hedefe sevk edileceğini belirtmek için kullanılır.
- **Seçili ürünleri sevk et**: Bu işlem, hareket sepetindeki seçili satırların bir hedefe sevk edileceğini belirtmek için kullanılır.
- **Tüm ürünleri çek**: Bu işlem, hareket sepetindeki tüm satırların seçili bir mağaza konumundan çekileceğini belirtmek için kullanılır.
- **Seçili ürünleri çek**: Bu işlem, hareket sepetindeki seçili satırların seçili bir mağaza konumundan çekileceğini belirtmek için kullanılır.
- **Tüm ürünleri teslim al**: Bu işlem, hareket sepetindeki tüm satırların teslim alınacağını için belirtmek kullanılır. POS'ta bu işlem kullanılırsa, müşteri siparişi öde ve al hareketine dönüştürülür.
- **Seçili ürünleri teslim al**: Bu işlem, hareket sepetindeki seçili satırların, satınalma sırasında müşteri tarafından satın alınacağını belirtmek için kullanılır. Bu işlemden yalnızca [karma sipariş](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders) senaryosunda yararlanılır.
- **Siparişi geri çağır**: Bu işlem, müşteri siparişlerini aramak ve getirmek için kullanılır, böylece POS kullanıcıları gerektiğinde karşılama ile ilgili işlemlerini düzenleyebilir, iptal edebilir veya gerçekleştirebilir.
- **Teslimat şeklini değiştir**: Bu işlem, önceden sevkiyat için yapılandırılmış olan satırlar için teslimat şeklini, kullanıcıların "tüm ürünleri sevk et" veya "seçilen ürünleri sevk et" akışının aşamalarının üzerinden yeniden geçmelerine gerek kalmadan teslim etme modunu hızla değiştirmek için kullanılabilir.
- **Havale geçersiz kılma**: Bu işlem, müşterinin seçili müşteri siparişi için ödeyeceği depozito tutarını değiştirmek için kullanılabilir.

![POS hareket ekranındaki işlemler](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>POS'ta müşteri siparişleriyle çalışma

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
5. Bir malzeme çekme tarihi seçin.
6. Vadesi gelen hesaplanmış tutarların ödemesini yapmak için ödeme işlevlerini kullanın veya vadesi gelen miktarları değiştirmek için **Havale geçersiz kılma** işlemini kullanın ve sonra ödemeyi uygulayın.
7. Tam sipariş toplamı ödenmediyse, müşterinin ödemeyi daha sonra (malzeme çekme sırasında) sağlayıp sağlamayacağını veya kredi kartı bilgilerinin güvenli şekilde saklanarak ve malzeme çekme sırasında kullanılıp çekim yapılıp yapılmayacağını seçin.

### <a name="edit-an-existing-customer-order"></a>Geçerli bir müşteri siparişini düzenle

Çevrimiçi veya mağaza kanalında oluşturulan perakende siparişleri gerektiğinde, POS aracılığıyla geri çekilebilir ve düzenlenebilir.

> [!IMPORTANT]
> Çağrı merkezi kanalında oluşturulan siparişler, bu kanalda [Sipariş tamamlamayı etkinleştir](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) ayarı açıksa, POS üzerinden düzenlenemez. Doğru ödeme işleminin yapıldığından emin olmak için, bir çağrı merkezi kanalında oluşturulan ve Sipariş tamamlamayı etkinleştirme işlevini kullanan siparişlerin Commerce Headquarters'da çağrı merkezi uygulaması aracılığıyla düzenlenmesi gerekir.

Commerce 10.0.13 ve önceki sürümlerde, kullanıcılar yalnızca siparişler tam olarak açıksa desteklenen müşteri siparişlerini POS üzerinden düzenleyebilirler. Bir siparişin satırları karşılama (çekme, paketleme, vb.) amacıyla işlenmişse, sipariş POS'ta düzenlemek için kilitlenir.

> [!NOTE]
> Commerce 10.0.14 sürümde, [genel önizleme](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) sürümünde sunulan bir özellik siparişin bir kısmı karşılansa bile POS aracılığıyla kullanıcıların müşteri siparişlerini düzenlemesine olanak sağlar. Ancak, tamamen faturalanmış siparişler POS üzerinden düzenlenemez. Bu önizleme özelliğini test etmek ve ek geribildirim sağlamak için, **Özellik yönetimi** çalışma alanında **Satış Noktası'nda kısmen karşılanmış siparişleri düzenle (Önizleme)** özelliğini açın. Çağrı merkezi kanalında oluşturulan ve Sipariş tamamlamayı etkinleştirme işlevini kullanan müşteri siparişleri bu özellik etkinleştirildikten sonra da düzenlenemez.

1. **Siparişi geri çağır** seçeneğini belirleyin.
2. Siparişi bulmak için filtre girmek üzere **Ara**'yı kullanın ve sonra **Uygula** seçeneğini belirleyin.
3. Sonuç listesinden siparişi seçin ve sonra **Düzenle**'yi seçin. **Düzenle** düğmesi kullanılamıyorsa, sipariş düzenlenmenin mümkün olmadığı bir durumdadır.
4. Hareket sepetinden, müşteri siparişinde gerekli tüm değişiklikleri yapın. Bazı değişiklikler düzenleme sırasında yasaklanmış olabilir.
5. Ödeme işlemini seçerek düzenleme işlemini tamamlayın.
6. Herhangi bir değişiklik yapmadan düzenleme işleminden çıkmak için, **Hareketi hükümsüz kıl** işlemini kullanabilirsiniz.



### <a name="cancel-a-customer-order"></a>Müşteri siparişini iptal etme

1. **Siparişi geri çağır** seçeneğini belirleyin.
2. Siparişi bulmak için filtre girmek üzere **Ara**'yı kullanın ve sonra **Uygula** seçeneğini belirleyin.
3. Sonuç listesinden siparişi seçin ve sonra **İptal**'i seçin. **İptal** düğmesi kullanılamıyorsa sipariş, iptal edilmesinin artık mümkün olmadığı bir durumdadır.
4. İptal masraflarının yapılandırılması durumunda, bunları onaylayın. Gerektiğinde iptal masraflarını onaylamadan önce, ayarlayabilirsiniz. 
5. Hareket sepetinden, bir ödeme işlemi seçerek iptal işlemini tamamlayın. Ödenen depozitolar iptal masrafını aşarsa, iade ödemelerinin yapılması gerekebilir.
6. Herhangi bir değişiklik yapmadan iptal işleminden çıkmak için, **Hareketi hükümsüz kıl** işlemini kullanabilirsiniz.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>POS'tan müşteri sipariş sevkiyatını veya malzeme çekmeyi sonlandırma

Bir sipariş oluşturulduktan sonra, maddeler müşteri tarafından bir mağaza konumundan çekilir veya siparişin yapılandırmasına bağlı olarak sevk edilir. Bu işlem hakkında daha fazla bilgi edinmek için [mağaza sipariş karşılama](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview) belgelerine bakın.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Müşteri siparişleri için zaman uyumsuz işlem akışı

Müşteri siparişleri POS'ta zaman uyumlu ya da zaman uyumsuz modda oluşturulabilir. POS'ta müşteri siparişleri oluştururken performans sorunları veya kullanıcı gecikmeleri fark ederseniz, zaman uyumsuz sipariş oluşturmayı etkinleştirmeyi düşünebilirsiniz.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Müşteri siparişlerinin zaman uyumsuz modunda oluşturulmasını etkinleştirin

1. Commerce yönetim merkezinde, **İşlev profilleri** sayfasında, yapılandırmak istediğiniz mağazaya karşılık gelen işlevsellik profilini seçin.
2. **Genel** hızlı sekmesi üzerinde, **Müşteri siparişlerini zaman uyumsuz modda oluştur** seçeneğini **Evet** olarak ayarlayın.

**Müşteri siparişlerini zaman uyumsuz** moda oluştur seçeneği **Evet** olarak ayarlanmışsa, müşteri siparişleri her defasında zaman uyumsuz modda oluşturulur, Retail Transaction ServicePerakende İşlem Hizmeti (RTS) etkin olsa bile. Bu seçeneği **Hayır** olarak ayarlarsanız, müşteri siparişleri her defasında zaman uyumlu modda RTS kullanarak oluşturulur. Müşteri siparişleri zaman uyumsuz modda oluşturulduğunda, Commerce Pull (P) işlerinden Commerce Headquarters'da perakende satış hareketleri olarak çekilir ve oluşturulur. **Siparişleri eşitle** elle veya toplu bir iş aracılığıyla çalıştırıldığında perakende hareketlerine ait karşılık gelen satış siparişleri oluşturulur.

## <a name="additional-resources"></a>Ek kaynaklar

[Karma müşteri siparişleri](hybrid-customer-orders.md)
