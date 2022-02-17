---
title: Fiziksel değer ve işaretleme ile FIFO
description: İlk Giren İlk Çıkar (FIFO), ilk alınan girişlerin ilk olarak çıkartıldığı bir stok modelidir. Stoktan yapılan mali olarak güncelleştirilen çıkışlar, stok hareketinin mali tarihine göre stoka yapılan ilk mali güncelleştirilen girişlere karşılık kapatılır.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092152"
---
# <a name="fifo-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile FIFO

[!include [banner](../includes/banner.md)]


İlk giren ilk çıkar (FIFO), ilk olarak üretilen veya alınan stoğun ilk satıldığı, kullanıldığı veya ilk elden çıkarıldığı bir stok yönetimi ve değerleme yöntemidir. Microsoft Dynamics 365 Supply Chain Management'ta stok kapanış işlemi sırasında, sistem ilk girişin ilk çıkışla eşleştirileceği, ve diğerlerinin de bu düzende yapılacağı kapanışları oluşturur.

Kapatmalar ve eşleştirme ilkesi, stok hareketlerinin mali tarihine dayanır. Kapatma ve düzeltmelerin ön değerlendirmesi, stok yeniden hesaplama işlemi çalıştırılarak gerçekleştirilebilir.

Stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyerek FIFO ilkesini geçersiz kılabilirsiniz. Kapatma oluşturmak ve çıkışların değerini FIFO ilkesine göre ayarlamak için FIFO stok modelini kullandığınızda periyodik stok kapatma işlemi gerekir. Stok kapatma işlemini çalıştırana kadar çıkış hareketleri fiziksel ve mali güncelleştirmeler gerçekleştiği sırada, değişen ortalamaya göre değerlendirilir. İşaretlemeyi kullanmıyorsanız fiziksel veya mali güncelleştirme gerçekleştirildiğinde çalışma ortalaması hesaplanır. Aşağıdaki örnekler, üç farklı konfigürasyonda FIFO kullanımının etkisini göstermektedir:

- **Fiziksel değeri dahil et** seçeneği olmadan FIFO
- **Fiziksel değeri dahil et** seçeneği ile FIFO
- İşaretleme ile FIFO

## <a name="fifo-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan FIFO

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
- 7\. Stok kapanışı gerçekleştirilir. FIFO yöntemine dayanarak, ilk mali olarak güncelleştirilen çıkış ilk mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Bu örnekte, 1B ve 3B arasında bir kapatma oluşturulur. 3b'de -6,00 ABD doları şeklinde bir ayarlama yapılır ve sonuçta elde edilen nihai maliyet 10,00 ABD doları olur.

Yeni cari ortalama maliyet fiyatı, mali olarak güncelleştirilen hareketlerin ortalamasını yansıtır. Aşağıdaki çizimlerde **Fiziksel değeri dahil et** seçenek kullanılmadığında FIFO stok modelinin bu hareket serisindeki etkilerini gösterir.

![Fiziksel değeri dahil et seçeneği kullanılmadan FIFO.](./media/fifo-without-include-physical-value.png)

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Diyagramdaki her tarih ince siyah bir dikey çizgi ile ayrılır. Tarih, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="fifo-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği ile FIFO

**Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu seçildiğinde, sistem, cari ortalama maliyet fiyatını hesaplamak için hem fiziksel hem de mali giriş hareketlerini kullanır. Uygun olan yerlerde sistem, fiziksel olarak güncelleştirilmiş çıkış hareketinde düzeltmeler de yapar. FIFO stok modelini kullanan stok kapatma işlemi, yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar. Aşağıdaki çizimde şu hareketler gösterilmiştir:

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
- 7\. Stok kapanışı gerçekleştirilir. FIFO yöntemine dayanarak, ilk mali olarak güncelleştirilen çıkış ilk mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Bu örnekte, 1B ve 3B arasında bir kapatma oluşturulur. 3b'de -6,00 ABD doları şeklinde bir ayarlama yapılır ve sonuçta elde edilen nihai maliyet 10,00 ABD doları olur. Ayrıca, hareket 6a, 2b giriş hareketi maliyetine ayarlanacaktır. Giriş mali değil, yalnızca fiziksel olarak güncelleştirildiğinden sistem bu hareketleri kapatmaz. Bunun yerine, fiziksel çıkış hareketine yalnızca -1,67 ABD doları düzeltme nakledilir ve sonuçta elde edilen düzeltilmiş maliyet 22,00 ABD doları olur.

![Fiziksel değeri dahil et seçeneği ile FIFO.](./media/fifo-with-include-physical-value.png)

**Madde modeli grubu** sayfasında **Fiziksel değeri dahil et** seçeneğini belirleyip belirlemediğinize bakılmaksızın, stok kapatma işleminin çalıştırılmasına ilişkin sonucun aynı olduğuna dikkat edin. **Fiziksel değeri dahil et** seçeneği yalnızca, çalışan ortalamayı etkiler.

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Diyagramdaki her tarih ince siyah bir dikey çizgi ile ayrılır. Tarih, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="fifo-with-marking"></a>İşaretleme ile FIFO

İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz.

Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etsin. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak için bu ürün için daha fazla ödemeniz gerekecek. Bu stok maddesinin satış siparişi faturası için marja veya satılan malların maliyetine (COGS) yansıtılacağından emin olmanız gerekiyor. Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Satış siparişi belgesi, sevk irsaliyesi veya fatura nakledilmeden önce satın alma siparişine işaretlenirse, satılan malların maliyeti maddenin cari ortalama maliyeti yerine 120,00 ABD Doları olur. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir. Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir.

Bir giriş hareketi bir çıkış hareketiyle eşleşecek şekilde işaretlendiğinde, ürün modeli grubunda tanımlanan değerlendirme yöntemi göz ardı edilir ve sistem bu hareketleri birbirine karşılık kapatır. **Satış siparişi satırları** hızlı sekmesinde **Stok \> İşaretleme**'yi seçerek **Satış siparişi ayrıntıları** sayfasındaki bir satış siparişi satırına karşı hareketi el ile işaretleyebilirsiniz. Açık giriş hareketlerini **İşaretleme** sayfasında görebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz. Aşağıdaki çizimde bu hareketler gösterilmiştir:

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
- 7\. Stok kapanışı gerçekleştirilir. FIFO yöntemini kullanan işaretleme ilkesine göre, işaretlenen hareketler birbirine karşılık olarak kapatılır. Bu örnekte, 3b, 2b'ye karşılık olarak kapatılır ve değeri 22,00 ABD dolarına getirmek için 3b'ye nakledilen 6,00 ABD doları tutarında bir düzeltme deftere nakledilir. Bu örnekte, hiçbir ek kapatma yapılmaz, çünkü kapanış yalnızca mali olarak güncelleştirilmiş hareketler için kapatma oluşturur.

Aşağıdaki çizimde çıkışlar ve girişler kullanıldığında FIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir.

![İşaretleme ile FIFO.](./media/fifo-with-marking.png)

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Diyagramdaki her tarih ince siyah bir dikey çizgi ile ayrılır. Tarih, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar ve işaretlemeler, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
