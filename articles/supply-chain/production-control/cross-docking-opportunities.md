---
title: Üretim emirlerinden çıkış noktalarına çapraz sevk
description: Bu konu, bir üretim hattından bir harici nakliye sevk noktasından tamamlanmış olarak raporlanan çapraz sevk malzemesinin yönetilme işlemini açıklar.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockOpportunityPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8691bb6702028070810a1503add33985de5ede3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553034"
---
# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Üretim emirlerinden çıkış noktalarına çapraz sevk

[!include [banner](../includes/banner.md)]

Bu konu, bir üretim hattından bir harici nakliye sevk noktasından tamamlanmış olarak raporlanan çapraz sevk malzemesinin yönetilme işlemini açıklar.

<a name="introduction"></a>Giriş
------------

Üretimden harici bir konuma çapraz sevk, yüksek hacimli üretim yapan ve bitirilmiş ürünleri, üretim hatlarından bitirilmiş olarak raporlandıktan sonra en kısa zamanda nakletmek isteyen üreticiler için önemlidir. Amaç, ürünleri üretim tesisinin envanterinde biriktirmek yerine, müşteri talebine fiziksel olarak yakın bulunan dağıtım merkezlerine nakletmektir.

Bu durumda, ürüne anlık talep yoktur ve üretim tesisindeki ambar konumlarında muhafaza edilmeleri gerekir. Bu işlem *fırsatçı çapraz sevk* olarak da bilinir, bu da ürünün sevk edilmesi için talep olduğunu belirtir, daha sonra bu ürünün, dahili depoya koyulmaktansa fırsat olarak değerlendirilmelidir.

Aşağıdaki örnekler, üretim hattının sonundan başlayan üç fark gösterir (2).

Bir ürün üretim çıkış konumuna (3) bitmiş olarak raporlanır ve bir forklift sürücüsü paleti bu konumdan (3) alır.

-   Ürünü üretimden (1) dağıtım merkezine (7) nakletmek için planlanmış bir etkinlik (6) mevcutsa, kamyon sürücüsü, paleti bölüm kapısına (4) koymak üzere sistem tarafından yönlendirilir.
-   Bir treyler bölme kapısına zaten atanmışsa, kamyon sürücüsü ürünü doğrudan treylere yüklemek üzere yönlendirilir.
-   Ürünü nakletmek için planlanmış etkinlik yoksa, forklift sürücüsü ürünü dahili bir ambar (5) konumunda depolamak üzere yönlendirilir.

