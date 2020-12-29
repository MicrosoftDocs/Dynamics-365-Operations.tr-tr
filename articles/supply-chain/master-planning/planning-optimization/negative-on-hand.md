---
title: Eldeki eksi miktarları planlama
description: Bu konu, planlama en iyileştirmesi kullanılırken eldeki eksi stokun nasıl işlendiğini açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439269"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Eldeki eksi miktarları planlama

[!include [banner](../../includes/banner.md)]

Sistem negatif toplu eldeki miktarı gösteriyorsa, planlama altyapısı miktardan fazla tedarik oluşmasını önlemeye yardımcı olmak için miktarı 0 (sıfır) olarak değerlendirir. Bu işlevsellik şu şekilde çalışır:

1. Planlama en iyileştirme özelliği, eldeki miktarları en düşük kapsam boyutları düzeyinde toplar. (Örneğin, *yerleşim* bir karşılama boyutu değilse, planlama en iyileştirme *ambar* düzeyinde eldeki miktarları toplar.)
1. En düşük karşılama boyutlarının eldeki toplam miktarı negatifse, sistem eldeki miktarın gerçekten 0 (sıfır) olduğunu varsayar.

> [!IMPORTANT]
> Planlama sistemi yalnızca giriş verileri kadar kesin olabilir. Giriş verileri doğru değilse, eksi eldeki kayıtlar, Microsoft Dynamics 365 Supply Chain Management'ın stok bilgilerinin gerçek dünya ile eşitlenmemiş olduğunu gösterir. Bu nedenle, planlama sonucu düzden olacaktır. Doğru planlama sonucu elde etmek için, eksi eldeki bir miktarı gösteren kayıt sayısını en aza indirmelisiniz.

## <a name="example-1"></a>Örnek 1

Ambar 13, aşağıdaki şekilde yapılandırılır:

- **Kapsam kodu:** Min./Maks.
- **Minimum:** 15 parça (adet)
- **En fazla** : 25 adet.

Kapsam boyutlarının en düşük düzeyi *ambar*, aşağıdaki eldeki miktarlar *yerleşim* düzeyinde kaydedilir:

- **Site 1, ambar 13, konum 1:** 20 adet.
- **Site 1 ambar 13, konum 2:** &minus;8 adet.

Bu nedenle, ambar 13'ün eldeki toplama miktarı 12 adet olarak kullanılır. (= 20 adet &minus; 8 adet.).

Bu durumda, planlama alt yapısı 12 adette toplam eldeki miktarı kullanır. ambar 13 için.

Sonuç 13 adete ait planlı bir sipariş. (= 25 adet &minus; 12 adet) 13 numaralı ambarı 12 adetten 25 adede kadar doldurmak için.

## <a name="example-2"></a>Örnek 2

Ambar 13, aşağıdaki şekilde yapılandırılır:

- **Kapsam kodu:** Min./Maks.
- **En düşük:** 15 adet
- **En fazla** : 25 adet.

Kapsam boyutlarının en düşük düzeyi *ambar*, aşağıdaki eldeki miktarlar *yerleşim* düzeyinde kaydedilir:

- **Site 1, ambar 13, konum 1:** 4 adet.
- **Site 1 ambar 13, konum 2:** &minus;8 adet.

Bu nedenle, ambar 13'ün eldeki toplama miktarı &minus;4 adet olarak kullanılır. (= 4 adet &minus; 8 adet.). Diğer bir deyişle, 0'dan (sıfır) azdır.

Bu durumda, planlama alt yapısı, 13 ambar için eldeki miktarın 0 PC olduğunu varsayar. &minus;4 adet yerine.

Sonuç 25 adete ait planlı bir sipariş. (= 25 adet &minus; 0 adet) 13 numaralı ambarı 0 adetten 25 adede kadar doldurmak için.

## <a name="related-resources"></a>İlgili kaynaklar

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama](get-started.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Planlama işini iptal etme](cancel-planning-job.md)
