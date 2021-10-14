---
title: Uygulanabilir fiyatları ve iskontoları arama
description: Bu yordam, bir satış siparişi oluşturmak zorunda kalmadan belirli bir müşteri için geçerli olan ürün fiyat ve iskonto bulmayı gösterir.
author: Henrikan
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c80ae00e1bcbc4498ec4705195c3208170cee1b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578932"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Uygulanabilir fiyatları ve iskontoları arama

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satış siparişi oluşturmak zorunda kalmadan belirli bir müşteri için geçerli olan ürün fiyat ve iskonto bulmayı gösterir. Bu yordam belirli bir örneği adım adım izler ve örneği takip ederken gerekli değerleri seçebilmek için USMF demo şirketini kullanmanız gereklidir.


## <a name="find-the-applicable-price"></a>Uygulanabilir fiyatı bulun
1. Sales and marketing > Prices and discounts > Find prices (Satış ve pazarlama > Fiyatlar ve iskontolar > Fiyatları bul) menüsüne gidin.
2. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
3. Listede, müşteri US-001'i bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Madde numarası alanına 'T0004' girin.
    * Miktar alanı varsayılan olarak 1'e ayarlıdır. Fakat, söz konusu ürün için müşterinin vermek istediği siparişin boyutunu biliyorsanız, yerine bu değeri girin. Bu bilgiler, müşteri ile olan ticari anlaşmalarının miktar kırılması varsa, yani ürünün fiyatı satın alınan minimum miktara bağlıysa, ilgilidir.  
6. Tarih alanına, sipariş verebilmek için müşterinin beklediği bir tarihi girin. 
    * Tarih bugünün tarihi ya da gelecekteki herhangi bir tarih olabilir.  
    * Sistem şimdi belirtilen miktarla seçilen tarihte, seçilen müşteri tarafından satın alınan, seçilen ürün miktarı için geçerli olan fiyatı getirir. Bu örnekte, müşteri US-001 bugün T0004 ürününden 1 birim satın aldıysa, 350 Kanada doları ücretlendirilir. Bu fiyat müşteri ile mevcut bulunan ve etkin olan ticari sözleşmeden ileri gelmektedir.      Sayfadaki diğer alanlar, ürün hakkında fiyat, ürün maliyeti (eğer ana ürün üzerinde ayarlandıysa) ve hesaplanmış karlılık gibi bilgiler verir.  
    * İlgili ürün çeşitlerini göster seçeneği işaretliyse bu, ürün çeşitleri ile ilgili başka ticari sözleşmeler olduğunu gösterir.  
7. İlgili ürün çeşitlerini göster onay kutusuna tıklayın.
    * Boyutları hakkında bilgi verilen, ürün çeşitlerinin bir listesi gösterilir.  
8. Listede, Beyaz rengi temsil eden çizgiyi işaretleyin.
    * Ürün fiyatının, boyut belirtilmemiş olduğunda önceden görüntülenenden farklı olduğuna dikkat edin.  
9. Satış fiyatlarını görüntüle'ye tıklayın.
    * Fiyat (satış) sayfası, ürün ve türevleri de dahil olmak üzere, ilgili tüm ticari sözleşmeleri görüntüler.  
10. Sayfayı kapatın.

## <a name="find-the-applicable-discount"></a>Uygulanabilir indirimi bulun
Müşteri hesabı alanının müşteri numarası US-001'i içerdiğinden emin olun    
1. Madde numarası alanına 'T0012' girin.
    * Miktar alanının 1'e ayarlandığından emin olun.  
    * Gösterilen ürün T0012 için aşağıdaki fiyatlandırma ayrıntıları bir veya daha fazla ticari sözleşmeden ileri gelmektedir: Birim fiyatı 1.000 Kanada doları ve iskonto yüzde 5.  
2. Miktarı '20' olarak ayarlayın.
    * Artan sipariş miktarı, müşteriye sunulan satır iskontosunun yüzde 5'ten 7'ye çıkmasına sebep olur.  
    * Net tutar, birim tutarı, iskonto ve toplam miktara göre hesaplanır.  
3. Satır iskontolarını görüntüle'ye tıklayın.
    * Ürün T0012 için iki indirim sözleşmesi vardır; 1 il 10 arasında sipariş satırı miktarı içi yüzde 5 ve 10 üzerinde sipariş miktarlar için yüzde 7 indirim. Bir indirimin bir grup ürüne uygulandığını (bu örnekteki ürün T0012'nin bir parçası olduğu Grup kodu 01) unutmayın.  
4. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]