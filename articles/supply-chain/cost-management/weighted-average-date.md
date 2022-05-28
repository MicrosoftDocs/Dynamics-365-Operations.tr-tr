---
title: Fiziksel değer ve işaretlemeyi dahil et ile ağırlıklı ortalama tarihi
description: Ağırlıklı ortalama tarihi, stoktan çıkışların stok kapatma dönemindeki her ayrı gün için stoka girişi yapılan maddelerin ortalama değeriyle değerlendirildiği ağırlıklı ortalama ilkesini temel alan bir stok modelidir.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672136"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Fiziksel değer ve işaretlemeyi dahil et ile ağırlıklı ortalama tarihi

[!include [banner](../includes/banner.md)]

*Ağırlıklı ortalama tarihi*, her bileşenin çarpanıyla (madde hareketi) önemini (maliyet fiyatı) yansıtan bir faktörle (miktar) çarpılmasıyla hesaplanan bir stok modelidir. Yani başka bir deyişle ağırlıklı ortalama, her gün alınan tüm stokun ortalama değerine ve önceki dönemden elde edilen tüm stoka dayalı olarak çıkış hareketlerinin maliyetini atayan bir stok modelidir.

Ağırlıklı ortalama tarih stok modelini kullanarak bir stok kapanışı gerçekleştirdiğinizde, bir kapatmanın oluşturulabileceği iki yol vardır. Tipik olarak, tüm girişler alınan toplam miktarı ve değeri kapsayan bir sanal çıkışa karşı kapatılır. Bu sanal çıkışın, çıkışların kapatılmasını sağlayan bir karşılık gelen sanal girişi bulunmaktadır. Bu şekilde, tüm çıkışlar her gün aynı ortalama maliyeti alacaktır. Sanal sorun ve sanal giriş, sanal bir aktarım olarak kabul edilebilir. Bu sanal transfer, *ağırlıklı ortalama stok kapanış transferi* olarak anılır. Bu nedenle, Bu kapatma yöntemine *ağırlıklı ortalama özetlenmiş kapatma* denir. Yalnızca tek bir giriş varsa, tüm çıkışlar bundan kapatılabilir ve sanal transfer oluşturulamaz. Bu kapatma yöntemine, *doğrudan kapatma* adı verilir. Stok kapanışı gerçekleştirildikten sonra elde olan tüm stoklar önceki dönemin son gününden ağırlıklı ortalama tarihe göre değerlendirilir ve sonraki dönemdeki ağırlıklı ortalama hesaplamaya dahil edilir.

Stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyerek ağırlıklı ortalama tarihi ilkesini geçersiz kılabilirsiniz. Kapatma oluşturmak ve çıkışların değerini ağırlıklı ortalama tarihi ilkesine göre ayarlamak için ağırlıklı ortalama tarihi stok modelini kullandığınızda periyodik stok kapatma işlemi gerekir. Stok kapatma çalıştırana kadar çıkış hareketleri fiziksel ve mali güncelleştirmeler gerçekleştiği sırada, değişen ortalamaya göre değerlendirilir. İşaretlemeyi kullanmıyorsanız fiziksel veya mali güncelleştirme gerçekleştirildiğinde çalışma ortalaması hesaplanır.

Ağırlıklı ortalama tarihi stok kapanışı yöntemi her gün aşağıdaki formüle göre hesaplanır:

*Maliyet* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = Hareketin miktarı
- *P* = Hareketin fiyatı

Başka bir deyişle, ağırlıklı ortalama maliyet, başlangıç fiyatı çarpı başlangıç miktarı artı her bir girdi miktarı çarpı giriş fiyatı toplamının giriş miktarı artı giriş miktarlarına bölünmesiyle bulunur.

Stok kapatma sırasında, hesaplama her gün kapanış dönemi boyunca gerçekleştirilir.

> [!NOTE]
> Kapatmalar hakkında daha fazla bilgi için bkz. [Stok kapatma](inventory-close.md).

Aşağıdaki örnekler, beş yapılandırma ile ağırlıklı ortalama tarih kullanmanın etkisini gösterir:

