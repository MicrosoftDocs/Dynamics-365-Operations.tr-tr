---
title: Satış noktasında sipariş işlemini geri çekme
description: Bu konu, POS'taki geliştirilmiş sipariş geri çekme sayfaları için kullanılabilen özellik yeteneklerini açıklar.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799119"
---
# <a name="recall-order-operation-in-pos"></a>Satış noktasında sipariş işlemini geri çekme

[!include [banner](includes/banner.md)]

Commerce satış noktasındaki (POS) **sipariş geri çekme** işlemi, güncelleştirilmiş sipariş arama ve filtreleme özellikleri ve siparişe özel bilgiler sağlar. Bu özellik Commerce 10.0.15 sürümü ve sonrasında bulunur.

Bu işlevi etkinleştirmek için, Commerce Headquarters'daki **Özellik yönetimi** çalışma alanında yer alan **POS'taki iyileştirilmiş sipairş geri çekme işlemi** özelliğini açın. Özellik etkinleştirildikten sonra, değiştirilen bazı yeteneklerden yararlanmak için [ekran düzenlerini](pos-screen-layouts.md) güncelleştirmeyi düşünebilirsiniz.

**Sipariş geri çekme** işlemi düğmesinin yapılandırması, kuruluşların işlemi önceden tanımlanmış bir görüntü ile dağıtmasını sağlar.

![Düğme grubu yapılandırması](media/recallorderbuttongrid.png)

Ekran seçenekleri şunlardır:
- **Hiçbiri** – Bu seçenek, işlemi belirli bir ekran olmadan dağıtır. Kullanıcı bu yapılandırmayla işlemi açtığında, sipariş araması ve bulması veya önceden tanımlanmış bir sipariş filtresi seçmesi istenir.
- **Karşılanacak siparişler** – Kullanıcı operasyonu başlattığında, kullanıcının geçerli mağazası tarafından karşılanması gereken siparişlerin listesini arayıp görüntülemek için bir sorgu otomatik olarak çalışır. Bu siparişler, mağaza içi malzeme çekme veya mağaza sevkiyatı için yapılandırılır ve bu siparişlerin satırları henüz çekilmemiştir veya paketlenememiştir.
- **Çekilecek siparişler** – Kullanıcı operasyonu başlattığında, kullanıcının geçerli mağazasında mağazadan çekme için yapılandırılan siparişlerin listesini arayıp görüntülemek için bir sorgu otomatik olarak çalışır.
- **Sevk edilecek siparişler** – Kullanıcı operasyonu başlattığında, kullanıcının geçerli mağazasından sevkiyat için yapılandırılan siparişlerin listesini arayıp görüntülemek için bir sorgu otomatik olarak çalışır.

POS'tan **Sipariş geri çekme** işlemi başlatılırken, görüntü **Hiçbiri** olarak yapılandırıldığında, kullanıcı siparişleri aşağıdaki yollardan biriyle arayabilir ve alabilir.
- Sipariş barkodlarını tarama. Bu, eşleştirmeler için sipariş numarası, kanal referansı ve giriş kodu alanlarını arar.
- Filtre ölçütüne uyan siparişleri bulmak üzere filtreleme mekanizmasını kullanmak için uygulama çubuğunda **Siparişleri ara** veya **Ara ve filtrele** simgesini seçin.
- **Siparişleri Göster** açılır menüsünden (karşılanacak siparişler, alınacak siparişler veya sevk edilecek siparişler) önceden tanımlanmış filtreler arasından seçim yapın.

![RecallOrderMainMenu](media/recallordermain.png)

Arama ölçütleri uygulandıktan sonra, uygulama eşleşen satış siparişlerinin listesini görüntüler. Arama/filtre seçeneklerini kullanırken, alınan siparişlerin kullanıcının geçerli mağazasıyla bağlantılı siparişler olması gerekmediğini göz önünde bulundurun. Bu arama işlemi, sipariş başka bir mağaza/kanal ya da ambar konumu tarafından oluşturulmuş veya karşılanacak olsa bile arama ölçütleriyle eşleşen tüm müşteri siparişlerini alır ve görüntüler.

![RecallOrderDetail](media/orderrecalldetail.png)

Bir kullanıcı ek ayrıntıları görüntülemek için listeden bir sipariş seçebilir. Ekranın sağ tarafındaki bilgi paneli sipariş satırı detayları, teslimat detayları ve karşılama detayları da dahil olmak üzere seçili siparişle ilgili özellikleri görüntüler.

Uygulama çubuğunda, kullanıcı bir operasyon seçebilir. Siparişin durumuna bağlı olarak, belirli operasyonlar etkinleştirilmemiş olabilir.

- **İade** – Seçilen müşteri siparişindeki faturalanan ürünlerden herhangi biri için iade oluşturma sürecini başlatır.

- **İptal** – Seçili satış siparişinin tam iptalini yapar. Bu seçenek, çağrı merkezi kanalı aracılığıyla başlatılan siparişler için kullanılamaz ve bir siparişi kısmen iptal etmek için kullanılamaz.

- **Karşıla** – Kullanıcıyı, seçilen sipariş için ön filtre uygulanacak sipariş karşılama sayfasına aktarır. Yalnızca seçili sipariş için kullanıcının mağazası tarafından karşılanmaya açık olan sipariş satırları görüntülenir.

- **Düzenle** – Kullanıcıların seçili müşteri siparişinde değişiklik yapmasına olanak tanır. Siparişler yalnızca [belirli senaryolarda düzenlenebilir](customer-orders-overview.md#edit-an-existing-customer-order).

- **Teslim alma** -Siparişte, kullanıcının geçerli mağazasında ürün teslim alma için belirlenmiş bir veya daha fazla satır varsa, bu seçenek kullanılabilir. Bu işlem, kullanıcının teslim alınacak ürünleri seçmesine izin veren ve teslim alma satış işlemini oluşturan teslim alma akışını başlatır.

## <a name="add-notifications-to-the-recall-order-operation"></a>Sipariş geri çekme işlemine bildirim ekleme

İsterseniz, 10.0.18 ve sonrasında **sipariş geri çağırma** işlemi için POS bildirimleri canlı kutucuk uyarıları yapılandırabilirsiniz. Daha fazla bilgi için, bkz. [Satış noktasında (POS) sipariş bildirimlerini gösterme](notifications-pos.md).  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
