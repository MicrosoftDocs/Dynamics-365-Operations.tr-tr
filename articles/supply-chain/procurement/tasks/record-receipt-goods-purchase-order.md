--- 
title: "Satınalma siparişindeki malların girişini kaydetme"
description: "Bu yordam, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini gösterir."
author: FrankDahl
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Satınalma siparişindeki malların girişini kaydetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini gösterir. Ayrıca ambarda ürün girişini kaydedip ardından satınalma siparişi üzerinde kaydetmek de mümkündür. Bu görev genelde bir satınalma temsilcisi veya bir borç hesapları koordinatörü tarafından yapılır. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Örnek, yordamı bir görev kılavuzu gibi kullanabilmeniz için basit bir satınalma siparişini oluşturma adımlarını içerir. Yordamı kendi verilerinizde kullanıyorsanız Mal girişini kaydet alt görevinden başlamalısınız.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Malların girişi için yeni bir satınalma siparişi hazırlayın
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanına, US-101 girin.
4. Tamam'a tıklayın.
5. Madde numarası alanına M0001 girin.
6. Miktar alanına 5 girin.
7. Eylem Bölmesinde, Satınalma öğesine tıklayın.
8. Onayla seçeneğine tıklayın.

## <a name="record-receipt-of-goods"></a>Mal girişini kaydetme
1. Eylem Bölmesinde, Al öğesine tıklayın.
2. Ürün girişi seçeneğine tıklayın.
    * Miktar alanı almak istediğiniz miktar için farklı seçenekler seçmenize olanak sağlar. Örneğin, bir miktar daha önceden ambarda kaydedildiyse Kayıtlı miktarı seçebilirsiniz.  Bu örnek için Sipariş edilen miktar değerini kullanın.   
3. Ürün girişi alanına herhangi bir değer yazın.
    * Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.  
4. Satırlar bölümünü genişletin.
5. Miktarı '4' olarak ayarlayın.
    * Burada, sipariş üzerindeki her bir satır için alınan miktarı el ile belirleyebilme imkanınız bulunur.  
6. Satırlar bölümünü daraltın.
7. Tamam'a tıklayın.
    * Mallar şimdi satınalma siparişinde alındı olarak kaydedilir ve bunu yansıtan belge olarak bir ürün giriş yevmiye defteri oluşturulur. Satınalma siparişiyle oluşturulan günlükleri gözden geçirmek ve nelerin ve ne zaman alındığını görmek için Ürün giriş etkinliğini kullanabilirsiniz.  


