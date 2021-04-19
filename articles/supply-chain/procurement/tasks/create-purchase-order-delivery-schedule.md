---
title: Teslimat planı olan satınalma siparişi oluşturma
description: Bu konu, satınalma siparişi için teslimat oluşturmayı göstermektedir.
author: kamaybac
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d788aaf3dc45542e20745cb295d77efdc277a4be
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812367"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Teslimat planı olan satınalma siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, satınalma siparişi için teslimat oluşturmayı göstermektedir. Teslimat planı, bir siparişteki veya günlükteki miktarın birden fazla sevkiyatlar halinde teslim edilmesi istendiği zaman kullanılır. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Bu prosedür tipik olarak bir satın alma temsilcisi tarafından gerçekleştirilir.

## <a name="create-a-delivery-schedule"></a>Teslimat planı oluşturma
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Satınalma siparişleri > Tüm satın alma siparişleri** öpesine gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satıcı hesabı** alanına `US-101` girin.
4. **Tamam**'ı seçin.
5. **Madde numarası** alanına `M0001` girin.
6. **Miktar** alanına `10` girin.
7. **Satın alma siparişi satırı**'nı seçin.
8. **Satış teslimat planı**'nı seçin.
- **Teslimat planı** sayfası, sipariş satırı toplam miktarının satıcıdan teslim edileceği sevkiyat sayısını belirtmenize olanak tanır.  
- Varsayılan olarak, sistem orijinal satınalma satırının toplam miktarını ve diğer teslimat ayrıntılarını ilk teslimat planı satırına kopyalar. Bu örnekte iki sevkiyat planı oluşturacağız ve ikinci sevkiyatın tarihi, ilk sevkiyattan bir hafta sonra olacak.  
9. **Miktar** alanında, miktarı `4` olarak değiştirin.
10. **Yeni**'yi seçin.
11. **Miktar** alanına, kalan miktar olarak `6` girin.
- Teslimat tarihi alanında ilk teslimat satırındaki tarihten bir hafta sonraki tarihi seçin.  
- **Toplam** ve **Kalan** alanlarına bakarak, teslimat planı satırlarına tahsis edilen toplam miktarı izleyebilirsiniz. Kalan miktar sıfır olduğunda, orijinal satırdan alınan tüm miktar plana tahsis edilmiştir.  
12. **Gider dönüştürme** bölümünü genişletin.
- Burada seçenekler, teslimat planı satırları üzerinden masrafları nasıl dağıtmak istediğinizi kontrol etmenize olanak tanır. **Brüt tutarları kopyala**'yı seçerseniz her teslimat satırına orijinal sipariş satırındaki masraf tutarı kopyalanır. **Teslimat satırlarına tahsis et** seçeneği orijinal satırdaki masrafı her bir teslimat satırındaki miktara göre böler.  
13. **Gider dönüştürme** bölümünü daraltın.
14. **Tamam**'ı seçin.
- Teslimat planı siparişe artık uygulanmıştır.  
- Ticari satırı olarak anılan orijinal sipariş satırı, birden fazla teslimatlı bir Siparişe dönüştürülmüştür. Farklı bir simgeyle işaretlenir ve teslimat satırları için başlık olarak işlev görür.  
15. İki teslimat satırının ilki olan ikinci sipariş satırını seçin.
- Teslimat satırları olarak anılan iki yeni satır bir teslim planı oluşturur. Sipariş orijinal satıra göre değil, bu satırlara göre işlenir. Onaylar, ürün girişi günlükleri veya faturalar gibi belgeler yazdırılırken yalnızca teslimat satırları gösterilir.  

## <a name="change-the-delivery-schedule"></a>Teslimat planını değiştirin
Teslimat satırlarında miktarı değiştirebilirsiniz. Bunu yaparsanız, ticari satırı otomatik olarak güncelleştirilip, teslimat satırlarındaki toplam miktara çevrilir.  
1. İlk teslimat satırının **Miktar** alanında miktarı `4`'ten `5`'e değiştirin.
2. İlk sipariş satırını (ticari satırı) seçin.  
- Ticari satırındaki miktar 11'e değiştirilmiştir.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Teslimat planlarını kullanarak ürün girişini işleyin
Satınalma siparişi ürün girişi işlenmeden önce onaylanmalıdır. Bu örnekte giriş doğrudan satınalma siparişi üzerinden kaydedilir. Mallar ambara ulaştığında da giriş kaydedilmiş olur.  
1. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
2. **Onayla**'yı seçin.
3. Eylem Bölmesinde, **Teslim alma**'yı seçin.
4. **Ürün girişi**'ni seçin. **Ürün girişi** alanına herhangi bir değer yazın.
- Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.  
- **Miktar** alanında, **Sipariş edilen miktar**'ı seçin. Bu seçenek, sipariş satırlarının birlikte oluşturulduğu miktar için girişin işleneceği anlamına gelir.  
- **Ürün girişi yazdır** alanının **Hayır** olarak ayarlandığından emin olun. Bu örnekte, yazdırma gerekli değildir.  
5. **Satırlar** bölümünü genişletin.
- Ürün girişinin orijinal sipariş satırı değil iki teslimat satırı için oluşturulduğuna dikkat edin. Giriş ambarda kaydedilmişse teslimat planı satırlarında da kaydedilmiş olur.  
6. **Satırlar** bölümünü daraltın.
7. Girişi nakletmek için **Tamam**'ı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]