---
title: Müşterinin ileri tarih atılmış çekini kapatma
description: Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e61ac6d6785dd0383d5e5dcaca4cc55bf6deb52
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780028"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Müşterinin ileri tarih atılmış çekini kapatma

[!include [banner](../../includes/banner.md)]

Çek, banka tarafından tahsil edildikten sonra vadeli çek kapatılabilir. Bu mali işlem ayrıca vadeli çek için köprü hesabı hareketini de kapatmaktadır. 

Buna başlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir.

1) İleri tarih atılmış çekleri ayarlama

2) Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme 



Bu görevin rolü Haznedar'dır.



Bu yordam, USMF demo şirketini kullanır.

1. **Kredi ve Tahsilatlar > Sorgular ve raporlar > Ödemeler > Müşteri vadeli çekleri** seçeneğine gidin.
2. **Kapatma**'ya tıklayın.
3. **Kliring girişlerini kapat**'a tıklayın.
    * Çek hareketi için müşteri hesabını kapatın.  
4. Sayfayı kapatın.
5. **Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.
6. **Göster** alanında, bir seçenek seçin.
7. **Sadece kullanıcı tarafından oluşturulmuş** onay kutusunu temizleyin veya seçin.
8. Listede, istenen kaydı bulun ve seçin.
9. **Satırlar**'a tıklayın.
10. **Fiş**'e tıklayın.
11. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
