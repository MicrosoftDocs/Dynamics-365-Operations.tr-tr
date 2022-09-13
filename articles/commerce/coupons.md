---
title: Kuponlar
description: Bu makale, Microsoft Dynamics 365 Commerce'teki kuponla ilişkili özelliklere genel bakış sağlar.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 2594848948b141015adfaa4ec27e2c2b4cc4dcd2
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410782"
---
# <a name="coupons"></a>Kuponlar

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'teki kuponla ilişkili özelliklere genel bakış sağlar.

Kuponlar, hareketleri iskontoları eklemek için kullanılan barkodlar ve kodlardır. Perakendeciler, marka tanıma, dönüşümü artırma, müşteri tabanlarını koruma, satışları ve sonuçta geliri artırmaya yardımcı olmak için, olası veya mevcut müşterilere kuponlar dağıtır. Kuponlar en popüler pazarlama araçlarından birine dönüşmüştür ve e-ticaret satışlarında yeni bir normdur.

Dynamics 365 Commerce'te kuponlar indirimlerle bağlantılıdır ve indirimlere ek bir doğrulama olarak kabul edilir. Her kupon bir iskontoyla ilişkilidir ve bağlantılı iskonto, kuponun geçerli olduğu ürünler kümesini tanımlar.

Bir indirimle ilişkilendirilmiş fiyat grupları, kuponun kullanılabileceği uygun koşulları tanımlar. Bu koşullar, müşteri gruplarını ve satış kanallarını içerir. Kuponlar ayrıca, isteğe bağlı kullanım sınırlamalarını yapılandırmak için kullanılabilecek **Kullanım sınırı** ve **Müşteri gereklidir**  özelliklerini sağlar.

Her kuponda birden fazla kupon kodu ve kupon barkodu olabilir ve her kodun kendi geçerlilik tarihi aralığı ve durumu bulunabilir. Bir kodun durumu **Devre dışı** olarak ayarlandıysa, kod herhangi bir kanalda kullanılamaz.

## <a name="set-up-a-coupon"></a>Kupon ayarlama

Kupon ayarlamadan önce, kupon bar kodu ve iki numara serisi ayarlamanız gerekir.

Commerce headquarters'ta bir kupon ayarlamak için bu adımları izleyin.

1. **Perakende ve Ticaret \> Stok yönetimi \> Barkodlar ve etiketler \> Maske karakterleri**'ne gidin.
1. **Kupon kodu** türünün maske karakterini oluşturmak için **Ekle**'yi seçin. **Karakter** alanında, kullanılmayan herhangi bir karakteri seçebilirsiniz.
1. **Perakende ve Ticaret \> Stok yönetimi \> Barkodlar ve etiketler \> Maske karakterleri**'ne gidin.
1. **Kupon** türünün barkod maskesini oluşturmak için **Yeni**'yi seçin.
1. **Perakende ve Ticaret \> Stok yönetimi \> Barkodlar ve etiketler \> Barkod kurulumu**'na gidin.
1. Az önce oluşturduğunuz barkod maskesini kullanan bir barkod oluşturmak için **Yeni**'yi seçin.
1. **Kuruluş yönetimi \> Numara serileri**'ne gidin.
1. İki yeni numara serisi oluşturun:

    1. **Kupon numarası** referansı için bir seri. Bu seri, kuponun benzersiz tanımlayıcısını tanımlar.
    1. **Kupon kodu kimliği** referansı için bir seri. Bu seri, bir kupondaki her kupon kodunun benzersiz tanımlayıcısını tanımlar.

    Her iki numara serisi için **Kapsam** alanını **Şirket** olarak ayarlamanız gerekir. Çoğu durumda, her iki numara serisi otomatik olarak oluşturmalıdır.

1. **Commerce parametreleri \> Fiyatlar ve iskontolar \> Kuponlar**'a gidin.
1. **Kupon barkod maskesi** alanını, daha önce oluşturduğunuz barkoda ayarlayın.
1. **Commerce parametreleri \> Numara serileri**'ne gidin.
1. **Kupon numarası** ve **Kupon kodu kimliği** referansları için daha önce oluşturduğunuz numara serilerini seçin.

