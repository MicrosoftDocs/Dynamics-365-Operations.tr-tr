---
title: "Planlanan maliyetler için bir maliyetlendirme sürümü kullanarak maliyet değişikliklerinin benzetimini yapın"
description: "Bu makalede, mamul bir maddenin hesaplanan maliyetlerindeki maliyet değişikliklerinin etkisinin benzetimini, planlanan maliyetler için ayrı bir maliyetlendirme sürümüyle nasıl yapabileceğiniz açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 07dc838b38b060d45930a24b13be3dc283457282
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Planlanan maliyetler için bir maliyetlendirme sürümü kullanarak maliyet değişikliklerinin benzetimini yapın

[!include[banner](../includes/banner.md)]


Bu makalede, mamul bir maddenin hesaplanan maliyetlerindeki maliyet değişikliklerinin etkisinin benzetimini, planlanan maliyetler için ayrı bir maliyetlendirme sürümüyle nasıl yapabileceğiniz açıklanmaktadır.

Mamul bir maddenin hesaplanan maliyetlerindeki maliyet değişikliklerinin etkisinin benzetimini, planlanan maliyetler için ayrı bir maliyetlendirme sürümüyle yapabilirsiniz. Artımlı maliyet değişikliklerini yansıtan bekleyen maliyet kayıtlarını girmek ve üretilmiş maddelerdeki maliyet etkisini hesaplamak için bu ayrı maliyetlendirme sürümünü kullanın. Ürün reçetesi hesaplamalarında Etkin maliyetlerin geri dönüş ilkesi kullanılacağı için, yalnızca artımlı maliyet değişiklikleri girilmelidir.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Benzetim maliyetlendirme sürümünü tanımlama yönergeleri
Benzetim için maliyetlendirme sürümünü tanımlarken aşağıdaki yönergeleri kullanın:

-   **Planlanan maliyetler** için bir maliyetlendirme türü atayın.
-   Maliyetlendirme sürümü için, **Benzetim** gibi anlamlı bir tanımlayıcı atayın.
-   İçeriğin maliyet kayıtlarını içerdiğinden emin olun.
-   Maliyet kaydı girişine izin verin. Bekleyen maliyetlerin girilmesini engellemeyin.
-   Tüm tesisler için maliyet kaydı girişine izin verin. Tesis belirtirseniz, söz konusu tesise yapılan maliyet kaydı girişi sayısını sınırlarsınız.
-   Beklemedeki maliyetlerin etkinleştirilmesini önleyin. Benzetim maliyetlendirme sürümündeki maliyet kayıtları için yalnızca bekleyen maliyetlerin girilmesi gerekir.
-   Bir "başlangıç" tarihi girmeyin. Benzetim maliyetlendirme versiyonunu kullanan her ürün reçetesi hesaplaması için bir hesap tarihi girilir.
-   **Geçerli etkin** için bir geri dönüş ilkesi belirtin. Geri dönüş ilkesi, geçerli etkin maliyetleri diğer tüm maliyet kayıtları için kaynak olarak kullanırken, benzetim amaçlı olarak artımlı maliyet değişikliklerinin girilmesine olanak tanır. Tüm geçerli etkin maliyetlerin diğer tüm maliyet kayıtları için varolduğunu varsayıyoruz.
-   **Sürüm maliyet fiyatı** için bir maliyet fiyatı modeli belirtin ancak hesaplamaları kısıtlamayın. Örneğin, benzetimler satın alınan maddeler için maliyet katkı verilerinin kaynağını göstermek üzere bir **Ürün reçetesi hesaplama grubu** maliyet fiyatı modelini de kullanabilir.
-   **Çok düzeyli** bir açılım modu belirtin ancak hesaplamaları kısıtlamayın. Benzetimler başka açılım modları kullanabilir.

## <a name="costing-versions"></a>Maliyet sürümleri
Aşağıdaki senaryolarda, maliyet değişiklikleri etkisinin benzetimini uygulamak amacıyla benzetim maliyetlendirme sürümünün nasıl kullanıldığı gösterilmektedir. Benzetimi yapılmış bir maliyet değişikliğini girmeden önce, temiz bir başlangıç noktası elde edebilmeniz için benzetim maliyetlendirme sürümündeki bekleyen maliyet kayıtlarını silin. Madde fiyatları ve maliyet kategori fiyatlarıyla ilişkili bekleyen maliyet kayıtlarını görüntülemek ve silmek için **Madde fiyatı** sayfasını kullanın.

-   Satın alınan bir maddedeki maliyet değişikliğinin benzetimini uygulayın. Örneğin, maliyet değişikliği kritik satın alınan malzemelerin maliyetinde beklenen bir artış veya azalışı yansıtabilir. Satın alınan bir madde için farklı maliyet tanımlamak amacıyla, benzetim maliyetlendirme sürümü içerisinde bekleyen maliyet kaydını girmek için **Madde fiyatı** sayfasını kullanın.
-   Bir maliyet kategorisindeki maliyet değişikliğinin benzetimini yapın. Örneğin, maliyet değişikliği, operasyon kaynakları için işçilik ücretlerinde veya saatlik ücretlerde beklenen bir artışı veya düşüşü yansıtabilir. Bir maliyet kategorisi için farklı maliyet tanımlamak isterseniz, benzetim maliyetlendirme sürümü içerisinde bekleyen bir maliyet kaydını girmek için **Maliyet kategorisi fiyatı** sayfasını kullanın.
-   Maliyet değişikliğinin benzetimini bir dolaylı maliyet hesap formülünde uygulayın. Örneğin, maliyet değişikliği üretim genel giderlerinde beklenen bir artış veya azalışı yansıtabilir. Dolaylı maliyet hesap formülünde değişikliği tanımlamak amacıyla, benzetim maliyetlendirme sürümünün benzetiminde bekleyen bir maliyet kaydı girmek ve değişikliği doğrulayıp kaydetmek için **Maliyetlendirme tablosu kurulumu** sayfasını kullanın.

Benzetimi yapılmış maliyet değişikliklerini girdikten sonra, maliyet değişikliklerinden etkilenen mamul maddelerin maliyetlerini hesaplayın. Benzetim maliyetlendirme sürümü için **Hesaplama** sayfasını kullanın ve maliyet değişikliklerinden etkilenecek seçili mamul maddeleri belirtin. Ürün reçetesi hesaplamaları, belirli maddeleri seçmediğiniz sürece tüm mamul maddelere uygulanır. Alternatif olarak, ürün reçetesi hesaplama seçeneğini kullanım yeri güncelleştirmeleri için kullanabilirsiniz. Benzetimi yapılan maliyet değişikliklerinin seçili mamul maddelerin maliyetlerini nasıl etkilediğini analiz etmek için benzetim maliyetlendirme sürümü içerisindeki madde maliyet kayıtlarını görüntüleyin. Maliyetleri görüntüleyip analiz etmek için **Madde fiyatı** sayfasını ve **Madde maliyetini hesapla** sayfasını kullanın.




