---
title: Ağırlıklı ortalama tarihi
description: Ağırlıklı ortalama tarihi, stoktan çıkışların stok kapatma dönemindeki her ayrı gün için stoka girişi yapılan maddelerin ortalama değeriyle değerlendirildiği ağırlıklı ortalama ilkesini temel alan bir stok modelidir.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9963c17d8ac1854a42cac2a0e19615f13e8cc006
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543641"
---
# <a name="weighted-average-date"></a>Ağırlıklı ortalama tarihi

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Ağırlıklı ortalama tarihi, ağırlıklı ortalama ilkesini temel alan bir stok modelidir. Ağırlıklı ortalama ilkesi için, stoktan yapılan çıkışlar, stok kapanış döneminde her gün stoğa alınan maddelerin ortalama değerinden değerlenir. 

Ağırlıklı ortalama tarihi kullanarak stok kapanışı çalıştırdığınızda, tüm günlük girişler bir sanal bir çıkışa karşılık kapatılır. Bu sanal çıkış o güne ilişkin toplam alınan miktarı ve değeri tutar. Sanal çıkış, çıkışların kapatılacağı karşılık gelen bir sanal girişe sahiptir. Bu nedenle, tüm çıkışlar aynı ortalama maliyeti alır. Sanal çıkış ve sanal giriş, *ağırlıklı ortalama stok kapatma transferi* olarak bilinen sanal bir transfer olarak görülebilir. 

Bu tarihte veya bu tarihten önce yalnızca bir giriş gerçekleştiyse, ortalamayı değerlemeniz gerekmez. Tüm çıkışlar bu girişten kapatılacağından, sanal transfer oluşturulmaz. Benzer şekilde, o tarihte yalnızca çıkışlar oluşursa, ortalamanın değerlendirileceği bir giriş yoktur ve sanal transfer oluşturulmayacaktır. Ağırlıkı ortalama tarihini kullandığınızda, stok hareketlerini belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyebilirsiniz. Bu durumda, ağırlıklı ortalama tarihi kuralı kullanılmaz. Ağırlıklı ortalama tarihi stok modelini kullanırken aylık stok kapatma yapmanızı öneririz. 

Aşağıdaki formül, ağırlıklı ortalama tarih stok kapanış yöntemini hesaplamada kullanılır: 

Ağırlıklı ortalama = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) 

Stok kapatma sırasında, hesaplama aşağıdaki görselde gösterildiği gibi, her gün kapanış dönemi boyunca gerçekleştirilir. 

![Ağırlıklı ortalama tarihi günlük hesaplama modeli](./media/weightedaveragedatedailycalculationmodel.gif) 

Satış siparişleri, stok günlükler ve üretim emirleri gibi stoktan ayrılan stok hareketleri deftere nakil tarihinde tahmini maliyet fiyatından gerçekleştirilir. Tahmini maliyet fiyatı, yürütülen ortalama maliyet fiyatı olarak da bilinir. Stok kapanış tarihinde, sistem önceki dönemlere, önceki güne ve geçerli güne ait stok hareketlerini inceler. Bu analiz, aşağıdaki kapanış ilkelerinden hangisinin kullanılacağını belirlemek için kullanılır:

-   Doğrudan kapatma
-   Özetlenmiş kapatma

Kapatmalar, kapanış tarihin ağırlıklı ortalamasını düzeltmek için çıkışları ayarlayan stok kapanışı deftere nakilleridir. 

**Not:** Kapatma işlemleri hakkında daha fazla bilgi için stok kapatmayla ilgili makaleye bakın. Aşağıdaki örnekler, beş yapılandırma ile ağırlıklı ortalama kullanmanın etkisini gösterir:

