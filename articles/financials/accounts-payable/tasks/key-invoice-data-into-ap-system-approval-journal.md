--- 
title: "Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme"
description: "Bu görev kılavuzu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı gösterecek."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı gösterecek.


## <a name="create-and-post-and-invoice"></a>Fatura oluşturun ve nakledin
1. Borç hesapları > Faturalar > Fatura kaydı'na gidin.
2. Yeni'ye tıklayın.
3. Kullanmak istediğiniz fatura kaydının adını seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Defteri açıp gider satırlarını girmek için Satırlar'a tıklayın.
6. Bir satıcı seçin. Örneğin, ABD-104'ü girin veya seçin
7. Fatura alanına bir değer girin.
8. Tanım alanına bir değer girin.
9. Alacak alanına bir sayı girin.
10. Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.
11. Bir onaylayanı vurgulayın ve o onaylayanı seçmek için Seç'e tıklayın.
12. Deftere Naklet öğesine tıklayın.
13. Sayfayı kapatın.
14. Sayfayı kapatın.

## <a name="approve-an-invoice"></a>Fatura onaylayın
1. Borç hesapları > Faturalar > Fatura onayı'na gidin.
2. Yeni'ye tıklayın.
3. Kullanmak istediğiniz fatura onayı günlüğünün adını seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Onaylamak istediğiniz faturaları seçebileceğiniz bir sayfayı görüntülemek için Satırlar'a tıklayın.
6. Onaya hazır olan faturaların tümünü görüntülemek için Fişleri bul'u seçin.
7. Oluşturduğunuz faturayı işaretleyin.
8. Seç'e tıklayın.
    * Yukarıda seçtiğiniz fişler, seçiminizden sonra bu listeye taşınır.  
9. Tamam'a tıklayın.
10. Faturaya bir gider hesabı eklemek için Hesap numarası alanına tıklayın.
11. Hesap numarası girin ve sekme tuşuyla alandan çıkın. Örneğin, 600120 girin.
12. Deftere Naklet öğesine tıklayın.
13. Nakledilen girişleri görüntülemek için Fiş'e tıklayın.
    * Onay Bekleyen Fatura hesabı ters kaydedilir ve yerine gerçek gider hesabı geçirilir.  


