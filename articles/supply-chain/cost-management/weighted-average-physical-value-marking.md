---
title: Fiziksel değer ve işaretleme ile ağırlıklı ortalama
description: Ağırlıklı ortalama, stoktaki çıkışların stok kapanış dönemi sırasında stokta ve önceki dönemdeki eldeki stoklarda girişi yapılan maddelerin ortalama değeri ile değerlendirildiği ortalama ağırlık ilkesine dayanan bir stok modelidir.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c80dcdc08432bb68478827c8763735e644aa4a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675305"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile ağırlıklı ortalama

[!include [banner](../includes/banner.md)]

Ağırlıklı ortalama, her bileşenin çarpanıyla (madde hareketi), önemini (maliyet fiyatı) bir faktörden (miktar) yansıtılırken elde edilen ortalamayı esas alan bir stok modelidir. Yani başka bir deyişle ağırlıklı ortalama, dönem içinde alınan tüm stokun ortalama değerine ve önceki dönemden elde edilen tüm stoka dayalı olarak çıkış hareketlerinin maliyetini atayan bir stok modelidir.

Ağırlıklı ortalama stok modelini kullanarak bir stok kapanışı gerçekleştirdiğinizde, bir kapatmanın oluşturulabileceği iki yol vardır. Tipik olarak, tüm girişler alınan toplam miktarı ve değeri kapsayan bir sanal çıkışa karşı kapatılır. Bu sanal çıkışın, çıkışların kapatılmasını sağlayan bir karşılık gelen sanal girişi bulunmaktadır. Bu şekilde, tüm çıkışlar aynı ortalama maliyeti alacaktır. Sanal çıkış ve giriş *ağırlıklı ortalama stok kapanışı transferi* olarak adlandırılan bir sanal transfer olarak görülebilir. Bu kapatma yöntemine *ağırlıklı ortalama özetlenmiş kapatma* denir. Yalnızca tek bir giriş varsa, tüm çıkışlar bundan kapatılabilir ve sanal transfer oluşturulamaz. Bu kapatma yöntemine, *doğrudan kapatma* adı verilir. Stok kapanışı gerçekleştirildikten sonra elde olan tüm stoklar önceki dönemden ağırlıklı ortalamaya göre değerlendirilir ve sonraki dönemdeki ağırlıklı ortalama hesaplamaya dahil edilir.

Stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyerek ağırlıklı ortalama ilkesini geçersiz kılabilirsiniz. Kapatma oluşturmak ve çıkışların değerini ağırlıklı ortalama ilkesine göre ayarlamak için ağırlıklı ortalama stok modelini kullandığınızda periyodik stok kapatma işlemi gerekir. Stok kapatma işlemini çalıştırana kadar çıkış hareketleri fiziksel ve mali güncelleştirmeler gerçekleştiği sırada, değişen ortalamaya göre değerlendirilir. İşaretlemeyi kullanmıyorsanız fiziksel veya mali güncelleştirme gerçekleştirildiğinde çalışma ortalaması hesaplanır.

Ağırlıklı ortalama stok kapanışı yöntemi aşağıdaki formüle göre hesaplanır:

- Ağırlıklı ortalama = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q= hareketin miktarı  
P = hareketin fiyatı

Kapatmalar, kapanış tarihin ağırlıklı ortalamasını düzeltmek için çıkışları ayarlayan stok kapanışı deftere nakilleridir. Aşağıdaki örnekler, beş farklı yapılandırma ile ağırlıklı ortalama kullanmanın etkisini gösterir:

- **Fiziksel değeri dahil et** seçeneği olmadan ağırlıklı ortalama doğrudan kapatma
- **Fiziksel değeri dahil et** seçeneği kullanılmadan ağırlıklı ortalama özetlenmiş kapatma
- **Fiziksel değeri dahil et** seçeneği ile ağırlıklı ortalama doğrudan kapatma
- **Fiziksel değeri dahil et** seçeneği ile ağırlıklı ortalama özetlenmiş kapatma
- İşaretleme ile ağırlıklı ortalama

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama doğrudan kapatma

Doğrudan kapatma ilkesi, ek stok hareketleri oluşturmadan doğrudan girişler ve sorunlar arasında kapatma işlemi oluşturur. Sistem bu doğrudan kapatma ilkesini aşağıdaki durumlarda kullanır:

- Dönem içinde bir giriş ve bir veya daha çok çıkış deftere nakledildiğinde.
- Dönem içinde yalnızca çıkışlar deftere nakledildiğinde ve stok önceki kapanıştan eldeki maddeleri içerdiğinde.

