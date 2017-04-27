---
title: "Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-17 15 - 15 - 52
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 1afd7855fd05d0bacb60a7a45bba68e7041a4f4b
ms.lasthandoff: 03/29/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama



Bir stok kapanışı gerçekleştirdiğinizde, tüm girişler alınan toplam miktarı ve değeri kapsayan bir sanal çıkışa karşı kapatılır. Bu sanal çıkışın, çıkışların kapatılmasını sağlayan bir karşılık gelen sanal girişi bulunmaktadır. Bu şekilde, tüm çıkışlar aynı ortalama maliyeti alacaktır. Sanal çıkış ve giriş ağırlıklı ortalama stok kapanışı transferi olarak adlandırılan bir sanal transfer olarak görülebilir.
Yalnızca tek bir giriş varsa, tüm çıkışlar bundan kapatılabilir ve sanal transfer oluşturulamaz. Ağırlıklı ortalamayı kullandığınızda, ağırlıklı ortalama kuralını kullanmak yerine, stok hareketlerini belirli bir madde girişinin belirli bir çıkışa karşı kapatılmasını sağlayacak şekilde işaretleyebilirsiniz. Ağırlıklı ortalama stok modelini kullandığınızda aylık stok kapanışını kullanmanızı öneririz. Ağırlıklı ortalama stok kapanışı yöntemi aşağıdaki formüle göre hesaplanır:
-   Ağırlıklı ortalama = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Stok çıkışlarını terk eden stok hareketleri. Buna satış emirleri, stok günlükleri ve üretim emirleri dahildir, deftere nakil tarihinde tahmini bir maliyet fiyatında gerçekleşir. Bu tahmini maliyet fiyatına cari ortalama da denir. Stok kapanışı zamanında, sistem önceki ve geçerli dönemlerin stok hareketlerini analiz eder ve aşağıdaki kapanış ilkelerinden hangisinin kullanılması gerektiğini belirler.
-   Doğrudan kapatma
-   Özetlenmiş kapatma

Kapatmalar, kapanış tarihin ağırlıklı ortalamasını düzeltmek için çıkışları ayarlayan stok kapanışı deftere nakilleridir. Aşağıdaki örnekler, beş farklı yapılandırma ile ağırlıklı ortalama kullanmanın etkisini gösterir:
-   Fiziksel değeri dahil et seçeneği olmadan ağırlıklı ortalama doğrudan kapatma
-   Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama özetlenmiş kapatma
-   Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama doğrudan kapatma
-   Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama özetlenmiş kapatma
-   İşaretleme ile ağırlıklı ortalama

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama doğrudan kapatma
Doğrudan kapatma ilkesi, daha eski sürümlerde kullanılan ağırlıklı ortalama için olanla aynıdır. Sistem doğrudan giriş ve çıkışlar arasında kapatır. Sistem bu doğrudan kapatma ilkesini belirli durumlarda kullanır:
-   Dönem içinde bir giriş ve bir veya daha fazla çıkış deftere nakledildiğinde
-   Dönem içinde yalnızca çıkışlar deftere nakledildiğinde ve stok önceki kapanıştan eldeki maddeleri içerdiğinde

Aşağıdaki senaryoda, mali olarak güncelleştirilmiş giriş ve çıkış deftere nakledilmiştir. Stok kapanışı sırasında, sistem, girişi doğrudan çıkışa karşılık kapatır ve çıkışta maliyet fiyatı için bir ayarlama yapılması gerekmez. Aşağıdaki hareketler grafikte gösterilmektedir.
-   1a. Her biri 10,00 ABD Doları'ndan 5 miktarı için güncelleştirilen stok fiziksel girişi
-   1b. Her biri 10,00 ABD Doları'ndan 5 miktarı için güncelleştirilen stok mali girişi
-   2a. Her biri 10,00 ABD Doları'ndan 2 miktarı için güncelleştirilen stok fiziksel çıkışı
-   2b. Her biri 10,00 ABD Doları'ndan 2 miktarı için güncelleştirilen stok mali çıkışı
-   3. Stok kapanışı, stok mali girişini stok mali çıkışına kapatmak için doğrudan kapatma yöntemi kullanılarak gerçekleştirilir.

