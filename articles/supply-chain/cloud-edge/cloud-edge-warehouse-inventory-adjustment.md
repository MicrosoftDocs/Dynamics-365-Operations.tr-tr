---
title: Ambar stoku düzeltmesi
description: Bu konu, Ambar stoğu ayarlama günlüğü ve ölçek birimleri kullanırken işleme hakkında bilgi sağlar.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938238"
---
# <a name="warehouse-inventory-adjustment"></a>Ambar stoku düzeltmesi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ambar stoğu ayarlama özelliği, [üretim iş yükleri](cloud-edge-workload-manufacturing.md) ve [ambar yönetimi iş yükleri](cloud-edge-workload-warehousing.md) için bulut ve kenar ölçek birimleri çalıştırıldığında kullanılır.

Bir çalışan, bir ölçek birimi ambar yönetimi iş yüküne karşı ambar uygulamasını kullanarak stok ayarlaması yaptığında eldeki fiziksel güncelleştirmesi **Ambar stok ayarlaması günlüğü** toplu işlemi tarafından işlenmelidir. Bu özelliği, **Ambar yönetimi > Periyodik görevler > Ambar stoğu ayarlama günlüğü**'ne giderek çalıştırabilirsiniz.

Şu anda aşağıdaki ambar uygulaması iş süreçleri, ölçek birimi iş yükleri üzerinde **Ambar stok ayarlama günlüğü**'nü kullanır:

- Ayarlama giriş/çıkış
- Döngü sayımı
- Plaka yükleme

Merkez ve ölçek birimi dağıtımları stok kayıtlarını paylaştığı için bulut ve uçta stok ayarlama işleminin bir parçası olarak çeşitli stok hareketleri oluşturulur.

## <a name="inventory-adjustment-example"></a>Stok ayarlama örneği

Bu örnekte, ambar çalışanı eldeki stok eklenmesini kaydetmek için ambar uygulamasını kullandı.

İlk olarak, ölçek birimi iş yükü, pozitif fiziksel ayarlama için bir ambar stoğu ayarlama hareketi oluşturur ve bu durum daha sonra merkez ile eşitlenir ve merkezde eldeki stok artışına neden olur.

| Türü                                    | Ölçek birimi | Yön | Hub |
|-----------------------------------------|------------|-----------|-----|
| Ambar stoku düzeltmesi          | +1         | ->        | +1  |

Daha sonra merkez, [ileti işlemcisi iletileri](cloud-edge-message-processor-messages.md) üzerinden alınan bir sayım günlüğü deftere nakil işlemini işler. Bu, ek eldeki stoğu güncelleştirir. Eldeki stoğun çift olmasını engellemek için, merkez bu işlemin bir parçası olarak mahsup hareket oluşturur ve ambar stok ayarlamasıyla ilişkili daha önceden kaydedilen eldeki stoğu kaldırır.

| Türü                                    | Ölçek birimi | Yön | Hub |
|-----------------------------------------|------------|-----------|-----|
| Sayım                                | +1         | <-        | +1  |
| Ambar stok ayarlaması (Mahsup) | -1         | <-        | -1  |

Bir ölçek birimi bir merkez üzerinde **Ambar stoğu ayarlama günlüğü** oluşturduktan sonra, hem **Sayım günlüğü**'nü hem de **Mahsup günlük**'ü inceleyebilirsiniz (bunların ikisi de merkez tarafından düzeltme işleminin bir parçası olarak oluşturulur).

Aşağıdaki adımları gerçekleştirerek, Supply Chain Management'taki bu günlük girişlerini inceleyebilirsiniz:

1. Ölçek biriminde oturum açın.
1. **Ambar yönetimi \> Periyodik görevler \> Ambar stok ayarlaması günlüğü**'ne gidin.
1. **Ambar stoğu düzeltme günlüğü** sayfasında, eldeki stok değişikliğini kaydeden günlüğü bulun ve açın. **Günlük satırları** bölümü, bu günlük tarafından kaydedilen düzeltmeleri gösterir.
1. Merkezde oturum açın.
1. **Ambar yönetimi \> Periyodik görevler \> Ambar stok ayarlaması günlüğü**'ne gidin.
1. Merkez ve ölçek birimi eşitlendiyse **Ambar stoğu ayarlama günlüğü** sayfasında aynı günlüğün listelendiğini görmeniz gerekir.
1. Günlüğü açın. [İleti işlemci iletileri](cloud-edge-message-processor-messages.md) işlendiyse başlıkta **Sayım günlüğü** ve **Mahsup günlük** bağlantılarını görürsünüz.
    - **Sayım günlüğü**, günlük satırlarıyla aynı boyut değerlerini göstermelidir.
    - **Mahsup günlük**, çift stok ayarlamasını kaldıran mahsup değeri göstermelidir.
    > [!NOTE]
    > Tüm eşitleme ve işleme işlemleri tamamlandığında, **Sayım günlüğü** ve **Mahsup günlük** ölçek birimiyle geri eşitlenir. Bunlar ayrıca ilgili **Ambar stok ayarlama günlüğü** sayfasından da görüntülenebilir.
