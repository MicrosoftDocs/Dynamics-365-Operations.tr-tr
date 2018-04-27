---
title: "Konsinye stok yenileme siparişi oluşturma"
description: "Bu yordam bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı gösterir."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Konsinye stok yenileme siparişi oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı gösterir. Ayrıca ürünlerin alımını, konsinye stoğun satıcının sahibi olduğu eldeki stok olarak kaydedilecek şekilde kaydetmeyi de gösterir. Bu yordam normalde tedarik profesyoneli tarafından gerçekleştirilir. Bu kılavuzu USMF demo şirketinde kullanabilirsiniz. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.




## <a name="create-a-consignment-replenishment-order"></a>Konsinye stok yenileme siparişi oluşturma
1. Tedarik ve kaynak atama > Konsinye > Konsinye stok yenileme siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında satıcı US-104'ü seçin.
    * Stok sahipleri sayfasında sahip olarak kayıtlı bir satıcı seçmeniz gerekir.  
4. Tamam'a tıklayın.
5. Satır ekle'ye tıklayın.
6. Madde numarası alanına M9211CI yazın.
    * Konsinye stoğu için ayarlanmış bir madde seçmeniz gerekir.  
7. Miktar alanına bir sayı girin.
8. İstenen teslim tarihi alanına bir tarih girin.
    * İstenen ve onaylanan tarihler, malların beklenen varış tarihi için MRP altyapısı tarafından kullanılır.  
9. Teyit edilmiş teslimat tarihi alanına bir tarih girin.
10. Satır ayrıntıları bölümünü genişletin.
11. Stok boyutları sekmesine tıklayın.
12. Stok boyutları sahibi alanında sahibi göstermek için sayfayı yenileyin.
    * Satıcı US-104 artık sahip olarak listelenir.  

## <a name="check-the-inventory-transaction-status"></a>Stok hareketi durumunu denetleme
1. Stok'u tıklatın.
2. Hareketler'e tıklayın.
3. Listede, seçili satırı işaretleyin.
    * Giriş alanının Sipariş edildi olarak ayarlandığına dikkat edin.  
4. Sayfayı kapatın.

## <a name="receive-items"></a>Maddeleri al
1. Ürün girişi seçeneğine tıklayın.
2. Harici ürün girişi alanına bir değer yazın.
3. Miktar alanına, burada gösterilenden daha küçük bir sayı girin.
4. Tamam'a tıklayın.

## <a name="check-the-on-hand-inventory"></a>Eldeki stoğu denetleme
1. Stok'u tıklatın.
2. Eldeki öğesine tıklayın.
3. Genel Bakış'a tıklayın.
    * Satıcının sahip olduğu konsinye, stok olarak alınan maddelerin elde kullanılabilirdir. Konsinye stok yenileme siparişinde kalan miktar Toplam sipariş edilen alanında gösterilir.  
4. Sayfayı kapatın.
5. Kapat’a tıklayın.

