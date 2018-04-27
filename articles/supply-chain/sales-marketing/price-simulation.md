---
title: Fiyat benzetimi
description: "Bu makalede, teklifler için fiyat benzetimiyle ilgili bilgiler verilmektedir. Fiyat benzetimi, belirli bir fiyat taahhüdünde bulunmadan önce teklif verme işlemi sırasında gelecekteki satış fiyatı kesintilerinin etkisini değerlendirmenize yardımcı olur."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1db68ea5728cc417f0e70675d9074d5b054883da
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="price-simulation"></a>Fiyat benzetimi

[!INCLUDE [banner](../includes/banner.md)]

Bu makalede, teklifler için fiyat benzetimiyle ilgili bilgiler verilmektedir. Fiyat benzetimi, belirli bir fiyat taahhüdünde bulunmadan önce teklif verme işlemi sırasında gelecekteki satış fiyatı kesintilerinin etkisini değerlendirmenize yardımcı olur.

Bir teklif için fiyat benzetimi, yeni toplam tutarı önerilen yeni bir fiyata dayanarak gösterir. Fiyat benzetimi, varolan bir teklif içinde oluşturulan belirli bir satır için yeni bir tutar da gösterebilir. Fiyat benzetimi girebilir ve daha sonra uygulayabilirsiniz. Alternatif olarak, özgün teklifi bir fiyat benzetimi olmadan kullanabilir ve satış sürecinde müşteri ile çalışırken daha fazla değişiklik yapabilirsiniz.  

Bir fiyat benzetimi, teklifteki fiyatı değiştirmez. Fiyat benzetimi bir teklifinin tamamına uygulanırsa, teklif başlığında özel bir indirim olarak kabul edilir. Fiyat benzetimi belirli maddelerle uygulanırsa, teklif satırlarında özel bir indirim olarak kabul edilir. Oluşturulan bir teklif satırındaki birim satış fiyatı, bu fiyat benzetimi uygulandığında değişmez. Bunun yerine, teklif satırındaki fiyat azaltımına karşılık gelen bir iskonto yüzdesi uygulanır. Bir fiyat benzetimi uygulandığında, birim satış fiyatı ve iskonto yüzdesi teklif satırına veya teklif başlığına transfer edilir.  

**Not:** Bir fiyat benzetimini çalıştırırken, yalnızca geçerli satış para birimi benzetim oluşturmak için kullanılır. Ancak teklif toplamlarını görüntülediğinizde, şirket para birimi ve satış para biriminin bir karışımını görürsünüz.  

Teklifi satırlarına eklenen ek maddeler, satır iskontoları veya çoklu satırlı iskontolarını tetikleyebilir. Ayrıca teklif satırlarının katkı paylarını ve katkı oranlarını ve tüm iskontoyu değiştirebilecek toplam iskontoları da tetikleyebilirler.  

Bir teklifin hedeflerinde fiyat ayarlamalarının etkisini izlemek için ayrıca birden çok fiyat benzetimi de çalıştırabilirsiniz. Bu benzetimleri çalıştırarak, teklifin genel fiyatını veya teklif içerisindeki bir veya daha fazla belirli satırın fiyatını ayarlamanıza ve satışı kapatmaya en çok yardımcı olabilecek gibi görünen fiyat benzetimini uygulayabilirsiniz.  

Bir teklif oluşturduğunuzda, bir uyarı ayarlayabilirsiniz. Uyarıların kullanılabileceği bazı yollar şu şekildedir:

-   Bunlar, kuruluştaki tekliflerinin durumu hakkında size bilgi verebilir.
-   Bunlar, belirli bir teklifin gözden geçirilmesini tetiklemek veya iskonto sınırları aşıldığında bilgi verebilirler.

## <a name="price-simulation-and-discounts"></a>Fiyat benzetimi ve iskontolar
İskontoların ve fiyatların doğru hesaplandığından garanti etmek için, iskonto içeren tekliflerde fiyat benzetimlerini çalıştırırken dikkatli olmanız gerekir. Tüm fiyat benzetimleri, etkin teklif satırında veya teklifin tamamında özel iskontolar olarak değerlendirildiğinden, iskontolardaki farklılıkları izlemelisiniz.

### <a name="types-of-discounts-in-trade-agreements"></a>Ticaret sözleşmelerindeki iskonto türleri

