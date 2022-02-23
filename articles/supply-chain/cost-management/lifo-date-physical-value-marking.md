---
title: Fiziksel değer ve işaretleme ile LIFO Tarihi
description: Son giren ilk çıkar Tarihi (LIFO Tarihi), LIFO ilkesine dayanan bir stok modelidir. Stok çıkışları, stok hareketinin tarihine dayalı olarak son son girişlerine göre kapatılır. LIFO Tarihini kullanarak, çıkıştan önce hiçbir giriş yoksa, çıkış, çıkış tarihinden sonraki tüm girişlere karşılık olarak kapatılır. Aynı tarihteki birkaç çıkış son çıkış, son giriş sırasıyla kapatılabilir.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2c06443532519ad5d6c36a6f4ed1f1c4d136664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967645"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile LIFO Tarihi

[!include [banner](../includes/banner.md)]

Son giren ilk çıkar Tarihi (LIFO Tarihi), LIFO ilkesine dayanan bir stok modelidir. Stok çıkışları, stok hareketinin tarihine dayalı olarak son son girişlerine göre kapatılır. LIFO Tarihini kullanarak, çıkıştan önce hiçbir giriş yoksa, çıkış, çıkış tarihinden sonraki tüm girişlere karşılık olarak kapatılır. Aynı tarihteki birkaç çıkış son çıkış, son giriş sırasıyla kapatılabilir. 

Son giren ilk çıkar Tarih (LIFO Tarihi) stok modelini kullandığınızda, çıkıştan önce hiçbir giriş yoksa, çıkış, çıkış tarihinden sonraki tüm girişlere karşılık olarak kapatılır. Aynı tarihteki birkaç çıkış son çıkış, son giriş sırasıyla kapatılabilir. LIFO Tarihi kullandığınızda, LIFO Tarihi kuralı kullanmak zorunda değilsiniz. Bunun yerine, stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyebilirsiniz. 

LIFO Tarihi stok modelini kullanırken periyodik stok kapatma yapmanızı öneririz. 

Aşağıdaki örnekler, üç farklı yapılandırmada LIFO Tarihi kullanımının etkisini göstermektedir:

-   **Fiziksel değeri dahil et** seçeneği kullanılmadan LIFO Tarihi
-   **Fiziksel değeri dahil et** seçeneği kullanılarak LIFO Tarihi
-   İşaretleme kullanılarak LIFO Tarihi

## <a name="lifo-date-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan LIFO Tarihi
Bu örnekte ürün model grubu, fiziksel değeri dahil edecek şekilde işaretlenmemiştir. Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. 15,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   4b. 15,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   6. Stok kapanışı gerçekleştirilir. LIFO Tarihi yöntemine dayanarak, son mali olarak güncelleştirilen çıkış, tarihe göre mali olarak güncelleştirilen son girişe karşılık kapatılır. Çıkış hareketinde 5,00 ABD Doları tutarında bir düzeltme yapılır. Bu hareketler birbirlerine karşılık kapatılır.

Yeni cari ortalama maliyet fiyatı, 15,00 ABD Doları tutarında mali olarak güncelleştirilen hareketlerin ortalamasını yansıtır. 

Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanılmadığında LIFO Tarihi stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. ![Fiziksel Değeri Dahil Et Seçeneği ile LIFO Tarihi](./media/lifodatewithoutincludephysicalvalue.gif) 

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
- Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar@Birim fiyatı biçiminde belirtilir.
- Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
- Parantezler içinde gösterilmeyen bir stok hareketi değeri, stok hareketinin stoka mali olarak nakledildiğini gösterir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="lifo-date-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılarak LIFO Tarihi
**Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusunu seçebilirsiniz. Bu durumda, sistem cari ortalama maliyet fiyatını hesaplamak için hem fiziksel hem de mali olarak güncelleştirilen hareketleri kullanır. Uygun olan yerlerde sistem, fiziksel olarak güncelleştirilmiş çıkış hareketinde düzeltmeler de yapar. **Fiziksel değeri dahil et** seçim kutusunun onay işareti kaldırıldığında, LIFO Tarihi stok modeli ile stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar. 

