--- 
title: "Satış fiyatı seçim ölçütü oluşturma"
description: "Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59f6a4131f6a27c0089a1259e3f849f91a47bc87
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-price-selection-criteria"></a>Satış fiyatı seçim ölçütü oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir. Bu yordam için kullanılabilir en az bir satış fiyatı modeli olması gerekir. Bu örnek için, USMF demo veri şirketinde Hoparlör çözümü satış fiyatı modeli için fiyat modeli kullanılır. Genel olarak bu yordamı bir ürün yöneticisi kullanır.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Mevcut satış fiyatı modeli için yeni bir ölçüt ekleme
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, Hoparlör çözümü ürün modeli için satır seçin ancak model adı bağlantısına tıklamayın.
4. Eylem Bölmesinde,Model öğesine tıklayın.
5. Fiyat modeli ölçütlerine tıklayın.
6. Yeni'ye tıklayın.
7. Ad alanına "Müşteri grubu 10" yazın.
    * Fiyat modeli ölçütünün adı, temel alınan seçim ölçütlerinin tanımlanmasına yardımcı olmak için kullanılır.  
8. Fiyat modeli alanına bir değer girin veya seçin.
9. Sipariş türü alanında Satış siparişi'ni seçin.
    * Sipariş türü seçim sorgusu için kullanılacak veri tabanı alanlarını belirler.  
10. Geçerlilik başlangıcı alanına bir tarih girin.
11. Geçerlilik sonu alanına bir tarih girin.
12. Kaydet'e tıklayın.

## <a name="create-the-query-for-the-selection-criteria"></a>Seçim ölçütleri için sorgu oluşturma
1. Düzenle öğesine tıklayın.
2. Tablo alanında, Müşteriler'i seçin. 
3. Alan alanında Müşteri grubu'nu seçin.
    * Bu örnekte, seçim ölçütü için belirli bir müşteri grubu kullanacağız.  
4. Ölçütler alanında Müşteri grubu 10'u seçin. 
5. Tamam'a tıklayın.


