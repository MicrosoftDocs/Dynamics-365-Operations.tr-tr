---
title: Satınalma siparişindeki malların girişini kaydetme
description: Bu konu, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini açıklar.
author: mkirknel
manager: tfehr
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6365ccf4414e49bc1f22bcedb42f192c5c9a5ee8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207635"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Satınalma siparişindeki malların girişini kaydetme

[!include [banner](../../includes/banner.md)]

Bu konu, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini açıklar. Ayrıca ambarda ürün girişini kaydedip ardından satınalma siparişi üzerinde kaydetmek de mümkündür. Bu görev genelde bir satınalma temsilcisi veya bir borç hesapları koordinatörü tarafından yapılır. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Örnek, yordamı bir görev kılavuzu gibi kullanabilmeniz için basit bir satınalma siparişini oluşturma adımlarını içerir. Yordamı kendi verilerinizde kullanıyorsanız **Mal girişini kaydet** alt görevinden başlamalısınız.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Malların girişi için yeni bir satınalma siparişi hazırlayın
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma siparişleri > Tüm satınalma siparişleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. **Satıcı hesabı** alanına `US-101` girin.
4. **Tamam**'ı seçin.
5. **Madde numarası** alanına `M0001` girin.
6. **Miktar** alanına `5` girin.
7. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
8. **Onayla**'yı seçin.

## <a name="record-receipt-of-goods"></a>Mal girişini kaydetme
1. Eylem Bölmesinde, **Teslim alma**'yı seçin.
2. **Ürün girişi**'ni seçin. **Miktar** alanı almak istediğiniz miktar için farklı seçenekler seçmenize olanak sağlar. Örneğin, bir miktar daha önceden ambarda kaydedildiyse **Kayıtlı miktar**'ı seçebilirsiniz. Bu örnek için **Sipariş edilen miktar** değerini kullanın.
3. **Genel bakış** bölümünü genişletin.
4. **Ürün girişi** alanına herhangi bir değer yazın. Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.  
5. **Satırlar** bölümünü genişletin.
6. **Miktar**'ı '4' olarak ayarlayın. Burada, sipariş üzerindeki her bir satır için alınan miktarı el ile belirleyebilme imkanınız bulunur.  
7. **Tamam**'ı seçin. Mallar şimdi satınalma siparişinde alındı olarak kaydedilir ve bunu yansıtan belge olarak bir ürün giriş yevmiye defteri oluşturulur. Satınalma siparişiyle oluşturulan günlükleri gözden geçirmek ve nelerin ve ne zaman alındığını görmek için Ürün giriş etkinliğini kullanabilirsiniz.  

