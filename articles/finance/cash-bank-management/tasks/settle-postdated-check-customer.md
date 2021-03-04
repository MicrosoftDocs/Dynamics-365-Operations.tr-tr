---
title: Müşterinin ileri tarih atılmış çekini kapatma
description: Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448878"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Müşterinin ileri tarih atılmış çekini kapatma

[!include [banner](../../includes/banner.md)]

Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir. Bu mali işlem ayrıca vadeli çek için köprü hesabı hareketini de kapatmaktadır. 

Buna başlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir.

1) İleri tarih atılmış çekleri ayarlama

2) Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme 



Bu görevin rolü Haznedar'dır.



Bu yordam, USMF demo şirketini kullanır.

1. Kredi ve Tahsilatlar > Sorguları ve raporları > Ödemeler > Müşteri vadeli çekleri seçeneğine gidin.
2. Kapatma'yı tıklayın.
3. Kliring girişlerini kapat'a tıkla.
    * Çek hareketi için müşteri hesabını kapatın.  
4. Sayfayı kapatın.
5. Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.
6. Göster alanında, bir seçenek seçin.
7. Sadece kullanıcı tarafından oluşturulmuş onay kutusunu temizleyin veya seçin.
8. Listede, istenen kaydı bulun ve seçin.
9. Satırlar seçeneğini tıklatın.
10. Fiş'e tıklayın.
11. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]