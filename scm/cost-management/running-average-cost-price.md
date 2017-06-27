---
title: "Cari ortalama maliyet fiyatı"
description: "Stok kapanışı işlemi, maddenin madde modeli grubunda seçilen stok değerleme yöntemine dayanarak çıkış hareketlerini giriş hareketlerine karşılık kapatır. Ancak, stok kapanışı çalıştırılmadan önce, sistem çoğu durumda çıkış hareketlerini deftere nakletmek için kullanılan bir cari ortalama maliyet fiyatı hesaplar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a73ce12f1064c44b2af0fa4f33c63f1a6bddab89
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="running-average-cost-price"></a>Cari ortalama maliyet fiyatı

[!include[banner](../includes/banner.md)]


Stok kapanışı işlemi, maddenin madde modeli grubunda seçilen stok değerleme yöntemine dayanarak çıkış hareketlerini giriş hareketlerine karşılık kapatır. Ancak, stok kapanışı çalıştırılmadan önce, sistem çoğu durumda çıkış hareketlerini deftere nakletmek için kullanılan bir cari ortalama maliyet fiyatı hesaplar.

Sistem, aşağıdaki formülü kullanarak maddenin söz konusu yürütülen ortalama maliyet fiyatını tahmin eder: 

Tahmini fiyat = (Fiziksel tutar + Mali tutar) ÷ (Fiziksel miktar + Mali miktar)

## <a name="using-the-running-average-cost-price"></a>Cari ortalama maliyet fiyatını kullanma
Aşağıdaki tabloda sistemin ne zaman stok hareketlerini cari ortalama maliyet fiyatını kullanarak deftere naklettiği ve ne zaman madde master kaydında tanımlı maliyet fiyatını kullandığı gösterilmiştir.

| Koşul                                               | Sistem, tahmini cari ortalama maliyet fiyatını kullanır | Sistem, madde masterında tanımlanan maliyet fiyatını kullanır |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Hem pay\* hem de payda\*\* pozitiftir.  | Evet                                                      | Hayır                                                                |
| Pay\*, payda\*\* veya her ikisi de negatiftir. | Hayır                                                       | Evet                                                               |
| Payda\*\* 0'dır (sıfır).                        | Hayır                                                       | Evet                                                               |

\* Pay = (Fiziksel tutar + Mali tutar) \*\* Payda = (Fiziksel miktar + Mali miktar) 

**Not:** Bir madde için **Fiziksel değeri dahil et** seçeneği seçilmezse, sistem hem fiziksel tutar hem de fiziksel miktar için 0 (sıfır) kullanır. Bu seçenek hakkında daha fazla bilgi için, bkz. [Fiziksel değeri dahil et](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Fiyat yükselmesinden kaçınma
Bazı nadir durumlarda sistem fiyat için temel alacağı yeterli girişe sahip olmadan birkaç çıkış fiyatlandırır. Bu senaryo, cari ortalama maliyet fiyatı tahmininde aşırı şişmeye neden olabilir. Ancak, fiyat yükselmesinden kaçınmak veya olduğu zaman etkilerini azaltmak için alabileceğiniz önlemler vardır. **Senaryo** **Fiziksel değeri dahil et** seçeneğini belirlediğiniz bir madde için aşağıdaki hareketler gerçekleşir:

1.  Mali olarak 100,00 Amerikan dolarında 100 miktarını alırsınız.
2.  Mali olarak 200 miktarını çıkarırsınız.
3.  Fiziksel olarak 202,00 Amerikan dolarında 101 miktarını alırsınız.

Bir madde için tahmini cari ortalama maliyet fiyatını incelediğinizde, 1,51 Amerikan doları maliyet fiyatı beklersiniz. Bunun yerine, şu formüle dayalı olarak 102,00 Amerikan dolarlık bir tahmini cari ortalama bulursunuz: Tahmini fiyat = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 Bu fiyat yükselmesinin gerçekleşme sebebi, 2. adımda 200 madde mali olarak çıkarıldığında, sistemin maddelerden 100'ünü karşılık gelen girişe sahip olmadan önce fiyatlandırmak zorunda olmasıdır. Bu durum, negatif stok sonucunu doğurur. Ardından, sistem, bekleyebileceğimiz gibi 1,00 Amerikan dolarlık bir birim fiyatı tahmin eder. Ancak karşılık gelen 100 giriş geldiğinde, her birinin birim fiyatı 2,00 Amerikan doları olur. 

**Not:** Çıkışlar negatif stok oluşturmasına rağmen, çıkış fiyatı hesaplandığında stok pozitiftir. Madde masterındaki fiyat yerine cari ortalama maliyet fiyatının kullanılmasının nedeni budur. Bu noktada, sistemdeki stok mahsup değeri 100,00 USD'dir. Bu mahsup 100 parça üzerinden oluşturulmuş olsa da, her biri 1,00 Amerikan dolarlık bir birim mahsup olduğunda artık yalnızca tek parça stokumuz olur. Bu nedenle, bu tek parçaya 100,00 Amerikan dolarlık bir mahsup tahsis edilir. Sonuç, aşırı şişirilmiş maliyet fiyatıdır. 

**Not:** Karşılaştırma için, senaryodaki 2. ve 3. adımlar yer değiştirdiğinde 1,51 Amerikan dolarlık bir birim fiyatına 200 maddenin çıkarılacağını ve bir parçanın 1,51 Amerikan doları birim fiyatında kalacağını görebilirsiniz. Bu fiyat yükseliş senaryosu negatif stok durumunda gerçekleşebildiğinden, aşağıdaki durumlarda kaçınılması zordur:

-   Çıkış fiyatlarını eldeki değer ve miktarda tahmin etmeniz gerekiyorsa.
-   Çıkış ve girişlerde eldeki değeri ve miktarı ayarlamanız gerekiyorsa.
-   İş modeliniz elinizde olandan daha çok parçayı göndermenize veya fiyatlandırmanıza olanak veriyorsa.
-   Size gönderilen giriş değerini ve miktarını kabul etmeniz gerekiyorsa.

İş modeliniz bunlara olanak verse de, aşağıdaki uygulamalar fiyat yükseliş senaryosuna neden olabilecek negatif miktarların oluşmasını engellemenize yardımcı olabilir:

-   Bir madde için **Fiziksel değeri dahil et** seçeneğini belirlerseniz, **Madde model grupları** sayfasındaki **Fiziksel negatif stok** onay kutusunun seçimini kaldırın.
-   Bir madde için **Fiziksel değeri dahil et** seçeneğini *belirlemezseniz*, **Madde model grupları** sayfasındaki **Mali negatif stok** onay kutusunun seçimini kaldırın.

Ayrıca, fiziksel stok değerinizdeki maksimum mahsubun, fiziksel hareket sayısı ile fiziksel ve mali fiyatlar arasındaki farkla sınırlı olduğunu aklınızda bulundurun. Tüm fiziksel hareketler sonunda mali olarak güncelleştirildiği sürece fiziksel değer aşırı düzeylere yükselemez. Son olarak, biriken mahsup sadece tek parça yerine eldeki birden çok parça üzerine dağıtıldığında, yükselmenin etkisi önemli ölçüde azalır.




