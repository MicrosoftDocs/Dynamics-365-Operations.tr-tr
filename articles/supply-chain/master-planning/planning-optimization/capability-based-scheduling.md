---
title: Yeteneğe dayalı kaynak seçimi ile zamanlama
description: Bu makalede, bir işlem için kaynak gereksinimleri olarak yetenekler belirterek sonsuz kapasite zamanlaması gerçekleştirilirken kaynak seçimi açıklanmaktadır.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739911"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Yeteneğe dayalı kaynak seçimi ile zamanlama

[!include [banner](../../includes/banner.md)]

Üretim rotası işlemi için kaynak gereksinimlerini belirterek o işlemi gerçekleştirmek için neyin gerekli olduğunu tanımlarsınız. Örneğin, bir işlem belirli bir kaynağı veya kaynak grubunu ya da beceri veya yeteneklerin bir birleşimini gerektirebilir. Bu makalede, bir işlem için kaynak gereksinimleri olarak yetenekler belirterek sonsuz kapasite zamanlaması gerçekleştirilirken kaynak seçimi açıklanmaktadır.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Yetenek tabanlı planlama özelliğini açma veya kapatma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla özellik varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Planlamayı En İyi Duruma Getirme için sonsuz kapasite planlaması* özelliğini bularak bu işlevi açabilir veya kapatabilir.

Bu özellik hakkında daha fazla bilgi için bkz. [Sonsuz kapasiteyle zamanlama](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Yetenek tabanlı zamanlama

Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Tek bir işlem kaynağına birden fazla yetenek atanabilir ve birden fazla kaynağa tek bir yetenek atanabilir. Araçlar, satıcılar, makineler, konumlar, tesisler ve insan kaynakları gibi her türlü kaynağa yetenek atanabilir.

Yetenekleri kaynak gereksinimleri olarak belirlediğinizde siparişler zamanlanana kadar kaynak tahsisatını erteleyebilirsiniz. Rota işlemine belirli kaynaklar veya kaynak grupları atamak yerine her bir rota işlemi için gerekli olan yetenekleri tanımlayabilirsiniz. Ardından zamanlama sırasında sistem, kaynaklar için tanımlanan yeteneklerle gerekli yetenekleri eşleştirir. Sistem yalnızca gereksinimleri karşılayan kaynakları seçer.

İşlem kaynağına yetenek atamak için **Kaynaklar** sayfasının **Yetenekler** hızlı sekmesini kullanın. Yeteneğe kaynak atamak için **Kaynak yetenekleri** sayfasının **Kaynaklar** hızlı sekmesini kullanın. Her iki sayfaya da gezinme bölmesindeki **Üretim denetimi \> Kurulum \> Kaynaklar** altından erişebilirsiniz. Her iki hızlı sekme de seçilen bir kaynak veya yetenekle ilişkili kaynakları listeleyen bir ızgara içerir. Her iki hızlı sekme de ızgaraya satır eklemek, ızgaradan satır kaldırmak ve ızgaradaki satırları düzenlemek için kullanabileceğiniz bir araç çubuğu içerir. Izgara aşağıdaki sütunları içerir:

- **Kaynak** veya **Yetenek**: Satır tarafından atanan kaynağı ya da yeteneği seçin.
- **Açıklama**: Kaynağın veya yeteneğin kısa bir açıklamasını girin.
- **Yürürlük Tarihi**: Kaynak veya yetenek atamasının geçerli olduğu ilk tarihi belirtin. Zamanlama sırasında sistem, süresi dolmuş bir yetenek atamasına sahip bir kaynağı veya yeteneği, bu kaynak gereksinimleri karşılasa bile kullanmaz.
- **Bitiş Tarihi**: Kaynak veya yetenek atamasının geçerli olduğu son tarihi belirtin. Zamanlama sırasında sistem, süresi dolmuş bir yetenek atamasına sahip bir kaynağı veya yeteneği, bu kaynak gereksinimleri karşılasa bile kullanmaz.
- **Düzey**: Kaynağın yetenek için sahip olması gereken yeterlilik düzeyini belirtin. Ardından, kaynak veya yetenek gereksinimi için bir **İhtiyaç duyulan minimum düzey** değerini belirtirseniz zamanlama altyapısı kaynak seçimi sırasında yeterlilik düzeyini dikkate alır. Sistem, yalnızca kaynak gereksiniminde belirtilen en düşük düzeye eşit veya bu düzeyi aşan bir düzeyde gerekli yeteneğe sahip kaynakları seçer.
- **Öncelik**: Bu alan henüz Planlama Optimizasyonu tarafından desteklenmemektedir. Ancak kullanımdan kaldırılan master planlama altyapısını kullanıyorsanız kaynak önceliğini tanımlamak için kaynak veya yetenek atamasındaki **Öncelik** alanını kullanabilirsiniz. **Zamanlama parametreleri** sayfasındaki **Birincil kaynak seçimi** alanında *Öncelik* seçilirse zamanlama sırasında sistem, önce en yüksek önceliğe (**Öncelik** alanındaki en düşük sayısal değer) sahip olan kaynağı seçer.

## <a name="example"></a>Örnek

Bu örnek, zamanlama altyapısının kaynakları yeteneğe göre nasıl seçtiğini gösterir.

Üretim rotasında beş işlem var: *10*, *20*, *30*, *40* ve *50*. Her rota işlemi, farklı yeteneklere sahip bir kaynak gerektiriyor. Örneğin, rota işlemi *10*, hoparlör monte etme (*0050 Hprlr Montajı*) ve ahşap işleme (*1010 Ahşap yetenekleri*) yeteneğine sahip bir kaynak gerektiriyor. Rota işlemi *50*, ürün paketleme yeteneğine (*0070 Paketleme yeteneği*) sahip bir kaynak gerektiriyor.

![Zamanlama için kullanılan yetenek.](media/capability-based-scheduling.png "Zamanlama için kullanılan yetenek.")

Altyapı, zamanlama sırasında işlem gereksinimlerini karşılayan kaynakları arar. Örneğin, zamanlama altyapısı *10* işlemini gerçekleştirmek için *00101* kaynağını seçer, çünkü bu kaynak gerekli her iki özelliğe de sahip olan kaynaklar arasında bulunan ilk kaynaktır. Zamanlama altyapısı *50* işlemini gerçekleştirmek için *00301* kaynağını seçer, çünkü bu kaynak paketleme yeteneğine sahip tek kaynaktır.

Ardından, yeterlilik seviyeleri kullanımının bu örneğin nasıl etkileyeceğini inceleyelim:

- *10* işlemi, *0059 Montaj* yeteneği için en düşük *7* düzeyinde yeterlilik gerektirir.
- *00101* kaynağının *0059 Montaj* yeteneği için yeterlilik düzeyi *5*'tir.
- *00102* kaynağının *0059 Montaj* yeteneği için yeterlilik düzeyi *10*'dur.

Bu durumda, sonsuz kapasite zamanlaması sırasında zamanlama altyapısı *10* işlemini gerçekleştirmek üzere *00102* kaynağını seçer, çünkü bu kaynak *00101* kaynağından farklı olarak yetenek için gerekli yeterlilik seviyesine sahiptir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
