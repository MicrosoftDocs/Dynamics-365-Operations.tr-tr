--- 
title: "Tek seferlik tedarikçi için satınalma siparişi oluşturma"
description: "Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Tek seferlik tedarikçi için satınalma siparişi oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir. Satıcı hesabını el ile oluşturmak yerine tedarikçi satınalma siparişi ile otomatik olarak oluşturulur. Satınalma siparişleri genellikle bir satınalma temsilcisi tarafından oluşturulur. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Tek seferlik satıcı hesabının Hesap borç parametreleri sayfasında ayarlanması bir önkoşuldur.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Tek seferlik tedarikçi için satınalma siparişi oluşturma
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Tek seferlik tedarikçi alanında Evet'i seçin.
    * Bir satıcı hesabı otomatik olarak oluşturulur ve satınalma siparişine atanır. Satıcı hesabı, Borç hesapları parametreleri sayfasındaki Genel sekmede belirtilen şablona göre oluşturulur.  
4. Ad alanına tedarikçinin adını yazın.
5. Tamam'a tıklayın.
    * Satınalma siparişi şimdi tamamlanabilir ve başka bir sipariş gibi işlenebilir. Bunun yapılmasıyla ilgili özel karakterler bulunmamaktadır. Fatura, hareket vade sonunu siparişle oluşturulmuş satıcı hesabı üzerinden dahil eder ve sonra ödeme işlenir. Bu tamamlandığında, satıcı hesabı silinebilir. Bu genellikle Borç hesapları departmanı tarafından yapılır.  


