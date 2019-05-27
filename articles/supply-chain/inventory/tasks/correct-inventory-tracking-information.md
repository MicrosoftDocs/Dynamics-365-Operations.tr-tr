---
title: Stok izleme bilgilerini düzeltme
description: Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfe0f6995598757dcea824e1bb4f7ef8ab54a67b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549944"
---
# <a name="correct-inventory-tracking-information"></a>Stok izleme bilgilerini düzeltme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar. Bu örnekte, başka bir toplu iş için yanlış kaydedilmiş bir toplu iş değiştirerek denetlenen toplu iş ürününün bilgileri güncelleştirilir. Bu yordamı, USPI demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. Kendi verilerinizi kullanıyorsanız, toplu iş etkin olan bir ürününüz olması ve yerleşim denetimli olmaması gerekir. Stok transferleri için ayarlanmış bir stok günlüğü adı da olması gerekir. Bu görevler normalde ambar personeli tarafından yerine getirilir.


## <a name="create-an-inventory-transfer-journal"></a>Bir stok transferi günlüğü yaratma
1. Transfer'e gidin.
2. Yeni'ye tıklayın.
3. Ad alanına bir değer girin veya buradan bir değer seçin.
4. Tamam'a tıklayın.

## <a name="create-journal-lines"></a>Günlük satırları oluştur
1. Yeni'ye tıklayın.
2. Madde numarası alanında bir değer girin veya seçin.
    * USPI kullanıyorsanız, M5003 öğesini seçin.  
3. Miktar alanına bir sayı girin.
4. Stok boyutları sekmesine tıklayın.
5. Ürün numarası alanında bir değer girin veya seçin.
6. Tesis alanına bir değer girin veya buradan bir değer seçin.
7. Ambar alanında bir değer girin veya bir değer seçin.
8. Ürün numarası alanında bir değer girin veya seçin.

## <a name="post-the-journal"></a>Günlüğü deftere naklet
1. Deftere Naklet öğesine tıklayın.
2. Tamam'a tıklayın.

## <a name="check-tracing-information"></a>İzleme bilgilerini denetleme
1. Stok'u tıklatın.
2. İzle'yi tıklatın.
3. Tamam'a tıklayın.
    * Bu izleme bilgilerini kullanarak stoktan düzeltilen toplu işi izleyebilirsiniz.  Bu bilgileri görmek için Ürün izleme sayfasını da kullanabilirsiniz.  
4. Sayfayı kapatın.

## <a name="check-inventory-transactions"></a>Stok hareketlerini denetleme
1. Stok'u tıklatın.
2. Hareketler'e tıklayın.
    * Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.   

