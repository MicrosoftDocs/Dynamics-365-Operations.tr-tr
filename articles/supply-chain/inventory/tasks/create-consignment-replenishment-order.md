---
title: Konsinye stok yenileme siparişi oluşturma
description: Bu konu bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı açıklar.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9076207b73c6c76cfc44e1e02b21aad4e3f321f8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574605"
---
# <a name="create-a-consignment-replenishment-order"></a>Konsinye stok yenileme siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı açıklar. Ayrıca ürünlerin alımını, konsinye stoğun satıcının sahibi olduğu eldeki stok olarak kaydedilecek şekilde kaydetmeyi de gösterir. Bu yordam normalde tedarik profesyoneli tarafından gerçekleştirilir. Bu kılavuzu USMF demo şirketinde kullanabilirsiniz. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.

## <a name="create-a-consignment-replenishment-order"></a>Konsinye stok yenileme siparişi oluşturma
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Konsinye > Konsinye stok yenileme siparişleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. **Satıcı hesabı** alanında, satıcı **USD-104**'ü seçin (**stok sahipleri** sayfasında sahip olarak kayıtlı bir satıcıyı seçmeniz gerekir). 
4. **Tamam**'ı seçin.
5. **Satır ekle**'yi seçin.
6. **Madde numarası** alanına, `M9211CI` yazın (konsinye stok için ayarlanmış bir maddeyi seçmeniz gerekir).
7. **Miktar** alanına bir sayı girin.
8. **İstenen teslim tarihi** alanına bir tarih girin. İstenen ve onaylanan tarihler, malların beklenen varış tarihi için MRP altyapısı tarafından kullanılır.  
9. **Teyit edilmiş teslimat tarihi** alanına bir tarih girin.
10. **Satır ayrıntıları** bölümünü genişletin.
11. **Stok boyutları** sekmesini seçin.
12. **Stok boyutları sahibi** alanında sahibi göstermek için sayfayı yenileyin. Satıcı US-104 artık sahip olarak listelenir.  

## <a name="check-the-inventory-transaction-status"></a>Stok hareketi durumunu denetleme
1. **Stok**'u seçin.
2. **Hareketler**'i seçin.
3. İstenen satırda **Giriş** alanının **Sipariş edildi** olarak ayarlandığına dikkat edin.  
4. Sayfayı kapatın.

## <a name="receive-items"></a>Maddeleri al
1. **Ürün girişi**'ni seçin.
2. **Harici ürün girişi** alanına bir değer yazın.
3. **Miktar** alanına, burada gösterilenden daha küçük bir sayı girin. 
4. **Tamam**'ı seçin.

## <a name="check-the-on-hand-inventory"></a>Eldeki stoğu denetleme
1. **Stok**'u seçin.
2. **Eldeki** öğesini seçin.
3. **Genel bakış**'ı seçin. Satıcının sahip olduğu konsinye, stok olarak alınan maddelerin elde kullanılabilirdir. Konsinye stok yenileme siparişinde kalan miktar **Toplam sipariş edilen** alanında gösterilir.  
4. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]