---
title: Ödeme yöntemleri
description: Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka yapılandırılmalıdır. Bu makale, ayarlayabileceğiniz ödeme türlerini ve bunları ayarlamak için gerekli işlemi açıklamaktadır.
author: BrianShook
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: d16cdf237042471d367adb7081bf34e9c8a9460f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272835"
---
# <a name="payment-methods"></a>Ödeme yöntemleri

[!include [banner](includes/banner.md)]

Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka yapılandırılmalıdır. Bu makale, ayarlayabileceğiniz ödeme türlerini ve bunları ayarlamak için gerekli işlemi açıklamaktadır.

Perakendeciler, sattıkları ürünler ve hizmetler karşılığında çeşitli türlerde ödemeler kabul edebilirler. Nakit, en yaygın ödeme yöntemi olmasına rağmen perakendeciler çek, kart, makbuz vb. şeklinde de ödeme kabul edebilmektedirler. Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka Dynamics 365 Commerce içinde yapılandırılmalıdır. Aşağıdaki listede, ayarlanabilecek her bir ödeme türü açıklanmaktadır:

- **Nakit** – Banknot veya bozuk para gibi bir para birimi cinsinden fiziksel formda paradır. Para birimi, şirket para birimi ya da mağazanın yerel para birimi olabilir.
- **Çek** – Belirli bir bankadan belirli bir para biriminde belirli bir tutarın ödemesinin yapılmasını bildiren, ciro edilebilir bir araçtır.. Başka bir geçerlilik dönemi belirtilmediği sürece çekler tipik olarak süresiz olarak veya imzalandığı tarihten itibaren altı ay geçerlidir. Bu dönem, çekin çıkartıldığı bankaya bağlı olarak değişmektedir. Sipariş çekleri, zimmet çekleri, hamiline yazılan çekler veya hesaba ödenen çekler vb. gibi çeşitli çek türleri bulunmaktadır. Çek, her mağaza için bir ödeme yöntemi olarak ayarlayabilirsiniz. Çekler, şirket düzeyinde veya mağaza düzeyinde tanımlanan para biriminde kabul edilebilir. Bir mağazada ödeme yöntemi olarak çek kabul etmeden önce mutlaka ödeme yöntemi olarak çek seçeneğini ayarlamanız gerekir.
- **Döviz** – Şirketin kullandığı para biriminden dışında temel ödeme aracıdır. Bozuk paralar ve kağıt paralar para birimi kapsamındadır. Dövizle ödeme yöntemi, kullanılan tüm para birimlerini temsil etmektedir. Bu ödeme yöntemini kullanmadan önce para birimlerini ayarlamanız ve para birimleri için kambiyo bilgilerini belirlemeniz gerekir.
- **Kart** – Banka kartı ve kredi kartı vb. gibi tüm kart türleri. Her türlü kart çeşidini temsil etmek üzere organizasyon seviyesinde bir kartla ödeme yönteminin kurulması doğru bir karar olacaktır. Ardından, mağaza düzeyinde her bir kart veya aynı ayarlar kullanılarak işlenen her kart grubu için bir ödeme yöntemi ayarlayın. Bir mağazada ödeme yöntemi olarak kart kabul etmeden önce banka kartları ve kredi kartları gibi, piyasada bulunan üretici kartlarını belirlemeniz gerekir.
- **Credit memo** – Satış noktasında oluşturulan veya ödenen credit memo'lardır. Credit memo bir iadeli satış için çıkartılan bir normal veya iadeli bir credit memo'dur. Credit memo'lar sadece kısmen geri ödeniyorsa program, yeni bakiye için yeni bir credit memo hazırlayacaktır. Yeni cerdit memo'nun yeni bir numarası olur. Bir credit memo sadece bir defa kullanılabilir ve sistem kullanılan tüm numaraların bir kaydını tutar. Kayıtlar **Credit memo tablosu** sayfasında görülebilir. Bir müşteri, credit memo değerini birden fazla defa kullanamaz.
- **Hediye Kartı** – Satış noktasında çıkartılan ve ödenen hediye kartlarıdır. Hediye kartlarında para üst verilmesine izin verilmez. Tüm hediye kartlarında kart numarası eşlemeleri olmalıdır. 
- **Müşteri hesabı** – Satış anında kayıtlı bir müşteri hesabına şarj edilebilen ödemelerdir. Bu ödeme yöntemini ayrıca müşteri başka bir ödeme yöntemi kullanarak bir ödeme yaptığında satış bilgileri veya müşteriye özel indirimler almak için kullanabilirsiniz. Bu durumda, müşteriye özel bilgileri ayarlamanız gerekir.
- **Bağlılık programı puanları** – Müşterilerin bağlılık programları aracılığıyla biriktirdiği puan. Bağlılık programları oluşturursanız, müşteriler puan kazanabilir ve sonra bu puanları çeşitli şekillerde kullanabilir. Örneğin, bazı sadakat programlarında müşteriler, sadakat puanlarını bir indirim olarak ve hatta bir ödeme yöntemi olarak kullanabilmektedirler.

Ödeme yöntemleri ayarlamak için, aşağıdaki görevleri tamamlamanız gerekir.

1. Bir organizasyon için ödeme yöntemini ayarlayın. Tüm organizasyon tarafından kabul edilen ödeme yöntemleri oluşturun.
2. Organizasyon kapsamında kart tipleri ve kart numaraları oluşturma. Kredi kartları veya ATM kartları kabul ediliyorsa, kartlar için bir ödeme yöntemi oluşturmanız ve sonra organizasyon kapsamındaki kart tiplerini ve kart numaralarını oluşturmanız gerekir.
3. Mağaza ödeme yöntemini ayarlayın. Ödeme yöntemlerini her bir mağazayla ilişkilendirin ve ardından her bir ödeme yöntemi için mağazaya özel ayarları girin.
4. Mağazalar için kart ödeme yöntemleri ayarlayın. Mağazanın kabul ettiği tüm kart ödeme yöntemleri için kart kurulumunu tamamlayın.

## <a name="handle-change-tendering-for-payment-methods"></a>Ödeme yöntemleri için ödeme değişikliğini işle

Satış noktası hareketleri sırasında fonların müşterilere geri dönmesi gerekiyorsa bazı ödeme yöntemleri doğrudan ödeme değiştirmeyi desteklemez. Ödeme değişikliğini yalnızca **Nakit** ve **Para birimi** ödeme yöntemleri kullanılabilir. 

Bir hareket sırasında ödeme değişimini gerektiren servis taleplerini işlemek gerekiyorsa ancak ödeme yöntemi bunu desteklemiyorsa, bir **Ödeme değişikliği** ödeme yöntemini tanımlayabilirsiniz. Mağaza için mağaza ödeme yöntemlerini ayarladığınızda, kullanılacak ödeme yöntemini seçin. Sonra, **Değiştir** bölümünde **Ödeme değiştir** alanına bir bedel ödemesini değiştir seçeneği girin. Örneğin, nakitin beldel ödemesi değiştirme seçeneği olarak kullanılabileceğini değiştirmek için **1** girebilirsiniz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