Bu örnekte ürün model grubu, fiziksel değeri dahil edecek şekilde işaretlenmiştir. 

Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 18,33 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   4b. Her biri 18,33 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   5a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   5b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   6. Stok kapanışı gerçekleştirilir. LIFO Tarihi yöntemine dayanarak, son güncelleştirilen çıkış, tarihe göre güncelleştirilen son girişe karşılık düzeltilir veya kapatılır. Mali giriş hareketi bir fiziksel güncelleştirme hareketine karşılık düzeltildiği için bu hareketler birbirleri tarafından kapatılmaz. Bunun yerine yalnızca çıkış hareketinde 6,67 Dolarlık bir düzeltme yapılır.

Yeni cari ortalama maliyet fiyatı, 20,00 ABD Doları tutarında mali olarak güncelleştirilen hareketlerin ortalamasını yansıtır. 

Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. ![Fiziksel Değeri Dahil Et Seçeneği ile LIFO Tarihi](./media/lifodatewithincludephysicalvalue.gif) 

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
- Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar@Birim fiyatı biçiminde belirtilir.
- Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
- Parantezler içinde gösterilmeyen bir stok hareketi değeri, stok hareketinin stoka mali olarak nakledildiğini gösterir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="lifo-date-with-marking"></a>İşaretleme kullanılarak LIFO Tarihi
İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz. 

Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etsin. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak için bu madde için daha fazla ödemeniz gerekecek. Bu stok maddesinin bu satış siparişi faturası için marja veya satılan malların maliyetine (COGS) yansıtılacağından emin olmanız gerekiyor. 

Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Bu satış siparişi belgesi, sevk irsaliyesi veya fatura nakledilmeden önce satın alma siparişine işaretlenirse, satılan malların maliyeti maddenin cari ortalama maliyeti yerine 120,00 ABD Doları olur. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir. 

Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir. 

Örneğin, bir giriş hareketi bir çıkış hareketi için işaretlenir. Bu durumda, maddenin madde modeli grubunda tanımlı olan değerlendirme yöntemi göz ardı edilir ve sistem bu hareketleri birbirine karşılık kapatır. 

Hareketin deftere nakledilmeden önce bir giriş için bir çıkış hareketi işaretleyebilirsiniz. Bunu **Satış siparişi bilgileri** sayfasındaki bir satış siparişi satırından yapabilirsiniz. Açık giriş hareketlerini **işaretleme** sayfasında görebilirsiniz. 

Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi de işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz. 

Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   5a. Her biri 21,25 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali ve fiziksel olarak güncelleştirilmiş hareketlerin cari ortalaması).
-   5b. 1 miktarındaki stok mali çıkışı hareket deftere nakledilmeden önce stok girişi 2b'ye işaretlenir. Hareket, her biri 20,00 ABD Doları maliyet fiyatı ile deftere nakledilir.
-   6a. Her biri 21,25 ABD Doları maliyet fiyatındaki 1 miktarındaki stok fiziksel çıkışı.
-   7. Stok kapanışı gerçekleştirilir. Mali olarak güncelleştirilen İlk giren ilk çıkar (FIFO) hareketi var olan bir girişe işaretlendiğinden, bu hareketler birbirine karşılık kapatılır ve bir düzeltme yapılmaz.

Yeni cari ortalama maliyet fiyatı 27,50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. 

Aşağıdaki çizimde, çıkışlar ve girişler arasında işaretleme kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. ![İşaretleme ile LIFO Tarihi    ](./media/lifodatewithmarking.gif) 

**Diyagramın anahtarı**

- Stok hareketleri dikey oklarla temsil edilir.
- Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
- Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
- Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar@Birim fiyatı biçiminde belirtilir.
- Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
- Parantezler içinde gösterilmeyen bir stok hareketi değeri, stok hareketinin stoka mali olarak nakledildiğini gösterir.
- Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
- Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
- Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
- Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.




