---
title: Satıcı faturasını kaydetme ve teslim alınan miktarla eşleştirme
description: Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa79ab46e9fdc6f8a2b4524d372949314ac2d200
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448758"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Satıcı faturasını kaydetme ve teslim alınan miktarla eşleştirme

[!include [banner](../../includes/banner.md)]

Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir. Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun. 

Borç hesapları parametreleri sayfasında Fatura eşleştirme doğrulaması seçeneğinin işaretlendiğinden, Uyuşmazlıkları olan faturayı deftere naklet alanı ayarının Onay gerektir yapıldığından ve Satır eşleme ilkesi ayarının Üç yönlü eşleştirme yapıldığından emin olun.

Bu yordam, USMF demo şirketini kullanır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. Tüm satınalma siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Satıcı hesabı alanına bir değer girin.
5. Tamam'a tıklayın.
6. Satır ekle'ye tıklayın.
7. Madde numarası alanına bir değer girin.
8. Eylem Bölmesinde, Satınalma öğesine tıklayın.
9. Onayla seçeneğine tıklayın.

## <a name="post-a-product-receipt"></a>Ürün girişini deftere nakledin
1. Eylem Bölmesinde, Al öğesine tıklayın.
2. Ürün girişi seçeneğine tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ürün girişi alanına bir değer girin.
5. Tamam'a tıklayın.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Satıcı faturasını kaydedin ve bir ürün girişiyle eşleyin
1. Eylem Bölmesinde, Fatura öğesine tıklayın.
2. Fatura'ya tıklayın.
3. Numara alanına bir değer girin.
4. Varsayılan başlangıç: Sipariş miktarı'na tıklayarak açılır iletişim kutusunu açın.
5. Satırlar için varsayılan miktar alanında bir seçenek belirtin.
6. Tamam'a tıklayın.
7. Evet'i tıklatın.
8. Ürün girişlerini eşleştir'e tıklayın.
9. Tamam'a tıklayın.
10. Eylem Bölmesinde, Gözden geçir öğesine tıklayın.
11. Eşleşme ayrıntıları öğesine tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]