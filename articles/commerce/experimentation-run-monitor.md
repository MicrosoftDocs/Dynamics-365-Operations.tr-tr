---
title: Deneme çalıştırma ve izleme
description: Bu konuda, üçüncü taraf bir hizmette deneme çalıştırma ve izlemenin nasıl yapılacağı anlatılmaktadır. Ayrıca deneme başlatıldıktan sonra varyasyonlarda nasıl değişiklik yapılacağı da açıklanmaktadır.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 1af5676511c16d0492a7c3a61b7bf3a88b43758a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349268"
---
# <a name="run-and-monitor-an-experiment"></a>Deneme çalıştırma ve izleme

Bu konu, üçüncü taraf bir uygulamada denemelerinizin nasıl çalıştırılacağını ve izleneceğini ve gerekirse varyasyonların nasıl değiştirileceğini açıklar. Bu konudaki adımları tamamlamadan önce denemenizi Commerce'ta [yayımlamanız](experimentation-preview-publish.md) gerekir. 

Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir. Ek adımlar ayrı konularda ele alınmıştır.

[ ![Deneme kullanıcı yolculuğu - Çalıştırma ve İzleme.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Varyasyonlarınızı yayımladıktan sonra, Commerce'ta denemenizi çalıştırmak için yapmanız gereken tüm adımlar tamamlanır. Sonraki adım, bir sayfa istediklerinde her kullanıcıya hangi varyasyonun gösterileceğini belirlemektir. Üçüncü taraf hizmeti bu belirlemeyi yapar ancak önce hizmet içinde denemeyi etkinleştirmeniz gerekir. Deneme etkinleştirme adımları hizmetler arasında farklılık gösterdiğinden, hizmetiniz veya sağlayıcınızla birlikte gelen yönergeleri izlemeniz gerekir. Deneme etkinleştirilmemişse, kullanıcılar yalnızca sayfanın varsayılan sürümünü görürler - hiçbir varyasyon görüntülenmez.

İstatistiksel olarak geçerli sonuçlar için veri toplamak amacıyla denemeyi uzun süre çalışır durumda tutmanız gerekir. Deneme çalışırken, denemeyle ilgili verileri ve analizleri izlemek için üçüncü taraf hizmetini kullanın.

## <a name="adjust-your-variations"></a>Varyasyonlarınızı ayarlama
Herhangi bir nedenle varyasyonlarınızı değiştirmeniz gerekirse, aşağıdaki adımları izleyin.

> [!IMPORTANT]
> Commerce veya üçüncü taraf hizmetindeki canlı bir denemede değişiklik yaparsanız, sonuçlarınız önemli ölçüde etkilenebilir. Denemenin çalışmaya devam etmesine izin verin ve sonra büyük değişiklikler için yeni bir deneme oluşturmayı deneyin.

1. Commerce site oluşturucuda, sol gezinti bölmesinde **Denemeler**'i seçin ve ardından denemeyi seçin. 
1. Açılan menüden güncelleştirmek istediğiniz varyasyonu seçin.
1. Gerekli değişiklikleri yapın ve ardından varyasyonları önizleyin ve yayımlayın. Daha fazla bilgi için, bkz. [Denemeyi önizleme ve yayımlama](experimentation-preview-publish.md).
1. Bir denemenin kurulumuyla ilgili değişiklikler yapmak için üçüncü taraf hizmetine gidin.
    
## <a name="previous-step"></a>Önceki adım
[Deneme önizleme ve yayımlama](experimentation-preview-publish.md)

## <a name="next-step"></a>Sonraki adım
[Varyasyon yükseltme ve denemeyi tamamlama](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]