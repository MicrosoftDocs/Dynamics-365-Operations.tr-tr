---
title: Sonsuz kapasiteyle planlama
description: Bu makalede sonsuz kapasite planlama hakkında bilgi verilmektedir. Geçerli özellik sınırlamaları da açıklanmaktadır.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740018"
---
# <a name="scheduling-with-infinite-capacity"></a>Sonsuz kapasiteyle zamanlama

[!include [banner](../../includes/banner.md)]

*Planlamayı En İyi Duruma Getirme için sonsuz kapasite planlama* özelliği rota bilgilerine dayalı planlama olanağı sunar. İşleri, çeşitli rota kurulumları aralığını temel alarak planlamanızı sağlar. Planlama, rota operasyon sırası veya rota operasyon kaynaklarıyla ilgili gereksinimler dahil olmak üzere sık kullanılan rota ayarlarını kapsar.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Sonsuz kapasite planlama özelliğini açma veya kapatma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla özellik varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Planlamayı En İyi Duruma Getirme için sonsuz kapasite planlaması* özelliğini bularak bu işlevi açabilir veya kapatabilir.

Bu özellik hakkında daha fazla bilgi için bkz. [Yeteneğe dayalı kaynak seçimi ile zamanlama](capability-based-scheduling.md).

## <a name="added-functionality"></a>Eklenen işlev

*Planlamayı En İyi Duruma Getirme için sonsuz kapasite planlama* özelliği rota bilgilerine dayalı iş planlama olanağı sunar. Bu nedenle, üretim süreçlerini planlamak için bir rota kurulumu kullanılabilir. Bu özellik, kullanımdan kaldırılan master planlama altyapısında olmayan bazı sınırlamalar içerse de, üretim senaryoları için gerekli olan en yaygın işlevleri destekler.

Özellik, hem *basit rotaları* hem de *rota ağlarını* dikkate alır. Rota operasyonlarında **Sonraki** alanını kullanarak, birden fazla başlangıç noktası ve paralel çalışacak birden fazla operasyon içeren karmaşık rotalar ayarlayabilirsiniz. Sistem, planlama sırasında bu tip karmaşık rota yapılarını dikkate alır.

Ek olarak, özellik rotalardaki *paralel operasyonları* destekler. Rota operasyonlarında **Öncelik** alanındaki *Birincil* ve *İkincil* seçeneklerini kullanarak, bir rota operasyonunu birincil operasyon olduğu ve başka bir operasyonun ikincil olduğu bir rota yapısı tanımlayabilirsiniz. Bu durumda sistem, planlama sırasında rota yapısını dikkate alır.

Planlama süresi sırasında sistem bir operasyon için belirtilen *kaynak gereksinimlerini* de dikkate alır. Sistem, operasyonu gerçekleştirmek için hangi kaynakların gerekli olduğunu belirlemek amacıyla kaynak gereksinimlerini kullanır. Şu anda, *Planlamayı En İyi Duruma Getirme için sonsuz kaynak planlama* özelliği aşağıdaki kaynak gereksinimleri türlerini destekler:

- Kaynak türü
- Kaynak
- Kaynak grubu
- Yetenek (Daha fazla bilgi için bkz. [Yeteneğe dayalı kaynak seçimi ile zamanlama](capability-based-scheduling.md).)

> [!NOTE]
>
> - Kaynak ve/veya kaynak grubu sonsuz kapasiteye ayarlanmışsa, master planlama bunları sonsuz kapasite olarak kabul eder.
> - Yetenekler veya sertifika gereksinimleri gibi insan kaynaklarıyla ilgili gereksinimler henüz desteklenmemektedir.

Özellik ayrıca **Ayar zamanı** ve **Çalışma zamanı** operasyon özelliklerini de destekler. Bir rota operasyonunda bu özellikleri ayarladığınızda, planlama süreci uygun kurulum ve süreç işleri oluşturacaktır.

Özetle, planlama en sık kullanılan senaryoları destekler. Rotayı oluşturabilir, birincil ve ikincil operasyonlar ekleyebilir, sonraki operasyonları tanımlayabilir, kaynak gereksinimlerini ekleyebilir ve kurulum zamanı ve çalışma zamanı ekleyebilirsiniz. Sistem, planlama sırasında bu bilgileri dikkate alacaktır.

## <a name="limitations"></a>Sınırlamalar

*Planlama Optimizasyonu için sonsuz kapasite planlama* özelliğini kullandığınızda aşağıdaki sınırlamalar geçerlidir:

- Özellik yalnızca sonsuz kapasiteyi destekler.
- Özellik, kaynak yük işlevini desteklemez.
- Özellik rota hurdasını dikkate almaz.
- Özellik, *Süre*'yi yalnızca birincil kaynak seçimi olarak destekler.
