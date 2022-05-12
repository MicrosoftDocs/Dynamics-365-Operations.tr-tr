---
title: WHS öğeleri için Inventory Visibility desteği
description: Bu konu, Stok Görünürlüğü'nün gelişmiş ambar işlemleri (WHS öğeleri) için etkinleştirilen öğeleri desteklemesini açıklar.
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625408"
---
# <a name="inventory-visibility-support-for-whs-items"></a>WHS öğeleri için Inventory Visibility desteği

[!include [banner](../includes/banner.md)]

Bu konu, Stok Görünürlüğü'nün gelişmiş ambar işlemleri (WHS öğeleri) için etkinleştirilen öğeleri desteklemesini açıklar. Bu yeteneği Stok Görünürlüğüne ekleyen özellik *Gelişmiş WHS* olarak adlandırılır.

## <a name="whs-items"></a>WHS maddeleri

Bir WHS maddesi, gelişmiş ambar işlemleri (WHS) etkinleştirilmiş ve aynı zamanda etkin olan bir ambarda işlenen bir maddedir.

Microsoft Dynamics 365 Supply Chain Management içindeki **Ambar yönetim** modülü hakkında daha fazla bilgi için, bkz. [Ambar yönetimine genel bakış](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Özellik kapsamı

Stok görünürlüğünün gelişmiş WHS özelliği eldeki sorguları temel alan eldeki miktar hesaplamalarına odaklanır. Bu özellik genel olarak ambar işleme faaliyetlerini yönetmek için stok görünürlüğünü kullanmanıza olanak vermek amacıyla tasarlanmamıştır. Stok Görünürlüğü, kendi kullanıcılarına ambara özgü kavramlar ortaya çıkarmaz. Aşağıda bu kavramların bazı örnekleri verilmiştir:

- Rezervasyon hiyerarşisi
- Bir madde veya ambarın WHS destekli olup olmadığı
- Birim sıra grubu kodu
- Sevk irsaliyeleri, yüklemeler, dalgalar ve çalışma gibi ambara özgü işlemler

Stok Görünürlüğü, bu bilgileri Supply Chain Management gönderilen verilere göre sorgular. WHS'ye özel veriler (başka bir deyişle, `WHSInventReserve` tablosundaki veriler) kullanıcılar tarafından görülemez.

Stok görünürlüğü için Gelişmiş WHS özelliğini kullandığınızda, tüm sorgu sonuçları, doğrudan Supply Chain Management'ta yapılan sorgulardan elde edilen sonuçlarla aynı olacaktır. Ancak, mobil uygulama biraz farklı hesaplama mantığı kullandığından, bunlar Warehouse Management mobile app kullanılarak yapılan sorgulardan elde edilen sonuçlarla aynı olmayacaktır.

## <a name="when-to-use-the-feature"></a>Özelliğin ne zaman kullanılacağı

Aşağıdaki koşulların tümünün yerine getirilebileceği senaryolarda stok görünürlüğü için Gelişmiş WHS özelliğini kullanmanızı öneririz:

- Stok görünürlüğünün Supply Chain Management verilerini eşitliyorsunuz.
- Supply Chain Management'ta WHS kullanıyorsunuz.
- Kullanıcılar, ambar düzeyinden farklı düzeylerdeki WHS maddeler için rezervasyonlar yapar (örneğin, ambar çalışmasını kullandığınızdan).

Diğer senaryolarda, stok görünürlüğünün gelişmiş WHS özelliğinin etkin olup olmamasına bakılmaksızın eldeki sorgu sonuçları aynı olacaktır. Ek olarak, bu senaryolarda özelliği etkinleştirmezseniz, daha az hesaplama ve daha az ek yükü olduğundan performans daha iyi olacaktır.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Stok görünürlüğü için Gelişmiş WHS özelliğini etkinleştir

Stok görünürlüğü için Gelişmiş WHS özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. Supply Chain Management ortamınızda yönetici olarak oturum açın.
1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını açın ve aşağıdaki özellikleri etkinleştirin, aşağıdaki sırada:

    1. *Stok Görünürlüğü tümleştirmesi*
    1. *Stok Görünürlüğünde ambar maddelerini etkinleştir*

1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri**'ne gidin.
1. **WHS Maddelerini etkinleştir** sekmesinde, **WHS Maddelerini etkinleştir** seçeneğini *Evet* olarak ayarlayın.
1. Power Apps'da oturum açın.
1. **Yapılandırma** sayfasını açın ve ardından **Özellik Yönetimi** sekmesinde, *AdvancedWHS* özelliğini etkinleştirin.
1. Supply Chain Management'ta, **Stok Yönetimi \> Periyodik Görevler \> Stok Görünürlüğü tümleştirmesi**'ne gidin.
1. Eylem Bölmesinde, Stok Görünürlüğünü geçici olarak devre dışı bırakmak için **Devre dışı bırak**'ı seçin.
1. Eylem Bölmesinde, Stok Görünürlüğünü yeniden etkinleştirmek için **Etkinleştir**'i seçin. Eklenti yeniden yüklenir ve yeni özellik şimdi etkinleştirilmiştir. WHS bağlantılı verileriniz Stok Görünürlüğüne eşitlenmeye başlar.

## <a name="query-on-hand-quantities-of-whs-items"></a>WHS maddelerinin eldeki miktarlarını sorgula

WHS öğelerini sorgulamak için, WHS olmayan öğeler için kullandığınız [uygulama programlama arabirimini (API) ve ileti sözdizimini](inventory-visibility-api.md) kullanırsınız. Bir maddenin bir WHS maddesi mi yoksa bir WHS olmayan madde mi olduğunu belirtmek zorunda değilsiniz. Stok Görünürlüğü, depolanan verilere dayalı olarak, maddeleri otomatik olarak ayırır.

WHS maddeleri için olan sorguların sonuçları esas olarak, WHS olmayan maddelerle ilgili sonuçlarla aynıdır. Tek fark, `fno` veri kaynağından alınan aşağıdaki fiziksel önlemlerin Supply Chain Management'ta WHS mantığına göre hesaplanmasını sağlar:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Diğer tüm fiziksel ölçüler, stok görünürlüğü için Gelişmiş WHS özelliği devre dışı bırakıldığında olduğu gibi hesaplanır.

WHS maddeleri için eldeki hesaplamaların nasıl çalıştığı hakkında ayrıntılı bilgi edinmek için, bkz. [Ambar yönetiminde rezervasyonlar](https://www.microsoft.com/download/details.aspx?id=43284) teknik incelemesi.

Dataverse'e aktarılan veri varlıkları henüz diğer WHS madde miktarlarını güncelleştiremez. Veri varlıklarında gösterilen miktarlar, hem WHS olmayan maddeler hem de WHS mantığdan etkilenmeyen miktarlar (`AvailPhysical`, `AvailOrdered`, `ReservPhysical`, `ReservOrdered` ve `fno` veri kaynağı dışında) için doğrudur.

Supply Chain Management veri kaynağında depolanan, WHS madde miktarlarındaki değişikliklere izin verilmez. Stok Görünürlüğünün diğer özellikleri gibi, çakışmaların engellenmesine yardımcı olmak için bu sınırlama uygulanır.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Stok Görünürlüğünde WHS maddeleri için geçici rezervasyon

Genel olarak, WHS maddelerinde [geçici rezervasyon](inventory-visibility-reservations.md) desteklenir. WHS ile ilgili fiziksel ölçüleri, geçici ayırma hesaplamalarına dahil edebilirsiniz. 

Bilinen bir sınırlamaya göre, şu anda, WHS maddeleri için *rezervasyon* hesaplaması kullanılabilir durumda değildir. Bu nedenle, geçici rezervasyonun bulunduğu geçerli boyutların üzerinde rezervasyon varsa, *rezervasyon* hesaplaması için kullanılabilir. [Geçici ayırma API'sinde](inventory-visibility-api.md#create-one-reservation-event) **ifCheckAvailForReserv** seçeneği devre dışı bırakıldığında, yazılım ayırmaları etkilenmez.

Bu sınırlama, yazılım ayırmalarını temel alan özellikler ve özelleştirmeler için de geçerlidir (örneğin, ayırma).

## <a name="calculate-available-to-promise-quantities"></a>Taahhüde kullanılabilir miktarları hesapla

Çözüm, WHS maddeleri için [taahhüde kullanılabilir (ATP)](inventory-visibility-available-to-promise.md) destekler. ATP hesaplamalarını, WHS'ye özgü ayrıntıları endişelenmeden tanımlayabilirsiniz.
