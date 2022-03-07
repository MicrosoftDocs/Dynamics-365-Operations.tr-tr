---
title: AI-ML tabanlı ürün önerisi sonuçlarını ayarlama
description: Bu konu, yapay zeka makine öğrenme (AI-ML) tabanlı ürün öneri sonuçlarının işletmenize nasıl uyarlanacağını açıklamaktadır.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5374b2ce559134bd26036b06ac6d96a9f5510ab847544707fc9885506aaab547
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748534"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>AI-ML tabanlı ürün önerisi sonuçlarını ayarlama


[!include [banner](includes/banner.md)]

Bu konu, yapay zeka makine öğrenme (AI-ML) tabanlı ürün öneri sonuçlarının işletmeniz için nasıl ayarlanacağını açıklamaktadır. 

Ürün önerilerini etkinleştirdikten sonra, varsayılan ayarlar etkili olur; Bu parametreler birçok gereksinim için çalışır. Sonuçların satış hareketi ile uyumlu olup olmadıklarını değerlendirmek için bir zaman harcamaya plan yapmak en iyisidir. Yeniden test etmeden önce parametreleri değiştirmeden önce, birkaç gün için sonuçları değerlendirme öneriyoruz. 

## <a name="understanding-recommendation-list-parameters"></a>Öneri listesi parametrelerini anlama

Parametreleri değiştirmeden önce, aşağıdaki sonuçların nasıl etkilendiklerini öğrenin.

### <a name="trending-product-list"></a>"Trend" ürün listesi

"Trend" ürün listesi, değiştirilebilen iki parametreye sahiptir:

![Örnek "Trend" listesi varsayılan parametresi](./media/exampletrendingparameters.png)

1. **Son X günden yeni ürünleri dahil et** - Ürün adaylarını seçmek için geçerli tarihten önce belirtilen gün sayısına eklenen ürünler. Resimdeki varsayılan değer, ürünlerin eski ürün listesinde 180 gün içinde kullanılabilir olmasını önerir.
1. **Son X günden satışları dahil et** - Ürün sipariş etmek için geçerli tarihten önce belirtilen gün sayısındaki satış işlemleri. Yukarıdaki varsayılan değer, son 30 gün içinde bir ürünün yaptığı tüm satınalmaların, ürünün trend ürün listesine yerleştirilmesiyle ilgili olarak kullanılmasını önerir. 

### <a name="best-selling-product-list"></a>"Trend" ürün listesi

İşinize bağlı olarak "En iyi satış" listesi, her ikisi de sipariş ürünleri için hareket verileri kullansa bile, daha fazla satan sonuçlar elde edilebilir. En iyi satış, sınıflama tarihine bağlı olarak kesilmediğinden, en iyi satış çok popüler olan, trend listesinden düşmüş olan daha eski ürünleri vurgulayabilir. 

"En iyi satış" ürün listesi, değiştirilebilen bir parametreye sahiptir:

![Örnek en iyi satış listesi varsayılan parametresi.](./media/examplebestsellingparameters.PNG)

1. **Son X günden satışları dahil et** - Ürün sipariş etmek için geçerli tarihten önce belirtilen gün sayısındaki satış işlemleri. Yukarıdaki varsayılan değer, son 30 gün içinde bir ürünün yaptığı tüm satınalmaların, ürünün en iyi satış çok popüler olan ürün listesine yerleştirilmesiyle ilgili olarak kullanılmasını önerir. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Öneri listelerine el ile ürün ekleme veya kaldırma

### <a name="for-new-trending-or-best-selling-lists"></a>"Yeni", "trend" veya "en İyi satış" listeleri için

1.  **Perakende ve Ticaret** > **ürün önerileri** > **öneri parametrelerine** gidin.
1.  Paylaşılan parametreleri listesinde, **öneri listelerini** seçin.
1.  Ürünlerin ekleneceği veya kaldırılacağı listeyi seçin.
1.  Tabloya ürün eklemek için **Satır ekle** seçin. 
1.  Ürün sütunu altında, **adı** veya **ürün numarasını** kullanarak ürünü arayın.

    ![Yeni ürün listesinde ürün arama örneği.](./media/examplenewlistconfiguration1.png)

1.  Satır türü sütunu altında, iki seçenekten birini belirleyin:
    -   **Dahil et** – bir ürünü listenin önüne zorlar
    -   **Dışla** – bir ürünün listede görünmesini kaldırır
    
    ![Ürünü yeni ürün listesinden içerme veya hariç tutma örneği.](./media/examplenewlistconfiguration2.png)

1.  **Görüntüleme sırasının** değiştirilmesi, **dahil** edilen ürünlerin listede görüneceği sırayı değiştirir.
    - İki ürün aynı **görüntü sipariş** değerine sahipse, bu iki sonucun son sırası arka ofisten farklı olabilir.
1.  Tablodan ürün kaldırmak için: kaldırılacak satırı seçin ve **Kaldır** 'ı seçin.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>"Bunları da beğenenler" ve "Birlikte sık satın alınanlar" listeleri için

"Sıklıkla birlikte satın alınanlar" veya "Bunları da beğendiler" listeleri bağlamında, makine öğrenme, özel bir üretim ürünü için yaygın olarak satın alınan ilgili ürünleri önermek amacıyla tüketici satın alma düzenlerini analiz etmek için kullanılır. 
 
*Tohum ürünü*, sonuçları oluşturmak istediğiniz ürün. Öneri listelerini el ile ayarlama bağlamında, bu ürün için sonuç ekliyor veya kaldırırsınız. 

Bir çekirdek ürünle ilgili sonuçları el ile eklemek veya kaldırmak için aşağıdaki adımları izleyin:
1.  **Tohum ürünü** seçin. 
1.  **Ürün** sütunu altında, **adı** veya **ürün numarasını** kullanarak ürünü arayın.
![Yeni ürün listesinde ürün arama örneği.](./media/exampleFBTlistconfiguration1.png)
1. **Satır türü** sütunu altında, iki seçenekten birini belirleyin:
    - **Dahil et** – bir ürünü listenin önüne zorlar
    - **Dışla** – bir ürünün listede görünmesini kaldırır     
![En sık satın alınan listede ürün ekleme veya çıkarma örneği.](./media/exampleFBTlistconfiguration2.png)
1.  Tablodan ürün kaldırmak için: kaldırılacak satırı seçin ve Kaldır 'ı seçin.


## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]