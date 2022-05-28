---
title: Fiziksel değer ve işaretleme ile LIFO tarihi
description: Son giren ilk çıkar Tarihi (LIFO tarihi), LIFO ilkesine dayanan bir stok modelidir. Stok çıkışları, stok hareketinin tarihine dayalı olarak son son girişlerine göre kapatılır. LIFO tarihini kullanarak, çıkıştan önce hiçbir giriş yoksa, çıkış, çıkış tarihinden sonraki tüm girişlere karşılık olarak kapatılır. Aynı tarihteki birkaç çıkış son çıkış, son giriş sırasıyla kapatılabilir.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ca344e6ca81814e787046f6ece97625d035346d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671464"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile LIFO tarihi

[!include [banner](../includes/banner.md)]

Son giren ilk çıkar tarihi (LIFO tarihi), ilk olarak üretilen veya alınan stoğun son satıldığı, kullanıldığı veya ilk elden çıkarıldığı bir stok yönetimi ve değerleme yöntemidir. Microsoft Dynamics 365 Supply Chain Management'ta stok kapanış işlemi sırasında, sistem en eski tarihle başlayarak her bir tarih için son girişin ilk çıkışla eşleştirileceği, ve diğerlerinin de bu düzende yapılacağı kapanışları oluşturur. Son giren ilk çıkar tarihi (LIFO tarihi) stok modelini kullandığınızda, çıkıştan önce hiçbir giriş yoksa, çıkış, çıkış tarihinden sonraki tüm girişlere karşılık olarak kapatılır. Kapatmalar ve eşleştirme ilkesi, stok hareketlerinin mali tarihine dayanır. Birden fazla aynı tarihteki çıkış olduğunda; son çıkış, son giriş sırasıyla kapatabilir. Kapatma ve düzeltmelerin ön değerlendirmesi, stok yeniden hesaplama işlemi çalıştırılarak gerçekleştirilebilir.

Stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyerek LIFO tarihi ilkesini geçersiz kılabilirsiniz. Kapatma oluşturmak ve çıkışların değerini LIFO ilkesine göre ayarlamak için LIFO tarihi stok modelini kullandığınızda periyodik stok kapatma işlemi gerekir. Stok kapatma işlemini çalıştırana kadar çıkış hareketleri fiziksel ve mali güncelleştirmeler gerçekleştiği sırada, değişen ortalamaya göre değerlendirilir. İşaretlemeyi kullanmıyorsanız fiziksel veya mali güncelleştirme gerçekleştirildiğinde çalışma ortalaması hesaplanır.

LIFO tarihi stok modelini kullanırken periyodik stok kapatma yapmanızı öneririz.

Aşağıdaki örnekler, üç farklı yapılandırmada LIFO tarihi kullanımının etkisini göstermektedir:

- **Fiziksel değeri dahil et** seçeneği kullanılmadan LIFO tarihi
- **Fiziksel değeri dahil et** seçeneği kullanılarak LIFO tarihi
- İşaretleme ile LIFO tarihi

## <a name="lifo-date-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan LIFO tarihi

Bu örnekte ürün model grubu, fiziksel değeri dahil edecek şekilde işaretlenmemiştir. Aşağıdaki çizimde bu hareketler gösterilmiştir:

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması)
- 7\. Stok kapanışı gerçekleştirilir. LIFO tarihi yöntemine dayanarak, ilk tarihten başlayarak son mali olarak güncelleştirilen çıkış ilk mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Bu örnekte, 3b ve 2b arasında bir kapatma oluşturulur. 3b'de 6,00 ABD doları şeklinde bir ayarlama yapılır ve sonuçta elde edilen nihai maliyet 22,00 ABD doları olur.

Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanılmadığında LIFO tarihi stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir.

![Fiziksel değeri dahil et seçeneği kullanılmadan LIFO tarihi.](media/lifo-date-without-include-physical-value.png)

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Diyagramdaki her tarih ince siyah bir dikey çizgi ile ayrılır. Tarih, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="lifo-date-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılarak LIFO tarihi