- **Fiziksel değeri dahil et** seçeneği kullanılmadan ağırlıklı ortalama tarihi doğrudan kapatma
- **Fiziksel değeri dahil et** seçeneği kullanılmadan ağırlıklı ortalama tarihi özetlenmiş kapatma
- **Fiziksel değeri dahil et** seçeneği kullanıldığında ağırlıklı ortalama tarihi doğrudan kapatma
- **Fiziksel değeri dahil et** seçeneği kullanıldığında ağırlıklı ortalama tarihi özetlenmiş kapatma
- İşaretleme kullanıldığında ağırlıklı ortalama tarihi

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Fiziksel değeri dahil et seçeneği kullanılmadığında ağırlıklı ortalama tarihi doğrudan kapatma

Doğrudan kapatma ilkesi, ek stok hareketleri oluşturmadan doğrudan girişler ve sorunlar arasında kapatma işlemi oluşturur. Sistem bu doğrudan kapatma ilkesini aşağıdaki durumlarda kullanır:

- Dönem içinde bir giriş ve bir veya daha çok çıkış deftere nakledildiğinde.
- Dönem içinde yalnızca çıkışlar deftere nakledildiğinde ve stok önceki kapanıştan eldeki maddeleri içerdiğinde.

Bu örnekte, serbest bırakılan ürünün **Madde modeli grubu** sayfasında **Fiziksel değeri dahil et** onay kutusu temizlenmiş değildir. Aşağıdaki diyagramda bu hareketler gösterilmiştir:

**1. Gün:**

- 1a. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 3a. 10,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 10,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).

**2. Gün:**

- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).

**3. Gün:**

- 7\. Stok kapanışı gerçekleştirilir. 30 Aralık (12/30) için mali olarak yalnızca tek bir makbuz güncelleştirildiği için sistem, 12/30'da ağırlıklı ortalama tarih yöntemine dayalı olarak doğrudan kapatma yöntemini kullanır. Bu örnekte, 1B ve 3B hareketleri arasında bir kapatma oluşturulur. 3b hareketinin değerini 20,00'a getirecek bir 10,00 ABD doları değerinde düzeltme yapılır. 31 Aralık'ta (12/31) hiçbir düzeltme veya kapatma işlemi yapılmaz, çünkü 12/31 üzerinde mali olarak güncelleştirilmiş bir sorun yoktur.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil** et seçeneği kullanılmadan doğrudan kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama tarihi doğrudan kapatma.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Diyagramın anahtarı:**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Tarihler, ince siyah dikey çizgilerle ayrılır. Tarihler, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgilerle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama tarihi özetlenmiş kapatma

Bir dönemde birden fazla makbuz olduğunda ağırlıklı ortalama tarihi, tek bir gün dahilindeki tüm girişlerin *ağırlıklı ortalama stok kapanışı* denilen bir harekette özetlendiği bir özetlenmiş kapatma ilkesini kullanır. Gündeki tüm girişler, yeni oluşturulan stok hareketinin çıkışına karşılık kapatılır. Günün tüm çıkışları, yeni stok hareketinin girişine karşılık kapatılır. Stok kapanmasından sonra elde kalan stok değeri varsa, eldeki stok değeri, ağırlıklı ortalama stok kapatma hareketlerinin makbuz hareketine dahil edilir.

Aşağıdaki diyagramda bu hareketler gösterilmiştir:

**1. Gün:**

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).

**2. Gün:**

- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).

**3. Gün:**

- 7\. Stok kapanışı gerçekleştirilir.
- 7a. Tüm stok mali girişlerinin kapatmalarını toplamak için Ağırlıklı ortalama stok kapanışı hareketi mali çıkışı oluşturulur.

    - 1B hareketi, 10,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
    - 2B hareketi, 22,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
    - 7A hareketi, 32,00 USD değerinde kapatılan tutarla 2 miktarı için oluşturulur. Bu hareket, dönemde mali olarak güncelleştirilen iki giriş hareketinin toplamını kaydırır.

