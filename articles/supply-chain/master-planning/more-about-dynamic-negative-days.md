---
title: Negatif günler ve dinamik negatif günler
description: Bu konu, negatif günler ve dinamik negatif günler hakkında bilgi verir ve işinize yardımcı olması için bunları nasıl kullanabileceğinizi açıklar.
author: t-benebo
manager: AnnBe
ms.date: 06/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: ''
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff907a624d62b00d2aaf21c185175e8717b6c624
ms.sourcegitcommit: b3d099eb1f9a8a582c02ea6c5ee30c830d53a411
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "1628800"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negatif günler ve dinamik negatif günler

[!include [banner](../includes/banner.md)]

Bu konu, negatif günler ve dinamik negatif günler hakkında bilgi verir ve işinize yardımcı olması için bunları nasıl kullanabileceğinizi açıklar. *Negatif günler zaman dilimi* negatif stoğunuz olduğunda veya yeni bir stok yenileme siparişi vermeden önce beklemek istediğiniz gün sayısını temsil eder.

Bu konuda, aşağıdaki bilgileri öğreneceksiniz:

- Planlı siparişleri oluşturma
- Negatif günler zaman dilimi ve maddenin sağlama süresi arasındaki ilişki
- Dinamik negatif günlerin zaman dilimi hesaplaması ve maddenin sağlama süresinin hesaplama ile nasıl hesaplandığı.
- Negatif günlerle ilişkili [malzeme ihtiyaç planlamasında çalışma süresinin iyileştirilmesine yönelik öneriler (MRP) (master planning)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) nasıl yorumlanır

Bu konu, bu bilgileri anlamanıza yardımcı olması için üç kuramsal senaryo kullanır. Senaryolar arasındaki fark, talep ettiğiniz noktadır: maddenin teslim süresinden önce, sırasında veya sonrasında.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Senaryo 1: maddenin sağlama süresinden önce talep alırsınız

İsteğe bağlı olarak, madde bekleme süresi ya da sağlama süresi başlamadan hemen önce bir talep alabilirsiniz. Bu senaryoya bir örnek aşağıda verilmiştir:

- DemoProduct maddesinin altı günlük bir satınalma sağlama süresi vardır.
- Sıfırıncı günde (1 Ocak), DemoProduct maddesi için stok düzeyi 0'dır (sıfır).
- Sıfırıncı günde (1 Ocak), DemoProduct öğesinin 10'u miktarında bir satış siparişi alırsınız.
- Yedi (7 Ocak) numaralı günde,DemoProduct öğesinin 10'u miktarında mevcut bir satınalma siparişi vardır.

Aşağıdaki çizim, bu senaryonun grafiksel bir görünümünü göstermektedir.

