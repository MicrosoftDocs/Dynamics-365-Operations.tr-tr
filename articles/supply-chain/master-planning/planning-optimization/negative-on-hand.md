---
title: Eldeki eksi miktarları planlama
description: Bu konu, planlama en iyileştirmesi kullanılırken eldeki eksi stokun nasıl işlendiğini açıklar.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: bb837a38485bad2b9b76a5e4f20d311c0281e192
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625407"
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

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Eldeki negatif stoğa karşı bir ayırma olduğunda planlama

Fiziksel ayırmalar varken stoğu ayarlarsanız bir siparişin negatif stoğa karşı fiziksel olarak ayrıldığı bir duruma neden olabilirsiniz. Bu durumda, fiziksel bir rezervasyon bulunduğundan, ayrılmış miktarı karşılamak için kaynağınızın olması gerekir. Bu nedenle, ikmal gereklidir, bu nedenle sistem ya mevcut eldeki envanter tarafından karşılanamayan miktarı doldurmak için planlı bir sipariş oluşturur ya da kalem için mevcut bir siparişle kapatır.

Aşağıdaki örnek bu senaryoyu göstermektedir.

### <a name="example"></a>Örnek

Sistem aşağıdaki şekilde yapılandırılmıştır:

- *FG* ürünü mevcuttur ve eldeki stok miktarı *10* adettir.
- Ürün yapılandırması, fiziksel negatif stoğa izin verir.
- *10* adet *FG* ürünü için bir satış siparişi var.
- Satış siparişi miktarı, mevcut eldeki stoğa karşı fiziksel olarak ayrılmıştır.

Ardından, eldeki envanter 5 olacak şekilde *FG* ürününün miktarını ayarlarsınız. Eldeki ürün stoğu 5 olduğundan, satış siparişi miktarı artık eldeki mevcut olmayan miktara karşı ayrılmıştır (eldeki 0 olsaydı benzer olurdu, bu durumda satış siparişi negatif stoka karşı ayrılırdı). Master planlamayı şimdi çalıştırırsanız, *FG* için 5 miktarında bir planlı sipariş oluşturularak satış siparişi tedariki sağlanır çünkü Planlama Optimizasyonu her zaman fiziksel rezervasyon tedariki için mevcut kaynakları kullanır veya yeni bir planlı sipariş oluşturur.

## <a name="related-resources"></a>İlgili kaynaklar

- [Planlama Optimizasyonuna genel bakış](planning-optimization-overview.md)
- [Planlama Optimizasyonunu kullanmaya başlama](get-started.md)
- [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)
- [Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)
- [Planlama işini iptal etme](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
