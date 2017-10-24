---
title: "Fiziksel değer ve işaretleme ile LIFO"
description: "Son Giren İlk Çıkar (LIFO), son (en yeni) girişlerin en önce çıkarıldığı bir stok modelidir. Stok çıkışları, stok hareketinin tarihine dayalı olarak son son girişlerine göre kapatılır."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 86bafb9346b7335bf0a5d6c156eee6d53f1998a9
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="lifo-with-physical-value-and-marking"></a>Fiziksel değer ve işaretleme ile LIFO

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Son Giren İlk Çıkar (LIFO), son (en yeni) girişlerin en önce çıkarıldığı bir stok modelidir. Stok çıkışları, stok hareketinin tarihine dayalı olarak son son girişlerine göre kapatılır. 

Son Giren İlk Çıkar (LIFO) stok modelinde, en son (en yeni) girişler ilk önce çıkar. Stok çıkışları, stok hareketinin tarihine dayalı olarak son girişlere göre kapatılır. LIFO'yu kullandığınızda, LIFO kuralını kullanmak zorunda değilsiniz. Bunun yerine, stok hareketlerini, belirli bir madde çıkışının belirli bir girişe göre kapatılması için işaretleyebilirsiniz. LIFO stok modelini kullanırken dönemsel bir stok kapanışı önerilir. 

Aşağıdaki örnekler, üç farklı konfigürasyonda LIFO kullanımının etkisini göstermektedir:

-   **Fiziksel değeri dahil et** seçeneği olmadan LIFO
-   **Fiziksel değeri dahil et** seçeneği ile LIFO
-   İşaretleme kullanılarak LIFO

## <a name="lifo-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan LIFO
Bu örnekte ürün model grubu, fiziksel değeri dahil edecek şekilde işaretlenmemiştir. Aşağıdaki çizimde bu hareketler gösterilmiştir:

-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   5a. Her biri 20,00 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   5b. Her biri 20,00 ABD Doları maliyet fiyatında 1 miktarındaki stok mali çıkışı (mali olarak güncelleştirilen hareketlerin cari ortalaması).
-   6. Stok kapanışı gerçekleştirilir. LIFO yöntemine dayanarak, mali olarak güncelleştirilen son çıkış mali olarak güncelleştirilen son girişe karşılık kapatılır. Çıkış hareketinde 10,00 ABD Doları tutarında bir düzeltme yapılır.

Yeni cari ortalama maliyet fiyatı, 15,00 ABD Doları tutarında mali olarak güncelleştirilen hareketlerin ortalamasını yansıtır. Aşağıdaki çizimde, **Fiziksel değeri dahil et** seçeneği kullanılmadığında LIFO stok modelinin bu hareket serisindeki etkileri gösterilmiştir. ![Fiziksel Değeri Dahil Et Seçeneği Kullanılmadan LIFO](./media/lifowithoutincludephysicalvalue.gif) 

**Diyagramın anahtarı**

-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unit fiyat biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantezler içinde gösterilmeyen bir stok hareketi değeri, stok hareketinin stoka mali olarak nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="lifo-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılarak LIFO
**Madde model grupları** sayfasındaki bir madde için **Fiziksel değeri dahil et** onay kutusu seçildiğinde, sistem, cari ortalama maliyet fiyatını hesaplamak için hem fiziksel hem de mali giriş hareketlerini kullanır. Uygun olan yerlerde sistem, fiziksel olarak güncelleştirilmiş çıkış hareketinde düzeltmeler de yapar. **Fiziksel değeri dahil et** seçim kutusunun onay işareti kaldırıldığında, LIFO envanter modeli ile stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar. 

Aşağıdaki çizimde şu hareketler gösterilmiştir:

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
-   7. Stok kapanışı gerçekleştirilir. LIFO yöntemine dayanarak, son çıkış hareketi son güncelleştirilen girişe karşılık ayarlanır veya kapatılır.

Hareket 6a, 4b giriş hareketine ayarlanacaktır. Giriş mali değil, yalnızca fiziksel olarak güncelleştirildiğinden sistem bu hareketleri kapatmaz. Bunun yerine, fiziksel çıkış hareketine yalnızca 8,75 ABD Doları tutarında bir düzeltme nakledilir. 5b hareketi, 3a fiziksel giriş hareketine ayarlanır. Sistem, ikisi de mali olarak güncelleştirilmediğinden bu hareketleri kapatmaz. Bunun yerine, bu çıkış hareketine yalnızca negatif 3,75 ABD Doları tutarında bir düzeltme yapılır. Yeni cari ortalama maliyet fiyatı 20.00 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. 

Aşağıdaki çizimde **Fiziksel değeri dahil et** seçeneği kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. ![Fiziksel Değeri Dahil Et Seçeneği ile LIFO](./media/lifowithincludephysicalvalue.gif) 

**Diyagramın anahtarı**

-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unit fiyat biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantezler içinde gösterilmeyen bir stok hareketi değeri, stok hareketinin stoka mali olarak nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.

## <a name="lifo-with-marking"></a>İşaretleme kullanılarak LIFO
İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz. Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etsin. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak için bu ürün için daha fazla ödemeniz gerekecek. 

Bu stok maddesinin bu satış siparişi faturası için marja veya satılan malların maliyetine (COGS) yansıtılacağından emin olmanız gerekiyor. Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Bu satış siparişi belgesi, sevk irsaliyesi veya fatura nakledilmeden önce satın alma siparişine işaretlenirse, satılan malların maliyeti maddenin cari ortalama maliyeti yerine 120,00 ABD Doları olur. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir. 

Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir. 

Hareket deftere nakledilmeden önce bir çıkış hareketini bir giriş hareketi için işaretleyebilirsiniz. Bunu **Satış siparişi bilgileri** sayfasındaki bir satış siparişi satırından yapabilirsiniz. Açık giriş hareketlerini **işaretleme** sayfasında görebilirsiniz. 

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
-   7. Stok kapanışı gerçekleştirilir. Mali olarak güncelleştirilen FIFO hareketini var olan bir girişe işaretlendiği için, bu hareketler birbirine karşılık olarak kapatılır ve bir düzeltme yapılmaz.

Yeni cari ortalama maliyet fiyatı 27.50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. 

Aşağıdaki çizimde çıkışlar ve girişler kullanıldığında LIFO stok modelinin bu hareket serisi üzerindeki etkileri gösterilmiştir. ![İşaretleme ile LIFO    ](./media/lifowithmarking.gif) 

**Diyagram anahtarı**

-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unit fiyat biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantezler içinde gösterilmeyen bir stok hareketi değeri, stok hareketinin stoka mali olarak nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketi yeni bir etiketle gösterilir.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki stok hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve *Stok Kapanışı* etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden kesikli kırmızı oklarla temsil edilir.