- 7b. Mali olarak deftere nakledilmiş çıkış için mahsup olarak ağırlıklı ortalama stok kapanış hareketi mali girişi oluşturulur.

    - 3B hareketi, 16,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır. 1 Aralık'ta (12/1) mali olarak deftere nakledilen hareketlerin ağırlıklı ortalaması olduğundan bu hareket düzeltilmemiştir.
    - 7B hareketi, 32,00 USD mali tutarıyla 2 miktarı ile mahsup hareket 3b'ye kapatılmış bir 16,00 USD tutarı için oluşturulur. Bu hareket, dönemde mali olarak güncelleştirilen bir çıkış hareketinin toplamını kaydırır. Hala bir tane elde olduğu için hareket açık kalır.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil et** seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama tarihi özetlenmiş kapatma.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Diyagramın anahtarı:**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Tarihler, ince siyah dikey çizgilerle ayrılır. Tarihler, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgilerle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Fiziksel değeri dahil et seçeneği kullanıldığında ağırlıklı ortalama tarihi doğrudan kapatma

Ürünün geçerli sürümünde, **Fiziksel değeri dahil et** seçeneği ağırlıklı ortalama tarihi stok modeli ile, ürünün daha eski sürümlerinde olduğundan farklı şekilde çalışır. **Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu işaretlenirse, sistem, cari ortalama maliyet fiyatını ve tahmini giriş maliyet fiyatını hesaplamak için fiziksel olarak güncelleştirilmiş girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatına dayanarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır.

Aşağıdaki diyagramda bu hareketler gösterilmiştir:

**1. Gün:**

- 1a. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 3a. 15,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 3b. 15,00 ABD doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).

**2. Gün:**

- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. Her biri 21,25 ABD Doları maliyetinde 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).

**3. Gün:**

- 7\. Stok kapanışı gerçekleştirilir. 30 Aralık (12/30) için mali olarak yalnızca tek bir makbuz güncelleştirildiği için sistem, 12/30'da ağırlıklı ortalama tarih yöntemine dayalı olarak doğrudan kapatma yöntemini kullanır. Bu örnekte, 1B ve 3B hareketleri arasında bir kapatma oluşturulur. 12/30 tarihinde ilgili girişte herhangi bir düzeltme yapılmaz. Ek olarak, 31 Aralık'ta (12/31) hiçbir düzeltme veya kapatma işlemi yapılmaz, çünkü 12/31 üzerinde mali olarak güncelleştirilmiş bir sorun yoktur.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil** et seçeneği kullanılarak doğrudan kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği kullanılarak ağırlıklı ortalama doğrudan kapatma.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Diyagramın anahtarı:**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Tarihler, ince siyah dikey çizgilerle ayrılır. Tarihler, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgilerle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Fiziksel değeri dahil et seçeneği kullanıldığında ağırlıklı ortalama tarihi özetlenmiş kapatma

Ürünün geçerli sürümünde, **Fiziksel değeri dahil et** seçeneği ağırlıklı ortalama ile, ürünün daha eski sürümlerinde olduğundan farklı şekilde çalışır. **Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu işaretlenirse, sistem, cari ortalama maliyet fiyatını ve tahmini maliyet fiyatını hesaplamak için fiziksel olarak güncelleştirilmiş girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatına dayanarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır. Ağırlıklı ortalama stok modelini kullanırken aylık bir stok kapanışı gerçekleştirmenizi öneririz. Bu ağırlıklı ortalama tarihi özetlenmiş kapatma örneğinde, stok modeli grubu fiziksel değeri içerecek şekilde işaretlenmiştir.

Aşağıdaki diyagramda bu hareketler gösterilmiştir:

**1. Gün:**

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 3b. 16,00 ABD doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).

**2. Gün:**

- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,67 ABD doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).

**3. Gün:**

- 7\. Stok kapanışı gerçekleştirilir.
- 7a. Tüm stok mali girişlerinin kapatmalarını toplamak için Ağırlıklı ortalama stok kapanışı hareketi mali çıkışı oluşturulur.

    - 1B hareketi, 10,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
    - 2B hareketi, 22,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
    - 7A hareketi, 32,00 USD değerinde kapatılan tutarla 2 miktarı için oluşturulur. Bu hareket, dönemde mali olarak güncelleştirilen iki giriş hareketinin toplamını kaydırır.

