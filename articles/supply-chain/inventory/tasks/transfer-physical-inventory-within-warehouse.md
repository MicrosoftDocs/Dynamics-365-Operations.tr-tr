---
title: Ambar içindeki fiziksel stoğu transfer etme
description: Bu yordam, bir ürünün bir yerleşimden başka bir yerleşimdeki ambara taşınması kaydı için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7715c8e7a56703993e8512af03f2ab8d6802a987
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916588"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Ambar içindeki fiziksel stoğu transfer etme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir ürünün bir yerleşimden başka bir yerleşimdeki ambara taşınması kaydı için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar. Buna başlamadan önce stok transferleri için ayarlanmış bir stok günlüğü adı olması gerekir. USMF demo verisi şirketindeki bu yordam ile gösterilen örnek değerleri nasıl kullanacağınızı veya ayarlanmış ürün ve yerleşimleriniz varsa kendi verilerinizi nasıl kullanacağınızı adım adım görebilirsiniz. Bu görevler normalde ambar personeli tarafından yerine getirilir.


## <a name="create-an-inventory-transfer-journal"></a>Bir stok transferi günlüğü yaratma
1. **Gezinti bölmesinde**, **Stok yönetimi > Maddelerin girdileri> Maddeler > Aktarma** üzerine gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. **Tamam**'a tıklayın. Her bir günlük satırının 'Başlangıç' ve 'Bitiş' boyutlarını belirtmek için seçenek vardır. Bu günlük türü için bunlar önemlidir. Ürünleri yerleşimlere farklı kurallar kullanarak transfer edebilirsiniz. Bu örnekte, aynı ambar içindeki bir ürün bir plaka denetimli olan bir yerleşimden plaka denetimli olmayan bir yerleşime transfer ediliyor.   

## <a name="create-journal-lines"></a>Günlük satırları oluştur
1. **Günlük satırları hızlı sekmesi** içinde **Yeni** üzerine tıklayın.
2. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin. USMF kullanıyorsanız, 'A0001' öğesini seçebilirsiniz.  
3. **Kaynak tesis** alanında bir değer girin veya bir değer seçin. USMF kullanıyorsanız, '2' öğesini seçebilirsiniz.  
4. **Hedef tesis** alanında bir değer girin veya bir değer seçin. USMF kullanıyorsanız, '2' öğesini seçebilirsiniz.  
5. **Kaynak ambar** alanında bir değer girin veya bir değer seçin. USMF kullanıyorsanız, '24' öğesini seçebilirsiniz.  
6. **Hedef ambar** alanında bir değer girin veya bir değer seçin. USMF kullanıyorsanız, '24' öğesini seçebilirsiniz.  
7. **Çıkış yerleşimi** alanında bir değer girin veya seçin. USMF kullanıyorsanız, 'FL-001' öğesini seçebilirsiniz.  
8. **Hedef yerleşim** alanında bir değer girin veya seçin. USMF kullanıyorsanız, 'BULK-001' öğesini seçebilirsiniz.  
9. **Miktar** alanına bir sayı girin.
10. **Satır ayrıntıları** hızlı sekmesinde, **Stok boyutları** sekmesini tıklatın.
11. **Giden stok boyutları** içinde, **Lisans plakası** alanında, bir değer girin ya da seçin. USMF kullanıyorsanız, '24' öğesini seçebilirsiniz.  
12. **Kaydet**'e tıklayın.

## <a name="post-the-inventory-transfer-journal"></a>Stok transfer günlüğünü deftere nakletme
1. **Eylem bölmesinde** **Deftere naklet** öğesine tıklayın.
2. **Tamam**'a tıklayın.

## <a name="view-inventory-transactions"></a>Stok hareketlerini görüntüle
1. **Stok**'u tıklatın.
2. **Hareketler**'i tıklatın. Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.  