Kuponu ayarlamak için, iskontoyu ve kuponu ayrı olarak oluşturmalı ve sonra kupon yapılandırmasının **İskonto** alanında iskontoyu seçerek bunları bağlamalısınız. Kupon bir iskontoya bağlandıktan sonra, değerler kuponun durumu ve geçerlilik dönemi tarafından belirlendiğinden, bağlı iskontonun **Durum**, **Geçerlilik tarihi** ve **Bitiş tarihi** alanları salt okunur olur. Kuponun durumu **Etkin** olarak ayarlandığında, bağlı iskontonun durumu otomatik olarak **Etkinleştirildi** olarak güncelleştirilir. Aynı şekilde, kuponun durumu **Etkin Değil** olarak ayarlandığında, bağlı iskontonun durumu otomatik olarak **Devre Dışı** olarak güncelleştirilir.

## <a name="use-a-coupon"></a>Bir kuponu kullanma

Bir satış hareketine Commerce satış noktasında (POS) kupon uygulamak için kupon kodu veya kupon barkodu kullanabilirsiniz. Kupon kodu kullanmak için **Kupon kodu ekle** işlemini seçin ve kodu girin. Kupon barkodu kullanmak için tarama cihazını kullanarak barkodu tarayabilir veya **Hareket** ekranındaki sayısal klavyeyi kullanarak barkodu girebilirsiniz.

Perakendeciler, kasiyerlerin yatıştırma veya ürün kusurları nedeniyle müşterilere sabit tutarlı iskontolar verebilmelerini isterler ancak kupon kodlarını yazdırıp kasiyerlere dağıtmak istemezler. Bu durumda kupon için **Kupon kodu olmadan uygula** seçeneğini **Evet** olarak ayarlayabilirsiniz. POS kasiyerleri daha sonra, kodu el ile girmeden bir harekete kupon eklemek için **Kullanılabilir iskontoları görüntüle** işlemindeki **Kupon uygula** işlevini kullanabilirler. Kupon için birden çok kupon kodu varsa, sistem otomatik olarak ilk etkin kuponu seçer ve bunu harekete uygular.

Bir çağrı merkezi satış siparişine kupon eklemek için çağrı merkezi kullanıcısı satış siparişi sayfasındaki eylem bölmesinin **Yönet** sekmesinde **Kuponlar**'ı seçmelidir.

Bir e-ticaret siparişine kupon eklemek için alışverişçi, alışveriş sepetindeki **promosyon kodu** alanına kupon kodunu girebilir.

Satış siparişine kupon eklendikten sonra, gecikmiş hesaplamanın etkin olup olmamasına bakmaksızın fiyatlandırma altyapısı hemen tüm sipariş için yeniden hesaplamayı tetikler.

> [!NOTE]
> Commerce sürüm 10.0.30 ve öncesinde çağrı merkezi kullanıcıları, bir çağrı merkezi satış siparişine kupon ekledikten sonra, bu kuponla ilişkilendirilmiş olan indirimi uygulamak için eylem bölmesinin **Satış** sekmesindeki **Hesapla** grubunda **Yeniden hesapla** seçeneğini seçmelidir.

## <a name="coupon-usage-limit"></a>Kupon kullanım sınırı

Kuponlar sınırlı kullanım için yapılandırılabilir. Kullanım sınırı müşteri başına, kanal başına ya da genel olarak tanımlanabilir. Kullanım sınırı, kupondaki kupon kodu başına uygulanır. Örneğin, iki kupon kodu içeren bir tek kullanımlık kupon iki kez kullanılabilir: her kupon kodu için bir kez.

Kuponlar, satış kanalları genelinde kullanılabilir. Ancak çağrı merkezi için, sınırlı kullanım kuponları yalnızca çağrı merkezi kanalı için **Sipariş tamamlamayı etkinleştir** ayarı etkinleştirildiğinde uygulanabilir. **Sipariş tamamlamayı etkinleştir** ayarı devre dışıysa, yalnızca sınırlı olmayan kuponlar uygulanabilir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