- 7b. Mali olarak deftere nakledilmiş çıkış için mahsup olarak ağırlıklı ortalama stok kapanış hareketi mali girişi oluşturulur.

    - 3B hareketi, 16,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır. 1 Aralık'ta (12/1) mali olarak deftere nakledilen hareketlerin ağırlıklı ortalaması olduğundan bu hareket düzeltilmemiştir.
    - 7B hareketi, 32,00 USD mali tutarıyla 2 miktarı ile mahsup hareket 3b'ye kapatılmış bir 16,00 USD tutarı için oluşturulur. Bu hareket, dönemde mali olarak güncelleştirilen bir çıkış hareketinin toplamını kaydırır. Hala bir tane elde olduğu için hareket açık kalır.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil** et seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et ile ağırlıklı ortalama özetlenmiş kapatma.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Diyagramın anahtarı:**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Tarihler, ince siyah dikey çizgilerle ayrılır. Tarihler, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgilerle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-date-when-marking-is-used"></a>İşaretleme kullanıldığında ağırlıklı ortalama tarihi

İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz.

Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etti. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak üzere bu madde için daha fazla ödemeniz gerekecek. Bu stok maddesinin bu satış siparişi faturası için marja veya satılan malların maliyetine (COGS) yansıtılacağından emin olmanız gerekiyor.

Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Satış siparişi belgesi, sevk irsaliyesi veya fatura nakledilmeden önce satın alma siparişine işaretlenirse, satılan malların maliyeti maddenin cari ortalama maliyeti yerine 120,00 USD olur. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir.

Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir.

Bir giriş hareketi bir çıkış hareketiyle eşleşecek şekilde işaretlenirse, ürün modeli grubunda tanımlanan değerlendirme yöntemi göz ardı edilir ve sistem bu hareketleri birbirine karşılık kapatır.

Hareket deftere nakledilmeden önce bir çıkış hareketini bir giriş hareketi için işaretleyebilirsiniz. Bu işaretlemeyi **Satış siparişi bilgileri** sayfasındaki bir satış siparişi satırından yapabilirsiniz. Açık giriş hareketleri, **İşaretleme** sayfasında görüntülenebilir.

Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi de işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz.

Aşağıdaki diyagramda bu hareketler gösterilmiştir:

**1. Gün:**

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3c. 3b hareketinde stok mali çıkışı, 2b hareketi için stok mali çıkışı olarak işaretlenir.

**2. Gün:**

- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).

**3. Gün:**

- 7\. Stok kapanışı gerçekleştirilir. Ağırlıklı ortalama yöntemini kullanan işaretleme ilkesine göre, işaretlenen hareketler birbirine karşılık olarak kapatılır. Bu örnekte, 3b hareketi, 2b hareketine karşılık olarak kapatılır ve değeri 22,00 ABD dolarına getirmek için 3b hareketine nakledilen 6,00 ABD doları tutarında bir düzeltme deftere nakledilir. Bu örnekte, hiçbir ek kapatma yapılmaz çünkü kapanış yalnızca mali olarak güncelleştirilmiş hareketler için kapatma oluşturur.

Aşağıdaki diyagramda bu hareketler serisini, işaretleme ve ağırlıklı ortalama stok modeli kullanmanın etkilerini gösterir.

![İşaretleme ile ağırlıklı ortalama.](media/weighted-average-date-with-marking.png)

**Diyagramın anahtarı:**

- Stok hareketleri dikey oklarla temsil edilir.
- Fiziksel hareketler, daha kısa, açık gri oklarla gösterilir.
- Mali hareketler, daha uzun siyah oklarla gösterilir.
- Stoka yapılan girişler eksen üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar eksen altında dikey oklarla temsil edilir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Tarihler, ince siyah dikey çizgilerle ayrılır. Tarihler, diyagramın alt kısmında belirtilmiştir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgilerle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
