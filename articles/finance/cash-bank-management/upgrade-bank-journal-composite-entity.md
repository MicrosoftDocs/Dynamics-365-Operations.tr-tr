---
title: Banka günlüğü birleşik varlığını güncelleştirme
description: Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd6a1f9d7ba36e591d7e558956297781c346635c30c10d588c0dbe6d73301030
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733065"
---
# <a name="update-the-bank-journal-composite-entity"></a>Banka günlüğü birleşik varlığını güncelleştirme

[!include [banner](../includes/banner.md)]

Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir.

Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımları kullanın.

1.  Aşağıdaki banka günlüğü birleşik varlıklarını, varlıkları ve aşamalandırma tablolarını derleyin ve eşitleyin:
    -   Birleşik Varlık\\BankaGünlükVarlığı
    -   Varlık\\BankaGünlüğüBaşlıkVarlığı
    -   Varlık\\BankaGünlüğüSatırVarlığı
    -   Tablo\\BankaGünlüğüBaşlıkHazırlığı
    -   Tablo\\BankaGünlüğüSatırHazırlığı

2.  Veri yönetimi\\veri projeleri
    -   **Kaynak Veri** yerleşiminde **Banka Hareketi** türünü gösterin.
        -   Kaynak veri biçimi = XML Öğesi
        -   Varlık adı = Banka Günlüğü
        -   Yükleme veri dosyası = yeni sürüm ÖrnekBankaGünlüğüBirleşikVarlığı.xml
        -   Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.
        -   Eşlemeyi sıfırdan oluşturmak için **Evet**'e tıklayın.
        -   Banka Hareketi Türü'nün eşleştiğini doğrulayın.
            -   Satır varlığında **Haritayı görüntüle**'ye tıklayın.
            -   Banka Hareket Türü'nün Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.

3.  Yeni ekstreyi içe aktarın.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]