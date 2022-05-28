---
title: Müşteri ödeme tahminleri kullanma
description: Bu konu, Mali içgörülerimn deneme sürümünü kullanmak için gerekli ön koşulları ve kapsamlı adımları açıklar.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: ecc864485dfc106df22b48e92a85f2c73d58e0e8
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740638"
---
# <a name="use-customer-payment-predictions"></a>Müşteri ödeme tahminleri kullanma

[!include [banner](../includes/banner.md)]

Bu konu, Müşteri ödeme tahminlerinin nasıl kullanılacağını açıklar. Bu özelliği kullanmadan önce, kurulum adımlarını tamamladığınızdan emin olun. Daha fazla bilgi için bkz. [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md).

**Müşteri alacak ve tahsilatlarını yönetme** çalışma alanında ve **Hareket ödeme tahminleri** ile **Müşteri ödeme tahminleri** adlı iki yeni liste sayfasında müşteri ödeme tahminlerini görebilirsiniz.

### <a name="manage-customer-credit-and-collections-workspace"></a>Müşteri alacak ve tahsilatlarını yönetme çalışma alanı

**Müşteri alacak ve tahsilatlarını yönetme** çalışma alanı, **Hareket ödeme tahminleri** ve **Müşteri ödeme tahminleri** adlı iki yeni kutucuk içerir.

### <a name="transaction-payment-predictions-list-page"></a>Hareket ödeme tahminleri liste sayfası

**Hareket ödeme tahminleri** liste sayfasında, açık hareketlerin ödeme olasılığını **Zamanında**, **Geç** ve **Çok geç** demetlerinde görebilirsiniz. Izgaradaki her hareket için **Zamanında olasılığı** sütununda, faturanın vade tarihinde veya daha önce ödenme olasılığı gösterilir. Zamanında ödeme olasılığının yüzde 50'den az olduğu durumlarda geç ödeme riskini belirtmek için **Zamanında olasılığı** sütunundaki yüzdenin yanında kırmızı bir daire görünür.

[![Hareket başına ödeme tahmini sayfası.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Sayfanın sağ tarafındaki **İlgili bilgiler** bölmesinde tahminler hakkında daha fazla ayrıntı sağlanır.

- Izgarada seçilen hareket için **Ödeme tahmini** hızlı sekmesi; **Zamanında**, **Geç** ve **Çok geç** demetlerinde ödeme tahminlerinin ayrıntılarını gösterir. **Başlıca etmenler** bölümü, tahminleri etkileyen başlıca etmenleri gösterir. Başlıca etmenler, seçilen hareketin ve/veya söz konusu hareket müşterisinin öznitelikleridir.
- **Müşteri içgörüleri** hızlı sekmesi, seçili hareketin müşterisi için geçerli faturayı, ödemeyi ve tahsilat istatistiklerini gösterir.
- **Müşteri geçmişi** hızlı sekmesi, müşterinin ödeme geçmişini **Zamanında**, **Geç** ve **Çok geç** demetlerinde gösterir.

**Başlıca etmenler** bölümündeki ve **Müşteri içgörüleri** ile **Müşteri geçmişi** hızlı sekmelerindeki veriler, ödeme tahminlerinin açıklanmasına yardımcı olur. Bunlar, tahminlerin etkililiğine duyduğunuz güveni artırmaya yardımcı olabilir.

[![İlgili bilgiler bölmesinde ödeme tahminleri için grafik göstergeler.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Müşteri ödeme tahminleri liste sayfası

**Müşteri ödeme tahminleri** liste sayfası, toplam açık bakiyeyi ve **Zamanında**, **Geç** ve **Çok geç** demetlerinde ödenmesi tahmin edilen tutarı gösterir.

[![Müşteri başına ödeme tahminleri liste sayfası.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- Izgarada seçilen hareket için **Ödeme tahminleri** hızlı sekmesi; **Zamanında**, **Geç** ve **Çok Geç** demetlerinde ödeme tahminlerinin ayrıntılarını gösterir.
- **Müşteri içgörüleri** hızlı sekmesi, seçili hareketin müşterisi için geçerli faturayı, ödemeyi ve tahsilat istatistiklerini gösterir.
- **Müşteri geçmişi** hızlı sekmesi, müşterinin ödeme geçmişini **Zamanında**, **Geç** ve **Çok geç** demetlerinde gösterir.

**Customer Insights** ve **Müşteri geçmişi** hızlı sekmelerindeki veriler, ödeme tahminlerinin açıklanmasına yardımcı olur. Bunlar, tahminlerin etkililiğine duyduğunuz güveni artırmaya yardımcı olabilir.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Ödeme tahminlerinin doğruluğunu iyileştirme

**Alacak ve tahsilatlar \> Kurulum \> Mali içgörüler \> Mali içgörü parametreleri** bölümüne giderek ödeme tahminlerinin doğruluğunu görüntüleyebilirsiniz. **Müşteri ödemesi içgörüleri** sekmesinde, **Tahmin modeli** bölümünde tahmin modelinin doğruluğu yüzde olarak gösterilir.

Doğruluk oranından memnun değilseniz AI Builder uzantısı deneyimini açmak için **Model doğruluğunu iyileştir** bağlantısını seçin. AI Builder uzantısı deneyiminde, ödeme olasılıklarını doğru şekilde tahmin etmek için önemli olduğu düşündüğünüz alanları seçene kadar alanları seçebilir veya seçimlerini iptal edebilirsiniz. İşlemi tamamladığınızda thamin modelini kolayca yeniden eğitebilir ve yaptığınız değişiklikleri yayımlayabilirsiniz. Yeni eğitilen tahmin modeli, Dynamics 365 Finance'te tahminler için otomatik olarak seçilebilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
