---
title: Yenilik analizi, Sıklık analizi ve Parasal (RFM) analiz ayarlama
description: Bu makalede müşterilerinizin Recency, Sıklığı ve parasal (RFM) Analizi açıklanır.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 153759ac6b70235b79c080e934819536c2861371
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850183"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Yenilik analizi, Sıklık analizi ve Parasal (RFM) analiz ayarlama

[!include [banner](includes/banner.md)]

Bu makalede müşterilerinizin Recency, Sıklığı ve parasal (RFM) Analizi açıklanır.

Recency, sıklık ve parasal (RFM) analiz, organizasyonunuzun Müşteri Harcamaları tarafından üretilen verileri değerlendirmek için kullanabileceği bir pazarlama aracıdır . RFM analiz ayarladıktan sonra müşterilere Satın almalar yaparken hesaplanan bir RFM puan atanır. RFM puanı üç basamaklı derecelendirme veya kuruluşunuzun RFM analiz nasıl yapılandırdığına bağlı olarak bir toplama numarası olabilir. Kuruluşunuzun puanlama için üç basamaklı derecelendirme kullanması durumunda derecelendirme aşağıdaki şekilde çalışır:

- İlk basamak müşterinin recency derecesidir. Bu derece müşterinin kuruluşunuzdan en son ne zaman satınalma yaptığını gösterir.
- İkinci basamak müşteri sıklık derecesidir. Bu, genellikle müşterinin kuruluşunuzdan ne sıklıkla satınalma yaptığını gösterir.
- Üçüncü basamak müşterinin parasal derecelendirmesidir. Bu, müşterinin kuruluşunuzdan yaptığı satınalımlarda ne kadar para harcadığını gösterir.

Örneğin, kuruluşunuzun derecelendirme 1 ile 5 arası bir ölçek üzerinde 5 en yüksek derece olarak ayarlamıştır. Bu durumda, bir müşteri 535 derecesi müşteri hakkında aşağıdaki bilgileri gösterir:

- **5 recency derecesi** – müşteri yakın zamanda satın alma yapmıştır.
- **Sıklık derecesi 3** – müşteri oldukça sık, organizasyonunuzun ürünleri satın almaktadır.
- **Parasal derecesi 5** – Müşteri bir satın alma yaptığında önemli miktarda para harcar.

Kuruluşunuz için puan toplama bir numarası kullanıyorsa, bireysel derecelendirme birlikte eklenir. Aynı örnekte, müşterinin derecesi 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Kuruluşunuzdaki müşteriler için RFM analizini ayarlamak

1. **Çağrı merkezi** \> **Periyodik** \> **RFM analizi**'ne gidin.
2. **RFM analizi** sayfasında, **Yeni**'yi seçin. **RFM tanımı** alanına, RFM tanımıyla ilgili adı girin. Örneğin, tanımı RFM-A olarak adlandırabilirsiniz.
3. Bu RFM tanımı için bir başlangıç tarihi ve bitiş tarihi girin.
4. **Genel** hızlı sekmesinde, aşağıdakileri yapın:

    - RFM puanının her bölümünün eşit sayıda müşteri içermesi gerekiyorsa, **Eşit dağıtım** onay kutusunu seçin.
    - Üç puanı toplamak için **Puan ekle** onay kutusunu işaretleyin. Örneğin, bu müşteriye 535 yerine 13 RFM puanı verecektir.
    - Sistemin müşteriler için istatistik verilerini kaydetmesini sağlamak için **Geçmişi kaydet** onay kutusunu işaretleyin; böylece veriler RFM puanını hesaplamak için kullanılabilir.

5. **Recency** hızlı sekmesinde, aşağıdakileri yapın:

    - **Bölümler** alanına, müşterilerin recency puanını hesaplamak için kullanılacak bölümlerin veya grupların sayısını girin. Örneğin, 100 müşteriniz ve 5 bölümünüz varsa, her puanlama için 20 müşteri olacaktır. En yakın zamanda satınalım yapan 20 müşterinin recency puanı 5 olacaktır. Sonraki 20 müşterinin recency puanı 4 olacak ve bu şekilde devam edecektir. 50 müşteriniz varsa, 10 müşterinin recency puanı 5, 10 müşterinin recency puanı 4 olacak ve bu şekilde devam edecektir.
    - **Öncelik** alanında, bir müşteri için RFM puanı hesaplanırken recency parametresine diğer parametrelere oranla ne kadar ağırlık verileceğini seçin. Örneğin, recency puanına parasal puandan daha fazla değer atayabilirsiniz.
    - **Çarpan** alanına, recency puanının çarpılacağı değeri girin. Bir değer girmezseniz, puan çarpılmaz.
    - **Dönem** alanında, recency puanının hangi dönem için hesaplanacağını seçin. Örneğin haftalık veya aylık.

6. **Sıklık** hızlı sekmesinde, aşağıdakileri yapın:

    - **Bölümler** alanına, müşterilerin sıklık puanını hesaplamak için kullanılacak bölümlerin veya grupların sayısını girin.
    - **Öncelik** alanında, bir müşteri için RFM puanı hesaplanırken sıklık parametresine diğer parametrelere oranla ne kadar ağırlık verileceğini seçin.
    - **Çarpan** alanına, sıklık puanının çarpılacağı değeri girin. Bir değer girmezseniz, puan çarpılmaz.

7. **Parasal** hızlı sekmesinde, aşağıdakileri yapın:

    - **Bölümler** alanına, müşterilerin parasal puanını hesaplamak için kullanılacak bölümlerin veya grupların sayısını girin.
    - **Öncelik** alanında, bir müşteri için RFM puanı hesaplanırken parasal parametresine diğer parametrelere oranla ne kadar ağırlık verileceğini seçin.
    - **Çarpan** alanına, parasal puanın çarpılacağı değeri girin. Bir değer girmezseniz, puan çarpılmaz.
    - **Brüt/net** alanında, müşterinin parasal puanının brüt fatura tutarı mı yoksa net fatura tutarı mı kullanılarak hesaplanacağını seçin.
    - Müşterinin iade tutarlarının müşterinin toplam fatura tutarından çıkarılması gerekiyorsa, **İadeleri çıkar** onay kutusunu seçin.

## <a name="view-a-customers-rfm-score"></a>Bir müşterinin RFM puanını görüntüleme

Bu yordamı bir müşterinin RFM puanını görüntülemek için kullanın.

1. **Çağrı merkezi** \> **Günlükler** \> **Müşteri hizmetleri**'ne gidin.
2. **Müşteri Hizmetleri** bölmesindeki **Müşteri hizmetleri** sayfasında, arama alanlarında arama için kullanacağınız anahtar sözcüğü yazmayı seçin ve arama metnini girin.
3. **Ara**'yı seçin.
4. **Müşteri arama** sayfasında istediğiniz müşterinin kaydını seçin ve ardından **Müşteri seç**'e tıklayın.

RFM puanı **Müşteri Hizmetleri** sayfasının sağ tarafındaki **Sipariş geçmişi** grubunda görüntülenir.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>RFM analizi kaydı geçmişini görüntüleme veya silme

RFM analizi kaydı geçmişini görüntülemek veya silmek için bu yordamı kullanın.

1. **Çağrı merkezi** \> **Periyodik** \> **RFM analizi**'ne gidin.
2. **RFM analizi** sayfasında, görüntülemek istediğiniz kaydı seçin.
3. Kayıt geçmişini görüntülemek için **Geçmiş** hızlı sekmesini seçin.
4. Kayıt geçmişini silmek için **Geçmişi temizle**'yi seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]