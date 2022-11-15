---
title: Stok işaretleme
description: Bu makalede, kesinleştirilmiş siparişlerde stok işaretleme için kullanılabilecek seçenekler hakkında bilgi sağlanmaktadır.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740616"
---
# <a name="inventory-marking"></a>Stok işaretleme

[!include [banner](../../includes/banner.md)]

Bu makalede, kesinleştirilmiş siparişlerde stok işaretleme için kullanılabilecek seçenekler hakkında bilgi sağlanmaktadır.

*İşaretleme*, arz ve talebi bağlamak için kullanılır. Master planlamanın talebin nasıl olmasını beklediğini gösteren bir *ilişkilendirmeye* benzerdir. Planlama açısından temel fark işaretlemenin ilişkilendirmeden daha kalıcı olmasıdır.

İşaretleme özelliği, ilk giren ilk çıkar (FIFO) ve son giren ilk çıkar (LIFO) yaklaşımları için özel maliyetlendirme senaryolarını desteklemek üzere sunulmuştur. Ancak, artık bazı maliyetlendirme dışı senaryolar için de kullanılmaktadır. Arz ve talep arasında işaretleme isteğe bağlıdır ve neredeyse kalıcıdır. İşaretleme kullanıcı tarafından el ile kaldırılabileceği gibi, **İşaretlemeyi kaldır** seçeneğinin belirlendiği bir satış siparişi satırı açılımı çalıştırılarak da kaldırılır.

İlişkilendirme, talebi gerekli arzla bağlamak için kapsama sırasında master planlama tarafından kontrol edilir. İlişkilendirme, her planlama çalışmasının talebi kapsaması gereken arzı iyileştirmesi için güncelleştirilebilir. Master planlama, ilişkilendirme bilgilerini güncelleştirdiğinde, var olan tüm işaretler korunur.

İlişkilendirme; ilgili işaret, eldeki rezervasyonlar ve siparişe ait rezervasyonları dahil ederek aşağıdaki sırada başlar:

1. Talep ve arz arasında işaretleme
1. Eldeki rezervasyonlar
1. Siparişteki rezervasyonlar

Planlı bir siparişi kesinleştirirken, **Kesinleştirme** iletişim kutusu kesinleştirme sırasında oluşturulan siparişler için işaretleme seçeneklerini ayarlamak amacıyla kullanabileceğiniz bir **İşaretlemeyi güncelleştir** alanı sağlar. Aşağıdaki değerlerden birini seçin:

- *Hayır*: Stok işaretleme uygulanmaz.
- *Standart*: Stok işaretleme ilişkilendirmeye göre güncelleştirilir. Bir karşılama siparişi (arz) karşılığında bir gereksinim siparişi (talep) işaretlenir. Bazı miktarlar, karşılama siparişinde kalırsa işaretlenmez ve başvuru bilgileri boş bırakılır. Örneğin, 100 ea değerinde bir satış siparişi 150 ea değerinde bir satın alma siparişiyle ilişkilendirildirse, başvuru bilgileri yalnızca satış siparişine atanır.
- *Genişletilmiş*: Herhangi bir miktarın karşılama siparişinde kalıp kalmadığına bakılmaksızın, hem gereksinim siparişi (talep) hem karşılama siparişi (arz) işaretlenir. Örneğin, 100 ea değerinde bir satış siparişi 150 ea değerinde bir satın alma siparişiyle ilişkilendirildirse, başvuru bilgileri hem satış siparişine hem de satın alma siparişine atanır.
- *Tek düzeyli standart* – Tek düzeyli işaretleme kullanılır. Tek düzeyli işaretleme, ürün reçetesi (BOM) bileşenlerini değil yalnızca ana maddeyi işaretler. Bu nedenle, kesinleştirme sonrasında üretime yönelik bileşen atamasını esnek tutabilirsiniz. Tek düzeyli işaretleme, sistemin son dakikada gelen talep değişiklikleri için optimizasyon yapmasına olanak tanır. Tek düzeyli *standart* işaretlemede, gereksinim siparişleri karşılama emirlerine göre işaretlenir, ancak kalan miktarı olan karşılama siparişleri işaretlenmez.
- *Tek düzeyli genişletilmiş* – Tek düzeyli işaretleme kullanılır. Tek düzeyli *genişletilmiş* işaretlemede, gereksinim siparişleri karşılama emirlerine göre işaretlenir ve kalan miktar bulunmasından bağımsız olarak karşılama siparişleri her zaman işaretlenir.

Sisteminiz için varsayılan işaretleme seçeneğini ayarlamak için **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin. Sonra, **Standart güncelleştirme** sekmesinde, **İşaretlemeyi güncelleştir** alanını tercih ettiğiniz seçeneğe ayarlayın.

> [!NOTE]
> *Tek düzeyli standart* ve *Tek düzeyli genişletilmiş* seçenekleri yalnızca, sisteminizde *Siparişe göre tedarik otomasyonu* özelliği etkinse kullanılabilir. Bu özellik ve nasıl etkinleştirileceği hakkında daha fazla bilgi için bkz. [Siparişe göre tedarik otomasyonu](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
