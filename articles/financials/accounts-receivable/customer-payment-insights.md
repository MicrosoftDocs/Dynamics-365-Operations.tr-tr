---
title: Müşteri ödeme bilgileri (önizleme)
description: Bu konuda, Müşteri ödeme bilgilerinin, bir faturanın ne zaman ödeneceğini öngörmeye ve kuruluşlara zamanında ödeme yapma olasılığını artıran optimizasyon stratejileri oluşturmada nasıl yardımcı olabileceği açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "344674"
---
# <a name="customer-payment-insights-preview"></a>Müşteri ödeme bilgileri (önizleme)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Bu özellik, hedeflenen sürümün bir parçasıdır ve yalnızca Özel Önizleme'ye katılmayı seçen kullanıcılar tarafından kullanılabilir. Bu özellik, gelecekteki bir genel kullanım sürümüne eklenecektir.

# <a name="overview"></a>Genel bakış

Kuruluşlar genellikle bir müşterinin faturalarını ne zaman ödeyeceğini öngörmede zorluk yaşar. Bu bilgi eksikliği, yanlış nakit akışı tahminlerine, verimsiz tahsilat işlemlerine ve siparişlerin kredi riski yaratabilecek müşterilere gönderilmesine neden olabilir. Müşteri ödeme bilgileri (önizleme), bir faturanın ne zaman ödeneceğini öngörmek için makine öğrenimini kullanır. Ayrıca müşterilerin zamanında ödeme yapma olasılığını en üst düzeye çıkarmak için uyarlanabilecek optimizasyon stratejileri de sunar.

## <a name="predictions"></a>Öngörüler

Ödeme öngörüleri, aşağıdakilere yardımcı olarak kuruluşların iş süreçlerini iyileştirmelerine olanak tanır:

-   Geç ödeneceği öngörülen faturaları kolayca belirleyin.
-   Zamanında ödeme alma olasılığını artırmak için uygun önlemler alın.

Müşteri ödeme bilgileri (önizleme), bir faturanın ne zaman ödeneceğini öngörmek için makine öğrenimini kullanır. Bir faturanın ne zaman ödeneceğini öngörmek için kullanılan makine öğrenimi modelini oluşturmak için geçmiş fatura, ödeme ve müşteri verilerini kullanır.

Her açık fatura için Müşteri ödeme bilgileri (önizleme) üç ödeme olasılığı öngörür:

-  Ödemenin zamanında yapılma olasılığı (fatura vade tarihi içinde).
-  Ödemenin fatura vade tarihinden itibaren 30 gün içinde yapılma olasılığı.
-  Ödemenin fatura vade tarihinden sonraki 30 günden daha geç yapılma olasılığı.

Ödeme olasılığı öngörü bölümünde görüntülenebilir.

[![Ödeme öngörüleri](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Her faturaya, yukarıda tanımlanan üç öngörülen ödeme olasılığı senaryosundan biri kullanılarak ödemeyi kazanma olasılığı da atanır. En yüksek ödeme olasılığına sahip senaryo, kazanan senaryodur.


Örneğin, bir faturada öngörünün, faturanın zamanında ödenmesi olasılığını yüzde 71, faturanın vade tarihinden itibaren 30 gün içinde ödenmesi olasılığını yüzde 13 ve faturanın vade tarihinden sonraki 30 günden daha geç ödenme olasılığını yüzde 16 olarak gösterdiğini varsayalım. En yüksek olasılık, faturanın zamanında ödeneceği senaryoda gösterilir bu nedenle fatura, zamanında ödenme olasılığıyla etiketlenir.

[![Ödeme öngörüleri](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimizasyon stratejileri

Müşteri Ödeme Bilgileri (önizleme), ödeme öngörülerine ek olarak zamanında ödeme alma şansını artırmak için optimizasyon stratejileri kullanabilir. Bu şekilde kuruluşlar, kullanıcıların fatura ve müşteri parametrelerini ayarlamasına ve ardından faturaların zamanında ödenme olasılığına karşılık gelen etkiyi karşılaştırmasına izin vererek "Ya ise" analizi yapabilir.

Örneğin, bir kuruluş ödemeyi zamanında alma olasılığına faturalardaki nakit iskontosu güncelleştirmesinin etkisini değerlendirmek isteyebilir. Faturalar yeni iskontoyu kullanmak üzere optimize edildiğinde, kullanıcılar bu faturalar için zamanında ödeme alma olasılığına yapılan iskontonun etkisini inceleyebilir. İskontoyu uygulamanın maliyeti, ödemenin zamanında tahsil edilmesiyle karşılaştırıldığında daha düşükse kuruluş seçilen iskontoyu gelecekteki tüm açık siparişlere uygulamayı tercih edebilir.

> [!NOTE] 
> Şu anda Müşteri ödeme bilgileri (önizleme) için optimizasyon stratejisi olarak yalnızca iskonto kullanılabilir.

[![Optimize edilmiş öngörüler](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Müşteri ödeme bilgilerini (önizleme) edinme

Müşteri ödeme bilgilerini (önizleme) denemekle ilgileniyorsanız lütfen [Mali Bilgiler Önizleme ekibine](mailto:fiap@microsoft.com) e-posta gönderin. 

## <a name="privacy-statement"></a>Gizlilik Bildirimi

Önizlemeler, müşteri verilerini Amerika Birleşik Devletleri’nde saklar. Ayrıca önizlemeler (1), Dynamics 365 for Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri kullanmamalıdır ve (4) sınırlı desteğe sahiptir.
