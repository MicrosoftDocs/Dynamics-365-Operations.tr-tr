---
title: İade maliyet fiyatı ve iade lot kodu
description: İade edilen ürünlerin maliyetinin ürünleri müşteriye sattığınız zamandaki maliyete eşit olmasını isteyebilirsiniz. Bunu **İade lot kodu**'nu kullanarak yapabilirsiniz.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65d641cca1bf681dc84b8faaa9292b5a98a7221fd453351228a94671f75ad62
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776812"
---
# <a name="return-cost-price-and-return-lot-id"></a>İade maliyet fiyatı ve iade lot kodu        

[!include [banner](../includes/banner.md)]



Stoğa iade edilen ürünlerin maliyeti ürünlerin geçerli maliyeti kullanılarak hesaplanır. Ancak, iade edilen ürünlerin maliyetinin ürünleri müşteriye sattığınız zamandaki maliyete eşit olmasını isteyebilirsiniz. Bunu **Satış siparişi** formundaki **Satır ayrıntıları** hızlı sekmesinde yer alan **İade lot kodu** alanını kullanarak yapabilirsiniz.

Örneğin aşağıdaki senaryoyu dikkate alın: Bir müşteriye fatura kesiyorsunuz. Daha sonra müşteri teslim edilen ürünleri size iade ediyor. Ürünleri stoğa iade ediyorsunuz. Bu durumda, müşteriyi iade edilen ürünler için alacaklandırdığınızda, bu ürünlerin maliyeti ürünlerin geçerli maliyeti kullanılarak hesaplanır. Ancak, **İade lot kodu** alanını kullanırsanız, iade edilen ürünlerin maliyeti müşteriye yapılan orijinal satışın faturasındaki maliyet kullanılarak hesaplanır.

Müşteriden gelen iadeler için geçerli maliyet dışında bir maliyet kullanmak için aşağıdaki yöntemlerden birini kullanın.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Yöntem 1: İade maliyet fiyatını el ile girin.

Varsayılan olarak, bir iade siparişine maddeleri eklediğinizde, maddeler stoğa geçerli maliyet fiyatından iade edilir. Farklı bir iade maliyet fiyatı belirlemek için şu adımları izleyin.

1.  **Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.

2.  **Eylem bölmesinde** **Yeni** grubunda **İade siparişi**'ne tıklayın.

3.  **İade siparişi oluştur** formunda, bir müşteri hesabı seçin ve ardından **Tamam**'a tıklayın.

4.  **İade siparişi - RMA numarası: %1, %2** formunda bir madde seçin ve sonra **Miktar** alanına negatif bir miktar girin.

5.  **Satır ayrıntıları** hızlı sekmesine tıklayın.

6.  **Genel** sekmesinde, **İade maliyet fiyatı** alanına bir değer girin. Bu değer mallar stoğa iade edildiğinde kullanılır. Bir değer girmezseniz, mallar stoğa iade edildiğinde geçerli maliyet fiyatı kullanılır.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Yöntem 2: Maliyet fiyatının otomatik olarak müşteri fatura satırına bağlı olarak oluştur

İade satırları oluşturmak için tercih edilen yöntem budur. Ürünleri müşteriye sattığınız andaki ürün maliyetini kullanmak için bir iade siparişi oluşturun ve iade edilecek bir satış satırı belirtin.

1.  **Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.

2.  **Eylem bölmesinde** **Yeni** grubunda **İade siparişi**'ne tıklayın.

3.  **İade siparişi oluştur** formunda, bir müşteri hesabı seçin ve ardından **Tamam**'a tıklayın.

4.  **İade siparişi - RMA numarası: %1, %2** formunda, **Eylem Bölmesinde**, **Satış siparişini bul**'a tıklayın.

5.  **Satış siparişini bul** formunda, iade edilecek fatura satırını seçin ve **Tamam**'a tıklayın.
    
    **Genel** sekmesindeki **Satır ayrıntıları** hızlı sekmesinde **İade lot kodu** alanı orijinal satış satırındaki değeri görüntüler. Ayrıca, **İade maliyet fiyatı** alanı orijinal satış satırındaki maliyet değerini görüntüler.

## <a name="cost-calculation-example"></a>Maliyet hesaplama örneği

