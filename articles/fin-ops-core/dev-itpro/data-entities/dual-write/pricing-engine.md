---
title: İstek üzerine Dynamics 365 Supply Chain Management fiyatlandırma altyapısıyla eşitleme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta Dynamics 365 Sales'ın fiyatlandırma motorunun nasıl kullanılacağı açıklanmaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173189"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>İstek üzerine Dynamics 365 Supply Chain Management fiyatlandırma altyapısıyla eşitleme

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management, ticari sözleşmeleri, Fiyat listelerini, müşteri bağlılık programı programlarını, yükseltmeleri ve iskontoları işleyen bir fiyatlandırma altyapısı içerir. Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır. Çift yazmayı kullandığınızda, Dynamics 365 Sales içindeki teklif ve sipariş sayfalarındaki Dynamics 365 Supply Chain Management'tan fiyatlandırma motorunu kullanırsınız.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Sales'da Supply Chain Management fiyatlandırma altyapısını kullan

1. Sales'da **satışlar \>siparişlere** gidin.
2. Yeni sipariş oluşturmak için **Yeni**'yi seçin veya **Siparişlerim** listesinde mevcut siparişi seçin.
3. Yeni siparişi satırı ekleyin.
4. Yeni bir sipariş oluşturuyorsanız, eylem bölmesinde **fiyat siparişi** seçeneğini belirleyin. Mevcut bir siparişi güncelliyorsanız eylem bölmesinde **Yeniden hesapla** seçeneğini belirleyin.

    Aşağıdaki alanlar otomatik olarak doldurulur:

    + Ayrıntı Tutarı
    + İskonto yüzdesi
    + İskonto
    + Ön Navlun Tutarı
    + Navlun Tutarı
    + Toplam Vergi
    + Toplam Tutar

## <a name="how-it-works"></a>Nasıl çalışır

Sales'ta **fiyat siparişi** seçeneğini belirlediğinizde, ilgili satış siparişi için Supply Chain Management'te **Satış Siprişi \> Görüntüle** sekmesindeki **Toplamlar** işlevi çağrılır. Sales içindeki sipariş toplamlarında bulunan değerler, Supply Chain Management'ta karşılık gelen alanları doldurmak için kullanılır.

Supply Chain Management'ta satış siparişi toplamı hesaplandığında, hesaplama müşteri ve satış siparişinde listelenen ürünler için varolan ticari sözleşmeleri ve satış anlaşmalarını değerlendirir. Toplamları hesaplamak için bu bilgiler kullanılır. **Fiyat siparişi** seçildiğinde, Sales, Supply Chain Management'de yapılan tüm kurulumu otomatik olarak yansıtır.

## <a name="limitations"></a>Sınırlamalar

Sales içindeki alanlar doldurulduğunda, aşağıdaki sınırlamalar geçerlidir:

+ Supply Chain Management'ta bulunan masraf ve gider tahsisatının kurulumu Sales içinde çoğaltılmaz.
+ Fiyatlandırma, Supply Chain Management'ta satış siparişi satırı sayfasındaki **perakende kanal** alanında belirtilen özel perakende fiyatlandırmasını dikkate almıyor.
+ Supply Chain Management'ın **ticari kesinti Yönetimi** bölümünde tanımlanan iskontolar dikkate alınmazlar.
