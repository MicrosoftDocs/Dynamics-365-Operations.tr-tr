---
title: Satış siparişleri oluşturma
description: Bu prosedür, size bir satış siparişinin nasıl oluşturulacağını göstermektedir.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da460106c95f046e5762787ed169744dece0749f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204390"
---
# <a name="create-sales-orders"></a>Satış siparişleri oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedür, size bir satış siparişinin nasıl oluşturulacağını göstermektedir. Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz. Satış siparişleri genellikle bir satış siparişi işlemcisi tarafından oluşturulur. 

## <a name="enter-sales-order-header-details"></a>Satış siparişi üst bilgi ayrıntılarını girin
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Müşteri hesabı** alanında, aramayı açmak için açılır menü düğmesini seçin.
4. Listede müşteri kaydını bulup seçin.
    - Bu örnekte, US-004 müşteri hesabını seçin.  
5. **Tamam**'ı seçin.

## <a name="enter-sales-order-line-details"></a>Satış siparişi satır ayrıntılarını girin
    
Kuruluşunuz tarafından satılan ürünler; konfigürasyon, renk, boyut ve stil gibi farklılıklarla gelebilir. Ayrıca, ürünler; tesis, ambar ve palet gibi depolama boyutlarını ve parti ile seri numarası gibi bekletme boyutlarını kullanacak şekilde ayarlanabilir. Bu boyutlar atanırken, sipariş satırında bu boyutlara ait değerleri seçmeniz gerekir. Sipariş girişi etkinliğini artırmak için, ilgili boyut alanlarını sipariş kılavuzuna eklemek isteyebilirsiniz.
    
1. **Satış siparişi satırları** bölümünde, **Satış siparişi satırı**'nı seçin.
2. **Boyutlar**'ı seçin.
    
    Bu örnek için, Renk, Tesis ve Ambar boyutlarını seçin. Burada seçtiğiniz boyutlar satış siparişi kılavuzunda görünür. Seçimlerinizi devam ettirmek isterseniz **Kurulumu kaydet** seçeneğini Evet yapın.
    
3. **Tamam**'ı seçin.
4. **Madde numarası** alanında, açılır menü düğmesini seçerek aramayı açın.
5. Bu örnek için madde numarası olarak T0004'ü seçin.
    - Madde bir satış kategorinin parçasıysa, madde adı, Satış kategorisi alanında otomatik olarak görüntülenir.  
    - Ürün boyut alanları zaten değer içeriyorsa, bunun nedeni, değerin varsayılan bir ürün boyutu olarak kaydedildiği ürün kaydından kopyalanmış olmasıdır. Varsayılan değeri istediğiniz zaman değiştirebilirsiniz.   
6. **Renk** alanında, aramayı açmak için açılır menü düğmesini seçin.
7. Listede, istenen kaydı bulun ve seçin.
8. **Miktar** alanına bir sayı girin.
    - Madde satın alındığı, üretildiği ve depolandığı zamankinden farklı birimler halinde satılıyorsa ve ürün kaydında bir satış ölçü birimi ayarlanmışsa bu değer **Birim** alanında gösterilir. Değeri istediğiniz zaman değiştirebilirsiniz.   
    - **Tesis** alanı halihazırda bir değer içeriyorsa değer sipariş başlığından veya ürünle ilişkili sipariş ayarlarından kopyalanmıştır. Değeri istediğiniz zaman değiştirebilirsiniz. Alan boşsa bir değer seçin.   
    - **Birim fiyatı** alanı halihazırda bir değer içeriyorsa değer geçerli bir ticaret anlaşmasından veya ürün kaydından kopyalanmıştır. (Birim fiyatı satış anlaşmasından da alınmış olabilir, ancak satış siparişleri oluşturma süreci burada gösterilenden farklıdır.) Alan boşsa bir değer girin.   
    - **İskonto** alanı, ürün birimi başına bir iskonto tutarı içerir. Toplam satır iskonto tutarını hesaplamak için iskonto değeri satır miktarıyla çarpılır. **İskonto** alanı halihazırda bir değer içeriyorsa, değer geçerli bir ticaret anlaşmasından kopyalanmıştır. Alan boşsa ve müşteriye satır iskontosu yapmak istiyorsanız bir değer girin.  
    - **İskonto yüzdesi** alanı toplam satır brüt tutarından düşülecek bir yüzde değeri içerir.  **İskonto yüzdesi** alanı halihazırda bir değer içeriyorsa değer geçerli bir ticaret anlaşmasından kopyalanmıştır. Alan boşsa ve müşteriye satır iskontosu yapmak istiyorsanız bir değer girin. 
    - **Net** tutar alanı, iskontolarla ayarlanmış satır miktarı ve birim fiyatı temel alınarak hesaplanan bir değer içerir.  Hesaplanan değerin yerine başka bir değer geçirebilirsiniz.  

## <a name="review-the-order-totals"></a>Sipariş toplamlarını gözden geçirin
1. **Eylem Bölmesi**'nde, **Satış siparişi**'ni seçin.
2. **Toplamlar**'ı seçin.
    
    **Toplamlar** sayfasında tüm siparişin ayrıntıları görüntülenir. Bu ayrıntılar, nihai satır iskontoları için ayarlama yapılmış tüm satır net tutarlarının toplamı olan alt toplam tutarını; nihai sipariş düzeyinde iskonto, masraflar ve satış vergisi için ayarlama yapılmış bir alt toplam tutarı olan toplam fatura tutarını; müşterinin kredi limiti durumunu ve daha fazlasını kapsar. Fatura tutarı, müşterinin fatura belgesinde görünecek olan tutardır.  
    
3. **Tamam**'ı seçin.
