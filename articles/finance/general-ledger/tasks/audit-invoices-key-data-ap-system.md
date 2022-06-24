---
title: Borç hesaplarındaki faturaları ve önemli verileri denetleme
description: Bu makalede, borç hesaplarındaki faturaların ve önemli verilerin nasıl denetleneceği açıklanır.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76c45133091a86da773d7f63addd460abd92aae7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868372"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Borç hesaplarındaki faturaları ve önemli verileri denetleme

[!include [banner](../../includes/banner.md)]

Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir. Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun. 

**Borç hesapları parametreleri** sayfasında Fatura eşleştirme doğrulaması seçeneğinin işaretlendiğinden, **Uyuşmazlıkları olan faturayı deftere naklet** alanı ayarının **Onay gerektir** yapıldığından ve **Satır eşleme ilkesi** ayarının **Üç yönlü eşleştirme** yapıldığından emin olun.

Bu yordam, USMF demo şirketini kullanır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. **Tüm satınalma siparişleri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **Satıcı hesabı** alanına bir değer girin.
4. **Tamam** seçeneğini tıklatın.
5. **Satır ekle**'ye tıklayın.
6. **Madde numarası** alanına bir değer girin.
7. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
8. **Onayla**'yı tıklatın.

## <a name="post-a-product-receipt"></a>Ürün girişini deftere nakledin
1. Eylem Bölmesinde, **Teslim al** öğesine tıklayın.
2. **Ürün girişi** öğesine tıklayın.
3. **Ürün girişi** alanına bir değer girin.
4. **Tamam** seçeneğini tıklatın.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Satıcı faturasını kaydedin ve bir ürün girişiyle eşleyin
1. Eylem Bölmesinde, **Fatura > Fatura** öğesine tıklayın.
2. **Numara** alanına bir değer girin.
3. **Varsayılan başlangıç: Sipariş miktarı**'na tıklayarak açılır iletişim kutusunu açın.
4. **Satırlar için varsayılan miktar** alanında bir seçenek belirtin.
5. **Tamam** seçeneğini tıklatın.
6. **Evet** seçeneğini tıklatın.
7. **Ürün girişlerini eşleştir**'e tıklayın.
8. **Tamam** seçeneğini tıklatın.
9. Eylem Bölmesinde, **Gözden geçir** öğesine tıklayın.
10. **Eşleşme ayrıntıları** öğesine tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
