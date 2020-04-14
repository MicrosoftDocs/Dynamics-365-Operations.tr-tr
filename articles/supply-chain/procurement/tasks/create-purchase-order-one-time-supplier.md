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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a55cd8f21b99589a44f7509123d3417fd9dc07f6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147446"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Tek seferlik tedarikçi için satınalma siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir. Satıcı hesabını el ile oluşturmak yerine tedarikçi satınalma siparişi ile otomatik olarak oluşturulur. Satınalma siparişleri genellikle bir satınalma temsilcisi tarafından oluşturulur. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Tek seferlik satıcı hesabının Hesap borç parametreleri sayfasında ayarlanması bir önkoşuldur.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Tek seferlik tedarikçi için satınalma siparişi oluşturma
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Tek seferlik tedarikçi alanında Evet'i seçin.
    * Bir satıcı hesabı otomatik olarak oluşturulur ve satınalma siparişine atanır. Satıcı hesabı, Borç hesapları parametreleri sayfasındaki Genel sekmede belirtilen şablona göre oluşturulur.  
4. Ad alanına tedarikçinin adını yazın.
5. Tamam'a tıklayın.
    * Satınalma siparişi şimdi tamamlanabilir ve başka bir sipariş gibi işlenebilir. Bunun yapılmasıyla ilgili özel karakterler bulunmamaktadır. Fatura, hareket vade sonunu siparişle oluşturulmuş satıcı hesabı üzerinden dahil eder ve sonra ödeme işlenir.

