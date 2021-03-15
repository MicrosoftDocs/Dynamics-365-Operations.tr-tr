---
title: Müşteri ödeme tahminleri kullanma (önizleme)
description: Bu konu, Mali içgörülerimn deneme sürümünü kullanmak için gerekli ön koşulları ve kapsamlı adımları açıklar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/16/2020
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
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: e0445046d8016dfa2c02c1ff1a05bdd148f9409a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969265"
---
# <a name="use-customer-payment-predictions-preview"></a>Müşteri ödeme tahminleri kullanma (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, Müşteri ödeme tahminlerinin nasıl kullanılacağını açıklar. Bu özelliği kullanmadan önce, kurulum adımlarını tamamladığınızdan emin olun. Daha fazla bilgi için bkz. [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md).

**Müşteri alacak ve tahsilatlarını yönetme** çalışma alanında ve **Harekete göre ödeme tahminleri** ile **Müşteriye göre ödeme tahmini** adlı iki yeni liste sayfasında müşteri ödeme tahminlerini görebilirsiniz.

### <a name="manage-customer-credit-and-collections-workspace"></a>Müşteri alacak ve tahsilatlarını yönetme çalışma alanı

**Müşteri alacak ve tahsilatlarını yönetme** çalışma alanı, **Harekete göre ödeme tahmini** ve **Yüksek oranda geç bakiye öngörülen müşteriler** adlı iki yeni kutucuk içerir.

- **Hareket başına ödeme tahmini** kutucuğu, **Zamanında** demetinde yüzde 50'den daha az ödeme olasılığı olan açık müşteri hareketlerinin sayısı gösterilir. **Hareket başına ödeme tahminleri** liste sayfasını açmak için bu kutucuğu seçebilirsiniz.
- **Yüksek oranda geç bakiye öngörülen müşteriler**, toplam bakiyenin yarısından (yüzde 50) fazlasının geç ve/veya çok geç ödeneceği tahmin edilen müşterilerin sayısını gösterir. **Müşteri başına ödeme tahmini** liste sayfasını açmak için bu kutucuğu seçebilirsiniz.

