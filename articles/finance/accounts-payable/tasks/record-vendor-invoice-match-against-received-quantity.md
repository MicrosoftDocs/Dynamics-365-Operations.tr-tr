---
title: Satıcı faturasını kaydetme ve teslim alınan miktarla eşleştirme
description: Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778694"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Satıcı faturasını kaydetme ve teslim alınan miktarla eşleştirme

[!include [banner](../../includes/banner.md)]

Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir. Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun. 

**Borç hesapları parametreleri** sayfasında **Fatura eşleştirme doğrulamasını etkinleştir** seçeneğinin işaretlendiğinden, **Uyuşmazlıkları olan faturayı deftere naklet** alanı ayarının **Onay gerektir** yapıldığından ve **Satır eşleme ilkesi** alanının **Üç yönlü eşleştirme** yapıldığından emin olun.

Bu yordam, USMF demo şirketini kullanır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. **Tüm satınalma siparişleri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **Satıcı hesabı** alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. **Satıcı hesabı** alanına bir değer girin.
5. **Tamam**'a tıklayın.
6. **Satır ekle**'ye tıklayın.
7. **Madde numarası** alanına bir değer girin.
8. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
9. **Onayla**'yı tıklatın.

## <a name="post-a-product-receipt"></a>Ürün girişini deftere nakledin
1. Eylem Bölmesinde, **Teslim al** öğesine tıklayın.
2. **Ürün girişi** öğesine tıklayın.
3. Listede, seçili satırı işaretleyin.
4. **Ürün girişi** alanına bir değer girin.
5. **Tamam**'a tıklayın.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Satıcı faturasını kaydedin ve bir ürün girişiyle eşleyin
1. Eylem Bölmesinde **Fatura** öğesine tıklayın.
2. **Fatura** öğesine tıklayın.
3. **Numara** alanına bir değer girin.
4. **Varsayılan başlangıç: Sipariş miktarı**'na tıklayarak açılır iletişim kutusunu açın.
5. **Satırlar için varsayılan miktar** alanında bir seçenek belirtin.
6. **Tamam** seçeneğini tıklatın.
7. **Evet** seçeneğini tıklatın.
8. **Ürün girişlerini eşleştir**'e tıklayın.
9. **Tamam** seçeneğini tıklatın.
10. Eylem Bölmesinde, **Gözden geçir** öğesine tıklayın.
11. **Eşleşme ayrıntıları** öğesine tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
