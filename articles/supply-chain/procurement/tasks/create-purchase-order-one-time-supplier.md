---
title: Tek seferlik tedarikçi için satınalma siparişi oluşturma
description: Bu prosedür, size satınalma siparişinin tek seferlik bir tedarikçi için nasıl oluşturulacağını gösterir.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e6c8283290564d930418c1832bbd285532445ff0e69db8f78d13542c8232e97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720312"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]