---
title: Satın alma hareketlerinde stopaj vergisi
description: Stopaj vergisi yükümlülüğü olan satıcılar için **Tüm satıcılar** sayfasında varsayılan **Stopaj vergisi grubunu** atayabilirsiniz.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727216"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Satın alma hareketlerinde stopaj vergisi

Stopaj vergisi yükümlülüğü olan satıcılar için **Tüm satıcılar** sayfasında varsayılan **Stopaj vergisi grubunu** atayabilirsiniz.

1. **Gezinti bölmesi > Modüller > Borç hesapları > Satıcılar > Tüm satıcılar**'a gidin.

2. İlgili Satıcı hesabına tıklayın, **Düzenle**'ye tıklayın.

3. **Fatura ve teslimat** sekmesinde, **Stopaj vergisini hesapla** alanını **Evet** olarak ayarlayın.

   > [!NOTE] 
   > Verilerde bu satıcı için **Stopaj vergisini hesapla** açık değilse stopaj vergisi hesaplanmaz.

4. Stopaj vergisi grubundan bir **Stopaj vergisi grubu** seçin.

5. **Kaydet**'e tıklayın.

Stopaj vergisine tabi kelamler/hizmetler için **Serbest Bırakılan Ürünler**'de varsayılan **Kalem stopaj vergisi grubu**'nu atayabilirsiniz.

1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.

2. İlgili Madde numarasına tıklayın, **Düzenle**'ye tıklayın.

3. **Satın alma** sekmesinde **Stopaj vergisini hesapla**'ya tıklayın.

   > [!NOTE] 
   > **Serbest Bırakılan Ürün** sayfasındaki **Satın Alma** sekmesindeki bu madde için **Stopaj Vergisini Hesapla** **Evet** olarak ayarlanmazsa stopaj vergisi hesaplanmaz.

4. **Madde stopaj vergisi grubu** listesinden bir madde stopaj vergisi grubu seçin.

5. **Kaydet**'e tıklayın.

Stopaj vergisi grupları ve Madde stopaj vergisi grupları şu sayfalarda atanabilir: 

- **Satın alma siparişi**
- **Satıcı faturası**
- **Fatura günlüğü**

**Satın alma siparişleri** ve/veya **Bekleyen Satıcı faturaları** oluşturulurken, varsayılan Stopaj vergisi grubu ve Madde stopaj vergisi grubu satırlara aktarılır. **Satıcı fatura günlüğü** için, **Stopaj vergisini hesapla**'yı açabilir ve günlükteki **Genel** sekmesinde **Madde stopaj vergisi grubu**'nu seçebilirsiniz.

Geçici stopaj vergisi tutarı, **Satın alma siparişi** sayfasındaki **Toplamlar** sekmesinin **Ayarlanmış stopaj vergisi** alanında bulunur.

![Stopaj vergisi satın alma siparişine dahildir.](media/withholding-tax-adjusted.png)

Stopaj vergisi, **Satıcı ödeme günlüğünde** hesaplanır. İlgili stopaj vergisi kodlarını ve gerçek stopaj vergisi tutarlarını, **Hareketleri kapat** sayfasındaki **Stopaj vergisi** sekmesinde el ile ayarlayabilirsiniz.

![Stopaj, Hareketleri kapat sayfasında el ile ayarlanabilir.](media/withholding-tax-vendor-payment-tab.png)

Türetilen stopaj vergisi tutarı satıcı ödemesinden düşülür ve ilgili bir fişteki **Stopaj vergisi hesabına** nakledilir.

![İlgili fişi gösteren stopaj vergisi hesabı.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
