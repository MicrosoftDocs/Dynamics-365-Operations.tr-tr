---
title: Fiziksel değer ve işaretleme ile FIFO
description: İlk Giren İlk Çıkar (FIFO), ilk alınan girişlerin ilk olarak çıkartıldığı bir stok modelidir. Stoktan yapılan mali olarak güncelleştirilen çıkışlar, stok hareketinin mali tarihine göre stoka yapılan ilk mali güncelleştirilen girişlere karşılık kapatılır.
author: AndersGirke
manager: tfehr
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1322d43d536bf7ff4c40fcdecebbd95a46f70d2d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981596"
---
# <a name="fifo-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile FIFO

[!include [banner](../includes/banner.md)]

İlk Giren İlk Çıkar (FIFO), ilk alınan girişlerin ilk olarak çıkartıldığı bir stok modelidir. Stoktan yapılan mali olarak güncelleştirilen çıkışlar, stok hareketinin mali tarihine göre stoka yapılan ilk mali güncelleştirilen girişlere karşılık kapatılır. 

FIFO'yu kullandığınızda, FIFO kuralını kullanmak zorunda değilsiniz. Bunun yerine, stok hareketlerini, belirli bir madde girişinin belirli bir çıkışa göre kapatılması için işaretleyebilirsiniz. FIFO stok modelini kullanırken periyodik stok kapanışı yapmanızı öneririz. Aşağıdaki örnekler, üç farklı konfigürasyonda FIFO kullanımının etkisini göstermektedir:

-   **Fiziksel değeri dahil et** seçeneği olmadan FIFO
-   **Fiziksel değeri dahil et** seçeneği ile FIFO
-   İşaretleme ile FIFO

## <a name="fifo-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan FIFO
Bu örnekte ürün model grubu, fiziksel değeri dahil edecek şekilde işaretlenmemiştir. Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 10,00 ABD Doları maliyetinde 2 ürün tutarının stok fiziksel girişi.
-   2b. Her biri 10,00 ABD Doları maliyetinde 2 ürün tutarının stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   5a. Her biri 20,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   5b. Her biri 15,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   6. Stok kapanışı gerçekleştirilir. FIFO yöntemine dayanarak, ilk mali olarak güncelleştirilen çıkış ilk mali olarak güncelleştirilen girişe karşılık olarak kapatılır. Çıkış hareketinde 5,00 ABD Doları tutarında bir düzeltme yapılır.

Yeni cari ortalama maliyet fiyatı, mali olarak güncelleştirilen hareketlerin ortalamasını yansıtır. Aşağıdaki çizimlerde **Fiziksel değeri dahil et** seçenek kullanılmadığında FIFO stok modelinin bu hareket serisindeki etkilerini gösterir. 

![Fiziksel Değeri Dahil Et Seçeneği Kullanılmadan FIFO](./media/fifowithoutincludephysicalvalue.gif) 

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

## <a name="fifo-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği ile FIFO
**Madde model grubu** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu seçildiğinde, sistem, cari ortalama maliyet fiyatını hesaplamak için hem fiziksel hem de mali giriş hareketlerini kullanır. Uygun olan yerlerde sistem, fiziksel olarak güncelleştirilmiş çıkış hareketinde düzeltmeler de yapar. **Fiziksel değeri dahil et** seçim kutusunun onay işareti kaldırıldığında, FIFO envanter modeli ile stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar. Aşağıdaki çizimde şu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   5a. Her biri 21,25 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali ve fiziksel olarak güncelleştirilmiş hareketlerin cari ortalaması).
-   5b. Her biri 21,25 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali ve fiziksel olarak güncelleştirilmiş hareketlerin cari ortalaması).
-   6a. Her biri 21,25 ABD Doları maliyet fiyatındaki 1 miktarındaki stok fiziksel çıkışı.
-   7. Stok kapanışı gerçekleştirilir. FIFO yöntemine dayanarak, ilk mali çıkış hareketi, mali veya fiziksel olarak ilk güncelleştirilen girişe karşılık olarak düzeltilir veya kapatılır.

5b hareketi 1b giriş hareketine karşılık olarak kapatılır. Bu çıkış hareketine negatif 11.25 ABD Doları tutarında bir düzeltme yapılır. Yeni cari ortalama maliyet fiyatı 27.50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanıldığında FIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. 

![Fiziksel Değeri Dahil Et Seçeneği ile FIFO](./media/fifowithincludephysicalvalue.gif) 

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

## <a name="fifo-with-marking"></a>İşaretleme ile FIFO
İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz. Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etsin. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak için bu ürün için daha fazla ödemeniz gerekecek. Bu stok maddesinin bu satış siparişi faturası için marja veya satılan malların maliyetine (COGS) yansıtılacağından emin olmanız gerekiyor. Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Bu satış siparişi belgesi, sevk irsaliyesi veya fatura nakledilmeden önce satın alma siparişine işaretlenirse, satılan malların maliyeti maddenin cari ortalama maliyeti yerine 120,00 ABD Doları olur. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir. Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir. Bir giriş hareketi bir çıkış hareketiyle eşleştiğinde, ürün modeli grubunda tanımlanan değerlendirme yöntemi göz ardı edilir ve sistem bu hareketleri birbirine karşılık kapatır. Hareketin deftere nakledilmeden önce bir giriş için bir çıkış hareketi işaretleyebilirsiniz. Bunu **Satış siparişi bilgileri** sayfasındaki bir satış siparişi satırından yapabilirsiniz. Açık giriş hareketlerini **işaretleme** sayfasında görebilirsiniz. Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi de işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz. Aşağıdaki çizimde bu hareketler gösterilmiştir:

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
-   7. Stok kapanışı gerçekleştirilir. Mali olarak güncelleştirilen FIFO hareketini var olan bir girişe işaretlendiği için, bu hareketler birbirine karşılık olarak kapatılır ve bir düzeltme yapılmaz.

Yeni cari ortalama maliyet fiyatı 27.50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. Aşağıdaki çizimde çıkışlar ve girişler kullanıldığında FIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. 

![İşaretleme ile FIFO](./media/fifowithmarking.gif) 

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