**Madde model grupları** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu seçildiğinde, sistem, cari ortalama maliyet fiyatını hesaplamak için hem fiziksel hem de mali giriş hareketlerini kullanır. Uygun olan yerlerde sistem, fiziksel olarak güncelleştirilmiş çıkış hareketinde düzeltmeler de yapar. **Fiziksel değeri dahil et** seçim kutusunun onay işareti kaldırıldığında, LIFO tarihi stok modeli ile stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar.

Bu örnekte ürün model grubu, fiziksel değeri dahil edecek şekilde işaretlenmiştir. 

Aşağıdaki çizimde bu hareketler gösterilmiştir:

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 3b. 16,00 ABD doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,67 ABD doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 7\. Stok kapanışı gerçekleştirilir. LIFO tarihi yöntemine dayanarak, ilk tarihten başlayarak her bir tarih için son mali olarak güncelleştirilen çıkış ilk mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Bu örnekte, 2b ve 3b arasında bir kapatma oluşturulur. 3b'de 6,00 ABD doları şeklinde bir ayarlama yapılır ve sonuçta elde edilen nihai maliyet 22,00 ABD doları olur. Ayrıca, hareket 6a, 5b giriş hareketi maliyetine ayarlanacaktır. Giriş mali değil, yalnızca fiziksel olarak güncelleştirildiğinden sistem bu hareketleri kapatmaz. Bunun yerine, fiziksel çıkış hareketine yalnızca 6,33 ABD doları düzeltme nakledilir ve sonuçta elde edilen düzeltilmiş maliyet 30,00 ABD doları olur.

Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir.

![Fiziksel değeri dahil et seçeneği kullanılarak LIFO tarihi.](media/lifo-date-with-include-physical-value.png)

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Diyagramdaki her tarih ince siyah bir dikey çizgi ile ayrılır. Tarih, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="lifo-date-with-marking"></a>İşaretleme ile LIFO tarihi

İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz. Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etsin. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak için ürün için daha fazla ödemeniz gerekecek.

Bu stok maddesinin satış siparişi faturası için marja veya satılan malların maliyetine (COGS) yansıtılacağından emin olmanız gerekiyor. Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Bu satış siparişi belgesi, sevk irsaliyesi veya fatura nakledilmeden önce satın alma siparişine işaretlenirse, satılan malların maliyeti maddenin cari ortalama maliyeti yerine 120,00 ABD Doları olur. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir.

Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir.

Hareket deftere nakledilmeden önce bir çıkış hareketini bir giriş hareketi için işaretleyebilirsiniz. Bu işaretlemeyi **Satış siparişi satırları** hızlı sekmesinde **Stok \> İşaretleme**'yi seçerek **Satış siparişi ayrıntıları** sayfasındaki bir satış siparişi satırında yapabilirsiniz. Açık giriş hareketlerini **İşaretleme** sayfasında görebilirsiniz.

Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi de işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz.

Aşağıdaki çizimde bu hareketler gösterilmiştir:

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3c. 3b'de stok mali çıkışı, 1b için stok mali çıkışı olarak işaretlenir.
- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması)
- 7\. Stok kapanışı gerçekleştirilir. LIFO tarihi yöntemini kullanan işaretleme ilkesine göre, işaretlenen hareketler birbirine karşılık olarak kapatılır. Bu örnekte, 3b, 1b'ye karşılık olarak kapatılır ve değeri 10,00 ABD dolarına getirmek için 3b'ye nakledilen -6,00 ABD doları tutarında bir düzeltme deftere nakledilir. Bu örnekte, hiçbir ek kapatma yapılmaz, çünkü kapanış yalnızca mali olarak güncelleştirilmiş hareketler için kapatma oluşturur.

Aşağıdaki çizimde, çıkışlar ve girişler arasında işaretleme kullanıldığında LIFO tarihi stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. 

![İşaretleme ile LIFO tarihi.](media/lifo-date-with-marking.png)

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Diyagramdaki her tarih ince siyah bir dikey çizgi ile ayrılır. Tarih, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar ve işaretlemeler, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
