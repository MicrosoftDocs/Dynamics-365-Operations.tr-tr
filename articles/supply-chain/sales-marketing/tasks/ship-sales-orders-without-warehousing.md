---
title: Satış siparişlerini ambarlama olmadan sevk etme
description: Bu konu, ürünler müşteriye sevk edildiğinde bir satış siparişinin nasıl güncelleştireceğini açıklamaktadır.
author: omulvad
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0760ff5810bb832e25d6a2d473b3cda703872a05de4936191f91664406fe18c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767328"
---
# <a name="ship-sales-orders-without-warehousing"></a>Satış siparişlerini ambarlama olmadan sevk etme

[!include [banner](../../includes/banner.md)]

Bu konu, ürünler müşteriye sevk edildiğinde bir satış siparişinin nasıl güncelleştireceğini açıklamaktadır. Kılavuz, ambar yönetimi (temel veya gelişmiş depolama) için ayarlanmamış olan karşılama akışı için geçerlidir ve bu nedenle ürün çekme işleminin sevkiyat öncesinde kaydedilmesini gerektirmez. Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz. Her iki durumda da, bu göreve başlamadan önce stoklanmış bir ürünün, 1'den büyük bir miktar ile bir satış siparişini oluşturun. Bir deftere nakil hatasını önlemek için ürünün siparişte seçmiş olduğunuz tesisteki ve ambardaki eldeki miktarının, siparişteki miktarı karşıladığından emin olduğunu kontrol etmeniz gerekir.

## <a name="post-packing-slip-for-an-order"></a>Sipariş için sevk irsaliyesini deftere nakletme
1. Gezinti bölmesinde **Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.
2. Listede, bu görev için oluşturduğunuz siparişi bulun ve seçin.
3. Eylem Bölmesinde, **Çek ve paketle**  öğesine tıklayın.
4. **Sevk irsaliyesini deftere naklet**'i seçin.
5. **Parametreler** bölümünü genişletin veya daraltın.
6. **Miktar** alanında **Tümü** seçeneğini seçin.
    - Diğer seçenekler arasında **Şimdi teslim et** ve **Malzeme çekildi** bulunur. Sipariş satırı kısmen sevk edilecek şeklindeyse ve sipariş satırındaki **Şimdi teslim et** alanında bir miktar belirtilmişse, **Şimdi teslim et**'i seçmelisiniz. Malzeme çekme faaliyeti kuruluşunuzun karşılama akışı içerisinde bir malzeme çekme listesiyle yönetilen ve kaydedilen ayrı bir işlem olarak bulunuyorsa, **Malzeme çekildi**'yi seçmelisiniz.  
    - **Deftere nakil** seçeneğinin **Evet** olarak ayarlanmış olduğundan emin olun.  
7. **Sevk irsaliyesini yazdır** seçeneğini **Evet** olarak ayarlayın. **Genel bakış** sekmesinde bu nakil sırasında oluşturulacak sevk irsaliyelerinin bir listesi bulunur. Tek sipariş gönderiyorsanız, genellikle tek bir sevk irsaliyesi olur. Ancak, bu siparişlerin satırları farklı tesisler üzerinden sevk edilecekse, deftere nakil işlemi otomatik olarak uygun sayıda belgeye bölünür. Bu, değiştirilemez zorunlu bir durumdur. Benzer şekilde, sipariş satırları farklı teslimat adreslerine sevk edilecekse, deftere nakil işlemi yine birden çok belgeye bölünür ve sevkiyat ilkesi bölünme istenecek şekilde ayarlanır.  
8. **Satırlar** sekmesinde, sevk edilecek sipariş satırı için bir satır seçin.
9. **Güncelleştir** alanında orijinal miktardan daha düşük bir sayı girin.
10. **Tamam**'ı seçin.
11. **Evet**'i seçin.
12. Sayfayı kapatın.
13. Eylem Bölmesinde, **Seçenekler**'i seçin.
14. **Görünümü değiştir**'i seçin.
15. **Başlık görünümü**'nü seçin.
    - Siparişteki tüm satırlar tamamen sevk edilmişse, sipariş durumu Açık durumundan Teslim edildi'ye değiştirilir.  
    - Bu örnekte, sipariş satırı kısmen sevk edilmiştir. Bu nedenle, sipariş durumu Açık şeklinde kalır.     
    - Siparişi satırlarının en az biri sevk edildiğinden **Belge durumu** alanı Sevk irsaliyesi şeklinde ayarlanır.  
16. Eylem Bölmesinde, **Genel**'i seçin.
17. **Satır miktarı**'nı seçin.
18. Sayfayı kapatın.
19. Eylem Bölmesinde, **Çek ve paketle**  öğesine tıklayın.
20. **Sevk irsaliyesi**'ni seçin. **Sevk irsaliyesi günlüğü** sayfası, siparişiniz için oluşturulan tüm sevk irsaliyesi belgelerini içerir. Her belgenin ayrıntılarını gözden geçirebilir ve isterseniz bunları yazdırabilirsiniz.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]