Microsoft Dynamics 365 for Finance and Operations'daki ticari sözleşmeler, dört türde fiyat indirimine sahip olabilir. Bu iskontolar farklı maddeler, müşteriler veya fiyat grupları için ayarlanabilir ve bunlar için tarih sınırı belirlenebilir. Yanlış hesaplamaları önlemek için fiyat benzetimleri çalıştırdığınızda ticari sözleşmeleri dikkate almanız gerekir. Ticari anlaşmalarda yer alan dört iskonto tipi şunlardır:

-   **Satış fiyatı** – Maddeler için ayrı satış fiyatları belirtilebilir. Teklif satırları oluşturulduğunda, program bir öğe için doğru fiyatı arar ve teklif satırlarına transfer eder. Bu nedenle, bu tür bir indirimi olan bir ticaret anlaşması, fiyat benzetimini etkilemez. Teklif satırında kullanılan satış fiyatı, ticari anlaşmayı yansıtır.
-   **Satır iskontosu** – Özel indirimler sipariş edilen miktara bağlı olarak, maddeler için belirtilir. Fiyat benzetimini çalıştırmadan önce satır tutarları genellikle satır iskontosuna göre azaltılır. Bu nedenle, bu tür bir indirimi olan bir ticaret anlaşması, fiyat benzetimini etkiler.
-   **Çoklu satır indirimi** – Birleştirilmiş miktarlar sizin tanımladığınız sınırı aşarsa, sipariş edilen maddelerin önceden belirlenmiş olan birleşimleri siparişin tamamında bir iskontoyu tetikler. Fiyat benzetimini çalıştırmadan önce satır tutarları genellikle satır iskontosuna göre azaltılır. Bu nedenle, bu tür bir indirimi olan bir ticaret anlaşması, fiyat benzetimini etkiler.
-   **Toplam iskonto** – Birleştirilmiş tutarlar sizin tanımladığınız sınırı aşarsa, sipariş edilen maddelerin önceden belirlenmiş olan siparişin tamamında bir iskontoyu tetikler. Toplam iskonto teklif satırları tarafından oluşturulur. Ancak, toplam iskonto, teklif toplamına iskonto olarak uygulandığından, teklif toplamının miktarını azaltır. Bu nedenle, bu tür bir indirimi olan bir ticaret anlaşması, fiyat benzetimini etkiler.

### <a name="quotation-lines-and-trade-agreements"></a>Teklif satırları ve ticari anlaşmalar

Bir teklif satırını oluşturduğunuzda veya düzenlediğinizde, satır iskontoları otomatik olarak hesaplanır. Madde için ilgili satış fiyatı, ticaret anlaşmasına dayaranak bulunur.

## <a name="price-simulation-examples"></a>Fiyat benzetimi örnekleri
Aşağıdaki örneklerde teklif başlıkları ve tek satırlık maddeler için fiyat benzetimi kullanılır.

### <a name="price-simulation-for-quotation-headers"></a>Teklif başlıkları için fiyat benzetimi

Aşağıdaki satırları içeren bir teklif oluşturursunuz:

-   10 birim BR-12 maddesi (birim başına maliyet fiyatı 9,52 ABD doları ve birim başına satış fiyatı 15,32 ABD doları).
-   12 birim BR-14 maddesi (birim başına maliyet fiyatı 7,48 ABD doları ve birim başına satış fiyatı 13,75 ABD doları).

Aşağıdaki tablo teklif satırlarını göstermektedir.

|                            | Hesaplama                          | Sonuç   |
|----------------------------|--------------------------------------|----------|
| Satış miktarı             | 10 birim + 12 birim                  | 22 birim |
| ABD doları cinsinden satış değeri         | (10 x 15,32) + (12 x 13,75)          | 318,20   |
| ABD doları cinsinden maliyet değeri          | (10 x 9,52) + (12 x 7,48)            | 184,96   |
| ABD doları cinsinden katkı payı | 318,20 – 184,96                      | 133,24   |
| Katkı oranı         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | %41,87   |

Bir fiyat benzetimi çalıştırırsınız ve tüm teklif veya teklif başlığı için yüzde 15'lik bir toplam iskonto uygularsınız. Aşağıdaki tablo, fiyat benzetimi çalıştıktan sonra teklifin yeni toplamlarını gösterir.

