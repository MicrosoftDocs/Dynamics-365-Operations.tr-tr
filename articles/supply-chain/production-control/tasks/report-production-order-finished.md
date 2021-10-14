---
title: Üretim emrinin bittiğini rapor etme
description: Bu yordam, bir üretim emrinin nasıl tamamlanmış olarak bildirileceğini gösterir.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa27691942b27886e85c52b7b3a736a62db7b7bd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580612"
---
# <a name="report-a-production-order-as-finished"></a>Üretim emrinin bittiğini rapor etme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir üretim emrinin nasıl tamamlanmış olarak bildirileceğini gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu, üretim emri ömrünü açıklayan yedi yordamdan altıncısıdır.


## <a name="report-a-production-order-as-finished"></a>Üretim emrinin bittiğini rapor etme
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
    * Başlatıldı durumunda olan bir üretim emrini seçin.  
2. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
3. Tamamlandı olarak bildir öğesine tıklayın.
    * Bu sayfada, tamamlanmış olarak bildirilecek tamamlanmış ürün miktarını onaylayabilirsiniz.  
4. Genel sekmesine tıklayın.
5. Sağlam miktarını '18' olacak şekilde ayarlayın.
6. Hata miktarını '2' olacak şekilde ayarlayın.
7. Hata nedeni alanında 'Malzeme' öğesini seçin.
8. Son iş onay kutusunu işaretleyin veya temizleyin.
9. Hatayı kabul et onay kutusunu işaretleyin veya temizleyin.
10. Tamam'a tıklayın.

## <a name="verify-the-report-as-finished-journal"></a>Tamamlandı bildirimi günlüğünü onaylayın.
1. Eylem Bölmesinde, Görüntüle öğesine tıklayın.
2. Tamamlandı olarak işaretle'yi tıklatın.
3. Listede, seçili satırı işaretleyin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
    * Tamamlandı bildirimi günlüğü deftere nakledilir. Günlükte ayarlamalar yapmak istiyorsanız, üzerinde değişiklik yapabileceğiniz yeni bir günlüğü el ile oluşturabilirsiniz.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]