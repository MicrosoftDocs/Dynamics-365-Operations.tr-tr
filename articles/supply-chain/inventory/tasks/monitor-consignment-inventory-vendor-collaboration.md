--- 
title: "Satıcı iş birliğini kullanarak konsinye stoğu izleme"
description: "Bu yordam müşteriye konsinye olarak bıraktığınız ürünün stok düzeyi hakkında bilgileri görmek için satıcı işbirliğini kullanmayı gösterir."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Satıcı iş birliğini kullanarak konsinye stoğu izleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam müşteriye konsinye olarak bıraktığınız ürünün stok düzeyi hakkında bilgileri görmek için satıcı işbirliğini kullanmayı gösterir. Ayrıca müşteri stoğun sahipliğini üzerine aldığında stok tüketimini de izleyebilirsiniz. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="view-consumed-inventory"></a>Tüketilen stoğu görüntüleme
1. Satıcı iş birliği > Konsinye stok > Konsinye stoktan alınan ürünler'e gidin.
    * Liste, konsinye stoğun sahipliği satıcıdan müşteri olarak değiştirildiğinde oluşturulan ürün giriş satırlarını gösterir. Miktarları ve diğer bilgileri görmek için ekranı sağa doğru kaydırmanız gerekebilir. Bu listedeki bilgileri müşteriniz için fatura oluşturmada kullanabilirsiniz. Ayrıca verileri Microsoft Excel'e dışa aktarabilirsiniz.   
2. Satınalma siparişini görüntüle öğesine tıklayın.
3. Satır ayrıntıları bölümünü genişletin.
    * Satır, Konsinye olarak işaretlenir ve başlık bölümü satınalma siparişinin Alındı durumuna sahip olduğunu gösterir.  
4. Sayfayı kapatın.

## <a name="view-on-hand-inventory"></a>Eldeki stoğu görüntüleme
1. Satıcı iş birliği > Konsinye stok > Eldeki konsinye stok'a gidin.
    * Eldeki konsinye stok sayfası müşterinin ambarında sahip olduğunu stoğu gösterir. Boyutları görüntüle sekmesine tıklayarak, tesis ve ambar gibi ek boyutları da görüntüleyebilirsiniz.   


