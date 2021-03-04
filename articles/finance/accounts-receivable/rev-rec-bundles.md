---
title: Gelir kabulü paketleri
description: Bu konuda, Alacak hesaplarında bulunan gelir kabulü özelliğine dahil edilen paket işlevleri açıklanmaktadır. Paket, bir ana madde ve birden fazla bileşen madde içerir.
author: kweekley
manager: aolson
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: cf4d03c1a697259899c419ce084b35f4eddf13fe
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142311"
---
# <a name="revenue-recognition-bundles"></a>Gelir kabulü paketleri

[!include [banner](../includes/banner.md)]

Bu konuda, Alacak hesaplarında bulunan gelir kabulü özelliğine dahil edilen paket işlevleri açıklanmaktadır. Paket, bir ana madde ve birden fazla bileşen madde içerir. Sipariş girişinin daha etkili olması için ana madde bir satış siparişine girilir. Ancak, bileşen öğelerine genişletilir. Sevk irsaliyesi gibi şirket içi belgelerde bileşen maddeleri listelenir. Ancak, harici belgelerde yalnızca ana madde gösterilir.

> [!NOTE]
> Çevrimiçi, satış noktası (POS) ve çağrı merkezleri gibi Microsoft Dynamics 365 Commerce kanalları, gelir kabulünü (paket işlevi dahil) desteklemez. Buna Dynamics 365 Supply Chain Management ve Dynamics 365 Sales için nakit çözümü Aday Müşterisi dahildir. Gelir kabulünü kullanacak şekilde yapılandırılmış olan maddeler, Commerce kanallarında veya nakit çözümü Aday Müşterisinde oluşturulan siparişlere veya hareketlere eklenmemelidir.

Paketleri ayarlamak için gelir kabulü için yapılandırma anahtarlarını girmeniz gerekir. Ancak, gelir kabulü ayarlanmamış olsa bile, paketleri kullanabilirsiniz. Benzer şekilde, paketler ayarlanmamışsa gelir kabulünü kullanabilirsiniz. Gelir kabulü ayarlanmışsa bileşen maddeleri, bir satış siparişi faturalandığında gelir kabulü veya erteleme için kullanılan gelir fiyatını ve gelir çizelgesini belirler.

Paketlerin kurulumu, ürün reçetesi işlevini kullanır. Bir paket maddesinin nasıl ayarlanacağı hakkında bilgi için bkz. [Gelir kabulü kurulumu](revenue-recognition-setup.md). Ana madde bir paket olarak işaretlenirse diğer ürün reçetesi maddelerinden farklı şekilde değerlendirilir. Farkların listesi aşağıdadır:

- Paketler, satış siparişi sayfasındaki Eylem bölmesinin **Satış** sekmesindeki **Satış siparişini onayla** işlemi seçilerek satış siparişi onayı üzerinden genişletilmelidir. Paket maddeleri, **Satış siparişi satırları** hızlı sekmesindeki **Satış siparişi satırı** menüsünde, **Genişlet** altındaki **Ürün reçetesi satırı** seçilerek hiçbir zaman genişletilmemelidir. Aksi durumda, madde bir paket olarak değil, ürün reçetesi olarak kabul edilir.
- Sevk irsaliyesi veya fatura oluşturulmadan önce paket maddesi içeren bir satış siparişinin onaylanması gerekir.
- Bir paket, satış siparişi onayı üzerinden genişletildiğinde, ana madde iptal edilir ve birim fiyatı ile iskontolar paketin bileşen maddelerine tahsis edilir.
- Bileşen maddelerinin toplamı, her zaman ana maddedeki fiyata eşit olmalıdır. Bu nedenle, bileşen maddeleri için güncelleştirilebilecek veya değiştirilebilecek alanlarla ilgili sınırlamalar söz konusudur. Örneğin, birim fiyatı el ile değiştirilemez. Ayrıca, yeni bir fiyat anlaşmasını geçerli kılarak dolaylı olarak değiştirilemez. Yeni bir fiyat anlaşmasını önlemek için bileşen maddelerinde stok boyutları değiştirilemez.
- Satış siparişi onayı veya fatura gibi bir harici kullanıcılara yönelik belge yazdırıldığında, bileşen maddeleri değil, ana madde yazdırılır.

