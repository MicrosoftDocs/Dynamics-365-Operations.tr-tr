---
title: Kıymet KPI'ları
description: Bu konuda Kıymet Yönetimi'ndeki KPI'lar açıklanmaktadır.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b2122cb123e041d2194fa1ef5fd8024ec4c1a2a0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361102"
---
# <a name="asset-kpis"></a>Kıymet KPI'ları

[!include [banner](../../includes/banner.md)]

 

Varlık yönetiminde, kıymetler ve kıymet tipleri için çeşitli ana performans göstergelerini (KPI'lar) hesaplayabilirsiniz. Kullanım süresi, kesinti, süre sonu, onarım süresi ve arıza arasındaki ortalama süre (MTBF) ile ilgili olarak varlıkların performansına genel bir bakış almak için KPI'lar kullanılır.

1. **Varlık Yönetimi** > **Sorgular** > **Varlıklar** > **Varlık KPI'ları**'nı tıklatın.

2. Sabit kıymet **KPI'larıhesapla** iletişim kutusunda, gün içinde kullanılacak **zaman ölçeğini** ve **başlangıç tarihi** ve **bitiş tarihi** alanlarında bir dönem seçin. 

3. **Dahil edilecek kayıtlar** hızlı sekmesinde, gerekirse, hesaplamaya dahil edilecek belirli kıymetleri ve kıymet tiplerini seçebilirsiniz.

4. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

5. **Özet** hızlı sekmesinde, hesaplamanın sonuçları ızgara görünümünde görüntülenir. Her kıymet ayrı bir satırda görüntülenir.

6. **Seçili satır için KPI'lar** hızlı sekmesinde, **Özet** hızlı sekmesinde seçili olan kıymete ait hesaplamaları görürsünüz. KPI değerleri **zaman** , **kullanılabilirlik**, **çalışma emirleri**, **bakım**, **hatalar**, **bakım kapalı kalma** süresi ve **Maliyet** ile ilgili olarak sınıflandırılır.

Aşağıdaki tabloda, **Varlık KPI'ları** sayfasındaki alanların açıklamasını bulacaksınız.

| Alan                   | Tanım                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktif                   | Varlık kodu.                                                                                                                                                                                                                                                                                             |
| Toplam süre              | Hesaplamada kullanılan takvimde ayarlanan toplam süre. Sabit kaynakla ilişkili ise, ilgili kaynak takvimi kullanılır. Kıymet bir kaynakla ilişkili değilse, **kıymet yönetimi parametreleri** alanında **Standart takvim** alanında seçilen takvim kullanılır. |
| Çalışma süresi                  | Toplam süre eksi kesinti.                                                                                                                                                                                                                                                                            |
| Kesinti süresi                | Bakım kapalı kalma süresi, seçilen dönemdeki kıymet üzerinde yapılır.                                                                                                                                                                                                                              |
| Onarım zamanı             | Onarım iş emirleri üzerinde harcanan toplam çalışma saati sayısı.                                                                                                                                                                                                                                            |
| Kullanılabilirlik %'si          | Çalışma süresi toplam süresine bölünür ve 100 ile çarpıldı.                                                                                                                                                                                                                                                   |
| Hata sayısı        | Seçili dönemdeki kıymet üzerinde arıza nedenlerine kaydedilen hata nedeni sayısı.                                                                                                                                                                                                             |
| MTBF                    | Hata arasında toplam süre (kıymete kayıtlı hata sayısı) seçili dönemdeki ortalama zaman. Hata sayısı sıfır ise, MTBF toplam saate ayarlanır.                                                                                                                   |
| Başarısızlık oranı               | 1 MTBF'ye bölünür.                                                                                                                                                                                                                                                                                    |
| MRT                     | Ortalama Tamir süresi (kıymete kayıtlı hata sayısı) seçili dönemdeki varlıkta kayıtlı hataların tamir süresine bölünmesidir. Hata sayısı sıfır ise, MRT tamir süresi ayarlanır.                                                                                                                           |
| Durma sayısı         | Varlıkta oluşturulan toplam bakım kesinti süresinin sayısı.                                                                                                                                                                                                                                     |
| MTBS                    | Toplam süre, bakım aksama sayısı kaydı sayısına bölünen, durakları arasında geçen süre. Seçilen dönemde bakım kapalı kalma sayısı kaydı sıfır ise, MTBS değeri toplam zamana ayarlanır.                                                                                      |
| Önleyici maliyet         | Seçilen dönemde "Koruyucu" maliyet türüyle ilgili kıymete nakledilen maliyetler. Maliyet türleri, iş emri türlerinde ayarlanır.                                                                                                                                                                       |
| Düzeltici maliyet         | Seçilen dönemde "Düzeltici" maliyet türüyle ilgili kıymete nakledilen maliyetler. Maliyet türleri, iş emri türlerinde ayarlanır.                                                                                                                                                                       |
| Değiştirme değeri       | Değişiklik maliyeti olarak kıymet üzerinde tanımlanan değer.                                                                                                                                                                                                                                                  |
| Sabit kıymet türü:             | Kıymet üzerinde seçilen kıymet türünün tanımlaması.                                                                                                                                                                                                                                             |
| Üretici           | Kıymet üzerinde seçilen üreticinin tanımlaması.                                                                                                                                                                                                                                                 |
| Model                   | Kıymet üzerinde seçilen üretici modelinin tanımlaması.                                                                                                                                                                                                                                           |
| Başlangıç tarihi               | KM hesaplamasının başlangıç tarihi. Sabit kıymet hesaplama için seçilen başlangıç tarihinden sonra oluşturulmuşsa, kıymetin başlangıç tarihi bu alanda gösterilir.                                                                                                                                  |
| Bitiş tarihi                 | KM hesaplamasının bitiş tarihi. Hesaplama için seçilen bitiş tarihinden önce kıymet faaliyetsiz olarak kaydedilmişse, bu alanda kıymetin artık etkin olmadığı tarih gösterilir.                                                                                               |
| Zaman ölçeği              | KPI'ların hesaplanması sırasında kullanılacak zaman ölçeğini seçin: saatler, günler veya haftalar.                                                                                                                                                                                                            |
| Kullanılabilirlik            | Çalışma süresi toplam zamana bölündüğünde.                                                                                                                                                                                                                                                                         |
| İş emirleri             | KPI hesaplamasına dahil edilen iş emirlerinin toplam sayısı.                                                                                                                                                                                                                                          |
| İş emri saati         | İş emirleri üzerinde harcanan toplam çalışma saati sayısı.                                                                                                                                                                                                                                               |
| Birincil iş emirleri     | KPI hesaplamasına dahil edilen birincil iş emirlerinin sayısı.                                                                                                                                                                                                                                        |
| İkincil iş emirleri   | KPI hesaplamasına dahil edilen ikincil iş emirlerinin sayısı.                                                                                                                                                                                                                                      |
| Bakım iş emirleri | KPI hesaplamasına dahil edilen bakım iş emirlerinin sayısı. Bakım iş emri, ilişkili hata nedenlerine sahip olmayan iş sıralarıdır.                                                                                                                                                             |
| Bakım zamanı        | Bakım iş emirleri üzerinde harcanan toplam çalışma saati sayısı.                                                                                                                                                                                                                                       |
| İş emirlerini onar      | KPI hesaplamasına dahil edilen onarım iş emirlerinin sayısı. Bir onarım iş emri, hata sebebiyle oluşturulmuş bir iş emridir.                                                                                                                                                                        |
| Güvenilirlik %'si           | Zaman içinde, sabit kıymetin, giyme ve kesilmeleri nedeniyle daha az güvenilir hale gelebileceği anlamına gelen, bir varlık üzerindeki arıza kayıtlarında beklenen üstel gelişmeye dayalı hesaplama hesaplaması. Bu KPI'ın hesaplanması MTBF ve toplam saatine dayanır.                                                            |
| MTPS                    | Ortalama Zaman Üretim Durdurma, bakım kesinti süresinin bakım kesinti süresi kayıtlarına bölünmesidir. Seçilen dönemde bakım kapalı kalma sayısı kaydı sıfır ise, MTPS değeri sıfıra ayarlanır.                                                                               |
| Toplam maliyet              | Seçilen dönemde kıymete nakledilen toplam maliyetler.                                                                                                                                                                                                                                              |
| Yatırım maliyeti         | Seçilen dönemde "Yatırım" maliyet türüyle ilgili kıymete nakledilen maliyetler. Maliyet türleri, iş emri türlerinde ayarlanır.                                                                                                                                                                       |

Aşağıdaki şekil dört kıymet için bir KPI hesaplamasının ekran görüntüsünü gösterir.

![Dört varlık için KPI hesaplamasının ekran görüntüsü.](media/11-controlling-and-reporting.png)

- **Tüm varlıklar** alanında birden fazla varlık için çoklu seçim yapabilirve **Genel** sekmesindeki **Varlık KPI'ları** düğmesine tıklayabilirsiniz. Ardından, seçilen varlıkların KPI'larını hesaplamak için **Varlık KPI'ları hesapla** iletişim kutusunda **Tamam**'a tıklayın.  
- Bir KPI hesaplamasından alınan sonuçlar, kuruluma ve kesinti süresi neden kodlarının ayarına ve kullanımına bağlı olarak [bakım süresi kayıtlarını](../work-orders/maintenance-downtime.md) içerebilir veya içermeyebilir. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]