İade maliyet fiyatını belirtmek için bir iade siparişi satırındaki **İade lot kodu** alanını kullandığınızda, iade siparişi satırındaki maliyet kullanılır. Stok kapatma veya yeniden hesaplama işlevini çalıştırdığınızda, maliyet orijinal satış satırında ayarlanır. İade siparişi satırındaki maliyet otomatik olarak parça başına aynı maliyeti yansıtacak şekilde ayarlanır.

1.  Test adında bir ürün oluşturun ve serbest bırakın. **Serbest bırakılan ürün ayrıntıları** formunda, aşağıdaki bilgileri belirtin:
    
    1.  **Maliyetleri yönet** hızlı sekmesinde, **Madde grubu** alanında **Parçalar** grubunu seçin.
    
    2.  **Genel** hızlı sekmesinde, **Madde model grubu** alanında **DEF**'i seçin.
    
    3.  **Satınalma** hızlı sekmesinde **Fiyat** alanına maddenin maliyet fiyatı olarak 10,00 yazın.
    
    4.  **Eylem Bölmesi**'nde **Boyut grupları**'na tıklayın. **Depolama boyutu grubu** alanında **Yalnızca Tesis ve Ambar**'ı seçin. **İzleme boyutu grubu** alanında **Etkin olmayan izleme boyutları**'nı seçin.

2.  Parça başına 6,00 fiyatla Test maddesi için 10 parçalık bir satınalma siparişi oluşturun ve ardından satınalma siparişine ait faturayı deftere nakledin.
    
    Parça başına 8,00 fiyatla Test maddesi için 10 parçalık ikinci bir satınalma siparişi oluşturun ve ardından satınalma siparişine ait faturayı deftere nakledin.

3.  Test maddesinden beş parça satış yapmak için satış siparişine ait faturayı deftere nakledin.
    
    Bu durumda, satış siparişi satırı maliyeti 35,00 olur (5 parça \*7,00 parça başına ortalama maliyet).

4.  Müşteri için yeni bir iade siparişi oluşturun. **Satış siparişini bul** formunda, fatura satırını seçin ve **Tamam**'a tıklayın.

5.  **İade emri - RMA numarası: %1, %2** formunda, Test maddesini iade etmek için iade siparişi oluşturulduğunu doğrulayın. İade siparişi miktarı -5,00 olarak ayarlanır.
    
    **İade lot kodu** alanında bir lot kodu görüntülenir. Bu lot kodu, müşteriye satılan maddenin orijinal satış siparişinden alınır. **İade maliyet fiyatı** alanı orijinal satış satırındaki maliyet fiyatını gösterir.

6.  İade edilen maddelerin girişini kaydedin.

7.  İade edilen maddelerin sevk irsaliyesini deftere nakledin.

8.  İade sipariş için faturayı deftere nakledin. **Tüm satış siparişleri** liste sayfasında, sipariş türünün **İade siparişi** olduğu bir satış siparişi seçin.

9.  **Stok hareketleri** formunu açın. İadenin parça başına maliyetinin 7.00 olduğunu **İade maliyet fiyatı** alanındaki değeri kullanarak doğrulayın. **Maliyet tutarı** alanındaki toplam 35,00 olmalıdır. **İade siparişi - RMA numarası: %1, %2** formundan **Stok hareketleri** formunu açabilirsiniz. **Satırlar** ızgarasında **Stok** \> **Hareketler**'e tıklayın.

10. Stok ve ambar yönetiminde **Kapanış ve düzeltme** formunu kullanarak **3. Kapat** yordamını çalıştırın.
    
    Bu eylem orijinal satış satırında -35,00 olan maliyeti (5 parça \*7,00) -30,00 (5 parça \*6,00) olarak düzeltir. Bunun nedeki stok model grubunun ilk giren ilk çıkar (FIFO) kullanması ve parça başına 6,00'ın ilk satınalma siparişindeki FIFO maliyeti olmasıdır. Ek olarak, eylem iade satış satırındaki maliyeti orijinal satış satırındaki parça başına maliyetle eşleşecek şekilde ayarlar. Bu nedenle, iade satırındaki maliyet 35,00 yerine 30,00 olarak ayarlanır.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]