## <a name="bundles-on-sales-orders"></a>Satış siparişlerindeki paketler

USMF demo şirketi, aşağıdaki paket kurulumunu içerir. Gelir çizelgelerinin kurulumu gibi, gelir kabulüne yönelik tüm ayarların bu senaryoya dahil edilen maddelerden kaldırılmış olduğunu unutmayın.

**Ana madde:** Dizüstü bilgisayar paketi

- **Bileşen maddesi:** 1 adet madde 1000
- **Bileşen maddesi:** 1 adet madde S0021
- **Bileşen maddesi:** 1 adet Destek maddesi

Bileşen maddelerinin *temel satış fiyatı*, bileşenlerin kurulumunun temel bir parçasıdır. Temel satış fiyatı, bir maddenin **Satış** hızlı sekmesinde tanımlanır. Ana maddenin birim fiyatı bileşen maddelerine tahsis edildiğinde tahsisat faktörünü hesaplamak için kullanılır. Ticari anlaşma satış fiyatları hiçbir zaman bu amaçla kullanılmaz.

Bileşen maddeleri için aşağıdaki temel satış fiyatları tanımlanmıştır:

- **1000:** 1900,00 dolar
- **S0021:** 150,00 dolar
- **Destek:** 500,00

US-004 müşterisi Cave Wholesales için bir satış siparişi girilir. Girilen tek satır, Dizüstü bilgisayar paketi maddesi içindir. Üst satırın varsayılan birim fiyatı, ticari anlaşma veya temel satış fiyatı gibi çeşitli yerlerden alınabilir. Bu örnekte, birim fiyat olarak 2300 dolar el ile girilmiştir.

[![Satış siparişindeki dizüstü bilgisayar paketi maddesi](./media/bundle-01.png)](./media/bundle-01.png)

Satış siparişinde bir paket bulunduğundan bunun onaylanması gerekir. Onay iletişim kutusu, paket bileşenlerini gösterir.

[![Bileşen maddelerini gösteren satış siparişini onaylama iletişim kutusu](./media/bundle-02.png)](./media/bundle-02.png)

Ancak, yazdırılan onay raporu yalnızca paketin ana maddesini gösterir çünkü bu rapor, müşteriye yönelik, kurum dışında kullanılabilen bir belgedir.

[![Yalnızca ana maddeyi gösteren onay raporu](./media/bundle-03.png)](./media/bundle-03.png)

Satış siparişi onaylandıktan sonra, ana madde satış siparişinde gösterilmeye devam eder ancak durumu **İptal Edildi** olarak değiştirilir. Ek olarak, net tutar **Paket net tutarı** alanında izlenir. Fatura, bileşen maddelerini değil ana maddeyi gösterdiği için bu tutar faturayı yazdırmak için gereklidir.

Bileşen maddelerinin toplamı, yazdırılan faturada müşteriye sunulan tutar olduğundan bu değer **Paket net tutarı** değerine eşit olmalıdır. Faturanın genel muhasebeye nakledilen tutarlarla eşleştiğinden emin olmak için bileşen maddelerinizle ilgili düzenleme işlemleri kısıtlanmıştır. Örneğin, tesis ve Ambar değiştirilemez. Bunun nedeni, bu değişikliklerin ticari bir anlaşmayı temel alarak fiyat değişikliği tetikleyebilmesidir.

Ana madde satırındaki birim fiyatı, aşağıdaki şekilde bileşenlere tahsis edilir:

**Bileşenlerden alınan toplam temel satış fiyatları:** 1900 + 500 + 150 = 2550 dolar

