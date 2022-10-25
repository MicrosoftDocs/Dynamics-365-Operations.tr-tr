---
title: Talep-temelli planlama
description: Makalede, ayırma noktaları olarak ayarlanmış kalemler için planlı siparişlerin nasıl oluşturulacağı açıklanmaktadır.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f1e2cfca47d507c8de7f9323bb8e4262a0e90949
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689217"
---
# <a name="demand-driven-planning"></a>Talep-temelli planlama

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Makalede, ayırma noktaları olarak ayarlanmış kalemler için planlı siparişlerin nasıl oluşturulacağı açıklanmaktadır.

## <a name="net-flow-and-qualified-demand"></a>Net akış ve nitelikli talep

Master planlama sırasında sistem, eldeki fiili stoğa dayalı olarak mevcut etkin miktarı belirlemek için *net akış*, artı siparişte olan stok (henüz alınmamış mevcut tedarik siparişleri), eksi *nitelikli talep* (nitelikli yaklaşan satışlar) kavramlarını aşağıdaki çizimde gösterildiği gibi uygular. Sistem, bir kalemin hangi tampon bölgeye ait olduğunu ve sipariş edilen miktarın ne olması gerektiğini belirlerken, eldeki fiili stoğu değil net akışı değerlendirir.

![Net akış hesaplama tablosu örneği.](media/ddmrp-net-flow-example.png "Net akış hesaplama grafik örneği")

Bir planlama çalıştırması sırasında planlı bir sipariş tetiklendiğinde, sipariş edilen miktar maksimum seviyeden net akış çıkarılacaktır. Bir sipariş önceliği atamak için sistem, gereksinim tarihleri yerine [öncelik-temelli planlama](priority-based-planning.md) işlevini kullanır. Talep Temelli Malzeme Gereksinimleri Planlaması (DDMRP), sipariş edilen miktara göre planlı bir siparişin önceliğini maksimum stok yüzdesi olarak atar. Önceki çizimde, sipariş edilen miktar, maksimum miktarın yüzde 53'üdür. Bu nedenle, stok yenileme için sipariş önceliği 53 olacaktır. (Bağlam için 0 en yüksek önceliktir ve 100 en düşük önceliktir.)

*Nitelikli talep* vadesi geçmiş talep, artı bugünün talebi ve gelecekteki nitelikli siparişteki ani artışlarıdır. Aşağıdaki çizimde, bugün (12 Haziran) ve sonraki üç gün için talep seviyelerinin bir örneği gösterilmektedir. DDMRP, normal beklentileri aşan talebi belirlemek için sipariş ani artışı eşiği belirlemenize olanak sağlar. Eşik 25 parça olarak ayarlanırsa, çizimde gösterilen gelecek tarihlerden ikisi, sipariş ani artışı olarak nitelendirilecektir. [Ayırma noktası maddesi için arabellekleri ayarlama](ddmrp-buffer-profile-and-levels.md#set-up-buffers) bölümünde açıklandığı gibi, **Madde kapsamı** sayfasını kullanarak her ürün için ayrı ayrı sipariş ani artışı eşiği atamanız gerekir.

![Nitelikli talep hesaplama grafik örneği.](media/ddmrp-net-qualified-demand-example.png "Nitelikli talep hesaplama grafik örneği")

Vadesi geçmiş talep olmaması kaydıyla, şimdi 73'lük nitelikli bir talep elde etmek için iki ani sipariş artışının (29 ve 26) miktarlarına bugünün talebini (18) ekleyebilirsiniz. 23 Haziran için talep olmasına rağmen, net akış hesaplamasına dahil edilmediğine dikkat edin çünkü DDMRP planlı siparişi geleneksel planlama kapsam gruplarından farklı şekilde tetikler.

## <a name="generating-planned-orders-with-ddmrp"></a>DDMRP ile planlı siparişler oluşturma

Planlama çalıştırması sırasında, maddenin net akışı yeniden sipariş noktasının altına düşerse sistem yeni bir planlı sipariş oluşturur. DDMRP kullandığınızda, genellikle her gün bir planlama çalışması yaparsınız. Bu nedenle, hangi öğelerin yenilenmesi gerektiğini belirlemek için aslında stok seviyenizi günde bir kez kontrol edersiniz.

Aşağıdaki çizimde, 20 Haziran'da 18 adet, 21 Haziran'da 29 adet, 22 Haziran'da 26 adet ve 23 Haziran'da 20 adet siparişiniz olduğu bir duruma ilişkin örnek gösterilmektedir. Ani artışı eşiği 25 adet olarak ayarlandığından, bu siparişlerden ikisi ani artış olarak işaretlenir. Bu maddeden elde 220 adet bulunmaktadır.

![Planlama örneği 1.](media/ddmrp-planning-example-1.png "Planlama örneği 1")

Master planlamayı şimdi çalıştırırsanız, net akışın yeniden sipariş noktasının altına düştüğü tespit edilirse (bu örnekte 219 adet) planlı bir sipariş oluşturacaktır.

![Planlama örneği 2.](media/ddmrp-planning-example-2.png "Planlama örneği 2")

Bu örnek, maksimum düzeyden net akışın çıkarılmasıyla elde edilen 130 miktarı için planlı bir satınalma siparişi üretir. Planlanan siparişe, maksimum miktarın yüzdesine göre 53,07 öncelik atanır. Bu değerler 20 Haziran'da bulunduğundan, sistem 20 Haziran tarihli planlı bir sipariş artı madde için ayrıştırılmış sağlama süresi (bu örnekte beş iş günü) oluşturur. Bu nedenle, bugünden itibaren beş iş günü bir hafta olduğu için planlanan sipariş tarihi 27 Haziran'dır.

> [!NOTE]
> Planlama Optimizasyonu, yalnızca ayrılmış maddeleri DDMRP kullanarak hesaplar. Diğer tüm maddeler, standart malzeme gereksinimleri planlaması (MRP) kullanılarak hesaplanır.
