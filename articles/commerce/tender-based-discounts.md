---
title: Ödeme tabanlı iskontolar
description: Bu makalede, Microsoft Dynamics 365 Commerce'de perakendecilere belirli ödeme türleri için iskonto yapılandırma olanağı tanıyan ödeme tabanlo iskonto işlevi açıklanmaktadır.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473834"
---
# <a name="tender-based-discount"></a>Ödeme tabanlı iskonto

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'de perakendecilere belirli ödeme türleri için iskonto yapılandırma olanağı tanıyan ödeme tabanlo iskonto işlevi açıklanmaktadır.

Özel, markalı kredi kartları verme perakendeciler arasında genel bir uygulamadır. Perakendeciler için, bankalardan tercih edilen oranlar aldıklarından dolayı yararlıdır. Ek olarak, bu kredi kartları müşterilerin mağazayı daha sık ziyaret etmesini teşvik ettiğinden perakendecinin alt hattını geliştirmeye yardımcı olur. Bu nedenle, perakendeciler markalı kredi kartlarının müşteri tarafından kullanımını artırmak için bir teşvikte bulunur. Bu amaca ulaşmak için genellikle bu kredi kartlarını kullanan müşterilere ek indirimler sağlarlar.

Alternatif olarak, markalı kredi kartı sağlamayan perakendeciler müşterileri nakit, hediye kartları veya bağlılık programı puanları gibi diğer ödeme türlerini kullanarak ödeme yapmaya teşvik etmek isteyebilir. Bu şekilde kredi kartı işleme masraflarına ait giderleri azaltmaya yardımcı olabilirler. Bu nedenle, perakendeciler bu alternatif ödeme türlerini kullanan müşterilere indirimler sağlayabilir.

## <a name="tender-based-discount"></a>Ödeme tabanlı iskonto

Commerce, perakendecilerin hareket toplamı belirtilen bir tutarı aştığında ve müşteri tercih edilen ödeme yöntemini kullanarak ödeme yaptığında bir harekete uygulanacak bir iskonto yüzdesi yapılandırmasını sağlayan *ödeme tabanlı iskonto* özelliğini destekler. Ödeme tabanlı iskonto katman tabanlıdır, bu nedenle farklı iskonto yüzdeleri farklı tutar eşikleriyle ilişkilendirilebilir. Müşteri kısmi ödeme mi, tam ödeme mi yapacağınıza karar verebilir ve fiyatlandırma altyapısı uygun iskonto tutarını saptar. Ödeme tabanlı iskonto her zaman satış satırlarının ön vergi tutarı üzerinden verilir.

Ödeme tabanlı iskonto, yalnızca fiyatların kilitlendiği satış satırlarına uygulanabilir ve uygun satırlara orantılı olarak dağıtılır. Bir siparişe yeni satış satırları eklenirse, ödeme tabanlı iskonto ödeme sırasında yalnızca yeni satış satırlarına uygulanır. Malzeme çekme veya teslimat için bir müşteri siparişi yerleştirildiğinde, ödeme tabanlı iskonto yalnızca depozito tutarına uygulanır. Sipariş yerleştirildikten sonra, sipariş karşılama sırasında satış satırlarının fiyatları kilitlenir. Malzeme çekme sırasında ödenen veya sevkiyat sırasında onaylanan bakiyeye herhangi bir ödeme tabanlı iskonto uygulanmaz. Ödeme tabanlı iskonto, yalnızca sipariş alındığında perakendeci tüm tutarı depozito olarak tahsil ederse müşteri siparişi tutarının tamamına uygulanabilir.

Ödeme tabanlı iskontolar basit iskontolar, miktar iskontoları, eşik iskontoları, karıştırma ve eşleştirme iskontoları ve el ile iskontolar gibi madde tabanlı iskontolarla rekabet etmez. Ödeme tabanlı iskontolar her zaman madde tabanlı iskontoların üzerinden uygulanır. Bu nedenle, bir maddeye özel bir iskonto uygulanmış olsa bile, ödeme tabanlı iskonto özel iskontonun üzerine uygulanabilir. Benzer şekilde, harekete bir eşik iskontosu uygulanması ve ödeme tabanlı iskontonun toplamı eşiğin altına düşürmesi durumunda bile eşik indirimi harekete uygulanır.

