---
title: Çakışan iskontoları için en uygun birleşimi belirleme
description: İskontolar çakıştığında, en düşük hareket toplamını veya en yüksek toplam iskontoyu oluşturacak çakışan iskonto birleşimi belirlemeniz gerekir. Yaygın olarak kullanılan '1 satın al, 1 al X yüzdesi' (BOGO) perakende iskontosunda olduğu gibi, iskonto tutarı satın alınan ürünlerin fiyatına göre değişiklik gösterdiğinde, bu işlem birleşimsel iyileştirme konusu durumuna gelir.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: eebb532071e7c6bae7cfae93bfe795e79bb16c63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "360705"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Çakışan iskontoları için en uygun birleşimi belirleme

[!include [banner](includes/banner.md)]

İskontolar çakıştığında, en düşük hareket toplamını veya en yüksek toplam iskontoyu oluşturacak çakışan iskonto birleşimi belirlemeniz gerekir. Yaygın olarak kullanılan '1 satın al, 1 al X yüzdesi' (BOGO) perakende iskontosunda olduğu gibi, iskonto tutarı satın alınan ürünlerin fiyatına göre değişiklik gösterdiğinde, bu işlem birleşimsel iyileştirme konusu durumuna gelir.

Bu makale, Microsoft Dynamics AX 2012 R3, KB 3105973 (yayınlanma tarihi 2 Kasım 2015) veya sonrası ve Microsoft Dynamics 365 for Retail için geçerlidir. Zamanında uygulayabilmek için çakışan iskonto karmasını belirlemek için, çakışan iskontoları uygulamak için bir yöntem geliştirdik. Bu yeni yönteme **Marjinal değer sıralaması**. Marjinal değer sıralaması, olası çakışan iskonto birleşimlerini değerlendirmek için gerekli süre, **Perakende parametreleri** sayfasında yapılandırılabilen eşiği aştığında kullanılır. Marjinal değer sıralama yönteminde, iskontonun paylaşılan ürünlerdeki değeri kullanılarak her çakışan iskonto için hesaplanır. Çakışan iskontolar, en yüksek göreli değerden en küçük göreli değere doğru uygulanır. Yeni yöntem hakkında daha fazla bilgi için bu makalenin ilerleyen kısımlarındaki "Marjinal değer" bölümüne bakın. Ürün iskonto tutarları hareketteki başka bir ürün tarafından etkilenmiyorsa, marjinal değer sıralaması kullanılmaz. Örneğin, bu yöntem iki basit iskonto veya bir basit iskonto ve tek bir ürün miktarı iskontosu için kullanılmaz.

## <a name="discount-examples"></a>İskonto örnekleri

Ortak bir ürün kümesi üzerinde sayısız perakende iskontosu oluşturabilirsiniz. Ancak, herhangi bir sınır olmadığından, çeşitli ürünlerde kullanılması gereken iskontoları hesaplamaya çalıştığınızda performans sorunları ortaya çıkabilir. Bu sorun daha ayrıntılı şekilde aşağıdaki örneklerde gösterilmektedir. Örnek 1'de, iki ürün ve çakışan iki iskontoyla başlıyoruz. Daha sonra örnek 2'de, daha fazla ürün eklendikçe sorunun nasıl değişeceğini gösteriyoruz.

### <a name="example-1-two-products-and-two-discounts"></a>Örnek 1: İki ürün ve iki iskonto

Bu örnekte, her iskonto için uygun olarak belirlenecek iki ürün gereklidir ve iskontolar birleştirilemez. Bu örnekteki iskontolar **En iyi fiyat** iskontolarıdır. Her iki ürün de her iki iskonto için uygundur. İki iskonto şunlardır.

![Çakışan iskonto karması 01](./media/overlapping-discount-combo-01.jpg)

Her iki ürün için de bu iki iskontodan en iyi olanı her iki ürünün fiyatına bağlıdır. Her iki ürünün fiyatı eşit veya birbirine çok yakın olduğunda iskonto 1 daha iyi bir seçenektir. Bir ürünün fiyatı diğer ürünün fiyatından belirgin şekilde daha az olduğunda iskonto 2 daha iyi bir seçenektir. Bu iki iskontoyu birbirine karşı değerlendirmek için matematiksel bir formül buradadır.