[![Müşteri alacak ve tahsilatlarını yönetme çalışma alanı](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Hareket başına ödeme tahminleri liste sayfası

**Hareket başına ödeme tahminleri** liste sayfasında, açık hareketlerin ödeme olasılığını **Zamanında**, **Geç** ve **Çok geç** demetlerinde görebilirsiniz. Izgaradaki her hareket için **Zamanında olasılığı** sütununda, faturanın vade tarihinde veya daha önce ödenme olasılığı gösterilir. Zamanında ödeme olasılığının yüzde 50'den az olduğu durumlarda geç ödeme riskini belirtmek için **Zamanında olasılığı** sütunundaki yüzdenin yanında kırmızı bir daire görünür.

[![Hareket başına ödeme tahmini sayfası](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Sayfanın sağ tarafındaki **İlgili bilgiler** bölmesinde tahminler hakkında daha fazla ayrıntı sağlanır.

- Izgarada seçilen hareket için **Ödeme tahmini** hızlı sekmesi; **Zamanında**, **Geç** ve **Çok geç** demetlerinde ödeme tahminlerinin ayrıntılarını gösterir. **Başlıca etmenler** bölümü, tahminleri etkileyen başlıca etmenleri gösterir. Başlıca etmenler, seçilen hareketin ve/veya söz konusu hareket müşterisinin öznitelikleridir.
- **Müşteri içgörüleri** hızlı sekmesi, seçili hareketin müşterisi için geçerli faturayı, ödemeyi ve tahsilat istatistiklerini gösterir.
- **Müşteri geçmişi** hızlı sekmesi, müşterinin ödeme geçmişini **Zamanında**, **Geç** ve **Çok geç** demetlerinde gösterir.

**Başlıca etmenler** bölümündeki ve **Müşteri içgörüleri** ile **Müşteri geçmişi** hızlı sekmelerindeki veriler, ödeme tahminlerinin açıklanmasına yardımcı olur. Bunlar, tahminlerin etkililiğine duyduğunuz güveni artırmaya yardımcı olabilir.

[![İlgili bilgiler bölmesinde ödeme tahminleri için grafik göstergeler](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Müşteri başına ödeme tahmini liste sayfası

**Müşteri başına ödeme tahmini** liste sayfası, toplam açık bakiyeyi ve **Zamanında**, **Geç** ve **Çok geç** demetlerinde ödenmesi tahmin edilen tutarı gösterir.

[![Müşteri başına ödeme tahminleri liste sayfası](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Her bir demetteki ödeme tutarı, hareket bakiyesinin ağırlıklı ortalamasının toplamı olarak hesaplanır. Bu tutar, her bir demetteki ödeme olasılıklarına göre hesaplanır.

Örneğin, bir müşterinin her bir demette aşağıdaki ödeme olasılıklarına sahip üç açık hareketi vardır.

| Hareket | Tutar | Zamanında ödeme olasılığı | Geç ödeme olasılığı | Çok geç ödeme olasılığı |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | Yüzde 10                  | Yüzde 50               | Yüzde 40                    |
| T2          | 1,000  | Yüzde 50                  | Yüzde 30               | Yüzde 20                    |
| T3          | 10,000 | Yüzde 1                   | Yüzde 4                | Yüzde 95                    |

Bu durumda, her bir demet için ödemeler aşağıdaki şekilde tahmin edilir.

| Demetler   | Hareket T1      | Hareket T2         | Hareket T3            | Toplam |
|-----------|---------------------|------------------------|---------------------------|-------|
| Zamanında   | 100 × 10 ÷ 100 = 10 | 1.000 × 50 ÷ 100 = 500 | 10.000 × 1 ÷ 100 = 100    | 610   |
| Geç      | 100 × 50 ÷ 100 = 50 | 1.000 × 30 ÷ 100 = 300 | 10.000 × 4 ÷ 100 = 400    | 750   |
| Çok geç | 100 × 40 ÷ 100 = 40 | 1.000 × 20 ÷ 100 = 200 | 10.000 × 95 ÷ 100 = 9.500 | 9,740 |

Sayfanın sağ tarafındaki **İlgili bilgiler** bölümünde tahminler hakkında daha fazla ayrıntı sağlanır.

- Izgarada seçilen hareket için **Ödeme tahminleri** hızlı sekmesi; **Zamanında**, **Geç** ve **Çok Geç** demetlerinde ödeme tahminlerinin ayrıntılarını gösterir. **Başlıca etmenler** bölümü, ödemeleri etkileyen başlıca etmenleri gösterir. Başlıca etmenler, seçilen hareketin ve/veya söz konusu hareket müşterisinin öznitelikleridir.
- **Müşteri içgörüleri** hızlı sekmesi, seçili hareketin müşterisi için geçerli faturayı, ödemeyi ve tahsilat istatistiklerini gösterir.
- **Müşteri geçmişi** hızlı sekmesi, müşterinin ödeme geçmişini **Zamanında**, **Geç** ve **Çok geç** demetlerinde gösterir.

**Başlıca etmenler** bölümündeki ve **Müşteri içgörüleri** ile **Müşteri geçmişi** hızlı sekmelerindeki veriler, ödeme tahminlerinin açıklanmasına yardımcı olur. Bunlar, tahminlerin etkililiğine duyduğunuz güveni artırmaya yardımcı olabilir.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Ödeme tahminlerinin doğruluğunu iyileştirme

**Alacak ve tahsilatlar \> Kurulum \> Mali içgörüler \> Mali içgörü parametreleri** bölümüne giderek ödeme tahminlerinin doğruluğunu görüntüleyebilirsiniz. **Müşteri ödemesi içgörüleri** sekmesinde, **Tahmin modeli** bölümünde tahmin modelinin doğruluğu yüzde olarak gösterilir.

[![Ödeme tahminlerinin doğruluğu](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Doğruluk oranından memnun değilseniz AI Builder uzantısı deneyimini açmak için **Model doğruluğunu iyileştir** bağlantısını seçin. AI Builder uzantısı deneyiminde, ödeme olasılıklarını doğru şekilde tahmin etmek için önemli olduğu düşündüğünüz alanları seçene kadar alanları seçebilir veya seçimlerini iptal edebilirsiniz. İşlemi tamamladığınızda thamin modelini kolayca yeniden eğitebilir ve yaptığınız değişiklikleri yayımlayabilirsiniz. Yeni eğitilen tahmin modeli, Dynamics 365 Finance'te tahminler için otomatik olarak seçilebilir.

[![AI Builder uzantısı deneyimi](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Serbest bırakma ayrıntıları

Mali içgörüler genel önizleme, Amerika Birleşik Devletleri, Avrupa ve Birleşik Krallık'ta deneme için sunulmuştur. Microsoft, destek sunduğu bölge sayısını kademeli olarak artırmaktadır.

Genel önizleme özellikleri, yalnızca Katman 2 korumalı alan ortamlarında açık olabilir ve açılmalıdır. Korumalı alan ortamında oluşturulan kurulum ve AI modelleri, üretim ortamına geçirilemez. Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Önizlemeleri için Ek Kullanım Koşulları](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Gizlilik bildirimi

Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]