Bu örnekte, serbest bırakılan ürünün **Madde modeli grubunda** **Fiziksel değeri dahil et** onay kutusu temizlenmiş değildir. Aşağıdaki çizimde bu hareketler gösterilmiştir:

- 1a. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 3a. 10,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 10,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 4a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 4b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 5a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 6\. Stok kapanışı gerçekleştirilir. Dönem içinde mali olarak yalnızca tek bir makbuz güncelleştirildiği için sistem, ağırlıklı ortalama yöntemine dayalı olarak doğrudan kapatma yöntemini kullanır. Bu örnekte, 1B ve 3B arasında ve 1b ile 4b arasında bir kapatma oluşturulur. Çalışma ortalaması ağırlıklı ortalamaya eşit olduğu için herhangi bir düzeltme yapılmaz.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil** et seçeneği kullanılmadan doğrudan kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği Kullanılmadan WeightedAverage DS.](media/weighted-average-direct-settlement-without-include-physical-value.png)

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
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama özetlenmiş kapatma

Bir dönemde birden fazla makbuz olduğunda ağırlıklı ortalama, kapanış dönemi dahilindeki tüm girişlerin *ağırlıklı ortalama stok kapanışı* denilen bir harekette özetlendiği bir özetlenmiş kapatma ilkesini kullanır. Dönemdeki tüm girişler, yeni oluşturulan stok hareketinin çıkışına karşılık kapatılır. Dönemin tüm çıkışları, yeni stok hareketinin girişine karşılık kapatılır. Stok kapanmasından sonra elde kalan stok değeri varsa, eldeki stok değeri, ağırlıklı ortalama stok kapatma hareketlerinin makbuz hareketine dahil edilir.

Aşağıdaki hareketler, aşağıdaki grafikte gösterilmektedir:

- 1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 2b. Her biri 22,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 3a. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 3b. 16,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 4a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
- 5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 7\. Stok kapanışı gerçekleştirilir.
- 7a. Tüm stok mali girişlerinin kapatmalarını toplamak için Ağırlıklı ortalama stok kapanışı hareketi mali çıkışı oluşturulur.
  - 1B hareketi, 10,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
  - 2B hareketi, 22,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
  - 5B hareketi, 30,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
  - Hareket 7a. 62,00 USD değerinde kapatılan tutarla 3 miktarı için kapatılır. Bu hareket, dönemde mali olarak güncelleştirilen üç giriş hareketinin toplamını kaydırır.
- 7b. Mali olarak deftere nakledilmiş çıkış için mahsup olarak ağırlıklı ortalama stok kapanış hareketi mali girişi oluşturulur.
  - 3B hareketi, 20,67 USD değerinde kapatılan tutarla 1 miktarı için kapatılır. Bu hareket, dönem için mali olarak deftere nakledilen hareketlerin ağırlıklı ortalaması olan 16,00 USD orijinal değerini 20,67'ye getirmek için 4,67 USD tarafından düzeltilir.
  - Hareket 7b. 3b'yi denkleştirmek üzere 20,67 USD değerinde kapatılan tutarla 1 miktarı için kapatılır. Bu hareket, dönemde mali olarak güncelleştirilen bir çıkış hareketinin toplamını kaydırır.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil et** seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği kullanılmadan Ağırlıklı Ortalama SS.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

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
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama doğrudan kapatma

**Fiziksel değeri dahil et** parametresi ağırlıklı ortalama stok modeli ile, ürünün daha eski sürümlerinde olduğundan farklı şekilde çalışır. **Madde model grubu** formundaki bir madde için **Fiziksel değeri dahil et** seçeneğini işaretlediğinizde sistem, cari ortalama maliyet fiyatını ve tahmini çıkış maliyet fiyatını hesaplamak için fiziksel olarak güncelleştirilmiş girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatına dayanarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır.

Aşağıdaki hareketler, aşağıdaki grafikte gösterilmektedir:

- 1a. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 1b. Her biri 10,00 ABD Doları maliyetinde 10 miktarındaki stok mali girişi.
- 2a. Her biri 20,00 ABD Doları maliyetinde 10 miktarındaki stok fiziksel girişi.
- 3a. 15,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 3b. 15,00 ABD doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 4a. Her biri 15,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 4b. Her biri 15,00 ABD doları maliyetinde 1 miktarındaki stok mali çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 5a. Her biri 15,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel çıkışı (fiziksel ve mali olarak deftere nakledilmiş hareketlerin cari ortalaması).
- 6\. Stok kapanışı gerçekleştirilir. Dönem içinde mali olarak yalnızca tek bir makbuz güncelleştirildiği için sistem, ağırlıklı ortalama yöntemine dayalı olarak doğrudan kapatma yöntemini kullanır. Bu örnekte, 1B ve 3B arasında ve 1b ile 4b arasında bir kapatma oluşturulur. Hareket 3B ve 4B, her biri değeri 10,00 USD değerine getirmek için -5,00 USD tarafından düzeltilir.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil et** seçeneği ile doğrudan kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama DS.](media/weighted-average-direct-settlement-with-include-physical-value.png)

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
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama özetlenmiş kapatma

