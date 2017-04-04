---
title: "Çakışan indirimler en uygun birleşimi belirler"
description: "İndirimler örtüştüğünde en düşük hareket toplam üretecektir örtüşen iskonto veya en yüksek toplam iskonto birleşimi belirlemeniz gerekir. İskonto tutarı satın alınan ürünlerin fiyat göre değişir, ortak olduğu gibi &quot;1 satın almak, 1 X yüzde get off&quot; (BOGO) perakende indirim, bu işlem combinatorial iyileştirme bir sorun haline gelir."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Çakışan indirimler en uygun birleşimi belirler

İndirimler örtüştüğünde en düşük hareket toplam üretecektir örtüşen iskonto veya en yüksek toplam iskonto birleşimi belirlemeniz gerekir. İskonto tutarı satın alınan ürünlerin fiyat göre değişir, ortak olduğu gibi "1 satın almak, 1 X yüzde get off" (BOGO) perakende indirim, bu işlem combinatorial iyileştirme bir sorun haline gelir.

Bu makalede Microsoft Dynamics AX 2012 R3 KB (2 Kasım 2015'te yayımlandı) 3105973 ile uygulanır veya daha sonra Şubat 2016 için Microsoft Dynamics AX bırakın. Zamanında uygulamak ve perakende için Microsoft Dynamics AX'te kullanılabilir iskonto zengin işlevselliği sağlamak devam etmek için birlikte örtüşen indirimler belirlemek için bir yöntem çakışan indirimler uygulamak için sunulmuştur. Biz bu yeni yöntem çağrısı **Marjinal değeri sıralaması**. Marjinal değeri sıralaması, üst üste gelen indirimler olası birleşimlerini değerlendirmek için gereken zaman üzerinde yapılandırılabilir bir eşiği aştığında kullanılan **perakende parametreleri** Dynamics AX'de sayfa. Sıralama yöntemi Marjinal değeri paylaşılan ürünlerde indirim 's değeri kullanarak çakışan her indirim için bir değer hesaplanır. Çakışan indirimler, göreli en yüksek değerden en düşük değerine göreli sonra uygulanır. Yeni yöntemi hakkında daha fazla bilgi için bu makalenin ilerisindeki "Marjinal değeri" bölümüne bakın. Ürün iskonto tutarlarını hareket başka bir ürün tarafından etkilenmez, Marjinal değeri sıralaması kullanýlmaz. Örneğin, bu yöntem iki basit iskontoları veya basit iskonto ve tek bir ürün miktar indirim için kullanýlmaz.

## <a name="discount-examples"></a>Örnekler indirim
Dynamics AX uygulamasında perakende indirimler sınırsız sayıda ortak bir ürün kümesi oluşturabilirsiniz. Ancak, herhangi bir sınır olmadığından, performans sorunları çeşitli ürünlerde kullanılmalıdır iskontolarını hesaplamak çalıştığınızda ortaya çıkabilir. Bu sorunu daha ayrıntılı aşağıdaki örneklerde gösterilmektedir. Örnek 1'de, iki ürün ve üst üste gelen iki iskontonun başlayın. Daha sonra örnek 2'de, daha fazla ürün eklendikçe sorunu nasıl dönüşmesi gösteriyoruz.

### <a name="example-1-two-products-and-two-discounts"></a>Örnek 1: İki ürün ve iki indirimler

Bu örnekte, iki ürün için her indirim hak kazanmak için gereklidir ve indirimler birleştirilemez. Bu örnekte indirimler olan **en iyi fiyat** indirimler. Her iki ürün için her iki indirimler nitelendirin. Burada, iki iskontonun bulunmaktadır. [![Üst üste açılan 01 indirim](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) her iki ürün için bu iki iskontonun daha iyi iki ürün fiyatlar üzerinde bağlıdır. Her iki ürün için fiyat hemen hemen eşit veya eşit olduğunda, indirim 1 daha iyi olur. Bir ürünün fiyatını önemli ölçüde daha az diğer ürünün fiyatı indirim 2 daha iyi olur. Bu iki iskontonun birbirine karşı değerlendirmek için matematiksel kural şudur: [![Overlapping indirim açılan 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) 1 ürünün fiyatı 2 ürünün fiyatı iki-üç için eşit olduğunda, iki iskontonun eşit olduğuna dikkat edin. (İki ürün aynı fiyata sahip olduğunda) Bu örnekte, etkili iskonto yüzdesi 1 iskonto (iki ürün fiyatları uzaklaştırmamaya iken) birkaç yüzde 25'lik en değişir. Etkili iskonto yüzdesi 2 indirim için sabittir. Yüzde 20'si her zaman öyledir. Daha fazla veya daha az 2 indirim olabilir bir aralık indirim 1 etkili iskonto yüzdesine sahip olduğundan, en iyi İndirim İndirim gerekir iki ürün fiyatlar üzerinde bağlıdır. Bu örnekte, yalnızca iki ürün üzerinde sadece iki iskontonun uygulandığından hesaplama hızla tamamlandı. Yalnızca iki olası bileşimleri vardır: indirim 2 1 ya da bir indirim uygulaması bir uygulama. Hiçbir permütasyon hesaplamak için vardır. Her iskonto değeri her iki ürün kullanılarak hesaplanır ve en iyi indirim kullanılır.

### <a name="example-2-four-products-and-two-discounts"></a>Örnek 2: Dört ürünleri ve iki indirimler

Daha sonra dört ürünleri ve aynı iki iskontonun kullanacağız. Tüm dört ürünleri için her iki indirimler nitelendirin. On iki olası kombinasyonları vardır. Sonunda, iki iskontonun üç kombinasyonları işlemde uygulanacak: indirim 1, iki uygulamadan iki uygulama İndirim İndirim 2 1 ve bir indirim uygulamasının 2 veya bir uygulama. Olası birleşimlerini göstermek için farklı fiyatlara sahip dört üründen oluşan iki farklı ayarlar görünecektir:

-   Tüm dört ürünleri $15.00 aynı fiyata sahip. Bu durumda, en iyi İndirim İndirim 1 iki uygulama birleşimidir. İki ürün tam fiyat olacaktır ve iki yüzde 50 kapalı olacaktır. Hareket için indirimli toplam $15 (yüzde 25) ise (15 + 15 + 7.50 + 7.50) $45 undiscounted $60 toplamıdır. İndirim 2 yalnızca $12 (yüzde 20) ' dir.
-   $20 her iki ürün değil, $15 bir üründür ve $5 bir üründür. Bu durumda, en iyi İndirim İndirim 1 2 ve bir indirim uygulaması bir uygulama birleşimidir. İndirim aşağıdaki tablolarda gösterilmiştir.

Tabloların okumak için satır bir ürün ve bir sütundan bir ürün kullanın. İki $20 ürün birleştirdiğinizde örneğin 1 iskonto tablosunda $10 size. $15 ürün ve $5 ürün birleştirdiğinizde 2 İskontosu tablosunda $4 size. [![Üst üste açılan 03 indirim](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) önce herhangi iki ürünleri ya da indirim ile kullanılabilir en büyük indirim buluyoruz. İki tablodan tüm kombinasyonları iki ürün iskonto tutarını gösterir. Tabloları gölgeli kısımları bir ürünün kendisi ile biz yapamaz veya ters çifti, aynı üreten iki ürün iskonto tutarı ve göz ardı edilebilir nerede eşleştirilmiş ya da servis taleplerini gösterir. Tablolara bakarak, bu iki $20 maddeler için iskonto 1 ya da dört tüm ürünlerde indirim için kullanılabilir en büyük indirim olduğunu görebilirsiniz. (Bu indirim ilk tablodaki yeşil vurgulanır.) Bu $15 ürün ve $5 ürün bırakır. $4 İndirim İndirim 2 verir iken yeniden iki tablolara bakarak, bu iki ürünü $2.50 indirim, indirim 1 verir, görebilirsiniz. Bu nedenle, indirim 2 seçin. Toplam iskonto $14 olur. Bu tartışma görselleştirmek kolaylaştırmak için her iki iskonto 1 için tüm olası iki ürün birleşimler için etkili iskonto yüzdesini gösteren ve 2 indirim iki ek tablo aşağıdadır. Bu iki iskontonun için iki ürün iskonto getirilme sırasını önemi yoktur çünkü birleşimlerinin listesi yalnızca yarısını içerir. Yüksek etkili iskonto (yüzde 25) yeşil vurgulanır ve en düşük etkili iskonto (yüzde 10) kırmızı renkte vurgulanır. [![Üst üste açılan 04 indirim](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Not:** fiyatları farklılık ve iki veya daha fazla indirim rekabet, hem indirimler değerlendirmek ve bunları karşılaştırmak için garanti iskontolarını iyi birleşimi tek yolu değil.

## <a name="total-possible-combinations"></a>Toplam olası bileşimleri
Bu bölümde örnek önceki bölümden devam eder. Biz daha fazla ürünler ve başka bir indirim ve kaç birleşimleri hesaplanan karşılaştırılması ve bakın. Aşağıdaki tabloda, ürün miktarı arttıkça olası iskonto kombinasyonlarını sayısını gösterir. Tablo önceki örnekte olduğu gibi iki örtüşen indirimler olduğunda hem üç çakışan indirimler olduğunda ne olacağını gösterir. Değerlendirilmesi gereken olası iskonto kombinasyonlarını yakında ne hızlı bir bilgisayar hesaplayabilirsiniz sayısını aşıyor ve perakende hareketleri için kabul edilebilir için yeterince hızlı karşılaştırın. [![Üst üste açılan 05 indirim](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) zaman bile daha büyük miktarlar veya daha fazla üst üste gelen İndirimler uygulanmadan, milyonlarca kişiye göre olası iskonto kombinasyonlarını toplam sayısı hızla gider ve hızlı bir şekilde en iyi olası birleşimini seçin ve değerlendirmek için gereken süreyi belirgin hale gelir. Değerlendirilmesi gereken birleşimleri toplam sayısını azaltmak için perakende fiyatı altyapısında bazı iyileştirmeler yapılmış. Sayı örtüşen İndirimler ve miktarlar bir harekette sınırlı değildir çünkü ancak, çok sayıda birleşimleri her zaman örtüşen indirimler olduğunda değerlendirilmesi gerekecektir. Bu sorunu gideren yöntemi sıralaması Marjinal değeri sorundur.

## <a name="marginal-value-method"></a>Marjinal değeri yöntemi
Değerlendirilmesi gereken birleşimleri katlanarak artan bir dizi sorunu çözmek için bir iyileştirme bulunmaktadır her indirim üzerinde iki veya daha fazla indirim uygulanabilir ürün grubunu paylaşılan ürün başına değeri hesaplar. Biz bu değeri olarak başvurmak **Marjinal değeri** paylaşılan ürünler için indirim. Paylaşılan ürünler her iskonto dahil olduğunda Marjinal ürün artış toplam iskonto tutarı başına ortalama değerdir. Toplam iskonto tutarı (DTotal) paylaşılan ürünsüz iskonto tutarı çıkarılmadan yararlanarak Marjinal değeri hesaplanır (DMinus\\ Shared) ve bu fark paylaşılan ürünler (ProductsShared) sayısına bölünmesi. [![Üst üste açılan 06 indirim](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) her bir paylaşılan küme ürünleri iskontosunda Marjinal değeri hesaplandıktan sonra indirimler paylaşılan ürünler sırasıyla ayrıntısına, Marjinal yüksek değerinden düşük Marjinal değeri için uygulanır. Bu yöntem için her seferinde tek bir örneğini bir indirim uygulandıktan sonra kalan tüm iskonto olanakları karşılaştırıldığında değildir. Bunun yerine, üst üste gelen indirimler karşılaştırıldığında bir kez ve sonra sırayla uygulanır. Hiçbir ek karşılaştırmalar yapılır. Marjinal değeri yönteme geçmeyi eşik yapılandırabilirsiniz **indirim** sekmesinde **perakende parametreleri** sayfa. Toplam iskontosunu hesaplamak için kabul edilebilir süre perakende endüstrileri arasında değişir. Ancak, bu kez, bir saniye için milisaniye olarak onlarca aralığında genellikle düşer.


