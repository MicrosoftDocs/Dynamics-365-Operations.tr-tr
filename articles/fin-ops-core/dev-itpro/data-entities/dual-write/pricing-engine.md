---
title: Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta Dynamics 365 Sales'ın fiyatlandırma motorunun nasıl kullanılacağı açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f84a81444e6d5ce9a0d2da4c9a60b1ae3478ee2f
ms.sourcegitcommit: 2d8035f8bb75957c793c0d293c079a792595eeaf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2021
ms.locfileid: "7481327"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management, ticari sözleşmeleri, Fiyat listelerini, müşteri bağlılık programı programlarını, yükseltmeleri ve iskontoları işleyen bir fiyatlandırma altyapısı içerir. Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır. Çift yazmayı kullandığınızda, Dynamics 365 Sales içindeki teklif ve sipariş sayfalarındaki Dynamics 365 Supply Chain Management'tan fiyatlandırma motorunu kullanırsınız.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Sales'da Supply Chain Management fiyatlandırma altyapısını kullan

1. Sales'da **satışlar \>siparişlere** gidin.
2. Yeni sipariş oluşturmak için **Yeni**'yi seçin veya **Siparişlerim** listesinde mevcut siparişi seçin.
3. Yeni siparişi satırı ekleyin.
4. Yeni bir sipariş oluşturuyorsanız, eylem bölmesinde **fiyat siparişi** seçeneğini belirleyin. Mevcut bir siparişi güncelliyorsanız eylem bölmesinde **Yeniden hesapla** seçeneğini belirleyin.

    Aşağıdaki sütunlar otomatik olarak doldurulur:

    + Ayrıntı Tutarı
    + İskonto yüzdesi
    + İskonto
    + Ön Navlun Tutarı
    + Navlun Tutarı
    + Toplam Vergi
    + Toplam Tutar
    
5. Sistemin fiyatı hesaplamak amacıyla ticari sözleşmeleri dikkate aldığından emin olmak için:
    1. Supply Chain Management ortamınıza gidin.
    2. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
    3. Yan gezinti çubuğunda **Fiyatlar** sekmesini seçin.
    4. **Ticaret anlaşması değerlendirme** hızlı sekmesi altında, **El ile giriş** seçeneğindeki işareti kaldırın.

## <a name="how-it-works"></a>Nasıl çalışır

Sales'ta **fiyat siparişi** seçeneğini belirlediğinizde, ilgili satış siparişi için Supply Chain Management'te **Satış Siprişi \> Görüntüle** sekmesindeki **Toplamlar** işlevi çağrılır. Sales içindeki sipariş toplamlarında bulunan değerler, Supply Chain Management'ta karşılık gelen sütunları doldurmak için kullanılır.

Supply Chain Management'ta satış siparişi toplamı hesaplandığında hesaplama, müşteri ve satış siparişinde listelenen ürünler için mevcut ticari sözleşmeleri değerlendirir. Toplamları hesaplamak için bu bilgiler kullanılır. **Fiyat siparişi** seçildiğinde, Sales, Supply Chain Management'de yapılan tüm kurulumu otomatik olarak yansıtır.

## <a name="limitations"></a>Sınırlamalar

Sales içindeki sütunlar doldurulduğunda, aşağıdaki sınırlamalar geçerlidir:

+ Supply Chain Management'ta bulunan masraf ve gider tahsisatının kurulumu Sales içinde çoğaltılmaz.
+ Fiyatlandırma, Supply Chain Management'ta satış siparişi satırı sayfasındaki **Perakende Kanalı** sütununda belirtilen özel perakende fiyatlandırmasını dikkate almıyor.
+ Supply Chain Management'ın **ticari kesinti Yönetimi** bölümünde tanımlanan iskontolar dikkate alınmazlar.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
