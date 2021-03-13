---
title: Müşteriye ödeme tahminleri (önizleme)
description: Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamanıza yardımcı olan ödeme tahmini özelliği açıklanmıştır. Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanızı gerektiren durumları belirlemenize de yardımcı olabilir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: f306f9437b78005d8b8aa11f0b6f210ebdd4fd2a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995077"
---
# <a name="customer-payment-predictions-preview"></a>Müşteriye ödeme tahminleri (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamanıza yardımcı olan ödeme tahmini özelliği açıklanmıştır. Bu özellik, tahsilatları normalde yaptığınızdan daha erken başlatmanızı gerektiren durumları belirlemenize de yardımcı olabilir.

## <a name="overview"></a>Genel bakış

Kuruluşlar genellikle müşterilerinin faturalarını ne zaman ödeyeceklerini öngörmede zorluk yaşar. Bu içgörü eksikliği, aşağıdaki sorunlara neden olabilir:

- Daha az doğru nakit akışı tahminleri
- Çok geç başlayan tahsilat işlemleri
- Borcunu ödeyemeyecek müşterilere gönderilen siparişler

Müşteri ödeme tahminleri (önizleme), müşteri faturasının ne zaman ödeneceğini tahmin etme konusunda kuruluşlara yardımcı olur. Böylece, kuruluşlar zamanında ödeme alma olasılığı artırmaya yardımcı olan tahsilat stratejileri oluşturabilir.

## <a name="predictions"></a>Öngörüler

Ödeme tahminleri, kuruluşların, geç ödenme olasılığı yüksek olan faturaları tanımlamasına yardımcı olacak iş süreçlerini geliştirmesine olanak tanır. Kuruluş, faturanın zamanından ödenmesi olasılığını artırmaya yardımcı olan önlemler almak için bu bilgileri kullanabilir.

Müşteri ödeme tahminleri özelliği, bir müşterinin bekleyen bir faturayı ne zaman ödeyeceğini daha doğru tahmin için bir makine öğrenimi modeli kullanır. Bu makine öğrenimi modeli geçmiş faturaları, ödemeleri ve müşteri verilerini içerir.

Her açık fatura için özellik, üç ödeme olasılığından birini atar:

- Ödemenin zamanında yapılması olasılığı
- Ödemenin geç yapılması olasılığı
- Ödemenin çok geç yapılması olasılığı

Bu özellik ayrıca beklenen ödemelerin toplu görünümünü de sağlar.

[![Ödeme tahminlerinin toplu görünümü](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Her faturaya, zamanında ödeme yapılma olasılığı atanır. Zamanında ödeme olasılığı yüzde 50'nin altında olan faturalar, tahsilat temsilcisinin ilgilenmesinin gerekebileceğini belirtmek için kırmızı bir daireyle işaretlenir.

[![Ödeme olasılıklarının listesi](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Müşteri ödeme tahminleri özelliği, tahmini açıklamak için bağlam hakkında bilgiler de sağlar. Bu bilgiler arasında tahmini etkileyen başlıca etmenler, müşteriyle işin geçerli durumu ve müşterinin geçmiş ödeme davranışıyla ilgili ayrıntılar yer alır.

Birçok işletmede tahsilat işlemi reaktif bir faaliyettir. Diğer bir ifadeyle tahsilat işlemi, faturaların vadesi gelene kadar başlamaz. Müşteri ödeme tahminleri, kuruluşların tahsilatlar konusunda daha proaktif olmasını sağlar. Kuruluşun tahsilat sürecini başlatmak için hareketin gerçekleşme zamanını beklemesine gerek kalmaz. Bunun yerine, proaktif tahsilatların zamanında ödenme olasılığını artırıp artırmayacağını belirlemek için ödeme tahminleri özelliğini kullanabilirler.

## <a name="methodology"></a>Metodoloji

Geçmişte, yapay zeka (AI) çözümü geliştirmek ve dağıtmak genellikle zordu. Kullanılabilir bir AI çözümünü formüle etmek, geliştirmek, dağıtmak ve korumak için uzun zamandır çalışmakta olan veri bilimcileri, konu uzmanları (SME'ler) ve mühendislerden oluşan bir takım gerekliydi. Müşteri ödeme tahminleri, Microsoft Dynamics 365 Finance'te bir AI çözümünü dağıtmayı ve kullanmayı kolaylaştırır. Microsoft, Microsoft AI Builder üzerine inşa edilen AI çözümlerini önceden hazırlayıp sunuyor. Böylece kullanıcılar, akıllı tahminlerin avantajlarından yararlanmak için tek bir fare tıklamasıyla AI çözümünü dağıtabiliyor. Tahminlerin doğruluğundan memnun kalmazsanız bir uzman kullanıcı yine tek tıkla AI builder uzantısı deneyimine girebilir ve ardından tahminler oluşturmak için kullanılan alanları seçebilir veya alanların seçimini kaldırabilir. Hazır olduğunuzda modeli "eğitebilirsiniz" ve değişiklikleri yayımlayabilirsiniz. Yeni eğitilen model, Dynamics 365 Finance'te tahmin oluşturmak için otomatik olarak seçilebilir.

## <a name="release-details"></a>Serbest bırakma ayrıntıları

Mali İçgörüler genel önizleme, Amerika Birleşik Devletleri, Avrupa ve Birleşik Krallık'ta deneme için sunulmuştur. Microsoft, destek sunduğu bölgeleri kademeli olarak artırmaktadır.

Genel önizleme özellikleri, yalnızca Katman 2 korumalı alan ortamlarında açılmalıdır. Korumalı alan ortamında oluşturulan kurulum ve AI modelleri, üretim ortamına geçirilemeyebilir. Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Önizlemeleri için Ek Kullanım Koşulları](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Gizlilik bildirimi

Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.