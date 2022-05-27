---
title: Fiziksel değer ve işaretleme ile LIFO
description: Son Giren İlk Çıkar (LIFO), son (en yeni) girişlerin en önce çıkarıldığı bir stok modelidir. Stok çıkışları, stok hareketinin tarihine dayalı olarak son son girişlerine göre kapatılır.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45316c40cce988c0758e70af627b0123ec1f7873
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670454"
---
# <a name="lifo-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile LIFO

[!include [banner](../includes/banner.md)]

Son giren ilk çıkar (LIFO), ilk olarak üretilen veya alınan stoğun son satıldığı, kullanıldığı veya ilk elden çıkarıldığı bir stok yönetimi ve değerleme yöntemidir. Microsoft Dynamics 365 Supply Chain Management'ta stok kapanış işlemi sırasında, sistem son girişin ilk çıkışla eşleştirileceği, ve diğerlerinin de bu düzende yapılacağı kapanışları oluşturur. Kapatmalar ve eşleştirme ilkesi, stok hareketlerinin mali tarihine dayanır. Kapatma ve düzeltmelerin ön değerlendirmesi, stok yeniden hesaplama işlemi çalıştırılarak gerçekleştirilebilir.

Stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyerek LIFO ilkesini geçersiz kılabilirsiniz. Kapatma oluşturmak ve çıkışların değerini LIFO ilkesine göre ayarlamak için LIFO stok modelini kullandığınızda periyodik stok kapatma işlemi gerekir. Stok kapatma işlemini çalıştırana kadar çıkış hareketleri fiziksel ve mali güncelleştirmeler gerçekleştiği sırada, değişen ortalamaya göre değerlendirilir. İşaretlemeyi kullanmıyorsanız fiziksel veya mali güncelleştirme gerçekleştirildiğinde çalışma ortalaması hesaplanır.

Aşağıdaki örnekler, üç farklı konfigürasyonda LIFO kullanımının etkisini göstermektedir:

- **Fiziksel değeri dahil et** seçeneği olmadan LIFO
- **Fiziksel değeri dahil et** seçeneği ile LIFO
- İşaretleme kullanılarak LIFO

## <a name="lifo-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan LIFO

Bu örnekte, serbest bırakılan ürünün madde modeli grubunda **Fiziksel değeri dahil et** onay kutusu temizlenmiş değildir. Aşağıdaki çizimde bu hareketler gösterilmiştir:

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
- 7\. Stok kapanışı gerçekleştirilir. LIFO yöntemine dayanarak, ilk mali olarak güncelleştirilen çıkış son mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Bu örnekte, 5b ve 3b arasında bir kapatma oluşturulur. 3b'de 14,00 ABD doları şeklinde bir ayarlama yapılır ve sonuçta elde edilen nihai maliyet 30,00 ABD doları olur.

Aşağıdaki çizimde, **Fiziksel değeri dahil et** seçeneği kullanılmadığında FIFO stok modelinin bu hareket serisindeki etkileri gösterilmiştir.

![Fiziksel değeri dahil et seçeneği kullanılmadan LIFO.](./media/lifo-without-including-physical-value.png)

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

## <a name="lifo-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılarak LIFO

**Madde model grupları** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu seçildiğinde, sistem, cari ortalama maliyet fiyatını hesaplamak için hem fiziksel hem de mali giriş hareketlerini kullanır. Uygun olan yerlerde sistem, fiziksel olarak güncelleştirilmiş çıkış hareketinde düzeltmeler de yapar. **Fiziksel değeri dahil et** seçim kutusunun onay işareti kaldırıldığında, LIFO stok modeli ile stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar.

Aşağıdaki çizimde şu hareketler gösterilmiştir:

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
- 7\. Stok kapanışı gerçekleştirilir. LIFO yöntemine dayanarak, ilk mali olarak güncelleştirilen çıkış son mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Bu örnekte, 3b ve 5b arasında bir kapatma oluşturulur. 3b'de 14,00 ABD doları şeklinde bir ayarlama yapılır ve sonuçta elde edilen nihai maliyet 30,00 ABD doları olur. Ayrıca, hareket 6a, 4a giriş hareketi maliyetine ayarlanacaktır. Giriş mali değil, yalnızca fiziksel olarak güncelleştirildiğinden sistem bu hareketleri kapatmaz. Bunun yerine, fiziksel çıkış hareketine yalnızca 1,33 ABD doları düzeltme nakledilir ve sonuçta elde edilen düzeltilmiş maliyet 25,00 ABD doları olur.

Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir.

![Fiziksel değeri dahil et seçeneği ile LIFO.](./media/lifo-with-included-physical-value.png)

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

## <a name="lifo-with-marking"></a>İşaretleme ile LIFO

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
- 3c. 3b'de stok mali çıkışı, 2b için stok mali çıkışı olarak işaretlenir.
- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması)
- 7\. Stok kapanışı gerçekleştirilir. LIFO yöntemini kullanan işaretleme ilkesine göre, işaretlenen hareketler birbirine karşılık olarak kapatılır. Bu örnekte, 3b, 2b'ye karşılık olarak kapatılır ve değeri 22,00 ABD dolarına getirmek için 3b'ye nakledilen 6,00 ABD doları tutarında bir düzeltme deftere nakledilir. Bu örnekte, hiçbir ek kapatma yapılmaz, çünkü kapanış yalnızca mali olarak güncelleştirilmiş hareketler için kapatma oluşturur.

Yeni cari ortalama maliyet fiyatı 27.50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır.

Aşağıdaki çizimde çıkışlar ve girişler kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir.

![İşaretleme ile LIFO.](./media/lifo-with-marking.png)

**Diyagram anahtarı**

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
