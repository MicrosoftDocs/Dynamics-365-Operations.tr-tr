---
title: Üretim emrini başlatma
description: Bu yordam, üretim emirlerinin atölyede nasıl başlatılacağını gösterir.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa47510d84e5ee156d4f38a076ce17fad8359d147997349de023b64483d66160
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735147"
---
# <a name="start-a-production-order"></a>Üretim emrini başlatma

[!include [banner](../../includes/banner.md)]

Bu yordam, üretim emirlerinin atölyede nasıl başlatılacağını gösterir. Bu işlemde, zaman ve malzeme tüketimi bildirilir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu, üretim emri ömrünü açıklayan yedi yordamdan beşincisidir.


## <a name="start-a-production-order"></a>Üretim emrini başlatma
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
    * Serbest bırakılmış durumunda olan bir üretim emrini seçin.  
2. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
3. Başlat'a tıklayın.
    * Bu sayfada, üretim emrinin başlatılmasını onaylayabilirsiniz.  
4. Genel sekmesine tıklayın.
5. Operasyon Numarası Hayır. alanına '10' girin.
6. Otomatik rota tüketimi alanında, 'Her zaman' seçin.
7. Nakletme Rota kartını şimdi onaylayın kutusunu tıklatın.
8. Otomatik malzeme listesi tüketimi alanında, 'Her zaman' seçin.
9. Malzeme çekme listesini şimdi naklet kutusunu tıklatın.
10. Malzeme çekme listesini yazdır kutusunu tıklatın.
11. Tamam'a tıklayın.
    * Bu, üretim emri için kullanılan malzemeleri gösteren yazılı malzeme çekme listesidir.  
12. Sayfayı kapatın.

## <a name="validate-the-picking-list"></a>Malzeme çekme listesini doğrulayın
1. Eylem Bölmesinde, Görüntüle öğesine tıklayın.
2. Malzeme çekme listesi'ni tıklatın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Düzenle öğesine tıklayın.
6. Tüketim alanına bir sayı girin.
7. Deftere Naklet öğesine tıklayın.
8. Tamam'a tıklayın.
    * Üretim emri tarafından tüketilen malzemeler, malzeme çekme listesi günlüğü defterine nakledilir. Günlüğü deftere nakletmeden önce, tahmin edilen miktar ve gerçek tüketilen miktar arasında bir fark varsa gerekli ayarlamaları yapabilirsiniz.  
9. GridPanel sekmesini tıklatın.
10. Sayfayı kapatın.

## <a name="verify-the-route-card-journal"></a>Rota kartı günlüğünü doğrulayın
1. Eylem Bölmesinde, Görüntüle öğesine tıklayın.
2. Rota kartı'nı tıklatın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Düzenle öğesine tıklayın.
6. Saatler alanına bir sayı girin.
7. Deftere Naklet öğesine tıklayın.
8. Tamam'a tıklayın.
    * Tekil operasyonlar için harcanan zaman rota kartı günlüğünde kaydedilir. İyi ve hata miktarı da bildirilebilir.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]