Ödeme tabanlı iskontolar hareketin alt toplamını azaltsa da, harekete uygulanan otomatik masraflar etkilenmez. Örneğin, alt toplam 100 ABD dolarından fazla olduğundan teslimat masrafları 5 ABD doları olarak hesaplanırsa ve ödeme tabanlı iskonto tutarı tutarı 100 ABD dolarının altına düşürürse, sipariş için teslimat ücreti yine de 5 ABD doları olur.

Ödeme tabanlı iskonto şu anda iki ödeme türü ile sınırlıdır: kredi kartları ve nakit. Bir ödeme türü için birden fazla ödeme tabanlı iskonto yapılandırılırsa, yalnızca en iyi ödeme tabanlı iskonto uygulanır.

## <a name="pos-user-experience"></a>POS kullanıcı deneyimi

Ödeme tabanlı iskonto nakit olarak ayarlanmışsa ve satış noktasındaki kasiyer (POS) nakit ödemeyle satın alma hareketi için **Nakit ödeme** düğmesini seçerse, ödeme tabanlı iskonto harekete otomatik olarak uygulanır. Azaltılan tutar daha sonra bakiye olarak görüntülenir. Ancak, kasiyer ödeme ekranında **Geri** düğmesini seçerse, iskonto kaldırılır ve hareket ekranında orijinal tutar gösterilir. Ödeme satırı hükümsüz kılınırsa, ödeme tabanlı iskonto kaldırılır.

Kredi kartı ödemeleri için, perakendeciler bir veya daha fazla kredi kartı türünde ödeme tabanlı iskontoyu ayarlayabilir. Ancak, sistem kart yetkilendirilmediği sürece kullanılan kredi kartı türünü doğrulayamaz. İskonto yetkilendirmeden sonra uygulanırsa, ödeme onayı daha büyük bir tutar için olacaktır, ancak ödeme yakalama daha küçük bir tutar için gerçekleşecektir. Bu durumu engellemeye yardımcı olmak için, bir müşteri kredi kartıyla ödeme yaptığı takdirde, kasiyer müşteriye ek iskonto sağlayacak tercih edilen kredi kartlarını listeleyen bir iletişim kutusu görür. Böylece kasiyer, müşterinin ek indirim elde etmek için tercih edilen kartlardan birini kullanmak isteyip istemediğini sorabilir. Kasiyer tercih edilen bir kartı seçerse ödeme tabanlı iskonto harekete uygulanır ve azaltılan tutar ödeme ekranında gösterilir. Onay, düşürülen tutar için olacaktır. Müşteri, kasiyerin seçtiği karttan farklı bir kart takarsa, bir hata iletisi gösterilir ve yetkilendirme geçersiz kılınır.

## <a name="call-center-user-experience"></a>Çağrı merkezi kullanıcı deneyimi

Çağrı merkezi kullanıcısı çağrı merkezi siparişi sırasında **Tamamla**'yı seçerse **Toplamlar** ekranı görüntülenir. Önce, ödeme yöntemi henüz seçilmediğinden bu ekrandaki toplamlar ödeme tabanlı iskontoları içermez. **Ödeme ekle** ekranında, kullanıcı ödeme tabanlı iskontonun yapılandırıldığı ödeme yöntemini seçerse, ödeme tutarı indirimli tutarı yansıtacak şekilde otomatik olarak ayarlanacaktır. POS'taki müşteri gibi, çağrı merkezi müşterisi de tam ödeme mi, yoksa kısmi ödeme mi yapacağına karar verebilir. Ödenen tutara dayalı olarak, ödeme tabanlı iskonto satış siparişine uygulanır.

> [!NOTE]
> Çağrı merkezi siparişleri için kart doğrulaması yapılmaz. Örneğin, çağrı merkezi kullanıcısı kredi kartı olarak Visa seçerse ancak müşteri Mastercard kullanırsa, sistem indirimi yine de uygular.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