[![fırsatçı çapraz sevk](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Çapraz sevk yapılandır
Çapraz sevk işlemini **iş ilkelerinde** yapılandırırsınız. Bir iş ilkesi, bir iş emri türü, konum ve ürün içerir. Aşağıdaki örnekte, çapraz sevk ürün X ve konum Y için yapılandırılır.

#### <a name="work-order-types"></a>İş emri türleri

-   İş emri türü: Mamul malları depolama
-   İş oluşturme yöntemi: Çapraz sevk etme
-   Çapraz sevk ilkesi adı: Transfer emirleri

#### <a name="inventory-locations"></a>Stok konumları

-   Ambar: 51
-   Konum: Y

#### <a name="products"></a>Ürünler

-   Madde numarası: X

Şu anda, çapraz sevk yalnızca iki iş emri türü için yapılandırılabilir:

-   Yerine konan mamul mallar
-   Yerine konan ortak ürün ve yan ürün

**Çapraz sevk ilkesi** içerisinde hangi belge türünün çapraz sevk için uygulanabildiğini tanımlarsınız. Şu anda, desteklenen tek belge türü **Transfer siparişleri**'dir. Aşağıdaki örnek, bir çapraz sevk ilkesinin yapılandırılmasını gösterir.

### <a name="cross-docking-policy-name-transfer-order"></a>Çapraz sevk ilke adı: Transfer emri

- Sıra numarası: 10
  -   İş emri türü: Transfer sorunu
- Çapraz sevk talebi konum gerektirir: Yanlış
- Çapraz sevk stratejisi: Tarih ve saat

### <a name="sequence-number"></a>Numara serisi

**Sıra numarası**, belge türünün önceliğini belirtir. Şu anda, **Transfer sorunu** desteklenen tek türdür. Bu nedenle, sıra numarası yalnızca daha fazla iş emri türü desteklenirse önem kazanır.

### <a name="cross-docking-policy"></a>Çapraz sevk ilkesi

Çapraz sevk ilkesi ayrıca transfer siparişi talebinin öncelik verilmesi için ilkeyi ayarlar. Örneğin, birden fazla transfer siparişi aynı ürün için mevcutsa, yük üzerinde planlanan ve iş emri ile ilişkilendirilmiş olan tarih ve saat, siparişler arasındaki önceliği belirler. Planlanan tarih ve saat doğrudan yük veya yük ile ilişkilendirilmiş bir **randevu çizelgesi** üzerinde ayarlanabilir. Öncelik belirleme, çapraz sevk stratejisi tarafından belirlenir. Şu anda, yalnızca bir strateji mevcuttur: **Tarih ve saat**.

### <a name="cross-docking-demand-requires-location"></a>Çapraz sevk talebi konum gerektirir

Çapraz sevk ilkesinde, transfer emirlerinin çapraz sevk edilmeye uygun olabilmeleri için kriterler ayarlayabilirsiniz. Bu kriter, **Çapraz sevk talebi konum gerektirir** alanında ayarlanır. Yük ile ilişkilendirilmiş randevu zamanlamasındaki konum, çapraz sevk edilen ürünlerin son konumu olarak kullanılır. Çapraz sevk edilen ürünler için son konum, **Koyma** iş emri türü için **Transfer sorunu** için konum yönergesi tarafından belirlenir. **Çapraz sevk talebi konum gerektirir** alanını, tamamlanmış ürünlerin yalnızca bir treyler bir bölüm kapısına atanmışsa çapraz sevk edileceği bir senaryoda kullanışlı bulabilirsiniz. Bu senaryoda, ürünler üretim hattından doğrudan treylere taşınır. Bir treyler bölme kapısına atanmışsa, bir kullanıcı konumu randevu planına atar ve bu nedenle konumu çapraz sevke uygun hale getirir. Aşağıdaki bölümler iki örneği size açıklar.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Senaryo 1 – Üretimden transfer emirlerine çapraz sevk

Bir ürün üretim hattında tamamlanmış olarak raporlandığında, bir kamyona yüklenip bir üretim merkezine aktarılacağı bir bölme kapısı konumuna nakledilir. USMF şirketini kullanın.

1.  Çapraz sevk için yeni bir numara sırasını etkinleştirin. **Numara sıraları** sayfasına gidin ve **Oluştur** düğmesini seçin. Bir sihirbazı sizi tüm işlem boyunca yönlendirecektir.
2.  Bir çapraz sevk ilkesi yarat. **Çapraz sevk ilkesi** sayfasına gidin ve **Transfer emrinden çapraz sevk** adında yeni bir ilke oluşturun. Seçebileceğiniz tek iş emri türünün **Transfer sorunu** olduğunu ve kullanılabilen tek çapraz sevk stratejisinin **Tarih ve saat** olduğunu unutmayın.
3.  Bir iş ilkesi oluştur. **İş ilkeleri** sayfasına gidin ve **Çapraz Sevk L0101** adında yeni bir iş ilkesi oluşturun.
4.  Transfer emirleri için yüklerin otomatik olarak oluşturulmasını ayarlayın. Ambar parametrelerinde, yükleri, bir transfer emri oluşturulduğunda otomatik olarak oluşturulacakları şekilde ayarlayın. Transfer emrini çapraz sevk için uygun hale getirmek amacıyla bir yük gereklidir.
5.  Madde yükleme eşleşmesi ayarlayın. **Madde yükleme eşleşmesi** sayfasına gidin ve standart yük şablonunu **CarAudio** madde grubu için ayarlayın. Bu eşleşme yük şablonunu, transfer emri oluşturulduğunda yük üzerinde otomatik olarak ekleyecektir.
6.  Transfer emri oluşturma. Madde numarası L0101 için transfer emri oluştur. Miktar = 20.
7.  Transfer emrini yük planlama workbench'inden serbest bırakın. **Sevk** sekmesinde, yük hattının **Serbest bırak** menüsü üzerinde yük planlama workbench'i için menü öğesini seçin, **Ambara serbest bırak**'ı seçin. **Transfer sorunu** türünde bir açık dalga hattı şimdi transfer emri için artık mevcuttur.
8.  Bir üretim emri oluşturun. **Üretim emri** liste sayfasına gidin ve L0101 için bir üretim emri oluşturun. Miktar = 20. Üretim emrini tahmin edin ve başlatın. **Malzeme çekme listesini şimdi naklet** alanı **Hayır** olarak kalır.
9.  Mobil cihazdan tamamlanmış olarak raporlayın. Mobil cihaz portalına gidin ve menü öğesi **Tamamlanmış olarak raporla ve kaldır**'ı seçin. Mobil cihazdan L0101 tamamlanmış olarak raporlayın. Miktar = 10. Koyma konumunun **BÖLME KAPISI** olduğunu dikkate alın. Bu konum, **Koyma** iş emri türü için **Transfer sorunu** konum yönergesinden bulunur. **Transfer sorunu** türündeki işin oluşturulduğunu ve tamamlandığını da dikkate alın. İşi doğrulamak için transfer emri iş ayrıntılarına gidin.
10. Şimdi mobil cihazdan ek 10 adet daha bildirin. Yerine koyma konumunun yine **BÖLME KAPISI** olduğunu dikkate alın. Ayrıca 10 adet için **Transfer sorunu** türündeki yeni bir işin oluşturulduğuna dikkat edin.
11. Şimdi üretim emrinden 20 adet daha başlatmaya çalışın ve daha sonra 20 adeti mobil cihazı kullanarak tamamlanmış olarak raporlamaya çalışın. Bu sefer, konum **LP-001** koyma konumu olarak önerilir. Bu konum, **Tamamlanmış ürünleri koyma** için konum yönergesinden bulunur. Bu konum yönergesi, çapraz sevk için hiçbir fırsat olmadığından mevcut olmadığından kullanılır. LP-001 için transfer emri, adım 9 ve 10'da iki çapraz sevk etkinliği tarafından tamamlanır. **Tamamlanmış ürünleri yerine koyma** türündeki işin oluşturulduğuna ve işlendiğine dikkat edin.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Senaryo 2 - Üretimden transfer siparişine bir randevu zamanlama ile çapraz sevk

Bir ürün üretim hattında tamamlanmış olarak raporlandığında, bölme kapısı konumları için bir randevu zamanlaması tarafından kimlik verilmiş bir bölme kapısı konumuna aktarılır. USMF şirketini kullanın.

1.  Çapraz sevk ilkesini değiştirin. Senaryo 1'de oluşturduğunuz **Çapraz sevk talebi konum gerektirir** onay kutusunu seçerek çapraz sevk ilkesini değiştirin.
2.  Yeni transfer emri oluştur.
3.  **Yük planlama workbench'i** aç.
4.  Yük planlama workbench'inden, **Yükler** bölümüne gidin ve yeni bir randevu zamanlama oluşturmak için **Randevu zamanlama**'yı **Taşıma** menüsünden seçin. Randevu zamanlamasının transfer emrine **Sipariş numarası** alanında bir referansı olduğunu unutmayın. **Konumda planlanan başlangıç tarihi/saati** alanında, randevu için tarih ve saati ayarlayabilirsiniz. Bu tarih ve saat, çapraz sevk talebine çapraz sevk işlemi sırasında öncelik verildiğinde kullanılacaktır. Bu alanda ayarlayacağınız tarih ve saat **Zamanlanan yük nakil tarih ve saati** alanında, karşılık gelen yükte güncelleştirilecektir. **Sevk ayrıntıları** hızlı sekmesindeki konum, transfer siparişinin nakledileceği konumu belirler.
5.  **Yük planlama workbench'inde** ambara serbest bırakın.
6.  Madde numarası **L0101** için bir üretim emri oluşturun ve durumunu **Başlandı** olarak tutar 20 ile ayarlayın.
7.  Mobil cihazdan tamamlanmış olarak raporlayın.
8.  Mobil cihaz portalına gidin ve **Tamamlanmış olarak raporla ve kaldır** menü öğesini seçin.
9.  Madde numarası **L0101**'i mobil cihazdan tamamlanmış olarak raporlayın. Koyma konumunun şimdi **BÖLME KAPISI 2** olduğunu dikkate alın. Bu konum **Transfer alış irsaliyesi** konum yönergesi yerine randevu zamanlamasında bulunur.

### <a name="additional-information"></a>Ek bilgi

-   Çapraz sevk senaryosu toplu iş ve seri denetlenen öğeler için desteklenir; her ikisi de rezervasyon hiyerarşisinin üstünde ve altında toplu iş ve seri numarası boyutları ile tanımlanır. 