|                                                      | Hesaplama                               | Sonuç   |
|------------------------------------------------------|-------------------------------------------|----------|
| Satış miktarı                                       | 10 birim + 12 birim                       | 22 birim |
| ABD doları cinsinden eski satış değeri                               | (10 x 15,32) + (12 x 13,75)               | 318,20   |
| ABD doları cinsinden eski maliyet değeri                                | (10 x 9,52) + (12 x 7,48)                 | 184,96   |
| ABD doları cinsinden eski katkı payı                       | 318,20 – 184,96                           | 133,24   |
| Eski katkı oranı                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | %41,87   |
| Fiyat benzetimi ABD doları cinsinden %15 toplam iskonto | (15 × 318,2) ÷ 100                        | 47,73    |
| ABD doları cinsinden yeni satış değeri                               | 318,20 – 47,73                            | 270,47   |
| ABD doları cinsinden yeni katkı payı                       | 270,47 – 184,96                           | 85,51    |
| Yeni katkı oranı                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | %31,61   |

### <a name="price-simulation-for-single-line-items"></a>Tek satırlık maddeler için fiyat benzetimi

Aşağıdaki satırları içeren bir teklif oluşturursunuz:

-   10 birim BR-12 maddesi (birim başına maliyet fiyatı 9,52 ABD doları ve birim başına satış fiyatı 15,32 ABD doları).
-   12 birim BR-14 maddesi (birim başına maliyet fiyatı 7,48 ABD doları ve birim başına satış fiyatı 13,75 ABD doları).

Aşağıdaki tablo teklif satırlarını göstermektedir.

|                                      | Hesaplama                          | Sonuç   |
|--------------------------------------|--------------------------------------|----------|
| Satış miktarı                       | 10 birim + 12 birim                  | 22 birim |
| BR-12 için ABD doları cinsinden satış değeri         | 10 × 15,32                           | 153,20   |
| BR-14 için ABD doları cinsinden satış değeri         | 12 × 13,75                           | 165,00   |
| BR-12 için ABD doları cinsinden maliyet değeri          | 10 × 9,52                            | 95,20    |
| BR-14 için ABD doları cinsinden maliyet değeri          | 12 × 7,48                            | 89,76    |
| BR-12 için ABD doları cinsinden katkı payı | 153,20 – 95,20                       | 58,00    |
| BR-14 için ABD doları cinsinden katkı payı | 165,00 – 89,76                       | 75,24    |
| BR-12 için ABD doları cinsinden katkı oranı  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| BR-14 için ABD doları cinsinden katkı oranı  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| ABD doları cinsinden toplam satış değeri             | (10 x 15,32) + (12 x 13,75)          | 318,20   |
| ABD doları cinsinden toplam maliyet değeri              | (10 x 9,52) + (12 x 7,48)            | 184,96   |
| ABD doları cinsinden toplam katkı payı     | 318,20 – 184,96                      | 133,24   |
| Toplam katkı oranı             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | %41,87   |

Bir fiyat benzetimi çalıştırırsınız ve BR-12 birimlerine %10 toplam iskonto uygularsınız. Aşağıdaki tablo, fiyat benzetimi tek satırlık madde için çalıştıktan sonra teklifin yeni toplamlarını gösterir.

|                                                   | Hesaplama                             | Sonuç   |
|---------------------------------------------------|-----------------------------------------|----------|
| Satış miktarı                                    | 10 birim + 12 birim                     | 22 birim |
| BR-12 için ABD doları cinsinden eski satış değeri                  | 10 × 15,32                              | 153,20   |
| BR-12 için %10 indirim fiyat benzetimi | (10 × 153,2) ÷ 100                      | 15,32    |
| BR-12 için ABD doları cinsinden yeni satış değeri                  | (10 × 15,32) – 15,32                    | 137,88   |
| BR-14 için ABD doları cinsinden satış değeri                      | 12 × 13,75                              | 165,00   |
| BR-12 için ABD doları cinsinden maliyet değeri                       | 10 × 9,52                               | 95,20    |
| BR-14 için ABD doları cinsinden maliyet değeri                       | 12 × 7,48                               | 89,76    |
| BR-12 için ABD doları cinsinden yeni katkı payı          | 137,88 – 95,20                          | 42,68    |
| BR-14 için ABD doları cinsinden katkı payı              | 165,00 – 89,76                          | 75,24    |
| BR-12 için ABD doları cinsinden yeni katkı oranı           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| BR-14 için ABD doları cinsinden katkı oranı               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| ABD doları cinsinden yeni toplam satış değeri                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| ABD doları cinsinden toplam maliyet değeri                           | (10 x 9,52) + (12 x 7,48)               | 184,96   |
| ABD doları cinsinden yeni toplam katkı payı              | 302,88 – 184,96                         | 117,92   |
| Yeni toplam katkı oranı                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | %38,93   |

Fiyat benzetimi yalnızca uygulandığı satırı etkiler ve bu satırın toplamını düşürür.