Aşağıdaki diyagramda, bu hareketler serisi, Ağırlıklı ortalama stok modeli ve Fiziksel değeri dahil et seçeneği kullanılmadan doğrudan kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir. ![Fiziksel Değeri Dahil Et Seçeneği Kullanılmadan Ağırlıklı Ortalama Doğrudan Kapatma    ](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) Diyagram anahtarı
-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unitprice biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantez içinde olmayan bir stok hareketi değeri, stok hareketinin mali olarak stoka nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketine yeni bir etiket atanır.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve Stok Kapanışı etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden noktalı kırmızı oklarla temsil edilir.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği kullanılmadan ağırlıklı ortalama özetlenmiş kapatma
Ağırlıklı ortalama, kapanış dönemi dahilindeki tüm girişlerin Ağırlıklı ortalama stok kapanışı denilen bir harekette özetlendiği kapatma ilkesini kullanır. Dönemdeki tüm girişler, yeni oluşturulan stok transfer hareketinin çıkışına karşılık kapatılır. Dönemin tüm çıkışları, yeni stok transfer hareketinin girişine karşılık kapatılır. Eldeki stok, stok kapanışından sonra pozitifse, bu eldeki stok ve stok değeri yeni stok transfer hareketinde (giriş) özetlenir. Eldeki stok, stok kapanışından sonra negatifse, eldeki stok ve stok değeri tam kapatılmamış bireysel çıkışların toplamıdır. Aşağıdaki senaryoda birçok mali olarak güncelleştirilmiş giriş ile bir çıkış deftere nakledilmiştir. Stok kapanışı sırasında, sistem özetlenmiş stok transferi hareketini oluşturup nakleder ve dönemin tüm girişlerini özetlenmiş stok transferi çıkış hareketine karşılık kapatır. Dönem için deftere nakledilen tüm çıkışlar, özetlenmiş stok transferi giriş hareketine karşılık kapatılır. Ağırlıklı ortalama 15,00 ABD Doları olarak hesaplanır. Çıkış özgün olarak 14,67 ABD doları tutarındaki bir tahmini maliyet fiyatı ile deftere nakledilmiştir. Dolayısıyla, çıkışta negatif 0,33 ABD doları tutarında bir düzeltme oluşturulup deftere nakledilir. Stok kapanış tarihi itibariyle, eldeki stok 45,00 ABD Doları değeri ile 3 parçadır. Aşağıdaki hareketler aşağıdaki grafikte gösterilmektedir:
-   1a. Her biri 11,00 ABD Doları maliyetinde 2 miktarı için güncelleştirilen stok fiziksel girişi.
-   1b. Her biri 14,00 ABD Doları maliyetinde 2 miktarı için güncelleştirilen stok mali girişi.
-   2a. Her biri 12,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   2b. Her biri 16,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali girişi.
-   3a. Her biri 14,67 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel çıkışı (cari ortalama).
-   3b. Her biri 14,67 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali çıkışı (cari ortalama).
-   4a. Her biri 14,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   4b. Her biri 16,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali girişi.
-   5. Stok kapanışı gerçekleştirilir.
-   6a. Tüm stok mali girişlerinin kapatmalarını toplamak için “Ağırlıklı ortalama stok kapanışı hareketi” mali çıkışı oluşturulur.
-   6b. 5a için mahsup olarak “Ağırlıklı ortalama stok kapanış hareketi” mali girişi oluşturulur.

