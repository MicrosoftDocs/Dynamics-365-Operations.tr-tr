---
title: WMS öğeleri için Inventory Visibility desteği
description: Bu makale, Stok Görünürlüğü'nün ambar yönetim süreçleri (WMS öğeleri) için etkinleştirilen öğeleri desteklemesini açıklar.
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
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066625"
---
# <a name="inventory-visibility-support-for-wms-items"></a>WMS öğeleri için Inventory Visibility desteği

[!include [banner](../includes/banner.md)]

Bu makale, Stok Görünürlüğü'nün ambar yönetim süreçleri (WMS) için etkinleştirilen öğeleri desteklemesini açıklar. Bu yeteneği Stok Görünürlüğüne ekleyen özellik *Gelişmiş WMS* olarak adlandırılır.

## <a name="wms-items"></a>WMS maddeleri

Bir WMS öğesi, WMS için etkinleştirilmiş ve aynı zamanda WMS özellikli bir ambarda işlenen bir öğedir.

Microsoft Dynamics 365 Supply Chain Management içindeki **Ambar yönetim** modülü hakkında daha fazla bilgi için bkz. [Ambar yönetimine genel bakış](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Özellik kapsamı

Stok görünürlüğünün gelişmiş WMS özelliği eldeki sorguları temel alan eldeki miktar hesaplamalarına odaklanır. Bu özellik genel olarak ambar işleme faaliyetlerini yönetmek için stok görünürlüğünü kullanmanıza olanak vermek amacıyla tasarlanmamıştır. Stok Görünürlüğü, kendi kullanıcılarına ambara özgü kavramlar ortaya çıkarmaz. Aşağıda bu kavramların bazı örnekleri verilmiştir:

- Rezervasyon hiyerarşisi
- Bir madde veya ambarın WMS destekli olup olmadığı
- Birim sıra grubu kodu
- Sevk irsaliyeleri, yüklemeler, dalgalar ve çalışma gibi ambara özgü işlemler

Stok Görünürlüğü, bu bilgileri Supply Chain Management gönderilen verilere göre sorgular. WMS'ye özel veriler (başka bir deyişle, `WHSInventReserve` tablosundaki veriler) kullanıcılar tarafından görülemez.

Stok görünürlüğü için Gelişmiş WMS özelliğini kullandığınızda, tüm sorgu sonuçları, doğrudan Supply Chain Management'ta yapılan sorgulardan elde edilen sonuçlarla aynı olacaktır. Ancak, mobil uygulama biraz farklı hesaplama mantığı kullandığından, bunlar Warehouse Management mobile app kullanılarak yapılan sorgulardan elde edilen sonuçlarla aynı olmayacaktır.

## <a name="when-to-use-the-feature"></a>Özelliğin ne zaman kullanılacağı

Aşağıdaki koşulların tümünün yerine getirilebileceği senaryolarda stok görünürlüğü için Gelişmiş WMS özelliğini kullanmanızı öneririz:

- Stok görünürlüğünün Supply Chain Management verilerini eşitliyorsunuz.
- Supply Chain Management'ta WMS kullanıyorsunuz.
- Kullanıcılar, ambar düzeyinden farklı düzeylerdeki WMS maddeler için rezervasyonlar yapar (örneğin, ambar çalışmasını kullandığınızdan).

Diğer senaryolarda, stok görünürlüğünün gelişmiş WMS özelliğinin etkin olup olmamasına bakılmaksızın eldeki sorgu sonuçları aynı olacaktır. Ek olarak, bu senaryolarda özelliği etkinleştirmezseniz, daha az hesaplama ve daha az ek yükü olduğundan performans daha iyi olacaktır.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Stok görünürlüğü için Gelişmiş WMS özelliğini etkinleştir

Stok görünürlüğü için Gelişmiş WMS özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. Supply Chain Management ortamınızda yönetici olarak oturum açın.
1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını açın ve aşağıdaki özellikleri etkinleştirin, aşağıdaki sırada:

    1. *Stok Görünürlüğü tümleştirmesi*
    1. *Stok Görünürlüğünde ambar maddelerini etkinleştir*

1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri**'ne gidin.
1. **WMS Maddelerini etkinleştir** sekmesinde, **WMS Maddelerini etkinleştir** seçeneğini *Evet* olarak ayarlayın.
1. Power Apps'da oturum açın.
1. **Yapılandırma** sayfasını açın ve ardından **Özellik Yönetimi** sekmesinde, *AdvancedWHS* özelliğini etkinleştirin.
1. Supply Chain Management'ta, **Stok Yönetimi \> Periyodik Görevler \> Stok Görünürlüğü tümleştirmesi**'ne gidin.
1. Eylem Bölmesinde, Stok Görünürlüğünü geçici olarak devre dışı bırakmak için **Devre dışı bırak**'ı seçin.
1. Eylem Bölmesinde, Stok Görünürlüğünü yeniden etkinleştirmek için **Etkinleştir**'i seçin. Eklenti yeniden yüklenir ve yeni özellik şimdi etkinleştirilmiştir. WMS bağlantılı verileriniz Stok Görünürlüğüne eşitlenmeye başlar.

## <a name="query-on-hand-quantities-of-wms-items"></a>WMS maddelerinin eldeki miktarlarını sorgula

WMS öğelerini sorgulamak için, WMS olmayan öğeler için kullandığınız [uygulama programlama arabirimini (API) ve ileti sözdizimini](inventory-visibility-api.md) kullanırsınız. Bir maddenin bir WMS maddesi mi yoksa bir WMS olmayan madde mi olduğunu belirtmek zorunda değilsiniz. Stok Görünürlüğü, depolanan verilere dayalı olarak, maddeleri otomatik olarak ayırır.

WMS maddeleri için olan sorguların sonuçları esas olarak, WMS olmayan maddelerle ilgili sonuçlarla aynıdır. Tek fark, `fno` veri kaynağından alınan aşağıdaki fiziksel önlemlerin Supply Chain Management'ta WMS mantığına göre hesaplanmasını sağlar:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Diğer tüm fiziksel ölçüler, stok görünürlüğü için Gelişmiş WMS özelliği devre dışı bırakıldığında olduğu gibi hesaplanır.

WMS maddeleri için eldeki hesaplamaların nasıl çalıştığı hakkında ayrıntılı bilgi edinmek için bkz. [Ambar yönetiminde rezervasyonlar](https://www.microsoft.com/download/details.aspx?id=43284) teknik incelemesi.

Dataverse'e aktarılan veri varlıkları henüz diğer WMS madde miktarlarını güncelleştiremez. Veri varlıklarında gösterilen miktarlar, hem WMS olmayan maddeler hem de WMS mantığdan etkilenmeyen miktarlar (`AvailPhysical`, `AvailOrdered`, `ReservPhysical`, `ReservOrdered` ve `fno` veri kaynağı dışında) için doğrudur.

Supply Chain Management veri kaynağında depolanan, WMS madde miktarlarındaki değişikliklere izin verilmez. Stok Görünürlüğünün diğer özellikleri gibi, çakışmaların engellenmesine yardımcı olmak için bu sınırlama uygulanır.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Stok Görünürlüğünde WMS maddeleri için geçici rezervasyon

Genel olarak, WMS maddelerinde [geçici rezervasyon](inventory-visibility-reservations.md) desteklenir. WMS ile ilgili fiziksel ölçüleri, geçici ayırma hesaplamalarına dahil edebilirsiniz. 

Bilinen bir sınırlamaya göre, şu anda, WMS maddeleri için *rezervasyon* hesaplaması kullanılabilir durumda değildir. Bu nedenle, geçici rezervasyonun bulunduğu geçerli boyutların üzerinde rezervasyon varsa, *rezervasyon* hesaplaması için kullanılabilir. [Geçici ayırma API'sinde](inventory-visibility-api.md#create-one-reservation-event) **ifCheckAvailForReserv** seçeneği devre dışı bırakıldığında, yazılım ayırmaları etkilenmez.

Bu sınırlama, yazılım ayırmalarını temel alan özellikler ve özelleştirmeler için de geçerlidir (örneğin, ayırma).

## <a name="calculate-available-to-promise-quantities"></a>Taahhüde kullanılabilir miktarları hesapla

Çözüm, WMS maddeleri için [taahhüde kullanılabilir (ATP)](inventory-visibility-available-to-promise.md) destekler. ATP hesaplamalarını, WMS'ye özgü ayrıntıları endişelenmeden tanımlayabilirsiniz.
