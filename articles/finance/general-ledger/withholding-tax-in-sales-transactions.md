---
title: Satış hareketlerinde stopaj vergisi
description: Bu konuda, seçili müşteriler için stopaj vergisinin hesaplanmasından kaçınma adımları listelenir. Size ödemelerinde stopaj vergisi belirten müşteriler için varsayılan stopaj vergisi grubunu atayabilirsiniz.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: b221fc04ef82f148846fc0c282f6c8601f0eb4759d99a8dee02256cc0d42417f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747095"
---
# <a name="withholding-tax-in-sales-transactions"></a>Satış hareketlerinde stopaj vergisi

Bu konuda, seçili müşteriler için stopaj vergisinin hesaplanmasından kaçınma adımları listelenir. Size ödemelerinde stopaj vergisi belirten müşteriler için **Müşteriler** sayfasında varsayılan **Stopaj vergisi grubu**'nu atayabilirsiniz. 

1. **Gezinti bölmesi > Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.

2. İlgili müşteri hesabına tıklayın, **Düzenle**'yi tıklayın.

3. **Fatura ve teslimat** sekmesinde, **Stopaj vergisini hesapla** alanını **Evet** olarak ayarlayın.

   > [!NOTE] 
   > Master verilerde bu müşteri için **Stopaj vergisini hesapla** açık değilse stopaj vergisi hesaplanmaz.

4. Stopaj vergisi grubundan bir **Stopaj vergisi grubu** seçin.

5. **Kaydet**'e tıklayın.

Stopaj vergisine tabi kelamler/hizmetler için **Serbest Bırakılan Ürünler**'de varsayılan **Kalem stopaj vergisi grubu**'nu atayabilirsiniz.

1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.

2. İlgili Madde numarasına tıklayın, **Düzenle**'ye tıklayın.

3. **Satış** sekmesinde **Stopaj vergisini hesapla**'ya tıklayın.

   > [!NOTE] 
   > **Serbest Bırakılan Ürün** sayfasındaki **Satış** sekmesindeki bu madde için **Stopaj Vergisini Hesapla** **Evet** olarak ayarlanmazsa stopaj vergisi hesaplanmaz.

4. **Madde stopaj vergisi grubu** listesinden bir madde stopaj vergisi grubu seçin.

5. **Kaydet**'e tıklayın.

Stopaj vergisi grupları ve madde stopaj vergisi grupları **Satış siparişi** sayfası kullanılarak atanabilir. 

Yeni bir satış siparişi oluşturduğunuzda, varsayılan Stopaj vergisi grubu ve Madde stopaj vergisi grubu satış siparişi satırlarında varsayılan girişler olarak kullanılır.

Stopaj vergisi hesaplanır ve **Müşteri ödeme günlüğü**'ne nakledilir. İlgili stopaj vergisi kodunu ve gerçek stopaj vergisi tutarını, **Hareketleri kapat** sayfasındaki **Stopaj vergisi** sekmesinde el ile ayarlayabilirsiniz.

Hesaplanan stopaj vergisi tutarı müşteri ödemesinden düşülür ve ilgili bir fişteki **Stopaj vergisi mahsubu** hesabına nakledilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]