Aşağıdaki diyagramda, bu hareketler serisi, Ağırlıklı ortalama stok modeli ve Fiziksel değeri dahil et seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir. ![Fiziksel Değeri Dahil Et Seçeneği Kullanılmadan Ağırlıklı Ortalama Özet Kapatma    ](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) Diyagram anahtarı
-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unitprice biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantez içinde olmayan bir stok hareketi değeri, stok hareketinin mali olarak stoka nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketine yeni bir etiket atanır.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve Stok Kapanışı etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden noktalı kırmızı oklarla temsil edilir.
-   Kırmızı oklar, sistem tarafından oluşturulan çıkış hareketine karşılık kapatılmakta olan giriş hareketlerini gösterir.
-   Yeşil ok, orijinal olarak nakledilmiş çıkış hareketinin kapatıldığı sistem tarafından oluşturulmuş mahsup giriş hareketini temsil eder

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama doğrudan kapatma
Fiziksel değeri dahil et parametresi ağırlıklı ortalama stok modeli ile, ürünün daha eski sürümlerinde olduğundan farklı şekilde çalışır. Madde modeli grubu formunda bir madde için Fiziksel değeri dahil et kutusunu seçin. Ardından sistem tahmini maliyet fiyatını veya cari ortalamayı hesaplarken fiziksel olarak güncelleştirilen girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatına dayanarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır. Ağırlıklı ortalama stok modelini kullanırken aylık bir stok kapanışı öneririz. Bu ağırlıklı ortalama doğrudan kapatma örneğinde, madde modeli grubu fiziksel değeri içerecek şekilde işaretlenmiştir. Aşağıdaki hareketler aşağıdaki grafikte gösterilmektedir:
-   1a. Her biri 11,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali girişi.
-   2a. Her biri 15,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   3a. Her biri 12,50 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel çıkışı (fiziksel giriş değeri hesaba katıldığından cari ortalama maliyeti).
-   3b. Her biri 12,50 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali çıkışı (fiziksel giriş değeri hesaba katıldığından cari ortalama maliyeti).
-   4. Stok kapanışı gerçekleştirilir. Stok kapanışı sırasında, sistem yalnızca fiziksel olarak güncelleştirilmiş tüm stok hareketlerini göz ardı eder. Bunun yerine, doğrudan kapatma ilkesi kullanılır. Stok kapanış tarihi itibariyle mali olarak çıkarılmış stok hareketine 2,50 ABD Doları tutarında bir düzeltme nakledilir. Stok kapanışından sonra eldeki stok, 15,00 ABD Doları cari ortalama maliyet fiyatında 1 miktarında olur.

Aşağıdaki diyagramda, bu hareketler serisi, Ağırlıklı ortalama stok modeli ve Fiziksel değeri dahil et seçeneği ile doğrudan kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir. ![Fiziksel Değeri Dahil Et Seçeneği ile Ağırlıklı Ortalama Doğrudan Kapatma](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) Diyagram anahtarı
-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unitprice biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantez içinde olmayan bir stok hareketi değeri, stok hareketinin mali olarak stoka nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketine yeni bir etiket atanır.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve Stok Kapanışı etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden noktalı kırmızı oklarla temsil edilir.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Fiziksel değeri dahil et seçeneği ile ağırlıklı ortalama özetlenmiş kapatma
Fiziksel değeri dahil et parametresi, ağırlıklı ortalamayla, daha eski sürümlerdekinden farklı şekilde çalışır. Madde modeli grubu sayfasında bir madde için Fiziksel değeri dahil et kutusunu seçin. Ardından sistem tahmini maliyet fiyatını veya cari ortalamayı hesaplarken fiziksel olarak güncelleştirilen girişleri kullanır. Çıkışlar dönem sırasında bu tahmini maliyet fiyatına dayanarak deftere nakledilir. Stok kapanışı sırasında mali olarak güncelleştirilmiş girişler yalnızca ağırlıklı ortalama hesaplamasında hesaba katılır. Ağırlıklı ortalama stok modelini kullanırken aylık bir stok kapanışı öneririz. Bu ağırlıklı ortalama özetlenmiş kapatma örneğinde, stok modeli grubu fiziksel değeri içerecek şekilde işaretlenmiştir. Aşağıdaki hareketler aşağıdaki grafikte gösterilmektedir:
-   1a. Her biri 11,00 ABD Doları maliyetinde 2 miktarı için güncelleştirilen stok fiziksel girişi.
-   1b. Her biri 14,00 ABD Doları maliyetinde 2 miktarı için güncelleştirilen stok mali girişi.
-   2. Her biri 10,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   3a. Her biri 12,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   3b. Her biri 16,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali girişi.
-   4a. Her biri 13,50 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel çıkışı (fiziksel giriş değeri hesaba katıldığından cari ortalama maliyeti).
-   4b. Her biri 13,50 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali çıkışı (fiziksel giriş değeri hesaba katıldığından cari ortalama maliyeti).
-   5a. Her biri 14,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok fiziksel girişi.
-   5b. Her biri 16,00 ABD Doları maliyetinde 1 miktarı için güncelleştirilen stok mali girişi.
-   6. Stok kapanışı gerçekleştirilir. Stok kapanışı sırasında, sistem yalnızca fiziksel olarak güncelleştirilen tüm stok hareketlerini göz ardı eder. Yalnızca bir mali giriş olduğundan özetlenmiş kapatma ilkesi kullanılır. Stok kapanış tarihi itibariyle mali olarak çıkarılmış stok hareketine 1,50 ABD Doları tutarında bir düzeltme nakledilir. Stok kapanışından sonra eldeki stok, 15,00 ABD Doları cari ortalama maliyet fiyatında 3 miktarında olur.
-   7a. Tüm stok mali girişlerinin kapatmalarını toplamak için “Ağırlıklı ortalama stok kapanışı hareketi” mali çıkışı oluşturulur.
-   7b. 5a için mahsup olarak “Ağırlıklı ortalama stok kapanış hareketi” mali girişi oluşturulur.

