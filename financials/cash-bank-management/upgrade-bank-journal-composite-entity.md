---
title: "Banka günlüğü birleşik varlığını güncelleştirme"
description: "Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı&quot;na eklemek için aşağıdaki adımlar gereklidir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 364bdff8f8d825cc50760631bb533b531f8b2121
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Banka günlüğü birleşik varlığını güncelleştirme

[!include[banner](../includes/banner.md)]


Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir.

Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımları kullanın.

1.  Aşağıdaki banka günlüğü birleşik varlıklarını, varlıkları ve aşamalandırma tablolarını derleyin ve eşitleyin:
    -   Birleşik Varlık\\BankaGünlükVarlığı
    -   Varlık\\BankaGünlüğüBaşlıkVarlığı
    -   Varlık\\BankaGünlüğüSatırVarlığı
    -   Tablo\\BankaGünlüğüBaşlıkHazırlığı
    -   Tablo\\BankaGünlüğüSatırHazırlığı

2.  Veri yönetimi\\veri projeleri
    -   **Kaynak Veri**yerleşiminde **Banka Hareketi**türünü gösterin.
        -   Kaynak veri biçimi = XML Öğesi
        -   Varlık adı = Banka Günlüğü
        -   Yükleme veri dosyası = yeni sürüm ÖrnekBankaGünlüğüBirleşikVarlığı.xml
        -   Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.
        -   Eşlemeyi sıfırdan oluşturmak için **Evet**'e tıklayın.
        -   Banka Hareketi Türü'nün eşleştiğini doğrulayın.
            -   Satır varlığında **Haritayı görüntüle**'ye tıklayın.
            -   Banka Hareket Türü'nün Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.

3.  Yeni ekstreyi içe aktarın.





