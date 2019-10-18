---
title: İşçilik ve masraflar için standart maliyetleri yapılandırma
description: Bu konu, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı açıklar.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185417"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>İşçilik ve masraflar için standart maliyetleri yapılandırma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konu, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı açıklar. Bu görev, USSI veri kümesini kullanır.

1. Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Maliyet fiyatı (saat)**'na gidin.
2. **Yeni**'yi seçin.
3. **Yürürlük tarihi** alanına bir tarih girin.
4. **Maliyet fiyatı** alanına bir sayı girin. Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya maliyet fiyatını çalışan numarası, proje numarası, kategori, tarih veya tüm diğer birleşimlere göre ayarlayabilirsiniz. Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyine sahip maliyet fiyatıdır.  
5. **Kaydet**'i seçin.
6. Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Satış fiyatı (saat)**'na gidin.
7. **Yeni**'yi seçin.
8. **Yürürlük tarihi** alanına bir tarih girin.
9. **Geçerlilik** alanında bir seçenek seçin.
10. **Fiyatlandırma** alanına bir sayı girin. Saat hareketleri veya bir proje kategorisi için bir standart satış fiyatı ayarlayabilirsiniz. Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların bir birleşimine göre ayarlayabilirsiniz. Çalışan, Hizmet saatleri günlüğüne bir hareket girdiğinde uygulanan fiili satış fiyatı, en yüksek ayrıntı düzeyine sahip satış fiyatı olacaktır. Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.  
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Maliyet fiyatı (gider)**'na gidin.
14. **Yeni**'yi seçin.
15. **Yürürlük tarihi** alanına bir tarih girin.
16. **Maliyet fiyatı** alanına bir sayı girin. Birden fazla alan doldurulabilir ancak bu, kaydı kaydetmek için gereken en düşük düzeydir.  
17. **Kaydet**'i seçin.
18. Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Satış fiyatı (gider)**'na gidin.
19. **Yeni**'yi seçin.
20. **Yürürlük tarihi** alanına bir tarih girin.
21. **Geçerlilik** alanında bir seçenek seçin.
22. **Fiyatlandırma** alanına bir sayı girin. Çalışan bir masraf günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır. Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.  
23. **Kaydet**'i seçin.

