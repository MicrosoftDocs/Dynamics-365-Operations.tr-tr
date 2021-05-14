---
title: Vergi hesaplaması performansı, hareketleri etkiliyor
description: Bu konu, vergi hesaplama performansı ve bu performansın hareketler üzerindeki etkisiyle ilgili sorun giderme bilgiler sağlar.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947725"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Vergi hesaplaması performansı, hareketleri etkiliyor

[!include [banner](../includes/banner.md)]

Bazen bir hareket, vergi hesaplamasında bulunan performans sorunlarından etkilenir. Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.

## <a name="review-the-transaction-line-count"></a>Hareket satır sayısını gözden geçirin

Hareketin çok sayıda satırı olup olmadığını (örneğin, birkaç yüz) belirleyin. Çok sayıda satır yoksa bir sonraki bölüme geçin. Harekette birkaç yüz satır varsa, vergi hesaplamasını erteleyin. Daha fazla bilgi için bkz. [Defterlerde ertelenmiş vergi hesaplamayı etkinleştirme](enable-delayed-tax-calculation.md). 

Ardından, aşağıdaki koşullardan herhangi birinin yerine getirilip getirilmediğini belirleyebilirsiniz:

- Büyük dosyalardan içe aktarma hareketleri var.
- Aynı anda birden çok oturum, aynı hareket vergisi hesaplamasını işliyor.
- Hareketin birden çok satırı var ve görünümler gerçek zamanlı olarak güncelleştiriliyor. Örneğin, bir satırın alanları değiştirildiğinde, **Genel günlük** sayfasındaki **Hesaplanan satış vergisi tutarı** alanı gerçek zamanlı olarak güncelleştirilir.

   [![Günlük fişi sayfasındaki hesaplanan satış vergisi tutarı alanı](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Bu durumlardan herhangi biri geçerliyse vergi hesaplamasını erteleyin.

## <a name="review-the-call-stack"></a>Çağrı yığınını gözden geçirin

Vergi hesaplamasının birden çok kez çağrılıp çağrılmadığını belirlemek için çağrı yığınını gözden geçirin. Çok defa çağrılmadıysa bir sonraki bölüme geçin. Çağrı yığını çok defa çağrılmışsa vergi hesaplama zamanlarının azaltılmasına yardımcı olacak aşağıdaki adımları izleyin.

1. Defter, hareketi ele aldıysa vergi hesaplamayı erteleyin. Daha fazla bilgi için bkz. [Defterlerde ertelenmiş vergi hesaplamayı etkinleştirme](enable-delayed-tax-calculation.md).
2. Hareket bir satınalma siparişi ise ve uygulama sürümü 10.0.15'den daha yeni ise, **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** için denemeyi etkinleştirerek, vergi hesaplamasını son hesaplamaya kadar erteleyebilirsiniz.

## <a name="review-the-call-stack-timeline"></a>Çağrı yığını zaman çizelgesini gözden geçirin

Aşağıdaki sorunların mevcut olup olmadığını belirlemek için çağrı yığını zaman çizelgesini gözden geçirin. Bunlar mevcutsa sorunu gidermek için **TaxUncommittedDoIsolateScopeFlighting** için denemeyi etkinleştirin.

- Hareket, sistemin oturum sona erene kadar yanıt vermemesine neden olur. Bu nedenle, hareket vergi sonucunu hesaplayamıyor. Aşağıdaki görselde, aldığınız "Oturum sona erdi" ileti kutusu gösterilmektedir.

    [![Oturum bitti iletisi](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- **TaxUncommitted** yöntemleri, diğer yöntemlerden daha fazla zaman alabilir. Örneğin, aşağıdaki görselde **TaxUncommitted::updateTaxUncommitted()** yöntemi 43,347.42 saniye sürer ancak diğer yöntemler 0,09 saniye sürer.

    [![Yöntem süreleri](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Vergi hesaplamasını özelleştirme ve çağırma

Özelleştirdiğinizde, her satır için **insert()** veya **update()** yönteminde vergi hesaplamasını çağırmayın. Vergi hesaplaması, hareket düzeyinde çağrılmalıdır.

## <a name="determine-whether-customization-exists"></a>Özelleştirme olup olmadığını belirleyin

Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin. Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
