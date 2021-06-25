---
title: Müşteriye ödeme tahminleri (önizleme)
description: Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamanıza yardımcı olan ödeme tahmini özelliği açıklanmıştır. Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanızı gerektiren durumları belirlemenize de yardımcı olabilir.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 84a2342d76dc309fa1fd3de7b2c3de60e62e4d72
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186408"
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

Genel önizleme özellikleri, yalnızca Katman 2 korumalı alan ortamlarında açılmalıdır. Korumalı alan ortamında oluşturulan kurulum ve AI modelleri, üretim ortamına geçirilemeyebilir. Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Önizlemeleri için Ek Kullanım Koşulları](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
