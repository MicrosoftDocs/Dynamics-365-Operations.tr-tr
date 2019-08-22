---
title: İşçilik ve masraflar için standart maliyetleri yapılandırma
description: Bu yordam, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı gösterir.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845912"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>İşçilik ve masraflar için standart maliyetleri yapılandırma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı gösterir. Bu görev, USSI veri kümesini kullanır.

1. Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (saat) öğesine gidin.
2. Yeni'ye tıklayın.
3. Yürürlük tarihi alanına bir tarih girin.
4. Maliyet fiyatı alanına bir sayı girin.
    * Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya maliyet fiyatını çalışan numarası, proje numarası, kategori, tarih veya tüm diğer birleşimlere göre ayarlayabilirsiniz. Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyine sahip maliyet fiyatıdır.  
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.
7. Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (saat) öğesine gidin.
8. Yeni'ye tıklayın.
9. Yürürlük tarihi alanına bir tarih girin.
10. Geçerlilik alanında bir seçenek seçin.
11. Fiyatlandırma alanına bir sayı girin.
    * Saat hareketleri veya bir proje kategorisi için bir standart satış fiyatı ayarlayabilirsiniz. Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların bir birleşimine göre ayarlayabilirsiniz. Çalışan, Hizmet saatleri günlüğüne bir hareket girdiğinde uygulanan fiili satış fiyatı, en yüksek ayrıntı düzeyine sahip satış fiyatı olacaktır. Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.  
12. Kaydet'e tıklayın.
13. Sayfayı kapatın.
14. Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (gider) öğesine gidin.
15. Yeni'ye tıklayın.
16. Yürürlük tarihi alanına bir tarih girin.
17. Maliyet fiyatı alanına bir sayı girin.
    * Birden fazla alan doldurulabilir ancak bu, kaydı kaydetmek için gereken en düşük düzeydir.  
18. Kaydet'e tıklayın.
19. Sayfayı kapatın.
20. Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (gider) öğesine gidin.
21. Yeni'ye tıklayın.
22. Yürürlük tarihi alanına bir tarih girin.
23. Geçerlilik alanında bir seçenek seçin.
24. Fiyatlandırma alanına bir sayı girin.
    * Çalışan bir masraf günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır. Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.  
25. Kaydet'e tıklayın.

