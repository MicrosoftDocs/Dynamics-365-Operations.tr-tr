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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f8f2f8fe0dfd0eccd61ef76242e2a77c75b3983
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976253"
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