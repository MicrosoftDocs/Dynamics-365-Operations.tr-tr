---
title: Maliyetlendirme tabloları
description: Maliyetlendirme tablosunun kurulumu için iki hedef gerekir. İlk hedef olarak, üretilmiş bir madde veya üretim emri hakkındaki satılan malların maliyetini görüntüleme biçimini tanımlarsınız. Biçimlendirilmiş görüntüye maliyetlendirme tablosu adı verilir. İkinci hedef olarak, dolaylı maliyetleri hesaplama temelini tanımlarsınız. Maliyetlendirme tablosu kurulumu, bilgi görüntüleme ve dolaylı maliyet hesaplama formülleri için maliyet grubu özelliğini temel alır. Bu makalede maliyetlendirme tablosu kurulumunun iki hedefi açıklanmıştır.
author: JennySong-SH
ms.date: 11/18/2021
ms.topic: article
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6891fc4472e714133a7d0cdf77f2908becc0547c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672444"
---
# <a name="costing-sheets"></a>Maliyetlendirme tabloları

[!include [banner](../includes/banner.md)]

Maliyetlendirme tablosunun kurulumu için iki hedef gerekir. İlk hedef olarak, üretilmiş bir madde veya üretim emri hakkındaki satılan malların maliyetini görüntüleme biçimini tanımlarsınız. Biçimlendirilmiş görüntüye maliyetlendirme tablosu adı verilir. İkinci hedef olarak, dolaylı maliyetleri hesaplama temelini tanımlarsınız. Maliyetlendirme tablosu kurulumu, bilgi görüntüleme ve dolaylı maliyet hesaplama formülleri için maliyet grubu özelliğini temel alır. Bu makalede maliyetlendirme tablosu kurulumunun iki hedefi açıklanmıştır. 

Aşağıdaki tabloda, varsayılan ayarlar tarafından her role verilen erişim düzeyi de dahil olmak üzere, maliyetlendirme sayfalarına erişebilen hazır olmayan güvenlik rolleri listelenmiştir.

| Rol | Erişim
|---|---|
| Muhasebe müdürü | Düzenle |
| Stok muhasebe memuru | Göster |
| Stok muhasebecisi | Göster |

Maliyetlendirme tablosu, üretilmiş bir ürün veya bir üretim emri için satılmış olan malların maliyeti hakkındaki görüntüleme biçimidir. Bir maliyetlendirme tablosu ayarladığınızda, bilgilerin biçimini ve de dolaylı maliyetlerin hesaplanmasının bazını tanımlayabilirsiniz. Maliyetlendirme tablosu kurulumu, bilgi görüntüleme ve dolaylı maliyet hesaplama formülleri için maliyet grubu özelliklerini temel alır. Maliyetlendirme tablosu ayarının iki hedefi hakkında daha fazla bilgi şu şekildedir:

- **Maliyetlendirme tablosunun biçimini tanımlayın.** Bir maliyetlendirme tablosu için kullanıcı tanımlı biçim, üretilmiş olan satılan malların maliyetini içeren maliyetlerin segmentasyonunu belirler. Örneğin, bir ürünün satılan mallarının maliyeti, maliyet gruplarına dayalı olarak malzeme, işçilik ve genel giderler olarak bölümlenebilir. Bu maliyet grupları ürünlere, rota operasyonları için maliyet kategorilerine ve dolaylı maliyet hesaplama formüllerine atanır. Maliyetlendirme tablosunun biçimi, birden fazla maliyet grubu tanımlandığında genellikle ara toplamları gerektirir. Örneğin, malzemeyle ilişkili birden çok maliyet grubu bir araya toplanabilir. Maliyetlendirme tablosu biçiminin tanımlanması isteğe bağlıdır, ancak dolaylı maliyetler hesaplanacaksa bir maliyetlendirme tablosu biçiminin tanımlanması gerekir.
- **Dolaylı maliyetlerin hesaplanma temelini tanımlayın.** Dolaylı maliyetler, üretilmiş bir ürünün imalatıyla ilişkili üretim genel giderini yansıtır. Dolaylı maliyet hesaplama formülü bir ek talep ya da oran olarak ifade edilebilir. Ek talep, bir değerin yüzdesini, oran ise bir rota operasyonu için saat başına tutarı temsil eder. Bir maliyet grubu, bir işçilik maliyeti grubu için yüzde 100 ek talep veya makine maliyet grubu için 50,00 ABD Doları saatlik oran gibi, hesaplama formülünün temelini tanımlar. Bir hesaplama formülü ve maliyet grubu temelini tanımlamak istiyorsanız, genel gideri temsil eden maliyet grubunu tanımlamanızı ve kullanılan bir ek talep ya da oran yaklaşımının seçilmesini gerektirir.

Her hesap formülünün bir maliyet kaydı olarak girilmesi gerekir. Maliyet kaydı belirtilen bir maliyetlendirme sürümünden, bir ek talep yüzdesi veya bir oran tutarı, maliyet grubu temeli, bir durum ve bir yürürlük tarihinden oluşur. Bir maliyet kaydı ilk olarak girildiğinde **Bekleyen** durumundadır ve bir yürürlük tarihi vardır. Maliyet kaydını etkinleştirdiğinizde, kaydın durumu geçerli etkin kayıt olacak şekilde güncellenir ve yürürlük tarihi de etkinleştirme tarihine güncellenir. Maliyet kaydı, tesise özel bir hesaplama formülü için bir tesisi de belirtebilir. Alternatif olarak, hesaplama formülünü şirket genelinde bir formül belirtmek için **Tesis** alanını boş bırakabilirsiniz. Maliyet kaydı isteğe bağlı olarak, hesaplama formülü ürün başına işaretlendiğinde belirtilen bir ürünü veya ürün grubunu içerebilir. 

Dolaylı maliyet hesaplama formülleri için geçerli etkin maliyet kayıtları, üretim emri maliyetlerini tahmin etmek için kullanılır. Aynı zamanda, gerçek zaman ve malzeme tüketimiyle ilgili fiili maliyetleri hesaplamak için de kullanılır. Bekleyen maliyet kayıtları gelecek bir tarih için ürün reçetesi (BOM) hesaplamalarında kullanılır. 

Bir maliyetlendirme versiyonu için geçerli olan iki engelleme ilkesi, bekleyen maliyetlerin sürdürülebilirliğini ve bekleyen maliyetin başlatılabilirliğini belirler. Engelleme ilkelerini, veri sürdürmeye izin vermek ve bir maliyetlendirme versiyonu içersindeki maliyet verileri için veri sürdürmeyi engellemek için kullanın. 

Maliyetlendirme tablosu biçimini ve dolaylı maliyetlerin hesaplamalarını tanımladıktan sonra, bilgileri doğrulamak ve kaydetmek için ayrı bir adım gerçekleştirmelisiniz. Maliyetlendirme tablosu, satılan malların maliyeti hakkındaki bilgilerin tutarlı biçimde görüntülenebilmesi için şirket çapında bir biçimi temsil eder. 

Maliyetlendirme tablosu **Ürün maliyetini hesapla** sayfasının bir kısmı olarak görüntülenir. Maliyetlendirme tablosu, **Ürün fiyatı** sayfasında üretilmiş bir ürünün hesaplanmış maliyet kaydı veya **Ürün reçetesi hesaplama sonuçları** sayfasında siparişe özgü bir hesaplama kaydı için görüntülenebilir. Ayrıca, bir üretim emrinin **Fiyat hesaplama** sayfasının bir bölümü olarak da görüntülenebilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