- **Bileşen 1:** 2300 × (1900 ÷ 2550) = 1713,73 dolar
- **Bileşen 2:** 2300 × (500 ÷ 2550) = 450,98 dolar
- **Bileşen 3:** 2300 × (150 ÷ 2550) = 135,29 dolar

Bileşenlerin toplamı 2300 dolara eşit olmalıdır ve bu hesap doğrudur (1713,73 + 450,98 + 135,29 = 2300 dolar).

Tüm bileşen maddeleri için değişiklikler gerekiyorsa ana madde kaldırılır. Bu durumda, bileşen maddeleri de kaldırılır. Ana madde daha sonra yeniden eklenebilir ve gerekli düzenlemeler satış siparişi onaylanmadan önce tamamlanabilir.

[![Bileşen maddelerinde yapılan değişiklikleri içeren paket maddesi](./media/bundle-04.png)](./media/bundle-04.png)

Satış siparişi çekilip paketlendiğinde, belgeler yalnızca paketin bileşenlerini içerir. Sevk irsaliyesi ve fatura, paketin tamamını içermelidir. Aksi takdirde, bunlar deftere nakledilemez. Örneğin, iletişim kutusu üç bileşen maddesi gösterir. Bunlardan birini silmeye çalışırsanız paketlerdeki tüm ürünlerin faturalanmadan önce sevk edilmeleri gerektiğini bildiren bir hata iletisi alırsınız.

Paketler, tam paket olarak sevk edilmeli ve faturalanmalıdır. Örneğin, 1000 maddesinin miktarını 4 olarak değiştirip diğer bileşen maddelerinin miktarını 5'te bırakırsanız sevk irsaliyesi ve fatura deftere nakledilemez.

Kısmi tutar, yalnızca paketin tüm bileşenlerinin miktarı azaltılırsa sevk edilebilir ve faturalanabilir. Örneğin, bir satış siparişine Dizüstü Bilgisayar paketi maddesinin miktarı 5 olarak girilir. Satış siparişi onaylandıktan sonra, satış siparişinde üç bileşen maddesi gösterilir ve her birinin miktarı 5 olur. Varsayılan olarak sevkiyat ve faturalama sırasında miktar, her bileşen için 5 olarak ayarlanır. Ancak, üç bileşen maddesinin tümü için miktarı 3'e kadar ayarlayabilirsiniz. Bu durumda, üç tam paket sevk edilir ve faturalanır. Kalan iki paket maddesi (üç bileşen maddesinin her birinin miktarı 2'dir) sevk edilebilir ve daha sonra faturalanabilir.

Son adım, satış siparişini faturalamaktır. Faturalama sırasında, fatura iletişim kutusunda bileşen maddeleri gösterilir.

[![Bileşen maddelerini gösteren fatura iletişim kutusu](./media/bundle-06.png)](./media/bundle-06.png)

Ancak, yazdırılan faturada yalnızca ana madde gösterilir.
 
[![Yalnızca ana maddeyi gösteren yazdırılmış fatura](./media/bundle-07.png)](./media/bundle-07.png)

Maddenin durumu **İptal Edildi** olduğundan, deftere nakilden sonra oluşturulan fatura günlüğü paketin ana maddesini içermez.

[![Ana maddeyi içermeyen fatura günlüğü](./media/bundle-08.png)](./media/bundle-08.png)

Fatura deftere nakledildikten sonra gerçekleştirilen tüm işlemler fatura günlüğünü temel aldığından, bu fatura günlüğünün paketteki ana maddeyi içermemesi önemlidir. Örneğin, Eylem bölmesindeki **Satış** sekmesinden bir alacak dekontu oluşturursanız oluşturulan alacak dekontu bileşen maddelerini içerir ancak ana maddeyi içermez.

[![Bileşen maddelerini gösteren ancak ana maddeyi içermeyen alacak dekontu](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]