---
title: Ambar içindeki fiziksel stoğu transfer etme
description: Bu yordam, bir ürünün bir yerleşimden başka bir yerleşimdeki ambara taşınması kaydı için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: yufeihuang
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf5a3711cfcd6e5a2ddce09af8569ea26c3502c8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580804"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Ambar içindeki fiziksel stoğu transfer etme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ürünün bir yerleşimden başka bir yerleşimdeki ambara taşınması kaydı için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar. Buna başlamadan önce stok transferleri için ayarlanmış bir stok günlüğü adı olması gerekir. USMF demo verisi şirketindeki bu yordam ile gösterilen örnek değerleri nasıl kullanacağınızı veya ayarlanmış ürün ve yerleşimleriniz varsa kendi verilerinizi nasıl kullanacağınızı adım adım görebilirsiniz. Bu görevler normalde ambar personeli tarafından yerine getirilir.


## <a name="create-an-inventory-transfer-journal"></a>Bir stok transferi günlüğü yaratma
1. **Gezinti bölmesinde**, **Stok yönetimi > Maddelerin girdileri> Maddeler > Aktarma** üzerine gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. **Tamam**'a tıklayın. Her bir yevmiye defteri satırının 'Başlangıç' ve 'Bitiş' boyutlarını belirtmek için seçenek vardır. Bu günlük türü için bunlar önemlidir. Ürünleri yerleşimlere farklı kurallar kullanarak transfer edebilirsiniz. Bu örnekte, aynı ambar içindeki bir ürün bir plaka denetimli olan bir yerleşimden plaka denetimli olmayan bir yerleşime transfer ediliyor.   

## <a name="create-journal-lines"></a>Yevmiye defteri satırları oluştur
1. **Yevmiye defteri satırları hızlı sekmesi** içinde **Yeni** üzerine tıklayın.
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
1. **Eylem Bölmesi**'nde **Deftere naklet** öğesine tıklayın.
2. **Tamam**'a tıklayın.

## <a name="view-inventory-transactions"></a>Stok hareketlerini görüntüle
1. **Stok**'u tıklatın.
2. **Hareketler**'i tıklatın. Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]