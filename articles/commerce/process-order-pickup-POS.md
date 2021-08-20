---
title: POS'ta müşteri siparişi teslim alımını işleme
description: Bu konu, müşteri siparişi teslim alımlarını işlemek için satış noktası (POS) uygulamasında kullanılabilen işlevselliği açıklar.
author: Hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 598b155e1aa71cc7a23d1003331900604fb3de515381fd9c9987ed39bd9cbd2a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741074"
---
# <a name="process-customer-order-pickups-in-pos"></a>POS'ta müşteri siparişi teslim alımını işleme

[!include [banner](includes/banner.md)]

Mağaza teslim alımı için bir [müşteri siparişi](customer-orders-overview.md) oluşturulduğunda, mağaza kullanıcısı stok teslim alımını başlatmak için satış noktası (POS) uygulamasını kullanabilir. POS, son ödeme yakalamasını gerektiği gibi çalıştırır. Ayrıca, alınan miktarlar için stok ve mali deftere nakil işlemini de tamamlar.

Mağaza kullanıcısıysanız **Siparişi geri çağır** işlemini veya POS'taki **Sipariş karşılama** işlemini kullanarak teslim alma işlemini gerçekleştirebilirsiniz. **Teslim alma** işlemini kullanılabilir hale getirmek için önce şu adımlardan birini izlemeniz gerekir:

- **Siparişi geri çağırma** işlemini kullanmak için teslim alınacak siparişi arayın ve seçin.
- **Sipariş karşılama** işlemini kullanmak için bir veya daha fazla sipariş satırını arayın ve seçin.

Seçili sipariş veya sipariş satırları belirli bir mağazada teslim alım için yapılandırılmamışsa veya sipariş zaten tamamen teslim alınmışsa **Teslim alma** işlemi kullanılamaz.

![Teslim alma işlemi.](media/pickupoperation.png)

Microsoft Dynamics 365 Commerce 10.0.17 ve sonraki sürümlerinde, **Satış Noktasında teslim alma siparişi işleme için geliştirilmiş kullanıcı deneyimi**, Commerce Headquarters'daki Özellik yönetimi üzerinden açılabilir. Bu özellik kapalıysa, kullanıcılar teslim alım miktarlarını seçemez. Varsayılan olarak, satır için sipariş edilen tam miktar, teslim alınacak miktardır. Bu deneyim sorunlu olabilir çünkü kullanıcılar sipariş karşılama yoluyla teslim alma işlemi gerçekleştirirken teslim alım için bazı maddeleri seçmeyi unutabilirler.

**Satış Noktası'nda teslim alma siparişi işleme için geliştirilmiş kullanıcı deneyimi** özelliği, kullanıcılara teslim alınacak ürünlerin seçimi ve teslim alınacak ürünlerin miktarı üzerinde daha fazla kontrol sağlar. Kullanıcıların **Teslim al**'ı seçmeden önce sipariş karşılama sayfasındaki satış siparişinin her satırını seçmeleri gerekmez. Teslim alınabilecek tüm maddeler gösterilir. Kullanıcılar, yalnızca bir ürün satırı seçili olsa bile teslim alma için birden çok satır belirtebilir.

**Satış Noktası'nda teslim alma siparişi işleme için geliştirilmiş kullanıcı deneyimi** özelliği açıldığında ve **Teslim al** işlemini seçtiğinizde, **Teslim al** iletişim kutusu görüntülenir. Burada, teslim alınacak maddeleri ve miktarları seçebilirsiniz. Varsayılan olarak, teslim alındı veya paketlendi durumda stoku olan sipariş edilmiş herhangi bir miktar, teslim alım için uygun kabul edilir. Varsayılan olarak, bu miktar teslim alma miktarı olarak ayarlanır. Miktarın 0 (sıfır) olmaması ve seçili satır için toplam açık (yani, faturalanmamış) miktarı aşmaması koşuluyla, girilen miktarı değiştirebilirsiniz.

![Teslim al iletişim kutusu.](media/pickupselect.png)

Teslim alınacak miktarları seçtikten sonra **Teslim al**'ı seçtiğinizde hareket sayfası görüntülenir. [Çok yönlü kanal ödemeleri](omni-channel-payments.md) özelliği açıksa ve önceden yetkilendirilmiş kredi kartı ödemeleri varsa ödemeyi uygulamanız gerekir.

Hareket sayfasında, sistem seçilen satın alma maddeleri için ödenmesi gereken toplamı hesaplayarak ve daha önce uygulanan para yatırmaları veya yetkili kredi kartı ödemelerini çıkararak vadesi gelen tutarları hesaplar. Teslim alma hareketini tamamlamak için ödemeyi işlemeniz gerekir. Hareket sayfasının [ekran düzeni](pos-screen-layouts.md) **Hareketi sonlandır** işlemini de kapsayacak şekilde yapılandırılmışsa ve borç miktarı yoksa, bir ödeme yöntemi seçmeden hareketi tamamlayabilirsiniz. **Hareketi sonlandır** işlemi kullanılamıyorsa, bir ödeme yöntemi seçmek zorunda kalmadan hareketi sonuçlandırmak için **Toplamlar** bölmesinde **Borç tutarı: 0,00 TL** bağlantısını seçebilirsiniz.

![Müşteri siparişi teslim alma hareketi için hareket sayfası.](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Teslim alma satırlarını veya miktarlarını değiştirme

Teslim alınacak maddeleri seçtikten sonra teslim alma miktarını değiştirmeniz gerekiyorsa **Miktarı ayarla**'yı seçebilirsiniz. Teslim alma miktarını **0** (sıfır) olarak ayarlayamaz veya sipariş edilen satır için kalan faturalanmamış miktarı aşan bir değere artıramazsınız. Hareket sepetinden bir teslim alma satırını kaldırmak için **Hareketi geçersiz kıl**'ı seçin. Mevcut hareket durdurulacak ve **Teslim alma** işleminin akışı yeniden başlatılacaktır.

**Satış Noktası'nda teslim alma siparişi işleme için geliştirilmiş kullanıcı deneyimi** özelliği açıksa kuruluşlar hareket sayfasının ekran düzenine **Teslim alma satırlarını değiştir** işlemi için bir düğme ekleyebilir. POS'ta teslim alma hareketi sepetini oluşturup maddeleri seçtikten sonra, teslim alma maddelerini değiştirmeniz gerekiyorsa ancak tüm hareketi geçersiz kılmak istemiyorsanız **Teslim alma satırlarını değiştir**'i seçebilirsiniz. Görüntülenen **Teslim alma satırlarını değiştir** iletişim kutusunda, teslim alma maddelerini ve miktarlarını değiştirebilirsiniz. İşlem sepeti daha sonra değişikliklerinizi yansıtacak şekilde güncelleştirilir.

![Teslim alma maddelerini değiştir iletişim kutusu.](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]