-   **Fiziksel değeri dahil et** seçeneği kullanılmadan ağırlıklı ortalama tarihi doğrudan kapatma
-   **Fiziksel değeri dahil et** seçeneği kullanılmadan ağırlıklı ortalama tarihi özetlenmiş kapatma
-   **Fiziksel değeri dahil et** seçeneği kullanıldığında ağırlıklı ortalama tarihi doğrudan kapatma
-   **Fiziksel değeri dahil et** seçeneği kullanıldığında ağırlıklı ortalama tarihi özetlenmiş kapatma
-   İşaretleme kullanıldığında ağırlıklı ortalama tarihi

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Fiziksel değeri dahil et seçeneği kullanılmadığında ağırlıklı ortalama tarihi doğrudan kapatma
Geçerli sürüm, önceki sürümlerde kullanılan ağırlıklı ortalamayla aynı kapatma ilkesini kullanır. Sistem giriş ve çıkışlar arasında doğrudan kapatma yapar. Sistem bu doğrudan kapatma ilkesini belirli durumlarda kullanır:

-   Dönem içinde bir giriş ve bir veya daha fazla çıkış deftere nakledildiğinde.
-   Dönem içinde yalnızca çıkışlar deftere nakledildiğinde ve stok önceki kapanıştan eldeki maddeleri içerdiğinde.

Aşağıdaki senaryoda, mali olarak güncelleştirilmiş giriş ve çıkış deftere nakledilmiştir. Stok kapanışı sırasında, sistem girişi doğrudan çıkışa karşılık kapatır ve çıkışta maliyet fiyatı için bir ayarlama yapılması gerekmez. 

Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetindeki 5 miktar için güncelleştirilen stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 5 miktar için güncelleştirilen stok mali girişi.
-   2a. Her biri 10,00 ABD Doları maliyetindeki 2 miktar için güncelleştirilen stok fiziksel çıkışı.
-   2b. Her biri 10,00 ABD Doları maliyetindeki 2 miktar için güncelleştirilen stok mali çıkışı.
-   3. Stok kapanışı, stok mali girişini stok mali çıkışına kapatmak için doğrudan kapatma yöntemi kullanılarak gerçekleştirilmiştir.

![Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama tarihi doğrudan kapatma](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Çizimin anahtarı:**

-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde veya altında, stok hareketinin değeri *Miktar*@*Birim fiyatı* biçiminde belirtilir.
-   Bir stok hareketi değeri parantez içinde gösteriliyorsa , stok hareketi stoğa fiziksel olarak nakledilmiştir.
-   Bir stok hareketi değeri parantez içinde gösterilmiyorsa , stok hareketi stoğa mali olarak nakledilmiştir.
-   Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden çizgili kırmızı oklarla temsil edilir.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama tarihi özetlenmiş kapatma
Ağırlıklı ortalama, bir kapanış dönemindeki tüm girişlerin yeni bir stok transferi hareketinde özetlenmesi ilkesine dayanır. Bu hareket *ağırlıklı ortalama stok kapanışı* olarak bilinir. Günün tüm girişleri, yeni oluşturulan stok transfer hareketinin çıkışına karşılık kapatılır. Günün tüm çıkışları, yeni stok transfer hareketinin girişine karşılık kapatılır. Eldeki stok, stok kapanışından sonra pozitifse, bu eldeki stok ve stok değeri yeni stok transfer hareketi girişinde özetlenir. Eldeki stok, stok kapanışından sonra negatifse, eldeki stok ve stok değeri tam kapatılmamış bireysel çıkışların toplamıdır. 

Aşağıdaki senaryoda, mali olarak güncelleştirilmiş birkaç giriş ve çıkış dönem içinde deftere nakledilmiştir. Stok kapanışı sırasında, sistem her günün kapatma tarafından nasıl ele alınacağını belirlemek için her günü değerlendirir. 

Aşağıdaki çizimde bu hareketler gösterilmiştir: 

**1. Gün:**

-   1a. Stok fiziksel girişi her biri 15,00 ABD Doları değerindeki 3 miktar için güncelleştirilir
-   1b. Stok mali girişi her biri 15,00 ABD Doları değerinde 3 miktar için güncelleştirilir.
-   2a. 15,00 ABD Doları cari ortalama maliyetine sahip 1 miktarındaki stok fiziksel çıkışı.
-   2b. 15,00 ABD Doları cari ortalama maliyetine sahip 1 miktarındaki stok mali çıkışı.

Sistem 1. gün için doğrudan kapatma yaklaşımını kullanır. 

**2. Gün:**

-   3a. 15,00 ABD Doları cari ortalama maliyetine sahip 1 miktarındaki stok fiziksel çıkışı.
-   3b. 15,00 ABD Doları ortalama maliyetli 1 adet için stok mali çıkışı

Sistem 2. gün için doğrudan kapatma yaklaşımını kullanır. 

**3. Gün:**

-   4a. 15,00 ABD Doları cari ortalama maliyetine sahip 1 miktarındaki stok fiziksel çıkışı.
-   4b. 15,00 ABD Doları ortalama maliyetli 1 adet için stok mali çıkışı
-   5a. Her biri 17,00 ABD Doları değerindeki 1 miktarı için stok fiziksel girişi.
-   5b. Her biri 17,00 ABD Doları değerindeki 1 miktarındaki stok mali girişi.

Stok kapanışı gerçekleştirilir. Doğrudan kapatma kullanılması gerekir çünkü birden çok güne yayılmış birden çok giriş vardır.

-   7a. Bugüne kadar kapatılmamış tüm stok mali girişlerinin kapatmalarını özetlemek için 32,00 ABD Doları değerindeki 2 miktarı için ağırlıklı ortalama stok kapanışı mali çıkışı oluşturulur.
-   7b. 7a için mahsup olarak ağırlıklı ortalama stok kapanış hareketi mali girişi oluşturulur.

Sistem özetlenen stok transferi hareketini oluşturur ve deftere nakleder. Ayrıca sistem o güne ve eldeki stoka ait tüm girişleri özetlenmiş stok transferi çıkış hareketine karşılık kapatır. Günün tüm çıkışları, özetlenmiş stok transferi giriş hareketine karşılık kapatılır. Ağırlıklı ortalama maliyet fiyatı 16,00 ABD Doları olarak hesaplanır. Ağırlıklı ortalama maliyetini düzeltmek için çıkışın düzeltmesi 1,00 ABD Doları olur. Yeni cari ortalama maliyet fiyatı 16,00 Doları olur. 

Aşağıdaki şekilde, bu hareketler serisi, ağırlıklı ortalama stok modeli ve **Fiziksel değeri dahil et** seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir. 

![Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama tarihi özetlenmiş kapatma](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Çizimin anahtarı**

-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde veya altında, stok hareketinin değeri *Miktar*@*Birim fiyatı* biçiminde belirtilir.
-   Bir stok hareketi değeri parantez içinde gösteriliyorsa , stok hareketi stoğa fiziksel olarak nakledilmiştir.
-   Bir stok hareketi değeri parantez içinde gösterilmiyorsa , stok hareketi stoğa mali olarak nakledilmiştir.
-   Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden çizgili kırmızı oklarla temsil edilir.
-   Düz kırmızı renk çapraz oklar, sistem tarafından oluşturulan çıkış hareketine karşılık kapatılmakta olan giriş hareketlerini gösterir.
-   Düz yeşil çapraz ok, orijinal olarak nakledilmiş çıkış hareketinin kapatıldığı sistem tarafından oluşturulmuş mahsup giriş hareketini temsil eder

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Fiziksel değeri dahil et seçeneği kullanıldığında ağırlıklı ortalama tarihi doğrudan kapatma
Geçerli sürüm, önceki sürümlerde kullanılan ağırlıklı ortalama tarihi için aynı kapatma ilkesini kullanır. Sistem giriş ve çıkışlar arasında doğrudan kapatma yapar. Sistem bu doğrudan kapatma ilkesini belirli durumlarda kullanır:

-   Dönem içinde bir giriş ve bir veya daha fazla çıkış deftere nakledildiğinde.
-   Dönem içinde yalnızca çıkışlar deftere nakledildiğinde ve stok önceki kapanıştan eldeki stoku içerdiğinde.

**Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** seçim kutusu işaretlenirse, sistem, cari ortalama maliyet fiyatını ve tahmini maliyet fiyatını hesaplamak için fiziksel olarak güncelleştirilmiş girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatı temel alınarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Fiziksel değeri dahil et seçeneği kullanıldığında ağırlıklı ortalama tarihi özetlenmiş kapatma
**Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** seçim kutusu işaretlenirse, sistem, cari ortalama maliyet fiyatını ve tahmini maliyet fiyatını hesaplamak için fiziksel olarak güncelleştirilmiş girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatı temel alınarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır. Ağırlıklı ortalama kapanışı, bir kapanış dönemindeki girişlerin *ağırlıklı ortalama stok kapanışı* olarak bilinen yeni bir stok transfer hareketinde özetlenmesi ilkesine dayanır. Günün tüm girişleri, yeni oluşturulan stok transfer hareketinin çıkışına karşılık kapatılır. Günün tüm çıkışları, yeni stok transfer hareketinin girişine karşılık kapatılır. Eldeki stok, stok kapanışından sonra pozitifse, bu eldeki stok ve stok değeri yeni stok transfer hareketinde (giriş) özetlenir. Eldeki stok, stok kapanışından sonra negatifse, eldeki stok ve stok değeri tam kapatılmamış bireysel çıkışların toplamıdır.

## <a name="weighted-average-date-when-marking-is-used"></a>İşaretleme kullanıldığında ağırlıklı ortalama tarihi
İşaretleme bir hareket giriş hareketini bağlamanıza olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz. 

Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etti. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak amacıyla bu madde için daha fazla ödemeniz gerekecektir. Bu stok maddesinin bu satış siparişi faturası için marja veya satılan malların maliyetine (SMM) yansıtılacağından emin olmanız gerekir. Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Satış siparişi belgesi satınalma emrine sevk irsaliyesi veya fatura deftere nakledilmeden önce işaretlenmiştir. SMM, maddenin cari ortalama maliyeti yerine 120,00 ABD doları olacaktır. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir. Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir. Giriş hareketi bir çıkış hareketine işaretlendiğinde, maddenin madde model grubu içinde tanımlanan değerleme yöntemi göz ardı edilir. Bunun yerine, sistem bu hareketleri birbiriyle kapatır. 

Hareketin deftere nakledilmeden önce bir giriş için bir çıkış hareketi işaretleyebilirsiniz. Bunu **Satış siparişi bilgileri** sayfasındaki bir satış siparişi satırından yapabilirsiniz. Açık giriş hareketlerini **İşaretleme** sayfasında görebilirsiniz. Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi de işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz. Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 30,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel girişi.
-   4b. Her biri 30,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali girişi.
-   5a. 21,25 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali ve fiziksel olarak güncelleştirilmiş hareketlerin cari ortalaması).
-   5b. 1 miktarındaki stok mali çıkışı hareket deftere nakledilmeden önce stok girişi 2b'ye işaretlenir. Hareket, 20,00 ABD Doları maliyet fiyatı ile deftere nakledilir.
-   6a. 21,25 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı.
-   7. Stok kapanışı gerçekleştirilir. Mali olarak güncelleştirilen hareket var olan bir girişe işaretlendiği için, bu hareketler birbirine karşılık kapatılır ve bir düzeltme yapılmaz.

Yeni cari ortalama maliyet fiyatı 27,50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. Aşağıdaki şekil bu hareketler serisini, işaretleme ve ağırlıklı ortalama tarihi stok modeli kullanmanın etkilerini gösterir.

![İşaretleme ile ağırlıklı ortalama tarihi](./media/weightedaveragedatewithmarking.gif) 

**Çizimin anahtarı:**

-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde veya altında, stok hareketinin değeri *Miktar*@*Birim fiyatı* biçiminde belirtilir.
-   Bir stok hareketi değeri parantez içinde gösteriliyorsa , stok hareketi stoğa fiziksel olarak nakledilmiştir.
-   Bir stok hareketi değeri parantez içinde gösterilmiyorsa , stok hareketi stoğa mali olarak nakledilmiştir.
-   Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden çizgili kırmızı oklarla temsil edilir.