![Çakışan iskonto karması 02](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Ürün 1'in fiyatı, ürün 2'nin fiyatının üçte ikisine eşitse, iki iskonto eşittir. Bu örnekte, iskonto 1 için etkin iskonto yüzdesi, yüzde birkaç birim (iki ürünün fiyatı birbirinden farklı olduğunda) ile maksimum yüzde 25'e kadar (iki ürünün fiyatı aynı olduğunda) değişenlik gösterir. Etkin iskonto yüzdesi iskonto 2 için sabittir. Daima yüzde 20'dir. İskonto 1'in etkin iskonto yüzdesi iskonto 2'den daha fazla veya daha az olabilecek bir aralığa sahip olduğundan, en iyi iskonto iskonto yapılması gereken ürünlerin fiyatlarına bağlı olacaktır. Bu örnekte, yalnızca iki ürüne iki iskonto uygulanacağından, hesaplama hızlıca yapılmıştır. Yalnızca iki olası birleşim vardır: bir iskonto 1 uygulaması veya bir iskonto 2 uygulaması. Hesaplanacak permütasyon yoktur. Her iskontonun değeri her iki ürün kullanılarak hesaplanır ve en iyi indirim kullanılır.

### <a name="example-2-four-products-and-two-discounts"></a>Örnek 2: Dört ürün ve iki iskonto

Bundan sonra, dört ürün ve aynı iki iskontoyu kullanacağız. Her dört ürün de her iki iskonto için uygundur. Olası on iki birleşim vardır. Sonuç olarak, harekete üç birleşimden birinde iki iskonto uygulanacak: iki iskonto 1 uygulaması, iki iskonto 2 uygulaması veya bir iskonto 1 uygulaması ve bir iskonto 2 uygulaması. Olası birleşimleri göstermek için, farklı fiyatlara sahip dört üründen oluşan iki farklı kümeye bakacağız:

- Dört ürünün hepsi aynı fiyata sahip: $15,00. Bu durumda, en iyi indirim birleşimi iki iskonto 1 uygulamasıdır. İki ürün tam fiyata sahip olacak ve ikisinde yüzde 50 indirim olacaktır. Hareket için iskonto toplamı $45 (15 + 15 + 7,50 + 7,50) olacaktır, bu da iskonto uygulanmamış $60 toplam tutar üzerinden $15 indirim (yüzde 25) demektir. İskonto 2 yalnızca $12 (yüzde 20)'dir.
- İki ürününü her biri $20, bir ürün $15 ve bir ürün $5'dir. Bu durumda, en iyi iskonto birleşimi bir iskonto 2 uygulaması ve bir iskonto 1 uygulamasıdır. Aşağıdaki tablolarda iskontolar gösterilmiştir.

Tabloları okumak için, bir satırdan bir ürün ve bir sütundan bir ürün kullanın. Örneğin, iskonto 1 için verilen tabloda, $20 değerinde olan iki ürünü birleştirdiğinizde, $10 indirim yaparsınız. İskonto 2 için verilen tabloda, $15 değerinde olan ürün ile $5 değerinde olan ürünü birleştirdiğinizde, $4 indirim yaparsınız.

![Çakışan iskonto karması 03](./media/overlapping-discount-combo-03.jpg)

Önce, herhangi bir iskontoyu kullanarak iki üründen herhangi biri için mevcut olan en geniş iskontoyu buluyoruz. İki tablo, iki ürünün tüm kombinasyonları için iskonto tutarını gösterir. Tabloların gölgeli kısımları, bir ürünün kendisi ile eşleştirildiği, (bunu yapamayız) veya iki ürünün aynı iskonto tutarını oluşturacak şekilde ters eşleştirildiği ve yok sayılabilecek durumları gösterir. Tablolara bakarak, bu $20 değerindeki iki ürün için iskonto 1'in dört ürünün hepsi üzerindeki iskonto için kullanılabilecek en geniş iskonto olduğunu görebilirsiniz. (Bu indirim ilk tablodaki yeşil renkle vurgulanır.) Bu, yalnızca $15 değerinde ürün ve $5 değerinde ürün bırakır. İki tabloya tekrar baktığınızda, bu iki ürün için iskonto 1'in $2,50 değerinde bir iskonto sağlarken iskonto 2'nin $4 değerinde iskonto sağladığını görebilirsiniz. Bu nedenle, iskonto 2'yi seçiyoruz. Toplam iskonto $14 olur. Bu tartışmayı daha kolay şekilde görselleştirmek için, hem iskonto 1 hem de iskonto 2 için iki ürüne ilişkin tüm olası birleşimlerle ilgili etkin iskonto yüzdesini gösteren iki ek tablo sağlanmıştır. Bu iki iskonto için, iki ürününü hangi sırayla iskontoya konulduğu önemli olmadığından, birleşimler listesinin yalnızca yarısı dahil edilmiştir. En yüksek etkili iskonto (yüzde 25) yeşil renkle vurgulanır ve en düşük etkili iskonto (yüzde 10) kırmızı renkte vurgulanır.

![Çakışan iskonto karması 04](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Fiyatlar farklılık gösterdiğinde ve iki veya daha fazla iskonto rekabet ettiğinde, en iyi iskonto birleşimini garanti etmenin tek yolu her iki iskontoyu değerlendirmek ve karşılaştırmaktır.

## <a name="total-possible-combinations"></a>Toplam olası birleşimler

Bu bölümde önceki bölümde verilen örnekler devam etmektedir. Daha fazla ürün ve başka bir iskonto ekleyecek ve kaç birleşimin hesaplanması ve karşılaştırılması gerektiğini göreceğiz. Aşağıdaki tabloda, ürün miktarı arttıkça olası iskonto birleşimlerinin sayısı gösterilmektedir. Tablo, hem önceki örnekte olduğu gibi çakışan iki iskonto olduğunda hem de çakışan üç iskonto olduğunda ne olacağını gösterir. Değerlendirilmesi gereken olası iskonto birleşimlerinin sayısı, hızlı bir bilgisayarın bile perakende hareketleri için yeterince hızlı olacak şekilde hesaplayıp karşılaştırabileceği sayıyı aşar.

![Çakışan iskonto karması 05](./media/overlapping-discount-combo-05.jpg)

Daha yüksek miktarlar veya daha fazla çakışan iskonto uygulandığında, olası toplam iskonto birleşimi sayısı hızla milyonlara ulaşır ve en iyi olası birleşimi değerlendirmek ve seçmek için gereken süre hızla dikkate değer bir süreye ulaşır. Değerlendirilmesi gereken birleşimlerin toplam sayısını azaltmak için perakende fiyatı altyapısında bazı iyileştirmeler yapılmıştır. Ancak, bir hareketteki çakışan indirimlerin ve miktarların sayısı sınırsız olduğundan, çakışan iskontolar olduğunda daima çok sayıda birleşimin değerlendirilmesi gerekecektir. Bu sorun, marjinal değer sıralaması yönteminin eğildiği bir sorundur.

## <a name="marginal-value-method"></a>Marjinal değer yöntemi

Katlanarak artan değerlendirilecek birleşim sayısı sorununu çözmek için, iki veya daha fazla iskonto uygulanabilecek ürün kümesindeki her iskonto için paylaşılan ürün başına değeri hesaplayan bir iyileştirme bulunmaktadır. Bu değere, paylaşılan ürünler için iskontonun **marjinal değeri** olarak başvuruyoruz. Marjinal değer, her bir iskontoya paylaşılan ürünler eklendiğinde toplam iskonto tutarında ürün başına ortalama artış değeridir. Marjinal değer, toplam iskonto tutarı (DTotal) alınıp, paylaşılan ürünler olmadan iskonto tutarı (DMinus\\ Shared) düşülerek ve bu fark paylaşılan ürünlerin sayısına (ProductsShared) bölünerek hesaplanır.

![Çakışan iskonto karması 06](./media/overlapping-discount-combo-06.jpg)

Paylaşılan ürün kümesindeki her iskontonun marjinal değeri hesaplandıktan sonra, iskonotolar, kapsamlı olarak, yüksek marjinal değerden düşük marjinal değere doğru sıralanarak paylaşılan ürünlere uygulanır. Bu yöntem için, her tek iskonto örneği uygulandıktan sonra kalan iskonto olasıklıkları karşılaştırılmaz. Bunun yerine, çakışan iskontolar bir kez karşılaştırılır ve sonra sırayla uygulanır. Hiçbir ek karşılaştırma yapılmaz. Eşiği **Perakende parametreleri** sayfasının **İskonto** sekmesindeki marjinal değerine geçecek şekilde yapılandırabilirsiniz. Toplam iskontoyu hesaplamak için kabul edilebilir süre perakende endüstrileri arasında farklılık gösterir. Ancak, bu süre genellikle on milisaniye ile bir saniye aralığında olur.
