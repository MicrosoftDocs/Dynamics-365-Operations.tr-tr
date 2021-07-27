---
title: Nakit akışı tahmini (önizleme)
description: Bu konuda, Nakit akışı tahmini özelliği açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3f16c8471123969443af52ff9bed7fc017b8e9c2
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339227"
---
# <a name="cash-flow-forecast-preview"></a>Nakit akışı tahmini (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nakit akışı her işletme için kritik öneme sahiptir. Hatta kar elde eden şirketler bile, acil gereksinimlerini karşılamak için nakit akışını korumazsa borçlarını ödeyemeyebilir. Mali içgörülerdeki nakit akışı tahmini özelliği, şirketlerin nakit bakiyelerini etkili şekilde izlemesine ve yönetmelerine yardımcı olabilir. Bu özellik, işletmelerin nakit akışlarını geçmişe kıyasla daha doğru tahmin edebilmeleri için makine öğrenimini kullanır. Ayrıca yöneticilere, geçerli nakit pozisyonlarındaki fırsatları en iyi duruma getirecek kararlar alma konusunda yardımcı olabilir. 

Birçok şirket için nakit akışını yönetme ve nakit akışı tahminlerini çalıştırma; sıkıcı, yinelenen ve el ile gerçekleştirilen bir işlemdir. Pek çok şirket bunun için farklı karmaşıklık düzeylerine sahip Microsoft Excel çözümlerinden yararlanır. Nakit akışını doğru şekilde tahmin etmeyle ilgili zorluklardan bazıları şunlardır:

- Veriler aşağıdakiler dahil farklı yerlere dağılmış olduğundan karar mekanizmalarına sunulamaz: 
  - Muhasebe veya kurumsal kaynak planlama sistemi
  - Finansal planlama yazılımı
  - Excel
  - Ek yazılım uygulamaları 
- Tahmin, her etki alanı veya departman içinde "silolarda" içinde bulunan şirket içi bilgilere dayanır.
- Mali öğeler gerçekleştirildikten sonra nakit akışı tahminin doğruluğunu ölçmek kesin bir sonuç sunmaz ve zordur.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Nakit akışı tahmini özelliğinin ayrıntıları
Nakit akışı tahminleri özelliği aşağıdaki işlevleri içerir. 

- Harici sistemlerden gelen nakit akışı verilerini Dynamics 365 Finance'e tümleştirmeyi kolaylaştırır. Nakit akışı tahminleri veri içeri-dışarı aktarma çerçevesini de kullanabilir. Bu çerçeve Excel OData ile tümleştirmeyi kolaylaştırır. Ayrıca, kapsamlı bir nakit akışı çözümü oluşturmak için birden fazla kaynaktaki verileri birleştirebilirsiniz. 

- Akıllı bir nakit pozisyonu sağlar. Nakit pozisyonu, şirketin hesaplarına nakit gelmesini bekleyebileceği zamanı tahmin etmek için müşterinin ödeme davranışına göre oluşturulur. Ayrıca, gelecekteki fatura ve siparişlerin ödenebileceği zamanı tahmin etmek için ödeme yapan satıcıların geçmiş modellerini analiz eder. 

- AI Builder ile otomatikleştirilmiş tümleştirme aracılığıyla zaman serisi tahminini kullanarak uzun süreli tahminler için akıllı nakit akışı tahmini sağlar.

- Belirli nakit akışı pozisyonunu veya tahminlerini kaydetme, bunları düzenleme ve daha sonra tahmini gerçek mali değerlerle karşılaştırarak tahmin performansını ölçme özelliği sunar.

- Anlık görüntü karşılaştırmasıyla durum çözümlemeleri sağlar. Örneğin, iyimser, kötümser ve nakit akışının en gerçekçi görünümlerini temsil eden birden çok anlık görüntü oluşturabilir ve farklılıkları karşılaştırabilir ve görüntüleyebilirsiniz.

- Nakit akışı tahminini birden fazla para biriminde ve farklı tüzel kişilikler genelinde görüntüleme ve belirli bir banka hesabıyla ilişkili nakit akışını filtreleme ve görüntüleme özelliği sunar. 

- Mali boyutlarla ilgili banka hesaplarını filtrelemenizi ve görüntülemenizi sağlar.

Dynamics 365 Finance'teki nakit akışı tahmini işlevi; sıkıcı, karmaşık ve yinelenen nakit akışı tahmini işlemini basit ve otomatik bir işleme dönüştürmek için kuruluşunuzu destekler. Nakit akışı tahminlerinin en sıkıcı yönlerini otomatikleştirmek, istenen iş sonuçlarını elde etmek için kritik karar alma süreçlerine odaklanmanızı sağlar.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Nakit akışı tahmini için Boyutları ayarlama
**Nakit akışı tahmin kurulumu** sayfasındaki yeni bir sekme, **Nakit akışı tahmini** çalışma alanında filtre uygulamak için hangi mali boyutları kullanacağınızı kontrol etmenizi sağlar. Bu sekme yalnızca Nakit akışı tahminleri özelliği etkinleştirildiğinde görüntülenir. 

**Boyutlar** sekmesinde, filtre için kullanılacak boyut listesinden seçim yapın ve bunları sağ sütuna taşımak için ok tuşlarını kullanın. Nakit akışı tahmin verilerinin filtrelenmesi için yalnızca iki boyut seçilebilir. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