**Fiziksel değeri dahil et** parametresi, ağırlıklı ortalamayla, daha eski sürümlerdekinden farklı şekilde çalışır. **Madde modeli grubu** sayfasında bir madde için **Fiziksel değeri dahil et** onay kutusunu seçin. Ardından sistem tahmini maliyet fiyatını veya cari ortalamayı hesaplarken fiziksel olarak güncelleştirilen girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatına dayanarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır. Ağırlıklı ortalama stok modelini kullanırken aylık bir stok kapanışı öneririz. Bu ağırlıklı ortalama özetlenmiş kapatma örneğinde, stok modeli grubu fiziksel değeri içerecek şekilde işaretlenmiştir.

Aşağıdaki hareketler, aşağıdaki grafikte gösterilmektedir:

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
- 7\. Stok kapanışı gerçekleştirilir.
- 7a. Tüm stok mali girişlerinin kapatmalarını toplamak için Ağırlıklı ortalama stok kapanışı hareketi mali çıkışı oluşturulur.
  - 1B hareketi, 10,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
  - 2B hareketi, 22,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
  - 5B hareketi, 30,00 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.
  - Hareket 7a. 62,00 USD değerinde kapatılan tutarla 3 miktarı için kapatılır.  
- 7b. Mali olarak kapatılmış çıkış hareketleri için mahsup olarak ağırlıklı ortalama stok kapanış hareketi mali girişi oluşturulur.
  - 3B hareketi, 20,67 USD değerinde kapatılan tutarla 1 miktarı için kapatılır. Bu hareket, dönem için mali olarak deftere nakledilen hareketlerin ağırlıklı ortalaması olan 16,00 USD orijinal değerini 20,67'ye getirmek için 4,67 USD tarafından düzeltilir.
  - Hareket 7b. 3b'yi denkleştirmek üzere 20,67 USD değerinde kapatılan tutarla 1 miktarı için kapatılır.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil et** seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir.

![Fiziksel değeri dahil et seçeneği ile WeightedAverage SS.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

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
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="weighted-average-with-marking"></a>İşaretleme ile ağırlıklı ortalama

İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz.

Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etti. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak üzere bu madde için daha fazla ödemeniz gerekecek. Bu stok maddesinin bu satış emri faturası için marja veya satılan malların maliyetine yansıtılacağından emin olmanız gerekir.

Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Örneğin, bu satış emri belgesi satınalma emrine sevk irsaliyesi veya fatura deftere nakledilmeden önce işaretlenmiştir. Ardından SMM, maddenin cari ortalama maliyeti yerine 120,00 ABD doları olacaktır. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir.

Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir.

Bir giriş hareketi bir çıkış hareketine işaretlenir. Ardından, maddenin madde modeli grubu için seçilen değerlendirme yöntemi göz ardı edilir ve sistem bu hareketleri birbirine karşılık kapatır.

Hareket deftere nakledilmeden önce bir çıkış hareketini bir giriş hareketi için işaretleyebilirsiniz. Bunu **Satış siparişi bilgileri** sayfasındaki bir satış siparişi satırından yapabilirsiniz. Açık giriş hareketleri, **İşaretleme** sayfasında görüntülenebilir.

Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz.

Aşağıdaki hareketler, aşağıdaki grafikte gösterilmektedir:

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
- 6a. 23,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak deftere nakledilen hareketlerin cari ortalaması).
- 7\. Stok kapanışı gerçekleştirilir. Ağırlıklı ortalama yöntemini kullanan işaretleme ilkesine göre, işaretlenen hareketler birbirine karşılık olarak kapatılır. Bu örnekte, 3b, 2b'ye karşılık olarak kapatılır ve değeri 22,00 ABD dolarına getirmek için 3b'ye nakledilen 6,00 ABD doları tutarında bir düzeltme deftere nakledilir. Bu örnekte, hiçbir ek kapatma yapılmaz çünkü kapanış yalnızca mali olarak güncelleştirilmiş hareketler için kapatma oluşturur.

Aşağıdaki diyagram bu hareketler serisini, işaretleme ile ağırlıklı ortalama stok modeli seçmenin etkileriyle birlikte gösterir.

![İşaretleme ile Ağırlıklı Ortalama.](media/weighted-average-with-marking.png)

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
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
