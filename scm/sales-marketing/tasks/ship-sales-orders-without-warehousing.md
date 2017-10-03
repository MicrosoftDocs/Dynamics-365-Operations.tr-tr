--- 
title: "Satış siparişlerini ambarlama olmadan sevk etme"
description: "Bu kılavuz, ürünler müşteriye sevk edildiğinde bir satış siparişinin nasıl güncelleştireceğini açıklamaktadır."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: ab2b52b91bcaef57996ae35120e8713aac5852e7
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Satış siparişlerini ambarlama olmadan sevk etme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz, ürünler müşteriye sevk edildiğinde bir satış siparişinin nasıl güncelleştireceğini açıklamaktadır. Kılavuz, ambar yönetimi (temel veya gelişmiş depolama) için ayarlanmamış olan karşılama akışı için geçerlidir ve bu nedenle ürün çekme işleminin sevkiyat öncesinde kaydedilmesini gerektirmez. Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz. Her iki durumda da, bu göreve başlamadan önce stoklanmış bir ürünün, 1'den büyük bir miktar ile bir satış siparişini oluşturun. Bir deftere nakil hatasını önlemek için ürünün siparişte seçmiş olduğunuz tesisteki ve ambardaki eldeki miktarının, siparişteki miktarı karşıladığından emin olduğunu kontrol etmeniz gerekir.


## <a name="post-packing-slip-for-an-order"></a>Sipariş için sevk irsaliyesini deftere nakletme
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Listede, bu görev için oluşturduğunuz siparişi bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Eylem Bölmesinde, Çek ve paketle'ye tıklayın.
5. Sevk irsaliyesini deftere naklet'e tıklayın.
6. Parametreler bölümünü genişletin veya daraltın.
7. Miktar alanında, 'Tümü' öğesini seçin.
    * Diğer seçenekler arasında Şimdi teslim et ve Malzeme çekildi bulunur. Sipariş satırı kısmen sevk edilecek şeklindeyse ve sipariş satırındaki Şimdi teslim et alanında bir miktar belirtilmişse, Şimdi teslim et'i seçmelisiniz. Malzeme çekme faaliyeti kuruluşunuzun karşılama akışı içerisinde bir malzeme çekme listesiyle yönetilen ve kaydedilen ayrı bir işlem olarak bulunuyorsa, Malzeme çekildi'yi seçmelisiniz.  
    * Deftere nakil seçeneğinin Evet olarak ayarlanmış olduğundan emin olun.  
8. Sevk irsaliyesini yazdır seçeneğini Evet olarak ayarlayın.
    * Genel bakış sekmesinde bu nakil sırasında oluşturulacak sevk irsaliyelerinin bir listesi bulunur. Tek sipariş gönderiyorsanız, genellikle tek bir sevk irsaliyesi olur. Ancak, bu siparişlerin satırları farklı tesisler üzerinden sevk edilecekse, deftere nakil işlemi otomatik olarak uygun sayıda belgeye bölünür. Bu, değiştirilemez zorunlu bir durumdur. Benzer şekilde, sipariş satırları farklı teslimat adreslerine sevk edilecekse, deftere nakil işlemi yine birden çok belgeye bölünür ve sevkiyat ilkesi bölünme istenecek şekilde ayarlanır.  
9. Satırlar sekmesinde, sevk edilecek sipariş satırı için bir satır seçin.
10. Güncelleştir alanında orijinal miktardan daha düşük bir sayı girin.
11. Tamam'a tıklayın.
12. Evet'i tıklatın.
13. Sayfayı kapatın.
14. Eylem Bölmesinde, Seçenekler'e tıklayın.
15. Görünümü değiştir'e tıklayın.
16. Başlık görünümü'ne tıklayın.
    * Siparişteki tüm satırlar tamamen sevk edilmişse, sipariş durumu Açık durumundan Teslim edildi'ye değiştirilir.  
    * Bu örnekte, sipariş satırı kısmen sevk edilmiştir. Bu nedenle, sipariş durumu Açık şeklinde kalır.     
    * Siparişi satırlarının en az biri sevk edildiğinden Belge durumu alanını Sevk irsaliyesi şeklinde ayarlanır.  
17. Eylem Bölmesinde, Genel öğesine tıklayın.
18. Satırı miktarı'nı tıklatın.
19. Sayfayı kapatın.
20. Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.
21. Sevk irsaliyesi'ne tıklayın.
    * Sevk irsaliyesi günlüğü sayfası, siparişiniz için oluşturulan tüm sevk irsaliyesi belgelerini içerir. Her belgenin ayrıntılarını gözden geçirebilir ve isterseniz bunları yazdırabilirsiniz.  


