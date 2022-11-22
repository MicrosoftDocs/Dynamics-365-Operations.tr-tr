---
title: WMS öğeleri için Inventory Visibility desteği
description: Bu makale, Stok Görünürlüğü'nün ambar yönetim süreçleri (WMS öğeleri) için etkinleştirilen öğeleri desteklemesini açıklar.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762767"
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

Aşağıdaki koşulların tümünün yerine getirilebileceği senaryolarda stok görünürlüğü için WMS özelliğini kullanmanızı öneririz:

- Stok görünürlüğünün Supply Chain Management verilerini eşitliyorsunuz.
- Supply Chain Management'ta WMS kullanıyorsunuz.
- Kullanıcılar, ambar düzeyinin altındaki düzeylerdeki WMS maddeleri için rezervasyonlar yapar (örneğin, ambar işini işlediğinizden plaka düzeyinde).

Diğer senaryolarda, stok görünürlüğünün gelişmiş WMS özelliğinin etkin olup olmamasına bakılmaksızın eldeki sorgu sonuçları aynı olacaktır. Ek olarak, bu senaryolarda özelliği etkinleştirmezseniz, daha az hesaplama ve daha az ek yükü olduğundan performans daha iyi olacaktır.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Stok görünürlüğü için WMS özelliğini etkinleştir

Stok görünürlüğü için WMS özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. Supply Chain Management ortamınızda yönetici olarak oturum açın.
1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını açın ve aşağıdaki özellikleri etkinleştirin, aşağıdaki sırada:

    1. *Stok Görünürlüğü tümleştirmesi*
    1. *Stok Görünürlüğünde ambar maddelerini etkinleştir*

1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri**'ne gidin.
1. **WMS Maddelerini etkinleştir** sekmesinde, **WMS Maddelerini etkinleştir** seçeneğini *Evet* olarak ayarlayın.
1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
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

Diğer tüm fiziksel ölçüler, stok görünürlüğü için WMS özelliği devre dışı bırakıldığında olduğu gibi hesaplanır.

WMS maddeleri için eldeki hesaplamaların nasıl çalıştığı hakkında ayrıntılı bilgi edinmek için bkz. [Ambar yönetiminde rezervasyonlar](https://www.microsoft.com/download/details.aspx?id=43284) teknik incelemesi.

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>WMS maddeleri için eldeki stok liste görünümü ve veri varlığı

**Stok Görünürlüğü Özetini Önceden Yükle** sayfası, *Eldeki Dizin Sorgu Önyükleme Sonuçları* varlığı için bir görünüm sağlar. *Stok özet* varlığından farklı olarak, *Eldeki Dizin Sorgu Önyükleme Sonuçları* varlığı, ürünler için seçili boyutlarla birlikte bir eldeki stok listesi sağlar. Stok Görünürlüğü, önceden yüklenmiş özet verileri her 15 dakikada bir eşitler.

WMS maddeleriyle Stok Görünürlüğünü kullanıyorsanız ve WMS maddeleri için eldeki stok listesini görüntülemek istiyorsanız *Stok Görünürlüğü Özetini Önceden Yükle* özelliğini etkinleştirmenizi öneririz (Ayrıca bkz. [Kolaylaştırılmış eldeki stok sorgusunu önceden yükleme](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Dataverse'de karşılık gelen bir veri varlığı sorgu önyükleme sonucunu depolar ve bu 15 dakikada bir güncelleştirilir. Veri varlığının adı `Onhand Index Query Preload Result` olur.

> [!IMPORTANT]
> Dataverse varlığı salt okunurdur. Stok Görünürlüğü varlıklarındaki verileri görüntüleyebilir ve dışa aktarabilirsiniz ancak **değiştiremezsiniz**.

Supply Chain Management veri kaynağında (`fno`) depolanan, WMS madde miktarlarındaki değişikliklere izin verilmez. Bu davranış, Stok Görünürlüğünün diğer özelliklerinin davranışıyla eşleştirilir. Bu kısıtlama, çakışmaların engellenmesine yardımcı olmak için uygulanır.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>Stok Görünürlüğündeki diğer işlevler için WMS madde uyumluluğu

WMS maddeleri için [geçici rezervasyonlar](inventory-visibility-reservations.md) ve [stok tahsisatı](inventory-visibility-allocation.md) desteklenir. WMS ile ilgili fiziksel ölçüleri, geçici rezervasyon ve tahsisat hesaplamalarına dahil edebilirsiniz.

## <a name="calculate-available-to-promise-quantities"></a>Taahhüde kullanılabilir miktarları hesapla

Çözüm, WMS maddeleri için [taahhüde kullanılabilir (ATP)](inventory-visibility-available-to-promise.md) destekler. ATP hesaplamalarını, WMS'ye özgü ayrıntıları endişelenmeden tanımlayabilirsiniz.
