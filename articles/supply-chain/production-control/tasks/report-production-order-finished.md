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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9b676ffefa9fd4b8d66a5c35012630295f8a263
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828622"
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