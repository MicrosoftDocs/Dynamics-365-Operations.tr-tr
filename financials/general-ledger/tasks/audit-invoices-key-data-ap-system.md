--- 
title: "Borç hesaplarındaki faturaları ve önemli verileri denetleme"
description: "Satınalma siparişindeki mal ve hizmetler için satıcıdan bir fatura aldığınızda, iş süreçleri faturanın ödeme onayı alabilmesi için mal veya hizmetlerin alınmış olmasını gerektirebilir."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 38cc5587d970d05492638ed349484e6c002d5363
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Borç hesaplarındaki faturaları ve önemli verileri denetleme

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