![Senaryo 1'in grafik görünümü](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Olay A: Negatif günler maddenin sağlama süresinden daha küçüktür

Negatif günleri maddenin sağlama süresinden daha az olan bir sayıya ayarlarsanız MRP negatif günler zaman dilimi içindeki DemoProduct maddesi için giriş arar. Herhangi bir giriş bulamadığı için, MRP yeni planlı satınalma siparişi oluşturur. Bu planlı sipariş hemen altı gün geciktirilir (sağlama süresi). Bu nedenle, 7 Ocak'ta ulaşır. Yeni planlı satınalma siparişinin oluşturulması bunu gereksiz hale getirdiğinden, varolan satınalma siparişi **İptal** eylemi iletisi alır.

Aşağıdaki resim bu olayın ekran görüntüsünü gösterir.

![Olay A senaryo 1 için ekran görüntüsü](./media/negative-days-2.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay A senaryo 1 için grafik görünümü](./media/negative-days-3.png)

MRP performansı ve planlama tedirginliğini dikkate alırsanız bu olay iyi sonuç vermez. MRP yeni bir planlı sipariş oluşturmalı ve gecikmeleri ve eylemleri hesaplamalıdır. Bu görevler zaman alabilir. Bu olay, planınıza daha fazla hareket de ekler. Diğer taraftan, satış siparişi yedi gün değil, yalnızca altı gün gecikir.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Olay B: Negatif günler maddenin sağlama süresinden daha büyüktür

MRP performansını artırmaya yardımcı olmak için, Negatif günleri maddenin sağlama süresine göre daha büyük bir sayıya ayarlayabilirsiniz. Sağlama süresi içinde bu senaryoda tedarik sağlayamamanıza neden olacağından, bu aramanın anlamlı olduğu uzunlukta girişler için arama yapabilirsiniz. MRP için çalışma süresi daha kısa olsa da siparişler için ek gecikmelere dikkat etmelisiniz.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Olay C: Maddenin teslimat süresini otomatik olarak negatif gün zaman dilimi ile ilişkilendirme

Maddenin teslimat süresini otomatik olarak negatif gün zaman dilimi ile ilişkilendirmek için dinamik negatif günleri kullanın. Dinamik günleri kullanmak için **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin ve sonra, **Karşılama** bölümündeki **Genel** sekmede, **Dinamik negatif günleri kullan** seçeneğini **Evet** olarak ayarlayın. MRP daha sonra dinamik negatif günler zaman dilimi dahilindeki girişleri arar. Zaman dilimi aşağıdaki formül kullanılarak hesaplanır:

Dinamik negatif günler zaman dilimi = Satınalma sağlama süresi + Negatif günler zaman dilimi + (Geçerli tarih – Gereksinim tarihi)

(DemoProduct maddesinin varsayılan türü **Ürün** ya da **Transfer** ise sağlama süresi **stok** sağlama süresidir.)

Dinamik negatif günler kullanıldığında, MRP'nin girişler için aradığı zaman dilimi şimdi 6 + 2 + 0 = 8 gündür. MRP varolan satınalma siparişini bulur ve satış siparişini buna göre ilişkilendirir. Yeni planlı siparişler oluşturulmaz. Bu nedenle, MRP için çalışma süresi daha kısadır. Aşağıdaki şekil, DemoProduct maddesiyle ilgili net gereksinimleri gösterir.

![Senaryo 1 C olayı için net gereksinimler](./media/negative-days-4.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay C senaryo 1 için grafik görünümü](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Olay D: Yalnızca dinamik negatif günleri kullan

Negatif günleri **0**'a (sıfır) ayarlarsanız ve yalnızca dinamik negatif günler zaman dilimini kullanırsanız dinamik negatif günler zaman dilimi 6 + 0 + 0 = 6 gündür. Bu olayda, sonuç bu senaryo için A olayında elde edilen sonuçla aynıdır. MRP yeni bir planlı sipariş oluşturmalı ve gecikmeleri ve eylemleri hesaplamalıdır. Bu görevler uzun sürebilir ve ayrıca sinir bozucu olabilir. Ayrıca, işlemek için iki işleminiz daha vardır. Bir maddenin ulaşması için talep zamanında yerine getirilemediğinden, bu olay planınıza gereksiz zorluk ekler.

Aşağıdaki resim bu olay için ekran görüntüsünü gösterir.

![Olay D senaryo 1 için ekran görüntüsü](./media/negative-days-6.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay D senaryo 1 için grafik görünümü](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Olay E: Hem maddenin teslim süresinden daha fazla olan negatif günleri hem de dinamik negatif günlerin zaman dilimlerini kullanın

Negatif günleri maddenin sağlama zamanından daha büyük bir sayıya ayarlarsanız ve ayrıca dinamik negatif günler zaman dilimini kullanırsanız dinamik negatif günler zaman dilimi 6 + 6 + 0 = 12 gün olarak ayarlanır. Bu yaklaşım, MRP'nin sonuçları araması gereken çok uzun bir zaman dilimi oluşturabilir. Negatif günleri uzun bir zaman dilimine ayarladığınız bir olay ilgili E olayı hakkında bilgi almak için bu konunun [Conclusion](#conclusion) bölümüne bakın.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Senaryo 2: Maddenin sağlama süresi boyunca talep alırsınız

Maddenin sağlama süresi boyunca bir süre talep alabilirsiniz. Bu senaryoya bir örnek aşağıda verilmiştir:

- DemoProduct maddesinin altı günlük bir satınalma sağlama süresi vardır. 
- Sıfırıncı günde (1 Ocak), DemoProduct maddesi için stok düzeyi 0'dır (sıfır).
- Maddenin sağlama süresi içerisinde bulunan 4. günde (5 Ocak), DemoProduct maddesinin 10'unun miktarında satış siparişini alırsınız.
- Yedi (8 Ocak) numaralı günde,DemoProduct öğesinin 10'u miktarında bir satınalma siparişi vardır.

Aşağıdaki çizim, bu senaryonun grafiksel bir görünümünü göstermektedir.

![Senaryo 1'in grafik görünümü](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Olay A: Negatif günler maddenin sağlama süresinden daha küçüktür

Negatif günleri maddenin sağlama süresinden daha az olan bir sayıya ayarlarsanız MRP negatif günler zaman dilimi içindeki DemoProduct maddesi için giriş arar. Herhangi bir giriş bulamadığı için MRP, sipariş tarihi olarak geçerli tarihi kullanan yeni bir planlı satınalma siparişi oluşturur. Bu planlı sipariş hemen altı gün geciktirilir (sağlama süresi). Bu nedenle, 7 Ocak'ta ulaşır. Yeni planlı satınalma siparişinin oluşturulması bunu gereksiz hale getirdiğinden, varolan satınalma siparişi **İptal** eylemi iletisi alır.

Aşağıdaki resim bu olay için ekran görüntüsünü gösterir.

![Olay A senaryo 2 için ekran görüntüsü](./media/negative-days-9.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay A senaryo 2 için grafik görünümü](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Olay B: Negatif günler maddenin sağlama süresinden daha büyüktür

Bu olay senaryo 1 için B senaryosuna benzer. Negatif günleri maddenin sağlama süresine göre daha büyük bir sayıya ayarlarsanız yeni bir planlı sipariş elde etmezsiniz. Satış siparişi, varolan satınalma siparişine bağlıdır.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Olay C: Maddenin teslimat süresini otomatik olarak negatif gün zaman dilimi ile ilişkilendirme

Bu olay Senaryo 1 için olay C'ye benzer, çünkü dinamik negatif günler de o olayda olduğu gibi çalışır. Dinamik negatif günler zaman dilimi şimdi 6 + 2 – 4 = 4 gündür. Bu yaklaşımı kullanırsanız MRP varolan satınalma siparişini bulur ve satış siparişini buna iliştirir. Yeni planlı siparişler oluşturulmadığından, MRP için çalışma süresi daha kısadır.

Aşağıdaki resim bu olayın ekran görüntüsünü gösterir.

![Olay C senaryo 2 için ekran görüntüsü](./media/negative-days-11.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay C senaryo 2 için grafik görünümü](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Olay D: Yalnızca dinamik negatif günleri kullan

Negatif günleri **0**'a (sıfır) ayarlarsanız ve yalnızca dinamik negatif günler zaman dilimini kullanırsanız dinamik negatif günler zaman dilimi 6 + 0 – 4 = 2 gündür. Bu olayda, sonuç bu senaryo için A olayında elde edilen sonuçla aynıdır. Oluşun grafiksel görünüm için bkz. Bu senaryo için olay A.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Olay E: Hem maddenin teslim süresinden daha fazla olan negatif günleri hem de dinamik negatif günlerin zaman dilimlerini kullanın

Negatif günleri maddenin sağlama zamanından daha büyük bir sayıya ayarlarsanız ve ayrıca dinamik negatif günler zaman dilimini kullanırsanız dinamik negatif günler zaman dilimi 6 + 6 – 4 = 8 gün olarak ayarlanır. Bu yaklaşım, MRP'nin sonuçları araması gereken çok uzun bir zaman dilimi oluşturabilir. Negatif günleri uzun bir zaman dilimine ayarladığınız bir olay ilgili E olayı hakkında bilgi almak için bu konunun [Conclusion](#conclusion) bölümüne bakın.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Senaryo 3: Maddenin sağlama süresinden sonra talep alırsınız

Maddenin sağlama süresinden sonra talep alabilirsiniz. Bu senaryoya bir örnek aşağıda verilmiştir:

- DemoProduct maddesinin altı günlük bir satınalma sağlama süresi vardır.
- Sıfırıncı günde (1 Ocak), DemoProduct maddesi için stok 0'dır (sıfır).
- Maddenin sağlama süresi dışında bulunan yedinci günde (8 Ocak), DemoProduct maddesinin 10'unun miktarında satış siparişini alırsınız.
- 10 (11 Ocak) numaralı günde, DemoProduct öğesinin 10'u miktarında bir satınalma siparişi vardır.

Aşağıdaki çizim, bu senaryonun grafiksel bir görünümünü göstermektedir.

![Senaryo 3'in grafik görünümü](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Olay A: Negatif günler maddenin sağlama süresinden daha küçüktür

Negatif günleri maddenin sağlama süresinden daha düşük bir sayıya ayarlarsanız MİP satış siparişi gereklilik tarihinden iki gün öncesini arar. Herhangi bir şey bulamadığı için MRP, 2 Ocak'ta yeni planlı satınalma siparişi oluşturur. Bu planlı satınalma siparişi, satış siparişi talebinin yerine getirilmesi için zamanında sevk edilir. Gerekli olmadığı için varolan satınalma siparişi **İptal** eylemi iletisi alır.

Aşağıdaki resim bu olayın ekran görüntüsünü gösterir.

![Olay A senaryo 3 için ekran görüntüsü](./media/negative-days-14.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay A senaryo 3 için grafik görünümü](./media/negative-days-15.png)

> [!NOTE]
> Önceki ekran görüntüsünde, satınalma siparişinin gereksinim tarihi 12 Ocak'tır. Bu ekran görüntüsü 2015 tarihinde çekildiği için, 11 Ocak Pazar günü olan MRP, gereksinim tarihini 12 Ocak Pazartesi olan bir sonraki çalışma gününe taşındı. Bununla birlikte, satınalma siparişinin teslim tarihi 11 Ocak'tır.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Olay B: Negatif günler maddenin sağlama süresinden daha büyüktür

Negatif günleri maddenin sağlama süresine göre daha büyük bir sayıya ayarlarsanız yeni bir planlı sipariş elde etmezsiniz. Satış siparişi, varolan satınalma siparişine karşı ilişkilendirilir. Bu nedenle, satış siparişi gecikir. Planlı sipariş oluşturursanız satış siparişini zamanında sevk edebilirsiniz.

Aşağıdaki resim bu olayın ekran görüntüsünü gösterir.

![Olay B senaryo 3 için ekran görüntüsü](./media/negative-days-16.png)

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay B senaryo 3 için grafik görünümü](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Olay C: Maddenin teslimat süresini otomatik olarak negatif gün zaman dilimi ile ilişkilendirme

Bu olay Senaryo 1 için olay C'ye benzer, çünkü dinamik negatif günler de o olayda olduğu gibi çalışır, yoksa bu senaryo için olay B'de çalışır.

Dinamik negatif günler zaman dilimi 6 + 2 – 7 = 1 gündür. Ancak, bu olayda, sistem negatif günler sağlama süresini (2) kabul eder, çünkü MRP negatif gün sağlama süresi ve dinamik negatif gün sağlama süresi arasındaki maksimum değeri dikkate alır. Bu durumda, sonuç bu olay için A olayında elde edilen sonuçla aynıdır.

Aşağıdaki çizim, bu olayda ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Olay C senaryo 3 için grafik görünümü](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Olay D: Yalnızca dinamik negatif günleri kullan

Negatif günleri **0**'a (sıfır) ayarlarsanız ve yalnızca dinamik negatif günler zaman dilimini kullanırsanız dinamik negatif günler zaman dilimi 6 + 0 – 7 = -1 gündür. Bu olayda sistem, sağlama süresinin (2) olumsuz gün olduğunu kabul eder. Bu durumda, sonuç bu olay için A olayında elde edilen sonuçla aynıdır ve aynı dezavantajlara sahiptir. Oluşun grafiksel görünüm için bkz. senaryo 2 için olay A.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Olay E: Hem maddenin teslim süresinden daha fazla olan negatif günleri hem de dinamik negatif günlerin zaman dilimlerini kullanın

Bu olay 1 ve 2 numaralı senaryolar için E olayı ile aynıdır. Temelde aynı avantajlara ve dezavantajlara sahiptir.

## <a name="conclusion"></a>Sonuç

Bu konudaki üç senaryonun gösterdiği gibi, negatif günleri karşılama grubundaki maddelerin sağlama zamanından daha büyük bir sayıya ayarlamak iyi bir fikirdir. Yalnızca dinamik negatif günler kullanmak ve negatif günleriniz varsa yeni stok yenilemeyi sipariş etmeden önce beklemek istediğiniz gün sayısına göre negatif günleri ayarlamak da iyi bir fikirdir (başka bir deyişle, Talebi daha da geciktirmek istediğiniz gün sayısı). Ayrıca, aynı kapsam grubundaki maddeler benzer sağlama sürelerine sahip olmalıdır.

Negatif günleri **0**' a (sıfır) ayarlarsanız ve dinamik negatif günler kullanmazsanız MRP, talebi karşılamak için her zaman yeni bir planlı sipariş oluşturur. Bu durumda, stok biriktirmediğinizden emin olmak için eylem iletileriyle çalışmanız önemlidir.

Negatif günleri uzun bir zaman dilimine ayarlamak ve sonra da eylem iletileriyle çalışmak isteyebilirsiniz. Bu yaklaşım iyi planlama sonuçları verir, ancak aynı zamanda biraz daha yavaştır. Eylem iletilerini çözümlemeniz ve uygulamanız gerektiğinden, analiz etmek daha zor olabilir. Aşağıda bir örnek verilmiştir:

- DemoProduct maddesinin altı günlük bir satınalma sağlama süresi vardır.
- Sıfırıncı günde (1 Ocak), DemoProduct maddesi için stok 0'dır (sıfır).
- Sıfırıncı günde (1 Ocak), DemoProduct öğesinin 10'u miktarında bir satış siparişi alırsınız.
- 10. günde (10 Ocak), DemoProduct öğesinin 10'u miktarında bir satış siparişi alırsınız.
- 12 (12 Ocak) numaralı günde, DemoProduct öğesinin 10'u miktarında bir satınalma siparişi vardır.
- Negatif günler, maddenin sağlama zamanından çok daha fazla olacak şekilde **20** olarak ayarlanır.

Aşağıdaki çizim, ne yaşandığının grafiksel bir görünümünü göstermektedir.

![Örneğin grafik incelemesi](./media/negative-days-19.png)

MRP aşağıdaki sonuçları verir.

![Sonuçlar](./media/negative-days-20.png)

Önceki ekran görüntüsünde, satış siparişi gereksinim tarihi 10 Ocak yerine 9 Ocak'tır. Bu ekran görüntüsü 2015 tarihinde çekildiği için, 10 Ocak Cumartesi günü olan MRP, gereksinim tarihini 9 Ocak Cuma olan bir önceki çalışma gününe taşındı.

MRP, ilk satış siparişi tarafından talep edilen talebi yerine getirmek için planlı bir satınalma siparişi oluşturur, ancak varolan satınalma siparişini ilerletebileceğiniz ve bu sipariş miktarını artırabileceğiniz için planlı siparişi iptal etmeniz de önerilmektedir.

Sonuçlar yanlış, ancak MRP'nin tüm gecikmeleri ve önerileri oluşturması gerektiğinden, otomatik olarak çalışma süresi daha uzun olabilir. Ek olarak, planlayıcının MRP sonuçlarını anlaması için daha fazla süre gerekebilir. En önemlisi bu olayda, planlayıcının eylem iletilerini anlaması ve kullanması önemlidir.

Negatif günleri maddenin sağlama süresine daha yakın bir sayıya kadar azaltırsanız ve dinamik negatif günler kullanırsanız, MRP aşağıdaki sonuçları verir.

![Sonuçlar](./media/negative-days-21.png)

MRP, ilk satış siparişine iliştirilmiş bir planlı sipariş oluşturur. Daha sonra, beklenildiği gibi, ikinci satış siparişi negatif günler ayarına göre varolan satınalma siparişine karşı iliştirilir. Bu planlama sonucu da doğrudur ve MRP için çalışma süresi daha kısa olabilir. Bu olayda, eylem iletileriyle nasıl çalışacağının anlaşılması ve bilinmesi gerekli değildir.

İşletmeniz için doğru değerlerin girildiğinden emin olmanıza yardımcı olmak için hem işlevsellik hem de MRP çalışma süresi açısından düşünmeniz gerekir. Bu nedenle, en iyi değerleri belirlemek için biraz deneme ve hata işlemi kullanabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

Daha fazla tartışma için orijinal [(Dinamik) negarif günler hakkında daha fazla](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/) web günlüğü dosyasına bakın.
