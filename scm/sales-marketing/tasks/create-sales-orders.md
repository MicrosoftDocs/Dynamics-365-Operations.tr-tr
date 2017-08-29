--- 
title: "Satış siparişleri oluşturma"
description: "Bu prosedür, size bir satış siparişinin nasıl oluşturulacağını göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 62276765e1cc76b2328a7b5b57bd18593d93e4ab
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-orders"></a>Satış siparişleri oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, size bir satış siparişinin nasıl oluşturulacağını göstermektedir. Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz. Satış siparişleri genellikle bir satış siparişi işlemcisi tarafından oluşturulur. 




## <a name="enter-sales-order-header-details"></a>Satış siparişi üst bilgi ayrıntılarını girin
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede müşteri kaydını bulup seçin.
    * Bu örnekte, US-004 müşteri hesabını seçin.  
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Tamam'a tıklayın.

## <a name="enter-sales-order-line-details"></a>Satış siparişi satır ayrıntılarını girin
    * Kuruluşunuz tarafından satılan ürünler; konfigürasyon, renk, boyut ve stil gibi farklılıklarla gelebilir. Ayrıca, ürünler; tesis, ambar ve palet gibi depolama boyutlarını ve parti ile seri numarası gibi bekletme boyutlarını kullanacak şekilde ayarlanabilir. Bu boyutlar atanırken, sipariş satırında bu boyutlara ait değerleri seçmeniz gerekir. Sipariş girişi etkinliğini artırmak için, ilgili boyut alanlarını sipariş kılavuzuna eklemek isteyebilirsiniz.  
1. Satış siparişi satırına tıklayın.
2. Boyutlar'a tıklayın.
    * Bu örnek için, Renk, Tesis ve Ambar boyutlarını seçin. Burada seçtiğiniz boyutlar satış siparişi kılavuzunda görünür. Seçimlerinizi devam ettirmek isterseniz, Kurulumu kaydet seçeneğini Evet yapın.   
3. Tamam'a tıklayın.
4. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Bu örnek için madde numarası olarak T0004'ü seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
    * Madde bir satış kategorinin parçasıysa, madde adı, Satış kategorisi alanında otomatik olarak görüntülenir.  
    * Ürün boyut alanları zaten değer içeriyorsa, bunun nedeni, değerin varsayılan bir ürün boyutu olarak kaydedildiği ürün kaydından kopyalanmış olmasıdır. Varsayılan değeri istediğiniz zaman değiştirebilirsiniz.   
7. Renk alanında, açılır menü düğmesine tıklayarak aramayı açın.
8. Listede, istenen kaydı bulun ve seçin.
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Miktar alanına bir sayı girin.
    * Madde satın alındığından, üretiminden ve depolandığı halinden farklı birimler halinde satılırsa, ürün kaydında bir satış ölçü birimi ayarlanır ve bu değer Birim alanında gösterilir. Değeri istediğiniz zaman değiştirebilirsiniz.   
    * Site alanı zaten bir değer içeriyorsa, değer sipariş üst bilgisinden veya ürünle ilişkili sipariş ayarlarından kopyalanmıştır. Değeri istediğiniz zaman değiştirebilirsiniz. Alan boşsa bir değer seçin.   
    * Birim fiyatı alanı zaten bir değer içeriyorsa, değer geçerli bir ticaret anlaşmasından veya ürün kaydından kopyalanmıştır. (Birim fiyatı satış anlaşmasından da alınmış olabilir, ancak satış siparişleri oluşturma süreci burada gösterilenden farklıdır.) Alan boşsa bir değer girin.   
    * İskonto alanı, ürün birimi başına iskonto tutarı içerir. Toplam satır iskonto tutarını hesaplamak için iskonto değeri satır miktarıyla çarpılır.    İskonto alanı halihazırda bir değer içeriyorsa, değer geçerli bir ticaret anlaşmasından kopyalanmıştır. Alan boşsa ve müşteriye satır iskontosu yapmak istiyorsanız bir değer girin.  
    * İskonto yüzdesi alanı toplam satır brüt tutarından düşülecek bir yüzde değeri içerir.  İskonto yüzdesi alanı halihazırda bir değer içeriyorsa, değer geçerli bir ticaret anlaşmasından kopyalanmıştır. Alan boşsa ve müşteriye satır iskontosu yapmak istiyorsanız bir değer girin.  
    * Net tutar alanı, iskontolarla ayarlanmış satır miktarı ve birim fiyatı temel alınarak hesaplanan bir değer içerir.  Hesaplanan değerin yerine başka bir değer geçirebilirsiniz.  

## <a name="review-the-order-totals"></a>Sipariş toplamlarını gözden geçirin
1. Eylem Bölmesinde, Satış siparişi öğesine tıklayın.
2. Toplamlar öğesine tıklayın.
    * Toplamlar sayfasında tüm siparişin ayrıntıları görüntülenir. Bu ayrıntılar, nihai satır iskontoları için ayarlama yapılmış tüm satır net tutarlarının toplamı olan alt toplam tutarını; nihai sipariş düzeyinde iskonto, masraflar ve satış vergisi için ayarlama yapılmış bir alt toplam tutarı olan toplam fatura tutarını; müşterinin kredi limiti durumunu ve daha fazlasını kapsar.  Fatura tutarı, müşterinin fatura belgesinde görünecek olan tutardır.  
3. Tamam'a tıklayın.


