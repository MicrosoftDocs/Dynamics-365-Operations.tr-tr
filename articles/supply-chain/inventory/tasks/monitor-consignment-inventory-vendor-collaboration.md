---
title: Satıcı iş birliğini kullanarak konsinye stoğu izleme
description: Bu yordam müşteriye konsinye olarak bıraktığınız ürünün stok düzeyi hakkında bilgileri görmek için satıcı işbirliğini kullanmayı gösterir.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2e782bed4cd9f2f13e2ee45afffaef277279131
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020141"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Satıcı iş birliğini kullanarak konsinye stoğu izleme

[!include [banner](../../includes/banner.md)]

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

