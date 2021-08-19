---
title: Personel saat ve işe devam için bordro işlemini etkinleştirme
description: Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39f3495f23ece2ea6989c3a6d74e8694789ea8dd1ae663fad85143c327cde407
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726741"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Personel saat ve işe devam için bordro işlemini etkinleştirme

[!include [banner](../../includes/banner.md)]

Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>İlgili ödeme oranıyla ödeme türü oluşturma
1. Saat ve işe devam > Kurulum > Bordro > Ödeme türleri
2. Yeni'ye tıklayın.
3. Ödeme türü alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Kaydet'e tıklayın.
6. Oranlar'a tıklayın.
    * Ödeme türleri için oranlar belirli zaman aralıkları için ayarlanır ve çalışanlar için bireysel oranlar oluşturulabilir. Saat ve işe devamdaki ödeme türleri için oran oluşturmak her zaman gerekli değildir. Bu bilgi, ücretleri oluşturmak için kullanılan bordro sisteminde bulunabilir.  
7. Yeni'ye tıklayın.
8. Listede, seçili satırı işaretleyin.
9. Oran alanına bir sayı girin.
10. Kaydet'e tıklayın.

## <a name="create-a-pay-agreement"></a>Ödeme anlaşması oluşturma
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Ödeme anlaşmalarına gidin.
    * Saat ve işe devam > Kurulum > Ödeme anlaşmaları  
4. Yeni'ye tıklayın.
5. Ödeme anlaşması alanına bir değer girin.
6. Açıklama alanına bir değer girin.
7. Kaydet'e tıklayın.
8. Anlaşma satırlarına tıklayın.
9. Yeni'ye tıklayın.
10. Listede, seçili satırı işaretleyin.
11. Profil türü alanına bir değer girin veya buradan bir değer seçin.
12. Ödeme türü alanına bir değer girin veya buradan bir değer seçin.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Süre ve kayıtlı çalışan için ödeme anlaşması ayarlama
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Zaman kayıtlı çalışanlar'a gidin.
    * Saat ve işe devam > Kurulum > Zaman kayıtlı çalışanlar  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. İstihdam sekmesine tıklayın.
6. Zaman kaydı bölümünü genişletin.
7. Düzenle öğesine tıklayın.
8. Ödeme anlaşması alanına bir değer girin veya buradan bir değer seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]