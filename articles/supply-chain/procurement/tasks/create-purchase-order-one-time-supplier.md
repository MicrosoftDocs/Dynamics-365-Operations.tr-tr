---
title: Tek seferlik tedarikçi için satınalma siparişi oluşturma
description: Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beaf6bcbc870e11e74289375611c631306545633
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "312888"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Tek seferlik tedarikçi için satınalma siparişi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir. Satıcı hesabını el ile oluşturmak yerine tedarikçi satınalma siparişi ile otomatik olarak oluşturulur. Satınalma siparişleri genellikle bir satınalma temsilcisi tarafından oluşturulur. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Tek seferlik satıcı hesabının Hesap borç parametreleri sayfasında ayarlanması bir önkoşuldur.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Tek seferlik tedarikçi için satınalma siparişi oluşturma
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Tek seferlik tedarikçi alanında Evet'i seçin.
    * Bir satıcı hesabı otomatik olarak oluşturulur ve satınalma siparişine atanır. Satıcı hesabı, Borç hesapları parametreleri sayfasındaki Genel sekmede belirtilen şablona göre oluşturulur.  
4. Ad alanına tedarikçinin adını yazın.
5. Tamam'a tıklayın.
    * Satınalma siparişi şimdi tamamlanabilir ve başka bir sipariş gibi işlenebilir. Bunun yapılmasıyla ilgili özel karakterler bulunmamaktadır. Fatura, hareket vade sonunu siparişle oluşturulmuş satıcı hesabı üzerinden dahil eder ve sonra ödeme işlenir. Bu tamamlandığında, satıcı hesabı silinebilir. Bu genellikle Borç hesapları departmanı tarafından yapılır.  