Aşağıdaki diyagramda, bu hareketler serisi, ağırlıklı ortalama stok modeli ve Fiziksel değeri dahil et seçeneği kullanılmadan özetlenmiş kapatma ilkesi seçimlerinin etkileriyle birlikte gösterilmektedir. ![Fiziksel Değeri Dahil Et Seçeneği ile Ağırlıklı Ortalama Özet Kapatma    ](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) Diyagram anahtarı
-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unitprice biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantez içinde olmayan bir stok hareketi değeri, stok hareketinin mali olarak stoka nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketine yeni bir etiket atanır.
-   Her dikey ok, 1a gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve Stok Kapanışı etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden noktalı kırmızı oklarla temsil edilir.
-   Kırmızı oklar, sistem tarafından oluşturulan çıkış hareketine karşılık kapatılmakta olan giriş hareketlerini gösterir.
-   Yeşil ok, orijinal olarak nakledilmiş çıkış hareketinin kapatıldığı sistem tarafından oluşturulmuş mahsup giriş hareketini temsil eder

## <a name="weighted-average-with-marking"></a>İşaretleme ile ağırlıklı ortalama
İşaretleme bir hareket giriş hareketini bağlamanıza, işaretlemenize veya vermenize olanak sağlayan bir işlemdir. İşaretleme bir hareket nakledilmeden önce veya nakledildikten sonra gerçekleşebilir. İşaretlemeyi, hareket deftere nakledildiğinde veya stok kapanışı gerçekleştirildiğinde stokun tam maliyetinden emin olmak istediğinizde kullanabilirsiniz. Örneğin, Müşteri Servisi departmanınız önemli bir müşteriden bir acele sipariş kabul etti. Bu acele bir sipariş olduğundan, müşterinizin gereksinimlerini karşılamak için bu madde için daha fazla ödemeniz gerekecek. Bu stok maddesinin bu satış emri faturası için marja veya satılan malların maliyetine yansıtılacağından emin olmanız gerekir. Satınalma siparişi deftere nakledildiğinde stok girişi 120,00 ABD Doları maliyetinde yapılır. Örneğin, bu satış emri belgesi satınalma emrine sevk irsaliyesi veya fatura deftere nakledilmeden önce işaretlenmiştir. Ardından SMM, maddenin cari ortalama maliyeti yerine 120,00 ABD doları olacaktır. Satış siparişi sevk irsaliyesi veya faturası işaretlemeden önce nakledilirse satılan malların maliyeti cari ortalama maliyet fiyatında nakledilir. Stok kapanışı gerçekleştirilmeden önce bu iki hareket birbirine işaretlenmeye devam edebilir. Bir giriş hareketi bir çıkış hareketine işaretlenir. Ardından maddenin madde modeli grubu için seçilen değerlendirme yöntemi göz ardı edilir ve sistem bu hareketleri birbirine karşılık kapatır. Hareketin deftere nakledilmeden önce bir giriş için bir çıkış hareketi işaretleyebilirsiniz. Bunu Satış emri ayrıntıları sayfasındaki bir satış emri satırından yapabilirsiniz. Açık giriş hareketleri, işaretleme sayfasında görüntülenebilir. Hareket deftere nakledildikten sonra bir giriş için bir çıkış hareketi işaretleyebilirsiniz. Deftere nakledilmiş bir stok ayarlama günlüğünden, stoklanmış bir madde için açık bir giriş hareketine yönelik bir çıkış hareketini eşleştirebilir veya işaretleyebilirsiniz. Aşağıdaki hareketler aşağıdaki grafikte gösterilmektedir:
-   1a. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   1b. Her biri 10,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   2a. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   2b. Her biri 20,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   3a. Her biri 25,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4a. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok fiziksel girişi.
-   4b. Her biri 30,00 ABD Doları maliyetinde 1 miktarındaki stok mali girişi.
-   5a. 21,25 ABD Doları maliyet fiyatında 1 miktarındaki stok fiziksel çıkışı (mali ve fiziksel olarak güncelleştirilmiş hareketlerin cari ortalaması).
-   5b. 1 miktarındaki stok mali çıkışı hareket deftere nakledilmeden önce stok girişi 2b'ye işaretlenir. Hareket, 20,00 ABD Doları maliyet fiyatı ile deftere nakledilir.
-   6a. Her biri 21,25 ABD Doları maliyet fiyatındaki 1 miktarındaki stok fiziksel çıkışı.
-   7. Stok kapanışı gerçekleştirilir. Mali olarak güncelleştirilen hareket varolan bir girişe işaretlendiğinden, bu hareketler birbirine karşılık kapatılır ve bir düzeltme yapılmaz.

