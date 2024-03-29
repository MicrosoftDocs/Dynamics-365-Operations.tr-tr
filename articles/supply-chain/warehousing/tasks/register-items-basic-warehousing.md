---
title: Bir madde geliş günlüğü kullanılarak temel ambarlama için etkinleştirilen madde için maddeleri kaydetme
description: Bu prosedürde, Stok yönetimi modülündeki "temel depolama" işlevini kullanırken madde varış günlüğüyle maddelerin nasıl kaydedileceğini göreceksiniz.
author: Mirzaab
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76dd2bfd57db7dfd5c2baf59a864e59a509a64e0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577804"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Bir madde geliş günlüğü kullanılarak temel ambarlama için etkinleştirilen madde için maddeleri kaydetme

[!include [banner](../../includes/banner.md)]

Bu prosedürde, Stok yönetimi modülündeki "temel depolama" işlevini kullanırken madde varış günlüğüyle maddelerin nasıl kaydedileceğini göreceksiniz. Bu genellikle bir teslim alma memuru tarafından yapılır. Bu prosedürü demo veri şirketi USMF'de, gösterilen örnek değerlerle çalıştırabilirsiniz.  USMF kullanmıyorsanız, bu kılavuzu başlatmadan önce, elinizde açık bir satınalma siparişi satırı içeren onaylı bir satınalma siparişi bulunması gerekir. Satırdaki öğenin stoğunun tutulması gerekir Ayrıca, maddenin tesis ve ambarın etkin olduğu bir depolama boyutu grubuyla ilişkilendirilmesi gerekir.


## <a name="create-item-arrival-journal-header"></a>Bir madde varış günlüğü üst bilgisi oluşturun
1. Stok yönetimi > Yevmiye defteri girişleri > Madde varışı > Madde varışı öğesine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
    * USMF kullanıyorsanız, WHS yazabilirsiniz. Başka veriler kullanıyorsanız, adını seçtiğiniz günlükte iki özelliğin olması gerekir: Malzeme çekme yerleşimini denetle ayarı Hayır, Karantina yönetimi ayarı Hayır olmalıdır.  
4. Sevk irsaliyesi alanına bir değer girin.
    * Bu, satıcının çıkardığı sevk irsaliyesindeki sevk irsaliyesi kodudur. Benzersiz bir numara ekleyin.  
5. Numara alanında, satınalma siparişini seçin.
6. Tamam'a tıklayın.

## <a name="add-lines-to-item-arrival-journal"></a>Madde varış günlüğüne satırlar ekleyin
1. İşlevler'i tıklatın.
2. Satır oluştur'a tıklayın.
    * Satırlar bu günlüğe el ile girilebilir veya otomatik olarak oluşturulabilir. Burada size bunun otomatik olarak nasıl oluşturulduğu gösterilecek.  
3. Miktarı başlat onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
    * Bu, satın alma siparişi satırında kaydedilmemiş miktarı olan yevmiye defteri satırlarında miktarı başlatır.  
4. Tamam'a tıklayın.

## <a name="post-the-journal"></a>Günlüğü deftere naklet
1. Deftere Naklet öğesine tıklayın.
2. Tamam'a tıklayın.

## <a name="generate-the-product-receipt"></a>Ürün girişini oluşturun
1. İşlevler'i tıklatın.
2. Ürün girişi seçeneğine tıklayın.
3. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]