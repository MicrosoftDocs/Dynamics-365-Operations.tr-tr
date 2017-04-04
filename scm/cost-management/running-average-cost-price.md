---
title: "Cari ortalama maliyet fiyatı"
description: "Çıkış hareketleri için giriş hareketlerini, maddenin madde model grubunda seçili stok değerleme yöntemi temel stok kapatma işlemi kapatır. Ancak, stok kapanışı çalıştırmadan önce sistem çıkış hareketleri deftere naklettiğinizde, genel olarak kullanılan bir ortalama maliyet fiyatı hesaplar."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Cari ortalama maliyet fiyatı

Çıkış hareketleri için giriş hareketlerini, maddenin madde model grubunda seçili stok değerleme yöntemi temel stok kapatma işlemi kapatır. Ancak, stok kapanışı çalıştırmadan önce sistem çıkış hareketleri deftere naklettiğinizde, genel olarak kullanılan bir ortalama maliyet fiyatı hesaplar.

Sistem aşağıdaki formülü kullanarak bir madde için ortalama maliyet fiyatı çalışan bu tahminleri: tahmini Fiyat = (fiziksel tutar + mali tutarı) ÷ (fiziksel miktar + mali miktarı)

## <a name="using-the-running-average-cost-price"></a>Cari ortalama maliyet fiyatını kullanma
Ortalama maliyet fiyatı'nı kullanarak sistem stok hareketleri ne zaman nakleder ve maliyet fiyatı madde ana kayıt üzerinde tanımlanan kullandığında aşağıdaki tabloda gösterilmektedir.

| Koşul                                               | Sistem tahmini ortalama maliyet fiyatı kullanır. | Maliyet fiyatı madde Yöneticisinde tanımlanan sistem kullanır |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Her iki pay\* ve payda\*\* pozitif olan.  | Evet                                                      | Hayır                                                                |
| Pay\*, payda\*\*, ya da her ikisi de negatif. | Hayır                                                       | Evet                                                               |
| Payda\*\* 0 (sıfır)'dır.                        | Hayır                                                       | Evet                                                               |

\*Pay (fiziksel tutar + mali tutarı) = \*\*payda = (Fiili miktar + mali miktarı) **Not:**, **fiziksel değeri dahil et** bir madde için seçeneği seçili değilse, sistem fiziksel tutar ve fiziksel miktarı için 0 (sıfır) kullanır. Bu seçenek hakkında daha fazla bilgi için, bkz. [Fiziksel değeri dahil et](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Fiyat yükselmesinden kaçınma
Yeterli giriş fiyatı için temel olan önce çok seyrek olarak çeşitli sorunları sistem fiyatları. Bu senaryo, cari ortalama maliyet fiyatı tahmininde aşırı şişmeye neden olabilir. Ancak, fiyat yükselmesinden kaçınmak veya olduğu zaman etkilerini azaltmak için alabileceğiniz önlemler vardır. **Senaryo** **Fiziksel değeri dahil et** seçeneğini belirlediğiniz bir madde için aşağıdaki hareketler gerçekleşir:

1.  Mali olarak 100,00 Amerikan dolarında 100 miktarını alırsınız.
2.  Mali olarak 200 miktarını çıkarırsınız.
3.  Fiziksel olarak 202,00 Amerikan dolarında 101 miktarını alırsınız.

Bir madde için tahmini cari ortalama maliyet fiyatını incelediğinizde, 1,51 Amerikan doları maliyet fiyatı beklersiniz. Bunun yerine, bir tahmini Bul aşağıdaki formüle göre USD 102.00, ortalama çalışan: tahmini fiyat = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 200 öğeleri adım 2'de mali olarak verildiğinde, karşılık gelen bir giriş varsa önce sistem 100 maddelerin fiyat gerekir çünkü bu fiyatlandırma yükseltme oluşur. Bu durum, negatif stok sonucunu doğurur. Tahmin edebileceiniz gibi sistem sonra birim fiyatı, USD 1.00 olarak tahmin eder. Ancak karşılık gelen 100 giriş geldiğinde, her birinin birim fiyatı 2,00 Amerikan doları olur. **Not:** Çıkışlar negatif stok oluşturmasına rağmen, çıkış fiyatı hesaplandığında stok pozitiftir. Madde masterındaki fiyat yerine cari ortalama maliyet fiyatının kullanılmasının nedeni budur. Bu noktada, stok değeri uzaklığına USD 100.00 sistemi vardır. Bu mahsup 100 parça üzerinden oluşturulmuş olsa da, her biri 1,00 Amerikan dolarlık bir birim mahsup olduğunda artık yalnızca tek parça stokumuz olur. Bu nedenle, bu tek parçaya 100,00 Amerikan dolarlık bir mahsup tahsis edilir. Sonuç, aşırı şişirilmiş maliyet fiyatıdır. **Not:** Karşılaştırma için, senaryodaki 2. ve 3. adımlar yer değiştirdiğinde 1,51 Amerikan dolarlık bir birim fiyatına 200 maddenin çıkarılacağını ve bir parçanın 1,51 Amerikan doları birim fiyatında kalacağını görebilirsiniz. Bu fiyat yükseliş senaryosu negatif stok durumunda gerçekleşebildiğinden, aşağıdaki durumlarda kaçınılması zordur:

-   Çıkış fiyatlarını eldeki değer ve miktarda tahmin etmeniz gerekiyorsa.
-   Çıkış ve girişlerde eldeki değeri ve miktarı ayarlamanız gerekiyorsa.
-   İş modeliniz elinizde olandan daha çok parçayı göndermenize veya fiyatlandırmanıza olanak veriyorsa.
-   Size gönderilen giriş değerini ve miktarını kabul etmeniz gerekiyorsa.

İş modeliniz bunlara olanak verse de, aşağıdaki uygulamalar fiyat yükseliş senaryosuna neden olabilecek negatif miktarların oluşmasını engellemenize yardımcı olabilir:

-   Bir madde için **Fiziksel değeri dahil et** seçeneğini belirlerseniz, **Madde model grupları** sayfasındaki **Fiziksel negatif stok** onay kutusunun seçimini kaldırın.
-   Bir madde için **Fiziksel değeri dahil et** seçeneğini *belirlemezseniz*, **Madde model grupları** sayfasındaki **Mali negatif stok** onay kutusunun seçimini kaldırın.

Ayrıca, fiziksel stok değerinizdeki maksimum mahsubun, fiziksel hareket sayısı ile fiziksel ve mali fiyatlar arasındaki farkla sınırlı olduğunu aklınızda bulundurun. Tüm fiziksel hareketler sonunda mali olarak güncelleştirildiği sürece fiziksel değer aşırı düzeylere yükselemez. Son olarak, biriken mahsup sadece tek parça yerine eldeki birden çok parça üzerine dağıtıldığında, yükselmenin etkisi önemli ölçüde azalır.