Yeni cari ortalama maliyet fiyatı 27,50 ABD Doları tutarındaki mali ve fiziksel olarak güncelleştirilmiş hareketlerin ortalamasını yansıtır. Aşağıdaki diyagram bu hareketler serisini, işaretleme ile Ağırlıklı ortalama stok modeli seçmenin etkileriyle birlikte gösterir. ![İşaretleme ile Ağırlıklı Ortalama    ](./media/weightedaveragewithmarking.gif) Diyagram anahtarı
-   Stok hareketleri dikey oklarla temsil edilir.
-   Stoka yapılan girişler zaman çizgisinin üzerinde dikey oklarla temsil edilir.
-   Stoktan yapılan çıkışlar zaman çizgisinin altında dikey oklarla temsil edilir.
-   Her dikey okun üstünde (veya altında), stok hareketinin değeri Miktar Quantity@Unitprice biçiminde belirtilir.
-   Parantezler içinde gösterilen bir stok hareketi değeri, stok hareketinin stoka fiziksel olarak nakledildiğini gösterir.
-   Parantez içinde olmayan bir stok hareketi değeri, stok hareketinin mali olarak stoka nakledildiğini gösterir.
-   Her yeni giriş veya çıkış hareketine yeni bir etiket atanır.
-   Her dikey ok, *1a* gibi bir sıra tanımlayıcısıyla etiketlenir. Tanımlayıcılar, zaman çizgisindeki hareket nakillerinin sırasını belirtir.
-   Stok kapanışları, kırmızı dikey bir kesikli çizgiyle ve Stok Kapanışı etiketiyle temsil edilir.
-   Stok kapanışıyla gerçekleştirilen kapatmalar, bir girişten çıkışa çapraz olarak giden noktalı kırmızı oklarla temsil edilir.




