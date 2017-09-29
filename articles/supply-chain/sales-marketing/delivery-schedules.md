---
title: "Teslimat zaman çizelgeleri"
description: "Teslimat zaman çizelgeleri tek bir satış siparişi, satış teklifi veya satın alma emri için birden fazla teslimat kullanılıyorken sipariş çizgisi miktarını izlemenize olanak tanır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 701a8b2b94fecedcddada46ad6438448254c8e77
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017

---

# <a name="delivery-schedules"></a>Teslimat zaman çizelgeleri

[!include[banner](../includes/banner.md)]


Teslimat zaman çizelgeleri tek bir satış siparişi, satış teklifi veya satın alma emri için birden fazla teslimat kullanılıyorken sipariş çizgisi miktarını izlemenize olanak tanır.

Bir sipariş veya teklif satırındaki toplam miktarın çok sayıda sevkiyat ile teslim edilmesi gerekiyorsa, bir teslimat planı kullanın. Bireysel sevkiyatlar teslimat satırlarıyla gösterilir. İki veya daha fazla teslimat satırı bir teslimat planı oluşturur. Teslimat satırları farklı teslim tarihleri; miktarları; teslimat şekilleri; tesis ve ambar gibi depolama boyutları içerebilir.  

**Bir teslimat zamanlaması örneği**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Toplam sipariş (orijinal sipariş satırı) | 600 sandalye                               |
| Talep edilen teslimat planı       | Aylık 100 sandalye                     |
| Teslimat için talep edilen zaman aralığı | 6 ay, her ayın ilk gününde |

Bu senaryoda, müşteri altı aylık bir dönem için 100 sandalyelik kümeler halinde 600 sandalye teslimatı talep etmektedir. Teslimat gereksinimlerini takip etmek için bir teslimat zamanlaması oluşturursunuz. Teslimat planı sayfasında, altı ayrı teslimat satırı oluşturursunuz. Her teslimat satırında 100 sandalye vardır ve bu 100 sandalyenin teslimat tarihini gösterir. Bu durumda, her satır takip eden altı aylık dönemin ilk ayına mahsup eder.  

Bir teslimat planı oluşturduğunuzda, orijinal sipariş satırının türü otomatik olarak **Birden fazla teslimatlı sipariş satırları** seçeneğine değiştirilir. Bu türde bir satıra ticari bir satır olarak bakılır ve bir simgeyle işaretlenir. Teslimat satırı, farklı bir simgeyle işaretlenir. Bir teslimat satırlarında bir miktarı değiştirirseniz. ticari satırı güncelleştirilip, teslimat planı toplam miktarına çevrilir. Ticaret anlaşması sipariş için bir toplam iskonto tanımladıysa, teslimat zamanlaması siparişinizin toplam sipariş iskontosuna uygun olduğundan emin olur, sipariş birden fazla teslimata ayrılmış olsa bile.  

Teslimat planı olan siparişler teslimat satırları göz önüne alınarak işlenir. İşlemlere sevk irsaliyelerinin deftere nakli, ürün girişleri ve faturalama dahildir.  

Teslimat planı olan siparişlerin belge çıktıları ve teklifleri yalnızca teslimat satırlarını gösterir. Orijinal satırları (ticari satırlar) göstermez. **Not:** Ek olarak aşağıdaki işlemleri gerçekleştirdiğinizde yalnızca teslimat satırları gösterilir:

-   Naklet
-   Sayfaları kopyala
-   Liste sayfalarına ve raporlara gözat

Satış tekliflerini onayladığınızda, elde edilen satış siparişleri sipariş satırlarında birden çok teslimat olsa bile tam teslimat planını gösterir. Ayrıca, tüm teslimat planı satış siparişleri, satış teklifleri ve satınalma siparişleri gibi önemli sayfaların tümünde gösterilir.



