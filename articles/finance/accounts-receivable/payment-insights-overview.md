---
title: Müşteri ödeme öngörüleri (Önizleme)
description: Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamaya yardımcı olan ödeme içgörüleri özelliği açıklanmıştır. Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanıza gerekçe olabilecek durumları belirlemenize yardımcı olabilir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d01f15223b4665caec16d6a4e51a5121a0ed94ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012176"
---
# <a name="customer-payment-insights-preview"></a>Müşteri ödeme öngörüleri (Önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamaya yardımcı olan ödeme içgörüleri özelliği açıklanmıştır. Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanıza gerekçe olabilecek durumları belirlemenize yardımcı olabilir. 

## <a name="overview"></a>Genel bakış

Müşterilerinin faturalarını ne zaman ödeyeceklerini tahmin etmek zor olabilir. Bu bilgi eksikliği, daha az doğru nakit akışı tahminlerine, çok geç gerçekleşen tahsilat işlemlerine ve ödemelerinde temerrüde düşebilecek müşterilere gönderilen siparişlere yol açar. Müşteri ödeme içgörüleri (Önizleme), müşteri faturasının ne zaman ödeneceğini tahmin etme konusunda kuruluşlara yardımcı olur. Bu bilgiler kuruluşların, zamanında ödeme olasılığını artıran tahsilat stratejileri oluşturmalarına yardımcı olabilir. 

## <a name="predictions"></a>Öngörüler

Ödeme tahminleri, kuruluşların geç ödeme olasılığı olan faturaları kolayca tespit etmelerine ve zamanında ödeme alma şanslarını artıracak uygun önlemleri almalarına yardımcı olarak iş süreçlerini iyileştirmelerini sağlar.

Geçmiş faturalardan, ödemelerden ve müşteri verilerinden yararlanan bir makine öğrenimi modeli kullanan Müşteri ödeme öngörüleri (Önizleme), bir müşterinin ödeme bekleyen bir faturayı ne zaman ödeyeceğini daha doğru tahmin eder.

Her açık fatura için Müşteri ödeme içgörüleri (Önizleme) üç ödeme olasılığı tahmin edebilir:

-   Ödemenin zamanında yapılma olasılığı 
-   Ödemenin geç yapılma olasılığı
-   Ödemenin çok geç yapılma olasılığı

Müşteri ödeme içgörüleri (Önizleme), beklenen ödemelerin toplu görünümünü de sunar. Bu da kuruluşların üç olasılıktan birinde (Zamanında, Geç ve Çok geç) müşteriden bekleyebilecekleri toplam ödeme tutarını anlamalarına yardımcı olabilir.

[![Ödeme tahminlerinin toplu görünümü](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Ayrıca, her faturaya bir zamanında ödeme yapılma olasılığı da atanır. Zamanında ödeme olasılığı %50'nin altındaysa bu faturalara tahsilat uyarısı gerekebileceğini belirtmek için faturalar kırmızı bir daire ile etiketlenir. 

[![Ödeme olasılıklarının listesi](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Ayrıca Müşteri ödeme öngörüleri (Önizleme) tahminleri etkileyen en önemli faktörler, müşteriyle olan işin mevcut durumu ve geçmiş müşteri ödeme davranışı hakkında ayrıntılar gibi tahminleri açıklamak için bağlamsal bilgiler de sağlar. Birçok işletmede, tahsilat süreci reaktif bir faaliyettir; tahsilat süreci faturaların vadesi gelinceye kadar başlamaz. 

Müşteri ödeme öngörüleri (Önizleme) ile kuruluşlar tahsilatlarda daha proaktif olabilir. Tahsilat sürecinin başlaması için hareketlerin gerçekleşme zamanını beklemelerine gerek kalmaz. Bunun yerine, proaktif tahsilatların zamanında ödenme olasılığını artırıp artırmayacağını belirlemek için ödeme tahmini özelliğini kullanabilirler. Ödeme tahmini, aynı zamanda işletmelere tahsilat sürecinin erken başlamasını haklı gösteren bilgiler de sağlar.

## <a name="methodology"></a>Metodoloji

Bir yapay zeka çözümü geliştirmek ve dağıtmak zordur. Kullanılabilir bir yapay zeka çözümünü formüle etmek, geliştirmek, dağıtmak ve korumak için uzun zamandır çalışmakta olan veri bilimcileri, konu uzmanları ve mühendislerden oluşan bir takım gereklidir. Yapay zeka çözümlerinin Finance'ta dağıtımını ve kullanılmasını kolaylaştırıyoruz. Finance'ta Microsoft AI Builder üzerine inşa edilen yapay zeka çözümleri hazırlıyoruz. Tek tıkla bir son kullanıcı, yapay zeka çözümünü dağıtabilir ve akıllı tahminlerin avantajlarından yararlanmaya başlayabilir. Kuruluş, tahminlerin doğruluğundan memnun kalmazsa bir uzman kullanıcı yine tek tıkla AI builder uzantısı deneyimine girebilir ve ardından tahminler oluşturmak için kullanılan alanları seçebilir veya alanların seçimini kaldırabilir. Hazır olduklarında, değişiklikler konusunda eğitim verip değişiklikleri yayımlayabilirler ve eğitimi verilmiş model, Finance'taki tahminler için otomatik olarak seçilir.

## <a name="how-to-get-customer-payment-insights-preview"></a>Müşteri ödeme öngörüleri (Önizleme) edinme

Müşteri ödeme içgörüleri (Önizleme) uygulamasını denemek istiyorsanız lütfen [Müşteri ödeme içgörüleri (Önizleme)](mailto:fiap@microsoft.com) adresine e-posta gönderin.

## <a name="privacy-notice"></a>Gizlilik Bildirimi

Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri kullanmamalıdır ve (4) sınırlı desteğe sahiptir.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]